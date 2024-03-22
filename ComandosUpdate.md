## Comandos de MongoDB
### Update

#### UpdateOne:

>db.libros.updateOne(
    {titulo:'Java para todos'},
    {$set:{titulo:'Java el rey'}}
)

>db.libros.updateOne(
    {_id:10},
    {$set:{
        "precio":10.2,
        "cantidad":50
        }}
)

#### UpdateMany:

>db.libros.updateMany(
{
    precio:{$gt:100}
},
{
    $set:{precio:150}}
)

>db.libros.updateMany(
{
    precio:{$gt:100}
},
{   
    $set:{precio:150}
}
)

>db.libros.updateMany(
    {},
    {$inc:{precio:5}}
)

>db.libros.updateMany(
    {_"_id":10},
    {{$inc:{precio:5}}}
)

>db.libros.updateMany(
    {"cantidad":{$gt:20}},
    {$mul:{precio:2}}
)