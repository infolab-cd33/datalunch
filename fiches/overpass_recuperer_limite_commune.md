---
author:  Vincent Bergeot
description: récupérer des données provenant d'OpenStreetMap
image_url : https://upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Openstreetmap_logo.svg/145px-Openstreetmap_logo.svg.png
title: Overpass, récupérer la limite d'une commune
link: https://github.com/infolab-cd33/datalunch/overpass_recuperer_limite_commune.md
categorie: geomatique
niveau: intermédiaire
licence: CC-By-SA
date: 15/02/2016
---

## Principes - Ce que nous allons faire
* Récupérer la limite administrative d'une commune
## Ingrédients - Ce dont nous avons besoin
* Une connexion internet,
* Le tag pour une limite communale -> admin_level=8
* Le nom d'une commune -> par exemple : Créon
## Étapes - Comment allons-nous procéder ?
* [Aller sur Overpass](http://overpass-turbo.eu/)

* Construire et exécuter la requête avec l'assistant

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/overpass/overpass-commune-1.png)

   * Cela donne ceci :

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/overpass/overpass-commune-2.png)

* exporter le résultat en geojson et enregistrer le sur votre ordinateur,

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/overpass/overpass-commune-3.png)


## Aller + loin :
Quelques sources :

## A savoir :


## Liens avec d’autres fiches :
* [Insérer les limites d'une commune dans Umap](./#fiche/umap_limite_commune.md)
* [Fermer la limite de la commune dans OpenStreetMap](./#fiche/josm_fermer_une_commune.md)
