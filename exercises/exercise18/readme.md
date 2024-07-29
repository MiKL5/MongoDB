# **L’agrégation des données `$group` et `distinct()`** <a href="../../"> <img src="https://github.com/MiKL5/devWeb/raw/master/Assets/Images/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
Mongosh
```json
// Regouper par type de film et quantifer les types
db.Movies.aggregate( [ {$group:{_id:'$Type', nombre:{$sum:1} } } ] ); // nombre est un alias
// Combien de types ?
db.Movies.distinct("Type"); // 3 types : game, movie, series
```
Avec `aggregate()` regoupement par type nécessite `$`.
---