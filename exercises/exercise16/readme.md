# Trier les données avec `sort()` <a href="../../"> <img src="https://github.com/MiKL5/BI/blob/master/assets/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
Via Mongosh
```json
// trier les noms alphabétiquement
db.customers.find().sort({"nom":1});
// trier par âge descendants
db.customers.find().sort({"age":-1});
// Insérer une valeur à David
db.customers.insertOne( {nom:"David" , age:20 , loisir:["voiture" , "violon"] } );
// tier avec âge et nom
db.customers.find().sort( {nom:1 , age:-1} );
```
Via MongoDB Compass
```json
// Dans sort
{nom:1}
{nom:1 , age:-1}
```