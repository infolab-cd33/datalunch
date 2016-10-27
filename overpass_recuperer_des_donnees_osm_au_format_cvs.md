# Récupérer des données dans OpenStreetMap

- **Niveau** : Débutant / Intermédiaire / **Avancé** / Expert
- **Auteur** : Tiers-Libres
- **Date de MàJ** : 26/10/2016
- **Licence** : CC-BY
- [Pour revenir au dépot](http://datalunch.datalocale.fr)

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

