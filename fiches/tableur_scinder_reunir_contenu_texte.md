---
author:  Suzanne Galy
description: Manipuler le contenu d'une cellule de tableur numérique pour extraire des données
image_url : https://github.com/infolab-cd33/datalunch/raw/master/img/csv/file_formats_4_csv-512.png
title: Tableur : scinder ou réunir du contenu texte
link: https://github.com/infolab-cd33/datalunch/overpass_recuperer_limite_commune.md
categorie: geomatique
licence: CC-By-SA
date: 10/10/2016
niveau: intermédiaire
---

## Principes - Ce que nous allons faire
Nous allons scinder le texte d'une colonne en une ou plusieurs colonnes distinctes. Nous allons ensuite regrouper le contenu texte de plusieurs cellules en une seule et même cellule (concatener).

## Ingrédients - Ce dont nous avons besoin

- Un outil tableur : [LibreOffice Calc](https://fr.libreoffice.org/download/libreoffice-stable/),
Tableur issu de la suite bureautique open source Libre Office.
- Un fichier de données au format CSV : liste-site-departement-Gironde_test [[Liste des bâtiments du Conseil général de la Gironde](https://github.com/infolab-cd33/datalunch/blob/master/img/nettoyer/liste-sites-departement-Gironde_test.csv)].
Liste des sites gérés par le conseil général sur lesquels se trouvent les différents bâtiments du conseil général accueillant des agents administratifs ou du public.

## Étapes - Comment allons-nous procéder ?

### Télécharger et ouvrir le fichier

* cliquer sur l'onglet "raw" puis ctrlA (ou clic droit puis "sélectionner tout" le texte)
* le "copier-coller" dans un bloc note (éditeur de texte), puis "enregistrer sous" le fichier au format CSV sur le bureau ou autre dossier de votre ordinateur.
* clic droit sur le fichier : "ouvrir avec" LibreOffice Calc
* une fois ouvert, il est recommandé d'enregistrer une copie de ce fichier en le renommant par exemple liste-sites_copie afin de ne pas modifier le fichier source.

### Scinder du texte contenu dans une cellule en une nouvelle colonne ou plusieurs

Tout d'abord, pour ne pas écraser le texte des colonne existantes dans le tableur, il faut créer une ou plusieurs nouvelles colonnes vides à droite de celle que l'on souhaite scinder.
Ici,
* sélectionner la colonne L "Statut"
* clic droit sur l'en-tête "L" et choisir "insérer des colonnes à gauche". Répéter l'opération deux fois.
Puis,
* sélectionner la colonne K "date de création"
* dans le menu "Données", choisir "texte en colonnes"
* une nouvelle fenêtre s'ouvre. Choisir le délimiteur de scission du texte. Ici, il s'agit de la barre oblique "/" que l'on tape dans le champ texte "Autre" (une visualisation du résultat apparait en dessous)
* cliquer sur OK

On dispose désormais de trois colonnes à renommer : "jour de création", "mois de création" et "année de création"

### Réunir le contenu texte de plusieurs cellules : concatener.

Cette fonction s'appelle "Concatener". Nous allons la mettre en oeuvre pour regrouper le texte des trois colonnes "jour", "mois" et "année" que nous venons de créer dans le fichier.
Pour cela :
* créer une nouvelle colonne N à droite de la colonne M.
* dans la première celulle de la 2e ligne, insérer la formule suivante :

    =CONCATENER (K2;"/";L2;"/";M2)

Cette formule indique :
* les cellules à regrouper : K2, L2 et M2
* les autres éléments de délimitation de texte que l'on souhaite insérer (un espace, une parenthèse, une barre oblique, etc.) indiqués entre-guillemets
Tout ces éléments doivent être séparés par un point-virgule.

* Puis cliquer sur OK pour obtenir le résultat souhaité

## Aller + loin :
* [Aide de Libre Office Calc](https://help.libreoffice.org/Calc/Welcome_to_the_Calc_Help/fr)

## A savoir :
Le format csv est un format ouvert et libre. Il ne permet pas de stocker des formules ni leurs résultats comme Excel ou Calc mais il peut être lu aussi bien par un humain que par un ordinateur ce qui en fait un format d'interopérabilité.

## Liens avec d’autres fiches
* [Ouvrir et nettoyer un fichier CSV](./#fiche/ouvrir_et_nettoyer_fichier_csv.md)
* [Nettoyer un jeu de données : la fonction SI](./#fiche/Nettoyer_des_donnees_fonction_SI.md)
