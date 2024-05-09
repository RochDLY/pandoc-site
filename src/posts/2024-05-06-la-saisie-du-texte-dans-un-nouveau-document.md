---
title: "La saisie du texte dans un nouveau document"
date: 2024-05-06
---

## Introduction

Lors du chapitre précédent, nous avons défini l'*intimité du
chercheur* comme le résultat produit par les écrits savants, parmi
lesquels nous retrouvons les publications scientifiques qui sont l'objet de
notre recherche.
Ces publications scientifiques peuvent être assimilées à des documents
numériques, soit un espace délimité dans lequel sont organisées des informations
selon des normes établies par les impératifs technologiques d'une chaîne
éditoriale, par exemple avec des protocoles de communication des documents ou
encore des formats.
Dans cette chaîne, la réalisation d'un document nécessite ainsi des interactions
entre une multitude d'agents, qu'ils soient numériques ou humains, pour advenir.
À chacune des étapes de sa constitution, ces interactions entre les agents
laissent des traces à l'intérieur du document que nous considérons comme des
traces de cette intimité du chercheur.
Ces traces sont des indices d'une intimité passée et donc de la matérialité de
cette dernière. 

Avec ce chapitre, nous commençons à détailler la relation qu'entretiennent un
auteur et un ordinateur dans l'acte d'écriture scientifique dans un environnement
numérique^[À chaque fois que nous ferons référence à l'écriture, il faudra
la comprendre comme l'écriture scientifique en environnement numérique sauf
mention différente.].

Ce dispositif que nous venons de décrire fait écho aux théories de
l'éditorialisation [@vitali-rosati_editorialization_2018] et de
l'énonciation éditoriale [@souchier_image_1998].
Ainsi, cette écriture numérique n'est plus définie en tant que
fruit d'une seule fonction auctoriale, mais l'est par un ensemble de fonctions
éditoriales dont la fonction auctoriale fait partie.

Selon ce dispositif, et puisque notre hypothèse positionne l'intime en tant que
produit de l'écriture, nous pouvons nous demander quelle est la contribution de
l'environnement d'écriture à cet intime lors de la saisie d'un nouveau
document.

Ainsi, parmi toutes les fonctions éditoriales que l'on pourrait énumérer, nous nous
intéressons dans ce chapitre à la saisie d'un texte et à l'environnement support
[@zacklad_organisation_2012] dans lequel il s'inscrit.

Une première partie sera dédiée à montrer les rouages de l'écriture numérique
en mettant en lumière le système de communication entre humain et machine à
l'aide des logiciels se trouvant à l'interface entre les deux.

Nous nous appuyons sur les particularités de l'écriture numérique
[@bouchardon_lecriture_2014; @crozat_ecrire_2016;  @souchier_numerique_2019] et
sur le fonctionnement de la machine pour illustrer, dans une deuxième partie,
le rôle de médiation joué par les logiciels -- entendu comme une suite
d'instructions écrites -- entre la saisie du texte au clavier et les
traitements appliqués à ces informations, jusqu'à leur stockage dans une mémoire
informatique. 

Tandis que chaque environnement a ses propres modalités d'écriture que nous ne
pouvons pas toutes énumérer, nous étudions dans la deuxième partie de ce
chapitre l'éditeur de texte sémantique Stylo et les différentes représentations
du texte qu'il génère. Ces représentations intermédiaires circulent entre les
espaces de Stylo -- client et serveur -- par différents canaux et protocoles
pour former, à travers une série de documents produits, une dynamique
constitutive du sens de l'écriture [@merzeau_editorialisation_2013] propre à cet
environnement.

Stylo est un éditeur de texte sémantique en ligne développé pour l'édition
savante en sciences humaines et sociales (SHS) et en lettres.
Stylo est autant un projet de recherche qu'un outil d'écriture et d'édition, qui
entend poser une question décisive : qu'est-ce qu'écrire en environnement
numérique en SHS ?

C'est un outil libre et _open source_ conçu en 2017 par la Chaire de recherche
du Canada sur les écritures numériques (CRCEN) [@vitali-rosati_ecrire_2020], et
soutenu depuis 2020 par les Très grande infrastructure de recherche Huma-Num.
Guillaume Grossetie et Thomas Parisot, tous deux développeurs, maintiennent et
développent l'infrastructure technique de Stylo avec la CRCEN depuis plusieurs
années, équipe dans laquelle je suis fortement impliqué depuis le début de
l'année 2022.

