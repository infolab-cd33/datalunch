---
author: Pascal Romain
description: >-
  À partir d'un export des données d'osm en geojson, nous allons transformer ces
  données pour pouvoir les enregistrer dans un fichier au format .csv.
image_url: http://adresse.data.gouv.fr/static/img/csv-grey.svg
title: Exporter les données d'open street map dans un fichier csv
published: true
---

# Exporter les données d'open street map dans un fichier csv

- **Niveau** : Intermédiaire
- **Auteur** : Pascal Romain
- **Date de MàJ** : 27/08/2016
- **Licence** : CC-by-sa
- [Pour revenir au dépot](https://infolab-cd33.github.io/daktary/)

## Principes - Ce que nous allons faire

* exporter des données d'open street map
* importer ces données dans un outil de conversion
* exporter les données converties dans un fichier csv

## Ingrédients - Ce dont nous avons besoin

Pour ce tutoriel nous pouvons utiliser les applications sans authentification. Il faut donc juste connaître les adresses web (url) des 2 services que nous allons utiliser : 

* [overpass](http://overpass-turbo.eu/) : une interface pour faciliter l'extraction de données de la base de données d'open street map
* [geojson.io](http://geojson.io) : un outil de cartographie, spécialisé dans le format de données geojson et qui dispose d'outils de conversion et d'import/export très pratiques.

## Étapes - Comment allons-nous procéder ?

La première étape consiste à extraire les données d'osm en utilisant l'assistant fournit par overpass. Cette étape est décrite dans la fiche [export des données d'osm](https://infolab-cd33.github.io/daktary/#infolab-cd33/datalunch/blob/master/overpass_recuperer_des_donnees_osm.md) mais je vais en reprendre ici rapidement les étapes :

Note : il peut arriver que le service overpass "plante" car le nombre de données à retourner dans le navigateur est trop important. Il faut parfois réduire la couverture géographique pour laquelle on souhaite extraire des données ou utiliser un autre moyen d'extraction.

* sélectionner le département de la Gironde par exemple 

![illustration overpass](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/selectionOverpass.PNG)

* cliquer sur assistant
* consulter la liste des points d'intérêts disponibles dans le schéma de la base de données [wiki](http://wiki.openstreetmap.org/wiki/Key:amenity)
* récupérer la liste par exemple des boîtes à livres (amenity=public_bookcase)
* saisir ce couple clé/valeur dans la fenêtre de l'assistant

![illustration overpass](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/assistantOverpass.png)

* cliquer sur construire et exécuter une requête
* cliquer sur exporter et choisir le format geojson

![illustration geojson](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/export-csv-osm/exportGeojson.png)

* sélectionner les données exportées et les copier ou enregistrer le résultat dans un fichier sur le disque dur de l'ordinateur
* se rendre sur le site [geojson.io](http://geojson.io)
* cliquer sur open > geojson
* si tout se passe bien, les données extraites d'osm apparaissent sur l'écran.
* A partir de là les données d'osm sont éditables et on peut changer la forme et l'apparence des marqueurs, modifier les données ou en ajouter.
* ensuite il suffit de cliquer sur save pour enregistrer le résultat dans une variété de format différent. Nous choisissons pour ce tutoriel csv car le résultat est ensuite consultable dans un tableur numérique de type calc ou excel et qu'il est possible d'importer le résultat dans le prévisualiseur de la ressourcerie datalocale.

## Aller + loin : 
Quelques sources : 

* [liste des points d'intérêts osm](http://wiki.openstreetmap.org/wiki/Amenity)
* [overpass](http://wiki.openstreetmap.org/wiki/Overpass_turbo)

## A savoir : 

Le format geojson est un format inspiré du format json très utilisé par les développeurs informatiques pour sa syntaxe souple et sa conscision. C'est un format ouvert également souvent utilisé par les bibliothèques de visualisation de données [wikipedia](https://fr.wikipedia.org/wiki/GeoJSON)
## Liens avec d’autres fiches :
