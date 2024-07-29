# **Les jointures**
MongoDB n’a pas à mettre en relation les documents ; ça se fait par des requêtes.  
```json
constemploi = db.customers.findOne( {"nom":'Thuillier'} );

constemploi = db.emploi.insertMany( [ {emploi:'Jardinier', nomid:constemploi._id} ] );
```