---
title: "Déploiement d'une instance de Stylo"
date: 2024-11-11
---

J'écris ce billet dans le but de garder une archive des étapes par
lesquelles je suis passé pour déployer une nouvelle instance de Stylo.

L'objectif de cette manipulation était à la fois de tester le guide
de déploiement que l'on a sur le
[dépôt de Stylo](https://github.com/RochDLY/stylo) et de comprendre un
peu mieux le fonctionnement de Stylo.

J'ai donc commencé par faire un fork de stylo (voir le lien précédent) et
j'ai installé une machine virtuelle ubuntu server 24.04.1 LTS.

## Liste des problèmes rencontrés

### Installation de Docker

Une fois installée et lancée, la documentation de Stylo nous indique que
tout commence avec l'installation de Docker (et Docker compose).

Dans la documentation, il y a cette ligne de commande :

`sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose`

Cette commande est obsolète, elle renvoie à la version `1.25.5` de docker-compose et génère des erreurs lors du build des conteneurs.

Pour parer à ce problème, la solution consiste à prendre la dernière version de docker, soit en changeant le `1.25.5` par la dernière version, soit en suivant la [documentation officielle de docker](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)

En suivant la documentation, on ajoute docker au dépôt et à chaque `atp-get update && apt-get upgrade` docker est mis à jour (attention que ça ne crée pas de conflit, il ne faut pas faire automatiquement la mise à jour).

### Désactivation du Apparmor sous Ubuntu

Il s'agit là d'un problème récurrent sur Ubuntu avec Docker : il est impossible de stopper un conteneur si l'application apparmor est lancée (et elle tourne automatiquement sous ubuntu).

Une solution un peu violente consiste à suivre les lignes de commandes suivantes :

```sh
sudo aa-remove-unknown
sudo service apparmor teardrop
sudo service docker restart
docker system prune --all --volumes
docker compose down
```

Avec ces commandes et pour tout le reste de la session, on pourra relancer / stopper les conteneurs autant de fois qu'on le veut.

### Nginx n'accède pas au répertoire de Stylo

`sudo chmod -R +x /path/to/stylo`

### Accès à Internet depuis la VM

Quelques paramètres réseaux à régler avant de pouvoir déployer l'instance de Stylo.
Pour permettre les requêtes et saisir des données, il faut ouvrir les ports 80 et 443 du réseau pour la VM.
Dans mon cas, la VM partageait le réseau de la distribution hôte (un windows) et n'était pas rendue visible depuis l'interface du réseau `192.168.1.1`.
Pour la rendre visible il ne faut pas que la VM profite du réseau hôte mais faire un `bridge`. De cette manière, la box internet peut détecter la VM comme une entité distincte.

### Build avec npm

Avec les derniers changements de Stylo, il est nécessaire de faire tourner node en parallèle de docker pour builder l'image de Stylo.

On peut suivre la documentation comme suit : 

1. Copier le fichier de configuration `cp stylo-example.env .env`
2. Générer le token GraphQL à renseigner en fin de `.en` avec `docker compose run -ti --build --rm graphql-stylo npm run generate-service-token --silent`
3. Modifier les URLs dans le `.env` pour qu'elles correspondent à l'URL de la nouvelle instance de Stylo (attention à bien renseigner `SNOWPACK_PUBLIC_GRAPHQL_ENDPOINT`)
3. `npm clean-install`
4. `npm --prefix front clean-install`
5. `npm --prefix export clean-install`
6. `npm --prefix graphql clean-install`

### Renseigner le fichier de configuration nginx

Suivre la [documentation](https://github.com/EcrituresNumeriques/stylo/blob/master/SERVER.md#install-a-reverse-proxy-nginx) sur github.

Penser à modifier le fichier de configuration : `/etc/nginx/sites-enabled/stylo.huma-num.fr.conf`.

### Construire les images docker

```sh
docker compose up -d mongodb-stylo export-gateway pandoc-api
npm run dev
```

Le paramètre `-d` de la commande `docker compose` permet de faire passer docker en arrière-plan (en daemon). On peut tout de suite lancer `npm run dev` dans le même terminal pour voir ce qu'il se passe sur cette nouvelle instance Stylo.

Lancer `npm` en parallèle du `docker compose` permet de sourcer correctement le
`.env` (cf [package.json sur
github](https://github.com/EcrituresNumeriques/stylo/blob/master/package.json#L15)).

Attention : cette partie est susceptible de changer bientôt, cf [#1097](https://github.com/EcrituresNumeriques/stylo/issues/1097).
