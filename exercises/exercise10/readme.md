# **Les opérateurs “OR” `$or` et “AND” `$and`** <a href="../../"> <img src="https://github.com/MiKL5/BI/blob/master/assets/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
```json
// Créer la nouvelle table
db.customers.insertMany( [
  { "_id": ObjectId("62987dae7ef39d4dc2ed3ad9"), "nom": "Thuillier", "age": 18, "loisir": ["musique", "football"] },
  { "_id": ObjectId("62987dae7ef39d4dc2ed3ada"), "nom": "Dupond", "age": 20, "loisir": ["gym", "restaurant"] },
  { "_id": ObjectId("62987dae7ef39d4dc2ed3adb"), "nom": "Aznavour", "age": 50, "loisir": ["running", "ecologie"] },
  { "_id": ObjectId("62987dae7ef39d4dc2ed3ade"), "nom": "David", "age": 47, "loisir": ["voiture", "violon"] },
  { "_id": ObjectId("62987dae7ef39d4dc2ed3adf"), "nom": "Olivier", "age": 59, "loisir": ["escalade", "violon"] }
] );
db.customers.find( {$or: [ {nom:"Thuillier"} , {loisir:"restaurant"} ] } ); // retourne 2 documents
db.customers.find( {$and: [ {nom:"Thuillier"} , {loisir:"restaurant"} ] } ); // aucun documents
// Chercher David et le loisir violon
db.customers.find( {$and: [ {nom:"David"} , {loisir:"violon"} ] } , {_id:0} ); // 1 personne

```
Avec MongoDB Compass
```json
{$or: [ {nom:"Thuillier"} , {loisir:"restaurant"} ] } // les 2 mêmes résultats
{$and: [ {nom:"Thuillier"} , {loisir:"restaurant"} ] } // aucun
{$and: [ {nom:"David"} , {loisir:"violon"} ] } // Une personne
```