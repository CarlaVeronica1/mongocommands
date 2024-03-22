## Comandos de MongoDB
### *Insert*

#### InsertOne:

>db.empleado.insertOne(
{nombre:'Ramon',
apellido:'Lopez',
edad:23}
)

>db.libros.insertOne(
{
    _id:10,
    "titulo":"Los enamorados",
    "autor":"Benito J.",
    "precio":1234.1
})

>db.libros.insertOne(
{_id:11,
titulo:'Estupro',
fianza:true,
anios_carcel:'dos'}
)
 
#### InsertMany: 

>db.empleado.insertMany(
{
    nombre:'Hermeregildo',
    edad:67
},
{
    nombre:'Soylavaca',
    edad:14,
    sexo:'Mujer'},
{
    nombre:'Romulo',
    edad:40,
    nacionalidad:'Nigeriano'
},
{
    nombre:'Cristian Andres',
    localidad:'Sn Miguel de las Piedras',
    nacionalidad:'Aleman',edad:'Esta morro'
})





