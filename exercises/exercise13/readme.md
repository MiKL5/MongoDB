# Ajouter une valeur avec`push`, en ajouter plusieurs avec `$each` et chercher un doublon avec `$addToSet` <a href="../../"> <img src="https://github.com/MiKL5/devWeb/raw/master/Assets/Images/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
```json
// Dupont à un troisième loisir le football
db.customers.updateOne( {nom:"Dupond"} , {$push: {loisir:"football"} } );
db.customers.updateOne( {nom:"Dupond"} , {$addToSet: {loisir:"football"} } ); // pas de modification
// M. Dupond aime aussi le violon, le dessin et le digital-art
db.customers.updateOne( {nom:"Dupond"} , {$addToSet: {loisir:{$each:["violon" , "dessin" , "digital-art"] } } } ); // Réussi

```
Via MongoDB Compass
```json
// AJouter la pétanque à Monsieur Dupond
Cliquer sur le crayon, sur le plus au début de la dernière ligne puis 'Add item after 2', noté pétanque, puis cliquer sur 'UPDATE'. // Il est possible d'ajouter entre n'importe quelle ligne. Autant de document nécessaire sont ajoutable.
```
**En JSON, il n’y a pas de notion d’intégrité, il peut y avoir des doublons.**  
**Il faut utiliser `$addToSet`.**
---