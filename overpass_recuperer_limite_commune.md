# Overpass, récupérer la limite d'une commune

- **Niveau** : Débutant / **Intermédiaire** / Avancé / Expert
- **Auteur** : Vincent Bergeot
- **Date de MàJ** : 15/02/2016
- **Licence** : CC-by-sa
- [Pour revenir au dépot](http://datalunch.datalocale.fr)

## Principes - Ce que nous allons faire
* Récupérer la limite administrative d'une commune
## Ingrédients - Ce dont nous avons besoin
* Une connexion internet,
* Le tag pour une limite communale -> admin_level=8
* Le nom d'une commune -> par exemple : Créon
## Étapes - Comment allons-nous procéder ?
* [Aller sur Overpass](http://overpass-turbo.eu/)

* Construire et exécuter la requête avec l'assistant ![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/overpass/overpass-commune-1.png)

   * Cela donne ceci : 
![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/overpass/overpass-commune-2.png)

* exporter le résultat en geojson et enregistrer le sur votre ordinateur,
![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/overpass/overpass-commune-3.png)


## Aller + loin : 
Quelques sources : 

## A savoir : 


## Liens avec d’autres fiches : 
* [Insérer les limites d'une commune dans Umap](http://datalunch.datalocale.fr/infolab-cd33/datalunch/umap_limite_commune.md)
* [Fermer la limite de la commune dans OpenStreetMap](http://datalunch.datalocale.fr/infolab-cd33/datalunch/josm_fermer_une_commune.md)