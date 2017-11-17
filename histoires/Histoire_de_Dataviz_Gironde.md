---
author: Pascal Romain
image_url: http://adresse.data.gouv.fr/static/img/csv-grey.svg
link: https://github.com/infolab-cd33/datalunch/blob/fiches-markdow/export-csv-osm.md
title: Exporter les données d'open street map dans un fichier csv
published: true
---
# La visualisation interactive des données budgétaires du Département de la Gironde

## Contexte

Dans le cadre de la saison 4 open data du Département de la Gironde, la direction des finances a souhaité être accompagnée pour :
- élaborer le cahier des charges d'une visualisation interactive du budget départemental (et la réalisation de visualisations),
- réaliser la libération de données relatives aux budgets.

==> 4 ateliers collectifs organisés entre mars et juin 2016 + un RDV "politique" + un atelier technique

Public des ateliers collectifs : 
> - 6 agents de la DFI, dont la Directrice
> - 3 agents de la DSIN
> - 1 élu (Vice-président chargé de la Citoyenneté, relations avec les usagers, communication et accès numériques)
> - 2 accompagnateurs Coop'Alpha
> - 2 experts en web design et développement web 

A l'issue des 4 ateliers, des orientations d'angles de sujets relatifs au budget du Département et leur mode de traitement ont été construites et priorisées  :

1. la visualisation des dépenses publiques → « A quoi sert la dépense publique ? »,
2. les grands équilibres budgétaires du département expliqués en 3’ (vidéo type Motion Design ou animation)),
3. les recettes et le rôle de l’impôt (datavisualisation)
4. le rôle de la dette / l’enjeu de la capacité d’épargne / le niveau d’endettement soutenable (jeu interactif sous la forme d'un simulateur)Lors des ateliers, 4 orientations d'angles de sujets relatifs au budget du Département et leur mode de traitement ont été construites et priorisées  :

## Quelles données budgétaires ?

> - Un jeu de données agrégées présentant les données financières selon des « standards » et critères importants à suivre dans le cadre de la gestion financière du département (endettement, types d’impôts, les dépenses par « compétences », …). 

[données agrégées](https://github.com/infolab-cd33/datalunch/blob/master/img/dataviz_finances/projet%20dataviz%20pr%20Alfresco%20V1%20%20SPPB%20-1.ods)

> - Les mêmes données, brutes, présentées selon la norme M52. Celle-ci permet la comparaison entre des départements. Mises à disposition au format souhaité (fichier de type .csv, encodage utf-8) pour plusieurs exercices budgétaires (depuis 2009)

[données M52](https://github.com/infolab-cd33/datalunch/blob/master/img/dataviz_finances/CreditsRealisesFonctionCA2009-2013.ods)

> une entrée par fonction 
> une entrée par article

Afin de pallier à la difficulté de diffuser les méthodes d’agrégation des données, un travail sur les formules d’agrégation en partant des données normalisées M52 a été mené au cours de l'atelier technique.

Deux résultats importants à souligner :

- un résultat attendu : obtenir plus de 90 % des données agrégées par la direction des finances en partant des données normalisées M52
- un résultat inattendu et positif : simplification de certaines des requêtes effectuées dans les outils métiers de la direction des finances

## La visualisation des données

### État de l’art
La question de la visualisation de données a été abordée à travers :

> - Des modes de visualisations des données
![Raw](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/dataviz_finances/raw_1.png) 
http://app.raw.densitydesign.org/

> - Les travaux réalisés sur les données budgétaires du département dans le cadre d'un workshop Datavisualisation organisé par l'Ecole de Communication visuelle de Bordeaux (ECV) en 2013 et associant des étudiants graphistes, journalistes et des dévelopeurs.

![departement33-depense.png](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/dataviz_finances/departement33-depense.png)
![departement33-depense2.png](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/dataviz_finances/departement33-depense2.png)

> - Des travaux menés par des médias

http://www.journaldunet.com/business/budget-ville/rennes/ville-35238
https://www.information.dk/databloggen/2014/08/finansloven-2015-visualiseret 

> - Des exemples mis en place par d’autres collectivités

http://dataviz.rennesmetropole.fr/budget/
http://dataviz.rennesmetropole.fr/budget/budget-rennes-metropole-2016/

> - Des projets internationaux
http://app.wheredoesmymoneygo.org//bubbletree-map.html#/~/total


### Maquettage de la Data-visualisation des dépenses
- Ingrid Babu et David Bruant, respectivement web-designer et développeur.

> - Développement de la représentation visuelle

![david.png](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/dataviz_finances/david.png)

> - Maquette graphique d'une page d'accueil

![wireframeHome.png](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/dataviz_finances/wireframeHome.png)

> - Maquette graphique de la Data-visualisation
![synthese.png](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/dataviz_finances/synthese.png)

### Des attentes fortes identifiées
 
- comparabilité des données dans le temps et entre départements
- présentation des masses budgétaires rapportée à l'échelle humaine et à l'impact de l'action « sur le terrain » : 
ratios, % du budget de l'action dans le budget global des dépenses, part (%) des bénéficiaires de l'action, courbe d'évolution de la dépense, ce qu'elles recouvrent concrètement en termes d'action du Département sur le territoire girondin, etc.

![synthese-process-dataviz.png](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/dataviz_finances/synthese-process-dataviz.png)

### Quelques préconisations formulées

- Méthodologiques : cycle de travail itératif + un chef de projet désigné
- Technologiques : ouvertes et pérennes, documentées, qualité (accessibilité), utilisables par non informaticiens.
- Juridique : licence libre pour faciliter la réutilisation, l’amélioration, la reprise par d’autres directions ou d’autres collectivités


## Résultat : l'appel d'offre

"Fourniture et mise en oeuvre d'applications de visualisation et de manipulation des données budgétaires du Département de la Gironde" 

Publié le 13 octobre 2016
Remise des offres le 04 novembre

http://marches-publics.gironde.fr/avis/index.cfm?fuseaction=pub.affPublication&IDM=356800&refPub=MPI-pub-2016287044&serveur=MPI&IDS=377






