---
author: Tiers Libres
description: Nettoyer les données à l'aide des fonctions de l'outil de tableur numérique.
image_url : https://www.datalocale.fr/base/images/logo-datalocale.jpg
title: Ouvrir et nettoyer un fichier de données au format CSV
categorie: manipulation
niveau: intermédiaire
date: 04/05/2016
licence: CC-By-SA
---

## Principes - Ce que nous allons faire
- Télécharger un fichier de données au format CSV
- Ouvrir le fichier à l'aide d'un logiciel tableur (voir la fiche fichiers_csv.md)
- Repérer des erreurs et automatiser le croisement des données avec une table de pilote
- Nettoyer les données à l'aide des fonctions de tri, filtre, rechercher&remplacer

## Ingrédients - Ce dont nous avons besoin

- Un outil tableur : [LibreOffice Calc](https://fr.libreoffice.org/download/libreoffice-stable/),
Tableur issu de la suite bureautique open source Libre Office, il interprète le format CSV pour présenter les données en lignes et colonnes sans autre intervention complémentaire de la part de l'utilisateur.
- Un fichier de données au format CSV : liste-site-departement-Gironde_test [[Liste des bâtiments du Conseil départemental de la Gironde](https://github.com/infolab-cd33/datalunch/blob/master/img/nettoyer/liste-sites-departement-Gironde_test.csv)].
Liste des sites gérés par le conseil Départemental de la Gironde sur lesquels se trouvent les différents bâtiments du conseil général accueillant des agents administratifs ou du public.

## Étapes - Comment allons-nous procéder ?

### Télécharger et ouvrir le fichier de données

- cliquer sur l'onglet "raw" puis ctrlA (ou clic droit puis "sélectionner tout" le texte)
- le "copier-coller" dans un bloc note (éditeur de texte), puis "enregistrer sous" le fichier au format CSV sur le bureau ou autre dossier de votre ordinateur.
- clic droit sur le fichier : "ouvrir avec" LibreOffice Calc
- une fois ouvert, il est recommandé d'enregistrer une copie de ce fichier en le renommant par exemple liste-sites_copie afin de ne pas modifier le fichier source.

Premier niveau d'analyse du fichier à vue d'oeil :
- 573 sites sont recensés (il y a 574 lignes au total)
- il contient de nombreuses erreurs (adresses, code postal, décalages colonnes, etc.)

### Générer une "table de pilote" (ou tableau croisé dynamique)

Une table de pilote va permettre de
- repérer rapidement des erreurs dans les cellules du fichier
- répondre facilement et rapidement à des questions en opérant des croisements et traitement statistiques des données

Exemple 1 :
- Sous quels statuts sont recensés les bâtiments du Département (colonne L "statut") ?
- Quel est le nombre de bâtiments par typologie de statut ?

Pour créer la table de pilote :
- sélectionner l'ensemble des données de la feuille où apparaissent les données à traiter (ctrl A)
- cliquer dans le menu "Insertion" puis "table de pilote", puis "OK" pour la proposition par défaut "Sélection active"
- Choix des critères pour la création de la table :
    - champs de la page : rien
    - champs de ligne : statut
    - champs de données : site ==> double clic sur "site" pour faire apparaître les options de fonction et choisir “nombre” afin d'obtenir le calcul du nombre de sites par type de statut

>RQ 1 : on modifie les critères de la table à l’aide de la fonction “éditer la mise en page” (par clic droit dans le tableau).
>RQ 2 : il est facile de retrouver où se situent les erreurs du tableur source. Ici, dans la colonne “statut”, on trouve des dates à la place d’un statut.

### Nettoyer les données
Trois fonctions simples permettent de corriger des erreurs dans un fichier de données. Il faut préalablement sélectionner la colonne dans laquelle on souhaite appliquer la fonctionnalité :

- Fonction de "Filtre"
rubrique Données, choisir "filtre", puis "autofiltre" : une flèche apparaît dans l'en tête de colonne qui permet de visualiser les intitulés (textes) ou valeurs (chiffres, nombre) présents dans la colonne.

Ici, appliquer un autofiltre à la colonne "statut", décocher "tout", sélectionner les "dates" repérées comme étant des erreurs (il s'agit de décalage d'informations dans les cellules), puis nettoyage manuel des lignes par copier-coller des cellules.

- Fonction "Tri"
rubrique Données, puis "trier" : une fenêtre "trier la plage" apparaît, choisir "étendre la sélection" de manière à ce que le tri s'opère sur l'ensemble des colonnes du tableur.
Choisir selon les critères un tri croissant ou décroissant. Les données sont regroupées selon ce critère.

Ici, appliquer un tri sur la colonne "date de création" par exemple pour ordonner les sites du plus ancien au plus récent.    

- Fonction "rechercher&remplacer"
Elle permet de supprimer dans une colonne sélectionnée un élément indésiré, par exemple une parenthèse ouverte '(' ou un "0" au début d'une suite de chiffres.
	- Sélection de la colonne
	- rubrique Edition, rechercher&remplacer : une fenêtre apparaît
	- indiquer l'élément "(" à "rechercher", puis laisser vide l'emplacement "rechercher par"
	- Cliquer sur "tout remplacer" (puis décocher "cellulles entières" s'il s'agit uniquement d'une partie de la cellule) pour que la parenthèse soit supprimée dans toutes les cellules de la colonne.
	- valider en cliquant sur "fermer"

Ici, appliquer la fonction sur la colonne "Ville", rechercher "Villenave d'ornon" (sans tiret) et remplacer par "Villenave-d'ornon" (avec tiret), par exemple.


## Pour aller plus loin :

- [Aide de Libre Office Calc](https://help.libreoffice.org/Calc/Welcome_to_the_Calc_Help/fr)
- [Apprendre à créer un tableau croisé dynamique avec LibreOffice Calc ](http://malick-nseck.developpez.com/tutoriels/apprendre-a-creer-tableau-croise-dynamique-avec-libre-office-calc/)

## A savoir :

Le fichier csv encodé en UTF8, avec pour séparateur la virgule ou le point virgule, est communément trouvé sur les portails opendata.

## Liens avec d’autres fiches :

- [Ouvrir et nettoyer un fichier CSV](./#fiches/ouvrir_et_nettoyer_fichier_csv.md)
