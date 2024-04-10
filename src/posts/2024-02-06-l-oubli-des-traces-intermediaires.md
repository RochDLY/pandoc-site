---
title: "L'oubli des traces intermédiaires"
date: 2024-02-06
---

## Résumé

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

## Plan

1. Introduire les chaîne éditoriales 
    - revue de litt sur des chaines numériques
    - fabrique de l'édition
2. Les transformations et les conversions
    - définir ces termes
    - le single source publishing
3. Les AST
    - origine de cet objet
    - utilisation pour du texte
4. Cas d'étude
    - livre contribution numérique
    - le pressoir
    - Pandoc
        - détailler AST
    - AST des documents produits
    - Comparaison si passage dans Stylo des mêmes textes pour produire des XML
      COMMONS et des HTML


## Introduction

Dans le chapitre précédent nous avons décrit les étapes d'écriture d'un texte dans Stylo et l'obtention d'une source séparée en trois documents : Markdown, YAML et BiBTeX.
Toutefois, à l'instar d'un document rédigé dans le format docx, aucune publication n'existe directement dans ce format.
Que ce soit pour un dépôt dans HAL (souvent au format PDF) ou une publication sur Cairn, OpenEdition ou Érudit, les documents sont publiés dans d'autres formats : XML, HTML, ePUB, PDF, etc.
