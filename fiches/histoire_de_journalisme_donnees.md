---
author: Suzanne Galy
description: Un module pédagogique de découverte et d'initiation au journalisme de données par Institut de journalisme de Bordeaux Aquitaine
image_url: https://www.datalocale.fr/base/images/logo-datalocale.jpg
title: Des enquêtes journalistiques nourries par les données
licence: CC-by-sa
categorie: datavisualisation
niveau: débutant
date: 12/05/2016
---

# Des enquêtes journalistiques nourries par les données
## Le Data Journalisme Lab de l'IJBA

Un module pédagogique de découverte et d'initiation au journalisme de données : http://datajournalismelab.fr/
par Institut de journalisme de Bordeaux Aquitaine

- Public : 37 étudiants en Master 1
- Durée : une journée de lancement + une journée de conférence de rédaction intermédiaire + neuf journées de production des enquêtes à l'IJBA (data + terrain)
- Objectif : réaliser des enquêtes nourries par les données sur des sujets locaux (Bordeaux et sa région)
- Final : debriefing collectif des enquêtes (Pitch) et mise en ligne

![debriefing collectif.jpg](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/datajournalismlab/debriefing_collectif.jpg)

## De 2012 à 2016

- Année 1 : production d'applications interactives
- Un dispositif pionnier en France
- 50 étudiants : journalistes IJBA + graphistes ECV + étudiants développeurs Epitech
- Depuis 2013 : production "autonome" de visualisations simples
![debriefing] (http://datajournalismelab.fr/wp-content/uploads/Presentation-des-prods-2-DJL-2016-1024x768.jpg)

### La Gironde sportive (2012)

http://www.2012.datajournalismelab.fr/wp-content/uploads/equipementsportifs/index.html

Projet :
> - Etablir une comparaison entre les équipements sportifs mis à disposition des pratiquants et leur nombre officiel (licenciés dans une fédération des sports concernés).

Données utilisées :
- Liste des établissements sportifs du département : http://catalogue.datalocale.fr/dataset/liste-equipements_sportifs-cg33
- Données produites par les étudiants : nombre de licenciés par sport

Traitement :
- Calcul statistique et classement des résultats

### Vit-on vraiment mieux en Gironde qu'en France ? (2012)

http://www.2012.datajournalismelab.fr/wp-content/uploads/visagesocialgironde/index.html

Projet :
> - Représenter le visage social de la Gironde, sa situation au niveau national et son évolution sur une période suffisamment significative pour pouvoir en tirer des conclusions.

Données utilisées :
- Profil développement durable de la Gironde : http://catalogue.datalocale.fr/dataset/indicesdd-agenda21-cg33 (période 2000-2008). Ces données permettent d’établir l’Indice de Situation Sociale Départementale (ou ISSD) : santé, logement, éducation et emploi, aide sociale
- Données Insee

Traitement :
- Choix d'indicateurs tels que le taux de chômage, la part des salariés en emploi précaire, le nombre de bénéficiaires des minimas sociaux,…
- Traitement statistique
- Mise en perspective (comparaison) avec les moyennes nationales

## Déroulement pédagogique en 2016

L'équipe d'intervenants :
http://datajournalismelab.fr/les-acteurs/

Accompagnement éditorial (recherche sources, analyse, problématisation / angle, enquête terrain) + technique (traitement des données, mise en forme)

Constats préliminaires :
Très peu d'étudiants sont issus de formation en mathématique, statistique ou informatique.
- « Culture des données » des étudiants très approximative
- Connaissance souvent faible des outils de tableur, des méthodes ou outils de visualisation des données

Déroulé pédagogique :
- Amorçage : culture des données + open data + data journalisme (histoire, méthodes, outils)
- Mise à disposition de jeux de données "sources" sur le thème de « l’espace public » : 12 groupes constitués
- Problématisation/angle, analyse des données, pré-enquête (documentation, revue de presse, pré-entretiens)
- Session de production

![Production2] (https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/datajournalismlab/production2.jpg)
![Production 1](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/datajournalismlab/production1.jpg)

Ecueils rencontrés :
- Perte de temps : recherche des sources, analyse des données et documentation sujet
- Précipitation : des données jugées pertinentes mais sans analyse de leur contenu réel (le sujet tombe à l'eau)
- Décrochage : le data journalisme, une discipline de "geek"

Enseignements :
- Le data journalisme : un registre éditorial spécifique qui fait appel à toutes les compétences du journalisme et exige de la rigueur.
- Progression des étudiants : connaissance des sources d’information, approche critique de ces sources, domaines de compétence des collectivités et organismes pourvoyeurs de données, travail sur les chiffres et les statistiques, notion d’angle, adéquation angle/sources, vérification information, techniques d’enquête et d’interview, écriture informative.

### Les outils du Lab

Extraction et traitement des données :
- Tabula : extraire les données d’un PDF pour construire un tableur
- Google Spreadsheet : outil tableur de Google
- Google Fusion Table
- Open Refine
- Import.io
- M. Data Converter

Edition de graphiques :
- Datawrapper
- Highcharts Cloud
- Google Charts
- Infogram
- Chartbuilder
- Raw
- Tableau Public

Visualisations de données géographiques :
- Umap, CartoDB et Mapbox
- StoryMaps
- Color Brewer
- Map Shaper
- Maps Engine (Google)
- HighMaps

Autres :
- TimelineJS
- TimelineVertical
- Juxtapose
- Odyssey
- DocumentCloud


### Exemples d'enquêtes

## Utilisation de données géographiques

#### Saisonniers : les précaires de la vigne (2013)

Projet :
> - Explorer un gisement de données en espérant y trouver des informations inédites et intéressantes.

http://www.2013.datajournalismelab.fr/saisonniers-les-precaires-de-la-vigne/

Données utilisées :
- comptage des bénéficiaires du RSA en Gironde par canton par commune et par an 2009, 2010 et 2011 : http://catalogue.datalocale.fr/dataset/liste-benef-rsa
- coordonnées géographiques des cantons de Gironde
- le recensement des habitants de chaque canton (Insee)
- recensement agricole 2010 et 2011 (Insee/data.gouv.fr)

Traitement :
- Recherche des données de coordonnées géographiques des cantons de Gironde, fusion avec base de données demandeurs RSA, géolocalisation de la base de données et cartographie Google des données brutes (Google Refine et Google Fusion Table)"
- Traitement statistique : pourcentage de demandeurs du RSA par rapport à la population des 20-64 ans dans chaque canton, cartographie Google (Google Fusion Table)
- Fusion en un seul fichier des coordonnées géographiques des communes girondines avec les données détaillant leur nombre d’exploitations viticoles respectives (Google Refine et Google Fusion Table)
- Superposition de la carte des communes viticoles avec la carte des concentrations de demandeurs du RSA par canton

## Utilisation d'un volume important de données

#### Les motards, fous du guidon ? (2016)

http://datajournalismelab.fr/les-motards-fous-du-guidon/

Données utilisées :
- Base de données accidents corporels de la circulation (data.gouv.fr)
https://www.data.gouv.fr/fr/datasets/base-de-donnees-accidents-corporels-de-la-circulation/

Quatre fichiers (véhicules, caractéristiques, lieux, usagers) * 130 000 lignes * dix colonnes

Projet :
> - Idée 1 : l'accidentologie des piétons à Bordeaux // aucune tendance dégagée (profils victimes, lieux, horaires, etc.) + trop faible échantillon "mortalité" pour une analyse pertinente.
> - Idée 2 : exploration en détail la base de données pour repérer des tendances // mortalité des deux roues motorisés plus importante en Gironde.

Un sujet "Etat des lieux" : les circonstances des différents accidents, notamment la temporalité (l’heure, le jour, le mois), les conditions météorologiques, l’état des chaussées, l’âge moyen des conducteurs, etc.

Traitement :
- Croisement des différents fichiers 2014 et 2015 avec Excel : de façon manuelle puis tableaux croisés, formule « RechercheV », formule « nb.si », etc.
- Analyse et choix de critères : cyclomoteurs de moins de 50cm3, scooters de moins de 50 cm3, motocyclettes comprises entre 50 cm3 et 125 cm3, scooters compris entre 50cm3 et 125cm3 et supérieurs à 125 cm3, les motocyclettes supérieures à 125 cm3.
- Graphiques et heatmap avec Highcharts, infographie avec Picktochart et cartographie avec Google My Maps

## Données non ouvertes / données produites

#### Pas trop de bio dans les vins de Bordeaux (2015)

http://www.2015.datajournalismelab.fr/pas-trop-de-bio-dans-les-vins-de-bordeaux/

Projet :
> - Savoir si le vin bio de Bordeaux est un marché de niche, constater quelles appellations étaient plus vertes que les autres et récolter des données de géolocalisation pour voir où se trouvait la majorité des exploitations bio. Puis, comparer ces surfaces viticoles bio avec celles des grandes régions viticoles de France.

Données utilisées :
Agence-bio, Arbio, Bio Gironde, CIVB, Syndicat des vignerons bio de Gironde : personne n’a accepté de communiquer de bases de données.

- chiffres de 2011 à 2014 des surfaces bio et de surfaces en conversion bio par région disponible sur le site de l’agence bio
- chiffres sur l’ensemble des surfaces viticoles disponibles sur le site du ministère de l’Agriculture
- liste des exploitants bio de Gironde avec le nom de l’exploitant, les données géographiques et la date d’entrée dans le bio : données scrappées par la doctorante Frédérique Célérier depuis un annuaire institutionnel.

Traitement :
- Calcul du taux d'évolution des surface bio 1995 - 2013
- Géolocalisation des surfaces bio de Gironde
- Calcul du pourcentage de bio sur le total des exploitants
- Cartographie chronologique de l'évolution des surfaces bio avec CartoDB, superposition dans l'image de la carte des AOC avec Google Earth, diagrammes avec Datawrapper, graphique et chiffres clés avec Infogr.am
