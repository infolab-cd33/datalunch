# Créer une carte dynamique en utilisant CartoDB

- **Niveau** : **Débutant** / **Intermédiaire** / Avancé / Expert
- **Auteur** : 8 Juin 2016
- **Date de MàJ** : 
- **Licence** : CC-BY
- [Pour revenir au dépot](http://datalunch.datalocale.fr)

## Principes
- Créer et nommer une carte dynamique (chronologique) avec CartoDB à partir d'un jeu de données
- Personnaliser les propriétés de la carte : design, textes

## Ingrédients
- Un compte CartoDB https://cartodb.com/
- Une base de données intégrant des coordonnées géographiques (colonnes latitudes et longitudes) au format CSV, xls, odt, etc.

Exemple avec [BDD-Passeports-arrivees.csv](https://github.com/infolab-cd33/datalunch/blob/master/img/Passeports/BDD-Passeports-arrivees.csv). Elle nous indique les destinations de voyages des Girondins en l'an 1800, qui avaient l'obligation de se faire délivrer un passeport pour chacun de leur voyage.


## Étapes
### Se créer un compte (gratuit) et se connecter à CartoDB 
On voit que l'on est identifié car notre *avatar* (photo ou image par défaut) apparaît en haut à droite.

### Création d'un jeu de données
Il y a deux tableaux de bord possibles accessibles à partir de la flèche située en haut à gauche de l'écran : "vos cartes" (yours maps) ou  "vos jeux de données" (your datasets")
![](https://github.com/infolab-cd33/datalunch/blob/master/img/Passeports/cartoDB_dashboard.jpg).

On choisit "You datasets" et on clique sur "New dataset"
![](https://github.com/infolab-cd33/datalunch/blob/master/img/Passeports/cartoDB_newdataset.jpg).

CartoDB nous propose plusieurs options : 
- connecter un jeu de données à partir d'un service externe : Google Drive, Dropbox, Twitter, etc.
- ou charger un jeu de données : par glisser-déposer (Drag&drop), chargement (Browse) ou en lui indiquant l'adresse internet du jeu de données 
![](https://github.com/infolab-cd33/datalunch/blob/master/img/Passeports/cartoDB_browsedataset.jpg)

On clique sur "Browse" pour charger notre jeu de données BDD-Passeports-arrivees.csv. depuis notre ordinateur.
Puis on clique sur "connect dataset", bouton vert situé en bas à droite de l'écran.

Le jeu de donnée apparaît dans une vue au format tableur (colonnes et lignes). 
Observation : CartoDB a identifié les colonnes latitude et longitude du jeu de données et a concaténé ces coordonnées géographiques dans une nouvelle colonne "the_geom".

A ce stade il est possible de modifier le titre du jeu de données, en cliquant directement dans le champ titre situé en haut à gauche de l'écran. Puis cliquer sur "save".

### Création d'une carte dynamique chronologique
Pour basculer vers la visualisation cartographique du jeu de données, cliquer sur "Map View" en haut au centre de l'écran. Vous pourrez revenir à la visualisation du tableur en cliquant sur "Data view".
![](https://github.com/infolab-cd33/datalunch/blob/master/img/Passeports/cartoDB_dataview.jpg)

Par défaut, CartoDB affiche les points géolocalisés de manière statique et en orange. 
![](https://github.com/infolab-cd33/datalunch/blob/master/img/Passeports/cartoDB_cartepardefaut.jpg)

Nous souhaitons que les "destinations" présentes dans le tableur apparaissent de manière progressive selon une chronologie : la "date de délivrance" du passeport. Nous devons donc modifier les paramètres de la carte et son design.

Pour cela, 
- cliquez dans le menu situé à droite de la carte sur le petit onglet intitulé "Wizards" (assistant)
![](https://github.com/infolab-cd33/datalunch/blob/master/img/Passeports/cartoDB_wizards.jpg)
- choisissez dans le menu déroulant le type de carte intitulé "Torque" adapté à une présentation chronologique de points. Le style "Torque Cat" diffère un peu en permettant d'attribuer des couleurs différentes aux points selon des catégories. 

Puis, modifiez les paramètres de la carte selon ce que vous souhaitez visualiser. 
![](https://github.com/infolab-cd33/datalunch/blob/master/img/Passeports/cartoDB_parametres.jpg)

Ici, pour indfiquer les données à afficher :
- Time Column = date_de_delivrance (indique la colonne des données chronologiques)
- Marker Type = ellipse (ou rectangle, au choix)

Pour modifier le design de la carte :
- Marker Fill : paramètre de remplissage des ellipses ou rectangles
- Marker Stroke : paramètre d'affichage des contours des ellipses ou rectangles
- Duration : durée d'affichage des points en secondes
- Steps : il est possible d'afficher l'intégralité des dates du tableur (lignes) ou seulement une partie
- Blend Mode : si vous disposez de différentes couches de données, permet de modifier la façon dont les couches sont mélangées pendant l'animation (ce n'est pas le cas ici)
- Trails : intensité du temps d'affichage du point
- Resolution : résolution d'affichage du point

Cliquer sur la carte pour refermer la fenêtre de menu.

Pour modifier le style du fond de carte, cliquer sur "Basemap", en haut de la carte à gauche, et choisissez celui qui vous convient. 
![](https://github.com/infolab-cd33/datalunch/blob/master/img/Passeports/cartoDB_basemap.jpg)

Cliquez sur "Visualize" en haut à droite de l'écran, puis "OK create Map" pour générer la carte.

Vous pouvez y ajouter un titre, du texte, des images en cliquant sur "Add element" en haut à gauche de la carte.
Vous pourrez la partager ou l'intégrer dans un site web en cliquant sur "Publish" en haut à droite de l'écran.

Résultat : http://bit.ly/1VM7ODy
![](https://github.com/infolab-cd33/datalunch/blob/master/img/Passeports/cartoDB_resultat.jpg)


## Aller + loin : 
- [Tutoriel maison de CartoDB](https://docs.cartodb.com/cartodb-editor/) très complet mais en anglais
- [Tutoriel cartoDB] en anglais sur les options d'édition des cartes de style "Torque" (https://docs.cartodb.com/cartodb-editor/maps/#torque)

## Liens avec d’autres fiches : 
- [Umap créer une carte](http://multibao-pntbr.rhcloud.com/infolab-cd33/datalunch/umap_creer_une_carte.md)

