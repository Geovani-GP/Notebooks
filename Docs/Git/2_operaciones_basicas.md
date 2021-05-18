# Creando un repositorio local.
Es tan sencillo como irse a un directorio de nuestra máquina desde la linea de comandos o dsde Git Bash, si estas en Windows. Empezamos con un directorio vacío, ya que se supone que estamos comezando nuestro proyecto y entonces podemos ejecutar el comando:

```cmd
git init
```

A partir  de ese momento tienes todo un repositorio de software completo en tu máquina del proyecto que tenías en ese diretorio. Puedes crear los archivos que quieras en el directorio(tu proyecto) y luego puedes enviarlos al repositorio haiendo un "commit".

# Añadir ficheros al repositorio
Antes de enviar cambios al repositorio, lo que se conoce como hacer commit, tienes que enviar
los ficheros a un área intermedia llamada "staging area" en donde se almacenan los archivos
que serían actualizados en el próximo commit. Éste es uno de los conceptos esenciales para
aprender Git y para mandar los ficheros a este área tenemos que añadirlos al repositorio.

```
git add nombre-del-fichero
```

Una vez añadido podrías ver que realmente tienes ese fichero en el "staging area", mediante el
comando "status".
git status
Verás que, entre las cosas que te aparecen como salida de ese comando, te dice que tienes tu
fichero añadido como "new file". Además te dice que estos cambios están preparados para
hacer commit.

En consideración "git add ." permite enviar todos los cambios en el working directory, incluyendo archivos nuevos y archivos que hayan sido modificados.
Una vez añadidos los archivos al staging area, ahora podremos hacer el commit sobre esos
ficheros.

```
git commit -m "este es mi primer commit"
```

Con esto ya tenemos nuestro primer archivo dentro del repositorio. A partir de aquí podremos
mantener y controlar los cambios que se hagan sobre este archivo (u otros que hayamos
incluido por medio del commit).

Si haces de nuevo un comando "git status" podrás comprobar que no hay nada para enviar al
repositorio. Eso quiere decir que la zona de Index está limpia y que todos los cambios están
enviados a Git.

*Información importante de Ramas: La rama principal, que se crea al iniciarse el repositorio; se llama "master". *

Cada vez que se modifica un fichero, se tiene que agregar al área intermedia con el comando
"add" y luego hacer el commit para que se actualice el repositorio con los archivos nuevos o
actualizados. Eso significa que en teoría cada vez que cambias un archivo tendrías que añadirlo
al Staging area para poder hacer el commit, aunque más adelante veremos que hay maneras de
automatizar las tareas un poco más y, mediante atajos, poder resumir el paso de hacer el "add"
cuando se ha cambiado el código de un fichero.

# Deshacer cambios
En cualquier momento puedo deshacer cambios que haya realizado en los archivos,
recuperando versiones anteriores que podamos tener en el repositorio. Podría descartar los
cambios que tengo en staging area.

```
git checkout -- nombre_fichero
```

En Git puedes tener código principalmente en tres lugares, el directorio de trabajo, en el
Staging area o en una versión que tengas en un commit antiguo de ese repositorio. Existen
diferentes comandos para hacer todas estas cosas, dependiendo del lugar de Git donde tengas
el código que quieres recuperar. Pero lo verdaderamente útil y potente que tenemos con el
control de versiones es poder recuperar archivos realizados commit anteriores, en el último
commit, pero también en otros que tengas más antiguos.
