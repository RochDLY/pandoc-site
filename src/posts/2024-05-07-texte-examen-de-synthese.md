---
title: "Texte présenté lors de l'examen doctoral de l'UdeM"
subtitle: "Juin 2023"
date: 2024-05-07
---

Ce document a été publié sur un ancien carnet accessible [ici](https://cailloux.en-cours-de.construction/posts/journal/sujetThese.html).
Le report de ce texte sur ce carnet fait suite à la nécessité que j'éprouve de me replonger à l'intérieur.

## Cadre d'écriture

### Contexte de la recherche  

Cette thèse est réalisée en cotutelle sous la direction de Marta Severo (Université Paris Nanterre, France), Emmanuel Château-Dutier et Marcello Vitali-Rosati (Université de Montréal, Canada).
Elle s'inscrit dans les deux disciplines que sont les sciences de l'information et de la communication et la littérature (avec une option en humanités numériques).

### La matière pour écrire

- Bibliographie : Générée au format BibTeX avec Zotero
- BIOS : Libreboot
- Bureau : Mate avec le gestionnaire de fenêtres Awesome
- Clavier : Qwerty canadien puis Qwerty US avec la surcouche Qwerty-Lafayette
- Éditeur de texte : Neovim (avec LazyVim en surcouche), Codium et Stylo
- Fonte utilisée : Jetbrains Mono et Courier New
- Format du document source : Quarto Markdown, une saveur particulière de Markdown dédiée à l'utilisation du logiciel Quarto ; et Markdown pour l'utilisation avec Pandoc et PagedJS
- Formats de publication :
    - HTML : produit avec Quarto
    - PDF : produit avec Pandoc et PagedJS
- Outil de transformation et conversion : J'utilise Quarto comme une surcouche de Pandoc (génération des commandes Pandoc à partir des paramètres YAML renseignés en en-tête de document)  ; Pandoc pour transformer le Markdown en un fichier temporaire HTML qui sera ensuite transformé en PDF à l'aide de PagedJS.
- Ordinateur : Lenovo Thinkpad T440P
- Pointeur : trackpad ou principalement sans pointeur (seulement des raccourcis clavier)
- Système d'exploitation : Devuan

### Problématique

Comment se manifeste l'intimité du chercheur dans les écritures savantes, et plus précisément dans les publications scientifiques ?

### Hypothèse 

L’hypothèse émise est celle d’une intimité produite par l’écriture. C’est-à-dire que le chercheur·e est le résultat des dynamiques d’écriture et de publication auxquelles il se mêle.
Il faut entendre par dynamiques un agencement complexe d’actions, d’événements, de liens entre des individus, des collectivités, des technologies, une structure composant la sphère sociale, politique et technologique dans laquelle s’insère la figure du chercheur·e.
Ce que nous essaierons de démontrer dans cette thèse est que cet intime, cette incrustation des chercheur·e·s dans les dynamiques mentionnées, est une production contingentée à l’acte d’écriture numérique.

### Résumé

À travers la recherche présentée ci-dessous, je souhaite étudier la façon dont se construit et se manifeste l'intimité du chercheur dans ses écritures numériques savantes.
Étant donné l'amplitude que représentent les écritures savantes comme objet de recherche, tous les types d'écriture qui la composent ne seront pas retenus.
Cette recherche sera concentrée sur les publications scientifiques.
L'intimité mentionnée dans le titre ne relève pas d'une acception commune : il ne s'agit pas de se focaliser sur des individualités particulières, mais sur le chercheur en sciences humaines et en lettres, en tant que **figure sociale** spécialiste qui est rattachée à un organisme ou à une institution publique, au 21^e^ siècle en occident. 
Afin de traiter cette problématique, je souhaite faire cette recherche dans l'axe de la théorie des médias dont le point d'origine se trouve dans les années 1960 avec les textes de Marshall McLuhan et connaît depuis l'apparition de différents courants de pensée.

Ce texte, habillé de son apparat savant, est le prémice d'une thèse de doctorat.  
Ce texte reflète quelques 18 mois d'un parcours académique situé à cheval entre Paris et Montréal.  
Ce sont des échanges animés voire passionnés, des conseils, des lectures, des essais et des doutes qui convergent dans ce tapuscrit.  
Au-delà de ces riches événements passés, ce texte tisse un nouveau lien entre vous, au moment où vous lisez ces lignes, et moi, auteur présupposé.  
En conséquence, les modalités de notre relation évoluent.  
Pour de brefs instants, nous ne sommes plus collègues, directeurs ou doctorant, mais examinateurs et candidat.  
Ce premier énoncé s'impose comme un cadre, un contexte qui dirige et délimite l'écriture avant même que la première lettre de ce texte ne soit inscrite sur mon disque dur.  
Une fois rédigé, corrigé et soumis à votre expertise, ce texte ne conditionnera pas seulement votre lecture et sa réception, mais également un échange à venir à propos de son contenu.  
L'entretien derrière nous, ce texte restera l'empreinte de cette étape primordiale du parcours de doctorat.

Ce texte catalyse l'ensemble de ces événements : il en est le milieu, le medium et la trace.   

Ce texte est notre relation.

## Présentation du sujet

Le postulat initial sur lequel je m'appuie est celui de la figure du chercheur comme constituée d'écritures puisque le parcours de recherche en est jalonné de toutes sortes : des ensembles de textes d'abord sous forme de mémoire et de thèse, des diplômes ou des qualifications, puis des articles et des monographies, des demandes de subvention, des carnets, des conférences, un *curriculum vitae*, des lettres, des compte-rendus, des observations, des découvertes, des analyses, des *posts* sur les réseaux sociaux ou encore des billets de blog, des courriels, *etc*.
Cette figure sociale est un *corps de textes* mû par l'écriture et possède un noyau : l'intime.
Plusieurs formats d'écritures savantes numériques viennent d'être nommés, ils constituent cependant un champ très vaste et plusieurs objets de recherche qui ne pourront pas tous être couverts.
L'ensemble nommé « écritures savantes » représente la totalité des écritures qui peuvent être rattachées à une figure sociale (celle du savant). Parmi toutes les écritures savantes se trouvent les publications scientifiques.
Ces publications sont un sous-ensemble sur lequel nous nous focaliserons pour notre recherche, et nous exclurons les autres.

L'intime, du latin *intimus*, est le superlatif de l'intérieur, noyau qui se trouve aux tréfonds de l'être et participe à sa constitution.
Cette notion apparaît pour la première fois en l'an 397 dans les écrits de Saint-Augustin [-@augustin_confessions_1993] et s'enrichit depuis d'une multitude d'acceptions [@montemont_dans_2009;@simonet-tenant_pour_2020].
Ainsi, l'intime désigne tour à tour des espaces tels que le boudoir ou la chambre, des informations, des relations, des correspondances, des carnets, des données, sans jamais trouver de forme réellement figée.
Finalement, ce concept désigne des rapports et des liens à soi et à l'autre [@jullien_intime_2013] rendus accessibles par le truchement d'objets ou d'espaces.
Sans entrer dans le champ de la psychanalyse, l'intime se rapproche de ce qui est décrit comme l'inconscient bien des siècles plus tard.
Dans le cadre de cette thèse, l'intime sera défini plus largement et considéré comme un ensemble d'expériences qu'un individu juge subjectivement comme inaliénable.
L'intime appartient à l'individu, mais cette appartenance n'est pas à saisir sous le sens de la propriété.
L'intime lui appartient, car l'intime **est** l'individu, l'appartenance est dans ce cas un abus de langage.
Ainsi, il semble incohérent d'associer l'intime à la propriété privée, débat qui fait couler tant d'encre, notamment depuis l'intrusion des questions juridiques en matière de distinction entre ce qui relève de la vie privée ou de la place publique et, plus tard, de la controverse sur les données personnelles (*privacy*) datant du début des années 2000.  

Un paradoxe réside dans cet intime qui subsiste à la fois entre des liens et des supports, ce qui participe à créer une certaine opacité autour de cette notion.
Selon la définition précédente, c'est l'expérience, à travers une médiation, qui est jugée intime.
Ainsi, les indices qui peuvent en résulter seraient des traces intimes.
Ces indices ou traces sont des marqueurs d'une intimité-déjà-passée (qui pourrait être réactivée à travers la médiation, par exemple par la relecture d'un texte) et ce sont eux qui peuvent s'échapper de la sphère de l'intime jusqu'à la sphère publique.
Pourtant, sans ce support sur lequel s'inscrivent les traces, l'intime n'existe pas.  
Ainsi présenté, ce paradoxe fait apparemment coexister (en friction) deux intimités : l'une est subjective et l'autre est indicielle (et matérielle).
Néanmoins, ces deux visions ne sont pas dans une opposition absolue.
La définition précédemment énoncée dépend d'un contexte et donc d'un système d'informations très particulier, car il est défini étanche et inviolable : une subjectivité détermine si un rapport appartient à ce champ d'expériences intimes ou non, donc si la médiation à soi-même ou à l'autre y est incluse ou non.
Dans ce contexte, les deux intimités mentionnées deviennent complémentaires et se suivent temporellement dans le système d'informations clos, c'est-à-dire que l'expérience est conditionnée par la matérialité de la médiation.
Les traces font partie intégrante de l'intime et permettent de réactiver l'expérience lors de chaque réactivation de celles-ci.
Or, si une trace échappe à ce système d'informations, si elle est publiée, elle ne peut plus appartenir à ce champ intime : sa valeur indicielle permet cependant à une extériorité de connaître l'existence d'une intimité-déjà-passée, mais elle tait l'expérience en elle-même puisque, nous l'avons vu, elle *est* l'individu, inviolable.
L'ensemble qu'est l'intime intègre en définitive l'expérience et son support, mais si le support en est détaché, il n'est plus intime, seulement un fragment l'évoquant.
Une fois exposée au dehors du système intime, la trace intime devient une trace de l'intime.

