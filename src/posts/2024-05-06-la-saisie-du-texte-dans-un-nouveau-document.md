---
title: "La production de l'intimité du chercheur par les publications savantes :
phase de saisie du texte"
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

Selon ce cadre théorique, et puisque notre hypothèse positionne l'intime en tant que
produit de l'écriture, nous pouvons nous demander quelle est la contribution de
l'environnement d'écriture à cet intime lors de la saisie d'un texte dans un
document.

Ainsi, parmi toutes les fonctions éditoriales que l'on pourrait énumérer, nous nous
intéressons dans ce chapitre à la saisie du texte et à l'environnement support
[@zacklad_organisation_2012] dans lequel il s'inscrit.
Lors de cette phase de l'écriture, cet environnement devient le lieu où se
manifeste un trouble entre ce que l'usager à l'intention d'écrire et le document
que produit la machine, qui est structuré selon les formats et protocoles
implémentés à l'intérieur de l'environnement.
Ce trouble nait de la rencontre entre une représentation du texte structurée
graphiquement et une représentation du texte structurée par du texte, comme
c'est le cas pour une page web interprétée par un navigateur et son pendant au
format HTML.
Notre intérêt se porte sur plus particulièrement sur le côté
machine de cette interaction humain-machine et comment elle perçoit, reçoit
et traite les informations pour produire le document à travers un environnement
particulier.

Afin de traiter cette problématique, nous nous appuyons dans un premier temps
sur les particularités de l'écriture numérique
[@bouchardon_lecriture_2014; @crozat_ecrire_2016;  @souchier_numerique_2019] et
sur le fonctionnement de la machine pour illustrer, dans une deuxième partie,
le rôle de médiation joué par les logiciels -- entendu comme une suite
d'instructions écrites -- entre la saisie du texte au clavier et les
traitements appliqués à ces informations, jusqu'à leur stockage dans une mémoire
informatique. 

Tandis que chaque environnement a ses propres modalités d'écriture que nous ne
pouvons pas toutes énumérer, nous nous appuyons dans la deuxième partie de ce
chapitre sur l'étude de l'éditeur de texte sémantique Stylo et les différentes représentations
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
[-@kittler_mode_2015; @kittler_gramophone_2018], qui s'appuie d'abord sur la description
du fonctionnement de la machine à écrire puis celle de l'ordinateur afin de comprendre
leur implication, en tant que média, dans le phénomène qu'est l'écriture.
Cette méthode implique de comprendre les comportements et les fonctionnements
techniques des composants à l'oeuvre dans la machine, et cela qu'ils relèvent du
matériel ou du logiciel.
En conséquence, nous mobilisons de la documentation technique pour étayer notre
propos et pour analyser les traces qui nous intéressent.  

## Écrire dans un environnement numérique

### Définir l'environnement où écrire

Par habitude, nous partons du présupposé que lorsque nous évoquons les mots
environnement d'écriture numérique ceux-ci sont synonymes environnement
d'écriture informatique et désignent la même chose.
En conséquence, lorsqu'il s'agit de convoquer l'écriture numérique nous pensons
tout de suite à un ordinateur, aux claviers, aux écrans et aux pointeurs qui
clignotent dans des éditeur de texte ou dans les champs des formulaires en
ligne.
Avec le numérique ubiquitaire [@citton_angles_2023], ces pratiques d'écriture
sont ancrées dans nos habitudes au point de ne plus les remettre en question.
Les dispositifs d'écriture analogique sont ainsi renvoyés à l'état de vestiges
archaïques, comme peuvent l'être les machines à écrire alors qu'elles ont été
fabriquées méticuleusement par des designers et des ingénieurs et qu'elles ont
fait la fierté et la renommée de certaines entreprises comme Olivetti en Italie.
Aujourd'hui ces machines sont complètement désuètes et inutilisées depuis
presque une trentaine d'années.
Elles sont maintenant exposées dans des musées -- entre autres au MoMA et au
Centre Pompidou -- et sont intégrées dans des collections permanentes ou
exhibées lors des expositions en lien avec les designers qui les ont
conçues^[C'est par exemple le cas de la machine à écrire Valentine conçue en
1968 par le célèbre designer Ettore Sottsass, machine qui est devenue le produit
emblématique de l'entreprise Olivetti lors de sa commercialisation en 1969.
Comme nous le verrons plus loin, lors des mêmes années aux États-Unis, le
président Johnson déclara qu'à l'échelle fédérale les ordinateurs doivent être
compatibles avec la norme ASCII.].

