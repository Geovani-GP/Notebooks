# ¿Que es GIT?
Git es un sistema extremadamente útil, pero resulta muy confuso cuando uno está iniciando.
Los sistema de control de versiones son programas que tienen como objetivo controlar los cambios en el desarollo de cualquier tipo de software, permitiendo conocer el estado actual de un proyecto, los cambios que se han realizado a cualquiera de sus partes, las personas que intervinieron, etc.

# Instalación Git
Tener Git instalado en local es condición indispensable para trabajar con el sistema de control
de versiones. El proceso para instalar Git es bien sencillo porque no difiere de la instalación de
cualquier otro software que hayas hecho

Si lo instalas en la propia consola del Windows, la única ventaja es que lo tendrás disponible
desde la ventana de línea de comandos de Windows y podrás hacer desde allí los comandos de
Git. Si lo instalas solo en Git Bash no habrá más problemas, solo que cuando quieras usar Git
tendrás que abrir la consola específica de Git que ellos llaman "git bash".
La manera más sencilla de saber si Git está instalado en tu sistema es a través del comando:

```
git version
```

Esto te mostrará en la pantalla el número de la versión de Git que tengas instalada. Si en
Windows instalaste Git en consola (la ventana de línea de comandos), observarás que en
cualquier consola de comandos de Windows tienes disponible Git. Si lo instalaste únicamente
en el Git Bash, no tendrás ese comando y Git no está disponible desde la consola de Windows.
Git Bash es la línea de comandos de Git para Windows, que además te permite lanzar
comandos de Linux básicos, "ls -l" para listar archivos, "mkdir" para crear directorios, etc. Es
la opción más común para usar Git en Windows.

Es indiferente si instalas Git en la línea de comandos del Windows o si lo instalas solamente en
el Git Bash. Simplemente escoge la que te sea más cómoda.

Descargar git en su ultima version desde el siguiente enlace https://git-scm.com/downloads.

# Primera configuración de Git, primers comandos que debes lanzar.
Antes que nada, inmediatamente después de instalar Git, lo primero que deberías hacer es
lanzar un par de comandos de configuración.

```
git config global user.name "Tu nombre aquí"
git config global user.email "tu_email_aquí@example.com"
```

Con estos comandos indicas tu nombre de usuario (usas tu nombre y apellidos generalmente) y
el email. Esta configuración sirve para que cuando hagas commits en el repositorio local, éstos
se almacenen con la referencia a ti mismo, meramente informativa. Gracias a ello, más
adelante cuando obtengas información de los cambios realizados en el los archivos del "repo"
local, te va a aparecer como responsable de esos cambios a este usuario y correo que has
indicado.
