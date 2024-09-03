---
title: "Constitution du modèle épistémologique du document primaire dans Stylo"
date: 2024-05-06
---

Note : PB globale : quelle épistémologie du document numérique pour les
publications scientifiques ?

## Introduction

Lors du chapitre précédent, nous avons défini le document comme étant l'objet au
coeur du processus de publication scientifique.
Qu'il s'agisse des premières revues savantes datant du XVII^e^ siècle ou des
revues numériques contemporaines, des lettres ou encore des livres, un document
est nécessaire pour fabriquer (Fauchié 2024) cet objet éditorial.
Ce document, dans sa forme (format, XXX) et sa struture (Zacklad,
Pédauque ...), et son statut de médiateur (Pédauque) dépasse son statut de simple
support de l'information.
Le support n'est alors plus considéré comme un élément neutre et devient, de par
sa matérialité, un élément constitutif du sens accordé au message qu'il porte.

Puisqu'il n'est pas un simple support, nous nous intéresserons dans ce chapitre 
à la construction de ce document scientifique en milieu numérique.
Comme cela a été énoncé dans le chapitre précédent, un document est un espace
numérique délimité dans lequel sont organisées des informations selon des normes
établies par les impératifs d'une chaîne de traitements, par exemple avec des
protocoles de communication des documents ou encore des formats.

Ainsi, cet espace alloué physiquement dans la mémoire numérique
va subir des modifications et être _redocumentarisé_ (Pedauque, Zacklad)
afin que l'information initiale qui y est contenue puisse être traitée et
transformée en un autre objet ou transportée en un autre espace.
[Ajouter une phrase sur la redocumentarisation]

Les documents numériques ayant pour devenir la publication scientifique
font principalement l'objet d'un traitement éditorial de l'information : saisie du
texte dans un format de traitement de texte ou de texte brut, conversions dans
divers formats de document, transformations du texte source selon des normes
éditoriales ou à la suite d'une relecture par les pairs, publication dans un
nouvel espace selon un format lié à cette action (que l'objet soit imprimé ou
publié en version numérique).

Dans cette chaîne, la réalisation d'un artefact publiable, c'est-à-dire un
document dans sa version finale, nécessite des interactions
entre une multitude d'agents pour advenir, qu'ils soient numériques ou humains.
Qu'il s'agisse de l'adaptation des références bibliographiques à une norme donnée,
de l'ajout des espaces fines insécables dans le texte, de la modification ou
correction de certaines sources d'information, ces étapes de l'élaboration du document
ainsi que toutes les autres proviennent des interactions entre des individus et
l'environnement support [zacklad_organisation_2012; Merzeau] qui produisent des traces à
l'intérieur du document que nous considérons
comme constitutives d'une épistémologie du document.
Elles sont les indices de ces interactions passées et incarnent un modèle de
représentation du document et par extension de la publication scientifique
concernée. 
Plutôt que de nous intéresser au document final tel qu'il est publié, nous nous
focalisons sur les interactions qui le précèdent et sur une épistémologie du
document en cours d'élaboration.

Nous consacrons ce chapitre aux premières interactions à l'origine de la
publication scientifique : la saisie d'un texte.
Pour ce faire, nous observerons les traces issues des interactions entre
un auteur et un ordinateur dans le document numérique^[À chaque fois que nous ferons
référence à l'écriture,
il faudra la comprendre comme l'écriture scientifique en environnement numérique sauf
mention différente.].

En ce sens, l'acte d'écriture numérique n'est plus défini en tant que
fruit d'une seule fonction auctoriale, mais l'est par un ensemble de fonctions
éditoriales dont la fonction auctoriale fait partie.

Ainsi, parmi toutes les fonctions éditoriales que l'on pourrait énumérer, nous nous
intéressons dans ce chapitre à la saisie du texte et à l'environnement support
[@zacklad_organisation_2012] dans lequel il s'inscrit.
Lors de cette phase de l'écriture, cet environnement devient le lieu où se
manifeste un trouble entre ce que l'usager à l'intention d'écrire et le document
que produit la machine, qui est structuré selon les formats et protocoles
implémentés à l'intérieur de l'environnement.
Ce trouble nait de la rencontre entre une représentation du document structuré
graphiquement et une représentation du document structuré par du texte, comme
c'est le cas pour une page web interprétée par un navigateur et son pendant au
format HTML.
Notre intérêt se porte plus particulièrement sur le côté
machine de cette interaction humain-machine, sur le modèle textuel de représentation,
et comment cette machine reçoit
et traite les informations pour produire le document à travers un environnement
particulier.

Afin de traiter cette problématique, nous nous appuyons dans un premier temps
sur les particularités de l'écriture numérique
[@bouchardon_lecriture_2014; @crozat_ecrire_2016; @souchier_numerique_2019] et
sur le fonctionnement de la machine pour illustrer, dans une deuxième partie,
le rôle de médiation joué par les logiciels -- entendus comme une suite
d'instructions écrites -- entre la saisie du texte au clavier et les
traitements appliqués à ces informations, jusqu'à leur stockage dans une mémoire
informatique. 

Tandis que chaque environnement a ses propres modalités d'écriture que nous ne
pouvons pas toutes énumérer, nous nous appuyons dans la deuxième partie de ce
chapitre sur l'étude de l'éditeur de texte sémantique Stylo et les différentes
représentations du texte qu'il génère.
Ces représentations intermédiaires circulent entre les
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
soutenu depuis 2020 par la Très grande infrastructure de recherche Huma-Num.
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
travers plusieurs fonctionnalités fondatrices ou plus récentes qui s'inscrivent
dans le domaine des technologies de l'édition
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
En s’appuyant sur Pandoc, un outil de conversion de documents désigné comme le
« couteau suisse de l’édition », le module d’export de Stylo génère les formats
de sortie PDF (avec l’aide de LaTeX), HTML, XML-TEI, DOCX ou encore XML
compatible avec le schéma COMMONS commun à Métopes, Cairn et OpenEdition.

Le choix d'étudier Stylo comme terrain pour cette recherche découle de plusieurs
raisons.
Tout d'abord, il s'agit d'un éditeur moderne construit avec les technologies du
Web les plus récentes.
Que ce soit à travers des environnements tels que Stylo, GoogleDoc, Hedgedoc ou
encore Framapad, les environnements d'écriture en ligne (Web) suscitent un
certain engouement auprès des utilisateurs notamment pour leur capacité à offrir
un espace de travail collaboratif en temps réel leur permettant d'écrire à
plusieurs dans cet espace.
La deuxième raison qui fait de Stylo un terrain opportun est l'accessiblité de
son code source.
Contrairement à d'autres éditeurs propriétaires comme l'est GoogleDoc, la
totalité du code de Stylo est disponible en ligne, ce qui est indispensable pour
notre étude.
Enfin, le fait d'être impliqué dans les développements de Stylo depuis plus de
deux ans m'offre une position privilégiée pour étudier cet éditeur puisque j'ai
accès aux différentes phases de tests des développements, me permettant ainsi
d'observer le comportement des nouvelles fonctionnalités et de participer à
leur  modification.
Grâce à cette position, j'ai également un accès direct à la communauté
d'utilisateurs, s'élevant à un peu plus de 6000 personnes fin 2023 pour plus de
40 000 documents différents.  
Du fait de mon implication dans Stylo, le regard que je porte sur ce terrain
n'est pas neutre et relève d'une forme de recherche-action [ajouter une
référence].

Alors que chaque signe et chaque trace inscrite dans l'éditeur de texte Stylo
incarne cette tension _entre_ l'utilisateur et la machine, dont les différences
de langage -- naturel et machine -- rend a priori toute communication directe
impossible, nous analysons les différents modes de communication des
informations dans Stylo pour suivre la circulation de ces traces et leur
empreinte dans le document.
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

À partir de cette étude, nous verrons qu'à l'intérieur de cet _entre_, les
traces de cette relation manifestent d'une composante aveugle de
l'écriture, puisque cette dimension de l'écriture n'est pas directement visible
pour l'auteur et relève alors d'une forme de déprise [sauret__2020] sur le texte
où se niche un aspect à notre connaissance ignoré de l'épistémologie du document.

## Écrire dans un environnement numérique

### Définir l'environnement où écrire

Par habitude, nous partons du présupposé que lorsque nous évoquons les mots
environnement d'écriture numérique, ceux-ci sont synonymes d'un environnement
d'écriture informatique et désignent la même chose.
En conséquence, lorsqu'il s'agit de convoquer l'écriture numérique, nous pensons
tout de suite à un ordinateur, aux claviers, aux écrans et aux pointeurs qui
clignotent dans des éditeurs de texte ou dans les champs des formulaires en
ligne.
Avec le numérique ubiquitaire [@citton_angles_2023], ces pratiques d'écriture
sont ancrées dans nos habitudes au point de ne plus les remettre en question.
Les dispositifs d'écriture analogique sont ainsi renvoyés à l'état de vestiges
archaïques, comme peuvent l'être les machines à écrire alors qu'elles ont été
fabriquées méticuleusement par des designers et des ingénieurs et ont
fait la fierté et la renommée de certaines entreprises comme Olivetti en Italie
juste avant que les ordinateurs n'arrivent sur le marché.
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
Cet ordinateur, équipé du processeur Intel 80C85 en 8-bits, pouvait également se
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
dans les bureaux, que ce soit dans les sphères professionnelles et personnelles.

La fin des années 1970 et les années 1980 marquent un tournant décisif pour
l'ordinateur personnel avec l'apparition des logiciels de traitement de texte et
la bataille qui sévit durant toute cette période pour en avoir le monopole.
M. Kirschenbaum et T. Bergin détaillent dans leurs travaux cette course au
développement de logiciels durant cette période pour obtenir un monopole sur le
marché de l'écriture avec un ordinateur
[@bergin_origins_2006; @bergin_proliferation_2006; @kirschenbaum_track_2016].
Avant l'engouement pour les interfaces graphiques et les gestionnaires de
fenêtres -- 1983 et 1984 avec l'entreprise Apple qui s'est largement inspirée
des interfaces graphiques développées par Xerox PARC dans les années 1970 -- la
seule interface affichée à l'écran était un terminal, un écran noir où clignote
un curseur.
Dans cette interface, la navigation s'y faisait au moyen de commandes.
Les premiers logiciels de traitement de texte comme Electric Pencil ne
permettent pas alors une gestion de la mise en page idéale ni ne fonctionnent sur
tous les modèles d'ordinateurs présents sur le marché^[Un autre logiciel comme
`TeX` développé en 1984 par Donald Knuth tente de résoudre ce problème de la
mise en page selon une approche WYSIWYM, que D. Knuth nomme
_Literate programming_ [@knuth_literate_1984] alors que la tendance est plutôt aux
interfaces WYSIWYG].
Ainsi, écrire sur un support connecté paraît aujourd'hui être une évidence alors
qu'il a fallu déployer de lourds efforts à une époque ou cette évidence était
incertaine.

L'écriture numérique est ainsi à distinguer de l'écriture dans un environnement
numérique : un ordinateur, Internet, le Web, une calculatrice ou une machine à
écrire de la dernière génération.
En tant qu'abstraction, l'écriture numérique est une représentation du monde
donnée, dont la qualification à travers un medium permet de l'incarner
physiquement et matériellement mais pas de la circonscrire.
En somme, cette représentation numérique du monde n'est pas nouvelle et ce n'est
pas l'ordinateur qui l'a apporté.
À notre connaissance, son origine remonte aux prémisses de l'écriture et des
développements des systèmes monétaires, nous dirait C. Herrenschmidt
[-@herrenschmidt_trois_2023].

Dorénavant, lorsque nous ferons référence à l'écriture numérique nous parlerons
d'une écriture numérique dans un environnement informatique.

### Les particularités de l'écriture numérique

Avant d'entamer une réflexion sur l'écriture numérique, convenons d'une brève
définition de l'écriture, car celle-ci a fait couler beaucoup d'encre
à son sujet, notamment depuis sa reconfiguration numérique au crépuscule
du 20^e^ siècle.
La définir tient généralement de la philosophie depuis Platon [phèdre],
de l'anthropologie [Leroi-Gourhan; Goody], des lettres [Christin], de
l'archéologie ou de la linguistique [Herrenschmidt], de la sémiotique
[Souchier, Jeanneret, Pedauque] ou encore des sciences de l'information et de la
communication [Bouchardon, Bachimont] ou de l'étude des médias [Kittler]
et cela pour ne mentionner qu'une infime partie des textes traitant ce sujet
parmi un nombre restreint de disciplines de la sphère académique.
Très largement, l'écriture est entendue comme « mode d'expression » et
« fonction de communication » au sein d'une société [@christin_origines_1999].
Anne-Marie Christin distingue deux tendances principales de l'origine de
l'écriture : l'écriture selon la trace, étant soit comprise comme le signe
verbal transposé sur un support soit comme la marque laissée par un corps, soit
l'écriture selon le signe dans son sens étymologique d'« événement inaugural
[qui] participe d’une révélation » tant qu'il s'inscrit dans un « système »
telle
que la disposition des entrailles d'une bête sacrifiée lors d'une cérémonie
[@christin_origines_1999; @vitali-rosati_quest-ce_2020-1].
À défaut de prendre parti pour l'un ou l'autre de ces paradigmes, nous pouvons
retenir deux caractéristiques qui leur sont communes et que l'on retrouve dans
tous types d'écriture, même numérique.
Lorsque l'écriture est convoquée, elle fait appel à deux actions : l'inscription
et l'interprétation [@pedauque_document_2006].
Qu'il s'agisse d'une trace ou d'un signe, retenons que l'écriture est toujours
inscrite sur un support et que cette inscription fait l'objet d'une lecture
et d'une interprétation.
Cette association apparaît régulièrement dans les travaux qui traitent de
l'environnement numérique, par exemple sous l'appellation de littératie
numérique chez Milad Doueihi [-@doueihi_grande_2011] ou de lettrure chez
Emmanuel Souchier [-@souchier__2012].

