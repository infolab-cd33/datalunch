# Ouvrir et nettoyer un fichier de données au format CSV

## Principes
- Télécharger un fichier de données au format CSV
- Ouvrir le fichier à l'aide d'un logiciel tableur
- Repérer des erreurs et automatiser le croisement des données avec une table de pilote
- Nettoyer les données à l'aide des fonctions de tri, filtre, rechercher&remplacer 

## Ingrédients

- un outil tableur : [LibreOffice Calc](https://fr.libreoffice.org/download/libreoffice-stable/),
    - Tableur issu de la suite bureautique open source Libre Office, il interprète le format CSV pour présenter les données en lignes et colonnes sans autre intervention complémentaire de la part de l'utilisateur.
- un fichier de données au format CSV : 20164_SIP_liste-sites / 
[Liste des bâtiments du Conseil général](http://catalogue.datalocale.fr/dataset/46ce3441-bfd5-4bb1-aaca-14c3e910a9d0)
    - Liste des sites gérés par le conseil général sur lesquels se trouvent les différents bâtiments du conseil général accueillant des agents administratifs ou du public.

##Étapes
#Télécharger et ouvrir le fichier 

- télécharger le fichier CSV sur le bureau de l'ordinateur ou dans un dossier
- clic droit sur le fichier : "ouvrir avec" LibreOffice Calc
- une fois ouvert, il est recommandé d'enregistrer une copie de ce fichier en le renommant par exemple 20164_SIP_liste-sites_copie afin de ne pas modifier le fichier source.

Premier niveau d'analyse du fichier à vue d'oeil : 
- 573 sites sont recensés (il y a 574 lignes au total)
- il contient de nombreuses erreurs (adresses, code postal, décalages colonnes, etc.)

#Générer une "table de pilote" (ou tableau croisé dynamique)
Une table de pilote va permettre de 
- repérer rapidement des erreurs dans les cellules du fichier 
- répondre facilement et rapidement à des questions en opérant des croisements et traitement statistiques des données

Exemple 1 : 
- Sous quels statuts sont recensés les bâtiments du Département (colonne L "statut") ?
- Quel est le nombre de bâtiments par typologie de statut ?

Pour créer la table de pilote :

- sélectionner l'ensemble des données de la feuille où apparaissent les données à traiter (ctrl A)
- cliquer dans le menu "Données" puis "table de pilote" puis "créer", puis "OK" pour la proposition par défaut "Sélection active"
- Choix des critères pour la création de la table : 
    - champs de la page : rien
    - champs de ligne : statut
    - champs de données : site ==> double clic sur "site" pour faire apparaître les options de fonction et choisir “nombre” afin d'obtenir le calcul du nombre de sites par type de statut

>RQ 1 : on modifie les critères de la table à l’aide de la fonction “éditer la mise en page” (par clic droit dans le tableau).
>RQ 2 : seuls 570 sites apparaissent dans le décompte “Total Résultat” : il est facile de retrouver où se situent les erreurs du tableur source. Ici, dans la colonne “statut”, on trouve des dates à la place d’un statut.

#Nettoyer les données
Trois fonctions simples permettent de corriger des erreurs dans un fichier de données : 
- Fonction de "Filtre"
rubrique Données, choisir "filtre", puis "autofiltre" : une flèche apparaît dans l'en tête de colonne qui permet de visualiser les intitulés (textes) ou valeurs (chiffres, nombre) présents dans la colonne. 
Ici, sélection des "dates" repérées comme étant des erreurs (décalage de cellules dans les colonnes adresses 2, code postal) puis nettoyage manuel des lignes par copier-coller des cellules.

- Fonction "Tri"
rubrique Données, puis "trier" : une fenêtre "trier la plage" apparaît, choisir "étendre la sélection" de manière à ce que le tri s'opère sur l'ensemble des colonnes du tableur. 
Choisir selon les critères un tri croissant ou décroissant. Les données sont regroupées selon ce critère.

- Fonction "rechercher&remplacer" 
Elle permet de supprimer dans une colonne sélectionnée un élément indésiré, par exemple une parenthèse ouverte '(' ou un "0" au début d'une suite de chiffres.
 
- Sélection de la colonne
rubrique Edition, rechercher&remplacer : une fenêtre apparaît
indiquer l'élément "(" à "rechercher", puis laisser vide l'emplacement "rechercher par" 
Cliquer sur "tout remplacer" (puis décocher "cellulles entières" s'il s'agit uniquement d'une partie de la cellule) pour que la parenthèse soit supprimée dans toutes les cellules de la colonne. 
valider en cliquant sur "fermer"


#Pour aller plus loin : 

- [Aide de Libre Office Calc](https://help.libreoffice.org/Calc/Welcome_to_the_Calc_Help/fr)
- [Apprendre à créer un tableau croisé dynamique avec LibreOffice Calc ](http://malick-nseck.developpez.com/tutoriels/apprendre-a-creer-tableau-croise-dynamique-avec-libre-office-calc/)
