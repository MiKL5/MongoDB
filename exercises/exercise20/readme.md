# **Les jointures** <a href="../../"> <img src="https://github.com/MiKL5/devWeb/raw/master/Assets/Images/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
MongoDB n’a pas à mettre en relation les documents ; ça se fait par des requêtes.  
```json
constemploi = db.customers.findOne( {"nom":'Thuillier'} );

constemploi = db.emploi.insertMany( [ {emploi:'Jardinier', nomid:constemploi._id} ] );
```