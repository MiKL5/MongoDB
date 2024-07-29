# **Insérer plusieurs documents simultanément avec une boucle** <a href="../../"> <img src="https://github.com/MiKL5/devWeb/raw/master/Assets/Images/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
```json
for (let i=0; i< 10; i ++) {db.camion.insert({nom:'camion ${i'});}
db.camion.count(); // 10
db.camion.find(); // liste
```