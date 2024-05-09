---
title: 'Créer un nouvel export dans Stylo compatible avec `ekdosis`'
date: 2024-02-15
---

## Avant-propos

Ce billet est l'occasion d'écrire sur les différents échanges auquel j'ai
participé pour essayer de définir les besoins d'écriture en matière d'édition
critique.
Les éditions critiques se munissent d'appareil critique au sein du texte\ : ce
sont des notes particulières dans lesquelles les auteur.e.s insèrent des
commentaires, des variantes, etc.. bref toute leurs recherche.

En somme, les textes critiques sont très particuliers et ont besoin d'une
structure spécifique et très précise.
Pour répondre à ce besoin, on pense tout de suite à du `xml`.
Cependant, écrire dans différentes langues (parfois mortes), en navigant dans
plusieurs manuscrits et notes, complexifie largement le processus d'écriture
surtout lorsqu'il faut en plus penser la syntaxe `xml` avec les bonnes balises
et la bonne indentation.
Et puis tous les philologues ne sont pas adeptes des technologies `xml`.

Dans ce paysage se dressent deux voies principales pour éditer ce type de
texte\ :

- logiciel de traitement de texte (avec un système de notes), tout repose sur le
  travail d'un.e éditeur.ice.
- encodage du texte en `xml`, ce qui permet de parser les contenus
automatiquement dans la suite du traitement des textes.

Dans un cas comme dans l'autre, l'environnement de travail n'est pas
satisfaisant.

Une solution alternative serait l'usage de LaTeX et du paquet [`ekdosis`](http://www.ekdosis.org/)
développé présicément dans ce but (mis en production en 2020) par Robert Alessi.

R. Alessi préconise l'emploie d'`ekdosis` dans l'éditeur de texte `emacs` (un
éditeur dans le terminal).
LaTeX se trouve à mi-chemin entre les deux solutions mentionnées précédemment
(parce qu'il permet à la fois de structurer les informations mais aussi de les
mettre en page).

Le seul *hic* de cette solution est qu'elle ne permet pas le travail
collaboratif synchrone.
En effet, on pourrait imaginer un travail mener sur une instance de git en ligne
pour gérer les textes en différé.

Cependant, cela nécessite un apprentissage supplémentaire, une autre technologie
à prendre en main ... et ça ne résoud pas le travail synchrone à distance.

## `ekdosis` et Stylo

Pour répondre à ce besoin, une idée serait d'intégrer `ekdosis` à Stylo.
Plusieurs possibilités se présentent à nous pour réaliser cela : 
- tordre un peu le Markdown et adapter sa syntaxe pour faire rentrer tout
l'appareil critique dedans (et on obtient ainsi un balisage plus léger que `xml` ou `LaTeX`).
- modifier le format source de Stylo et remplacer le Markdown par LaTeX.

### Première option

La première option a été prototypée par MVR en utilisant la syntaxe suivante\ :

```md
Cette fois, nous passons à un texte [[édité][Robert: critique]], avec des variantes.
Je demande à `ekdosis` de ne passer en `TEI xml` que [[cette portion][Roch: ce fragment]] du texte. 
```
Cette syntaxe en Markdown n'est pas valide, il faut ensuite la parser avec un script
particulier pour la transformer de la même manière qu'`ekdosis` (on peut
imaginer un filtre python intégré à la commande Pandoc).
Le principal défaut de cette notation est qu'elle tord trop le fonctionnement du
Markdown : ce n'est pas une notation interopérable avec d'autres écosystèmes.
Le second défaut est qu'elle n'intègre pas ekdosis mais le recopie: il faut donc
redévelopper tout ce que fait `ekdosis` dans Stylo pour obtenir un comportement
similaire.

### Deuxième option

*Mise à jour effectuée le 09 mai 2024.*

#### Fonctionnement

