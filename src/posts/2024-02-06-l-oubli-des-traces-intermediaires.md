---
title: "L'oubli des traces intermédiaires"
date: 2024-02-06
---

## Introduction

Lors du chapitre précédent, nous avons examiné à travers le cas d'étude Stylo
la première phase d'une chaîne éditoriale savante qu'est la saisie d'un texte.
En nous concentrant sur l'élaboration du document, élément au coeur du
traitement des informations, nous avons opté pour une méthodologie qualitative
d'observation des médiations à l'oeuvre pour en comprendre la construction, à
l'instar de ce que F. Kittler proposait dans ces travaux. 
Pour mener à bien cette étude nous nous sommes affranchis de la page qui, en
tant qu'élément graphique affiché à l'écran, cache et invisibilise les
opérations d'écriture réalisées par la machine.
Ainsi nous avons pu mettre en lumière les différentes formes de document par
lesquelles passe un texte saisi dans l'éditeur de texte Stylo, au nombre de
quatre, dont trois sont écrites par Stylo et une par l'auteur.
Dès lors, ceci nous a permis d'affirmer qu'il y a une co-construction du
document, que l'on peut considérer comme la source utilisée par une chaîne
éditoriale, entre l'environnement numérique d'écriture et l'auteur.  

Toutefois, ce document source n'est pas publiable en l'état.
En effet, qu'une chaîne d'édition soit orientée vers la publication imprimée ou
vers la publication numérique, les formats dans lesquels les textes
sont saisis ne sont pas adaptés à ces objets publiés.
Dans la plupart des cas de figure, les documents sources fournis par les auteurs
sont dans des formats provenant des traitements de texte (ODT pour LibreOffice,
DOCX pour MS Word, PAGES pour Pages, etc.) ou encore en texte brut (par exemple
Markdown) alors que sont préférés les formats PDF pour les impressions et HTML
pour les objets numériques (vers des sites web ou des ePUB). 

L'action suivant l'écriture consiste alors à transformer et adapter le contenu
textuel de la source à l'objet que l'on souhaite rendre public, tout en
respectant un certain nombre de règles éditoriales selon le type d'objet à
produire, que ce soit pour aboutir à un objet imprimé ou numérique, et des
politiques éditoriales en vigueur dans les maisons d'édition ou les revues
savantes concernées.
Cette transformation, que pour l'instant nous pouvons associer à des changements
de formats, procède à des modifications du texte original pour qu'il soit
adapté à l'objet désiré.
Ce faisant, la transformation réécrit intégralement le document pour en générer
un nouveau qui n'est plus le document source et cela au détriment d'une partie de
l'écriture initiale qui doit disparaître et ne sera, ce faisant, jamais publiée.

Dans ce troisième chapitre, nous démontrons qu'en effaçant des traces de
l'écriture du document source, ces transformations suppriment et cachent une
partie de cette intimité produite par le couple humain machine durant l'action
d'écriture.
Nous nous appuierons sur des cas concrets de transformations de textes du
livre nativement numérique, _Contribution numérique : cultures et savoirs_
réalisés avec le générateur de livre statique _Le Pressoir_ en nous appuyant sur
la même méthodologie de recherche que pour le chapitre précédent.


## Plan

