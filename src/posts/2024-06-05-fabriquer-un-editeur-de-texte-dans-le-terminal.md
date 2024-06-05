---
title: "Fabriquer un éditeur de texte dans le terminal"
date: "2024-06-05"
---

Ce billet, je l'écris avec Nano.
Depuis maintenant un peu plus d'une année, j'écris la quasi totalité de mes billets,
bouts de code (et presque mes courriels) depuis mon terminal.
C'est assez confortable de ne pas avoir à constamment changer d'environnement pour
travailler.

J'ai pu passer par Vi, Vim, un peu Emacs, Neovim, maintenant Nano et je ne suis pas
vraiment satisfait.
La plupart des fonctionnalités implémentées sont développées pour écrire du code ou
manipuler des fichiers de configuration.
Finalement, ces espaces d'écriture ne sont pas complètement adaptés pour écrire des textes
avec une orientation académique.
Aussi il y a trop de fonctionnalités qui ne sont pas utilisées dans ce cadre.
À quoi bon les charger / les avoir constamment si je ne m'en sers jamais ?

Le constat fait dans cet espace est le même que celui fait pour Stylo par la CRCEN
il y a quelques années : le modèle du document numérique de ces éditeurs de texte est-il
vraiment adaptés aux visions de ce que nous voudrions que soit un document savant ?

À mon sens Stylo devient un espace où trop de fonctionnalités sont entremêlées.
La philosophie Unix (Mike Gancarz) selon laquelle il est souhaitable de faire des
programmes qui ne font qu'une seule chose mais qui le font bien m'attire beaucoup plus.

Ayant envie d'explorer un peu plus certaines librairies Python (comme curses qui permet
de faire des applications python TUI) j'ai bien envie de me lancer dans le projet de
créer un éditeur de texte TUI adapté à certains besoins spécifiques d'écriture (la liste sera
dressée plus tard, et peut-être pas dans ce carnet).

Un projet a été initié sur [gitlab](https://gitlab.huma-num.fr/rdelannay/simple_text_editor).

Les sources d'inspiration pour amorcer la discussion sur les besoins à implémenter et
sur comment créer un éditeur TUI:

- [Tout le code de Wasim Lorgat](https://github.com/seeM/editor)
- [Le code source de nano](https://git.savannah.gnu.org/cgit/nano.git/tree/src)
- [Le code source de l'éditeur babi](https://github.com/asottile/babi/tree/main)
