# **Les opérateurs “greater than” `$gt`, “greater than or equal” `$gte`, “less than” `$lt`, “less than or equal” `$lte`** <a href="../../"> <img src="https://github.com/MiKL5/devWeb/raw/master/Assets/Images/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
```json
// Créer la table 'clients'
db.clients.insertMany( [ {nom:'Thuuillier' , age:18} , {nm:'Dupond' , age:20} , {nom:'Dupont' , age:50} , {nom:'Mary' , age:27} , {nom:'Delassus' , age:25} ] );
db.clients.find(); // tous les clients y sont
db.clients.count(); // 5
// Les personne de plus de 19 ans avec 'Greater than `$gt`'
db.clients.find({age: {$gt:19} } ); // 4 personnes ont plus de 19 ans
// Plus de 20 ans
db.clients.find({age: {$gt:20} } ); // 3 personnes
// 20 est plus
db.clients.find({age: {$gte:20} } ); // 4 personne
// moins de 50
db.clients.find({age: {$lt:50} } ); // 4
// 27 et moins
db.clients.find({age: {$lte:27} } ); // 4
```