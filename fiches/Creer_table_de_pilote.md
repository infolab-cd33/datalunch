---
title: Créer une table de pilote (ou tableau croisé)
author: Suzanne Galy
licence: CC-By-SA
description: Automatiser le croisement des données avec une table de pilote dans un tableur numérique (calc, excel).
image_url: https://github.com/infolab-cd33/datalunch/raw/master/img/csv/file_formats_4_csv-512.png
categorie: manipulation
niveau: intermédiaire
date: 01/11/2016
---

## Principes - Ce que nous allons faire
- Télécharger un fichier de données au format CSV
- Ouvrir le fichier à l'aide d'un logiciel tableur [voir la fiche](./#fiches/fichiers_csv.md)
- Automatiser le croisement des données avec une table de pilote

## Ingrédients - Ce dont nous avons besoin

- Un outil tableur : [LibreOffice Calc](https://fr.libreoffice.org/download/libreoffice-stable/),
Tableur issu de la suite bureautique open source Libre Office, il interprète le format CSV pour présenter les données en lignes et colonnes sans autre intervention complémentaire de la part de l'utilisateur.
- Un fichier de données au format CSV : "Citoyenneté-Etat civil : Naissances domiciliées de Poitiers" (https://www.data.gouv.fr/fr/datasets/citoyennete-etat-civil-naissances-domiciliees-de-poitiers/)

Nombre de naissances concernant les résidents de Poitiers selon les quartiers IRIS de Poitiers. La répartition géographique est faite selon le lieu de résidence de la Mére au moment de la naissance. Source Ville de Poitiers -Administration générale


## Étapes - Comment allons-nous procéder ?

### Télécharger et ouvrir le fichier de données

- Ouvrir LibreOffice Calc
Dans la rubrique Fichier choisir le menu ouvrir (ou ctrl+O ou pomme+O)
Une fenêtre permettant de définir les paramètres d'import de texte s'ouvre :

![fenêtre de paramétrage](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/csv/ouvrir-csv.png)

1. choisir un encodage de caractère : chaque fichier est produit dans un encodage.==> ici, unicode UTF-8
2. choisir une option de séparateur. ===> ici, virgule
Un fichier csv est un fichier texte dans lequel les données sont séparées par un délimiteur. Ce délimiteur est traditionnellement une virgule
3. option séparateur de texte ==> ici, "

Certaines valeurs peuvent contenir des virgules (5,6°C par exemple) Dans ce cas, si le délimiteur sélectionné est la virgule, lors de l'import du texte la valeur 5 et la valeur 6 vont être scindées en deux cellules.  Pour éviter cela il est possible de spécifier un séparateur de texte (par exemple "")

Cliquez sur OK

Une fois ouvert, il est recommandé d'enregistrer une copie de ce fichier en le renommant (copie) afin de ne pas modifier le fichier source.

### Générer une "table de pilote" (ou tableau croisé dynamique)

Une table de pilote va permettre de
* automatiser des croisements et traitement statistiques des données
* repérer rapidement des erreurs dans les cellules du fichier
* débuter l'analyse des données du fichier
* répondre facilement et rapidement à des questions

#Combien de naissances par quartier et par an ?

Pour créer la table de pilote :
* sélectionner l'ensemble des données de la feuille où apparaissent les données à traiter (ctrl A)
* cliquer dans le menu "Insertion" puis "table de pilote", puis "OK" pour la proposition par défaut "Sélection active"
* Choix des critères pour la création de la table (glisser-déposer les intitulés de colonnes dans les blocs correspondants) :
    * champs de la page : rien
    * champs de ligne : GRAND QUARTIER
    * champs de données : 2005, 2006, 2007, 2008, etc.

NB : par défaut, la table de pilote propose d'activer la fonction "sum" pour calculer la somme des naissances par année dans le bloc "champs de ligne". Il est possible de modifier cette fonction par un double clic sur le texte "sum-2005", puis en choisissant la fonction souhaitée (nombre, moyenne, écart type, etc.) parmi les propositions de la liste.

RQ 1 : on modifie les critères de la table à l’aide de la fonction “éditer la mise en page” (par clic droit dans le tableau).
RQ2 : si la feuille source est modifiée, on peut actualiser la table de pilote à l'aide de la fonction "actualiser" (par clic droit dans le tableau).

#Combien de naissances par quartier sur la période 2005-2014 ?
En l'état, les données du tableur ne permettent pas d'obtenir cette information par une table de pilote : il faudrait pouvoir croiser la colonne GRAND QUARTIER avec une colonne listant le total des naissances sur la période.

Cette colonne n'existant pas, il faut donc la créer :
* Attribuer un nom explicite en en-tête de la colonne M (par exemple "total période")
* Dans la cellule M2, activer la fonction Somme.

Plusieurs possibilités pour cela :

* dans la cellule, rédige la formule suivante : =SOMME(C2:L2), puis faire Entrer
* cliquer sur la cellule M2, puis saisissez la formule dans la ligne de saisie (barre de saisie blanche située juste au dessus du tableau), puis faire Entrer
* cliquer sur le bouton "assistant de fonctions" et sélectionner la liste la fonction SOMME puis écrire la formule après le signe =, puis faire Entrer
* cliquer sur le bouton du symbole ∑ (somme automatique) qui sélectionnera par défaut des valeurs à additionner, puis faire Entrer.

Une nouvelle valeur s'affiche désormais dans la cellule M2.

Il est possible d'appliquer la formule/fonction somme automatiquement à l'ensemble des lignes de la colonne M en positionnant le curseur de la souris sur le coin de la cellule M2 (une petite croix apparaît) :

* cliquer sur la croix et, sans relâcher le clic, l'étirer jusqu'au bas de la colonne
* double cliquer sur la croix (cela aura pour effet d'appliquer la fonction jusqu'au bas de la colonne)

Le tableur comporte désormais une colonne du total des naissances sur la période 2005-2014 (par ligne).

Pour créer la table de pilote du total des naissances par quartier sur la période :
* sélectionner l'ensemble des données de la feuille où apparaissent les données à traiter (ctrl A)
* cliquer dans le menu "Insertion" puis "table de pilote", puis "OK" pour la proposition par défaut "Sélection active"
* Choix des critères :
    * champs de la page : rien
    * champs de ligne : GRAND QUARTIER
    * champs de données : total période

## Pour aller plus loin :

* [Aide de Libre Office Calc](https://help.libreoffice.org/Calc/Welcome_to_the_Calc_Help/fr)
* [Apprendre à créer un tableau croisé dynamique avec LibreOffice Calc ](http://malick-nseck.developpez.com/tutoriels/apprendre-a-creer-tableau-croise-dynamique-avec-libre-office-calc/)

## A savoir :

Le fichier csv encodé en UTF-8, avec pour séparateur la virgule ou le point virgule, est communément trouvé sur les portails opendata.

## Liens avec d’autres fiches :

* [Ouvrir et nettoyer un fichier CSV](./#fiche/ouvrir_et_nettoyer_fichier_csv.md)
* [Créer un fichier csv](./#fiches/fichiers_csv.md)
