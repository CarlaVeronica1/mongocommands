## Comados de MongoDB
### *Operadores Lógicos*

#### $Or y $And

>db.libros.find({{$or:[{expresion1},{expresion2}]}})


todos aquellos libros 

>db.libros.find({
    $or:[
        {precio:{$gt:25}},{cantidad:{$lt:15}}
    ] 
})

Seleccionar libro de editorial biblio con precio mayor a 40 o libros de editorial planeta con precio mayor a 30

>db.libros.find(
{$or:[
    {
        $and:[{editorial:{$eq:'Biblio'}},{precio:{$gt:40}}]
    },
    {
    $and:[{precio:{$gt:30}},{editorial:{$eq:'Planeta'}}]
    }
]
    }
)


>db.libros.find(
{$or:[
    {
        $and:[{editorial:{$eq:'Biblio'}},{precio:{$gt:40}}]
    },
{
    $and:[{precio:{$gt:30}},{editorial:{$eq:'Planeta'}}
    ]
}
]
    },{
        titulo:1, cantidad:1, precio:1, _id:0
    }
)

>db.libros.find(
{$and:[
    {precio:{$gt:5}},
    {autor:{$exists:true}}
    ] 
})