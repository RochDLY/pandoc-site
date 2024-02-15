---
title: '`ekdosis` et Stylo'
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
_Work in progress_ (je reviendrai sur cette section lorsque nous aurons avancé
sur son cahier des charges !)
