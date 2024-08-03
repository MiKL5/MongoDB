# **Supprimer une collection et une base de données** <a href="../../"> <img src="https://github.com/MiKL5/BI/blob/master/assets/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
Via Mongosh
```json
// Trouver Aznavour avc l'id
db.customers.findOne(ObjectId("62987dae7ef39d4dc2ed3adb"))
// le supprimer
db.customers.deleteOne({ _id: ObjectId("62987dae7ef39d4dc2ed3adb") });
// Supprimer David
db.customers.deleteOne( {nom:"David"} );
// Supprimer plusieurs personnes par le nom
db.customers.deleteMany({ nom: { $in: ["Justine2", "Justine3"] } });
// Supprimer plusieurs personne par l'id
db.customers.deleteMany({ "_id": { $in: [ ObjectId("66a6b746a9d43d3ffbf2a193"), ObjectId("66a6b746a9d43d3ffbf2a195"), ObjectId("66a6b746a9d43d3ffbf2a197"), ObjectId("66a6b746a9d43d3ffbf2a199") ] } } );
// Supprimer la Database en cours
db.dropDatabase();
```
Via MongoDB Compass  

Pour un document, la corbeille ‘Remove document’, puis ‘DELETE’.  
Pour une collection trois point, ‘Drop collection’, saisir le nom, puis ‘Drop Collection’.  
Pour une bdd, la corbeille ‘Drop database’, saisir le nom, puis ‘Drop Database’.

**La fonction `remove()` est dépreciée, utiliser `deleteOne()` ou `deleteMany()`.**  
L’ObjectId doit être encapsuler dans un objet de filtre `_id` pour cibler correctement le document.  
Toute suppresion est irréversible et pas d’info avant d’agir.
---