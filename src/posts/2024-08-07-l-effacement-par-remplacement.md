---
title: "L'effacement par remplacement"
date: 2024-08-07
---

Notes pour le billet: 

- Le modèle épistémologique établi pendant l'écriture est effacé et remplacé
  durant le traitement éditorial du document au profit d'un modèle éditorial
choisi.
- les traces obtenues de la rencontre entre un auteur et un environnement sont
  alors supprimées.
- revenir sur le fonctionnement de l'écriture numérique et sa variabilité (c'est
  un fonctionnement intrinsèque au numérique).
    - quelques mots sur le fonctionnement même d'un disque dur et des droits
      d'écriture / lecture d'un espace numérique.
- exemple du pressoir et du livre Contribution numérique: cultures et savoirs.
    - les sources reçues en .odt et .docx
    - transformations via pandoc en markdown + yaml (voir les archives dans
      gitlab)
    - la déstructuration du contenu par Pandoc et son AST (explication de ce
      qu'est un AST)
    - restructuration en un document pandoc native (représentation de l'AST)
    - transformations vers le format souhaité et respect d'un autre modèle de
      représentation du document
- définir transformation et conversion


Note : travailler la question des transformations depuis la déprise, voir
ci-dessous.

---

Lorsque Stylo promeut une reprise en main du texte par les utilisateurs, il ne
faut pas comprendre un environnement moins complexe en termes d’interactions des
différentes composantes dans cet écosystème, il faut y voir une chaîne de
traitement transparente, libre et ouverte sur les transformations opérées dans
le texte.
Pourtant, plutôt qu’une reprise en main, nous lui préférons la notion de déprise
sur le texte, au sens que lui donnait Louise Merzeau [@sauret_revue_2020]^[Louise
Merzeau n’a jamais publié de document sur cette déprise, néanmoins Nicolas Sauret
mentionne ce concept et son sens dans sa thèse.].

> Cette formule est empruntée à Louise Merzeau qui l’employait pour parler des
> […] utilisateurs des grandes plateformes du Web [et de] la perte de contrôle
> de leurs usages, restreints et conditionnés par les algorithmes et par des
> interfaces de plus en plus normalisées.

Dans Stylo, les utilisateurs ne sont pas forcément conscients des formes documentaires
internes à cet environnement, ni de la circulation des informations entre les éléments
qui les constituent.
Cette part de Stylo cachée derrière l’écran relève de cette déprise.

Si l’on suit les différentes métamorphoses du texte par le biais des documents,
on se rend compte que la forme brute (Markdown, YAML, BibTeX) n’est inscrite nulle part.
On la retrouve soit sous sa forme interprétée par le navigateur (en réalité il s’agit
d’un document HTML), soit lors de l’export c’est-à-dire lorsque les documents sortent
de l’environnement Stylo.
En dehors de cette situation, il n’existe aucun document dont l’extension serait
.md et stipulerait que ledit document respecte les règles et normes de ce format.

À la différence des systèmes analogiques et continus, la rupture opérée par
l’écriture numérique réside entre autres dans cette discrétisation du texte
en de multiples documents, où chacun se voit doté d’un paratexte différent pour
circuler à travers les canaux de communication du système d’informations.

Dans Stylo, les documents y sont construits par l’ensemble des protocoles choisis lors
de l’établissement de cet environnement.
La déprise survient lors du choix de l’environnement par l’utilisateur.
Lorsqu’un utilisateur écrit dans Stylo, il accorde sa confiance dans les opérations que
réalise Stylo sur le document et dans la matérialité qu’il participe à lui conférer.

---