Toutefois, l'écriture numérique diffère d'une écriture plus traditionnelle,
telle que nous venons de la défnir, et se
distingue notamment par trois caractéristiques que sont la
calculabilité [@crozat_ecrire_2016], la variabilité [@bouchardon_lecriture_2014]
et la rupture sémiotique entre le geste d'écriture et l'inscription sur le
support [@pedauque_document_2006; @souchier_numerique_2019].

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
Comme McLuhan nous le rappelle dans son ouvrage _Pour comprendre les médias_
[-@mcluhan_pour_1977], les alphabets
composés de lettres (contrairement à ceux composés de pictogrammes) sont
asémantiques. Si toutefois les alphabets sont liés à une culture d'où ils
émergent, l'abstraction nécessaire pour représenter le monde sous forme de
chiffres détacherait a priori cette vision de tout sens.
En dehors de tout modèle mathématiques abstrait, et cela quel que soit le
langage ou la base utilisée pour l'écrire, `3`, `trois`, `three`, `III`, `0011`,
`zéro zéro un un`, un chiffre ne signifie pas grand-chose s'il n'est pas associé
à un système de valeurs particulier, par exemple le système métrique ou le
système international [@herrenschmidt_trois_2023].
En échange de cette perte de signification, l'écriture numérique y gagne cette
particularité d'être calculable et mesurable.

L'écriture numérique se distingue également des autres types d'écriture par une
troisième caractéristique.
Il s'agit de la première forme d'écriture où le geste d'écrire ne correspond pas
à l'action d'inscription du signe sur son support, phénomène que J. Bonaccorsi
nomme également déliaison [@bonaccorsi_fantasmagories_2020].
Lorsqu'on appuie sur une touche du clavier, par exemple la lettre `a`, elle ne
s'inscrit pas dans l'écran : l'instruction d'inscrire un signe dans la
mémoire de l'ordinateur est d'abord donnée à la machine, puis vient ensuite celle
de l'afficher à l'écran au moyen d'un logiciel particulier [@kittler_mode_2015;
@souchier_numerique_2019].
Néanmoins, le fait d'appuyer sur une touche du clavier lorsque l'ordinateur est
sous tension ne suffit pas pour déclencher cette instruction : si aucun
environnement dédié à l'écriture n'est préalablement exécuté, le fait d'enfoncer
une touche ne déclenchera aucune réaction de la part de la machine.
Par contre, lorsque l'on se situe dans un environnement où cette réaction est
attendue, comme un éditeur de texte, la frappe d'une touche déclenchera un
événement et le logiciel pourra générer l'instruction correspondant à l'action
d'écrire. 

Ces trois caractéristiques de l'écriture numérique ne sont pas uniquement des
propriétés qui s'ajoutent à l'existant et, d'une certaine manière, rendrait
l'écriture plus complexe.
L'écriture, nous l'avons évoqué, peut être ramenée aux actions d'inscription
dans la matière et de lecture.
Or, la calculabilité, la variabilité et la déliaison entre geste et inscription
perturbent notre définition de l'écriture puisque l'inscription et la lecture
des signes et/ou traces sur le support numérique sont des actions réalisées par la
machine et ne le sont plus par l'être humain, comme le souligne F. Kittler [@kittler_mode_2015].
F. Kittler poursuit sa réflexion plus loin jusqu'à soutenir, de manière
provocatrice, que l'humain n'écrit plus et qu'à l'ère du numérique, c'est la
machine qui écrit.
À défaut de prendre cette provocation au pied de la lettre, elle ouvre la
perspective d'une machine qui participe et contribue à l'écriture et, ce
faisant, participerait à la production d'une épistémologie du texte et du
document.

Seulement, la "machine" ou l'"ordinateur" sont des appellations
un peu vagues et ne rendent pas très explicite les
éléments qu'elles désignent, ni ceux qui sont impliqués dans cette action
d'écriture et dans cette relation entre humain et machine.

### La machine, une entité formée du couple matériel/logiciel

La représentation d'un ordinateur est souvent associée à un couple matériel /
logiciel.
La partie matérielle concerne tous les composants électroniques (carte mère,
mémoires, périphériques, etc.), alors que la partie logicielle englobe tous les
programmes permettant d'interagir avec la partie matérielle, comme le BIOS
(_Basic Input Output System_), le système d'exploitation ou encore un logiciel
de traitement de texte comme LibreOffice.

Ce couple matériel / logiciel range l'ordinateur dans la catégorie des appareils
programmables.
La plupart de nos appareils du quotidien ne sont pas programmables : ils
exécutent ce pour quoi ils sont conçus et ne font rien d'autre.
Dans le cas d'un ordinateur ou d'un téléphone intelligent, ou de tout autre
appareil programmable, leur conception prévoit qu'ils soient manipulables :
ils n'ont pas de fonction précise, néanmoins ils sont capables de répondre à
plusieurs fonctions.
Un ordinateur qui n'a aucune instruction ne pourra rien faire une fois alimenté.
C'est là que les logiciels interviennent : ils permettent un usage déterminé
d'un ordinateur en manipulant des informations de façon à exécuter une suite
d'instructions formelles.

Pour fonctionner, un ordinateur n'a besoin que des éléments suivants : une
alimentation, un processeur, une mémoire vive, des entrées et sorties et une
carte mère auxquels viennent s'ajouter un certains nombres de périphériques
(écrans, souris, clavier, etc.), des extensions pour prendre en charge une
partie des calculs que l'on peut appeler des cartes filles (carte son, carte
graphique) et des mémoires de stockage (disques durs).

