# **Insérer une ou plusieurs donnnées dans les documents**
## Insérer un document
Dans la console
```json
db.voiture.insertOne({"modele":"Peugoet"});
```
Dans Compass  
Copier le doucment, cliquer “Add data”, “Insert document”, puis insert.
```json
{
  "_id": {
    "$oid": "66a6342bb15540908e15ef71"
  }, "modele": "Lamborghini"
}
```
## Insérer plusieurs documents
Dans la console
```json
db.voiture.insertMany( [ {modele:"Renault"} , {modele:"Dacia"} ] );
```