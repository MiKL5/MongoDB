# **L’agrégation des données `$group` et `distinct()`**
Mongosh
```json
// Regouper par type de film et quantifer les types
db.Movies.aggregate( [ {$group:{_id:'$Type', nombre:{$sum:1} } } ] ); // nombre est un alias
// Combien de types ?
db.Movies.distinct("Type"); // 3 types : game, movie, series
```
Avec `aggregate()` regoupement par type nécessite `$`.
---