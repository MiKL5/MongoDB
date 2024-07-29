# **Le concept ’`Upsert`’**
Via Mongosh
```json
// Ajouter Justine et ses loisirs
db.customers.updateOne( { nom: "Justine" } , { $set: { loisir: ["crochet", "danse classique", "peinture", "running"] } } , { upsert: true } );
```
<!-- ```json
// Ajouter plusieurs personnes en une ligne
db.customers.updateOne( { nom: "Justine1" } , { $set: { loisir: ["crochet", "danse classique", "peinture", "running"] } } , { upsert: true } );db.customers.updateOne( { nom: "Justine2" } , { $set: { loisir: ["crochet", "danse classique", "peinture", "running"] } } , { upsert: true } );db.customers.updateOne( { nom: "Justine3" } , { $set: { loisir: ["crochet", "danse classique", "peinture", "running"] } } , { upsert: true } );db.customers.updateOne( { nom: "Justine4" } , { $set: { loisir: ["crochet", "danse classique", "peinture", "running"] } } , { upsert: true } );
// Autrement
db.customers.insertMany( [ { nom: "David", age: 60, loisir: ["voiture", "violon"] }, { nom: "David", age: 80, loisir: ["Voiture", "Violon"] } ] ) ;
``` -->