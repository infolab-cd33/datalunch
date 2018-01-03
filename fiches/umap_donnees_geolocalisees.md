---
author:  Vincent Bergeot
description: Insérer un fichier de données géolocalisées dans une carte Umap
image_url : https://www.datalocale.fr/base/images/logo-datalocale.jpg
title: Insérer des données géolocalisées dans Umap
link: https://github.com/infolab-cd33/datalunch/umap_donnees_geolocalisees.md
categorie: geomatique
niveau: débutant
date: 02/12/2015
licence: CC-By-SA
---

## Principes - Ce que nous allons faire
Insérer un fichier de données géolocalisées dans une carte Umap

## Ingrédients - Ce dont nous avons besoin
- Une carte Umap
- Un fichier de données géolocalisées par exemple en monfichier.csv

## Étapes - Comment allons-nous procéder ?
### Import de données à partir de monfichier.csv
On clique sur la flèche vers le haut, dans le menu de droite
![Importer des données](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/umap/Importer_des_donnees_sur_uMap_-_Etape0.png)

On va sélectionner son fichier monfichier.csv

Pour tester son fichier et ne pas le mélanger si il comporte des erreurs, on importe dans un nouveau calque. Si les données sont correctement importées, alors on efface le calque et on re-importe dans le calque approprié.

N.B : Attention les titres des colonnes ne doivent comporter ni accents, ni espaces. Pour séparer 2 termes utilisez des tirets (- ou _ )

Pour les colonnes contenant les coordonnées géographiques, vérifiez que le séparateur entre les degrés et les minutes est bien un point et pas une virgule (ex: 44.12345 plutôt que 44,46565)

## Aller + loin :
[Des guides](http://wiki.openstreetmap.org/wiki/FR:UMap/Guide) et [des vidéos](http://wiki.openstreetmap.org/wiki/UMap#Screencasts)

## A savoir :
Il existe plusieurs instances du logiciel Umap :

* [uMap](http://umap.openstreetmap.fr/fr/) / hébergée par [l'association OpenStreetMap France](http://openstreetmap.fr/)
* [Framacarte](https://framacarte.org) / hébergée par [l'association Framasoft](http://framasoft.net/)

## Liens avec d’autres fiches :
- [Géocoder un fichier d'adresse .csv](./#fiches/geocodage.md)
- [Créer une carte Umap](./#fiches/umap_creer_une_carte.md)