![Machine à écrire portative](https://www.photo.rmn.fr/CorexDoc/RMN/Media/TR1/YECPH3/07-521403.jpg "Machine à écrire portative")

Crédits : © Adagp, Paris. Crédit photographique : Georges Meguerditchian -
Centre Pompidou, MNAM-CCI /Dist. RMN-GP. Réf. image : 4N40151. Diffusion image :
[l’Agence Photo de la RMN](https://www.photo.rmn.fr/C.aspx?VP3=SearchResult&IID=2C6NU0CU7GAD)

![Publicité pour la machine à écrire Valentine](https://www.photo.rmn.fr/CorexDoc/RMN/Media/TR1/VYKH9X/13-519016.jpg "Publicité pour la machine à écrire Valentine")

Crédits : © Adagp, Paris. Crédit photographique : Jean-Claude Planchet - Centre
Pompidou, MNAM-CCI /Dist. RMN-GP. Réf. image : 4F40212 [2003 CX 6098]. Diffusion
image : [l’Agence Photo de la RMN](https://www.photo.rmn.fr/C.aspx?VP3=SearchResult&IID=2C6NU0DWCD6W)

Pourtant, les derniers modèles fabriqués par ces entreprises l'ont été dans les
années 1980 et 1990, comme c'est le cas du modèle ETP 55 Portable^[Cette machine
a été conçue par Mario Bellini pour Olivetti en 1987, voir
https://www.moma.org/collection/works/3641 site consulté le 21 février 2024.] où
sont intégrés des composants électroniques pour suivre le marché des
ordinateurs.
Les constructeurs ont opéré un changement de paradigme de l'analogique vers le
numérique dès les années 1970 et ont suivi les innovations technologiques
apportées par la miniaturisation des composants électroniques pour
l'informatique.
Pour preuve, en 1983, Perry A. King et Antonio Macchi Cassia conçoivent le
premier ordinateur personnel d'Olivetti avec le modèle M10 en adaptant un
clavier à un écran à cristaux liquide. 
et ordinateur, équipé du processeur Intel 80C85 en 8-bits, pouvait également se
connecter à tout un ensemble de périphériques comme des imprimantes.

![Photo d'un M10](http://munk.org/typecast/wp-content/uploads/2014/08/15635.jpg "Photo d'un M10")

Crédits : Photo trouvée sur le blog
[Munk.org](https://munk.org/typecast/2014/08/03/back-to-the-future-pram-and-the-promise-of-unified-memory-again/),
site consulté le 22 février 2024.

Il faut se rappeler qu'au début des années 1980 il n'est pas encore certain que
l'ordinateur personnel (avec sa tour et son écran à tube cathodique) deviendra
l'outil d'écriture par excellence.
À cette époque, les machines à écrire ont encore quelques avantages sur les
plans esthétique, financier et social puisque on les retrouve encore implantées
à la fois dans les sphères professionnelles et personnelles.

La fin des années 1970 et les années 1980 marquent un tournant décisif pour
l'ordinateur personnel avec l'apparition des logiciels de traitement de texte et
la bataille qui sévit durant toute cette période.
M. Kirschenbaum et T. Bergin détaillent dans leurs travaux cette course au
développement de logiciels durant cette période pour obtenir un monopole sur le
marché [@bergin_origins_2006; @bergin_proliferation_2006;
@kirschenbaum_track_2016].
Avant l'engouement pour les interfaces graphiques et les gestionnaires de
fenêtres -- 1983 et 1984 avec l'entreprise Apple qui s'est largement inspirée
des interfaces graphiques développées par Xerox PARC dans les années 1970 -- la
seule interface affichée à l'écran était un terminal et la navigation se faisait
au moyen de commandes.
Les premiers logiciels de traitement de texte comme Electric Pencil ne
permettent pas alors une gestion de la mise en page idéale ni ne fonctionne sur
tous les modèles d'ordinateurs présents sur le marché^[Un autre logiciel comme
`TeX` développé en 1984 par Donald Knuth tente de résoudre ce problème de la
mise en page selon une approche WYSIWYM alors que la tendance est plutôt aux
interfaces WYSIWYG].
Ainsi, écrire sur un support connecté paraît aujourd'hui être une évidence alors
qu'il a fallut déployer de lourds efforts à une époque ou cette évidence était
incertaine.

L'écriture numérique est ainsi à distinguer de l'écriture dans un environnement
numérique : un ordinateur, Internet, le Web, une calcultrice ou une machine à
écrire de la dernière génération.
En tant qu'abstraction, l'écriture numérique est une représentation du monde
donnée, dont la qualification à travers un medium permet de l'incarner
physiquement et matériellement mais pas de la circonscrire.
En somme, cette représentation numérique du monde n'est pas nouvelle et ce n'est
pas l'ordinateur qui l'a apporté.
À notre connaissance, son origine remonte aux prémisses de l'écriture et des
développements des systèmes monétaires, nous dirait C. Herrenschmidt
[-@herrenschmidt_les_2023].

Dorénavant, lorsque nous ferons référence à l'écriture numérique nous parlerons
d'une écriture numérique dans un environnement informatique.

### Les particularités de l'écriture numérique

L'écriture numérique diffère d'une écriture plus traditionnelle -- par exemple
manuscrite -- et se distingue notamment par trois caractéristiques que sont la
calculabilité [@crozat_ecrire_2016], la variabilité [@bouchardon_lecriture_2014]
et la rupture sémiotique entre le geste d'écriture et l'inscription sur le
support [@souchier_numerique_2019].

La première caractéristique est d'ordre computationnel : l'écriture devient
calculable et peut donc faire l'objet d'instructions. Pour réaliser cette
action, on procède à une équivalence où chaque signe que l'on peut inscrire dans
cet environnement à son pendant unique sous forme de bits.
Lorsque chaque caractère peut être identifié en tant que nombre, il devient
possible d'implémenter ce modèle dans une machine et de lui demander, grâce à
des instructions, d'appliquer des calculs.

L'exemple idéal pour illustrer cette caractéristique n'est rien de moins que la
machine imaginée par Alan Turing, qu'il présente en 1936 dans son article « On
Computable Numbers, with an Application to the Entscheidungsproblem » dans la
section _Computing machines_ [-@turing_computable_1936].
Ce que Turing décrit n'est pas une machine physique mais un modèle théorique,
une machine abstraite fondamentale pour les développements futurs de
l'informatique.
Cette machine est constituée de plusieurs éléments :

- un ruban («_tape_») divisé en sections (appelées «_square_») dont chacune peut
  porter un symbole (0 ou 1 car cette machine est dans un système binaire)
- un organe de lecture («_scan_») pour lire les symboles un à un («_scanned
  square and scanned symbol_») et un organe d'écriture pour modifier un symbole
ou en écrire un nouveau si la section est vide
- une mémoire pour se rappeler des sections déjà scannées («_remember some of
  the symbols which it has been "seen" (scanned) previously_»)
- des instructions pour se déplacer sur le ruban, soit d'une case vers la gauche
  soit d'une case vers la droite, lire et écrire («_scan and print_») ou
modifier la case scannée et se redéplacer avant de s'arrêter.

Théoriquement le ruban sur lequel la machine exécute ses programmes est infini
vers la gauche et la droite et cela afin de permettre l'exécution des
instructions les plus complexes.
La machine de Turing ne s'intéresse pas aux résultats des instructions ni à leur
signification, d'où résulte une forme d'automatisation de l'écriture.
L'espace de la machine, aussi vaste soit-il, n'est composé que de séries de 0 et
de 1 ainsi que de différents états, renvoyant à des instructions et permettant
ainsi à la machine de modifier son propre espace. Cette capacité de modification
peut être associée à la deuxième caractéristique de l'écriture numérique que S.
Bouchardon nomme la variabilité.

Le passage du signe à l'unité atomique et discrète qu'est le chiffre signifie un
changement de représentation du monde (au sens que K. Hayles donne au terme
_worldview_ [-@hayles_my_2005]) : le monde -- ou l'espace -- n'est alors plus
signifié par des mots ou des concepts, mais le devient par des chiffres.
Comme McLuhan nous le rappelle dès 1964 [-@mcluhan_pour_1977], les alphabets
composés de lettres (contrairement à ceux composés de pictogrammes) sont
asémantiques. Si toutefois les alphabets sont liés à une culture d'où ils
émergent, l'abstraction nécessaire pour représenter le monde sous forme de
chiffres détacherait a priori cette vision de tout sens.
En dehors de tout modèle mathématiques abstrait, et cela quel que soit le
langage ou la base utilisée pour l'écrire, `3`, `trois`, `three`, `III`, `0011`,
`zéro zéro un un`, un chiffre ne signifie pas grand chose s'il n'est pas associé
à un système de valeurs particulier, par exemple le système métrique ou le
système international [@herrenschmidt_trois_2023].
En échange de cette perte de signification, l'écriture numérique y gagne cette
particularité d'être calculable et mesurable.

L'écriture numérique se distingue également des autres types d'écriture par une
troisième caractéristique.
Il s'agit de la première forme d'écriture où le geste d'écrire ne correspond pas
à l'action d'inscription du signe sur son support, phénomène que J. Bonaccorsi
nomme déliaison [@bonaccorsi_fantasmagories_2020].
Lorsqu'on appuie sur une touche du clavier, par exemple la lettre `a`, cette
lettre n'est pas inscrite à l'écran : l'instruction d'inscrire un signe dans la
mémoire de l'ordinateur est donnée à la machine, puis celle de l'afficher à
l'écran au moyen d'un logiciel particulier [@kittler_mode_2015;
@souchier_numerique_2019].
Néanmoins, le fait d'appuyer sur une touche du clavier lorsque l'ordinateur est
sous tension ne suffit pas pour déclencher cette instruction : si aucun
environnement dédié à l'écriture n'est préalablement exécuté, le fait d'enfoncer
une touche ne déclenchera aucune réaction de la part de la machine.
Par contre, lorsque l'on se situe dans un environnement où cette réaction est
attendue, comme un éditeur de texte, la frappe d'une touche déclenchera un
événement et le logiciel pourra générer l'instruction correspondant à l'action
d'écrire. 

[ecrire une phrase ou deux de transition]

### La machine, une entité formée du couple matériel/logiciel.

La représentation d'un ordinateur est souvent associée à un couple matériel /
logiciel.
La partie matérielle concerne tous les composants électroniques (carte mère,
mémoires, périphériques, etc.), alors que la partie logicielle englobe tous les
programmes permettant d'interagir avec la partie matérielle, comme le BIOS
(_Basic Input Output System_), le système d'exploitation ou encore un logiciel
de traitement de texte comme LibreOffice.

Ce couple matériel / logiciel range l'ordinateur dans la catégorie des appareils
programmables.
La plupart de nos appareils du quotidien ne sont pas programmables : il
exécutent ce pour quoi ils sont conçus et ne font rien d'autre.
Dans le cas d'un ordinateur ou d'un téléphone intelligent, ou de tout autre
appareil programmable, leur conception prévoit qu'ils soient manipulables :
elles n'ont pas de fonction précise, néanmoins elles sont capables de répondre à
plusieurs fonctions.
Un ordinateur qui n'a aucune instruction ne pourra rien faire une fois alimenté.
C'est là que les logiciels interviennent : ils permettent un usage déterminé
d'un ordinateur en manipulant des informations de façon à exécuter une suite
d'instructions formelles.

Pour fonctionner, un ordinateur n'a besoin que des éléments suivants : une
alimentation, un processeur, une mémoire vive, des entrées et sorties et une
carte mère auxquels viennent s'ajouter un certains nombre de périphériques
(écrans, souris, clavier, etc.), des extensions pour prendre en charge une
partie des calculs que l'on peut appeler des cartes filles (carte son, carte
graphique) et des mémoires de stockage (disques durs).

Le processeur, ou microprocesseur pour les ordinateurs modernes, est le
calculateur central de l'ordinateur, c'est cet élément qui manipule toutes les
données à traiter -- que l'on appelle aussi le(s) coeur(s) de l'ordinateur.
Chaque modèle de processeur à une architecture qui lui est propre, ce qui veut
dire que chacun traite les informations **différemment** (même si le résultat
obtenu est identique).
Un processeur est un assemblage de multiples types de circuits dont l'élément le
plus petit est le transistor.
L'évolution des processeurs a suivi la loi Moore jusqu'au début des années
2020^[La première loi de Moore est relative à l'évolution des processeurs dans
le temps et stipule que le nombre de transistors présents dans les processeurs
doublera tous les dix-huit mois pour un coût constant.], date à partir de
laquelle nous arrivons à la limite physique de la miniaturisation d'un
transistor.

Le premier processeur commercialisé, le processeur Intel 4004, l'a été en
1971^[Voir la page web correspondante sur le site de l'entreprise Intel,
consulté le 16 février 2024 :
https://www.intel.fr/content/www/fr/fr/history/museum-story-of-intel-4004.html.].
Il s'agissait d'un processeur 4-bits comportant pas moins de 2300 transistors.
Lors de la commercialisation de cet objet s'opère un changement radical dans la
conception des ordinateurs puisque, dès lors, du fait de la miniaturisation de
ce composant, les ordinateurs deviennent accessibles au grand public.
En suivant la première loi de Moore, les microprocesseurs ont continué à évoluer
jusqu'à atteindre le nombre de plusieurs milliards de transistors par
processeur, démultipliant ainsi leur capacité de traitement des informations.

Cette miniaturisation est rendue possible par la gravure des transistors dans
des disques de silice (_wafer_) plutôt que l'usage plus coûteux et instable de
relais et de tubes électroniques.
Un transistor est un composant électronique dont le rôle est de laisser passer
ou non le courant grâce aux propriétés du semi-conducteur à partir duquel il est
fabriqué.
En fonction de la valeur du courant qui lui est appliqué, le résultat associé à
ce courant sera `0` ou `1`.
Ce transistor est l'élément physique qui incarne les portes logiques (ET, OU,
OUI, NON, XOR, etc.) et traitent les données.
Parmi tous les traitements possibles, certains nécessitent de garder en mémoire
des résultats intermédiaires pour aboutir.
Ils sont alors stockés dans la mémoire vive en attendant d'être réutilisés.

Toutes ces informations traitées, qu'elles soient transformées ou mémorisées,
proviennent de ce que l'on nomme des _entrées_. 
Ce sont ces entrées qui encodent les informations en chiffres.
Une fois traitées, ou lorsqu'elles sont appelées par un programme, ces données
transitent par les _sorties_.
Elles font la transformation inverse et décodent les chiffres en signes
interprétables.

L'encodage et le décodage des caractères accompagne toute l'histoire de
l'informatique (et du numérique).
Aux prémices de l'informatique, chaque matériel comportait ses propres
programmes et tables d'encodage, rendant ainsi possible la transposition des
données d'un matériel à un autre par équivalence.
Cependant, dans la plupart des cas, les données ne pouvaient pas circuler entre
les différents modèles d'ordinateur, ou alors au moyen de transformations
fastidieuses, rendant ainsi les traitements réalisés sur les données enfermés
dans des silos.
La norme ASCII (_American Standard Code for Information Interchange_) fait son
apparition dans les années 1960 pour résoudre l'enjeu d'interopérabilité de
l'encodage des données.
Soumise à l'_American Standards Association_ (d'abord ASA puis ANSI) en 1961 par
l'un de ses inventeurs, Bob Bemer, puis approuvée en 1963, l'ASCII permet
d'encoder 128 caractères sur 7 bits.
Néanmoins, ce n'est pas parce qu'un encodage est reconnue en tant que norme que
son usage est effectif à l'instant même de sa reconnaissance.
Il faut attendra 1968 que le président des États-Unis d'Amérique Johnson demande
à ce que l'ASCII devienne la norme fédérale d'encodage des informations afin de
réduire les incompatibilités au sein des réseaux de télécommunication pour
qu'elle commence à se répandre.
Dès 1969, tous les ordinateurs achetés par le gouvernement des États-Unis
étaient compatibles avec la norme ASCII.
Du côté des ordinateurs personnels, il faudra attendre le début des années 1980
pour que cette norme se répande grâce, entre autre, à son implémentation dans
les ordinateurs construits par IBM.
La norme X3.4:1986 en vigueur aujourd'hui, a été déposée auprès de l'ANSI en
1986.
C'est à partir de cette norme que d'autres ont été développées et restent
compatibles ASCII, comme c'est par exemple le cas de la norme Unicode, publiée
en 1991, qui est la plus répandue de nos jours puisqu'elle encode le plus de
caractères.
Si ASCII contient 128 points de code, le standard Unicode permet d'en encoder
plus de 149 000 sur une vingtaine de bits par point de code dans sa version 15.1
(de 2023).
Afin de préserver cette compatibilité entre les normes, il est d'usage d'encoder
les 128 premiers caractères de façon identique à la norme ASCII.

Il est intéressant d'introduire les logiciels et leur fonctionnement à partir du
matériel composant l'ordinateur et plus particulièrement à partir de la carte
mère.
Les fournisseurs de carte mère incorpore généralement dans leur carte une
première couche d'abstraction matérielle, un BIOS (_Basic Input Output
System_^[Système élémentaire d'entrée sortie]), flashé dans la mémoire morte de
l'ordinateur et programmé pour s'exécuter lors de la mise sous tension de ce
dernier.
Ce que l'on appelle _couche d'abstraction matérielle_ en informatique représente
la couche logicielle qui se trouve entre la partie matérielle et le système
d'exploitation. Comme son nom l'indique, la fonction principale de cette couche
est de permettre la manipulation du matériel tout en faisant abstraction de
celui-ci. 
Le BIOS, ce tout premier jeu d'instructions qu'un ordinateur réalise, est un
programme propriétaire chargé d'initialiser la séquence d'amorçage (_boot_) de
l'ordinateur, de trouver le système d'exploitation, les périphériques (_a
minima_ le clavier et l'écran) et d'opérer quelques vérifications de bon
fonctionnement des composants comme c'est le cas de l'horloge temps réel qui
fonctionne en tout temps, même lorsque l'ordinateur est éteint, et rythme la
totalité des cycles des autres circuits.
Hormis quelques rares initiatives telles que Libreboot^[Voir le site web de
Libreboot : https://libreboot.org/, consulté le 03 avril 2024.] et
Coreboot^[Voir le site web de Coreboot : https://www.coreboot.org/, consulté le
03 avril 2024.], des logiciels libres et _open sources_ chargés de remplacer
partiellement le BIOS propriétaire, la majorité des cartes mères sont liées à
leur BIOS du fait de l'ajout par Intel, à partir de 2006, d'un sous programme
nommé _Management Engine_ (ME) qui est accompagné d'un ensemble de modules comme
_Boot Guard_ et _Secure Boot_ dont l'objectif est de veiller à ce qu'il n'y ait
pas de corruption du système d'amorçage de l'ordinateur^[Des informations sur ce
sujet sont disponibles à cette adresse sur le site web de libreboot :
https://libreboot.org/faq.html#what-systems-are-compatible-with-libreboot ou
dans la documentation des matériels d'Intel :
https://www.intel.com/content/www/us/en/search.html?ws=idsa-default#q=boot%20guard&sort=relevancy&f:@tabfilter=[Developers],
consultés le 03 avril 2024.]. Ces programmes ont sans cesse été améliorés depuis
leur introduction en 2006 et, aujourd'hui, ils empêchent toute modification de
cette couche logicielle, la plus basse d'un ordinateur, si celle-ci n'est pas
vérifiée et validée (avec un système de clés cryptées) par la firme
propriétaire/fabricante.

Le BIOS est donc l'interface entre l'utilisateur et la machine qui nous permet
de manipuler les différentes entrées et sorties du système, donc de gérer les
périphériques, fonction que le système d'exploitation peut également réaliser
une fois que la phase d'amorçage est terminée.
Le système d'exploitation (OS pour _Operating System_), est un niveau
d'abstraction supplémentaire et se retrouve à l'interface entre les applications
logicielles et la couche matérielle.
Un OS est composé d'un ensemble de programmes permettant la bonne gestion des
ressources de l'ordinateur : mémoires, calculs, périphériques, les registres,
etc.
Chaque OS a un fonctionnement qui lui est propre : l'architecture des
informations -- l'arborescence des dossiers, l'indexation des documents et des
fichiers binaires change selon l'OS utilisé --, l'ordonnancement des tâches pour
le processeur ou encore l'allocation de la mémoire.
Malgré le fait que ce n'a pas toujours été le cas, les applications logicielles
sont installés à l'intérieur des systèmes d'exploitation et prêts à être
exécutés.
Le passage par un système d'exploitation permet aux logiciels de ne plus
dépendre d'un modèle particulier du _hardware_ et d'en faire justement
abstraction, le rendant ainsi opérable sur différentes machines.

[faire une phrase de transition]

### Une ouverture sur la machine

Ce tour d'horizon des particularités de l'écriture numérique et de l'agencement
entre logiciel et matériel dans la machine nous montre que la
conception de la machine ne permet pas à un auteur d'y inscrire des signes dans
sa mémoire, ni de pouvoir les consulter directement puisqu'elle lui est
inaccessible à moins qu'un intermédiaire ne servent d'interface.
La médiation entre une machine et un auteur se fait au moyen d'un langage
compréhensible par les deux parties, que l'on assemble sous la forme
d'instructions qui, une fois empaquetées, forment un logiciel.
Pour symboliser la médiation du matériel par la mise en place du logiciel à
l'interface de l'humain et de la machine, l'entreprise Microsoft emploie la
métaphore de la fenêtre (_window(s)_) à travers laquelle l'usager voit le
numérique, et donc l'ordinateur.
Pourtant, il ne faut pas s'y méprendre, quelle que soit la fenêtre logicielle,
elle ne permet d'accéder qu'à un certain nombre fini d'instructions.
Alors qu'en tant qu'appareil programmable qui ne se souci pas de la
signification du traitement des informations ni des résultats obtenus,
l'ordinateur semble être un environnement beaucoup plus vaste que ce que cette
fenêtre ne nous laisse croire [@turing_computable_1936].
Plutôt qu'une fenêtre comme ouverture ou passage vers le numérique, il serait
plus juste de considérer cette fenêtre comme une vision du monde parmi d'autres.
Cette vision du monde n'est pas seulement une vision particulière que l'humain a
de la machine car dans ce cas nous serions dans un paradigme anthropocentré et
utilitariste de la machine.
En nous déplaçant de l'autre côté de la fenêtre, on se rend compte que la vision
que porte la machine sur le monde est différente de la notre : la machine
incarne une autre vision du monde sous forme de matrice, où chaque élément
qu'elle perçoit l'est sous forme binaire.
Le monde n'est alors plus que chiffres, calculs et distances, comme c'est le cas
de la proposition de K. Hayles lorsqu'elle remplace Mère Nature par une Matrice
[@hayles_my_2005].

Un début de relation s'instaure entre l'humain et la machine grâce à l'entremise
du logiciel.
À travers cette interface, lorsque l'on touche une lettre du bout du doigt, la
machine devient alors accessible et l'impulsion (électrique) que cette action
génère se transforme en une lettre à l'écran.
Pour autant, cette accessibilité est-elle synonyme de mise en visibilité ?
Le fait que "ça marche" rendrait-il le document visible ?
C'est le rôle de l'interface graphique et des métaphores qu'elle véhicule que de
cacher le fonctionnement même de la machine [@jeanneret_y-t-il_2011].
La déliaison convoquée par Bonaccorsi [@bonaccorsi_fantasmagories_2020] prend
place dès cet instant dans le processus d'écriture puisqu'il ne s'agit pas
seulement de délier le geste de l'inscription mais également de faire
abstraction de tout le processus d'écriture au-delà du geste.
Ainsi, le logiciel aurait une double fonctionnalité : la première est une
médiation qui ouvre le dialogue avec la machine tandis que la seconde en fait
abstraction et la cache, ce qui a pour effet de rendre la machine quasiment
invisible à l'utilisateur.
Cependant, que découvrons-nous lorsque nous retirons ce voile devant la fenêtre
?
Là se dévoile un vaste écosystème constitué de formats, des protocoles et leurs
flux d'informations et de documents, parfois temporaires, voyageant d'une étape
à une autre, prenant forme et se transformant pour suivre un cheminement
prédéfini jusqu'à la création d'un document final que l'utilisateur récupère.
Chacune de ces fenêtres offre finalement une vision particulière d'un document
et un modèle épistémologique qui lui est propre
[@vitali-rosati_editorialization_2018].


Dans la partie suivante, nous étudions le logiciel Stylo à partir de l'écran comme
interface d'échange de signes entre les deux protagonistes, utilisateur et
machine, puis, en dépassant cette surface, et en nous dégageant du prisme essentialiste, nous démontrerons
que les différents agents d'un environnement -- principalement logiciels et humain 
-- sont des dynamiques qui, lorsqu'elles sont agencées dans une configuration
particulière, co-construisent l'écriture.

[détailler le prisme essentialiste en une phrase ou deux]

## Une médiation par l'écrit

### Le logiciel comme architexte

[reunir peut etre ces deux sous-parties]

### L'architexte derrière l'écran

### La page est un doudou

### Le logiciel est une médiation

### Les formats déterminent la sémantique du texte

### Co-écriture entre les agents

- mettre les différentes représentation du texte et les traces qu'elles laissent

### La déprise en main du texte

- inclure les formats pivots de Stylo

## Bibliographie
