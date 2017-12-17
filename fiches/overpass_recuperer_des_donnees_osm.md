---
author:  Vincent Bergeot
description: récupérer des données provenant d'OpenStreetMap
image_url : https://www.datalocale.fr/base/images/logo-datalocale.jpg
title: Récupérer des données dans OpenStreetMap
link: https://github.com/infolab-cd33/datalunch/overpass_recuperer_des_donnees_osm.md
categorie: géomatique
licence: CC-By-SA
niveau : avancé
date: 05/01/2016
---

[Pour revenir au dépot](http://datalunch.datalocale.fr)

## Principes - Ce que nous allons faire
Nous allons récupérer des données dans OpenStreetMap.

## Ingrédients - Ce dont nous avons besoin
* les couples clé=valeurs correspondants aux données dans OpenStreetMap

## Étapes - Comment allons-nous procéder ?

### se rendre sur un site overpass
* par exemple : http://overpass-turbo.eu/
![](http://www.datalocale.fr/drupal7/sites/default/files/fiches/overpass-01.png)
### saisir une requète overpass
* ouvrir l'assistant
![](http://www.datalocale.fr/drupal7/sites/default/files/fiches/overpass-02.png)
* écrire le couple "clé=valeur" rechercher/ par exemple amenity=school
![](http://www.datalocale.fr/drupal7/sites/default/files/fiches/overpass-03.png)
* Exécuter la requête
![](http://www.datalocale.fr/drupal7/sites/default/files/fiches/overpass-04.png)
### Améliorer sa requête
* Par défaut, la requête s’exécute sur la portion de carte visible (appelé bbox)
* Pour préciser sur une commune, dans l'assistant écrire par exemple : amenity=school in Créon
![](http://www.datalocale.fr/drupal7/sites/default/files/fiches/overpass-05.png)
* Les booléens existent : AND et OR, donc par exemple dans l'assistant amenity=school and school:FR=Maternelle in Créon
![](http://www.datalocale.fr/drupal7/sites/default/files/fiches/overpass-06.png)
* Transformer les surfaces en points
 * Dans la zone print results de la requête ajouter center après out body : out body center
![](http://www.datalocale.fr/drupal7/sites/default/files/fiches/overpass-07.png)
 * Exécuter / cela affiche à la fois la surface et un point au centre / les deux objets contiennent les mêmes informations
 * Ne plus voir les surfaces est possible en sortant "out skel qt;"
![](http://www.datalocale.fr/drupal7/sites/default/files/fiches/overpass-08.png)
 * Exécuter la requête / cela affiche seulement un point au centre contenant toute les informations

### exporter la requête
* cliquer sur exporter
![](http://www.datalocale.fr/drupal7/sites/default/files/fiches/overpass-09.png)
 * pour construire une carte dynamique dans Umap :
  * choisir "données brutes depuis l'API Overpass"
  * sélectionner l'adresse générée, la copier
 * les autres options permettent de récupérer les données sous divers formats

## Aller + loin :
Quelques sources :

## A savoir :

## Liens avec d’autres fiches :
