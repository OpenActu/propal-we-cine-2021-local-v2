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