Le processeur, ou microprocesseur pour les ordinateurs modernes, est le
calculateur central de l'ordinateur, c'est cet élément qui manipule toutes les
données à traiter -- que l'on appelle aussi le(s) coeur(s) de l'ordinateur.
Chaque modèle de processeur à une architecture qui lui est propre, ce qui veut
dire que chacun traite les informations différemment (même si le résultat
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
programmes et tables d'encodage, rendant ainsi "possible" la transposition des
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
Néanmoins, ce n'est pas parce qu'un encodage est reconnu en tant que norme que
son usage est effectif à l'instant même de sa reconnaissance.
Il faut attendre 1968 que le président des États-Unis d'Amérique Johnson demande
à ce que l'ASCII devienne la norme fédérale d'encodage des informations afin de
réduire les incompatibilités au sein des réseaux de télécommunication pour
qu'elle commence à se répandre.
Dès 1969, tous les ordinateurs achetés par le gouvernement des États-Unis
étaient compatibles avec la norme ASCII.
Du côté des ordinateurs personnels, il faudra attendre le début des années 1980
pour que cette norme se répande grâce, entre autres, à son implémentation dans
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

Pour pouvoir utiliser ces tables d'encodage et stocker des données dans la
mémoire d'un ordinateur, les utilisateurs ont besoin d'une interface les rendant
accessibles et manipulables.
Ces interfaces peuvent être rangées sous l'appellation de logiciel.
Il est intéressant d'introduire les logiciels et leur fonctionnement à partir du
matériel composant l'ordinateur et plus particulièrement à partir de la carte
mère.
Les fournisseurs de carte mère incorporent généralement dans leur carte une
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
leur BIOS du fait de l'ajout par Intel, à partir de 2006, d'un sous-programme
nommé _Management Engine_ (ME) qui est accompagné d'un ensemble de modules comme
_Boot Guard_ et _Secure Boot_ dont l'objectif est de veiller à ce qu'il n'y ait
pas de corruption du système d'amorçage de l'ordinateur^[Des informations sur ce
sujet sont disponibles à cette adresse sur le site web de libreboot :
https://libreboot.org/faq.html#what-systems-are-compatible-with-libreboot ou
dans la documentation des matériels d'Intel :
https://www.intel.com/content/www/us/en/search.html?ws=idsa-default#q=boot%20guard&sort=relevancy&f:@tabfilter=[Developers],
consultés le 03 avril 2024.].
Ces programmes ont sans cesse été améliorés depuis
leur introduction en 2006 et, aujourd'hui, ils empêchent toute modification de
cette couche logicielle, la plus basse d'un ordinateur, si celle-ci n'est pas
vérifiée et validée (avec un système de clés cryptées) par la firme
propriétaire/fabricante.
Il y aurait donc, au plus bas niveau d'abstraction matérielle dans un
ordinateur, une impositionaux utilisateurs d'une vision de la machine réalisée
par les quelques sociétés qui détiennent le monopole de la production de ce
composant. 

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
le processeur ou encore l'allocation de la mémoire, etc.
Malgré le fait que ça n'ait pas toujours été le cas, les applications logicielles
sont maintenant installées à l'intérieur des systèmes d'exploitation et prêtes à être
exécutées.
Le passage par un système d'exploitation permet aux logiciels de ne plus
dépendre d'un modèle particulier du _hardware_ et d'en faire justement
abstraction, les rendant ainsi opérables sur différentes machines.

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
Alors qu'en tant qu'appareil programmable qui ne se préoccupe pas de la
signification du traitement des informations ni des résultats obtenus,
l'ordinateur semble être un environnement beaucoup plus vaste que ce que cette
fenêtre ne nous laisse croire [@turing_computable_1936].
Plutôt qu'une fenêtre comme ouverture ou passage vers le numérique, il serait
plus juste de considérer cette fenêtre comme une vision du monde parmi d'autres.
Cette vision du monde n'est pas seulement une vision particulière que l'humain a
de la machine car dans ce cas nous serions dans un paradigme anthropocentré et
utilitariste de la machine.
En nous déplaçant de l'autre côté de la fenêtre, on se rend compte que la vision
que porte la machine sur le monde est différente de la nôtre : la machine
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
cacher le fonctionnement même de la machine [@jeanneret_y_2011].
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
machine, puis, en dépassant cette surface, et en nous dégageant du prisme
essentialiste^[Cette dimension essentialiste propre à l'interaction est
détaillée dans le chapitre 1 (ajouter lien)], nous démontrerons que les
différents agents d'un environnement -- principalement logiciels et
humain -- sont des dynamiques qui, lorsqu'elles sont agencées dans une
configuration particulière, co-construisent l'écriture.


## Une médiation par l'écrit

### Le logiciel comme architexte

Sans l'intervention du logiciel entre l'être humain et la machine, il ne serait
pas possible pour un auteur d'écrire sur le support de l'inscription numérique.
Si l'on considère l'écriture comme le geste d'inscrire une trace ou un signe sur
un support, alors l'écriture numérique n'est plus un fait humain mais un acte
réalisé par l'ordinateur lui-même.

L'interaction entre un humain et une machine consiste, comme nous l'avons vu, en
une série d'instructions que donne l'utilisateur à la machine qui, ensuite, les
exécute.
Le mécanisme sous-jacent à ce que l'on considère communément comme l'écriture
numérique -- frapper une touche du clavier et voir la lettre s'afficher à
l'écran -- s'avère être plus complexe.
Le moment de la frappe n'est plus le moment où le symbole que l'on voit figurer
sur la touche du clavier est inscrit dans le disque dur, il s'agit plutôt du
moment où une instruction est donnée à l'ordinateur qui ensuite se charge
d'inscrire la lettre correspondante sur le disque dur.
Si l'on se trouve dans le cas de figure de la saisie d'un texte dans un éditeur
de texte, l'instruction suivante, selon les logiciels et les actions souhaitées,
consiste à afficher à l'écran le symbole encodé dans la mémoire de l'ordinateur.

Pour réaliser cette suite d'actions, Yves Jeanneret et Emmanuël Souchier partent
de ce constat qu'il n'est pas possible d'écrire un texte numérique sans qu'un
autre texte soit déjà présent pour réaliser cette action.
Ce texte particulier qui pré-existe toute activité numérique est nommé
architexte [@souchier_numerique_2019].

L'architexte est un concept d'abord employé par Gérard Genette
[-@genette_introduction_1979] et désigne « l'ensemble des catégories générales,
ou transcendantes -- types de discours, modes d'énonciations, genre littéraires,
etc. --, dont relève chaque texte singulier ».

En 2019, dans leur ouvrage intitulé _Le numérique comme écriture_, G. Gomez
Mejia, W. Candel et E. Souchier résument l'architexte numérique comme :

> Initialement défini comme "écriture d'écriture" puis comme un "dispositif
> d'écriture écrit", l'architexte s'avère être un point de passage obligé pour
> toute activité numérique. Il n'y a effectivement pas d'écriture à l'écran sans
> un architexte qui la rend possible, l'accompagne et la formate. Pour la
> première fois de son histoire, l'homme a donc recours à des "dispositifs
> d'écriture écrits" spécifiques pour pouvoir pratiquer une activité d'écriture
> (E. Souchier, 1998, 2013). Or, précisément en ce qu'ils sont "eux-mêmes
> écrits", les architextes "sont des textes lisibles et interprétables. Porteurs
> et prescripteurs d'une écriture à venir, ils anticipent de ce fait une figure
> de l'auteur" (É. Candel, G. Gomez Mejia, 2013) et relèvent donc de
> "l'énonciation éditoriale" (E. Souchier, 1998).

Globalement, l'architexte incarne le cadre dans lequel les agents peuvent
écrire.
Il permet de faire la distinction entre un gabarit, entendu comme l'espace
proposé par les éditeurs de logiciels ou applications pour écrire, et le texte
saisi par l'utilisateur, c'est-à-dire le texte qui remplit le gabarit.
Cet architexte, ce cadre, est régi par des règles qui définissent comment l'on
peut écrire sur un support numérique mais également comment les caractères à
inscrire doivent être formatés.

Nous l'avons vu, l'architexte se positionne en tant que médiateur entre un
auteur et la machine qu'il emploie pour écrire.
Jusqu'à présent, la définition de l'architexte englobe largement tous les écrits
qui permettent d'écrire à l'écran.
En 2019, G. Gomez-Mejia, E. Souchier et E. Candel précisent ce que sont ces
méta-écritures et en dressent une typologie composée de quatre « cadres d'écrits
d'écran » :

- le matériel
- le système
- le logiciel
- le document

Le premier cadre, matériel, désigne toute la composante physique de l'ordinateur
et surtout l'écran sur lequel est affiché le texte.
Le cadre système, quant à lui, est associé à la couche permettant de générer un
environnement d'écriture numérique, initialisé par le BIOS et par le démarrage
du système d'exploitation qui constitue le deuxième élément principal du cadre
système.
Le cadre logiciel est relatif à l'ensemble des logiciels que l'on peut exécuter
dans un système d'exploitation, par exemple un terminal, un navigateur ou un
traitement de textes.
Enfin, le dernier cadre est celui du document.
Le document doit être compris comme un objet, ou une forme déterminée, à
l'intérieur duquel des éléments sémiotiques sont organisés et structurés
[@pedauque_document_2006; @zacklad_design_2019].

Ces cadres sont un début de réponse au dépassement de l'écran.
Néanmoins, plutôt que d'approfondir cette dimension invisible du texte, les
auteurs de l'architexte reviennent sur la couche graphique en ajoutant qu'« à
cet enchâssement de cadres, il faudrait encore ajouter ceux que composent, à
l'intérieur même du document, les rubriques, encadrés, cartouches, "boîtes de
dialogue" ou autres formes de cadres éditoriaux structurants pour le travail
même du texte ».

De plus, toujours selon les auteurs :

> Le premier "cadre" [qui] définit les conditions de possibilités matérielles de
> l'activité, est le seul inanimé. Les trois suivants, cadres système, logiciel
> et document, relèvent de l'ingénierie textuelle et définissent les conditions
> de réalisation de l'activité. On voit ainsi qu'une activité d'écriture
> réalisée sur le "document" d'un logiciel de traitement de texte est mise en
> abyme au sein de l'ensemble des autres "cadres" qui la rendent possible et la
> déterminent techniquement et sémiotiquement.

Ce premier cadre de « l'écrit d'écran » ne désigne en fin de compte, pour les
auteurs, que l'écran.
Or, il n'est pas nommé cadre écran mais cadre matériel et devrait renvoyer à
toute la dimension physique d'un ordinateur et pas seulement à l'organe
d'affichage qui, dans cette disposition, apparaît comme central dans le
fonctionnement d'un ordinateur.

Le dépassement de l'écran devient un acte symbolique nécessaire pour se soustraire à
une vision anthropocentrée des actions de lecture et d'écriture.
Pour effectuer ce changement de perspective, nous devons d'abord nous débarasser
d'un élément central à l'interface de l'humain et la machine : la page.

### La page est un doudou

Le terme _page_ revient de manière récurrente dans nos usages de l'ordinateur :
on le retrouve dans les logiciels de traitement de textes -- il y a même un
logiciel du nom de _Pages_ disponible dans l'environnement Apple --, dans les
livres numériques ou encore dans le Web où chaque URL est l'adresse d'une page.
Matthew Kirschenbaum et Thomas Bergin nous détaillent dans leurs travaux
l'arrivée de la page sur nos écrans durant les années 1970 et le début des
années 1980 [@kirschenbaum_track_2016; @bergin_origins_2006; @bergin_proliferation_2006].

Cet objet qu'est la page a été instauré dans l'ordinateur uniquement pour
reproduire une « habitude » et créer un lien fictif entre les visions du monde
de l'imprimerie et de l'informatique.
Cet artefact produit une forme de réconfort auprès de l'utilisateur pour que le
monde informatique lui semble plus tangible, qu'il ait quelque chose auquel se
raccrocher, d'où sa déclinaison dans des espaces différents qui ne ressemblent
plus du tout à des pages de livres ou de feuilles (par exemple la A4 lettre
US, ou le livre au format poche).
La page affichée à l'écran n'existe qu'à cet endroit, il ne s'agit que d'un
rendu graphique qui ne fait pas partie de l'écriture (au sens du texte saisi).

Le pouvoir de la page sur l'utilisateur est considérable étant donnée la nature
même de cet objet que l'on pourrait considérer comme l'un des seuls à être
virtuel et presque sans matérialité du point de vue de l'informatique.
Malgré tous les efforts effectués depuis son instauration à l'écran, la page
affichée n'est jamais la page imprimée car, aussi précis que soient les détails
typographiques que l'on peut y ajuster, elle ne reflétera jamais le grain,
l'épaisseur, l'odeur ou tout autre caractéristique physique du papier.

La critique énoncée à l'endroit de la page ne doit pas être réduite à une
apologie d'un mode sans page.
Elle consiste à montrer qu'à vouloir préserver une habitude pour _ne pas
effrayer_ l'utilisateur, la page fait écran devant l'ordinateur, et cache la
machine qui ne devient plus qu'un simple mécanisme au lieu d'être un agent de
l'énonciation éditoriale.

Cette peur de l'informatique pourrait relever essentiellement de l'angoise de
l'arrachement d'une valeur qui définie l'être humain et devienne une
caractéristique d'une autre entité, ne permettant plus de définir l'humain en
regard de ce que lui seul est capable de faire (Vitali-Rosati).

Kittler, à ce propos, nous rappelle qu'historiquement les caractéristiques qui
définissent l'être humain sont souvent le symbole du pouvoir et désigne plutôt
les hommes alors qu'à l'instant même où cette caractéristique est déchue de son
statut de marqueur de puissance, ce sont les femmes qui en héritent.
Dans le cas de l'écriture -- dactylographie et sténographie--, elles en
deviennent les expertes dès 1881, au moment même où les ventes de la machine à
écrire Remington II explosent alors que chute le pourcentage d'hommes dans ce
domaine [@kittler_gramophone_2018, p.306]. 
La Remington Model II de 1878 comporte une particularité, il s'agit de la
première machine à écrire comportant une touche SHIFT pour avoir les hauts de
casse et les bas de casse sur le même clavier, pourtant, malgré cette nouvelle
fonctionnalité, les ventes ne se développèrent pas dès cette date.
En 1881, l'entreprise modifie sa stratégie de vente et cible les femmes qui
n'ont pas de travail.
En parallèle, l'Association chrétienne de jeunes femmes de New York commence à
former des jeunes femmes à la dactylographie, fait qui a été ensuite reproduit
en Europe dû à son succès [@kittler_gramophone_2018, p.322].
Il y aurait donc une peur de perdre non seulement une caractéristique de
l'humanité mais surtout une caractéristique de la masculinité.

Néanmoins, avant d'en arriver à cette émotion forte qu'est la peur et qui
traduit une incapacité à définir l'être humain, nous pouvons nous appuyer sur la
pensée de Gunther Anders et convoquer une forme de honte
[@anders_obsolescence_2002] que la page camoufle.

Interagir avec une machine demande une certaine rigueur : qu'il s'agisse de
structurer un document ou de lui donner une série d'instructions (du code), une
machine ne peut interpréter l'ambiguité ou l'implicite culturel.
Cela voudrait dire qu'aucun échange humain-ordinateur ne peut reposer sur des
conventions culturelles de lecture et que l'instruction donnée n'a, en
elle-même, aucun sens.
Dès lors, comment pouvons-nous admettre que quelque chose qui n'a pas de sens
puisse en générer ?

La honte (prométhéenne) d'Anders est alors double : d'un côté il y a un mélange
de fierté devant cette machine créée par l'être humain et de honte parce que
l'individu isolé devant la machine sait que ce n'est pas lui qui l'a mise au
point et, de l'autre, il y a cette honte à être face à un outil qui réalise une
action mieux qu'on ne le ferait soi-même alors que cette dite machine n'a aucune
conscience de ce qu'elle réalise.

Le dépassement de la page et de l'écran est une proposition pour poser un autre
regard non anthrocopentré sur cette question de l'écriture numérique et laisser
de côté les modalités de définition de l'être humain.
Elle signifie qu'il ne s'agit plus de poser la question de l'auteur de
l'écriture, en admettant que c'est bien la machine qui écrit, mais de se
demander comment cette nouvelle fonction (inter)agit entre les agents
d'un système d'informations.
Que se passe-t-il lorsque cet ordinateur devient un agent actif qui écrit et
transmet des informations entre, d'une part, l'instructeur (la personne qui
donne des instructions) et la ou les personnes qui lisent les productions issues
du traitement de ces instructions (les productions écrites) ?
Dans cette configuration s'opère alors un changement radical de l'état de
l'ordinateur.
D'abord à l'état de médiateur puis de support de l'écriture, l'ordinateur passe
maintenant au statut d'entité agissante au sein d'un système d'informations.

### Le logiciel est une médiation

Traverser la page pour atteindre les couches inférieures nous amène à faire escale
sur la couche logicielle.
Le logiciel a un statut intéressant : on le considère souvent comme un
médiateur, un agent qui permet la communication et l'interaction humain-machine,
pourtant ce n'est pas le cas de toutes les recherches.
F. Kittler et sa très célèbre provocation « Es gibt keine Software », traduit
par _Le logiciel n'existe pas_ [-@kittler_mode_2015], nous rappelle que ces
écritures (qui nous permettent d'écrire), sont stockées et traitées par la
machine exactement de la même façon que n'importe quelle écriture numérique.

On retrouve tous ces textes numériques (logiciels et documents) au même niveau
hiérarchique dans l'architecture du système d'exploitation et le traitement qui
leur est appliqué par le processeur est identique.
La nomination des logiciels en tant qu'« écrits qui permettent les écrits
d'écran » par E. Souchier nous mène aussi à cette juxtaposition : finalement le
logiciel est de même nature que le texte que nous y rédigeons à l'intérieur.

Toutefois, une distinction persiste.
Si le texte peut être remédié dans un autre format -- et être imprimé par
exemple --, le logiciel quant à lui ne peut exister que dans son environnement
numérique.
Son code source peut lui aussi faire l'objet d'une remédiation
[@bolter_remediation_1998] mais il sera dénaturé, car sa fonction principale est
l'organisation du traitement des informations dans un ordinateur.
D'ailleurs, C. Herrenschmidt nous rappelle que le terme de logiciel a été forgé
à partir de la contraction du mot "logique" avec le mot "matériel"
[@herrenschmidt_trois_2023, p.474] , pour justement montrer à la fois l'opposition
du logiciel avec l'aspect matériel (_hardware_) et marquer leur
complémentarité : l'ordinateur (_hardware_) serait très peu accessible (voire
inaccessible) sans logiciel, et le logiciel n'existe pas en dehors de
l'ordinateur.

Lorsque l'on définit le logiciel en opposition au matériel, on les place tous
les deux au même niveau -- ils sont des entités équivalentes -- et cela nous
détache de ce que nous avons vu précédemment sur la place du logiciel aux côtés
de n'importe quel document à l'intérieur de la mémoire de l'ordinateur.

Un courant contemporain de la théorie des médias, l'intermédialité
montréalaise^[Le chapitre 1 devra décrire l'intermédialité
montréalaise, il faudra ajouter un renvoi ici] [@muller_lintermedialite_2000; @tadier_tentative_2021; @tadier__2021],
en tant qu'art pour penser les relations
[@tadier__2021], peut être mobilisée pour mieux comprendre les liens
entretenus par les agents de notre système, la machine avec elle-même,
humain-machine, machine-machine.

Ce qui est intéressant dans cette relation -- et que certains systèmes
d'exploitation cachent depuis plusieurs années -- est le fait que logiciel ne
puisse exister que dans un environnement très particulier et fragile.
Pour fonctionner, le logiciel doit être compatible avec plusieurs composants de
l'ordinateur. Les premiers composants sont matériels : est-ce que l'ordinateur a
une carte graphique, quel type de processeur ou la quantité de mémoire vive,
etc.
C'était un fait connu du temps des premiers logiciels comme WordPerfect
[@bergin_origins_2006; @kirschenbaum_track_2016; @kittler_mode_2015] et que l'on
voit de moins en moins aujourd'hui, notamment parce que 1) les logiciels à
installer sont disponibles pour beaucoup de matériels -- exceptés pour certains
jeux vidéos ou des programmes que l'on va préférer faire fonctionner sur des
"machines plus puissantes" avec plus de capacité de calcul -- et 2) parce que le
développement des téléphones intelligents depuis une vingtaine d'années a donné
naissance à un nouveau format d'application : les _progressive web apps_ qui
utilisent les technologies du web (HTML, CSS, JS) pour fonctionner et sont donc
exécutables sur plus de supports puisqu'elles sont agnostiques^[En informatique,
le qualificatif agnostique désigne une ressource indépendante du système au sein
duquel elle se trouve. Par exemple, un logiciel agnostique fonctionnerait de la
même manière sous différents systèmes d’exploitation. Il en gagne ainsi la
propriété d’interopérabilité.] vis-à-vis du système d'exploitation.
L'environnement matériel est donc une première condition pour faire fonctionner
un logiciel.
La deuxième est le système d'exploitation.
En fonction du système d'exploitation -- et de sa version -- un logiciel pourra
y être installé à l'intérieur.
Ce deuxième paramètre ne doit pas être sous-estimé, car l'écosystème des
logiciels fonctionne sur la base d'un système réticulaire : les programmes ne
sont pas développés _from scratch_, ils s'appuient sur d'autres briques
logicielles qui elles-mêmes s'appuient sur d'autres briques logicielles. Chacune
d'entre elles dépend d'une version particulière de l'autre. Si une version
venait à être mise à jour sans vérification préalable, alors le château de
cartes pourrait s'effondrer et le logiciel ne plus fonctionner.

