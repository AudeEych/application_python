# Application Gares en Ile de France
Application sur les gares en Ile de France, utilisant le jeu de données disponible sur le site Ile de France Mobilités (consultation mars 2023): https://data.iledefrance-mobilites.fr/explore/dataset/emplacement-des-gares-idf-data-generalisee/table/

Réalisée dans le cadre du cours de Python de Maxime Challon, TNAH 2022-2023 avec les consignes suivantes :

Réaliser une application lisant, modifiant et écrivant dans une base de
données préremplie :

a. plusieurs pages de rendus de données demandées, par exemple: un
catalogue, un endpoint JSON, des cartes, des graphes, etc.

b. la page de catalogue et le endpoint JSON devront intégrer des filtres sur les
données. Faire de même pour les cartes et les graphes serait un plus.

c. notions appelées: tables HTML, SQL, une bibliothèque JS pour les cartes
et/ou les graphes.

## Installation : 
Télécharger/cloner le dossier de l'application sur votre ordinateur

* Se rendre dans la racine de l'application
* installer un environnement virtuel. Sur la console Linux: 
virtualenv env -p python3

* Activer l'environnement virtuel:
source env/bin/activate

* Installer les modules nécessaires au fonctionnement de l'application: 
pip install -r requirements.txt

* Créer la base de données en SQLite à partir du fichier .csv fourni. Se rendre dans le sous dossier donnees_pour_sqlite, et exécuter le code python de création de la base:
python gares_to_sqlite.py

* La base de données est maintenant créée dans le dossier ("gares.sqlite"). 

* Revenir à la racine de l'application, et créer un fichier .env: touch .env

* Editer ce fichier avec les informations suivantes:
DEBUG=True
SQLALCHEMY_DATABASE_URI:<spécifier le chemin vers la base de données SQLite créée à l'étape précédente>
GARES_PER_PAGE=20

## Auteurs : Thomas Chaineux, William Le Roux, Aude Eychenne

