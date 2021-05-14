# IBM DB2
## conectar a la base de datos desde consola de IBM
En los programas instalados buscar DB2 Command Window

![](../Resources/db2/commandWindowdb2.png)

A continuación, escriba el comando db2:
```
C:\Program Files\IBM\SQLLIB\BIN>db2
```
Verá el siguiente procesador de linea de comandos para el cliente DB2:
```
db2 => 
```
A continuación, utilice el comando CONNECT para conectarse a una basde de datos especifica, por ejemplo, la base de datos books:
```
db2 => connect to books user db2admin
```
Este comando nos permite conectarnos a la base de datos utilizando el usuario con la contraseña. Debe proporcionar la contraseña correcta pra el usuario Books db2admin db2admin.

Aquií está la salida:
```
Database Connection Information

Database server        = DB2/NT64 11.1.4.4
SQL authorization ID   = DB2ADMIN
Local database alias   = BOOKS
```

Posteriormente, puede emititr cualquier instruccion SQL o el comando DB2 para interactuar con la base de datos Books. Por ejempo, el siguiente comando enumera todas las tablas de la base de datos: Books.
```
db2 => list tables
```

Esta imagen miestra la salida:

![](../Resources/db2/respuestaTables.png)

para finalizar, salga de la sesión mediante el comando quit:
```
db2 => quit
DB20000I  The QUIT command completed successfully.
```

## Conectar a la base de datos desde la consola de Windows.
Navegamos a la dirección en donde tenemos la base instalada DB2.

![](../Resources/db2/powershellDB2.png)!

nota: si escribimos ./db2.exe nos mostrará el siguiente error.

![](../Resources/db2/errorDb2.png)

Para solucionar el problema ejecutamos el siguiente comando:
```
.\db2cmd.exe -i -w db2clpsetcp     <-- para powershell
```

ahora si ejecutamos el comando db2, aceptara los comandos 

Para seleccionar la base de datos ejecutamos el comando
```
db2 => connect to books user db2admin
Escriba la contraseña actual de db2admin: ingresamos la contraseña
db2 => list tables
```

![](../Resources/db2/listablesPShell.png)

Si deseamos cambiar de base de datos ejecutamos el primer comando pero con nombre de la base de datos.