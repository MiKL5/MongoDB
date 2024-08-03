# **Trier avec limit() et skip()** <a href="../../"> <img src="https://github.com/MiKL5/BI/blob/master/assets/mongodb-ar21.svg" alt="MongoDB" align="right" height="64px"> </a>
`limit()` est une sorte de top 1, 2, 3…  
Quant à `skip()`, un saut de données (équivalent d’offset en T-SQL).

Via Mongosh
```json
// Les trois premier films
db.Movies.find( {} , {Title:1 , Year:1} ).limit(3);
// Afficher 10 films dés le troisième
db.Movies.find( {}, {Title:1 , Year:1} ).limit(3);
// Idem + titre décroissant
db.Movies.find( {}, {Title:1 , Year:1} ).sort({Title:-1}).skip(3).limit(10);
// idem et titre croissant
db.Movies.find( {}, {Title:1 , Year:1} ).sort({Title:1}).skip(3).limit(10);
```
Via MondoDB Commpass

À droite skip:3 et limit:10.  
Dans sort `{Title:-1}`.