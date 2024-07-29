# **Faire une requête avec jointure avec `$lookup`**
Mongosh
```json
// Affibler les notes correpondantes aux élèves
db.eleves.aggregate( [
    {
        $lookup:{
            "from" : "devoirs",
            "localField" : "code",
            "foreignField" : "code",
            "as" : "details_note"
        }
    }
] );
// Afficher de manière plus lisible
db.eleves.aggregate( [
    {
        $lookup:{
            "from" : "devoirs",
            "localField" : "code",
            "foreignField" : "code",
            "as" : "details_note"
        }
    },
    {
        $project:{
            "id" : 0,
            "detail_notes._id" : 0,
            "detail_note.code" : 0
        }
    }
] );
// Via la nouvelle collection projets
db.projets.insertMany( [ {"codes" : ["NAT123" , "NAT125"] , "mtiere" : "Dessin" , "note" : 15 } ] );
//
db.projets.aggregate( [
    {
        $unwind : "$codes" // coupe le table
    },
    {
        $lookup : {
            "from" : "eleves",
            "localField" : "code",
            "foreighField" : "code",
            "as" : "eleve"
        }
    },
    {
        $projets : {
            "_id" : 0,
            "codes" : 0,
            "eleve._id" : 0
        }
    }
] );
```
MongoDB Compass  
Dans Aggregation, `$lookup`
```json
{
    "from" : "devoirs",
    "localField" : "code",
    "foreignField" : "code",
    "as" : "detail_notes"
}
```