Pequeños consejos para sobrevivir en Vim
Para insertar texto (y estar en el modo de inserción): pulse 'i' y modifique el texto. Para volver al modo de comando pulse la tecla "ESC".

Para guardar el texto (En el modo de comandos): presione ': w'

To quit vim (in command mode): press ':q'

To quit vim without saving (in command mode): press ':q!'

To delete the line where the cursor is (in command mode): press 'dd'

El resaltado de sintaxis
Vim soporta resaltado de sintaxis. Para activarlo se abren

/etc/vim/vimrc

y elimine la línea


"Vim 5 y versiones posteriores son compatibles con resaltado de sintaxis. Uncommenting la siguiente
"Línea permite resaltado de sintaxis por defecto.
syntax on 
Otros editores de texto

