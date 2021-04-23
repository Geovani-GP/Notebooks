# Git

## Ramas (Branch)

En eld ia a dia del trabajo con git una de las cosas útiles que podemos hacer es trabajar con ramas. las ramas son caminos que puede tomar el desarrollo de un sofware, algo que ocurre naturalmente para resolver problemas o crear unas nuevas funcionalidades.


El comando git branch es el que se usa principalmente para trabajar con la creación de ramas, borrado de ramas y demas. Sin embargo no es el único comando para la operativa que veremos en este articulo, ya que existen otros subcomandos de Git utiles y necesarios para trabajar con ramas, como checkiut para moverse entre ramas o merge para fusionar ramas.

```
	git branch
```

Este comando nos da´ra el listado de las ramas que tengamos en un proyecto. pero hay que advertir qeu las ramas de un repositorio local puede ser distinta a las ramas de un repositorio remoto. por ejemplo, cuando clonas un repositorio de GitHub generalmente estás clonando únicamente la rama maste y no todas las ramas que se hayan creado a lo largo del tiempo.


## La rama Master o main

Cuando inicializamos un proyecto con Git automáticamente nos encontramos en una rama a la que se denomina "master" o "main".

***Puedes ver las ramas en la que te encuentras*** en cada instante con el comando

```
		git branch
```

Esta rama es la principal de tu proyecto y apartir de la que podrás crear nuevas ramas cuando lo necesites.

```
nota: Si has hecho algún commit en tu repositorio observaras que después de lanzar el comando "git branch" nos informa el nombre de la rama como "master" y si no has hecho un commit en tu proyecto observaras que no se ha creado todavía ninguna rama y que el comando branch no produce ninguna salida.
```

## Crear una rama nueva

El procedimiento para crear una nueva rama es bien simple. Usando el comando branch, seguido del nombre de la rama que queremos crear.

```
git branch nombredelarama
```

Este comando en sí no produce ninguna salida, pero podrías ver las "branches" de un proyecto con el comando "git branch", u obtener una descripción más detallada de las ramas con este otro comando:

```
git show-branch
```

Esto nos muestra todas las ramas del proyecto con sus commits realizados.

## Pasar de una rama a otra

Para moverse entre ramas usamos el comando "git checkout" seguido del nombre de la rama que queremos que sea activa.

```
git checkout nombredelarama
```

Esta sencilla operacion tiene mucha potencia, porque nos cambiara automáticamente todos los archivos de nuestro proyecto, los de todas las carpetas, para que tengan el contenido en el que se encuentren en la correspondiente rama.

El commando chechout tiene la posibilidad de permitirte crear una rama nueva y moverte a ella en un único paso. Para crear una nueva rama y situarte sobre ella tendrás que darle un nombre y usar el parámetro -b.

```
git checkout -b otrarama
```

Como salida obtendrás el mensaje Switched to a nuew branch 'otrarama '. Esto quiere decir que. además de crear la rama, nuestra cabecera está apuntando hacia esta nueva branch.

## Fusionar ramas

A medida que crees ramas y cambies el estado de las carpetas o archivos tu proyecto empezará a divergir de una rama a otra. Llegará el momento en el que te interese fusionar ramas para poder incorporar el trabajo realizado a la rama master.

El proceso fusionado se conoce como "merge" y puede llegar a ser muy simple o más complejo si se encuentra cambios que Git no pueda procesar de una manera automática. Git para procesar los merge usa un antecesor común y comprueba los cambios que han  introducido al proyecto desde entonces, combinando el código de ambas ramas.

Para hacer un merge nos situamos en una rama, en este caso "master" o "main", y decimos con qué otra rama se debe fusionar el codigo.

El siguiente comando, lanzado desde la rama "master", permite fusionarla con al rama "otrarama"

```
git merge otrarama
```

un merge necesita un mensaje, igual que ocurre con los commit.

```
git merge experimental -m "Esto es un merge con mensaje
```

Luego podremos comprobar que nuestra rama master tiene todo el código nuevo de la rama experimental y podemos hacer nuevos commits en master para seguir el desarrollod e nuestro proyecto ya con la rama principal, si es nuestro deseo.

## Fusionar los cambios de master en la rama en desarrollo

Durante tu trabajo en el desarrollo del proyecto gestionado con GIt también puede ser normal que se vayan haciendo cambios en la rama master, o en otras ramas en desarrollo, y quieras traerlos para tu rama actual. Por ejemplo, la rama experimental está tardando varios días o semanas en completarse y mientras tanto han agregado nuevas features que quieras que este disponibles tambien en la rama otrarama.

Entonces seguramente querrás traerte los cambios de la rama master. Para ello, estamos en la rama experimental, puedes lanzar el siguiente comando.

```
git merge master -m "un mensaje del merge de master en el branch otrarama"
```

Ya lo tienes! ahora tu rama está actualizada con todos los cambios en master. Puedes seguir dearrollando tu rama experimental sabiendo que tienes el proyecto actualizado.

## Subir rama al repositorio remoto (Github o similares).

Como  habíamos dicho anteriormente, por mucho que hagas la operativa descrita para crear ramas en tu ordenador, y las puedas ver en tu repositorio local con git branch, las ramas no se publicarán en Github o cualquer otro hosting de repositorios remoto.
Para que esto ocurra tienes que realizar especícamente la accion de subir una rama determinada.

La operativa de publicar una rama en remoto la haces mediante el comando push, indicando la opcion "-u" y el nombre de la rama que deseas subir. Por ejemplo:

```
git push -u origin nuevarama
```

Si estamos haciendo un push, empujando hacia origin o master (que son os nombres que suele dar al repositorio remoto), la rama con nombre "nuevarama".

Por cierto, si subimos el proyecto a Github podemos ver tambien un diagrama de las ramas que hemos ido creando y fusionar a master, en la seccion Graps/Network.

## Borrar una rama

En ocasiones puede ser necesario eliminar una rama del repositorio, por ejemplo porque nos ayamos equivocado en el nombre al crearla. Aquí la operativa puede ser diferente, dependiendo de si hemos subido ya esa rama a remoto o si todavía solamente está en local.

## Borrado de la rama local

Esto lo conseguimos con el comando git branch, solamente que ahora usaremos la opcion "-d" para indicar que esa rama queremos borrarla.

```
git branch -d rama_a_borrar
```

Sin embargo, puede que esta acción no nos funcione porque hayamos hecho cambios que no se hayan salvado en el repositorio remoto, o no se haya fusionado con otras ramas. En el caso de queramos forzar el borrado de la rama, para eliminarla independientemente de si se ha hecho el push o el merge, tendrás que isar la opcion "-D".

```
git branch -D rama_a_borrar
```
Debes prestar especial atención a esta opción "-D", ya que al eliminar de este modo pueden haber cambios que ya no se puedan recuperar. Como puedes apreciar, es bastante fácil de confundir con "-d", opción más segura, ya que no permite borrado de ramas en situaciones donde se pueda perder código.

## Eliminar un Branch en remoto

Si la rama que queremos eliminar está en el repositiorio remoto, la operativa es un poco diferente. Temenos que hacer un push, indicando la opcion --delete, seguida de la rama que se desea borrar.

```
git push origin --delete rama_a_borrar
```
