# **Les opérateur “IN” `$in`, “NOT IN” `$nin` et “ALL” `$all`** <a href="../../"> <img src="https://github.com/MiKL5/BI/blob/master/assets/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
Avec Mongosh
```json
// Afficher les infos de David et Olivier
db.customers.find( {nom: {$in: ["David" , "Olivier"] } } );
db.customers.find( {nom: {$in: ["David" , "Olivier"] } }  , {_id:0} );
// Afficher tous sauf eux
db.customers.find( {nom: {$nin: ["David" , "Olivier"] } }  , {_id:0} );
// Qui aime le violon est les voitures ?
db.customers.find( {loisir: {$all: ["violon" , "voiture"] } }  , {_id:0} ); // David
// Qui aime le violon .
db.customers.find( {loisir: {$all: ["violon"] } }  , {_id:0} ); // David et Olivier
```
Avec MongoDB Compass
```json
{nom: {$in: ["David" , "Olivier"] } }
{nom: {$nin: ["David" , "Olivier"] } }
{loisir: {$all: ["violon" , "voiture"] } }
{loisir: {$all: ["violon" , "voiture"] } }
```
___
`$all` ne prend que les valeurs voulues dans tout le tableau