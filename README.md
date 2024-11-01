# Installation

## Pré-requis

Docker 23.7 et GIT 2.34 doivent préalablement être installé en ligne de commande

# Guide d'installation de l'environnement

1. Créer un répertoire de travail dans lequel sera déposé les sources
```
mkdir propal-we-cine-2021 &&
cd propal-we-cine-2021 &&
git clone https://git.intranet.dita-transport.com/dita-services/propal-we-cine-2021/local.git &&
git clone https://git.intranet.dita-transport.com/dita-services/propal-we-cine-2021/webapp.git &&
mkdir -p local/php8/log/apache2/webapp &&
mkdir -p local/php8/share/webapp &&
cd local &&
docker compose up -d
```

2. Installation de webapp

Se reférrer à *../webapp/README.md*

3. Installation de minio 

Cette étape, il faut se connecter à l'interface web (http://localhost:9001). Les actions à mener sont les suivantes : 
* Création d'un utilisateur 
Cliquez sur Identity, Users, puis Create a user.
Définissez une access key (username), une secret key (password) et sélectionnez la politique d'accès "readwrite", ensuite un bucket.
Ces variables sont référencé au sein de webapp respectivement par MINIO_ACCESS_KEY, MINIO_SECRET_KEY et MINIO_BUCKET au travers du .env

Important: La configuration est essentielle pour que les tests de validation sur MINIO soient opérationnels