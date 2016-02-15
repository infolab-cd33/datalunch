# Vous avez dit BDD ?

- **Niveau** : **Débutant** / Intermédiaire / Avancé / Expert
- **Auteur** : Vincent Bergeot
- **Date de MàJ** : 06/01/2016
- **Licence** : CC-by-sa
- [Pour revenir au dépot](http://datalunch.datalocale.fr)

## Objectifs de cette présentation
Découvrir les bases de données :

- Définition
- Quelques abréviations
- Quelques ordres de grandeurs
- Contruire une base de données

## Définition
*Une base de données (en anglais : database) est un outil permettant de stocker et de retrouver l'intégralité de données brutes ou d'informations en rapport avec un thème ou une activité ; celles-ci peuvent être de natures différentes et plus ou moins reliées entre elles. Dans la très grande majorité des cas, ces informations sont très structurées, et la base est localisée dans un même lieu et sur un même support.*

https://fr.wikipedia.org/wiki/Base_de_donn%C3%A9es

## Différence entre tableur et base de données

Comment faire cette table ?

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/bdd/bdd-01.png)

#### Dans un tableur
je note les noms de colonnes, je remplis les données.

**Problème : j'écris trois fois Durand**

Alors que je pourrai n'écrire que cela :

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/bdd/bdd-02.png)

Mais dans ce cas, j'ai besoin de connaître la "relation" entre "Durand" d'une part et "Paul, Jacques, Louis"

#### Dans une base de données
Je vais créer 2 tables 

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/bdd/bdd-03.png)

et définir une relation entre elles 

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/bdd/bdd-04.png)

Pour obtenir à la fin une base de données avec plusieurs tables :

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/bdd/bdd-05.png)

Donc effectivement pour 3 enfants et leur père ce n'est pas forcément nécessaire mais si on fait cela pour tous les pères du monde !!!

Les images proviennent du site [http://www.3stone.be](http://www.3stone.be/access/articles.php?lng=fr&pg=221), sous licence CC-by-sa

#### Conclusion
Pour peu de données, un tableur est suffisant, facile à mettre en œuvre, utilisation relativement simple, permet de rapidement voir si les données sont *propres* (en triant, observant, ...)

Pour beaucoup de données, la base de données devient nécessaire. Plus performante sur des gros volume de données, plus adaptées pour faire des recherches et des vérifications de "propreté", la mise en œuvre demande une plus grande réflexion sur les tables de données et leurs relations.

## Quelques abréviations
- bdd -> Base de données
- sgbd -> Système de Gestion de Base de Données
 - l'ensemble des logiciels qui vont permettre d'exploiter la base de données
- ODbL -> Open Database License
 - licence permettant la réutilisation des données contenues dans la base -> fréquemment utilisée pour les données ouvertes.

## Quelques ordres de grandeurs
de quelques mégaoctets à plusieurs téraoctet

## Des données plus ou moins structurées


## Aller + loin : 
Quelques sources : 
- https://fr.wikipedia.org/wiki/Base_de_donn%C3%A9es
- https://fr.wikipedia.org/wiki/NoSQL
- https://fr.wikipedia.org/wiki/MongoDB


## A savoir : 

Dans une base de données "classique" dite relationnelles, la structure de départ est primordiale et souvent complexe à modifier par la suite.

Pour pallier à cela et permettre d'éviter cette structuration à-priori, on parle de plus en plus de base de données NoSQL (Not only SQL en anglais).

Pour obtenir cela :

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/bdd/bdd-06.png)

on va utiliser pour les données une forme comme ceci :

![](https://raw.githubusercontent.com/infolab-cd33/datalunch/master/img/bdd/bdd-08.png)

Images issues de [wikipédia](https://fr.wikipedia.org/wiki/MongoDB)
