---
title: "Je n'ai pas écrit mon billet"
date: "2023-11-07"
---

Hier soir, je me suis installé derrière mon clavier avec l'envie d'écrire un nouveau billet dans ce carnet très vide.

Sauf que je ne l'ai pas fait.

En ouvrant mon éditeur de texte j'ai décidé de regarder à nouveau la structure du site web, et une chose en entraînant une autre, je n'ai même pas créé le fichier pour y écrire le billet.
Mon constat est le suivant : certaines informations, notamment les métadonnées, ont été rentrées en « dur » dans le _template_ (ça allait plus vite pour regarder le résultat).
Or la plupart des générateurs de site statique proposent un fichier de configuration dans lequel les informations relatives au site généré sont insérées.
De cette manière, le _template_ reste générique et s'adapte à différents contenus.
Par exemple, si le titre du site web est appelé à plusieurs endroits dans les _templates_, il n'y a plus besoin d'aller changer cette information partout, au risque d'en oublier une !
Avec un fichier de configuration il devient possible de ne modifier les informations qu'à cet endroit.

Heureusement pour moi, Pandoc intègre cette fonctionnalité avec le paramètre `metadata-file=NOM-DU-FICHIER` que l'on peut intégrer dans une commande Pandoc aussi simplement que cela.
Ainsi, j'ai ajouté un fichier `metadata.yml` à la racine des sources du site et j'ai modifié les _templates_ pour qu'ils prennent en charge les données du fichier YAML plutôt que mes données en dur.

Un `make html` plus tard je me rends compte d'un autre problème (qui était déjà connu mais je l'ai laissé de côté jusqu'à ce soir) : la commande `make html` ne recompile pas les pages du site quand je modifie les _templates_, ce qui est embêtant.
On peut se retrouver, comme ce fût le cas lors des étapes de construction du générateur, avec une modification dans un éléments `partials`, comme le menu de navigation en haut de toutes les pages, prise en compte uniquement dans les pages recompilées.
Les fichiers HTML des pages qui ne sont pas recompilées n'ont pas changé et, en conséquence, le menu diffère d'une page à l'autre.

J'ai discuté de ce problème avec Louis-Olivier aujourd'hui, il y a également été confronté.
La solution repose sur le fonctionnement de Make.
Les instructions inscrites dans le Makefile (appelons les _recettes_ comme le fait Louis-Olivier) dépendent d'une série de dépendances.
En lisant la recette, Make vérifie l'état des dépendances avant d'exécuter les différentes instructions.

Une dépendance d'une recette peut être une autre recette, que l'on nomme _sous-recette_ pour s'y retrouver, qui elle-même peut avoir des dépendances et des instructions.
C'est ce principe que nous avons appliqué à nos recettes pour générer des pages HTML qui sont recompilées lorsque les _templates_ sont modifiés.

Prenons un exemple dans le Makefile : 

```
docs/index.html: src/index.md templates/index.html $(metadata_site)
	@ echo "Production de l'index."
	@ pandoc \
  	$< \
		$(PANDOCFLAGS) \
		--template templates/index.html \
		--output $@
	@ echo "L'index est construit."
```

La recette est construite comme suit : le premier élément passé à la recette est son nom `docs/index.html` ; ensuite viennent les dépendances après les `: src/index.md templates/index.html $(metadata_site)`.
Jusque-là nous avions seulement `src/index.md` qui pointait vers la source de l'index. Si l'index était modifié, Make se chargeait de recompiler.
Le procédé est le même pour le template en ajoutant simplement la dépendance `templates/index.html`.

Il y a quand même un petit "mais". 

Le `templates/index.html` dépend lui aussi de plusieurs `partials`.

Dans la continuité de la recette créée pour produire l'index.html, il nous faut une sous-recette pour indiquer à Make les modifications faites dans les différents `partials`.
On crée une variable `index-partials` pour lui passer tous les fichiers concernés (comme ça la sous-recette est plus facile à lire), puis on passe juste l'instruction `touch` à la sous-recette. `touch` ne fait que modifier la date de modification du fichier qui sert d'information à Make pour savoir quoi recompiler.

```
# sous-recette pour le template de l'index
index-partials = \
	templates/partials/footer.html \
	templates/partials/head.html \
	templates/partials/header.html \
	templates/partials/nav.html

templates/index.html: $(index-partials)
	@ touch $@
```
