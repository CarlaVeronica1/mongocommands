## Comandos en Mongodb
### *Expresiones Regulares*

**Nota: Mongodb es sensible a mayusculas y minusculas.**

 Este primer código significa que de la bd libros buscara todo titulo que contenga una "t".   
 *select * from libros where titulo like '%t%'*.
>db.libros.find("titulo" :/t/)

de la bd libros buscara todo titulo que contenga una "MongoDB".
>db.libros.find({
    "titulo":/MongoDB/
})
de la bd libros buscara todo titulo que termine con "tos".
>db.libros.find("titulo":/tos$/)

de la bd libros muestra a todos los que empiezen con M.
>db.libros.find("titulo":/^M/)

Con la funcion **$regex** se puede realizar lo mismo.
>db.libros.find("titulo":{$regex:'para'})

>db.libros.find("titulo":{$regex:/para/})

Para que el lenguaje no note entre mayusculas y minusculas se usa la función **$options**.
>db.libros.find("titulo":{
    {$regex:/mongo/,
    $options:"i"}
})

**Nota: options:"i" es pra el case sensitive, para que no lo limite**