1. Les traces numériques
    - définir trace numérique et leur lien avec l'intime
    - production de documents et désintéressement des fichiers temporaires ou
      des écrits de la machine (ex: pour la fouille de texte des archives du web
on supprime le bruit)
    - effacement et oubli des traces intimes (_parsing = action d'effacer ?_)
2. Introduire les chaîne éditoriales 
    - revue de litt sur des chaines numériques
    - fabrique de l'édition
3. Les transformations et les conversions
    - définir ces termes
    - le single source publishing
    -  Les AST
        - origine de cet objet
        - utilisation pour du texte
        - Introduire AST Pandoc
        - Introduire Living paper
4. Cas d'étude
    - livre contribution numérique
    - le pressoir
    - Pandoc
        - détailler AST
    - AST des documents produits
    - Comparaison si passage dans Stylo des mêmes textes pour produire des XML
      COMMONS et des HTML ?

## Notes


Dans cette partie sont traitées les écritures intermédiaires que l'on trouve
entre la source rédigée et l'objet final produit.
Bien souvent, à l'intérieur d'une chaîne éditoriale, le texte produit par un
auteur est dans une forme brute.
Ce texte doit subir une série de transformations (allant de une à plusieurs)
pour produire les éléments finaux : des fichiers au format PDF à imprimer, des
version HTML pour les ePubs ou pour un site web, ou encore des documents au
format XML.

Les transformations d'un format vers un autre ne se déroulent pas par magie, et
l'ordinateur ne "connait" pas les équivalences entre les syntaxes de chaque format.

Pour cela, il faut établir des règles pour formaliser ces équivalences, quand
cela est possible.
Parfois, cela n'est pas possible car ce qui existe dans un format n'existe pas
dans un autre, et il faut alors trouver des solutions alternatives pour
contourner ces problèmes.

Nous avons vu que le format Markdown était un langage de balisage léger pensé en
lien avec le format HTML, de cette manière un `## titre de niveau 2` déclaré en
Markdown peut être transformé en `<h2>titre de niveau 2 </h2> en HTML`.

Ce que l'on remarque c'est que la structure rédigée dans la source est supprimée
-- et oubliée -- pour laisser la place à une structure rédigée par la machine.
Dans certains peuvent se retrouver différents formats intermédiaires, entre la
source et le produit fini, qui sont quasiment invisibles et dont on ne retient
rien, et qui pourtant participé à cette destructuration/restructuration du
document.

Par exemple pour produire un document PDF depuis une source au format Markdown
il faut utiliser un document intermédiaire comme une transformation au format
TeX avant de pouvoir produire le fichier PDF.
Cette transformation LaTeX est temporaire, elle peut être préservée pour
vérification, mais n'est jamais archivée.

Deux transformations sont effectuées dans cet exemple, et deux structurations de
contenus disparaissent.

Note : revenir dans le chapitre sur les archives sur l'oubli de ces traces
structurelles.

Si un auteur.e saisit `##` ce n'est pas la même chose que `<h2>`.
Même si les deux éléments peuvent être lu de la même manière (ceci est un titre
niveau deux), dans un cas il s'agit d'un titre de niveau deux en Markdown et
dans l'autre un titre de niveau 2 en HTML.

Il y a donc une énorme différence sémantique puisque l'une des balises dépend
des spécifications d'un format et la deuxième d'un autre : ce ne sont pas les
mêmes signes qui sont inscrits dans la matière et ils ne se lisent pas de la
même façon.

Or nous observons la disparition de ces signes lors des transformations des
documents alors que ces signes sont pourtant différents.

La machine réécrit le texte et le restructure pour qu'il soit interprétable dans
des environnements autres.
En faisant cela, elle supprime une partie de l'architexte de la source ou du
fichier intermédiaire pour qu'il soit conforme à ce nouvel environnement.
Il y a donc un effacement de l'architexte en creux de la réécriture par la
machine.

Les questions que nous pouvons nous poser relèvent de la sélection de
l'architexte du produit final (politique éditoriale) et de la différence qu'il
existe entre la source et l'objet transformé ?

Le livre Contribution numérique ... sera étudié pour illustrer l'oubli de ces
traces intermédiaires.

Montrer l'arbre abstrait syntaxique de Stylo et celui du Pressoir avec la base
commune md, yaml, bibtex + pandoc et montrer que les output ne sont pas les
mêmes, que malgré les différences dans l'arborescence en fin de chaine
éditoriale, le sens produit diffère ...

## Les chaînes éditoriales

## Les traces numériques

## Les transformations et les conversions

## Conclusion
