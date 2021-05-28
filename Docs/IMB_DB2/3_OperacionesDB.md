# Operaciones con base de datos
Se muestran algunas formas de las operaciones que se pueden hacer en DB2

## Crear base de datos.
La siguiente instrucción se utiliza para crear la basde de datos:

```db2
db2 => CREATE DATABASE books
```

Tomará un tiempo para crear la base de datos. Una vez creada, verá el siguiente mensaje:

```db2
db2 =>The CREATE DATABASE command completed successfully

```

Esto significa que ah creado correctamente una nueva base de datos.

Para enumerar todas las bases de datos de la instancia actual, utilice el comando: 

```db2
db2 => list database directory
```

Nos mostrará las bases de datos disponibles.

## Crear tablas desde un archivo.
```
db2 -stvf d:\bookdb\create.sql
```

Despues, utizaremos el siguiente comando para ejecutar el script .sql datos para insertar datos en las tablas.

```db2
db2 -stvf d:\bookdb\data.sql
```

## Llenar datos desde un archivo.
Por último, utilice el siguiente comando para comprobar si los datos se cargan correctamente:

```
db2 select count(*) author_count from authors
```
