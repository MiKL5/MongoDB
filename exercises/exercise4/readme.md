# **Recherche simple avec `fint()`** <a href="../../"> <img src="https://github.com/MiKL5/devWeb/raw/master/Assets/Images/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
Pour cela, il faut utiliser le premier argument
```sql
-- recherche simple
db.table.find({Title:'My Life as a Teenage Robot'});
db.table.find({Title:'My Life as a Teenage Robot'}).pretty();
-- rechercher les films avec robots en titre
b.table.find({Title:/Robot/}).pretty();
-- idem sans avoir à respecter la casse
db.table.find({Title:/robot/i}).pretty();
-- combien de documents sont retournés
db.table.find({Title:/robot/i}).count(); -- il y en a 20
```
Dans la console
```sql
{Title: "Robot"} -- rien
{Title: "Robot Carnival"} -- trouvé
{Title: /Robot/} -- trouvé 20
{Title: /robot/i} -- idem
-- avec la 3 dans la case `limit` de la console, il remonte les trois premiers
```
Les simple guillements `'` ou double `"` n’omt pas d’importance.
La touche entrée lance `find` avec la console.