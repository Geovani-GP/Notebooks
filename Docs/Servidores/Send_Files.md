# Enviar/Copiar archivos a través de SSH con SCP
SCP hace uso de SSH (Secure Shell) para hacer copias seguras y encriptadas.

## Uso de SCP
Tenemos que tener claros los parámetros de los que consta la instrucción:


- Usuario: el nombre de usuarios que utilicemos en el servidor.
- Host: dirección IP o dominio del servidor remoto.
- Archivo origen: ruta del archivo que queremos copiar.
- Directorio origen: ruta del directorio completo que queremos copiar.
- Directorio destino: ruta donde queremos copiar el archivo.


## COPIAR ARCHIVOS DE LOCAL A SERVIDOR
Si queremos subir el archivo archivo.txt de nuestro ordenador a la carpeta /home/usuario del servidor, hacemos lo siguiente:

```
$ scp archivo.txt usuario@dominio.com:/home/usuario
```

## COPIAR ARCHIVOS DE SERVIDOR A LOCAL
Si queremos copiar el fichero archivo.txt del servidor a nuestro ordenador en la carpeta Documentos, hacemos lo siguiente:

```
$ scp usuario@dominio.com:/home/usuario/archivo.txt Documentos
```

## COPIAR ARCHIVOS DE SERVIDOR A SERVIDOR
Para copiar un archivo de un servidor a otro, hacemos lo siguiente:

```
$ scp usuario1@dominio1.com:/home/usuario1/archivo.txt usuario2@dominio2.com:/home/usuario2/
```

## COPIAR UN DIRECTORIO COMPLETO
Para copiar un directorio completo de mi ordenador al servidor, por ejemplo /home/mario/carpeta a /home/usuario, añadimos un -r en el comando:
```
$ scp -r /home/mario/carpeta usuario@dominio.com:/home/usuario
```
## LIMITAR EL ANCHO DE BANDA
Para no sobrecargar demasiado el servidor, es posible limitar el ancho de banda de la transferencia. Con el parámetro -l podemos indicar la velocidad (en Kbps).

```
$ scp -l limite usuario@dominio.com:/home/usuario/archivo.txt Documentos
```
