# **L’agrégation avec MongoDB Compass**
Dans l’onglet “Aggregations” , “Add Stage”.  
Stage 1 : `$project`
```json
{
  nom:"Dupond" // Affiche tous les documents avec Dupond
}
// Ou
{
  nom:1,
  age:1
}
```
Stage 2 : `$match`
```json
{
  age:{$gt:20} // Les personnes de plus de 20 ans
}
```
Stage 3 : `$group`
```json
{
  _id: '$nom',
  age_moyen: {
    $avg: '$age' // Les Davis ont en moyenne 60 ans (faux) Si $match est activé
  }              // est 50 ans quand $match est désactivé
}
```
Stage 4 : `$sort` et désactiver le stage 3
```json
{
  _id: '$nom',
  age_max: {
    $max: '$age' // Le plus vieux Davis à 80 ans
  }
}
```
Stage 5 : `$sort` les moyennes d’âge ascendant
```json
{
  age_moy: 1
}
```
Stage 6 : `$count` afficher les 5 documents
```json
'age_moy'
```
Stage 7 : `$project` diviser l’âge par 2 `$project`
```json
{
  nom:1,
  age:{$divide:['$age',2] }
}
```
Supprimer un stage : Cliquer les `...`, puis `Delete stage`. Il n’y a pas de confirmation.  