Stylo a pour objectif de transformer le flux de travail numérique des revues
savantes en SHS.
En tant qu'éditeur de texte sémantique WYSIWYM, il vise à améliorer la chaîne de
publication académique [@kembellec_lerudition_2020], tout en invitant à une
réflexion théorique et pratique sur nos façons d'écrire et d'éditer.

Prendre le contrôle de son propre texte, voilà ce que permet aujourd'hui Stylo à
travers plusieurs fonctionnalités fondatrices ou toutes nouvelles -- depuis la
version 3.0 -- qui s'inscrivent dans le domaine des technologies de l'édition
numérique [@blanc_technologies_2018] : balisage du texte pour une structure
sémantique fine, import de données bibliographiques structurées depuis
l'application Zotero, mot-clés contrôlés depuis plusieurs ontologies,
prévisualisation avec la possibilité d'annoter avec Hypothesis, génération de
plusieurs formats (HTML, PDF, XML ou DOCX), export respectant les standards de
l'édition scientifique, fonctions avancées de rechercher-remplacer, édition
collaborative simultanée, accès aux données via une API GraphQL, etc.
Contrairement aux outils de traitement de texte tels que Microsoft Word ou
LibreOffice, Stylo cherche à promouvoir et à encourager l'utilisation de
standards ouverts.

Au coeur de Stylo ce sont donc les formats de balisage Markdown, de
sérialisation de données YAML ou encore de structuration de références
bibliographiques BibTeX qui offrent la possibilité de produire plusieurs formats
de sortie depuis une source unique.
Stylo suit donc le principe de _single source publishing_
[@fauchie_fabriquer_2024].
Pandoc, le « couteau suisse de l'édition », génère les formats de sortie PDF
(avec l'aide de LaTeX), HTML, XML-TEI ou encore DOCX.

Le choix d'étudier Stylo comme terrain pour cette recherche découle de plusieurs
raisons.
Tout d'abord, il s'agit d'un éditeur moderne construit avec les technologies du
Web les plus récentes.
Cet environnement Web suscite un certain engouement auprès des utilisateurs,
notamment pour sa capacité à offrir un espace de travail collaboratif en temps
réel leur permettant d'écrire à plusieurs dans cet espace.
La deuxième raison qui fait de Stylo un terrain opportun est l'accessiblité de
son code source.
Contrairement à d'autres éditeurs propriétaires comme l'est GoogleDoc, la
totalité du code de Stylo est disponible en ligne, ce qui est indispensable pour
notre étude.
Enfin, le fait d'être impliqué dans les développements de Stylo depuis plus de
deux ans m'offre une position privilégiée pour étudier cet éditeur puisque j'ai
accès aux différentes phases de tests des développements, me permettant ainsi
d'observer le comportement des nouvelles fonctionnalités et de les modifier.
Grâce à cette position, j'ai également un accès direct à la communauté
d'utilisateurs, s'élevant à un peu plus de 6000 personnes fin 2023 pour plus de
40000 documents différents.  
Du fait de mon implication dans Stylo, le regard que je porte sur ce terrain
n'est pas neutre et relève d'une forme de recherche-action [ajouter une
référence].

Alors que chaque signe et chaque trace inscrite [@christin__1999;
@vitali-rosati__2020] dans l'éditeur de texte Stylo incarne cette tension
_entre_ l'utilisateur et la machine, dont les différences de langage -- naturel
et machine -- rend a priori toute communication directe impossible, nous
analysons les différents modes de communication des informations dans Stylo pour
suivre les traces de l'intime qui y circulent.
Pour en découvrir plus sur cet _entre_, nous étudions cette distance à partir de
la méthode employée par le théoricien des médias F. Kittler
[-@kittler_mode_2015; @kittler_gramophone_2018], qui s'appuie sur la description
du fonctionnement de la machine à écrire et de l'ordinateur afin de comprendre
leur implication, en tant que média, dans le phénomène qu'est l'écriture.
Cette méthode implique de comprendre les comportements et les fonctionnements
techniques des composants à l'oeuvre dans la machine, et cela qu'ils relèvent du
matériel ou du logiciel.
En conséquence, nous mobilisons de la documentation technique pour étayer notre
propos et pour analyser les traces qui nous intéressent.  
