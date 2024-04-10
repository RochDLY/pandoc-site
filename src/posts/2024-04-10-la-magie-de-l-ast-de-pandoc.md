---
title: "La magie de l'AST de Pandoc"
date: 2024-04-10
subtitle: "Nouvel essai pour intégrer ekdosis dans stylo"
---

## Nouvel essai pour intégrer ekdosis dans Stylo

Les scripts peuvent être retrouvés sur [ce dépôt
gitlab](https://gitlab.huma-num.fr/ecrinum/stylo/ekdosis4stylo/-/tree/master/test_lua-filter?ref_type=heads)

### Fonctionnement

Dans ce dossier nous trouvons une autre méthode pour intégrer ekdosis à Stylo.

Pandoc interprète les balises LaTeX lorsqu'elle se trouvent dans des documents
en Markdown.

Pour observer cette interprétation, il faut aller regarder ce qu'il se passe
dans l'AST du document, auquel on accède par la commande suivant :

`pandoc -f markdown -t native sample.md --lua-filter=style-tex.lua -s -i`

On y trouve la chose suivante : `RawInline (Format "tex") "\\emph{emphase}"`.

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

Cette information est déclarée dans sample.md :

```yaml
---
title: "Test 1"
header-includes: |
    \usepackage{ekdosis}
---
```

Elle est bien traduite dans l'AST dans le bloc des métadonnées par : 

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
dans le document `\begin{ekdosis}` et `\end{ekdosis}.

Les ajouter manuellement dans le Markdown perdrait l'intérêt de l'utilisation du
Markdown (autant tout faire en LaTeX sinon).
L'idée en cours de test est de rendre ces balises discrètes en utilisant un
filtre LUA où une division en Markdown (inline ou en block) associée à la classe
`variant` ajoute les balises autour du paragraphe où ekdosis est employé.

C'est ce que l'on retrouve dans le filtre `style-tex.lua`.

### Commandes

Pour produire le pdf, utiliser la commande suivante : 

```sh
pandoc sample.md -o sample.pdf -s -i --pdf-engine=lualatex --lua-filter=style-tex.lua
```

### Erreurs

Actuellement, le PDF produit comporte des erreurs puisque l'appareil critiques
avec les variantes ne sont pas affichés en bas de page. Il faut certainement
corriger le filtre LUA.

Affaire à suivre