Pour réaliser un export vers pdf et xml-tei [ekdosis](http://www.ekdosis.org/),
la méthode la plus élégante consiste à intégrer ekdosis à Stylo.

Nous avons déjà presque toutes les technologies à disposition (puisque Pandoc
utilise TeXlive pour compiler les pdf). 

Pandoc interprète les balises LaTeX lorsqu'elle se trouvent dans des documents
en Markdown.

Pour observer cette interprétation, il faut aller regarder ce qu'il se passe
dans l'AST du document, auquel on accède par la commande suivant :

`pandoc -f markdown -t native sample.md --lua-filter=style-tex.lua -s -i`

On y trouve la chose suivante (voir sample.md plus bas) : `RawInline (Format
"tex") "\\emph{emphase}"`.

Au milieu d'un paragraphe (`Para`), Pandoc parse correctement le latex et le
reconnait sous sa forme brute dans un élément _inline_.

Lors d'une transformation en PDF, l'emphase déclarée en latex dans le markdown
sera bien interprétée.

Pour ce qui concerne l'intégration d'ekdosis dans du Markdown nous avons besoin
d'un élément supplémentaire.
Par précaution, il vaut mieux indiquer le package utilisé que l'on déclare
normalement dans le préambule d'un document LaTeX.

Pandoc accepte cette information si elle est indexée dans une en-tête YAML du
document Markdown sous la clef `header-includes`.

Cette information est déclarée par exemple dans un fichier sample.md :

```md
---
title: "Test 1"
header-includes: |
    \usepackage[teiexport]{ekdosis}
---

##  Test de LaTeX inline

Ceci est un paragraphe en Markdown.

Ceci est un paragraphe md avec une \emph{emphase} en latex.

## Test de blocs

::: variant
I met my friend \app{
    \lem{Peter}
    \rdg{John}
    } at the station yesterday.
:::

::: variant
I met my friend \app{
    \lem{Robert}
    \rdg{Roch}
    } at the station yesterday.
:::

```

L'en-tête est bien traduite dans l'AST dans le bloc des métadonnées par : 

```
Meta
    { unMeta =
        fromList
          [ ( "header-includes"
            , MetaBlocks
                [ RawBlock (Format "tex") "\\usepackage{ekdosis}" ]
            )
          , ( "title" , MetaInlines [ Str "Test" , Space , Str "1" ] )
          ]
    }
```

Avec ceci nous sommes presque prêt à utiliser ekdosis dans Stylo (en préservant
la
syntaxe ekdosis et le traitement par le compilateur LuaLaTeX tels qu'ils ont été
pensés par R. Alessi).

Pour fonctionner il manque un élément, la balise indiquant l'emploie d'ekdosis
dans le document `\begin{ekdosis}` et `\end{ekdosis}`.

Les ajouter manuellement dans le Markdown perdrait l'intérêt de l'utilisation du
Markdown (autant tout faire en LaTeX sinon).
L'idée est de rendre ces balises discrètes en utilisant un
filtre LUA où une division en Markdown (inline ou en block) associée à la classe
`variant` ajoute les balises autour du paragraphe où ekdosis est employé.

C'est ce que l'on peut obtenir avec le filtre suivant:

```lua
function Div (element)
    if element.classes[1] == 'variant' then
        return {
            pandoc.RawInline('tex', '\\begin{ekdosis}'),
            element,
            pandoc.RawInline('tex', '\\end{ekdosis}'),
        }
    end
end
```

#### Commandes

Pour produire le pdf, utiliser les commandes suivantes : 

```sh
pandoc sample.md -o sample.pdf -s -i --pdf-engine=lualatex
--lua-filter=style-tex.lua

## La commande ci-dessus ne fonctionne pas, voir explication

## Faire les commandes suivantes:

pandoc sample.md -o sample.tex -s --lua-filter=style-tex.lua

lualatex sample.tex

lualatex sample.tex

lualatex sample.tex
```
Compiler le Markdown avec Pandoc (et le compilateur lualatex) fonctionne pour
produire un PDF mais ne fonctionne pas avec ekdosis.

La raison est assez simple : ekdosis a besoin de compiler le fichier tex 3 fois
pour produire le pdf. La première fois il génère l'appareil critique dans un
fichier temporaire `sample.ekd`, la deuxième fois il opère des calculs pour
numéroter les lignes et la troisième fois il génère le document PDF
correctement.

Le problème rencontré avec Pandoc est que ce dernier ne prend pas en charge de
fichier extérieur, excepté les filtres et les templates. Du coup, même si on
recompile 3x depuis Pandoc, l'appareil critique présent dans `sample.ekd` ne
sera pas pris en compte.

Le plus simple est alors de produire le fichier tex avec Pandoc puis de compiler
le tex en PDF en appelant lualatex 3 fois.

#### Dépendances

Attention, la version de TeXlive installée sur stylo export est une version
allégée.
Un certain nombre de dépendances sont nécessaires pour faire fonctionner ekdosis
et devront être ajoutées. 

Voici la liste des dépendances d'ekdosis : 

```
ekdosis-dependencies/ekdosis-dependencies.tex
tex/lualatex/ekdosis/ekdosis.sty
texlive/2024/texmf-dist/tex/generic/etexcmds/etexcmds.sty
texlive/2024/texmf-dist/tex/generic/expkv-bundle/expkv-def.tex
texlive/2024/texmf-dist/tex/generic/expkv-bundle/expkv-pop.tex
texlive/2024/texmf-dist/tex/generic/expkv-bundle/expkv.tex
texlive/2024/texmf-dist/tex/generic/iftex/ifluatex.sty
texlive/2024/texmf-dist/tex/generic/iftex/iftex.sty
texlive/2024/texmf-dist/tex/generic/infwarerr/infwarerr.sty
texlive/2024/texmf-dist/tex/generic/kvdefinekeys/kvdefinekeys.sty
texlive/2024/texmf-dist/tex/generic/ltxcmds/ltxcmds.sty
texlive/2024/texmf-dist/tex/generic/pdftexcmds/pdftexcmds.sty
texlive/2024/texmf-dist/tex/latex/auxhook/auxhook.sty
texlive/2024/texmf-dist/tex/latex/base/article.cls
texlive/2024/texmf-dist/tex/latex/base/size10.clo
texlive/2024/texmf-dist/tex/latex/base/ts1cmr.fd
texlive/2024/texmf-dist/tex/latex/etoolbox/etoolbox.sty
texlive/2024/texmf-dist/tex/latex/expkv-bundle/expkv-def.sty
texlive/2024/texmf-dist/tex/latex/expkv-bundle/expkv-opt.sty
texlive/2024/texmf-dist/tex/latex/expkv-bundle/expkv-pop.sty
texlive/2024/texmf-dist/tex/latex/expkv-bundle/expkv.sty
texlive/2024/texmf-dist/tex/latex/float/float.sty
texlive/2024/texmf-dist/tex/latex/graphics/keyval.sty
texlive/2024/texmf-dist/tex/latex/ifoddpage/ifoddpage.sty
texlive/2024/texmf-dist/tex/latex/kvoptions/kvoptions.sty
texlive/2024/texmf-dist/tex/latex/kvsetkeys/kvsetkeys.sty
texlive/2024/texmf-dist/tex/latex/l3backend/l3backend-luatex.def
texlive/2024/texmf-dist/tex/latex/lineno/lineno.sty
texlive/2024/texmf-dist/tex/latex/paracol/paracol.sty
texlive/2024/texmf-dist/tex/latex/refcount/refcount.sty
texlive/2024/texmf-dist/tex/latex/snapshot/snapshot.sty
texlive/2024/texmf-dist/tex/latex/trivfloat/trivfloat.sty
texlive/2024/texmf-dist/tex/latex/zref/zref-abspage.sty
texlive/2024/texmf-dist/tex/latex/zref/zref-base.sty
texlive/2024/texmf-dist/tex/latex/zref/zref-user.sty
texlive/2024/texmf-dist/tex/lualatex/luacode/luacode.sty
texlive/2024/texmf-dist/tex/luatex/ctablestack/ctablestack.sty
texlive/2024/texmf-dist/tex/luatex/luatexbase/luatexbase.sty
```
