---
title: "Installer FuguIta en liveUSB"
date: 2024-05-06
---

Ce billet est destiné à mes premières expériences avec
[OpenBSD](https://www.openbsd.org/).
On en discute depuis un moment avec R. Alessi et j'ai vraiment
envie de le tester .

C'est une autre vision du système d'exploitation que nous avons l'habitude de
rencontrer avec Microsoft, Apple et Linux (je ne détaillerai pas ce sujet dans
ce billet).

Mais ma configuration actuelle me convient, et j'ai mes habitudes
d'environnement de travail que je ne veux pas chambouler du jour au lendemain.
J'ai commencé l'écriture de la thèse depuis quelques mois et ce n'est
franchement pas le moment de changer d'environnement. 

Actuellement mon T440P tourne sous Devuan avec deux disques montés en RAID1.
Peut-être que si j'ai un peu de temps cet été je pourrais supprimer le RAID et
installer un OpenBSD à côté du Devuan pour ne pas perdre mes données et tester
les deux environnements en parallèle.

## Installation de FuguIta

En attendant de faire ça, R. Alessi m'a parlé de [FuguIta](https://fuguita.org/) une
_livesystem_ OpenBSD que l'on peut installer sur une clé USB notamment pour en
faire une LiveUSB !
Aujourd'hui je me suis donc amusé à configurer une clé USB pour tester un
environnement OpenBSD (ultra portable pour le coup, il rentre dans la poche).

Et là, ce n'est pas si simple, je m'y suis repris à plusieurs reprises pour
avoir la configuration que je voulais (en gros bourrin, lorsque je ratais une
étape, j'ai opté pour un formatage de la partition et une réinstallation
totale).

On peut suivre les étapes de l'installation (qui est très bien documentée) sur
le site de [FuguIta](https://fuguita.org/?FuguIta/StartGuide).

Il n'y a qu'à un seul endroit où j'ai personnalisé l'installation, c'est pour la
[personnalisation du bureau](https://fuguita.org/?FuguIta/StartGuide#y699e366).
Lors de l'installation, on doit utiliser la commande `dtjsetup` pour paramétrer l'environnement du bureau.

Au lieu de frapper cette commande on peut utiliser `DTJ_WMS='awesome'
dtjsetup` pour ajouter à la liste de la commande le gestionnaire de fenêtre
[Awesome](https://awesomewm.org/) que j'ai l'habitude d'utiliser avec Devuan.

Ensuite, pour m'encombrer au minimum, j'ai choisi l'option `1` pour le desktop
(`no desktop(wm only)`).

Une fois arrivé au bout de la page d'instructions tout est ok ! FuguIta est bien
paramétré et les sauvegardes se font bien sur la clef USB, quand je shutdown la
machine tout se déroule correctement.

Bon on était juste en mode console et il n'y avait aucune icône nulle part ni
aucun paquet installé.

Au redémarrage de la machine je suis d'ailleurs perdu et je ne sais pas comment
démarrer X11 pour sortir du mode console, la solution :

```sh
rcctl enable xenodm
rcctl start xenodm
```

C'est parti ! Le fameux FUGU apparaît à l'écran !

Entre temps petite crise intérieure, awesome ne fonctionnait pas (puisque
j'avais oublié de déplacer le fichier `rc.lua` dans `.config/awesome` ...)

## Installation des logiciels

Tout fonctionne bien, on arrive directement dans ksh émulé par ... XTERM.

Là je me suis dit que c'était pas possible, je passe mes journées à écrire /
lire dans un terminal et il me faut autre chose comme environnement.

En plus j'en profite, c'est le moment de commencer à configurer et installer mes
softwares préférés ! 

Alors pour le petit tip : `apt` c'est pour linux, pour OpenBSD il faut utiliser
`pkg_add` ! La liste des paquets disponibles est [ici](https://openports.pl/) ou
[là](https://openbsd.app/).

Alors que j'avais décidé de ne rester que dans le terminal sur cette clé usb, je
me lance quand même dans l'installation d'un truc "sûr", pour ne pas louper les
premières installations (sans customisation) :

- Thunderbird (c'est ok ça fonctionne)
- Firefox (ça ne marche pas bien, aucun caractère ne s'affiche)
- Chromium (impeccable)

Là je décide d'éteindre la machine complètement et de la rallumer pour voir ce
que ça donne ... eh bien ce fut un enfer !

La commande `shutdown -h -p now` a pris plus de 20 minutes (j'ai programmé une
sauvegarde avec `usbfadm` pour que tout se synchronise à chaque arrêt (ça lance
une synchronisation avec la commande `usbfadm -r`). 

À bout de patience j'appuie sur le bouton pour arrêter l'ordinateur de force.
C'était une grosse erreur ! 
Lorsque j'ai rallumé la machine et booté sur la clef j'ai eu droit à l'erreur
`warning /mnt was not properly unmounted`. Et bien sûr là, il n'y a plus rien qui
fonctionne correctement.

Je fouille les forums à la recherche d'une solution, a priori c'est un problème
souvent rencontré sur les machines virtuelles mais pas trop grave et impossible
à résoudre.

Caillou pas content.

Comme OpenBSD est bien fichu, il ouvre une petit `xconsole` au démarrage qui
montre toutes les activités en cours.
Là-dedans je vois un message en boucle (forcément puisque le disque qui
contenait les données n'était pas monté) indiquant d'utiliser `fsck` pour
résoudre le problème.

En ligne beaucoup de personnes déconseillent d'utiliser cette commande car mal
utilisée elle peut planter le disque contenant les données.
D'ailleurs il faut absolument l'utiliser sur un disque **non monté**.

Il y a très peu d'exemples d'utilisation alors je me réfère au `man`uel  pour
essayer de comprendre comment on s'en sert.

Une fois à peu près sûr je lance la commande `fsck -p /dev/sd..`. Soulagement
total, le disque est réparé et bien monté.

Je continue mon installation :

- L'éditeur Vim (j'ai récupéré mon `.vimrc` sur le Devuan)
- Le gestionnaire de fichier Midnight commander (et son éditeur super cool)
- J'ai eu envie de changer Xterm, j'ai installé [st](https://st.suckless.org/)
    - pour ouvrir une fenêtre de terminal dans awesome, il faut utiliser le
      combo de touches `Super+Enter`. Du coup `pkg_add st` ne suffit pas.
    - il faut également modifier le fichier `.config/awesome/rc.lua` et
      remplacer `terminal=xterm` par `terminal=st`.
  aka _Simple Terminal_ de Suckless (j'aime bien l'idée !)
- VLC

Voilà où j'en suis pour l'instant ! 

Les prochaines étapes seront :

- Gestionnaire de courriels (Mutt)
- Git (et tous mes repo)
- LazyGit (TUI vraiment cool)
- J'ai l'habitude d'utiliser ohmyzsh parce que ces fonctionnalités sont cools,
  je vais voir si je trouve autre chose pour ksh mais pas sûr, j'aime bien le
terminal brut aussi.
- L'affichage des contours des fenêtres est vraiment moche, il faudrait une
  esthétique un peu plus léchée
- le clavier est configuré en qwerty US, j'aime bien la variante
  qwerty-lafayette pour avoir les accents !
- ipconfig et autres utilitaires pour gérer les connexions internet (là je suis
  juste avec un RJ45)
- un lecteur de PDF
- LibreOffice mais je suis pas sûr, je pense que cette clef ne servira qu'à un
  usage dans le terminal.
- Le navigateur Lynx

Je suis plutôt content de cette installation ! Avec ça je devrais me
familiariser avec OpenBSD avant d'entamer une conversion totale :-)

(Et puis ça me fait un environnement de travail minimaliste pour écrire du texte
au kilomètre.)