D'ailleurs, une pratique courante en développement informatique consiste à créer
un environnement virtuel -- une bulle -- à l'intérieur même de son ordinateur
pour y installer des versions sélectionnées de dépendances logicielles afin
qu'elles ne soient pas victimes d'un effet de bord dû à une mise à jour d'un
autre programme (et d'autre dépendances).

Le logiciel est un langage de haut niveau qui permet de manipuler des données
jusqu'au plus bas niveau de l'ordinateur, au niveau des entrées et des sorties.
Toutes ces manipulations sont exécutées en appelant des instructions dans ce
réseau de dépendances/logiciels pour que les données puissent descendre les
couches et être transformées jusqu'à atteindre leur espace de stockage dans la
mémoire morte.

Le nom qui désigne un logiciel comme MS Word, Stylo ou LibreOffice désignent
plus que les vagues notions que peuvent être leur fonctionnalité principale,
dans ces cas-ci l'édition de texte, et peuvent être définis par la totalité des
instructions mobilisées dans la manipulation des informations.
À l'instar de McLuhan [-@mcluhan_pour_1977], l'on pourrait percevoir les
logiciels comme des espaces construits -- des architectures de l'information
[@broudoux_larchitecture_2013] soignées -- avec une topologie qui leur est
propre et à travers laquelle chaque suite d'instructions forme une route que des
unités sémiotiques empruntent pour y être transformées en unités calculables.

Chaque environnement d'écriture incarne un modèle et une vision du traitement de
l'information, que l'on peut englober sous le nom de cet environnement.
Lors de l'interaction entre un usager et une machine, par le biais de cet
environnement, les médiations à l'oeuvre sont des représentations de ce modèle
dont les traces présentes dans les documents sont les indices.

En prenant le cas de Stylo, nous pouvons détailler ce que désigne cette
appellation en fouillant l'architecture logicielle, puisque le code est
en libre accès, afin de cibler les traces de cette relation entre l'auteur
et son environnement.

Tout d'abord, Stylo représente un espace sur le Web dans lequel nous pouvons
écrire en suivant la syntaxe de trois formats de texte brut, le Markdown, le
YAML et le BibTeX.
Le Web fonctionne différemment d'un environnement local sur son ordinateur
personnel.

Alain Mille en dresse l'histoire depuis les débuts d'Internet dans les années
1960 [-@mille_internet_2014] à partir du réseau filaire ARPAnet développé par le
département de la défense américaine.
Seulement, comme le souligne A. Mille, il manque une brique pour que naisse
l'Internet : un protocole de transfert des documents.
Le premier protocole a vu le jour en 1969^[Il n'y a pas de corrélation directe
avec l'utilisation de la norme ASCII par les institutions américaines à cette
date, néanmoins on remarque qu'il y a un engouement pour l'informatique à la fin
des années 1960.] et a fait l'objet de la première RFC^[On peut retrouver tout le contenu de cette RFC sur cette page web : https://www.rfc-editor.org/rfc/rfc3.html. Les RFC sont numérotées, dans ce cas-ci il s'agit de la RFC 3, et vont par ordre croissant. Une modification d'un document numéroté fait l'objet d'un nouveau numéro et rend obsolète la version antérieure. Comme on peut la page Web, la RFC 3 est rendue obsolète par la numéro 10, puis la 16, etc.] (_Request for comments_)
avant de trouver une forme plus aboutie dans le protocole TCP en 1974 --
décrit par Vincent Cerf et Bob Kahn -- et permet
avec sa distribution sous forme de paquets la naissance d'Internet.
Ce n'est qu'en 1990, au CERN ((Organisation européenne pour la recherche
nucléaire)), que Tim Berners-Lee participe à la conception du Web -- et du _World
Wide Web_ -- pour pallier le problème d'échanges de documents numériques
rencontré dans cette institution grâce au développement du langage de balisage HTML.
Le Web vient donc répondre à un besoin, celui de la compatibilité des
informations et de leur interoperabilité dans une structure.
En créant un environnement spécifique composé de normes de structuration des
informations interprétable par un logiciel, le navigateur, le Web devient
agnostique et ne dépend plus de la même couche d'abstraction logicielle
qu'un environnement local. 
L'ordinateur devient un terminal, un client à partir duquel on peut se connecter
au réseau et accéder aux informations qui y circulent.

C'est ainsi que sur le Web, l'action de stockage des données est généralement séparée
de l'espace d'affichage dans le navigateur.
Les données sont stockées dans une base de données sur un serveur.
Il y aurait donc au moins deux modules différents, la partie _client_ -- ce qui
est affiché dans le navigateur -- et la partie _serveur_ où sont organisées
les informations. 

Nous retrouvons ce fonctionnement dans Stylo avec la partie serveur et la
partie client auxquelles vient s'ajouter un troisième bloc pour exporter les
données afin de les extraire de cet environnement client - serveur.
L'architecture logicielle de Stylo peut donc être scindée en trois parties.

![Les différents modules de Stylo](https://s3.hedgedoc.org/demo/uploads/afdf01ec-bd0b-4b38-8394-752d6e2d1e4b.png "Les différents modules de Stylo")

Tout d'abord, nous retrouvons la base de données où sont stockées toutes les
informations et données de Stylo : les comptes utilisateurs, les articles, les
espaces de travail, les corpus, etc.
Cette base de données est réalisée avec MongoDB, un système de gestion de base
de données non relationnelles développé en 2007 et s'appuyant sur des documents
structurés au format JSON.

Le deuxième bloc de Stylo est le module d'export qui permet de transformer les
informations saisies et visibles dans l'éditeur en de multiples documents.
Tout ce module est développé et maintenu avec le langage de programmation Python
par David Larlet.
Cette brique technologique est articulée autour du logiciel de transformation et
de conversion Pandoc^[Pandoc est un incontournable pour transformer des
documents. Il a été développé et maintenu en Haskell par son créateur John
MacFarlane depuis 2006.] déployée sur un serveur et rendue accessible via une
autre API^[La pandoc-api est accessible à cet _endpoint_ :
https://pandoc-api.stylo.huma-num.fr/] fabriquée à partir du framework
FastAPI^[FastAPI est disponible à cette adresse : https://fastapi.tiangolo.com/,
consulté le 24 février 2024.].
Le module d'export intégré à Stylo^[On peut trouver le module d'export à cette
URL : https://export.stylo.huma-num.fr/] permet de convertir et de transformer
les textes sources en une multitude d'artefacts, selon les capacités de
transformation et de conversion du logiciel Pandoc auquel il est rattaché.

Le dernier bloc de Stylo concerne l'interface que les utilisateurs voient
affichée sur leur écran.
Étant donné que Stylo est accessible via un navigateur web, l'interface a été
conçue avec les technologies de cet environnement.
On retrouve des objets en HTML, en CSS et en Javascript.
Le _framework_ React, une surcouche à Javascript _open source_ développée par
Facebook (aujourd'hui Meta) en 2013, a été employé pour faire les différents
composants de l'interface et intégrer de nombreuses librairies telle que _i18n_
qui permet d'implémenter le multilinguisme dans l'interface et changer la langue
affichée à l'écran en un seul clic.

L'éditeur de texte, pièce maîtresse de Stylo, s'appuie sur la technologie
Monaco^[Voir le site web dédié à l'éditeur Monaco :
https://microsoft.github.io/monaco-editor/, consulté le 29 février 2024.]
développé par Microsoft et rendu disponible sous licence MIT.

Ces deux blocs, la base de données MongoDB et l'interface web, ne sont
pas en communication directe.
Les champs de texte dans la partie HTML ne permettent pas d'écrire directement
dans la base de données.
En conséquence, un canal de communication devait être établi entre ces deux
objets pour que les données puissent être accessibles à la fois en lecture, pour
l'affichage dans la page web, et en écriture pour ajouter, modifier ou supprimer
des éléments.
Pour mettre en oeuvre cette communication, une API (_Application Programming
Interface_) utilisant le langage de requête GraphQL a été mise en place et
rendue accessible via le protocole HTTP (_Hypertext Transfert
Protocol_)^[L'_endpoint_ de l'API GraphQL de Stylo est accessible ici :
https://stylo.huma-num.fr/graphql.], la surcouche du protocole internet utilisée
pour le web.
Le langage de requête et de manipulation des données GraphQL a également été
développé par Facebook à partir de 2012 puis publié en _open source_ en 2015.

L'une des particularités d'une API GraphQL, contrairement à une API REST par
exemple, est qu'elle sert l'ensemble des données à une seule adresse (_endpoint_)
alors que plus généralement, les données sont accessibles à des URL très
précises, ce qui a pour effet de rendre explicite la structuration des données
dans la base.
En ne servant les données qu'à une seule adresse, l'API s'échappe de la
contrainte de la structuration des données et contourne les problèmes récurrents
d'_over-fetching_ ou d'_under-fetching_ que l'on peut rencontrer dans certaines
applications^[Ces deux problèmes désignent soit une récupération trop importante
de données et nécessite un tri après récupération des données sur le serveur,
soit un manque de données pallié par un deuxième appel ou plus au serveur pour
compléter le besoin.]
L'API GraphQL est donc agnostique à l'égard de la forme de la base de données.
Par contre, la définition de requêtes adressables à la base de données doit être
déclarée pour que l'on puisse faire circuler les informations entre le serveur
et le client.
Pour effectuer cela, GraphQL à son propre langage de description de schéma (SDL,
_Schema Definition Language_) et permet de déclarer explicitement les
différentes façons d'écrire une requête.

Par exemple dans Stylo, le champ `user` contient les informations suivantes^[La
modélisation du schéma GraphQL de Stylo est accessible sur le dépôt Github à
l'adresse
suivante :https://github.com/EcrituresNumeriques/stylo/blob/master/graphql/models/user.js] :

- _id
- displayName
- username
- authType
- email
- firstName
- lastName
- institution
- tags
- permissions
- acquintances
- articles
- workspaces
- admin
- yaml
- zoteroToken
- createdAt
- updateAt
- apiToken
- addContact
- removeContact
- stats

Une requête simple consisterait à vouloir récupérer l'adresse courriel liée à
mon compte utilisateur: 

```graphql
query usermail {
    user {
        email
    }
}
```

et renverrait comme réponse :

```graphql
{
    "data": {
        "user": {
            "email": "roch.delannay@umontreal.ca"
        }
    }
}
```

Cet exemple montre qu'il y a une certaine économie de l'information implémentée
dans le fonctionnement même de GraphQL pour n'aller chercher que les
informations nécessaires pour une requête particulière, pour peu que la requête
en elle-même soit bien rédigée.
D'ailleurs, il s'agit là d'un des écueils potentiels de GraphQL : des requêtes
mal formulées peuvent aller à l'encontre de ce principe.

Dans Stylo, chaque fonctionnalité, chaque bouton (ou presque) qui réalise une
action de lecture ou d'écriture est lié à une requête GraphQL et au schéma de
donnée correspondant.
Chacune de ces actions suit en conséquence une modalité d'inscription dans la
base de données se conformant à l'architecture implémentée lors des développements de
Stylo et produit une vision du document. 
 
Le protocole HTTP comporte deux méthodes bien connues pour faire circuler des
informations entre un client et un serveur : `GET` et `POST`.
Un des arguments phares présenté par GraphQL est sa dimension agnostique par
rapport au protocole de communication des informations employé, que ce soit HTTP
ou des WebSockets ou autre.
Pourtant, malgré la capacité de GraphQL à être utilisable avec toutes les
méthodes d'HTTP^[Voir https://graphql.or/learn/serving-over-http/, consulté le
24 février 2024.], une bonne pratique appliquée par la communauté GraphQL est
l'emploi du protocole HTTP couplé à la méthode `POST` pour tous types de
requêtes (que ce soit une `query`, une `mutation` ou encore une `subscription`).
Lors de la transmission des informations par la méthode `GET`, toutes les
informations sont insérées dans l'URL ce qui 1) les rend visibles (et
vulnérables) et 2) impose une limite du nombre de caractères (aux alentours de
2000 au maximum) au risque de déclencher une erreur 414 (URL trop longue).
En conséquence, il est préférable d'utiliser la méthode `POST` pour envoyer ou
récupérer des informations, car elles ne seront ni visibles ni limitées en
longueur.
Malgré l'aspect agnostique de GraphQL, la forme textuelle des requêtes implique
en elle-même un choix particulier de transmission des informations avec ce qu'il
comporte comme avantages et inconvénients.

Les spécificités du protocole HTTP sont définies dans les _Request for
Comments_ (RFC) publiés par l'_Internet Engineering Task Force_ (IETF) fondée en
1986 et dont le siège se trouve aux États-Unis.
Les documents et leurs contenus sont régulièrements mis à jour par la communauté
qui participe à ces commentaires.
Le numéro de la RFC en lien avec la méthode `POST` est le 9110^[Voir la page web
https://www.rfc-editor.org/rfc/rfc9110#name-introduction, consultée le 24
février 2024.] publié en juin 2022.

La méthode `POST` est définie dans le paragraphe 9.3.3 comme :

> The POST method requests that the target resource process the representation
> enclosed in the request according to the resource's own specific semantics.
> For example, POST is used for the following functions (among others) :
> - Providing a block of data, such as the fields entered into an HTML form, to
>   a data-handling process;
> - Posting a message to a bulletin board, newsgroup, mailing list, blog, or
>   similar group of articles;
> - Creating a new resource that has yet to be identified by the origin server;
>   and
> - Appending data to a resource's existing representation(s).^[Traduction
>   personnelle : La méthode POST demande à la ressource cible de traiter la
>   représentation incluse dans la demande selon sa propre sémantique. Par
>   exemple, la méthode POST est utilisée pour les usages suivants (parmi
>   d'autres) : Fournir les blocs de données, comme les champs d'un formulaire
>   HTML, à un traitement de données ; Publier un message sur un tableau
>   d'affichage, un groupe d'échange, une liste de diffusion, un blog ou un
>   groupe d'articles similaire ; Créer une nouvelle ressource qui n'a pas
>   encore été identifiée par le serveur d'origine ; et Ajouter des données à la
>   (aux) représentation(s) existante(s) d'une ressource.]

À travers cette brève définition, l'on remarque que l'usage principal de la
méthode `POST` est plutôt relatif à l'envoi d'informations, qu'elles soient
nouvelles ou mises à jour.
Le comportement de `POST` fait toutefois débat, notamment quant à son usage pour
l'envoi de certaines informations puisque, comme cela est indiqué dans sa
définition, `POST` laisse le soin au serveur (la ressource cible) de traiter les
données contenues dans son message selon sa propre sémantique.
En somme, contrairement à d'autres méthodes comme `PUT`, `POST` n'est pas
idempotente^[L’idempotence signifie qu’une opération a le même effet et cela
quel que soit le nombre d’application.], ce qui pourrait entraîner des
différences de résultat lors de l'exécution d'une requête.
Par exemple, la duplication d'une requête en cas de problème de connexion.
Au contraire, une méthode idempotente comme `PUT` ou `DELETE` aurait le même effet
du côté du serveur et cela quel que soit le nombre de fois que cette requête lui
aura été envoyée : une ressource supprimée ne le sera qu’une fois.

Cependant, cette caractéristique tend à disparaître dans le cas de l'utilisation
de `POST` avec une structure GraphQL puisque cette dernière ne dépend pas d'une
architecture composée de multiples adresses (une pour chaque ressource) mais
d'une seule adresse à laquelle on soumet des requêtes.
Dans le cas de Stylo, `POST` est donc soumis à l'architecture GraphQL, on peut
donc bien considérer GraphQL agnostique à l'égard de la méthode `POST` du
protocole HTTP.

Enfin, dans le cas d'une requête `POST`, le contenu à envoyer sur le serveur est
formaté en JSON.
Ci-dessous un exemple de requête `POST` envoyée depuis l'interface Web de Stylo
vers le serveur :

```JSON
{"query":"query updateWorkingVersion(articleId: ID!, $content:
WorkingVersionInput!)
{\n
article(article: $articleId) {\n
updateWorkingVersion(content: $content) {\n
updatedAT\n
}\n
}\n
}",
"variables":{"userId":"61d62.....",
"articleId":"65e0e38129637c0012ef7a",
"content":{"md":"Ajout du texte pour la requête HTTP 'POST'"}}}
```

Autrement dit, chaque fonctionnalité décrit de manière formelle la structuration
des informations dans Stylo, donc ce que Stylo écrit dans la base de données et
dans les textes puisque ce sont les informations renseignées qui seront
intégrées dans les documents exportés.
En ce sens, Stylo et ses protocoles pré-construisent la totalité de ce qu'un
utilisateur peut saisir dans l'interface et sera enregistré dans la base de
données.
Cette préconstruction est la vision du document incarnée dans Stylo.
Puisqu'il y a une pré-construction du document et du texte, nous pouvons à ce
stade présupposer qu'il y a une pré-construction des traces issues des interactions avec
l'utilisateur et qu'elles se matérialisent dans des
fragments comme celui présenté ci-dessus.

Cette description très générale des moyens de communication à l'oeuvre entre les
différents modules de Stylo nous montre déjà que l'information saisie dans cet
éditeur de texte est formatée par une architecture de données alors que nous
n'avons pas encore abordé les conditions de l'écriture avec les trois formats
pivots d'un document dans Stylo.

### Les formats déterminent la sémantique du texte

[Trouver quelques références sur les formats, ex la these de de Mourat sur le
vacillement des formats]

Selon les formats d'écriture, et lorsque l'on sort du paradigme WYSIWYG pour
celui du WYSIWYM, on s'émancipe de la surcouche de mise en page pour entrer
directement dans la couche de la structuration des contenus, là où les formats
remplacent la couche supprimée par une autre couche graphique et rendent leur
structure visible.

_What You See Is What You Get_, ou WYSIWYG, est l'acronyme généralement employé
pour désigner les outils qui adoptent une surcouche graphique de gestion de la
mise en page des contenus d'un document, au risque de ne pas structurer les
informations qu'il contient avec finesse.
Le paradigme opposé, _What You See Is What You Mean_ (WYSIWYM), distingue la
mise en page graphique des éléments du texte de leur structuration.
Les formats employés sont généralement du texte brut et permettent dans la
plupart des cas de baliser le contenu pour définir la nature des éléments à
décrire.
C'est le cas, par exemple, de tous les langages de balisages hérités de SGML
(_Standard Generalized Markup Language_) tels que HTML ou XML mais également les
langages de balisage léger comme Markdown, AsciiDoc, reStructuredText, etc.

À ce stade, l'agent humain ne dépend pas d'un logiciel particulier pour saisir
son texte puisque la saisie d'un texte dans un format _plain text_ peut l'être dans
n'importe quel environnement.
Écrire en texte brut signifie également ouvrir les possibilités de structuration
du texte : ce n'est plus un logiciel de traitement de texte, MSWord, GoogleDoc
ou LibreOffice qui décide de l'organisation des connaissances à l'intérieur du
document, suivant un phénomène de documentarisation [@zacklad_design_2019], mais
le choix d'un format ou d'une saveur particulière d'un format : le
positionnement de l'autorité est alors déplacé vers un niveau plus bas.

L'encodage d'un texte en XML illustre bien ce propos.
XML, pour _eXtensible Markup Language_, est à la fois un format de modélisation
du texte et un métalangage qui définit ses propres règles.
Plus souple que le HTML dont les balises sont figées, XML permet à chaque
utilisateur de créer son propre système hiérarchique arborescent par
l'élaboration de balises personnalisées.
Postérieur d'une décennie au format HTML, la publication des recommandations de
la première version (1.0) du métalangage XML voit le jour en 1998.

La souplesse mentionnée précédemment n'empêche pas une rigueur extrême dans la
structuration des contenus : chaque document formaté en XML doit, pour être
valide, être conforme à un schéma dont la fonction est de définir des règles de
structuration des informations documentées.
Ce fonctionnement rend XML interopérable entre différents systèmes
d'informations et chaque document XML devient transformable en un autre document
XML.

Que l'on soit sous système d'exploitation Linux, MacOS ou Windows, le XML peut
être saisi et lu dans tous les éditeurs de texte.
Chacun est en capacité de créer ses propres régles d'agencement des contenus en
créant un schéma qui correspond aux besoins d'une chaîne éditoriale.

Par exemple, lors de l'édition d'un article scientifique, comment pouvons-nous
définir un auteur ?

Si l'on écrit la chaîne de caractère "Rémi Dupont" à la fin du texte, nous
pouvons, par convention de lecture, deviner que "Rémi" est le prénom de l'auteur
et "Dupont" son nom.
Or, pour l'ordinateur, cette chaîne de caractère n'est rien d'autre qu'une série
de caractères qui n'a aucune valeur sémantique particulière, hormis peut-être
qu'il s'agit d'un paragraphe.

Si l'on saisit cette même chaîne de caractères en XML, on peut ajouter une
balise `<auteur>Rémi Dupont</auteur>` pour signifier explicitement qu'il s'agit
de l'auteur du texte.

Il est également possible de préciser encore plus cette notion d'auteur en y
ajoutant par exemple des balises `<prénom>` et `<nom>` à l'intérieur de la
balise `<auteur>`.
La description de ce qu'est un auteur, pour l'écriture de cet exemple, devient
formelle et explicite.
Cependant, pour l'écriture savante, est-ce qu'un auteur est seulement un nom et
un prénom ?
En fonction des contextes de publication, il est possible qu'un autre agent, la
revue, définisse également la notion d'auteur avec d'autres informations telles
que l'affiliation académique, une adresse courriel et un identifiant unique
comme l'ORCID.
Rémi Dupont prendrait alors la forme suivante :

```xml
<auteur>
    <nom>Dupont</nom>
    <prenom>Rémi</prenom>
    <courriel>remi.dupont@universite.fr</courriel>
    <affiliation>Université X ou Y</affiliation>
    <orcid>XXXXXXXXX</orcid>
</auteur>
```
Le format XML est un exemple très explicite.
La sémantique du texte y est structurée selon deux dimensions, à la fois en
termes de structuration verticale des informations mais aussi dans la saisie des
noms des balises qui, en général, renvoient à des éléments lisibles et
compréhensibles, ce qui n'est pas le cas de tous les formats -- au prix d'un
balisage dit plus verbeux et parfois lourds dans le texte.
D'autres langages de balisage, notamment ceux qualifiés de légers comme le
Markdown, emploient des symboles tels que `=` ou `#` pour structurer les
informations à l'intérieur d'un document.
Contrairement à ce que nous avons vu avec le XML, la signification des éléments
structurants n'est pas forcément explicite pour une lecture humaine, même si
l'on peut la deviner ou l'apprendre.

Le terme format est avant tout un terme technique, il délimite les
caractéristiques d'un objet.
Ces caractéristiques sont formulées par un certain nombres de données,
d'instructions, ou de règles.
L'objectif est de disposer d'un consensus pour dialoguer autour d'un objet ou de
faire communiquer des processus qui traîtent ou qui produisent des formats.

Le format est une contrainte technique dans des environnements qui peuvent être
très divers : formats d'objets physiques comme le papier, formats informatiques
que nous connaissons par l'extension des fichiers sur nos ordinateurs, ou
formats littéraires concernant l'agencement des mots et des phrases.
Nous nous concentrons ici sur les formats informatiques.
En fonction des nécessités d'un système d'exploitation, d'un programme
informatique ou d'une plateforme en ligne, un format caractéristique sera
requis pour agencer et organiser les informations selon les règles qui le
définissent [bachimont_ingenierie_2007].
Un format qui n'est pas standard (ces caractéristiques doivent être décrites),
qui n'est pas ouvert (il est possible de comprendre comment le format
fonctionne) ou qui nécessite un environnement très spécifique pour être
interprété ou transformé va générer beaucoup d'obstacles pour son utilisation.

La contrainte du format est liée à d'autres contraintes comme la compatibilité
(quel format peut être lu par quel programme ou logiciel ?), l'interopérabilité
(est-ce que le format peut être utilisé de la même façon quel que soit
l'environnement ?), la dépendance (de quoi un système a-t-il besoin pour traiter
le format ?) et les droits associés (est-ce que le format peut être lu, modifié
ou partagé ?).

Si le but du format est de constituer une série d'informations compréhensibles,
utilisables et communicables, il reste une contrainte forte pour les chaînes de
publication [@mourat_vacillement_2020].
Que ce soit en tant que format d'entrée, format pivot de transformation ou
format de publication -- nous reviendrons sur les transformations et les
artefacts publiables dans le chapitre 3 --, il déterminera le
fonctionnement de la chaîne.

Comme nous l'avons déjà mentionné, il y a trois formats centraux dans l'éditeur
de texte Stylo : le Markdown pour le corps du texte, le YAML pour les
métadonnées et le BibTeX pour les références bibliographiques.
Chacun de ces formats a sa propre histoire et ses propres spécifications.
Afin de mieux comprendre la structuration des informations dans Stylo, nous
allons passer en revue certaines des particularités de ces formats et de leur
implémentation dans l'éditeur.

Mardown est un langage de balisage léger créé en 2004 par John Gruber^[Voir son
site web, consulté le 31 mars 2024 :
https://daringfireball.net/projects/markdown/].
Sa syntaxe, beaucoup plus légère
et moins verbeuse que le HTML dont il est issu, permet de structurer et de
décrire sémantiquement le texte. Il a été pensé pour pouvoir être converti
facilement vers d’autres formats comme HTML, LaTeX ou PDF. Markdown se distingue
des autres langages de balisages légers, car il est déclinable en différentes
variantes (ou saveurs). Chacune d’entre elles ajoute une particularité dans la
syntaxe Markdown. Parmi les plus populaires, on retrouve :

- CommonMark^[Les spécificités de CommonMark sont disponibles sur le site web
  dédié à cette saveur : https://commonmark.org/, consulté le 31 mars 2024.]
- GitHub Flavored Markdown (GFM)^[Celles de GFM sont disponibles sur cette page
  web : https://github.github.com/gfm/, consultée le 31 mars 2024.]
- MultiMarkdown^[Celles de MultiMarkdown sont disponibles sur cette page web :
  https://rawgit.com/fletcher/MultiMarkdown-6-Syntax-Guide/master/index.html,
cinsultée le 31 mars 2024.]
- Pandoc^[Celles de Pandoc sont disponibles sur cette page web :
  https://pandoc.org/MANUAL.html#pandocs-markdown, consultée le 31 mars 2024.]
- Quarto^[Celles de Quarto sont disponibles sur cette page web :
  https://quarto.org/docs/authoring/markdown-basics.html, consultée le 31 mars
2024.]

Cette capacité à être déclinable et adaptable distingue fortement Markdown des
autres langages de balisage.
En effet, puisque chaque saveur contient des éléments personnalisés de
structuration des contenus -- des balises --, il est important de connaître la
saveur que l'on doit utiliser dans un environnement au risque de se retrouver
avec des balises qui ne sont pas interprétées et qui par extension, n'ont aucune
signification pour cet envrionnement.

Par exemple, la saveur Quarto Markdown utilise la structure ci-dessous pour
insérer une vidéo dans un texte.
Cependant, ce marquage ne sera interprété que lorsque Quarto transformera le
document Markdown en un autre document, or dans Stylo cette ligne sera traitée
comme un paragraphe et ne sera pas transformée parce que Stylo ne connaît pas
cette structure puisque la saveur Quarto de Markdown n'y est pas prise en
charge.

```md
{{< video https://www.youtube.com/embed/wo9vZccmqwc >}}
```

À ce propos, aucune saveur spécifique n'a été implémentée dans Stylo pour
laisser le champ libre aux utilisateurs d'employer celle qui leur convient le
mieux.
Néanmoins, lorsque les sources sont transformées par le module d'export
(l'export des sources n'est pas concerné), les utilisateurs doivent respecter
les préconisations du logiciel Pandoc puisque c'est ce dernier qui
réalise les transformations et conversions des documents.
Les saveurs les plus couramment utilisées avec Pandoc sont CommonMark et
GitHub Flavored Markdown^[Outre celle qui porte son nom, Pandoc prend en
charge d'autres variantes de Markdown comme cela est indiqué dans la
documentation à ce sujet : https://pandoc.org/MANUAL.html#markdown-variants.].

Autrement dit, Stylo n'impose pas de variante de Markdown si l'on s'en sert
comme éditeur de texte sans la nécessité d'utiliser le module d'export.
Dès qu'une chaîne éditoriale s'appuie sur ce module, comme c'est le cas pour la
chaîne Stylo utilisant l'export XML TEI conforme au schéma COMMONS commun à
Métopes et OpenEdition, il devient essentiel d'employer les
variantes que traitent Pandoc pour que les transformations et conversions se
fassent sans erreur.
Pour conclure sur le langage de balisage Markdown, sa possible déclinaison en
diverses saveurs fait de ce langage un avantage et un inconvénient.
C'est un avantage pour sa plasticité et son adaptibilité aux besoins d'une
communauté ou d'un projet.
Cependant, si les adaptations réalisées le sont dans une niche, soit parce que
la communauté qui en définit les règles comporte trop de peu de membres, soit
parce qu'il n'y a qu'un seul environnement qui traite cette saveur, le Markdown
perd sa caractéristique interopérable et contraint les usagers à bricoler des
équivalences entre les transformations pour préserver la structuration des
contenus.

Dans Stylo, la sérialisation des métadonnées est réalisée en YAML qui, dans sa version
originale de 2004 avait pour signification _Yet Another Markup Language_ puis se
transforme à l’occasion de la publication de sa version 1.1 en _YAML Ain’t
Markup Language_.
YAML est un langage de sérialisation de données pour tous les
langages de programmation.
Un usage récurrent qui en est fait consiste à utiliser
YAML pour créer des fichiers de configuration. Dans le cas des outils liés à
l’édition numérique, YAML sera utilisé pour enregistrer les métadonnées
associées à un document.
Le principe de YAML est très facile à assimiler puisqu'il repose sur le même
fonctionnement qu'un dictionnaire avec la structure `clef: valeur`.
Chacun a la possibilité de créer de toute pièce son document YAML et
de choisir les `clefs` et les `valeurs` qui leur sont associées.
C'est ensuite l'application qui va parser le contenu en suivant l'architecture
des informations dans le fichier YAML.
Dans Stylo, les `clefs` ont été prédéterminées lors des développements de
l'interface et les utilisateurs n'ont plus qu'à remplir un formulaire pour
déclarer les `valeurs` qui seront associées aux différentes `clefs` -- un mode
graphique permet d'accéder au contenu en YAML brut sans surcouche.

Si nous reprenons l'exemple de l'auteur mentionné précédemment, un auteur est
déclaré comme suit dans Stylo :

```yaml
authors:
  - affiliations: ''
    biography: ''
    email: ''
    foaf: ''
    forename: ''
    isni: ''
    orcid: ''
    surname: ''
    viaf: ''
    wikidata: ''
``` 

Les métadonnées sélectionnées pour représenter l'auteur dans Stylo reflète
principalement les besoins émis par les revues, par exemple Sens Public ou
Humanités Numériques, ou les plateformes de diffusion telles qu'Érudit et
OpenEdition.
Dans Stylo, un auteur est donc représenté uniquement par ces informations. 
Néanmoins, il arrive que certains utilisateurs ou institutions requièrent
d'autres informations pour décrire plus précisément un auteur et nécessite des
adaptations.
Par exemple, la clef YAML `affiliations` désigne sans distinction l'institution,
le laboratoire ou encore le département de rattachement.
Pourtant, selon les revues, il peut être important de faire formellement cette
différence.
Dans Stylo, la notion d'auteur ne s'incarne qu'à travers ce choix qui a été
implémenté.
L'auteur est donc formellement constitué de 10 entrées au maximum.
Ce qui est valable pour les auteurs l'est également pour les autres types de
données décrites dans les métadonnées du document.
La réduction d'un auteur à quelques mot-clés n'est pas très importante
puisqu'elle couvre les besoins de la plupart des revues -- ce qui est quand même
l'objectif de Stylo --.

Au-delà de Stylo, l'utilisation de YAML est toutefois controversée.
Contrairement à d'autres langages de structuration de données dont le
comportement est pérenne, comme le standard JSON (_JavaScript Object Notation_)
publié pour la première fois en 1999^[Voir le site web de JSON :
https://www.json.org/json-en.html, consulté le 31 mars 2024.], YAML 1.0 subit
des modifications régulières depuis 2004 avec une version 1.1 en 2005 puis une
version 1.2 en 2009 et une dernière mise à jour en 2021 avec la version 1.2.2.
Là où une certaine stabilité que l'on trouve dans des formats tel que JSON
apporte une forme de pérennité pour les applications, malgré une modification
mineure en 2005 avec la suppression de la saisie de commentaires dans les
documents au format JSON, YAML fait le choix d'évoluer et de s'adapter aux
besoins des communautés.
Cependant, comme le mentionne Ruud van Asseldonk sur son blog^[Voir le blog de
Ruud van Asseldonk :
https://ruudvanasseldonk.com/2023/01/11/the-yaml-document-from-hell, consulté le
31 mars 2024.], ces mises à jour peuvent générer des complications lorsque les
fichiers YAML doivent passer d'un environnement à un autre alors que les
versions de YAML utilisées sont différentes.
Par exemple, Pandoc intègre en juillet 2018 la version 1.2 de YAML^[Voir la page
des _releases_ de Pandoc :
https://pandoc.org/releases.html#pandoc-2.2.2-2018-07-16, consultée le 31 mars
2024.] où nous pouvons y lire : 

> Update manual for “true” YAML values. Now that we’re using HsYAML and YAML
> 1.2, the valid true values are true, True, TRUE. NOTE! y, yes, on no longer
> count as true values.

Le changement de version génère une modification de comportement des valeurs `y,
yes, on` qui signifiaient le booléen `true` dans la version 1.1 et ne sont plus
que des chaînes de caractères à partir de la version 1.2.
Or, tous les parseurs de YAML n'ont pas fait cette mise à jour. Par exemple, la
très répandue librairie Python PyYaml, dont la dernière mise à jour remonte à
juillet 2023^[Voir la page web de la librairie :
https://pypi.org/project/PyYAML/, consultée le 31 mars 2024.], s'appuie toujours
sur la version 1.1 de YAML.
En somme, si un document doit passer d'un environnement utilisant la version 1.1
ou la version 1.2, les informations structurées ne seront pas traitées de la
même manière.

Nous sommes en droit de nous demander pourquoi YAML reste aussi populaire ?
Ruud van Asseldonk apporte plusieurs réponses à cette question.
La première est que YAML fait partie des plus anciens langages de sérialisation
de données et répondait alors à un besoin de toute une génération de
développeurs, ensuite il permet l'écriture de commentaires à l'intérieur des
documents, c'est-à-dire du texte qui ne sera pas traité par le parseur, alors
que JSON ne le permet pas.
Des alternatives comme le langage TOML^[Voir le site web du langage TOML :
https://toml.io/en/, consulté le 31 mars 2024.] ont vu le jour dans les années
2010 (2013 pour le TOML) pour tenter de pallier les problèmes sus-mentionnés.
Le langage TOML est par exemple utilisée pour le fichier de configuration du
paquet Python "Pressoir-CLI" afin de déclarer différents paramètres, par exemple
de mise en page, parsés par le Pressoir et utilisés pour générer des livres au
format HTML. Cet outil fera l'objet d'une analyse détaillée dans le prochain
chapitre^[Le pressoir-cli est un paquet python développé par la CRCEN et
disponible à cette page web : https://pypi.org/project/pressoir-cli/, consultée
le 31 mars 2024.]. 

Enfin, le dernier format pivot utilisé dans Stylo, le BibTeX, est utilisé pour
structurer les références bibliographiques.
BiBTeX est un format standard permettant de décrire des listes de références
bibliographiques inventé par Oren Patashnik en 1985 pour l'écosystème LaTeX.
Au-delà de LaTeX, c'est un format largement utilisé par les gestionnaires de
références bibliographiques comme Zotero^[Zotero est un logiciel de gestion de
références bibliographiques très connu, il est l'alternative libre et _open
source_ à Mendeley, voir le site web de Zotero : https://www.zotero.org/,
consulté le 31 mars 2024.] ou eBib^[EBib est un logiciel de gestion de
références bibliographiques fonctionnant depuis l'éditeur de texte Emacs, voir
le site du projet : https://joostkremers.github.io/ebib/, consultée le 31 mars
2024.].

Le choix d'intégrer BibTeX à Stylo provient de la possibilité d'utiliser l'API
de Zotero dans l'éditeur de Stylo pour récupérer les informations relatives aux références
bibliographiques.
Ce fonctionnement entre Zotero et Stylo permet aux utilisateurs de ne passer que
rarement par la forme brute du BibTeX, puis il permet de décentraliser la
gestion et le nettoyage des informations de chaque référence dans Zotero et
limite les phases de nettoyage des informations à ce seul espace.
Stylo est plutôt prévu pour récupérer des listes de références bibliographiques
et procurer des fonctionnalités pour les intégrer dans un texte.
L'utilisation du format BibTeX permet d'automatiser la saisie et la
transformation des références bibliographiques selon les styles requis pour un
document.
Pourtant, ce choix pourrait être tout à fait discutable du fait des limites de
Zotero et de BibTeX.
Lors de la création d'un nouvel objet dans Zotero, le premier élément à saisir
est le type d'objet à référencer. Le nombre de types est limité à 17. Cela
couvre une bonne partie des besoins académiques mais pas les exceptions qui vont
toutes rentrer dans le dernier type `@misc` pour « tout autre type de
document ».
Il en va de même pour les informations rattachées à chaque type de données^[cf.
le tableau des champs accolés aux types de documents en annexe.] : selon les
disciplines ou pour certains documents très particuliers, les champs de
Zotero peuvent être trop restrictifs alors qu'il serait nécessaire de pouvoir
saisir de nouvelles entrées pour enrichir les données bibliographiques tout en
préservant leur structuration. Actuellement, la seule possibilité serait
d'utiliser le champ `Extra` pour ajouter une information supplémentaire sous la
forme de chaîne de caractères sans avoir de structure explicite.

D'autres problèmes peuvent surgir entre la représentation d'une référence
bibliographique dans Zotero et dans Stylo/Pandoc.
Lors de l'édition d'articles en anglais et en français, nous nous sommes aperçus
d'une différence de comportement importante entre ce que prévoit le format
BibTeX, son interprétation dans Zotero et celle que l'on en fait dans Stylo.
Avec BibTeX il existe plusieurs paramètres de langues : `langid` et `language`.
`langid` permet initialement d'identifier la langue à appliquer à l'entrée
(comme traitement) et `language` sert à déclarer la langue employée dans le
document.
Stylo et Pandoc prennent les deux paramètres en charge, alors que dans Zotero il
n'est possible de renseigner que `language` et pas `langid`, `language`
combinant les deux objets.
En récupérant les références bibliographiques depuis Zotero, Stylo récupère
seulement le paramètre `language` puisque le paramètre `langid` n'existe pas
dans Zotero.
Lors du traitement des informations avec Pandoc, il n'est pas possible de
déclarer le traitement à appliquer à la référence bibliographique.
Par défaut, Stylo va appliquer la langue du contenu du texte dans Stylo à toutes
les références bibliographiques. Dans un texte comme celui-ci, le paramètre par
défaut est réglé sur le français.
Les références en anglais seront alors transformées selon les règles
orthotypographiques françaises et pas selon les normes anglaises.
Pour une structure éditoriale telle qu'une revue, ce paramètre n'est pas
opérationnel.
De ceci découle une discussion entre les membres de l'équipe de développement de
Stylo^[Voir la discussion sur GitHub :
https://github.com/EcrituresNumeriques/stylo/pull/991, consultée le 31 mars
2024.] sur la conduite à tenir pour informer les usagers de ce problème et
trouver une solution pour le contourner.
À ce jour, nous avons décidé de renseigner le problème dans la documentation de
Stylo^[Voir la documentation de Stylo :
http://stylo-doc.ecrituresnumeriques.ca/fr/bibliographie/#lettres-capitales-pour-les-titres-en-anglais,
consultée le 31 mars 2024.] pour avertir les utilisateurs.
Une modification du format ou du fonctionnement du gestionnaire de références
bibliographiques serait beaucoup trop lourde en termes d'effets de bord dans
Stylo, c'est pour cela qu'à ce stade nous en sommes restés à cette solution.

Étant strictement définis par des règles, les formats dépassent une simple
manière de saisir une donnée.
À travers ces formats et les modes de lectures que l'on peut y adosser,
les informations saisies se voient dotées de comportements et peuvent modifier
l'interprétation que l'on peut en faire, comme nous l'avons vu avec le YAML.  
Le choix des formats dans lesquels les utilisateurs peuvent saisir leurs textes
et leurs données n'est pas anodin.
Qu'il soit ancien, récent, verbeux ou léger, permissif ou rigide,
le format d'écriture conditionne ce que l'on a le droit d'écrire ou non.
En ce sens la décision de ce qui peut être saisi est déjà prise avant qu'un
texte soit frappé sur le clavier.
Par exemple, dans Stylo, le Markdown ne permet pas à un philologue de saisir
explicitement un appareil critique.
C'est une syntaxe qui n'existe pas alors que c'est le cas pour d'autres
environnements comme LaTeX et le paquet
[`ekdosis`](http://www.ekdosis.org/) développé et maintenu par Robert Alessi.
Dans ce cas-ci, puisque l'appareil critique n'existe pas en Markdown, il ne
peut pas exister dans Stylo sauf si l'utilisateur fait abstraction du format et qu'il
change de paradigme pour celui de la page et de la représentation graphique.
En faisant cela, l'utilisateur fait également abstraction de la machine et de
ce qu'elle peut interpréter du contenu puis écrire dans le texte.
Lorsque nous sommes dans un environnement mis à disposition comme Stylo, le
risque est que celui-ci ne soit pas complètement adapté à des besoins ou à une
intention.
Il risque d'y avoir une friction entre les formats imposés par l'environnement
et les besoins en écriture.

### Co-écriture entre les agents

En régissant les procédés de saisi du texte, un rapport de force semble
s'instaurer entre les instances éditrices des architextes (que ce soit des
collectifs, des institutions ou des entreprises) et les usagers [@souchier].
Dans le cas d'un logiciel de traitement de texte lorsque, par exemple, Microsoft
propose une modification de la police utilisée par défaut dans une version
actualisée du logiciel MSWord, Microsoft change également les manières d'écrire
de tous les individus à travers le monde qui utilisent ce logiciel (et qui ont
installé la mise à jour). 

Si l'on s'arrête à la vision superficielle du texte, comme le propose J. Goody
avec la raison graphique [@goody_raison_1979], on ne voit que les modifications d'affichage des
éléments graphiques, mais nous oublions ceux qui sont invisibles et cachés
derrière la page.

Certes, les interfaces d'écriture sont présentées sous la forme de gabarits que
l'on doit remplir, comme on peut le faire avec des logiciels de création de
diapositives dont chacune est découpée en sections contenant tour à tour des
images, des titres ou du texte.
Dans cet exemple-ci nous avons affaire à une construction visuelle du document :
un emplacement pour le titre de la diapositive, un autre pour le texte, un autre
pour une image ou pour un graphique, etc.
À ce sujet, E. Tufte [-@tufte_cognitive_2003] a publié un article sur
l'utilisation du logiciel PowerPoint et démontre à travers plusieurs cas d'étude
les effets du logiciel sur la forme des présentations et des informations
qu'elles contiennent.
La thèse qu'il y défend est que ce logiciel, en 2003, « [...] perturbe, domine
et banalise systématiquement le contenu. » ^[Traduction personnelle : \[...\]
routinely disrupts, dominates, and trivializes content.] notamment parce qu'il
« facilite activement la réalisation de présentation légère »^[Traduction
personnelle : actively facilitates the making of lightweight presentations.].
À travers son analyse des usages de PowerPoint, E. Tufte nous montre qu'il
ne s'agit pas d'un manque de fonctionnalité pour enrichir des supports de
présentation, que l'auteur qualifie de pauvres, mais que le logiciel lui-même
induit ce type de présentation avec des _templates_ préfabriqués, des
réalisations de graphiques automatisées ou d'autres fonctionnalités similaires
qui appauvrissent les présentations parce que leur fonctionnement est calqué sur
un modèle de présentation marketing qui n'est pas adapté aux sciences.
Il ne s'agit plus seulement de remplir des gabarits préfabriqués mais également
de penser les formes que peuvent prendre l'information, ce que Tufte nomme « The
Cognitive Style of PowerPoint », qui n'est pas sans rappeler la raison
computationnelle de Bruno Bachimont [-@bachimont_intelligence_2000].
 
En changeant de paradigme, de la raison graphique pour celui de la raison
computationnelle, l'assujetissement à ces architextes dépasse cette surcouche
graphique et concerne également toutes les sous-couches (in)visibles de
structuration textuelle du texte, mais aussi tout le processus d'inscription du
document dans la mémoire, ainsi que les protocoles et méthodes qui permettent
d'accéder à ces données.
Comme nous l'avons vu précédemment, ce n'est pas l'image du texte affichée à
l'écran qui est sauvegardée mais bien une suite de caractères binaires dont
l'écriture intermédiaire est une suite de symboles, de chiffres et de lettres. 

Pourtant, on constate un paradoxe entre le nom d'un logiciel comme Pages, un
traitement de texte disponible sous MacOS convoquant la métaphore de la page
comme imaginaire en y enfermant les utilisateurs, et le rôle de guide qu'il doit
remplir dans le traitement des informations.
Dans ce cas-ci, le nom du logiciel ne réfère ni à son fonctionnement ni à son
utilité.
Alors que dans les années 1980, lors de la génèse des traitements de texte, les
lettres `WP` signifiaient WordPerfect^[Cet acronyme correspondait à la commande
pour exécuter le logiciel depuis un terminal, alors qu'aujourd'hui il réfère
plutôt au logiciel WordPress.], et que la plupart des autres concurrents
employaient également le mot _word_ dans le nom de leur logiciel, car c'est bien
le mot et son traitement informatique qui était au centre des développements, la
démarche d'Apple en 2005 nous montre un changement de perspective : on passe du
mot à la page.
L'attention est portée à un autre endroit, sur une page que génère Pages et qui
n'existe pas dans d'autres environnements.
La page créée dans cet espace n'est pas reproductible ailleurs même si le
document qui en résulte est ouvert, à un autre moment, par le biais d'un autre
logiciel.
La page de Pages devient un espace délimité qui n'existe sous cette forme qu'à
cet endroit.
Depuis vingt ans que cet outil est nativement disponible sur les ordinateurs de
chez Apple, la compatibilité avec d'autres formats et/ou logiciels augmente
tardivement, en témoigne les arguments de communication mis en avant sur la page
web du logiciel^[Voir le site web, consulté le 21 mars 2024 :
https://www.apple.com/pages/compatibility/] mais compatible ne veut pas dire
identique.
En plus de n'être accessible que **sous** MacOS, cette page ne l'est également
que **sous** Pages : cette formulation courante laisse entendre que
l'utilisateur devient alors sujet de son environnement d'écriture, nous dit F.
Kittler [-@kittler_mode_2015].

Cette position kittlerienne, que l'on peut qualifier d'essentialiste, pose les
fondations des travaux de K. Hayles [@hayles_my_2005], du posthumanisme, et du
nouveau matérialisme, courants dans lesquels s'inscrivent en outre les travaux
de K. Barad [-@barad_meeting_2007; -@barad_frankenstein_2023] et ceux de M.
Vitali-Rosati [-@vitali-rosati_pour_2021].
Pourtant, leur approche du rapport entre humain et machine est radicalement
différente de celle de F. Kittler.
Alors que F. Kittler identifie la machine et l'utilisateur par une série de
propriétés ou définitions *avant* leur interaction, quasiment de manière
décisive, les posthumanistes choisissent de ne pas déterminer les agents
préalablement à l'environnement mais comme résultats de l'agencement de
plusieurs dynamiques dans un espace donné.
C'est en ce sens que sont mobilisées et développées les notions de _worldview_
ches K. Hayles, où Mère Nature devient une Matrice (_My Mother was a Computer_),
l'_intra-action_ à la place d'interaction puisque les agents ne sont pas
prédéterminés chez K. Barad et enfin l'_éditorialisation_ chez M. Vitali-Rosati qui
propose une ontologie de la médiation (métaontologie) selon laquelle le media
n'existe pas, on y retrouve la provocation de Kittler, et que toutes ces
dynamiques, ces intra-actions, sont des médiations dont la matérialité, dans un
agencement donné, produit du sens [@vitali-rosati_media_2019].

Ainsi, l'assujetissement de l'humain aux logiciels que nous avons mentionné, que
F. Kittler critique vivement dans ses travaux, n'a plus de raison d'être dans
cette perspective non-essentialiste offerte par l'éditorialisation puisque ces
entités sont uniquement déterminées lorsqu'il y a intra-action.
Les relations entre les agents ne peuvent plus être présupposées et leur
détermination est réalisée depuis un référentiel quasiment unique si l'on
considère que les paramètres de cet environnement sont variables et que la
probabilité d'obtention de conditions strictement identiques est quasi nulle. 
Depuis cette perspective où l'on considère les différents agents comme des
productions de leur agencement dans un écosystème, il devient intéressant
d'observer leur relation tout au long de ce processus pour comprendre comment
ils s'affectent les uns les autres.

Néanmoins, un trouble persiste dans cette relation entre ces agents.
Ce dernier se manifeste entre ce que l’usager à l’intention d’écrire et le document que
produit la machine, qui est structuré selon un certains nombres de normes,
formats, etc., implémentés dans un logiciel.
Ce trouble nait de la rencontre entre une représentation du texte structurée
graphiquement et une représentation du texte structurée par du texte, entre une
raison graphique et une raison computationnelle,
comme c’est le cas pour une page web interprétée par un navigateur et son
pendant au format HTML.
En ce sens, nous examinons la possibilité que l’écriture numérique puisse
être affublée d’une caractéristique supplémentaire : la cécité.
Cette caractéristique nous semble présente dans le fait qu’il y ait plusieurs
angles morts entre ces deux conceptions du texte qui ne permettent ni à
l’utilisateur ni à la machine de voir le texte dans sa totalité.
La piste de ce trouble nous mène également à comprendre l'enjeu de cette
relation entre l'usager et son environnement.
En le dévoilant, nous mettrons à jour les indices de la rencontre entre un
auteur et son environnement d'écriture.

Dans Stylo, nous savons que le texte est saisi par l'utilisateur en
Markdown (YAML et BibTeX également), puis est envoyé sur le serveur au moyen
d'une requête GraphQL au format JSON contenue dans une requête HTTP utilisant la
méthode `POST` comme modalité de circulation de l'information.
Entre ces étapes persiste une phase qui n'a pas encore été évoquée : la requête
`POST` envoyée au serveur ne s'effectue pas en continu entre le client et le
serveur, ce n'est pas un flux et l'on n'écrit pas directement dans la base de
données.
Une phase latente se glisse dans l'interface Web entre le moment où
l'utilisateur frappe les touches de son clavier et le moment où la base de
données est mise à jour.
Cette phase est rendue visible par l'affichage du message au-dessus de l'éditeur
de texte.
Lorsque aucune touche du clavier n'est enfoncée pendant un certain laps de temps
(quelques secondes), le message "_Last saved..._" est remplacé par "_saving_" :
la copie de travail vient d'être enregistrée dans la base MongoDB grâce à la
requête GraphQL `updateWorkingCopy()`.
Dans ce laps de temps entre la frappe des mots au clavier et l'envoi de la
requête au serveur, qu'advient-il du texte ?

Comme cela est mentionné précédemment, l'espace d'écriture de Stylo est un
espace web.
Pour y accéder, nous avons besoin d'un logiciel particulier -- un navigateur ou
un fureteur -- capable d'interpréter du HTML, du CSS et d'exécuter du
Javascript.
Lorsque l'on écrit dans Stylo -- et de surcroit dans le composant Monaco --,
le texte saisi doit être manipulable et interprétable par le navigateur pour
pouvoir être envoyé sur le serveur.
C'est le rôle de Monaco de traiter cette couche d'informations.
À l'écran, l'utilisateur voit s'afficher du Markdown tel qu'il le frappe,
pourtant cette information n'est inscrite sur aucun support en dehors du rendu
visuel affiché à l'écran.
Monaco travaille avec des *modèles* et ce sont avec eux que l'utilisateur
interagit.
Chaque modèle est rattaché à une URI (que l'on peut identifier avec
l'identifiant des articles) et c'est de cette manière que Monaco peut manipuler
le DOM (_Document Object Model_) du navigateur pour créer le texte et son rendu
graphique dans un format de texte brut.

Le DOM est une représentation abstraite d'un document HTML exécutée dans le
navigateur.
Tous les éléments structurés à l'intérieur de ce document deviennent des objets,
des noeuds manipulables avec du Javascript.
C'est grâce à ce procédé qu'une page web est rendue dynamique.
Puisque la construction du DOM dépend du navigateur employé, nous pouvons en
déduire que ce document sera différent selon le navigateur ou les différentes
versions d'un même logiciel.
Pour accéder à ce DOM il suffit d'ouvrir les outils de développements du
navigateur et d'inspecter le contenu de la page HTML.

Ci-dessous, une première image pour montrer le texte saisi à l'écran et une
deuxième pour montrer ce qui est inscrit dans le DOM.

![Exemple de texte saisi en Markdown dans Stylo](https://s3.hedgedoc.org/demo/uploads/fbed0e8c-2963-49a4-9ae4-76db68af4108.png "Exemple de texte saisi en Markdown dans Stylo")

![Affichage du DOM pour le texte correspondant](https://s3.hedgedoc.org/demo/uploads/62292c15-8649-4e48-b1fd-d5ae242338b1.png "Affichage du DOM pour le texte correspondant")

L'état du texte inscrit dans le DOM est différent de celui qui apparaît à
l'écran.
Le Markdown se retrouve encapsulé dans des balises attribuées par l'éditeur
Monaco et la syntaxe Markdown se retrouve à l'état de chaîne de caractères : la
balise de titre de niveau 2 (`##`) n'a plus de valeur sémantique.
Le DOM interprète la structure HTML des informations contenues dans Monaco pour
les afficher de façon à ce que l'utilisateur puisse avoir un rendu graphique du
texte qu'il a saisi, comme la colorisation syntaxique des balises.
Néanmoins, pour Stylo, le texte saisi n'a en lui-même aucun sens et il ne doit
pas en avoir puisque c'est cette particularité qui rend l'écriture
automatisable.

Écrire dans un environnement comme Stylo ne consiste pas seulement en une simple
saisie du texte à l'écran.
Lorsque nous avons l'impression d'écrire en Markdown, Stylo écrit un texte bien
différent.
Le texte affiché dans Stylo passe en réalité, d'un point de vue matériel, par au
moins 4 représentations différentes :

- le texte saisi en Markdown (affichage à l'écran)
- la représentation du texte dans le DOM réalisé dans le navigateur par
  l'éditeur Monaco
- la requête GraphQL envoyée au serveur au format JSON par HTTP
- l'état de sauvegarde sur le serveur dans la base de données MongoDB

Saisir du texte dans Stylo nécessite en réalité une multitude d'étapes
invisibles -- on pourrait plutôt les qualifier d'automatisées --
mais que pourtant Stylo rédige et inscrit dans la mémoire numérique.

Chacun de ces états a une signification particulière.
Le premier état est la projection d'une structure de l'information, tandis que
le deuxième en permet l'interprétation et l'affichage par le navigateur, la
troisième est une représentation formatée pour circuler entre un client et un
serveur et enfin, la quatrième, est à l'état de stockage, prête à être appelée
pour réaliser le chemin en sens inverse.

Ces différents états du texte sont plus que de simples représentations. Ce sont
des documents différents et chacun à une signification et un usage qui lui est
propre.
Par exemple, la forme en Markdown brut ne peut pas circuler en l'état avec le
protocole HTTP, il lui manque toute une série d'informations et une
transformation vers un autre format (le JSON) pour employer ce canal de
communication : ce dont s'occupe Stylo.

Parmi ces quatre documents produits pour écrire, un seul l'est par l'utilisateur
tandis que les autres formes sont écrites par Stylo.

Écrire dans un environnement numérique dépasse l'encodage de signes dans un seul
format d'écriture.
Comme nous l'avons vu avec Stylo, ce sont différents protocoles qui sont
mobilisés pour produire une suite de documents intermédiaires et, par ce
cheminement, imprègnent l'écriture d'une matérialité.
Lorsque Stylo promeut une reprise en main du texte par les utilisateurs, il ne
faut pas comprendre un environnement moins complexe en termes d'interactions des
différentes composantes dans cet écosystème, il faut y voir une chaîne de
traitement transparente, libre et ouverte sur les transformations opérées dans
le texte.
Pourtant, plutôt qu'une reprise en main, nous lui préférons la notion de
**déprise** sur le texte, au sens que lui donnait Louise Merzeau
[@sauret_revue_2020]^[Louise Merzeau n'a jamais publié de document sur cette
déprise, néanmoins Nicolas Sauret mentionne ce concept et son sens dans sa
thèse.]. 

> Cette formule est empruntée à Louise Merzeau qui l’employait pour parler des
> […] utilisateurs des grandes plateformes du Web [et de] la perte de contrôle
> de leurs usages, restreints et conditionnés par les algorithmes et par des
> interfaces de plus en plus normalisées.

Dans Stylo, les utilisateurs ne sont pas forcément conscients des formes
d'écriture internes à cet environnement, ni de la circulation des informations
entre les éléments qui le constituent.
Cette part de Stylo cachée derrière l'écran relève de cette déprise. 

Si l'on suit les différentes métamorphoses du texte, on se rend compte que la
forme brute (Markdown, YAML, BibTeX) n'est inscrite nulle part.
On la retrouve soit sous sa forme
interprétée par le navigateur (en réalité il s'agit d'un document HTML), soit
lors de l'export c'est-à-dire lorsque les documents sortent de l'environnement
Stylo.
En dehors de cette situation, il n'existe aucun document dont l'extension serait
`.md` et stipulerait que ledit document respecte les règles et normes de ce
format. 

À la différence des systèmes analogiques et continus, la rupture opérée par
l'écriture numérique réside entre autres dans cette discrétisation du texte en de
multiples documents, où chacun se voit doté d'un paratexte différent pour
circuler à travers les canaux de communication du système d'informations.

Dans Stylo, les textes y sont écrits par l'ensemble des protocoles choisis lors
de l'établissement de cet environnement.
La déprise sur le texte survient lors du choix de l'environnement par
l'utilisateur.
Lorsqu'un utilisateur écrit dans Stylo, il accorde sa confiance dans les
opérations que réalise Stylo sur le texte et dans la matérialité qu'il participe
à lui conférer.

Toutes ces dynamiques éditorialisent et constituent les traces d'une
épistémologie du document primaire avant toute transformation par le reste de la
chaîne éditoriale.
Autrement dit, écrire dans l'environnement Stylo produit quelque chose qui ne
serait pas identique dans un autre environnement, car les dynamiques observées
seraient affectées par d'autres facteurs et produiraient ainsi une autre chose.
Le choix de l'environnement d'écriture constitue en conséquence un choix
politique puisque cet environnement agit et produit une matérialité singulière.

## Conclusion

À la question de la place de l'environnement d'écriture dans le processus de
saisi d'un texte numérique et du modèle épistémologique qui en découle,
nous avons émis l'hypothèse que cet environnement dépasse son statut
utilitariste de support pour celui de dynamique constitutive du sens de ce texte.
En nous appuyant sur le fonctionnement d'un ordinateur et sur les
caractéristiques de l'écriture numérique, tant la partie matérielle que la
partie logicielle, nous avons écarté la page affichée à l'écran pour nous
confronter aux logiciels et aux médiations qu'ils représentent dans la relation
entre humain et machine dans l'acte d'écriture. 

En nous appuyant sur la notion d'éditorialisation, telle qu'elle
s'inscrit dans le nouveau matérialisme et le posthumanisme, nous avons observé
les intra-actions à l'oeuvre dans l'éditeur de texte Stylo.
À partir de ce positionnement théorique dont le prisme non-essentialiste ne
prédétermine pas les agents en amont de l'interaction, nous avons considéré à la
fois l'auteur et la machine comme deux agents de l'énonciation
éditoriale.
 
Pour réaliser cette étude, nous nous sommes appuyés sur une méthode empruntée au
théoricien des médias Friedrich Kittler dont l'analyse repose sur la description
technique du fonctionnement des éléments mobilisés.

L’observation du phénomène de création d’un document texte dans un environnement
d’écriture spécialisé pour l’écriture savante à travers le prisme des strates de
l’écriture numérique, du matériel au logiciel, a mis en évidence
différents angles morts de la relation entre un auteur et son environnement
d'écriture dans lesquels se nichent les traces de leurs interactions.
Qu’ils s’incarnent dans des documents temporaires comme le DOM du navigateur ou dans
des protocoles de transmissions des informations comme HTTP, ces angles morts de
l’écriture numérique, produits par cette relation, nous montrent que certaines
parties de cette écriture ne sont finalement pas directement accessibles à ces
deux agents alors qu’elles participent à la matérialité conférée au document produit.
Une forme de déprise est instaurée dans cette relation et que l’auteur accepte,
bon ou malgré lui, lorsqu’il emploie un environnement d’écriture numérique.
En ce sens, un certain degré de confiance (aveugle) est accordé à l’environnement
d’écriture choisi dans le processus de production du document.

En observant diverses saisies de fragments de texte selon les formats pivots utilisés
dans Stylo, le Markdown, le YAML et le BibTeX, nous nous sommes aperçus qu'ils ne
sont jamais inscrits directement selon les formats mentionnés mais qu'ils passent par
quatre états différents : la saisie à l'écran, la manipulation par le DOM du
navigateur dans l'éditeur Monaco, la requête GraphQL formatée en JSON pour être
transporté par la méthode `POST` du protocole HTTP et le stockage dans la base de
données MongoDB.
Le texte est ainsi transformé en différents états pour qu'il puisse circuler
dans Stylo entre l'espace où il est saisi, que l'on peut retrouver à une adresse
unique (l'URL de l'article), et l'espace où il sera stocké dans le serveur de la
TGIR Huma-num qui héberge l'application.
De nouvelles informations sont alors inscrites dans le texte lors de ces
métamorphoses : la structure du document varie à chaque étape.
Ainsi, les caractères qui constituent le document changent et en modifient
profondément le sens.
Parmi les quatre états mentionnés, seulement le premier est saisi par
l'utilisateur et les autres sont écrits par Stylo.
Néanmoins écrire avec Stylo ne nécessite pas de connaître ces différentes
phases.
Il y aurait donc une relation entre un auteur et Stylo qui prendrait naissance
dans une forme de déprise où l'utilisateur accorde sa confiance dans les
manipulations du texte que l'application réalise.
En se référant à l'éditorialisation, nous pouvons affirmer que chacune de ces
quatre phases contribue à la matérialité du texte saisi et qu'en ce sens il y a
co-écriture entre l'utilisateur et Stylo.

Les marqueurs de cette relation entre un auteur et l'environnement d'écriture Stylo,
les traces d'une épistémologie singulière, apparaissent à chacune des phases du
document et y sont inscrites à l'intérieur.
En suivant le fil de ces traces, il devient possible de suivre l'ensemble des
médiations et des conditions de l'environnement numérique produisant le document
primaire et son texte, source que traitera la chaîne éditoriale jusqu'à sa publication.  

## Bibliographie
