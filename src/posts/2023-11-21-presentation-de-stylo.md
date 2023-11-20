---
title: "Présentation de Stylo"
date: "2023-11-21"
---

Nous pouvons commencer cette présentation par sa version la plus courte, plagiat d'Antoine F. qui lors d'un colloque s'exclamait après plus de 2h heure de patience devant un poster : « MSWords sucks and Stylo is the best tool ! ».
Fin de la présentation, merci d'être venu !

Pour la version la plus longue, j'aimerais introduire mon propos par des remerciements à toutes les personnes ayant participé au déploiement sans accroc de la version 3.0 (rendu officiel le 20 novembre).
Cet événement nous montre que Stylo est avant tout un composite fait d'étudiants, d'éditeurs, de développeurs, de chercheurs, de graphistes, d'auteurs, de textes, de codes, de protocoles, etc. et qu'il ne s'agit pas juste d'un service web.

Néanmoins, lors de présentations plus classiques, Stylo est présenté comme un éditeur de texte sémantique pour l'édition scientifique en sciences humaines et sociales et en lettres et comme un projet de recherche qui questionne la signification de l'écriture et entend proposer une épistémologie du texte.

Jusqu'à présent, Stylo était présenté avec pour objectif la reprise en main des modes de production du sens pour les chercheuses, les chercheurs, les étudiantes et étudiantes et les revues, ou encore la reprise de contrôle de son propre texte (sous-entendu la structuration du contenu).

Peut-être qu'à cet endroit il y a une erreur d'énoncé : les utilisateurs de Stylo ne reprennent pas en main les modes de production, mais ils s'y trouvent confrontés et à même de les comprendre.
On ne reprend pas en main cette production du sens -- nous pouvons ranger cet argument dans la catégorie marketing --, bien au contraire, on la partage avec d'autres entités que l'on peut raisonnablement identifier par Stylo dans un premier temps, nous y reviendrons plus tard.

Refaisons un point rapide sur Stylo : c'est un outil libre et _open source_ conçu en 2017 par la CRCEN et soutenu depuis 2020 par la TGIR Huma-Num.
Stylo a pour objectif de transformer le flux de travail numériques des revues savantes.
En tant qu'éditeur de texte WYSIWYM (_What you see is what you mean_), il vise à améliorer la chaîne de publication académique tout en invitant à une réflexion théorique et pratique sur nos façons d'écrire et d'éditer.

La chaîne proposée par Stylo repose sur 3 formats pivots de texte brut : le Markdown, pour le corps du texte, le YAML pour la sérialisation des métadonnées et le BibTeX pour les références bibliographiques.

Ces 3 formats sont ce que nous pouvons nommer la source des textes savants qui, lors de l'export, seront transformés par Pandoc en différents artefacts, selon ce que souhaite l'auteur.
La capacité d'export de Stylo est donc complètement associée à la capacité de conversion et de transformation de Pandoc.
Voici donc une brique de plus dans l'identité de Stylo.

Depuis le début de l'année 2023, Stylo s'est doté de nouvelles fonctionnalités et a fait peau neuve deux fois. Les mues de Stylo sont très proche, est-ce la puberté ?
(Note : Margot emploie ce terme dans son chapitre sur le média, sache toutefois que j'ai employé cette métaphore avant de lire ton chapitre. J'espère que tu ne m'en voudras pas trop !)

Ces nouvelles fonctionnalités (intégrées à la demande des utilisateurs : elles reflètent les besoins d'écriture en contexte numérique) sont : 

- l'édition collaborative synchrone
- les espaces de travail 
- les corpus (qui ne sont pas terminés)
- l'intégration de l'éditeur de texte Monaco
- l'interface multilingue (fr et en pour l'instant)
- une API GraphQl accessible en lecture et en écriture
- un module d'export stable et l'intégration de l'export vers _TEI Commons_ 
- une refonte de la documentation pour suivre toutes ces évolutions

Voilà ce que vous en avez déjà lu si vous avez bien fait vos devoirs.

Ce que l'on peut en dire c'est que Stylo en 2023 n'est plus du tout Stylo de 2020 ou 2022, c'est un outil qui a été adapté aux besoins formulés par la communauté qui en a l'usage.

Pourtant, les mêmes réticences reviennent dans les discours des personnes qui ne veulent pas l'utiliser (et on s'en fiche, le but ce n'est pas de convertir tout le monde au texte brut).
On peut souvent entendre de la part des réfractaires : 

- Stylo comporte des bugs ;
- C'est trop difficile, les interfaces graphiques sont plus agréables (ou on en a l'habitude) 
- Google Doc, MSWord ou tout autre logiciel de traitement de texte sont plus fonctionnels (alors que ce n'est pas vrai, ce sont les assistants d'édition qui font tout le travail d'invisibiliser les utilisations approximatives de ces logiciels, cf le CMS Lodel d'OpenEdition)
- le balisage du texte est lourd 
- on y comprend rien

