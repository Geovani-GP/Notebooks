## Servicios Superhouse

# Productos - Promociones
GET Muestra los productos de las promociones
https://superhouse.mx/getpromoindividual.php
error: , success:data

# Bodegas
GET Busca Bodegas por codigo postal, recibe 1 parametro CP(string)
https://superhouse.mx/busqueda_mibodega_cp1.php?
error: , success: numero

# Categorias
POST Obtiene el numero de bodega a partir del resultado de la busqueda de bodegas, recibe un parametro idbod(1) tipo numerico
https://superhouse.mx/getcategoria.php
error: ,  success: data

# Total de productos por sub-categoria
GET Muestra el total de productos de una categoria, recibe 1 parametro cate(1) de tipo numerico   ////
http://superhouse.mx/buscanumpro05.php?cate=18
error: , success: data 

# Busca sub-categorias y pagina
GET Buscar Productos por numero de categoria y numero de pagina, recibe 2 parametros cate(1) pag(1) de tipo numericos ////
http://superhouse.mx/buscacate02.php?cate=1&pag=1
error: 198, success: data

# Promotor
GET Verifica que el codigo sea correcto, recibe 1 parametro promotor(6A78F6BE46)   ////
http://superhouse.mx/vericodpromo2.php?promotor=6A78F6BE46
error:201, success: data

# Iniciar Sesion
GET Inicia Sesion, recibe 2 parametros user=(email), pass=(string) ////
http://superhouse.mx/getlogin2.php?user=asdqweasd&pass=asdqweasdqwe
error: 198, success: data

-- mail: sotoarmando781@gmail.com
-- pass: a

# Registro de Usuario
GET Registra usuario
http://superhouse.mx/registrouser2.php   ////
error: 2 ningun dato       , error, 1 correo registrado        success: data

# Buscar Productos
GET busca productos, recibe dos parametros (busq , pag), se le asina la pagina por default 1
http://superhouse.mx/busquedash.php   ////
error:                        success:data

# Muestra el totoal de productos al buscar
Get retorna el numero de productos encontrados para paginar, recibe un parametro de busqueda (busq)
http://superhouse.mx/buscanumpro2sh.php     ////
error:                       success: numero