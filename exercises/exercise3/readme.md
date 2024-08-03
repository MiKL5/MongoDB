# **Limiter les données avec `LIMIT`** <a href="../../"> <img src="https://github.com/MiKL5/BI/blob/master/assets/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
```sql
-- Aficher les trois premiers enregistrements
db.table.find().limit(3);
db.table.find().limit(3).pretty();
-- Afficher les titres et années
db.table.find({}, {Title:1 , Year:1});
-- Idem sans l'id
db.table.find({}, {Title:1 , Year:1 , _id:0});
-- Retourner les trois premières lignes
db.table.find({}, {Title:1 , Year:1 , _id:0}).limit(3);
```
<!-- Les objets sont entre acolades -->
<!-- La casse est importante. -->