# **Insérer plusieurs documents simultanément avec une boucle**
```json
for (let i=0; i< 10; i ++) {db.camion.insert({nom:'camion ${i'});}
db.camion.count(); // 10
db.camion.find(); // liste
```