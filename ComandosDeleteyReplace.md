## Comandos en MongoDB
### *Borrar y Remplazar*

#### Replace:

Remplazar documentos completos (todos) REPLACE()

>db.libros.replaceOne(
    {"_id":10},
    {"titulo":"las patoaventuras de Ezequiel"}
)

**Notas: el _id no se puede remplazar ni actualizar.**


#### Delete (elimina datos) :

Se ocupa para borrar documentos 

##### DeleteOne:

>db.libros.deleteOne(
    {"titulo":'Java para todos'}
)

#### DeleteMany:

>db.libros.deleteMany(
    {cantidad:{$gt:150}}
)

#### DropDatabase:

db.dropDatabse()