# **MongoDB** <a href="https://github.com/MiKL5/BI/"> <img src="https://github.com/MiKL5/BI/blob/master/assets/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
MongoDB à été crée à New York par offrant une licence communotaire (gratuite). Il y a une licence enterprise permettant plus de services.  
MongoDB est la base de données NoSQL la plus populaire.  
NoSQL signifie Not Only SQL.  

Il n’y a pas de schéma relationnel entre les tables, il s’agit donc de données non structurées.  

Le NoSQL est largement répendu, e.g. Facebook, eBay. D’où la vélocité des pages.  
Cependant, d’où vient la fluidité et les performances très proche d’SQL, voire meilleures ?

Il faut savoir que cette base de données est orienté document, stock en JSON et CSV.  

Le `sharding` est une réplications sur un certain nombre de noeuds. La puissance de MongoDB est de bénéficier (e.g. dans un docker) de la réplication dynamique d’un certain nombre de noeuds.  

Son langage est très riche est n’a rien à voir avec le T-SQL.  

Les tables sont appeller collections.

0. [Connaître la version](docs/version)
___
## Créer une table de base de donnée et une collection
1. [Importer des données](exercises/exercise1)
2. [Affichier les documents de BDD](exercises/exercise2)
3. [Limiter les données `LIMIT()`](exercises/exercise3)
4. [Simple recherche `FIND()`](exercises/exercise4)
## Les requêtes
5. [Rechercher dans un tableau](exercises/exercise5)
6. [Ins2rer une ou plusieurs donn2es dqns les docuéents](exercises/exercise6)
7. [Suppriéer une collection](exercises/exercise7)
8. [Insérer plusieurs documents simultanément avec une boucle](exercises/exercise8)   
## Les opérateurs les plus courants
9. [`$gt`, `$gte`, `$lt`, `$lte`](exercises/exercise9)
10. [`$or`, `$and`](exercises/exercise10)
11. [`$in` , `$nin` , `$all`](exercises/exercise11)
## Mettre à jour et supprimer un document
12. [`Update` et `$set`](exercises/exercise12)  
13. [`Push`, `$each` et `$addtoset`](exercises/exercise13)  
14. [Le concept Upset](exercises/exercise14)  
15. [Supprimer une collection et une base de données](exercises/exercise15)
## Trier, agréger les données et les jointures
16.  [Trier les données avec le `sort`](exercises/exercise16)
17. [`Limit` et `Skip`](exercises/exercise17)
18. [L’agrégation `$group` et `distinct`](exercises/exercise18)
19. [L’agrégation avec MongoDB Compass](exercises/exercise19)
20. [Les jointures avec MongoDB](exercises/exercise20)
21. [Faire une requête avec jointure avec `$lookup`](exercises/exercise21)