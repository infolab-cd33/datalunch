# Nettoyer un jeu de données : la fonction « SI »

- **Niveau** : Débutant / **Intermédiaire** / Avancé / Expert
- **Auteur** : Suzanne Galy
- **Date de MàJ** : 31/05/2016
- **Licence** : CC-by-sa
- [Pour revenir au dépot](http://datalunch.datalocale.fr)

## Principes - Ce que nous allons faire
- Télécharger un fichier de données au format CSV
- Donner instruction au tableur d'opérer un « test logique » (la fonction SI) afin, ici, de copier des informations de colonnes distinctes dans une seule et même colonne

La fonction SI indique un test logique à effectuer

Syntaxe : SI (test;alors_valeurs;sinon_valeurs)
test représente toute valeur ou expression pouvant renvoyer VRAI ou FAUX.
alors_valeur (facultatif) est la valeur qui est renvoyée si le test logique est VRAI.
sinon_valeur (facultatif) est la valeur qui est renvoyée si le test logique est FAUX.
(Source : https://help.libreoffice.org/Calc/)

## Ingrédients - Ce dont nous avons besoin

- un outil tableur : [LibreOffice Calc](https://fr.libreoffice.org/download/libreoffice-stable/),
    - Tableur issu de la suite bureautique open source Libre Office, il interprète le format CSV pour présenter les données en lignes et colonnes sans autre intervention complémentaire de la part de l'utilisateur.
- un fichier de données : BDD_passeports_modifie.ods
[registre de l'année 1800 des Passeports délivrés par le Port de Bordeaux aux Girondins, source Archives départementales)

## Étapes - Comment allons-nous procéder ?
### Télécharger, ouvrir et « enregistrer sous » le fichier 
- télécharger le fichier BDD_passeports_modifie.ods sur le bureau de l'ordinateur ou dans un dossier
- clic droit sur le fichier : "ouvrir avec" LibreOffice Calc et « enregistrer sous » pour en faire une copie

### Mettre en œuvre la fonction SI (simple)
Dans mon tableur, je dispose de plusieurs colonnes indiquant des lieux de départs, idem pour les arrivées : 
- Lieux de départ : ville d'origine ancien, île d'origine ancien, département d'origine ancien, ville d'origine aujourd'hui, île d'origine aujourd'hui, département d'origine aujourd'hui
- Lieux d'arrivée : idem.

Pour générer une localisation, je vais devoir récupérer toutes ces informations pour ne disposer que d'une seule colonne «  Lieu d'origine » (U), que je créée.
⇒ entrer dans la première cellule de la colonne U, la formule Calc suivante : =SI(Q2<>"";Q2;M2)

Instruction donnée : SI la cellule de la colonne « ville origine aujourd'hui » (Q) est différente de "vide", reporter la cellule de la colonne Q. Sinon, reporter la cellule de la colonne « ville d'origine ancien » (M).

![Exemple « fonction SI » imbriquée fichier Passeports 1800 Gironde](URL image)

### Fonctions SI imbriquées
Les fonctions SI imbriquées, c’est-à-dire une fonction SI au sein d’une autre, vous permettent de tester plusieurs critères et augmentent le nombre de résultats possibles. 
Dans notre tableur, il y a plusieurs colonnes disposant des informations utiles à récupérer : ville d'origine ancien (M), île d'origine ancien (N), ville d'origine aujourd'hui (Q), île d'origine aujourd'hui (R). 
La complexité du report d'informations vient aussi des nombreuses cellules vides présentes dans ces colonnes. 
Je dois donc imbriquer plusieurs hypothèses de report d'informations pour compléter ma colonne U « Lieu d'origine ».

⇒ entrer dans la première ligne de la colonne U, la formule Calc suivante : =SI(Q2<>"";Q2;SI(M2<>"";M2;SI(N2<>"";N2;SI(R2<>"";R2;"Non renseigné"))))

Instruction donnée : SI la cellule de la colonne « ville aujourd'hui » (Q) est différente de "vide", reporter la cellule de la colonne Q ; Sinon, SI la cellule de la colonne « ville d'origine ancien » (M) n'est pas vide, reportez M. Sinon SI la colonne « île ancien » (N) n'est pas vide, reporter N. Sinon, SI la colonne « île origine aujourd'hui » (S) n'est pas vide, reporter S ; sinon inscrire la mention « Non renseigné ». 

J'applique la formule à l'ensemble de la colonne U.
Résultat : toutes mes cellules contiennent désormais une indication de lieu d'origine (ville ou nom d'île) actuel.

## Pour aller plus loin : 
- [Aide de Libre Office Calc sur les fonctions de test logique](https://help.libreoffice.org/Calc/Logical_Functions/fr )

## Liens avec d’autres fiches : 
-ouvrir_et_nettoyer_fichier_csv.md  https://github.com/infolab-cd33/datalunch/blob/master/ouvrir_et_nettoyer_fichier_csv.md
