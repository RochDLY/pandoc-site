---
title: 'Préparation du cours Identités numériques avec Quarto'
date: 2024-01-10
---

Pour ce billet je vais présenter l'environnement d'écriture que j'utilise pour
le cours sur les identités numériques dispensé à l'Université Paris Nanterre.

## Un peu de contexte

Depuis un peu plus de deux ans je teste différents dispositifs numérique
d'écriture allant d'interface de gestion sur le Web aux éditeurs de texte
intégrés au terminal comme vi ou emacs.

Un fait intéressant est que pour la plupart des solutions qui me conviennent, je
les garde installées sur ma machine (ou je garde un accès avec un compte en
ligne) et elles me servent pour un usage spécifique.

Par exemple pour saisir des notes ou des ébauches d'idées je me sert souvent de
l'application Stylo (quelques notes collaboratives y trainent depuis que la
fonctionnalité a été déployée).
Alors que pour saisir des notes de réunion ou pouvoir les partager rapidement
(tout en sachant que le contenu est complètement accessible pour qui a l'URL)
j'utilise Hedgedoc.

À l'occasion de la coécriture du rapport de recherche sur les forges de
publication avec Antoine, j'ai pu tester assez longuement Quarto.

C'est un système que j'ai laissé tomber pour mon carnet personnel (je préfère de
loin celui-ci).
Cependant, je continue pour l'instant de l'utiliser pour créer de petites
pages Web pour mes cours comme c'est le cas pour le cours sur les identités
numériques (cf
<https://identites-numeriques.en-cours-de.construction>).

Le site web est hébergé via le service gitpage sur GitHub. Le répertoire du site
se trouve ici : <https://github.com/RochDLY/identite_numerique>

## Environnement d'écriture

En plus d'installer Quarto sur son ordinateur, on a la possibilité de l'utiliser
dans différents environnements qui intègrent un plugin (pour faciliter son usage).
Dans mon cas je pourrais très bien l'utiliser dans Neovim (il s'agit de mon
environnement d'écriture le plus régulier), toutefois je me suis heurté à
un problème qu'il me semble difficile de contourner alors je l'utilise plutôt
dans VSCodium qui a l'avantage d'intégrer des boutons pour la transformation des
documents (et surtout pour la prévisualisation !).

Le problème rencontré dans Neovim (avec Quarto) est le suivant : étant sous une
distribution dont la fréquence de mise à jour des paquets est relativement basse
pour des raisons de stabilité, je me retrouve régulièrement avec une version de
Quarto qui nécessite une version de Neovim qui n'est pas encore disponible dans
le gestionnaire de paquet de Devuan.

(J'ai d'ailleurs un peu le même problème avec la version de LazyVim.)

En conséquence, je suis obligé de compiler manuellement Neovim pour avoir une
version compatible avec l'utilisation de Quarto dans cet environnement.

Étant donné que l'objectif est de ne pas aller à l'encontre du fonctionnement de
Devuan (si je dois faire la même chose pour tous les logiciels que j'utilise il
deviendrait nécessaire de se poser la question de la pertinence du choix du
système d'exploitation), je préfère utiliser VSCodium.

## Configuration de Quarto

### Le site web

Du côté de Quarto c'est assez simple à mettre en oeuvre.

Dans l'éditeur VSCodium, il suffit de créer un nouveau projet (_website_) et de
remplir les entrées du fichiers de configuration YAML `_quarto.yml`.

Pour ce site, les informations sont les suivantes :

```YAML
project:
  type: website

website:
  title: "Identités numériques"
  sidebar:
    style: "floating"
    search: true
    contents:
      - index.qmd
      - posts/bibliographie.qmd
      - section: "Séances de cours"
        contents:
          - posts/170124.qmd
      - section: "Outils"
        contents:
          - tools/gephi.qmd
          - tools/redaction.qmd
          - tools/stylo.qmd
          - tools/terminal.qmd
  page-footer:
    left: "© 2024 WTFPL, Roch Delannay"
    right: "Ce site a été réalisé avec [Quarto](https://quarto.org)"

format:
  html:
    theme: flatly
    css: styles.css
    toc: true

```

Le thème `flatly` utilisé n'est pas du tout modifié à l'exception de l'affichage
des balises `<iframe>` que je voulais un peu plus large pour y insérer les
slides prévues pour le cours.

En plus de l'index.qmd, on trouve toutes les ressources que j'utilise pour mon
cours dans des dossier séparés à la racine du projet :

- les billets (`posts/`)
- les `images/`
- les `slides/`
- des fiches d'aide (`tools/`)

Chaque nouvelle séance de cours fait l'objet d'un document qui est inséré dans
`posts/` auquel j'adjoins 3 entrées YAML en en-tête :

```YAML
---
title: "17 janvier 2024"
bibliography: chemin/vers/la/bibliographie.bib
nocite: false
---
```

Je donne pour titre du document la date du cours.
Ce titre est récupéré et apparaît dans le menu de navigation à gauche de
l'écran.

Étant donné que je travaille seul à l'édition de ce site web, j'utilise une
petite astuce pour mettre à jour facilement mon fichier de références
bibliographiques.
Ce document est créé depuis l'application Zotero (avec le plug-in Better BibTeX)
en exportant une bibliographie au format BibTeX avec l'option "Garder à jour".
De cette manière, je n'exporte la bibliographie qu'une seule fois et lorsque je
fais des mises à jour sur Zotero, le document exportés est également mis à jour.
Ainsi, je n'ai plus qu'à reconstruire le site avec Quarto pour modifier les
références bibliographiques du site web.

### Les slides

Je ne suis pas friand d'utiliser des slides pendant les cours, surtout lorsque
je prépare un site web pour rendre disponible les différentes ressources.
Vu que c'est une demande récurrente des étudiants, c'est quelque chose que j'ai
intégré à leur demande (bien que mes slides soient bien pauvres en contenu).

J'ai essayé de m'inspirer de ce que propose Antoine Fauchié a ses étudiants.
Il leur met à disposition un site web qui contient tous les supports de cours, y
compris les slides.
La beauté de l'environnement proposé par Antoine est de n'écrire qu'une seule
fois ses contenus qui approvisionnent ensuite les slides et le site web.

Néanmoins, je n'avais pas forcément besoin d'un tel système (avec la redondance
du contenu des notes dans les slides et dans les pages web).

Par contre, et c'est là que Quarto devient très pratique, je peux très
facilement intégrer des slides générées avec Quarto (en surcouche à RevealJS via
Pandoc) et les encapsuler dans le site du cours puisque les deux supports sont
au même format HTML !

(La suite devient un peu crade)

Plutôt que d'avoir tout une configuration RevealJS (c'est prévu pour plus tard),
je peux pour l'instant créer un simple document avec Quarto auquel je passe le
YAML suivant :

```YAML
---
title: "Titre de la séance"
author: "Roch Delannay"
date: "17 janvier 2024"
bibliography: /chemin/vers/la/bibliographie.bib
suppress-bibliography: true
format: 
    revealjs: 
        incremental: false
        scrollable: true
        theme: [simple, custom.scss]
        footer: "4L4IC01P - Université Paris Nanterre - Hiver 2024"
        embed-resources: true
---
```

Le gros tips de ce document là est le dernier paramètre passé au YAML, le
`embed-resources` permet de ne produire qu'un seul fichier HTML qui contient
absolument toutes les ressources nécessaire pour faire tourner les slides
correctement (images, scripts, styles, etc.).

Une fois produit, je déplace ce fichier dans le répertoire du projet du cours
dans le dossier `slides/` et je l'encapsule dans la page de mon cours au moyen
d'une `<iframe>`.
Comme le document HTML est également disponible à sa propre URL, il est aussi
très simple d'y accéder en plein écran pour naviguer facilement entre les
différents supports.
