# **Afficher les documents de BDD** <a href="../../"> <img src="../../../Assets/Images/mongodb-ar21.svg" alt="PostgreSQL" align="right" height="64px"> </a>
```sql
-- liste des tables
show dbs
-- ou
show databases
-- le résultat est
ELOA    44.00 KiB
admin   40.00 KiB
config  72.00 KiB
local   80.00 KiB

-- afficher la tabl
use ELOA;
switched to db ELOA

-- afficher la collecion d'ELOA
show collections table;

-- afficher la liste des documents de la collection
db.table.find;
db.table.find(); -- affiche tous les documents
db.table.find().pretty(); -- affiche le tout proprement
```
L’id est ajouter par MongoDB pour s’assurer qu’il est unique.