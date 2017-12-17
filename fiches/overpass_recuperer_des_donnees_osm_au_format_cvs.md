---
author: Tiers Libres
description: récupérer des données provenant d'OpenStreetMap au format csv pour pouvoir l'utiliser dans un tableur
image_url : https://www.datalocale.fr/base/images/logo-datalocale.jpg
title: Récupérer des données dans OpenStreetMap
link: https://github.com/infolab-cd33/datalunch/overpass_recuperer_des_donnees_osm_au_format_cvs.md
categorie: géomatique
licence: CC-By-SA
niveau : avancé
date: 26/10/2016
---

[Pour revenir au dépot](http://datalunch.datalocale.fr)

## Principes - Ce que nous allons faire
Nous allons récupérer des données provenant d'OpenStreetMap au format csv pour pouvoir l'utiliser dasn un tableur

## Ingrédients - Ce dont nous avons besoin
* les couples clé=valeurs correspondants aux données dans OpenStreetMap
* un exemple de requête
>[out:csv(name, amenity, "school:FR")][timeout:25];  
{{geocodeArea:Gironde}}->.searchArea;  
(
  node["school:FR"="collège"](area.searchArea);
  way["school:FR"="collège"](area.searchArea);
  relation["school:FR"="collège"](area.searchArea);
);  
out center;  
out skel qt;

## Étapes - Comment allons-nous procéder ?

### se rendre sur un site overpass
* par exemple : http://overpass-turbo.eu/
![](http://www.datalocale.fr/drupal7/sites/default/files/fiches/overpass-01.png)
### saisir une requête overpass
* remplacer la requête par la requête adaptée
* modifier le lieu de requête, les objets recherchés (tags OSM)
* Exécuter la requête
![](http://www.datalocale.fr/drupal7/sites/default/files/fiches/overpass-04.png)

Dans l'exemple donné ci-dessus, voici ce que cela donne sur le [site](http://overpass-turbo.eu/s/jDp).

## Aller + loin :
Quelques sources :

## A savoir :

## Liens avec d’autres fiches :
