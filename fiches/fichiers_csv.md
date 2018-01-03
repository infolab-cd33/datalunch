---
title: Produire un fichier CSV, bonnes pratiques
author: Suzanne Galy
licence: CC-By-SA
description: Créer ou interagir avec des fichiers au format csv.
image_url: https://www.datalocale.fr/base/images/logo-datalocale.jpg
link: https://github.com/infolab-cd33/datalunch/fichiers_csv.md
categorie: manipulation
niveau: débutant
date: 03/01/2016
---

## Principes - Ce que nous allons faire
Nous allons récupérer un fichier Excel ou Open/Libre Office et le transformer en fichier CSV pour permettre sa réutilisation aussi bien par les individus que par les machines.
Nous allons choisir :

- un délimiteur de caractère
- un encodage de caractères

## Ingrédients - Ce dont nous avons besoin

- Un tableur, en local ou en ligne
- Calc (Libre Office)
- Excel (MS Office)
- Google Sheets (Drive)

## Étapes - Comment allons-nous procéder ?

Pour ouvrir un fichier csv avec LibreOffice

Ouvrir LibreOffice Calc

Dans la rubrique Fichier choisir le menu ouvrir (ou ctrl+O ou pomme+O)

Une fenêtre permettant de définir les paramètres d'import de texte s'ouvre :

1. choisir un encodage de caractère : chaque fichier est produit dans un encodage.

Un jeu de caractères codés est un code qui associe un jeu de caractères abstraits d’un ou plusieurs systèmes d’écriture (comme des alphabets ou des syllabaires) utilisés pour transcrire des langues naturelles avec une représentation numérique pour chaque caractère de ce jeu, ce  nombre pouvant lui-même avoir des représentations numériques différentes. "Sur Internet, l'UTF-8 et l'ASCII sont les deux encodages les plus populaires depuis 2010.  En juillet 2012, leur utilisation est estimée à 80 %, (65 % + 15 %)  contre 10 % environ pour les encodages occidentaux (latin1).  L'utilisation des autres encodages est inférieure à 10 % sur internet." (source : wikipedia ). Dans le cas des fichiers produits par des sources françaises l'encodage est souvent le Latin1 ou l'UTF-8

2. choisir une option de séparateur.

Un fichier csv est un fichier texte dans lequel les données sont séparées par un délimiteur. Ce délimiteur est traditionnellement une virgule d'où le nom de ce format de fichier (Comma Separated Values : valeurs séparées par une virgule). Il faut ici sélectionner le délimiteur qui a été utilisé par le créateur du fichier. Vous avez le choix entre tabulation, virgule, point-virgule, espace ou autre. L'écran de pré-visualisation de Libre office présente la structuration du fichier en fonction du choix de délimiteur.

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/csv/calc_sep.png)

3. option séparateur de texte :
certaines valeurs peuvent contenir des virgules (5,6°C par exemple) Dans ce cas, si le délimiteur sélectionné est la virgule, lors de l'import du texte la valeur 5 et la valeur 6 vont être scindées en deux cellules.  Pour éviter cela il est possible de spécifier un séparateur de texte (par exemple "")

La fenêtre de prévisualisation affiche le rendu en fonction des options sélectionnées et vous permet de vous assurez que vous allez obtenir le résultat attendu

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/csv/calc_sepErreur.png)

Cliquez sur OK

le fichier est éditable dans calc.

Si vous souhaitez modifier l'encodage et/ou le délimiteur, vous pouvez enregistrer ce fichier dans le format natif de calc soit ods en cliquant sur fichier enregistrez sous, puis de répéter la même procédure en cliquant sur fichier enregistrer sous et en sélectionnant le format csv. La fenêtre d'enregistrement vous propose alors les options d'encodage et de délimiteur.

## Produire un fichier csv

Pour produire un fichier csv, nous allons utiliser un tableur numérique comme Calc de LibreOffice ou Excel de Microsoft (ou les suites bureautique en ligne comme Drive de Google ou autre)

la première étape consiste à créer une ligne pour le titre des colonnes. Le nommage des colonnes est important.
**Les noms des colonnes ne doivent comporter ni accents ni espaces et si possible ne pas dépasser une dizaine de caractères**. Il est également préconisé de ne pas utiliser les onglets ni de modifier la mise en page du tableur en faisant des fusions de cellules pour faciliter le traitement automatisé des données

La seconde étape consiste à rentrer les  valeurs dans les cellules. A chaque fois que vous devez entrer une valeur  il faut vous poser la question du tri. Un utilisateur va-t-il souhaiter  trier mes données suivant les valeurs disponibles dans cette colonne.  Lorsque la réponse est oui, il faut isolez les valeurs en question dans une colonne. par exemple pour une adresse, il vaut mieux séparer la  voie, le code postal et la ville dans 3 colonnes différentes pour  pouvoir ensuite facilement trier par le nombre code postal ou par la  ville alphabétique.

fichiers d'adresses : si vous souhaitez saisir des données de géolocalisation, il est préconisé de séparer ces données dans 2 colonnes portant les noms longitude et latitude car ces intitulés sont souvent recherchés automatiquement pour déterminer les coordonnées d'un lieu.

Une fois les données entrées vous pouvez cliquer sur enregistrer et choisir le format csv.

Vous pouvez ensuite importer ce fichier dans différents portails open data et consulter le résultat de la prévisualisation.

## Aller + loin :
Le format csv peut être utilisé pour décrire le contenu du fichier en utilisant la syntaxe.
Il  est notamment possible d'accompagner un fichier csv d'un fichier en json respectant une certaine syntaxe pour permettre de faciliter l'utilisation du fichier texte

[tabular data model](http://www.w3.org/TR/2015/WD-tabular-data-model-20150416/#simple-example)

## A savoir :
Le format csv est un format ouvert et libre. Il ne permet pas de stocker des formules ni leurs résultats comme Excel ou Calc mais il peut être lu aussi bien par un humain que par un ordinateur ce qui en fait un format d'interopérabilité.

## Liens avec d’autres fiches
