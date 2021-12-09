### Funcion CONCAT
La funcion concat recibe 2 arguentos CONCAT (x,y), el resultado va a ser la concatenación de las cadenas.
```SQL
Select concat('Esta es una cadena','esta es otra cadena')from dual;
```

```SQL
Select concat(concat('uno',' dos'),' tres') from dual;
```

```SQL
Select concat(concat(first_name,' '),last_name) employee_name, first_name || ' ' || last_name AS Employee_name_2 from employees where department_id=30;
```

### Función SUSBTR
Devuelve una subcadeba de una cadena mas grande SUBSTR(cadena,numero x[, posicion]

```SQL
SELECT SUBSTR('CADENA MUY LARGA DE EJEMPLO', 10) FROM DUAL;
```
```SQL
SELECT SUBSTR('CADENA MUY LARGA DE EJEMPLO', 10, 7) FROM DUAL;
```
```SQL
SELECT SUBSTR(10000-8, 3, 2) FROM DUAL;
```
```SQL
SELECT SUBSTR(SYSDATE, 4, 3) FROM DUAL;
```
```SQL
SELECT 'NOMBRE: ' || SUBSTR(first_name, 1, 1)  || '. ' last_name "Nombre"FROM Employees where SUBSTR(job_id,1,2 = 'AD');SELECT 'NOMBRE: ' || SUBSTR(first_name, 1, 1)  || '. ' || last_name "Nombre" FROM Employees where SUBSTR(job_id,1,2) = 'AD';
```
Mostrando los nombres de los datafiles apartir de una cadena completa con ruta del archivo
```SQL
Select SUBSTR(file_name, INSTR(file_name, '\', -1)+1) FROM dba_data_files;
```
### Funcion INSTR
Nos permite encontrar un caracter dentro de una cadena, ademas  nos es posible indicar un inicio de busqueda y que numero de ocurrencia queremos encontrar, basicamente esta funcion nos devuelve un numero.

```SQL
SELECT INSTR('Hola mundo', 'mu') FROM DUAL;
```
```SQL
SELECT * FROM departments where INSTR(department_name, 'on') = 2;
```

### Funcion LENGTH