Toutes ces critiques ne vont à l'encontre que d'un seul élément : le mode WYSIWYM que l'on a mentionné tout à l'heure.
La seule chose qui peut potentiellement faire l'objet de mécontentement est donc cette brique en surcouche sans jamais questionner tout le fonctionnement qui est en-dessous.
Ceci a quelque chose d'assez révélateur.

L'éditeur WYSYWYM vient en opposition au paradigme WYSIWYG (_What you see is what you get_) que l'on retrouve en général dans les outils de traitement de texte : c'est-à-dire des outils où l'on structure le contenu à partir d'une convention graphique.

Quelque part, cette situation positionne Stylo en concurrence avec les outils qui fonctionnent sur ce principe WYSIWYG.
On peut en citer quelques-uns comme l'emblématique MSWord, LibreOffice, Google Doc, etc.

De l'autre côté nous retrouvons des systèmes d'édition qui reposent sur des langages de balisages plus ou moins légers comme TeX et LaTeX, Typst, Asciidoc, etc.

Néanmoins, le positionnement de la Chaire vis-à-vis de Stylo est qu'il n'est pas un concurrent de ces mastodontes.
Ce n'est pas l'objectif premier, il ne s'agit pas de devenir une entreprise de service qui fournit une solution clef en main.
Stylo est et reste une preuve de concept grâce à laquelle nous essayons de formuler et d'implémenter des besoins sous la forme d'une fonctionnalité particulière.

En questionnant les pratiques d'écriture savante, Stylo pose aussi la question de l'expression formelle d'un outil d'écriture.
Comment exprimer une pratique avec un langage de programmation (sous la forme d'une fonction) ?

Cette question je vous laisse la digérer et je reprends mon fil. 

On voit donc apparaître une contradiction entre d'une part la volonté de l'équipe qui supervise le projet d'en faire une preuve de concept sans la mettre en concurrence avec quoi que ce soit, et l'imaginaire d'une communauté qui ramène tous les outils au même niveau (sous une dimension utilitariste) et met donc face à face Stylo et MSWord. Ce trait là est volontairement réducteur.

Cette prise de position nous ramène quelque part à la théorie des médias et au nouveau matérialisme d'où l'on considère le support du message comme porteur de sens, alors qu'un autre parti le considère comme neutre et sans aucune participation à la production du sens : voilà le premier fer de lance de Stylo.

Pour creuser un peu plus cette question du WYSIWYM et WYSIWYG nous allons reprendre les caractéristiques de l'écriture numérique.

L'écriture numérique se distingue principalement des autres types d'écriture grâce à deux caractéristiques : 

- la calculabilité ;
- la distinction entre le geste d'écriture et l'acte d'inscription du signe sur le support.

L'écriture numérique est souvent définie par sa caractéristique computationnelle : elle est calculable (Crozat, Kembellec, Vitali-Rosati, Bachimont, Merzeau).
C'est principalement ce trait de caractère calculatoire qui la distingue des autres types d'écriture.
Dans l'environnement informatique, chaque signe que l'on peut y inscrire à son pendant unique sous forme de bit.
Lorsque chaque caractère peut être identifié en tant que nombre, il devient possible d'implémenter ce modèle dans une machine et de lui appliquer des calculs.
Le passage du signe à l'unité atomique et discrète qu'est le nombre signifie un changement de représentation du monde : le monde n'est plus signifié par des mots ou des concepts mais le devient par des nombres.
Si toutefois beaucoup d'entre nous oublient que les alphabets composés de lettres (contrairement à ceux composés de pictogrammes) sont asémantiques, alors que McLuhan s'efforce de le rappeler dès 1964, une représentation du monde composée de chiffres n'a clairement plus aucune signification, vous en conviendrez.
Par contre, cette représentation numérique du monde gagne cette particularité d'être calculable et mesurable (voir le dialogue asynchrone sur l'espace numérique entre Luca Paltrienieri et M. Vitali-Rosati).
Nous remarquerons que j'ai volontairement distingué l'écriture numérique de l'environnement informatique.
En effet, cette représentation numérique n'est pas nouvelle et ce n'est pas l'ordinateur qui l'a apporté.
À notre connaissance, son origine remonte aux prémices de l'écriture et des développements des systèmes monétaires, nous dit Clarisse Herrenschmidt (2007).

