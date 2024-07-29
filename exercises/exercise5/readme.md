# **Rechercher dans un tableau**
```sql
db.technos.find().pretty();
-- Afficher l'équipe d'Andrw Clark dans le document "team"
db.technos.find({'team': 'Andrew Clark'}).pretty();
-- Avec la regex `/qqch/i`
db.technos.find({'team': /andrew clark/i}); -- même resultat
db.technos.find({'team': /andrew clark/i}).pretty(); -- organisé en json
```