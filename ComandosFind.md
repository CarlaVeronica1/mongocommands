## Comandos en MongoDDB
### *Find*

*Find:*

Encuentra todos los documentos dentro de los parametros insertados

>db.libros.find()

>db.libros.find(
{},
{titulo:1}
)

>db.libros.find(
{titulo:'Don Quijote'},
{titulo:1}
)

>db.libros.find(
{titulo:'Don quijote'},
{id:0,titulo:1,precio:25}
)

>db.libros.find(
{titulo:{$exists:true}}
)

>db.libros.find(
{autor:{$exists:false}}
)

>db.libros.find(
{
    precio:{$type:'double'}
})

>db.libros.find(
{precio:{$type:1}}
)

>db.libros.find({_id:9})