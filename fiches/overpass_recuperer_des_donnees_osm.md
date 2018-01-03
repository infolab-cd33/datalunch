---
author:  Vincent Bergeot
description: récupérer des données provenant d'OpenStreetMap
image_url : https://www.datalocale.fr/base/images/logo-datalocale.jpg
title: Récupérer des données dans OpenStreetMap
categorie: geomatique
licence: CC-By-SA
niveau : avancé
date: 05/01/2016
---

## Principes - Ce que nous allons faire
Nous allons récupérer des données dans OpenStreetMap.

## Ingrédients - Ce dont nous avons besoin
* les couples clé=valeurs correspondants aux données dans OpenStreetMap

## Étapes - Comment allons-nous procéder ?

### se rendre sur un site overpass
* par exemple : http://overpass-turbo.eu/

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/overpass-01.jpg)

### saisir une requète overpass
* ouvrir l'assistant

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/overpass-02.png)

* écrire le couple "clé=valeur" rechercher/ par exemple amenity=school

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/overpass-03.png)

* Exécuter la requête

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/overpass-04.jpg)

### Améliorer sa requête
* Par défaut, la requête s’exécute sur la portion de carte visible (appelé bbox)
* Pour préciser sur une commune, dans l'assistant écrire par exemple : amenity=school in Créon

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/overpass-05.png)

* Les booléens existent : AND et OR, donc par exemple dans l'assistant amenity=school and school:FR=Maternelle in Créon

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/overpass-06.png)

* Transformer les surfaces en points
 * Dans la zone print results de la requête ajouter center après out body : out body center

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/overpass-07.png)

 * Exécuter / cela affiche à la fois la surface et un point au centre / les deux objets contiennent les mêmes informations
 * Ne plus voir les surfaces est possible en sortant "out skel qt;"

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/overpass-08.png)

 * Exécuter la requête / cela affiche seulement un point au centre contenant toute les informations

### exporter la requête
* cliquer sur exporter

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/overpass-09.png)

 * pour construire une carte dynamique dans Umap :
  * choisir "données brutes depuis l'API Overpass"
  * sélectionner l'adresse générée, la copier
 * les autres options permettent de récupérer les données sous divers formats

## Aller + loin :
Quelques sources :

## A savoir :

## Liens avec d’autres fiches :
