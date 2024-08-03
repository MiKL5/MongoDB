# **Rechercher dans un tableau** <a href="../../"> <img src="https://github.com/MiKL5/BI/blob/master/assets/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
```sql
db.technos.find().pretty();
-- Afficher l'équipe d'Andrw Clark dans le document "team"
db.technos.find({'team': 'Andrew Clark'}).pretty();
-- Avec la regex `/qqch/i`
db.technos.find({'team': /andrew clark/i}); -- même resultat
db.technos.find({'team': /andrew clark/i}).pretty(); -- organisé en json
```