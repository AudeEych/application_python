# Application Gares IDF
Application sur les gares en Ile de France, pour le cours de Python de Maxime Challon, TNAH 2022-2023
_(juste en dessous des badges sympatiques à placer)_
L'application utilise le jeu de données disponible sur le site Ile de France Mobilités (consultation mars 2023):
https://data.iledefrance-mobilites.fr/explore/dataset/emplacement-des-gares-idf-data-generalisee/table/
[![forthebadge](http://forthebadge.com/images/badges/built-with-love.svg)]

Réaliser une application lisant, modifiant et écrivant dans une base de
données préremplie (possibilité d’utiliser les données utilisées dans l’UE3)
a. plusieurs pages de rendus de données seront demandées, par exemple: un
catalogue, un endpoint JSON, des cartes, des graphes, etc.
b. la page de catalogue et le endpoint JSON devront intégrer des filtres sur les
données. Faire de même pour les cartes et les graphes serait un plus.
c. notions appelées: tables HTML, SQL, une bibliothèque JS pour les cartes
et/ou les graphes.

## Installation : 
Télécharger/cloner le dossier de l'application sur votre ordinateur

Se rendre dans la racine de l'application
installer un environnement virtuel. Sur la console Linux: 
virtualenv env -p python3

Activer l'environnement virtuel:
source env/bin/activate

Installer les modules nécessaires au fonctionnement de l'application: 
pip install -r requirements.txt

Ensuite, créer la base de données en SQLite à partir du fichier .csv fourni. Se rendre dans le sous dossier donnees_pour_sqlite, et exécuter le code python de création de la base:
python gares_to_sqlite.py

La base de données est maintenant créée dans le dossier ("gares.sqlite"). 

Ensuite, revenir à la racine de l'application, et créer un fichier .env. 
touch .env

Editer ce fichier avec les informations suivantes:
DEBUG=True
SQLALCHEMY_DATABASE_URI:<spécifier le chemin vers la base de données SQLite créée à l'étape précédente>
GARES_PER_PAGE=20

## Auteurs : Thomas Chaineux, William LeRoux, Aude Eychenne

