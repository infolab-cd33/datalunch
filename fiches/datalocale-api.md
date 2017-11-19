---
title: Présentation de l'API de datalocale
author: Pascal Romain
licence: CC-By-SA
description: Présenter le fonctionnement de l'interface programmatique de datalocale.
image_url: http://adresse.data.gouv.fr/static/img/csv-grey.svg
link: https://github.com/infolab-cd33/datalunch/datalocale-api.md
categorie: programmation
---

- **Niveau** : Avancé
- **Date de MàJ** : 03/11/2016

[Pour revenir au dépot](http://datalunch.datalocale.fr)

## Principes - Ce que nous allons faire
Apprendre à utiliser l'API de CKAN pour interagir avec le catalogue datalocale
## Ingrédients - Ce dont nous avons besoin
Un navigateur Internet ou quelques connaissances en programmation.
## Étapes - Comment allons-nous procéder ?
=========
API guide
=========

L'**Action API** de CKAN est une interface puissante, de type RPC qui expose l'ensemble des fonctionnalités principales de CKAN aux clients d'API qui souhaitent les consommer. Tout ce que l'on peut faire au travers de l'interface web peut être réalisé au moyens de codes extérieures qui interagissent avec l'API. Par exemple, en utilisant l'API CKAN vous pouvez :

* récupérer une liste formatée en JSON de tous les jeux de données de datalocale, de tous les thèmes ou d'autres objets disponibles :

  https://www.datalocale.fr/api/3/action/package_list

  https://www.datalocale.fr/api/3/action/group_list

  https://www.datalocale.fr/api/3/action/tag_list

* récupérer une représentation JSON complète d'un jeu de données, d'une ressource ou d'un autre type d'objet:

  https://www.datalocale.fr/api/3/action/package_show?id=budget-du-departement-de-la-gironde

  https://www.datalocale.fr/api/3/action/tag_show?id=budget

  https://www.datalocale.fr/api/3/action/group_show?id=finances

* rechercher des jeux de données ou des ressources correspondant à une requête:

  https://www.datalocale.fr/api/3/action/package_search?q=budget

  https://www.datalocale.fr/api/3/action/resource_search?query=name:budget

* Créer, mettre à jour et supprimer des jeux de données, distributions ou d'autres objets
* Récupérer le flux d'activité des jeux de données récemment modifié sur datalocale:

  https://www.datalocale.fr/api/3/action/recently_changed_packages_activity_list

---------------------
Faire une requête d'API
---------------------

Pour appeler l'API CKAN, il faut envoyer un dictionnaire JSONdans une requête POST HTTP vers une des URL de l'API CKAN. Les paramètres de la fonction de l'API devraient ête contenues dans le dictionnaire JSON. CKAN retournera alors sa réponse dans un dictionnaire JSON.

Un moyen d'envoyer un dictionnaire JSON vers une URL est d'utiliser le client HTTP en ligne de commande `HTTPie <http://httpie.org/>`_.  Par exemple, pour récupérer la liste de tous les jeux de données du thème environnement sur datalocale.fr, il faut au préalable installer le client HTTPie sur vote ordinateur et ensuite appeler la fonction d'API ``package_list`` en lançant cette commande dans un terminal ::

    http https://www.datalocale.fr/api/3/action/package_list&groups=environnement

La réponse de CKAN ressemblera à cela ::

    {
        "help": "...",
        "result": [
            "education_et_communication",
            "emploi_et_travail",
            "energie",
            "environnement",
            "geographie",
            "relations_internationales"
        ],
        "success": true
    }


La même requête http peut être réalisée en utilisant le module Python standard ``urllib2`` , avec ce code Python::

    #!/usr/bin/env python
    import urllib2
    import urllib
    import json
    import pprint

    # Use the json module to dump a dictionary to a string for posting.
    data_string = urllib.quote(json.dumps({'id': 'finances'}))

    # Make the HTTP request.
    response = urllib2.urlopen('https://www.datalocale.fr/api/3/action/group_list',
            data_string)
    assert response.code == 200

    # Use the json module to load CKAN's response into a dictionary.
    response_dict = json.loads(response.read())

    # Check the contents of the response.
    assert response_dict['success'] is True
    result = response_dict['result']
    pprint.pprint(result)

## Aller + loin :

La liste des fonctions et méthodes de l'[API CKAN](docs.ckan.org/en/latest/api/index.html#action-api-reference)

[Quelques exemples de requête](http://docs.ckan.org/en/latest/api/index.html#api-examples)

## A savoir :

La définition d'une API [source:wikipedia](https://fr.wikipedia.org/wiki/Interface_de_programmation)

Le format de données JSON [source:wikipedia](https://fr.wikipedia.org/wiki/JavaScript_Object_Notation)
