---
title: Les aventures dans Stylo
date: "2023-12-06"
---

Cet automne a été particulièrement dense.
Lorsque j'écris ces lignes je suis à quelques jours de quitter une nouvelle
fois Montréal pour repartir à Paris.
Ce séjour n'aura pas été de tout repos, bien au contraire.
L'ambiance ressentie (que ce soit chez les collègues français ou québécois)
traduit clairement un épuisement général auquel je n'échappe pas.

Lors de mon séjour à la CRCEN ces derniers mois, j'ai principalement consacré
mon temps au projet de recherche Stylo, à ses développements, à sa maintenance,
aux expérimentations menées avec les partenaires du projet (revue Humanité
Numériques et Métopes), aux échanges avec les différents acteurs qui
participent de manière plus ou moins proche à ses développements (Antoine,
Marcello, David, Guillaume, Maïtanné, Louis-Olivier, Servanne, Nicolas, Yves
(x2), Camille), à dispenser des formations ou encore à m'occuper de la _hotline_
par courriel, en présence ou en visioconférence, réviser la documentation
(sur laquelle il faut encore revenir), etc.

Pour une recherche (plus globale que Stylo) qui devrait être menée en contexte
numérique, je n'aurais jamais autant écrit le mot Stylo sur une temporalité
aussi courte (on ne dirait pas comme ça mais 4 mois passent bien trop
rapidement !).

Au milieu de ce parcours est apparue une embûche : une demande de financement
refusée ...
Plusieurs semaines de travail tombent à l'eau et le calendrier des
développements doit être repensé.
Ça mine un peu le moral.
Ce projet, appelé Péristyles par ses membres, que j'affuble du petit nom de
Stylopes, tombe à l'eau pour une raison incompréhensible : "on" ne sait pas si
les auteurs sauront s'approprier l'outil.
Allez dire cela à notre petit bassin d'utilisateur.trice.s
(environ 4500 personnes) !

Le gros chantier de ce trimestre a été la version 3.0 de Stylo : on a mis à
jour la documentation, fait des tests en pagaille sur toutes les instances de
préproduction pour vérifier que tout fonctionnait correctement, préparé un peu
de communication sur le sujet (on a quand même été présent pendant 5 jours sur
les réseaux sociaux et sur quelques listes de diffusion DH) et, miracle, tout
se passe comme sur des roulettes.

Stylo est maintenant doté de nouvelles fonctionnalités (et boutons) :

- un mode d'écriture collaborative synchrone stable (on peut même kicker des
personnes qui travaillent sur un article #troll)
- un nouvel export en XML TEI compatible avec le schéma COMMONS (du coup on peut
aller faire un coucou à Métopes et OpenEdition)
- une interface (presque) bilingue
- une refonte du comportement des versions des documents
- une nouvelle fonctionnalité de partage stable nommée « espace de travail »

La date de _release_ était fixée au 20 novembre 2023 et les journées / semaines
qui ont suivies ont été dédiées à traquer et à chasser les bugs qui pouvaient
traîner.

Un autre chantier de Stylo est l'expérimentation avec la revue Humanités
Numériques (publiée par le diffuseur OpenEdition).
L'idée est simple : accompagner la revue dans un changement de _workflow_ et
remplacer MSWord par Stylo.
Pour réaliser ce projet nous avons mis en place une expérience pour tester la
chaîne Stylo > Métopes > Lodel à partir d'un article (qui est très long et à
travers lequel on a rencontré tous les problèmes possibles !).

D'ailleurs l'article a vu le jour sur le site de la revue !
On peut le retrouver [ici](https://journals.openedition.org/revuehn/3836) et
l'équipe de la revue parle de nous dans son
[édito](https://journals.openedition.org/revuehn/3886) !

Ce qui ressort de ces quelques mois est la nécessité d'intégrer une vérification
de la syntaxe Markdown dans les articles de Stylo : la plupart des erreurs
rencontrées par les usagers sont de cet ordre-là.
Certes il y a la documentation en ligne mais personne (ou peu de personnes) ne
va la consulter.
En conséquence, la _hotline_ se retrouve submergée pour des problèmes
relativement simple à résoudre, alors qu'un bon _linter_ Markdown pourrait au
moins en dégrossir la plupart.
C'est un truc auquel on pense depuis un moment mais c'est une fonctionnalité
reportée à plus tard faute de financement !
