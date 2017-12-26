---
author:  Vincent Bergeot
description: Insérer le tracé de la limite d'une commune dans une carte Umap
image_url : https://www.datalocale.fr/base/images/logo-datalocale.jpg
title: Insérer la limite d'une commune
link: https://github.com/infolab-cd33/datalunch/umap_limite_commune.md
categorie: geomatique
niveau: débutant
date: 15/02/2016
licence: CC-By-SA
---

[Pour revenir au dépot](http://datalunch.datalocale.fr)

## Principes - Ce que nous allons faire
- Insérer la limite d'une commune dans Umap

## Ingrédients - Ce dont nous avons besoin
- Une carte Umap
- Un fichier geojson de la limite communale

## Étapes - Comment allons-nous procéder ?
### Import de données à partir de monfichier.geojson
On clique sur la flèche vers le haut, dans le menu de droite
![Importer des données](https://wiki.openstreetmap.org/w/images/f/f7/Importer_des_donn%C3%A9es_sur_uMap_-_Etape0.PNG)

On va sélectionner son fichier monfichier.geojson

Pour tester son fichier et ne pas le mélanger si il comporte des erreurs, on importe dans un nouveau calque.

Si les données sont correctement importées, alors on efface le calque et on re-importe dans le calque approprié.


## Aller + loin :
[Des guides](http://wiki.openstreetmap.org/wiki/FR:UMap/Guide) et [des vidéos](http://wiki.openstreetmap.org/wiki/UMap#Screencasts)

## A savoir :
Il existe plusieurs instances du logiciel Umap :

* [uMap](http://umap.openstreetmap.fr/fr/) / hébergée par [l'association OpenStreetMap France](http://openstreetmap.fr/)
* [Framacarte](https://framacarte.org) / hébergée par [l'association Framasoft](http://framasoft.net/)

## Liens avec d’autres fiches :
- [Géocoder un fichier d'adresse .csv](http://datalunch.datalocale.fr/infolab-cd33/datalunch/geocodage.md)
- [Créer une carte Umap](http://datalunch.datalocale.fr/infolab-cd33/datalunch/umap_creer_une_carte.md)
* [Fermer la limite de la commune dans OpenStreetMap](http://datalunch.datalocale.fr/infolab-cd33/datalunch/josm_fermer_une_commune.md)
* [Récupérer la limite d'une commune venant d'OpenStreetMap](http://datalunch.datalocale.fr/infolab-cd33/datalunch/overpass_recuperer_limite_commune.md)
