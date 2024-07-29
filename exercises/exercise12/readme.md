# **Mettre à jour avec ‘Update’ et ’`$set`’** <a href="../../"> <img src="https://github.com/MiKL5/devWeb/raw/master/Assets/Images/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
Via Mongosh
```json
// Afficher toute la table "customers"
db.customers.find( {} , {_id:0} );
// David à 40 ans, corrigez ça !
db.customers.update( {nom:"David"} , {$set:{age:40} } );
// En fait, David à 37 ans
db.customers.updateOne( {nom:"David"} , {$set:{age:37} } );
// Olivier à 95 ans et aime le Piano en plus du violon et de l'escalade
db.customers.updateMany( {nom:"Olivier" } , {$set: {age: 95, loisir:["Escalade", "Piano", "Violon"] } } );

```
Via MongoDB Compass
```json
// Non, aprés vérification, Olivier à bien 59 ans corrigez depuis MongoDB Compass
Cliquer sur le crayon, changer l'âge, puis "UPDATE".
```

**MongoDB n’a pas de transaction, il est impossible de faire un rollback, il est impératif d’être sûr avant d’agir.**
---