Ce bref découpage d'une situtation *a priori* paradoxale sert principalement à lever l'ambiguité sur ce qui est considéré comme étant un objet intime.
Définir l'intime ne revient pas à le circonscrire dans un lien ou dans un support mais revient à définir un système d'informations particulier.
À l'intérieur de ce dernier sont véhiculées des traces intimes qui, si elles s'en échappent, perdent leur caractère intime au profit d'une valeur indicielle.
D'autant plus que lorsque nous nous appuierons sur la théorie des médias et sur la pensée de McLuhan, l'expérience et le medium ne seraient plus à distinguer : le medium deviendrait l'intime dans son intégralité (l'intime est une médiation s'inscrivant dans un système d'informations unique et déterminé). 

Prenons l'exemple d'une relation basée sur l'écriture et la lecture d'un texte rédigé dans le cadre d'un examen universitaire.
Conformément à ce qui vient d'être énoncé, l'environnement intime est déterminé selon deux paramètres : les protagonistes et un medium.  
Pour l'exemple, les protagonistes sont au nombre de six et le medium est composé d'un texte dans un format numérique, véhiculé par courriel.
Les actions d'écrire et de lire sont les médiations qui tissent le lien entre l'auteur et les lecteurs.
Ce sont elles qui participent à l'expérience intime de cette relation entre les différents protagonistes.
Les événements ainsi posés ne laissent aucun doute quant à l'existence de cette intimité grâce au texte même.
Lorsque l'auteur écrit son texte, il le fait avec une intention dirigée vers son lectorat alors composé de cinq personnes.
De la même façon, lorsque les lecteurs lisent le texte, leur attention se tourne vers les autres lecteurs et vers l'auteur.
Si cette relation se déroulait par téléphone ou voie postale et non par courriel, sa nature en changerait ou s'il n'y avait rien de cela, elle n'existerait peut-être pas.
L'écriture et la lecture d'un texte particulier sont les moments de connexion à l'autre ; de l'auteur vers les lecteurs, des lecteurs entre eux, des lecteurs vers les auteurs.  
Autre point remarquable, les propriétés intrinsèques au medium et à son mode de circulation permettent, dans ce cas-ci, une relation entre les protagonistes différée dans le temps.
Le lien qui existe entre eux repose d'abord sur la structure matérielle du texte, son format numérique, puis sur le protocole d'acheminement des informations par courriel entre les protagonistes et, enfin, la capacité de stockage des courriels sur un serveur (ce qui le rend accessible en dehors d'un temps instantanné).

Si nous modifions les paramètres de notre exemple pour une situation en visioconférence sans autre texte que celui d'un échange oral, les modalités de la relation entre les six individus s'en retrouve complètement modifiée : la temporalité devient instantannée et la relation n'existe que pour un temps encore plus limité que par des échanges courriels, temps qui équivaut à celui de la durée de la visioconférence.
En dehors de ce temps là, les seules traces qui subsisteront seront dans les mémoires des protagonistes.

D'ailleurs, si nous reprenons les échanges par courriels, cette connexion entre les émetteurs et les récepteurs du système d'informations intime ne s'établit pas seulement à la première lecture du texte, une relecture peut permettre de réactiver ce lien, et donc l'expérience vécue.
En revanche, si ce texte est **publié** dans un journal, ou sur un [blog](https://cailloux.en-cours-de.construction/posts/journal/sujetThese.html), il témoignera d'une intimité en cours ou d'une intimité passée, mais n'en dévoilera seulement que des indices plus ou moins flagrants : effet que certains spécialistes nomment extimisation.
Cette publication n'est plus qu'un indice du lien existant entre les six protagomistes de notre exemple et ne permet pas à un lecteur tiers de vivre l'expérience de ce lien : nous ne sommes plus dans le champ intime inaliénable décrit précédemment, mais plutôt dans ce que nous pourrions temporairement nommer un *champ extime*.
À défaut de pouvoir s'insérer dans cette relation indicielle, le lecteur extérieur (un septième protagoniste) crée, par son acte de lecture, une nouvelle relation avec l'auteur dont la nature serait *a priori* extime.

Cette perception de l'intime relève en conséquence d'une médiation particulière et concerne le rapport d'un individu à lui-même et/ou à l'autre.
L'intimité, lorsqu'elle est renvoyée à la figure du chercheur, pourrait être rattachée à l'écriture, ce qui constitue notre postulat initial.
Si le chercheur est constitué par des écritures, celles-ci doivent également avoir un rapport avec le noyau à *l'intérieur de l'intérieur* de cette entité.
Si nous suivions l'héritage cartésien traditionnel, et le célèbre *cogito ergo sum*, l'hypothèse que nous pourrions envisager pour répondre à notre problématique serait celle du sujet penseur, dont l'intimité permettrait de produire l'écriture.
Il y aurait une intimité détachée des écritures, pré-existante, à partir de laquelle seraient agrégées des écritures pour former l'image du chercheur.
La position que je souhaite tenir est tout à fait inverse, non anthropocentrée, et vient plutôt s'inscrire dans la pensée préhumaine, courant posthumain s'insérant dans la théorie des médias [@vitali-rosati_pour_2021] : celle où l'écriture précèderait l'intime.
Dès lors, le chercheur serait le résultat de dynamiques d'écritures et de publications auxquelles il est soumis, et son intimité résulterait de ce processus.
Ces dynamiques (que nous pourrions nommer conjonctures médiatrices [@vitali-rosati_media_2019]) sont un ensemble de médiations rattachées à différentes sphères politiques, techniques et sociales.
Elles définissent le milieu au sein duquel évolue le chercheur.
En somme, l'intimité du chercheur, et par extension le chercheur lui-même, n'existe que parce qu'un milieu particulier la fabrique.
Ainsi, la problématique formulée initialement peut être renversée : il ne s'agit plus de questionner l'expression de l'intimité du chercheur dans les écritures savantes, mais plutôt d'essayer de savoir quels sont les effets du numérique sur l'intimité du chercheur.

Toutefois, il est légitime de se poser la question de l'étude de l'intime : comment faire ?
L'objectif de cette recherche n'est pas de mettre en avant une individualité particulière, ou de se focaliser sur la dimension subjective de l'intime (par définition inaccessible).
Cet aspect de l'intime serait, a priori, impossible à étudier.
Pour autant, nous avons évoqué les traces de l'intime, celles qui persistent dans l'espace public et à partir desquelles nous pourrions mener notre recherche.

Aussi, l'étude de ces médiations intimes sera réalisée depuis les traces intimes et le prisme de la théorie des médias.
La genèse de cette théorie remonte aux années 1960 si nous laissons de côté les essais philosophiques qui traitent partiellement de ce sujet (nous pouvons remonter jusqu'à Platon).
À cette période, Marshal McLuhan, considéré unanimement comme le père des *media studies*, publie la *Galaxie Gutemberg* [-@mcluhan_galaxie_2017] et *Pour Comprendre les médias* [-@mcluhan_pour_1977], deux textes références en la matière.
La célèbre provocation « The medium is the message » se positionne à l'opposé de la pensée dominante de cette époque qui est issue de la cybernétique et de la théorie de l'information développée dans les années 1950 (entre autre par Shannon [-@shannon_mathematical_1948], Wiener, Turing) , celle où le medium n'est rien d'autre qu'un support de l'information, il n'entre pas dans l'équation du sens de cette dernière.
Au-delà d'une simple provocation, la pensée de McLuhan fait école [de Toronto] et continuera à frayer son chemin jusqu'en Europe. 

Dans l'Allemagne des années 1970, Friedrich Kittler [@mersch_theorie_2018;-@kittler_mode_2015;-@kittler_gramophone_2018] traite, à la suite de McLuhan, de la question de l'écriture et du medium qu'est l'ordinateur (sujet qui n'est pas tant abordé par McLuhan).
En France, les sciences de l'information et de la communication arrivent tardivement, il faut attendre 1975 pour que cette (inter)discipline naisse officiellement.
Quelques années plus tard, en 1979, Régis Debray emploie pour la première fois le terme de *médiologie* dans son ouvrage *Le pouvoir intellectuel en France*, cependant il faudra attendre la publication du *Cours de médiologie générale* en 1991 pour poser les fondations théoriques de ce champ d'étude, courant qui se distingue des autres écoles de pensée de la théorie des médias.
Par la suite, d'autres courants voient le jour à partir des années 1990 comme l'intermédialité [@tadier__2021] (école montréalaise dont l'origine se trouve dans les années 1960) ou encore la naissance de concepts qui s'inscrivent dans des courants plus génériques, par exemple l'énonciation éditoriale [@souchier_image_1998], la documentarisation [@zacklad_processus_2004;@zacklad_design_2019] et l'éditorialisation [@merzeau_editorialisation_2013;@vitali-rosati_pour_2021;@vitali-rosati_editorialization_2018] dans le courant francophone ou encore la *remediation* [@bolter_remediation_1998] pour le courant anglophone. 

La théorie des médias fait apparaitre **deux enjeux** autour de notre problématique : celui, tout d'abord, de l'apparition de l'intime au croisement de l'écriture numérique (technique) et du monde social, politique et culturel dans lequel évolue le chercheur, puis, celui de la transmission, donc de la nécessité de faire trace et mémoire. 

À l'endroit de l'écriture numérique, l'enjeu social, politique et culturel touche plus que toutes les autres la dimension de publication de la recherche.
Le modèle actuel de publication scientifique est hérité d'une tradition d'un peu plus de trois siècles : il faut remonter à la fin du 17^e^ et début du 18^e^ siècle pour observer la naissance des premières revues savantes [@vittu_trois_2019].
Lorsque le système postal n'est plus réservé à la noblesse, les savants l'emploient pour entretenir des correspondances entre eux.
Le papier est cher et précieux, les échanges sont relativement courts (quelques pages tout au plus) et ressemblent vaguement à une forme du type *article*.
En 1665, la première revue (Le Journal des Savants) fonctionne sur le principe d'un recueil de lettres qui puisse être rendu accessible à tous (publié) et se dégager ainsi du silo de la correspondance.
Le fonctionnement a depuis bien évolué, les outils techniques se globalisent et les protocoles de publications scientifiques ont bien changé.

La transition à la fin du 20^e^ siècle au numérique ubiquitaire déplace le paradigme de l'imprimerie traditionnelle vers celui de l'écriture numérique.
Cette écriture se voit dotée de nouvelles caractéristiques : elle ne concerne plus seulement l'inscription de signes sur un support, mais toutes les captations qui entrent dans le champ du numérique, puis elle devient computable.
S'opère alors une transformation des espaces et des architectures à laquelle le modèle de publication scientifique n'échappe pas [@vitali-rosati_quest-ce_2020-1].

La chaîne de publication scientifique mobilise différents acteurs : des éditeurs, des relecteurs, des développeurs Web, des outils, *etc*. 
Dès lors, l'écriture (numérique) savante se voit altérée par les modifications, les conversions ou les transformations. Ce fait n'est pas nouveau et ne date pas de l'ère numérique.
Cependant, une différence notable apparaît : les écritures numériques ne sont plus seulement le fait des êtres humains, tout un ensemble de robots, de logiciels, et d'algorithmes lisent, encodent et écrivent des textes qu'aucun humain ne lit.
Les textes écrits par des êtres humains sur un support numérique ne sont que des représentations de ce que cet ensemble numérique écrit, manipule ou transforme [@kittler_mode_2015].
Il s'agit de ce que Souchier désigne comme une « rupture sémiotique » [@souchier_numerique_2019].
L'auteur s'appuit obligatoirement sur des architextes [@souchier_pour_1999] pour amorcer l'action d'écriture, seulement cette action n'est pas celle qui enregistre l'information sur son support.
Le geste d'appuyer sur une touche du clavier est décorrélé de l'action d'inscription sur un support, d'autant plus que ces deux étapes sont réalisées dans des langages différents. 
Le langage naturel qui s'affiche à l'écran n'est ainsi qu'une représentation de sa nature numérique enregistrée sur un disque dur.
Sans la médiation opérée par les logiciels, le texte encodé sur le disque dur n'est plus accessible à la lecture.  
La lettrure (le regroupement des actions de lire et écrire en environnement numérique réalisé par Souchier) [@souchier_numerique_2019] devient complètement dépendante de son architexte pour exister.

Dans le cadre d'une chaîne éditoriale savante, la mobilisation de l'architexte devient plus complexe et peut perturber la nature même du texte.
Un texte est initialement rédigé dans un document sur un ordinateur, que ce soit dans une situation locale, ou sur un service Web dédié à l'écriture.
Une fois écrit, ce texte transite ensuite par plusieurs terminaux, sous différents systèmes d'exploitation et autres technologies dédiées à la lecture et à l'écriture, pour être annoté et corrigé par plusieurs mains avant d'être validé pour publication ; ainsi les acteurs de cette chaîne éditoriale (humains et numériques) participent à l'élaboration de cette écriture savante.
Étant donné que chaque logiciel et chaque version des logiciels fonctionnent différemment les uns des autres, chacun réécrit partiellement le texte (notamment dans le cas des logiciels de traitement de texte) et provoque ainsi un ensemble de modifications afin de nous rendre sa représentation en langage naturel accessible dans une interface.  
Il ne s'agit plus d'un système où la seule existence du chercheur repose sur la reconnaissance par les pairs, mais repose également sur toute une infrastructure sociale et technique qui participe littéralement à l'écriture du texte.
Nous pourrions à cet endroit émettre une nouvelle hypothèse d'une construction collective de l'intimité du chercheur (composée par les agents humains et les agents numériques qui participent à l'écriture).

Reprenons l'exemple précédent du texte comme medium de l'expérience intime entre les six protagonistes dans le cadre d'un examen universitaire, mais ce coup-ci lors de sa phase d'écriture, avant qu'il ne soit envoyé par courriel.
Nous pouvons d'ores et déjà observer que le texte au centre de la relation n'est pas sorti du néant ou de la seule volonté de son auteur présupposé. 
De la même façon que le contexte d'écriture, et donc ses normes et conventions, façonnent la relation ; les étapes de construction qui mènent à son existence en tant que medium de cette relation participent à l'écriture de sa forme finale.
Que ce soit délibéré ou par des conventions d'habitude, le choix de l'architexte, parce qu'il écrit tout autant voire plus que l'auteur et que les lecteurs, ne peut pas être un paramètre écarté de l'observation de la construction de l'intime.
Ce principe où toutes les interventions éditoriales dans un texte sont mises en lumière et participent à créer une forme d'auctorialité, Souchier et Jeanneret le nomme « énonciation éditoriale » [@souchier_image_1998;@jeanneret_lenonciation_2005].
Cette relation entre les protagonistes n'existe que parce que le texte en est le medium, mais aussi parce que les logiciels sont les supports des médiations qui ont lieu dans le système d'informations intimes.
Toutefois, s'appuyer uniquement sur le logiciel comme mode d'interaction avec le numérique serait une vision erronée car elle est trop superficielle.
Le numérique n'est pas un espace clos sur lui-même.
Dans ses récents travaux, Emmanuël Souchier [-@souchier_numerique_2019] propose des cadres sémiotiques fonctionnant sur le principe des couches informatiques (du *hardware* jusqu'au *software*). 
Ces cadres matériel, système, réseaux, logiciel, approfondissent déjà grandement la construction des échanges.
La complexité est telle que déjà la notion d'auteur commence à s'estomper. 
Pourtant, ces cadres sont encore trop restrictifs : nous l'avons vu, un format d'écriture (par exemple un article de revue ou une monographie), des conventions ou normes (disciplinaires, typographiques), des restrictions et des contraintes, *etc.*, participent tout autant à l'écriture et à la construction de la relation intime.
L'énonciation éditoriale s'étends au-delà des cadres techniques et éditoriaux.

Finalement, il ne s'agit plus seulement de réaliser des modifications dans le texte savant mais de modifier la structure du medium au fil de l'évolution du lien entre les protagonistes.
Tous les paramètres variables qui viennent d'être énoncés n'opèrent pas seulement des modifications qui relèvent de l'ordre du textuel, situées sur la couche supérieure du medium, c'est-à-dire le texte, mais opère plus en profondeur sur la structure du medium lui-même. 
Chaque choix, chaque action, qu'elle soit humaine ou machine, perturbe l'état initial du medium en y laissant des empreintes et des inscriptions pour en modifier les propriétés.

Un texte savant n'est plus seulement une page blanche sortie d'un logiciel de traitement de texte mais devient le porteur de toutes les médiations qui l'ont amenées jusqu'à la dernière étape de la chaîne de publication. 
De cette manière, le medium dépasse son statut de support de la relation pour devenir la relation même.

Alors, qu'advient-il de cette intimité une fois qu'elle est publiée ?
Jusqu'à présent, l'intérêt porté à la problématique était concentré sur l'écriture et le processus de publication, et soulève la possibilité que l'intimité produite par les écritures savantes ne soit pas individuelle, mais collective.
Une fois relâchée dans l'espace public, l'écriture se détache de l'intimité qu'elle a initiée et devient un ensemble de traces dont la fonction indicielle dévoile un fragment de cette dernière et participe à créer la représentation abstraite d'un chercheur dans l'écosystème savant.
Vitali-Rosati [-@vitali-rosati_pour_2021] défend la thèse que les écritures numériques façonnent les architectures de nos espaces, n'en serait-il pas de même pour les chercheurs ?
Est-ce que ces écritures numériques, ces traces intimes publiées, ne participeraient-elles pas à façonner les tréfonds de cette figure sociale qu'est le chercheur ?  
Cette question nous écarte de l'intimité vécue à la première personne (donc de l'expérience) que nous avons vu jusqu'à maintenant et nous renvoie à l'étymologie du superlatif de l'intérieur.
Il ne s'agit plus d'essayer de contenir une expérience et sa médiation, mais de représenter, depuis l'espace public, l'intérieur de l'intérieur de notre figure sociale à partir des traces qui subsistent d'elle.
Nous ne sommes plus dans un système d'informations fermé, mais dans un système ouvert et accessible.
Il pourrait même être qualifié de « public ».
Il ne s'agit plus de l'intime, mais d'une image de l'intimité renvoyée par les traces intimes que l'on peut (pour l'instant) nommer représentation.
Pour le reformuler, il s'agit de représenter la figure du chercheur depuis ses écritures laissées dans l'espace public.
L'enjeu est une recollection des traces, de la mémoire, par des agents externes, afin de reconstituer à travers les indices laissés une représentation de cette figure sociale. 
De la même manière que les chercheurs qui, dès l'origine, sont institués par les pairs, la représentation collective qui en persiste dans la sphère sociale est celle constituée par une communauté.
L'hypothèse émise ici est que la réactivation des traces intimes d'une œuvre -- citation dans d'autres écrits, dans les références bibliographiques ou dans les textes, réédition ou recherches menées sur ses écrits -- par des extériorités permet de faire exister le chercheur dans son monde social.

L'intimité du chercheur ferait ainsi l'objet d'un double mouvement. Nous retrouvons d'abord l'intimité telle qu'une expérience médiée au sein d'un système d'informations inviolable et vécue à la première personne, puis vient une intimité mémorielle dont l'ensemble des indices qui sont collectés par les autres, extérieurs au système d'informations précédent, forment une représentation de l'intime, et par extension du chercheur, dans la sphère sociale de la recherche.
L'hypothèse précédente pourrait être complétée par le fait que, dans sa relation au lectorat, le mode d'existence du chercheur (et la représentation de son intimité) continue à fluctuer dans le temps sous sa forme mémorielle.  

Par ailleurs, un des grands enjeux de la recherche est de faire trace. Au-delà des enjeux de publication, les écrits scientifiques servent de socle pour les générations à venir, nous amenant ainsi à considérer la question de la transmission, que nous pourrions formuler en deux sous-questions : 

- Comment fluctue cette représentation de l'intime (les rééditions, modifications de l'architexte, *etc.*) ?
- Quelle est le rôle de cette représentation de l'intime dans la transmission des savoirs ?

L'articulation théorique autour de la théorie des médias permettra dans un premier temps de définir l'intimité du chercheur et en quoi elle diffère des acceptions les plus communes. Ce premier aspect de la recherche sous-entend le dépassement de la fonction "support" que peut tenir l'écosystème numérique (*hardware*, plus *software*, plus espace public) pour devenir une dynamique participante de la fabrication de l'intime.
Ensuite, un second temps sera dédié à disséquer cette intimité nouvelle pour en découvrir les différentes composantes et leur participation à cette construction. Lors de cette étape, l'objectif sera de retracer les actions de l'ensemble des acteurs agissant sur le processus d'écriture des publications scientifique afin de déterminer leurs possibles contributions sur la publication (et sur l'intimité qui en résulte). Enfin, une dernière partie sera consacrée à la recollection des traces afin d'observer de quelle manière circulent les traces et s'il est possible de faire émerger une représentation de(s) l'intimité(s) concerné(s).

## Quelques réflexions méthodologique

Comme cela est mentionné précédemment, l'intime n'est pas un objet de recherche que l'on peut observer directement.
Sa dimension sensible, en tant qu'expérience subjective vécue à la première personne, échappe de par sa nature à tout regard extérieur.
De plus, l'intérêt de cette thèse n'est pas l'obervation d'une individualité particulière, mais bien l'intime en tant que ce qui constitue le chercheur en son for intérieur. 
Selon ce point de vue, l'hypothèse de l'intime comme émergeant des pratiques d'écriture ouvre la perspective d'étudier les conditions de la production de cet intime.
L'analyse du processus de construction de l'intime à travers l'observation des différentes conditions qui le produisent permettrait donc d'en comprendre la structuration et potentiellement d'en dégager une représentation.
Dans le cadre sur lequel nous nous focalisons, celui des publications scientifiques, les pratiques d'écritures qui les constituent suivent des protocoles précis que nous pouvons qualifier comme un ensemble générique nommé chaîne éditoriale savante.
Au-delà de la dimension éditoriale, la particularité de cette chaîne, par rapport à une chaîne plus traditionnelle, est qu'elle repose sur une étape supplémentaire : la relecture et la validation par des pairs.
À ce propos, John Maxwell aborde cette particularité sous l'angle de la bienveillance dans son article « The Care-ful Reviewer : Peer Review as if People Mattered » [@maxwell_care-ful_2022]. 
La thèse soutenue par Maxwell positionne le relecteur comme le garant de la relation entre un auteur et son lectorat.

Le relecteur n'agit plus seulement pour effectuer une relecture scientifique mais porte dès lors la responsabilité de la fonction de médiation du texte savant.
Cette perspective du *care* semble être un prisme intéressant à utiliser pour observer notre objet de recherche.
Toutefois, la thèse de Maxwell mérite un complément.
En effet, en nous appuyant sur le concept d'énonciation éditoriale, nous pouvons émettre l'hypothèse que la responsabilité de cette médiation relève non seulement du relecteur, mais aussi de l'ensemble des autres acteurs agissant sur le texte, c'est-à-dire de chaque maillon de la chaîne éditoriale savante.
Dans cette optique du *care*, nous pouvons par exemple mesurer les effets d'un acteur tel que le logiciel de (mal)traitement du texte, dont la contribution au texte doit être supprimée au risque de générer un texte insensé, comme c'est le cas dans les chaînes de publication des revues diffusées sur la plateforme OpenJournal.
Les assistants d'édition des revues concernées doivent restructurer la plupart des textes en supprimant les styles malins insérés dans le texte par le logiciel de traitement de texte afin de pouvoir les intégrer dans le logiciel Lodel, et les publier sur les sites Web des revues.

Aussi, nous serons attentif à bien référencer tous les acteurs mobilisés lors des différents terrains et à observer leurs impacts sur le texte. 
Dans le cadre particulier d'un rapport de recherche sur les chaînes de publication liées aux collections d'oeuvres d'art (en cours de publication) commandité par le groupe de recherche CIÉCO, nous avons, avec Antoine Fauchié, établi une grille d'analyse et d'observation des logiciels mobilisables dans ce contexte. 
Cette grille pourrait servir de base pour en établir une qui soit adaptée à notre problématique.

Le choix des logiciels mobilisés dans une chaîne éditoriale savante ne doit pas être la seule considération à prendre en compte.
D'autres variables nécessitent d'être prises en charge dans cette équation de production de l'intime. 
Voici une liste non exhaustive de ces paramètres : 

- les ordinateurs des individus concernés  ;
- les périphériques externes (souris, clavier, imprimante)
- les systèmes d'exploitation et leur version  ;
- les logiciels employés et leur version  ;
- les protocoles de partage des documents (courriel, git, voie postale)  ;
- les formats d'écritures (monographie, article de revue)  ;
- les conventions d'écriture (selon la discipline, selon le format de diffusion, normes bibliographiques, *etc.*)  ;
- le format de publication  ;
- les plateformes de diffusion  ;
- les conventions typographiques.

Cette première partie concerne seulement le processus de construction de l'intimité.
Aussi, il nous faut maintenant faire le travail inverse pour reconstituer une intimité à partir des indices disséminés dans des publications savantes.
De prime abord, cette reconstitution se décline en deux étapes.
Dans un premier temps, il s'agit d'effectuer une collection des publications scientifiques et des traces qu'elles contiennent, et de les organiser.
Dans un second temps, il faudra opérer autant que possible une rétro-ingénierie de la chaîne éditoriale savante menant à l'obtention de ces traces afin d'obtenir une représentation de l'intime la plus juste possible. 

Comme nous l'avons vu précédemment, le medium transporte en lui non seulement les textes inscrits à sa surface par les différents acteurs, mais aussi les traces des autres médiations qu'il aura traversé. 
Par exemple, si je souhaite me procurer un livre, est-ce que je consulte sa version web ? est-ce que je télécharge une version au format PDF ? est-ce que je l'achète sur amazon ou dans une librairie ?
La façon dont je me procure un texte savant détermine un contexte et un support de lecture, ainsi qu'un ensemble d'informations connexes, modifiant ainsi l'expérience de lecture.
Ces informations sont des données considérées comme contextuelles.
Pour les objets numériques ce sont généralement des informations que nous trouverons dans les métadonnées rattachées aux documents.

De fait, l'enjeu de cette deuxième partie consisterait à réunir les textes d'un·e chercheur·e et les informations contextuelles qui y sont rattachées afin de relire ses écrits au prisme de cette construction de l'intimité du chercheur·e (qui sera établie dans la première partie).
Cette collecte peut être réalisée notamment auprès de plusieurs entités telles que les plateformes de diffusions, les revues savantes, les pairs ou les maisons d'édition et comporte une multitude de formes différentes, d'objets, de formats, *etc*.

Ce procédé aura deux objectifs. 
Tout d'abord, le premier objectif sera de reconnaître les types de traces indicielles relative à une intimité : quels sont leurs formats et qu'est-ce qu'elles disent.
À partir de ces informations, nous pourrons comparer les deux approches de l'intime : sa construction et l'interprétation des indices.
Cette comparaison permettra de mettre en évidence le différentiel entre l'intime tel qu'il se forme et sa représentation dans l'espace public : qu'est-ce qui subsiste de cette intimité ? quels éléments disparaissent ?
Ensuite, le deuxième objectif de cette approche servira de socle pour traiter les dernières thématique de cette thèse : la mémoire et la transmission.

La temporalité de la recherche ne permettra peut-être pas d'approfondir l'ensemble de ces paramètres des publications savantes.
L'objectif principal des prochains mois sera de renforcer cette méthodologie qui, à ce jour, n'est pas assez mature.

## Références
