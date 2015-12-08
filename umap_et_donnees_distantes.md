# se rendre sur un site overpass
* http://overpass-turbo.eu/

# saisir une requète overpass
* ouvrir l'assistant
* écrire le couple "clé=valeur" rechercher/ par exemple amenity=school
* Exécuter la requête

# Améliorer sa requête
** par défaut, la requête s’exécute sur la portion de carte visible (appelé bbox)
** pour préciser sur une commune, dans l'assistant écrire par exemple : amenity=school in Créon
** les booléens existent : AND et OR, donc par exemple dans l'assistant amenity=school and school:FR=Maternelle in Créon
** "transformer" les surfaces en points
*** dans la zone print results de la requête ajouter center après out body : out body center -> exécuter / cela affiche à la fois la surface et un point au centre / les deux objets contiennent les mêmes informations
*** ne plus voir les surfaces est possible en sortant "out skel qt;" -> exécuter la requête / cela affiche seulement un point au centre contenant toute les informations 

# exporter la requête
* cliquer sur exporter
* données brutes depuis l'API Overpass
* sélectionner l'adresse générée, la copier

# Umap / Créer une carte
voir fiche

# Umap / Créer un calque
voir fiche

# Umap / Ajouter des données distantes
* dans les propriétés du calque, choisir Données distantes
* Dans URL, coller l'adresse provenant des données brutes de l'overpass
* sélectionner le format de données, ici osm
* si vous le souhaitez vous pouvez définir la zone d’exécution (en zoom) de la requête
* sélectionner dynamique pour que la mise à jour se fasse à chaque connection à la carte
* enregistrer

# Umap / Zoomer sur les données
* choisir le calque
* cliquer sur la loupe
