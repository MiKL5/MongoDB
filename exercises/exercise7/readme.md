# **Supprimer une collection** <a href="../../"> <img src="https://github.com/MiKL5/BI/blob/master/assets/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
En utilisant la console JavaScript “Mongosh”, il n’y a pas de message prévenant que la bdd sera supprimer.
```json
db.voiture.drop(); -- true
```
Via MongoDB Compass  
Cliquer sur les ’`...`’ à droite du nom de la collection, ’`drop collection`’, entrer le nom de la collection, puis ’`drop collection`’.
# Supprimer la base de données
```json
db.dropdatabase();
```
Depuis MongoDB Compass  
Cliquer sur la corbeille, entrer le nom, puis cliquer sur “Drop Database”.