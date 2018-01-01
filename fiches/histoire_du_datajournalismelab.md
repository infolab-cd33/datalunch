---
title: Des enquêtes journalistiques nourries par les données du Département
author: Vincent Bergeot
licence: CC-By-SA
description: Présentation des différents sessions de datajournaliseme de l'IJBA.
image_url: https://www.datalocale.fr/base/images/logo-datalocale.jpg
link: https://github.com/infolab-cd33/datalunch/histoire_du_datajournalismelab.md
categorie: culture
niveau: débutant
date: 03/11/2016
---
##Le Data Journalisme Lab de l'IJBA depuis 2012

Public : 36 étudiants de première année de master de l’IJBA

![debriefing collectif.jpg](./img/datajournalismlab/debriefing_collectif.jpg)

Année 1 : étudiants graphistes ECV et étudiants développeurs Epitech

Durée : deux journées de mise en route, deux semaines de production à l'IJBA (data + terrain) et quelques conférences de rédaction intermédiaires.

![Production 1](./img/datajournalismlab/production1.jpg)

Final : debriefing collectif des enquêtes et mise en ligne sur [datajournalismelab](http://www.datajournalismelab.fr)

## Les données du Département mises en scène

### Vit-on vraiment mieux en Gironde qu'en France ? (2012)

Projet : représenter le visage social de la Gironde, sa situation au niveau national et son évolution sur une période suffisamment significative pour pouvoir en tirer des conclusions.

[la dataviz en ligne](http://www.2012.datajournalismelab.fr/wp-content/uploads/visagesocialgironde/index.html)

Données utilisées :
- [Profil développement durable de la Gironde](https://www.datalocale.fr/dataset/profil-developpement-durable-de-la-gironde) (période 2000-2008)
Ces données permettent d’établir  l’Indice de Situation Sociale Départementale (ou ISSD) : santé, logement, éduction et emploi, aide sociale
- Données Insee

**Traitement :**
Choix d'indicateurs tels que le taux de chômage, la part des salariés en emploi précaire, le nombre de bénéficiaires des minimas sociaux,…
Traitement statistique
Mise en perspective (comparaison) avec les moyennes nationales

### La Gironde sportive (2012)

Projet : établir une comparaison entre les équipements sportifs mis à disposition des pratiquants et leur nombre officiel (licenciés dans une fédération des sports concernés).
[dataviz en ligne](http://www.2012.datajournalismelab.fr/wp-content/uploads/equipementsportifs/index.html)

Données utilisées :
- [Liste des établissements sportifs du département](https://www.datalocale.fr/dataset/liste-des-equipements-sportifs-du-departement)
- Données produites par les étudiants : nombre de licenciés par sport

**Traitement :**
Classement des résultats

### Saisonniers : les précaires de la vigne (2013)

Projet : explorer un gisement de données en espérant y trouver des informations inédites et intéressantes. Ici : la base de données du nombre de demandeurs du RSA répartis par canton, en Gironde, pour les années 2009, 2010 et 2011.
[dataviz en ligne](http://www.2013.datajournalismelab.fr/saisonniers-les-precaires-de-la-vigne/)

Données utilisées :
- [comptage des bénéficiaires du RSA par canton par commune et par an (conforme règles IRIS)](https://www.datalocale.fr/dataset/comptage-des-beneficiaires-du-rsa-par-canton-par-commune-et-par-an-conforme-regles-iris)
- Coordonnées géographiques des cantons de Gironde
- le recensement des habitants de chaque canton (Insee)
- Recensement agricole 2010 et 2011 (Insee/data.gouv.fr)

**Traitement :**
- recherche des données de coordonnées géographiques des cantons de Gironde, fusion avec base de données demandeurs RSA, géolocalisation de la base de données et cartographie Google des données brutes (Google Refine et Google Fusion Table)"
- Traitement statistique : pourcentage de demandeurs du RSA par rapport à la population des 20-64 ans dans chaque canton, cartographie Google (Google Fusion Table)
- Fusion en un seul fichier des coordonnées géographiques des communes girondines avec les données détaillant leur nombre d’exploitations viticoles respectives (Google Refine et Google Fusion Table)
- Superposition de la carte des communes viticoles avec la carte des concentrations de demandeurs du RSA par canton

### La Gironde prend un coup de vieux (2013)

Projet : De plus en plus de personnes âgées dépendantes en Gironde. Mais moins de places en maisons de retraite. Le maintien à domicile est-il la panacée ? Enquête.
[dataviz en ligne](http://www.2013.datajournalismelab.fr/la-gironde-prend-un-coup-de-vieux/)

Données utilisées :
- [Nombre de bénéficiaires de l'allocation personnalisée d'autonomie](https://www.datalocale.fr/dataset/nombre-de-beneficiaires-de-lallocation-personnalisee-dautonomie)
- INSEE

**Traitement :**
- Traitement statistique
- Visualisations avec Infogr.am
