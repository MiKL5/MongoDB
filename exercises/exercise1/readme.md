# **Importer des données** <a href="../../"> <img src="https://github.com/MiKL5/devWeb/raw/master/Assets/Images/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
en NoSQL, on utilise des fichiers de texte (JSON ou CSV) contenants des noms de champs et des valeurs.  
Un fichier JSON stock dans une structure hiérarchique.  
En NoSQL, tout est regroupé dans un fichier JSON ou CSV. Il n’y a pas de relation (jointure) entre les tables.  
Les infos sont stockées dans des documents intégrés à la base de données. 
## Via compass
Il faut d’abord créer une base de données.  
Collection name est le nom de la table. Puis `Import data`.  
Eventuellement, le type JSON ou CSV, choisir le fichier et valider.  
Compass dit le nombre d’importation. 
## Via Mongosh
Avec la commande `cd`, se positionner dans le répertoire ou MongoDB est installer.  
Choisir `mongoimport, la BDD, la collection, le format et le nom du fichier.
```zsh
mongoimport --db eloa --collection movies --jsonarray --file movies.json
``` 
Il n’import pas dans une BDD existante et dit le nombre de lignes importés.