---
author: Vincent Bergeot
description: Ajouter des informations à la limite administrative d'une commune pour obtenir une limite utilisable dans Umap.
image_url : https://upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Openstreetmap_logo.svg/145px-Openstreetmap_logo.svg.png
title: Fermer la limite administrative d'une commune
link: https://github.com/infolab-cd33/datalunch/josm_fermer_une_commune.md
categorie: geomatique
niveau: avancé
date: 17/02/2016
licence: CC-By-SA
---

## Principes - Ce que nous allons faire
* Ajouter des informations à la limite administrative d'une commune pour obtenir une limite utilisable dans Umap

## Ingrédients - Ce dont nous avons besoin
* [JOSM](https://josm.openstreetmap.de/), éditeur Java pour OpenStreetmap
* une connexion internet,
* Une limite communale dont les chemins (ways) ne sont pas de "type=outer,

## Étapes - Comment allons-nous procéder ?
* Ouvrir JOSM
* Récupérer la commune qui nous intéresse : Fargues,
![Télécharger la commune qui nous intéresse](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/josm/josm_outer_3.png)

* Identifier et éditer la relation,

![Édition de la relation](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/josm/josm_outer_4.png  "")

* Ajouter le rôle "outer" aux "chemins" de la relation,

![Édition de la relation](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/josm/josm_outer_5.png)

* Valider
* Envoyer les modifications sur OpenStreetMap

## Aller + loin :
Quelques sources :

## A savoir :

## Liens avec d’autres fiches :
