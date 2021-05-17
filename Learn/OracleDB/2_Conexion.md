# Oracle

## Despues de la instalación.
En consola escribir 
```
sqlplus
```

## Las credenciales para iniciar son las siguientes:
```
user-name: sys as sysdba
password: el que se indicó en la instalación
```

Ingresamos el comando:
```
show user;
```
nos mostrará 
`
USER is "SYS"
`

Nota: Tenemos que desbloquear la cuenta para el usuario HR, que vamos a usar para los ejemplos SQL.

## Desbloquear cuenta.

ejecutamos el siguiente comando:
```
ALTER USER hr IDENTIFY BY hr ACCOUNT UNLOCK; <- este ultimo (hr) es la contraseña que va a tener, podemos cambiarla por la que nosotros deseemos.
```

Para revisar que la cuenta este desbloqueada vamos a desconectarnos.

## Conectar y desconectar
Para conectar a un usuario se usa
```
connect
```
```
disconnect
```

## conectamos HR
Escribimos:
```dos
connect
Enter user-name:hr
Enter password:
Connected.
SQL> show user; <- consulta de prueba
```
`
USER is "HR"
`


comando para limpiar pantalla:

```
host cls
```

Mostramos los datos de la tabla paises.
```sql
SQL> SELECT * FROM countries;
```
