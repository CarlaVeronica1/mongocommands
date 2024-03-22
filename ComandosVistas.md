## Comandos de MongoDB
### *Vistas.*

#### DELIMITACIONES:

*Solo muestra ciertos atributos de la base de datos*

>db.libros.find(
    {},
    {
        {id:0,
        titulo:1,
        precio:1}
    }
)

#### SORT:

*En el sort se pone como se deben de acomodar los datos de acuerdo a cierto atributo*

**Notas: Si es ascendente se pone 1 y para descendente se agrega un -1**

>db.libros.find(
    {},{{id:0,titulo:1,precio:1}}).sort({titulo:1}
)

>db.libros.find(
    {},{{id:0,titulo:1,precio:1}}).sort({titulo:-1})

**Notas: la prioridad del sort es de izquierda a derecha.**

>db.libros.find(
    {},{titulo:1,precio:1,editorial:1,_id:0}).sort({titulo:1,editorial:1})

#### Limit:

*Limita el numero de resultados que se muestran en la vista.*

>db.libros.find(
    {},{titulo:1,precio:1,editorial:1,_id:0}).limit(2).sort({titulo:1,editorial:1})

>db.libros.find(
    {},{titulo:1,precio:1,editorial:1,_id:0}).size().sort({titulo:1,editorial:1})

#### Skip:

*Este metodo sirve para saltarse documentos*

>db.libros.skip()

 >db.libros.find(
    {},{"titulo":1,"precio":1,"_id":0,"editorial":1}).skip(3).sort({titulo:1}).limit(2)