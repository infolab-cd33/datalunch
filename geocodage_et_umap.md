# Qualité du tableur de données
on s'assure que les titres de colonnes aient des noms explicites mais sans caractères "particuliers" (pas d'accents, d'apostrophes, pas d'espaces)

# Export en format .csv (comma separated value)
Enregistrer sous sonnom.csv
cela ne sauvegarde pas les modifications, on fait bien un export du feuillet en cours

# Géocodage des données
* On va se servir de Addok, géocodeur : http://adresse.data.gouv.fr/csv/
* on y importe le fichier sonnom.csv,
* on glisse les colonnes adresse,
* ville qui nous intéresse pour le géocodage,
* on sélectionne le code postal correspondant,
* on s'assure d'avoir le bon encodage (pas de caractères anormaux dans la prévisualisation).
* On clique sur Lancer et on récupère un fichier en sonnom.geocoded.csv, qui comprend toutes les informations de sonnom.csv, plus des colonnes supplémentaires avec lattitude, longitude, l'adresse que cela renvoie, si c'est un numéro de rue, de maison, de ... code insee, et un result_score

## Vérification du géocodage
On ouvre le fichier sonnom.geocoded.csv et en particulier on regarde le result_score. On vérifie aussi le result_city, contexte, ...
Si il est trop proche de zéro, il y a des erreurs
Si il est proche de un, on est bon !

L'import dans Umap va également nous donner des infos sur la "qualité des données" du tableur initial.

# Cartographie avec Umap
[uMap](http://umap.openstreetmap.fr/fr/) permet de créer des cartes personnalisées sur des fonds OpenStreetMap en un instant et les afficher dans votre site.

[Des guides](http://wiki.openstreetmap.org/wiki/FR:UMap/Guide= et [des vidéos](http://wiki.openstreetmap.org/wiki/UMap#Screencasts)

## Configuration du compte umap
- On se crée un compte osm
- On fait un lien avec un compte (connection), je vous propose OpenStreetMap (OSM).
- Cela permet de retrouver toutes ses cartes

## Création d'une carte
* L'interface de [Umap](http://umap.openstreetmap.fr)

à gauche surtout la navigation et l'affichage
à droite les propriétés et fonctionnalités de l'ensemble de la carte (partage, édition, import, propriétés ...)


## Configuration
Garder en tête la filiation :)
Propriétés des cartes -> propriétés des calques -> propriétés des données
Cela va permettre d'hériter des propriétés ou de singulariser les propriétés carte > calque > donnée

On pourra toujours les modifier par la suite

	* Propriété de la carte
	* Propriété des calques
	* Propriétés des données

## Import de données à partir de sonnom.geocoded.csv

la flèche vers le haut, dans le menu de droite
!(https://wiki.openstreetmap.org/w/images/f/f7/Importer_des_donn%C3%A9es_sur_uMap_-_Etape0.PNG)
On importe dans un nouveau calque pour tester

### Personnalisation du calque

### Choix des pop-ups
