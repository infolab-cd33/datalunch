---
author:  Vincent Bergeot
description: Insérer le tracé de la limite d'une commune dans une carte Umap
image_url : http://umap.openstreetmap.fr/static/umap/img/logo.svg?1ba3dd07e5e5
title: Insérer la limite d'une commune
link: https://github.com/infolab-cd33/datalunch/umap_limite_commune.md
categorie: geomatique
niveau: débutant
date: 15/02/2016
licence: CC-By-SA
---

## Principes - Ce que nous allons faire
- Insérer la limite d'une commune dans Umap

## Ingrédients - Ce dont nous avons besoin
- Une carte Umap
- Un fichier geojson de la limite communale

## Étapes - Comment allons-nous procéder ?
### Import de données à partir de monfichier.geojson
On clique sur la flèche vers le haut, dans le menu de droite

![Importer des données](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/umap/Importer_des_donnees_sur_uMap_-_Etape0.png)

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
- [Géocoder un fichier d'adresse .csv](./#fiche/geocodage.md)
- [Créer une carte Umap](./#fiche/umap_creer_une_carte.md)
* [Fermer la limite de la commune dans OpenStreetMap](./#fiche/josm_fermer_une_commune.md)
* [Récupérer la limite d'une commune venant d'OpenStreetMap](./#fiche/overpass_recuperer_limite_commune.md)
