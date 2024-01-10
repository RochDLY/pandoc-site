---
title: 'Entretien avec Stéphane Pouyllau (Huma-Num)'
date: 2024-01-09
---

Ce billet fait l'objet de notes prises lors d'un entretien réalisé avec Stéphane
Pouyllau, responsable de l'Huma-Num Lab, le 9 janvier 2024 sur le campus
Condorcet.

Contexte :

Cet entretien a été réalisé avec l'objectif de glaner quelques informations sur
la composante Huma-Num du projet Stylo et de leur implication aux niveaux
humains et technologiques.

Huma-Num existe depuis un peu plus de 10 ans (2013) et a pour vocation
d'accompagner les chercheurs en SHS ainsi que de proposer une infrastructure
numérique cohérente pour répondre aux différents besoins de la recherche
aujourd'hui.

Selon le [site web d'Huma-Num](https://www.huma-num.fr/quest-ce-que-l-ir-huma-num/) :

> **La principale mission de l'IR** est de construire, avec les communautés et à
> partir d'un **pilotage scientifique**, une infrastructure numérique de niveau
> international pour les SHS.

Depuis 2020, Huma-Num est partenaire du projet Stylo développé à la CRCEN et
héberge l'application sur ses serveurs.

**Comment une institution française et une canadienne se rencontrent et
deviennent partenaires pour le développement d'un outil comme Stylo ?**

Les réflexions démarrent au congrès [DH2017](https://dh2017.adho.org/).
(travail entre Marcello, Michael, Stéphane autour d'Érudit).
À ce moment, Marcello et Nicolas mènent déjà une recherche sur l'écriture
savante en contexte numérique : ils utilisent déjà plusieurs briques
technologiques que l'on va retrouver plus tard dans Stylo (exemple : les formats
de texte brut) sans que ces briques soient réunis dans une même interface.

Lors du congrès qui réunit les membres à l'origine du projet, les réflexions
portent sur l'implémentation d'une chaine pour OpenEdition et Erudit.

**Comment en est-on arrivé à ce partenariat entre les deux institutions ?**

Le premier prototype fonctionnel de Stylo a été livré en 2019.
Du début du projet jusqu'à cette date, Stylo était développé en interne
par la CRCEN avec Servanne Monjour, Nicolas Sauret, Marcello Vitali-Rosati,
Arthur Juchereau, Margot Mellet et Antoine Fauchié.

À partir du premier trimestre 2020, Huma-Num a pu devenir un partenaire
officiel / institutionnel de la CRCEN et du CRIHN et a financé une partie du
projet.

Avant cette date, il n'y avait pas de cadre institutionnel pour pouvoir financer
un projet au Canada.
Une entente entre le CRIHN (sous la direction de Michael Sinatra) et Huma-Num
(sous la supervision de Stéphane Pouyllau) a été montée pendant les deux années
de développement du prototype (2017-2019) pour pouvoir financer Stylo.

Il faut savoir que le structure d'Huma-Num a changé durant les prémices de
Stylo. Le HNLab n'existait pas en 2017-19 et à ce moment-là Stéphane est
directeur technique d'Huma-Num.

Nous avons eu de la chance lors de l'établissement de l'entente car la personne
qui en avait la charge de  à l'UdeM a travaillé au préalable au CNRS ce qui en a
facilité le montage.
Les papiers ont été signés début 2020 au début de la pandémie.

La signature de cette entente entre le CRIHN et Huma-Num correspond également à
la fin du doctorat de Nicolas Sauret.
Ainsi, lorsque Stéphane a monté le HNLab, il a proposé d'accueillir Nicolas S.
au sein de cette structure pour continuer à piloter une partie du projet et
renforcer les liens entre les deux institutions.

Stylo est logé directement dans l'axe sur l'écriture scientifique du Lab.

> Ca me semblait indispensable de mettre de l'argent de Stylo qui fait un pont
entre le monde de l'écriture solitaire et celui de l'édition.

Complément d'information :
Le deuxième axe des missions du HNLab porte sur ce que Stéphane regroupe sous le
terme d'écriture scientifique.
Cet axe comporte trois parties :

- saisie du texte et du code avec Stylo et Jupyter Notebook
- stockage des données avec Nakala
- versionnement et déploiement continu (CI/CD) avec Gitlab

> C'est le design du cheminement qui est intéressant, pas le choix des
technologies. L'enjeu de l'axe 2 est épistémologique, pas technique.

**Comment a été décidé la répartition des missions autour des
développements/entretiens de Stylo ?**

L'entente entre le CRIHN et Huma-Num consiste à statuer que le HN Lab peut
contribuer financièrement aux développements de Stylo si quatre conditions sont
respectées :

- [X] migration de l'hébergement de Stylo (vers les serveurs d'Huma-Num)
- [X] interconnexion à Isidore (c'est actuellement le cas avec les mot-clés
contrôlés)
- [X] authentification Human-Id
- [X] Deux réunions de feuille de route par an

Aussi le HN Lab fait le choix de ne pas se mêler des choix de partenariats ou de
la communication que fait la CRCEN autour de Stylo.

**Quelles sont les ressources techniques mises à disposition pour Stylo ?
(modèle de serveur hardware, configuration de la machine virtuelle OS etc...)**

Stylo fait l'objet de deux machines virtuelles sur les serveurs d'Huma-Num
(basés à Lyon sur d'anciens DELL R630), une VM pour la préproduction de Stylo
(<https://stylo-dev.huma-num.fr>) et une VM pour l'application en production
utilisée par la communauté (<https://stylo.huma-num.fr>).

Les machines virtuelles sont dotés de 48Go d'espace disque et fonctionnent grâce
au système de virtualisation KVM, performant malgré qu'il soit peu souple /
ergonomique.
Pour illustrer ce manque de souplesse, pour augmenter la RAM allouée à la VM, il
faut la stopper puis exécuter de multiples commandes pour arriver à ce résultat
avant de la relancer.
Le système d'exploitation des VM est soit Debian soit CentOS (sachant que ce
dernier n'est plus maintenu, Huma-Num a décidé de migrer les VM sous CentOS sous
le système d'exploitation Rocket Linux)

Les racks sont gérés par l'hébergeur (CNRS qui héberge à Lyon dans un centre de
calcul créé en 1986).

**Quels sont les moyens humains disponibles pour Stylo ? (nom des postes /
rôles + indicateur temps par année)**

Avant la convention (entente) : il n'y avait pas de pôles différents (pas de HN
Lab)

Depuis l'entente :

- HN Lab pilotage et développements (Julie pour la partie backoffice et stats,
et Stéphane)
- HSTC (pôle infrastructure piloté par Gérald et Thomas) (réseaux et orchestrer
la VM)

**Quel est le coût de Stylo pour l'IR Huma-Num ?**

Il y a plus de 300 VM qui tournent chez Huma-Num.
On ne peut pas établir le coût individuel de chacune des machines virtuelles.

Toutefois, Huma-Num estime que le coût consolidé (c'est-à-dire comprenant toutes
les charges salariales, énergie, maintenance, etc.) s'élève à environ 2500 euros
par an pour chaque machine virtuelle.
Étant donné que Huma-Num déploie deux machines virtuelles pour Stylo, on peut
estimer le coût annuel à environ 5000 euros (en réalité il doit être légèrement
inférieur puisque ce sont de petites machines virtuelles).

Ajouté à cela, Huma-Num fournit une enveloppe supplémentaire d'environ 30000
euros chaque année pour financer une partie des développements de l'application.

**Comment vois-tu le futur de Stylo ?**

Lors de cette première période allant de 2020 à 2024 il fallait stabiliser Stylo
et y ajouter quelques fonctionnalités, ce que nous avons fait.
Maintenant on entre dans une période charnière de Stylo.
La phase suivante est une phase de consolidation : on professionnalise Stylo,
c'est-à-dire qu'il faudrait une entité institutionnelle intégralement dédiée au
projet pour pouvoir être réactif auprès de la communauté (par exemple en créant
un laboratoire commun dédié à cette mission).

Le coeur de Stylo est composé des trois formats standards que sont le Markdown,
le YAML et le BibTeX, le reste est périssable.
Ce qu'il faut garder c'est ce coeur là.
Dans cette même idée on pourrait imaginer un client de Stylo qui fonctionne
quelle que soit la distribution (MacOS, Linux ou Windows).
