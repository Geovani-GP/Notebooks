# VIM
Vim soporta resaltado de sintaxis. Para activarlo se abren

/etc/vim/vimrc

Mostrar ñ y acentos:
al final del archivo vimrc, Agregamos estas lineas y lo guardamos

Al archivo /etc/vimrc, Agregamos estas lineas al final del mismo. y lo guardamos.

set fileencodings=utf-8,ucs-bom,gb18030,gbk,gb2312,cp936
set termencoding=utf-8
set encoding=utf-8


## Lista de comandos VIM
### Modos de Vim
La Clave para aprender a manejar VIM es acostumbrarse a sus distintos modos de funcionamiento. Esta es la parte que hace a VIM especial y dificil de entender para las personas que se inician.

vim archivo.txt  => Cuando abrimos un archivo para editar con VIM, se inicia el modo comando

:i => El modo inseción nos sirve cuando queremos editar el texto del archivo, añadiendo nuevo contenido del con el teclad, o borrando caracter a caracter con las teclas (Retroceso/Supr). Para salir del modo inserción y volver al modo comando pulsamos la tecla escape ESC.


### Opciones de archivo


#### Modo Inserción
:w => Permite guardar el fichero.

:q => Salir de vim. Si el fichero ha sido modificado pero no se ha guardado, nos advertira y no podremos salir de Vim usando este comando.

:q! Salir del archivo sin guardar 
:wq => Hace el guardado del archivo y después sale de VIM.

#### Modo Comando
u => Deshacer acción
Ctrl+r => Rehacer una acción


### Movimiento dentro del editor

Además dee usar los cursores para movernos por el archivo, podemos movernos de una menra más rápida con algunos comandos:

k => arriba

j => abajo

l => derecha

h => izquierda

gg => Ponerse al inicio del fichero.

Shift+g => Ir a la última línea del fichero.

Num+G => ir a una linea determinada. Por ejemplo 14G llevaría el cursor a la línea 14; : set number => hace que el editor muestre el número de lineas.

$ => Ir al final de la linea.

0 => Ir al principio de la línea


### Edición


dd => El comando permite borrar la linea actual, donde está el cursor.

d+num => Permite borrar un número de líneas. Por ejemplo, d3 borrará tres líneas.



## Comandos para eliminar textos

x => Elimina el caracter

dw => Elimina la palabra en donde esta el cursor

db => elimina la palabra atras del cursor

dd => Elimina la linea

d$ => Elimina hasta el final de la linea

d^ (d caret, not CTRL d) => Elimina desde el inicio de la linea


### Buscar

Vim tiene unas herramientas muy potentes para buscar texto en los archivos. Los comandos más utiles son los siguientes:


/+texto => al pulsar <</>> se abre la funcion de búsqueda. Entonces podremos escribir el texto que queriamos buscar. El editor resaltará todas las apariciones de este texto. Pulsamos enter y nos llevará a la siguiente aparición de la búsqueda. con respecto a la posicion de nuestro cursor.

n y N => Una vez hemos aceptado una búsqueda, el comando **n** nos lleva a la siguiente aparicion de la cadena buscada. el comando **N** nos llevará a la anterior


### Otras ayudas
:h => Abre la ayuda principal de VIM. Esto hace que nuestra ventana de terminal se divida en dos editores. En este momento nuestro cursor estará en el texto del archivo de ayuda de vim.
Podremos leer el fichero y utilizar las funciones de búsqueda comentadas con anterioridad.
cuando queramos salir tenemos que hacerlo como cualquier otro fichero. usando el comando correspondiente de VIM, por ejemplo :q.



"Vim 5 y versiones posteriores son compatibles con resaltado de sintaxis. Uncommenting la siguiente
"Línea permite resaltado de sintaxis por defecto.
syntax on 
Otros editores de texto

### Comandos de utilidad

:set hls! => Activa/desactiva el resaltado de sintaxis

:set nu! => activa/desactiva la numeracion de filas

:set ai! => activa el autoidentado

:set spell => activa correccion ortografica

z=  => sigerir corrección

:diffupdate => modo diferencias

:compiler php => modo compilador

:syn on => sintaxis automatica
