## SERVICIOS ARVISGAME v.1.0
###### Elaborado por: Geovani Gómez Pérez, Richel Ociel Lima Sanchéz 13 de abril de 2021 15:34
##### Estos servicios muestran función, datos de entrada y salida.
##### Se muestra el orden en el que se tienen que almacenar la información referente al orden del índice.
|<a name="0">Índice</a>|||
|--------|--------|--------|
|- 1.- Usuarios|- 5.- Niveles|- 9.- Juegos-Niveles-Usuarios|
|	- 1.1.- [Agregar Usuarios](#1)|- 5.1.- [Agregar Niveles](#17)|- 9.1.- [Agregar Juegos-Niveles-Usuarios](#33)|
|	- 1.2.- [Actualizar Usuarios](#2)|- 5.2.- [Actualizar Niveles](#18)|- 9.2.- [Actualizar Juegos-Niveles-Usuarios](#34)|
|	- 1.3.- [Eliminar Usuarios](#3)|- 5.3.- [Eliminar Niveles](#19)|- 9.3.- [Eliminar Juegos-Niveles-Usuarios](#35)|
|	- 1.4.- [Consultar Usuarios](#4)|- 5.4.- [Consultar Niveles](#20)|- 9.4.- [Consultar Juegos-Niveles-Usuarios](#36)|
|- 2.- Productos|6.- Juegos-Niveles|- 10.- Juegos-Colección|
|	- 2.1.- [Agregar Productos](#5)|- 6.1.- [Agregar Juegos-Niveles](#21)|- 10.1.- [Agregar Juegos-Colección](#37)|
|	- 2.2.- [Actualizar Productos](#6)|-6.2.- [Actualizar Juegos-Niveles](#22)|- 10.2.- [Actualizar Juegos-Colección](#38)|
|	- 2.3.- [Eliminar Productos](#7)|-6.3.- [Eliminar Juegos-Niveles](#23)|- 10.3.- [Eliminar Juegos-Colección](#39)|
|	- 2.4.- [Consultar Productos](#8)|-6.4.- [Consultar Juegos-Niveles](#24)|- 10.4.- [Consultar Juegos-Colección](#40)|
|- 3.- Colecciones|- 7.- Misiones|- 11.- Juegos-Productos|
|	- 3.1.- [Agregar Colecciones](#9)|- 7.1.- [Agregar Misiones](#25)|- 11.1.- [Agregar Juegos-Productos](#41)|
|	- 3.2.- [Actualizar Colecciones](#10)|- 7.2.- [Actualizar Misiones](#26)|- 11.2.- [Actualizar Juegos-Productos](42)|
|	- 3.3.- [Eliminar Colecciones](#11)|- 7.3.- [Eliminar Misiones](#27)|- 11.3.- [Eliminar Juegos-Productos](#43)|
|	- 3.4.- [Consultar Colecciones](#12)|-7.4.- [Consultar Misiones](#28)|- 11.4.- [Consultar Juegos-Productos](#44)|
| - 4.- Juegos|- 8.- Misiones-Usuarios|
|	- 4.1.- [Agregar Juegos](#13)|- 8.1.- [Agregar Misiones-Usuarios](#29)|
|	- 4.2.- [Actualizar Juegos](#14)|- 8.2.- [Actualizar Misiones-Usuarios](#30)|
|	- 4.3.- [Eliminar Juegos](#15)|- 8.3.- [Eliminar Misiones-Usuarios](#31)|
|	- 4.4.- [Consultar Juegos](#16)|- 8.4.- [Consultar Misiones-Usuarios](#32)|
* * *
## Usuarios
```
http://sandbox.arvispace.com/arvisgameAPI/usuarios.php
```
#### <a name="1"> Agregar Usuario</a>
Petición: **POST**
Descripcion: Este servicio agrega usuarios por su correo electrónico
Datos de entrada: **mail varchar(60)**
Datos de salida: 1 success

#### <a name="2"> Actualizar Usuarios</a>
Petición: **POST**
Descripcion: Este servicio sirve para actualizar datos de usuarios
Datos de entrada: ** id_usuarios (INT), email_usuario varchar(60)**
Datos de salida: 1 success

#### <a name="3"> Eliminar Usuarios</a>
Petición: **POST**
Descripción: Este servicio elimina registro de usuario
Datos de entrada: **id_e (INT)**
Datos de salida: 1 success

#### <a name="4"> Consultar Usuarios</a>
Petición: **GET**
Descripción: Este servicio muestra todos los registros, si se agrega un parámetro para buscar un dato especifico solo mostrara ese dato.
Datos de entrada: **id (INT) (Opcional)**
Datos de salida:
- Muestra todos los registros de la tabla
- Muestra el registro de la tabla por id


[Regresar al Índice](#0)
* * *
## Productos
```
http://sandbox.arvispace.com/arvisgameAPI/productos.php
```
#### <a name="5"> Agregar Producto</a>
Petición: **POST**
Descripción: Este servicio agrega productos indicando su id del producto y el nombre del producto
Datos de entrada:  **id_producto(INT),producto varchar(60)**
Datos de salida: 1 success

#### <a name="6"> Actualizar Producto</a>
Petición: **POST**
Descripción: Este servicio sirve para actualizar datos de los productos por id
Datos de entrada: **id (INT), id_pro (INT), nom_pro varchar(60)**
Datos de salida: 1 success

#### <a name="7"> Eliminar Producto</a>
Petición: **POST**
Descripción: Este servicio elimina registro de productos por id
Datos de entrada: ** id_e (INT)**
Datos de salida: 1 success

#### <a name="8"> Consultar Producto</a>
Petición: **GET**
Descripción: Este servicio muestra todos los registros de productos, si se agrega un parámetro para buscar un dato especifico solo mostrara ese dato.
Datos de entrada: ** id (INT) (Opcional)**
Datos de salida:
- Muestra todos los registros de la tabla
- Muestra el registro de la tabla por id

[Regresar al Índice](#0)
* * *
## Colecciones
```
http://sandbox.arvispace.com/arvisgameAPI/colecciones.php
```
#### <a name="9"> Agregar Colección</a>
Petición: **POST**
Descripción: Este servicio agrega una colección indicando su nombre de la colección y icono que utilizara (ruta)
Datos de entrada:  **nombre_insert varchar(60),icon_insert varchar(50)**
Datos de salida: 1 success

#### <a name="10"> Actualizar Colección</a>
Petición: **POST**
Descripción: Este servicio sirve para actualizar datos de las colecciones por id
Datos de entrada: **id_update (INT), nombre_update varchar(50), icon_update varchar(50)**
Datos de salida: 1 success

#### <a name="11"> Eliminar Colección</a>
Petición: **POST**
Descripción: Este servicio elimina registro de las colecciones por id
Datos de entrada: ** id_colection_delete (INT)**
Datos de salida: 1 success

#### <a name="12"> Consultar Colección</a>
Petición: **GET**
Descripción: Este servicio muestra todos los registros de la colección, si se agrega un parámetro para buscar un dato especifico solo mostrara ese dato.
Datos de entrada: ** id_coleccion_read (INT) (Opcional)**
Datos de salida:
- Muestra todos los registros de la tabla
- Muestra el registro de la tabla por id

[Regresar al Índice](#0)
* * *
## Juegos
```
http://sandbox.arvispace.com/arvisgameAPI/games.php
```
#### <a name="13"> Agregar Juego</a>
Petición: **POST**
Descripción: Este servicio agrega juegos indicando el nombre del juego y la ruta del icono
Datos de entrada:  **nom varchar(50),icon varchar(50)**
Datos de salida: 1 success

#### <a name="14"> Actualizar Juego</a>
Petición: **POST**
Descripción: Este servicio sirve para actualizar datos de los juegos por id
Datos de entrada: **id_juego (INT), nombre (varchar(50), icono_juego varchar(50)**
Datos de salida: 1 success

#### <a name="15"> Eliminar Juego</a>
Petición: **POST**
Descripción: Este servicio elimina registro de juegos por id
Datos de entrada: ** id_prod (INT)**
Datos de salida: 1 success

#### <a name="16"> Consultar Juego</a>
Petición: **GET**
Descripción: Este servicio muestra todos los registros de juegos, si se agrega un parámetro para buscar un dato especifico solo mostrara ese dato.
Datos de entrada: ** id_juego (INT) (Opcional)**
Datos de salida:
- Muestra todos los registros de la tabla
- Muestra el registro de la tabla por id

[Regresar al Índice](#0)
* * *
## Niveles
```
http://sandbox.arvispace.com/arvisgameAPI/niveles.php
```
#### <a name="17"> Agregar Nivel</a>
Petición: **POST**
Descripción: Este servicio agrega niveles que serán utilizados por los juegos indicando su nombre del nivel
Datos de entrada:  **level varchar(60)**
Datos de salida: 1 success

#### <a name="18"> Actualizar Nivel</a>
Petición: **POST**
Descripción: Este servicio sirve para actualizar datos de los niveles por id
Datos de entrada: **id_nivel (INT), nombre varchar(60)**
Datos de salida: 1 success

#### <a name="19"> Eliminar Nivel</a>
Petición: **POST**
Descripción: Este servicio elimina registro de niveles por id
Datos de entrada: ** id_nivel_e (INT)**
Datos de salida: 1 success

#### <a name="20"> Consultar Nivel</a>
Petición: **GET**
Descripción: Este servicio muestra todos los registros de los niveles agregados, si se agrega un parámetro para buscar un dato especifico solo mostrara ese dato.
Datos de entrada: ** id (INT) (Opcional)**
Datos de salida:
- Muestra todos los registros de la tabla
- Muestra el registro de la tabla por id

[Regresar al Índice](#0)
* * *
## Niveles de Juegos


```diff
- Estos registros requieren que existan datos en Juegos y Niveles para su funcionamiento
```
```
http://sandbox.arvispace.com/arvisgameAPI/juegos_level.php
```
#### <a name="21"> Agregar Niveles a Juego</a>
Petición: **POST**
Descripción: Este servicio asignarán niveles para los juegos indicando su nombre del nivel
Datos de entrada:  **juego (INT), nivel(INT)**
Datos de salida: 1 success

#### <a name="22"> Actualizar o modificar el nivel del juego</a>
Petición: **POST**
Descripción: Este servicio actualiza los niveles asignados a los juegos, sé requiere de la id para la modificación
Datos de entrada: **id_game_level (INT), id_juego (INT), id_nivel(INT)**
Datos de salida: 1 success

#### <a name="23"> Eliminar nivel de un juego</a>
Petición: **POST**
Descripción: Este servicio elimina el registro del nivel asignado a un juego
Datos de entrada: ** id_g_l_e (INT)**
Datos de salida: 1 success

#### <a name="24"> Consulta los niveles de juegos</a>
Petición: **GET**
Descripción: Este servicio muestra todos los registros de los niveles asignados por juego, si se agrega un parámetro para buscar un dato especifico solo mostrara ese dato.
Datos de entrada: ** id (INT) (Opcional)**
Datos de salida:
- Muestra todos los registros de la tabla
- Muestra el registro de la tabla por id

[Regresar al Índice](#0)
* * *
## Misiones
```diff
- Este registro requiere que existan niveles asignados a juegos
```
```
http://sandbox.arvispace.com/arvisgameAPI/misiones.php
```
#### <a name="25"> Agregar misión</a>
Petición: **POST**
Descripción: Este servicio asignara la misión del juego
Datos de entrada:  **juego_nivel (INT), mision varchar(50)**
Datos de salida: 1 success

#### <a name="26"> Actualizar o modificar misión</a>
Petición: **POST**
descripción: Este servicio actualiza los niveles asignados a los juegos, sé requiere de la id para la modificación
Datos de entrada: **id_game_level (INT), id_juego (INT), id_nivel(INT)**
Datos de salida: 1 success

#### <a name="27"> Eliminar misión de un juego</a>
Petición: **POST**
descripción: Este servicio elimina el registro del nivel asignado a un juego
Datos de entrada: ** id_mision_e (INT)**
Datos de salida: 1 success

#### <a name="28"> Consulta las misiones </a>
Petición: **GET**
descripción: Este servicio muestra todos los registros de las misiones asignadas al juego, si se agrega un parámetro para buscar un dato especifico solo mostrara ese dato.
Datos de entrada: ** id_mision (INT) (Opcional)**
Datos de salida:
- Muestra todos los registros de la tabla
- Muestra el registro de la tabla por id

[Regresar al Índice](#0)
* * *
## Misiones de Usuarios
```diff
- Este registro requiere que existan Misiones de juegos y usuarios registrados
```
```
http://sandbox.arvispace.com/arvisgameAPI/mision_usuario.php
```
#### <a name="29"> Asignar misión a usuario</a>
Petición: **POST**
descripción: Este servicio asignará la misión del juego al usuario
Datos de entrada:  **user_fk (INT), mision_fk (INT), statusM(INT)**
Datos de salida: 1 success

#### <a name="30"> Actualizar o Modificar misión de Usuarios</a>
Petición: **POST**
descripción: Este servicio actualiza la misión del usuario, se requiere de la id para la modificación
Datos de entrada: **id (INT), mision (INT), usuario(INT), status(INT)**
Datos de salida: 1 success

#### <a name="31"> Eliminar misión de usuario</a>
Petición: **POST**
descripción: Este servicio elimina la asignación de misión al usuario
Datos de entrada: ** id_e (INT)**
Datos de salida: 1 success

#### <a name="32"> Consulta las misiones del usuario </a>
Petición: **GET**
descripción: Este servicio muestra todos los registros de las misiones asignadas a los usuarios, si se agrega un parámetro para buscar un dato especifico solo mostrara ese dato.
Datos de entrada: ** mision_usuario (INT), mision_mision(INT) (Opcional)**
Datos de salida:
- Muestra todos los registros de la tabla
- Muestra el registro de la tabla por id de misión y de usuario

[Regresar al Índice](#0)
* * *
## Niveles de Juegos a Usuarios
```diff
- Este registro requiere que existan Niveles de juegos y usuarios registrados
```
```
http://sandbox.arvispace.com/arvisgameAPI/niveles_usuario.php
```
#### <a name="33"> Asignar nivel de juego a usuario</a>
Petición: **POST**
Descripción: Este servicio asignará la misión del juego al usuario
Datos de entrada:  **usuario_fk (INT), juego_nivel_fk (INT), status_nivel(INT)**
Datos de salida: 1 success

#### <a name="34"> Actualizar o Modificar la asignación de misión del juego al usuario</a>
Petición: **POST**
Descripción: Este servicio actualiza la asignación de la misión del juego que tiene el usuario, se requiere de la id para la modificación
Datos de entrada: **id (INT), user (INT), juego_lvl(INT), status(INT)**
Datos de salida: 1 success

#### <a name="35"> Eliminar asignación de misión de usuario</a>
Petición: **POST**
descripción: Este servicio elimina la asignación de misión del juego al usuario
Datos de entrada: ** id_e (INT)**
Datos de salida: 1 success

#### <a name="36"> Consulta las misiones del usuario </a>
Petición: **GET**
Descripción: Este servicio muestra todos los registros de las asignaciones de misión que tiene el juego al usuario, si se agrega un parámetro para buscar un dato especifico solo mostrara ese dato.
Datos de entrada: ** id_usuario (INT)**
Datos de salida:
- Muestra todos los registros de la tabla
- Muestra el registro de la tabla por id de misión

[Regresar al Índice](#0)
* * *
## Juegos a Colección
```diff
- Este registro requiere que existan datos en Juegos y Colección.
```
```
http://sandbox.arvispace.com/arvisgameAPI/juegos_colecciones.php
```
#### <a name="37"> Asignar juego a colección</a>
Petición: **POST**
Descripción: Este servicio asignará la misión del juego al usuario
Datos de entrada:  **coleccion_insert (INT), juego_insert (INT)**
Datos de salida: 1 success

#### <a name="38"> Actualizar o Modificar la asignación de juego a colección</a>
Petición: **POST**
Descripción: Este servicio actualiza la asignación de la misión del juego que tiene el usuario, se requiere de la id para la modificación
Datos de entrada: **id_update (INT), juego_update (INT), coleccion_update(INT)**
Datos de salida: 1 success

#### <a name="39"> Eliminar asignación de juego de colección</a>
Petición: **POST**
Descripción: Este servicio elimina la asignación de misión del juego al usuario
Datos de entrada: ** id_delete (INT)**
Datos de salida: 1 success

#### <a name="40"> Consulta los juegos asignados a colección </a>
Petición: **GET**
Descripción: Este servicio muestra todos los registros de las asignaciones de juegos a colección, si se agrega un parámetro para buscar un dato especifico solo mostrara ese dato.
Datos de entrada: ** id_juegos_colecciones_read (INT)**
Datos de salida:
- Muestra todos los registros de la tabla
- Muestra el registro de la tabla por id

[Regresar al Índice](#0)
* * *
## Productos de los juegos
```diff
- Este registro requiere que existan productos y juegos
```
```
http://sandbox.arvispace.com/arvisgameAPI/juego_producto.php
```
#### <a name="41"> Asignar Productos a juego</a>
Petición: **POST**
Descripción: Este servicio asignará el producto al juego
Datos de entrada:  **id_productofk (INT), id_juegofk (INT)**
Datos de salida: 1 success

#### <a name="42"> Actualizar o Modificar la asignación de Productos a juego</a>
Petición: **POST**
Descripción: Este servicio actualiza la asignación del producto que tiene el juego, se requiere de la id para la modificación
Datos de entrada: **id (INT), id_product (INT), id_game(INT)**
Datos de salida: 1 success

#### <a name="43"> Eliminar asignación de Productos a juego</a>
Petición: **POST**
Descripción: Este servicio elimina la asignación de producto al juego
Datos de entrada: ** id_e (INT)**
Datos de salida: 1 success

#### <a name="44"> Consulta las asignaciones de los Productos del juego </a>
Petición: **GET**
descripción: Este servicio muestra todos los registros de las asignaciones que de productos que tiene el juego, si se agrega un parámetro para buscar un dato especifico solo mostrara ese dato.
Datos de entrada: ** id_juego_producto (INT)**
Datos de salida:
- Muestra todos los registros de la tabla
- Muestra el registro de la tabla por id

[Regresar al Índice](#0)
* * *