L'écriture numérique se distingue également des autres types d'écriture par le fait qu'il s'agit de la première écriture où le geste d'écrire ne correspond pas à l'action d'inscrire le signe sur son support. Lorsque j'appuie sur une touche du clavier, je n'inscris pas la lettre à l'écran : je donne une instruction à la machine d'inscrire un signe dans le disque dur puis de l'afficher à l'écran dans un logiciel dédié.
Lors de sa conférence «Le logiciel n'existe pas», Friedrich Kittler annonçait déjà il y a quelques décennies que l'être humain n'écrivait plus depuis les années 70' et que le dernier geste d'écriture remontait au dessin d'un processeur réalisé dans le garage d'un ingénieur travaillant pour la firme Intel.
Pour les références, au-delà de la provocation de F. Kittler, c'est également une thèse que l'on retrouve en sémiotique (Souchier, etc.).

Écrire dans un environnement informatique ne se réduit donc pas à un système où l'auteur déverse sa pensée sur un écran au moyen d'un clavier.
Écrire dans un environnement numérique c'est avant tout s'adresser à une machine.
Il y a donc, avant tout acteur d'une chaîne éditoriale ou lecteur potentiel (même soi-même), un dialogue entre un être humain et une machine.
Or, j'émets ici l'hypothèse (on revient vite à Stylo c'est promis) que si un éditeur WYSIWYG est plus attirant qu'un éditeur WYSIWYM, ce n'est pas tant pour des raisons de littératie numérique que parce que la surcouche graphique cache l'interaction avec la machine.

En cachant les actions de la machine, on l'évacue de l'équation de la production du texte et du sens alors que si on la montre (et Stylo en cache déjà beaucoup) on confronte l'usager à ce dialogue avec la machine.

Il en va de même pour les interfaces textuelles comme les lignes de commande : ce n'est pas qu'elles sont difficiles à utiliser mais qu'elle renvoie à un dialogue avec une machine.

Pourquoi cela dérange-t-il ? 
Marcello tenait le propos la semaine dernière (lors de sa présentation à l'ENS de Lyon le 14 novembre dernier) que cela est effrayant, que cela nous fait peur (la peur que ce qui nous caractérise en tant qu'humain nous échappe).
Se confronter à la machine consiste à accepter le fait que ce n'est plus l'humain qui écrit, mais que c'est bien le couple humain-machine qui réalise cet acte.
L'humain n'est alors plus en opposition avec la machine.

Néanmoins j'ai envie de modérer ce propos en m'appuyant sur la pensée d'Anders : avant de ressentir de la peur il y a de la honte.

Interagir avec une machine demande une certaine rigueur : qu'il s'agisse de structurer un document ou de lui donner une série d'instructions, une machine ne peut interpréter l'ambiguité.
Cela veut dire qu'aucun échange ne peut reposer sur des conventions culturelles et que l'instruction donnée n'a en elle-même aucun sens : comment admettre que quelque chose qui n'a pas de sens puisse en générer ?

La honte (prométhéenne) d'Anders est alors double : d'un côté il y a un mélange de fierté devant cette machine créée par l'être humain et de honte parce que l'individu devant la machine sait que ce n'est pas lui qui l'a mise au point (manière de ne pas essentialiser cette machine) et de l'autre il y a cette honte à être face à un outil qui réalise une action mieux qu'on ne le ferait soi-même (alors que cette dite machine n'a aucune conscience de ce qu'elle réalise).

Il n'y a pas de plus facile ou de plus intuitif mais il y a des méthodes pour se cacher de cette honte, et la plus couramment utilisée est d'inventer et d'ajouter des surcouches graphiques sous le prétexte d'aller plus vite et d'être plus productif.

Lorsqu'on est dans Stylo on est mis devant l'évidence que c'est Stylo qui produit le texte et son sens : si on structure le document c'est pour que Stylo puisse le transformer en un autre texte : PDF, HTML, XML, DOCX, etc.
Pour raccrocher les wagons avec ce que je disais au début de la présentation, avec Stylo il n'est donc plus question d'avoir le contrôle du texte mais bien au contraire d'accepter le fait que c'est une machine, donc Stylo, qui co-écrit un document avec son auteur et permet de surmonter cette honte.

Pour le mot de la fin, plus qu'un outil pour une littératie numérique, Stylo est avant tout un outil de désillusion et de déprise.
Afin d'être plus explicite, en ce qui concerne les outils WYSIWYG, en faisant de la page l'objet sur lequel toute l'attention doit être concentrée, on renvoie la machine à une simple vision utilitariste.
La page, qui pourtant est bien le seul objet virtuel que l'on peut rencontrer dans cet espace, est un objet qui n'existe que pour réconforter l'utilisateur dans un espace délimité et sur lequel il croit avoir le contrôle.

Stylo n'est pas en concurrence ou n'a pas de concurrent car il ne s'agit pas d'une course pour gagner un marché : c'est un premier pas pour s'affranchir de cette honte et de cette peur vers des environnements d'écriture sur-mesure que chacun peut se créer.










