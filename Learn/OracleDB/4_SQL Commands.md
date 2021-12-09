### DESCRIBE
La descripción de tablas, vistas, tipos y sinónimos contiene la siguiente información:

* El nombre de cada columna
* Si se permiten o no valores nulos (NULL o NOT NULL) para cada columna
* Datatype de columnas,porejemplo,CHAR,DATE,LONG, LONGRAW, NUMBER, RAW,ROWID,VARCHAR2 (VARCHAR) o XMLType
* Precisión de columnas (y escala, si la hubiera, para una columna numérica)

```sql
Describe jobs;
```
```sql
Desc jobs;
```

### SELECT
La instrucción Oracle SELECT se utiliza para recuperar registros de una o más tablas de una base de datos Oracle.

```sql
Select department_id as "id Departamento" from employees;
```


### DISTINCT
La cláusula se utiliza en una instrucción para filtrar filas duplicadas en el conjunto de resultados. Garantiza que las filas devueltas sean únicas para la columna o columnas especificadas en la cláusula.DISTINCTSELECTSELECT.

```sql
Select DISTINCT department_id as "id Departamento" from eployees;
```

### TABLA DUAL
Es una tabla creada automáticamente por Oracle Database junto con el diccionario de datos. está en el esquema del usuario, pero es accesible por el nombre para todos los usuarios. Tiene una columna, , definida como , y contiene una fila con un valor . Seleccionar de la tabla es útil para calcular una expresión constante con la instrucción. Debido a que solo tiene una fila, la constante se devuelve solo una vez. Como alternativa, puede seleccionar una constante, pseudocolumna o expresión de cualquier tabla, pero el valor se devolverá tantas veces como haya filas en la tabla.
```sql
Select 3 * 4 from dual;
--------------------------------
12
```

```sql
Select 'Hola mundo' from dual;
```

Fecha del sistema Sysdate
```sql
Select Sysdate from dual;
```

Concatenación ||
```sql
Select 'Esta es una cadena' || ' ' || 'otra cadena de prueba' from dual;
```

```sql
Select ('Usuario: ' || USER || '. el dia de hoy es: ' || SYSDATE) AS "Encabezado" from dual;
```

### WHERE & FILTROS

Diferente <>, !=, ^=
Menor que <, <=
Mayor que >, >=

```sql
Select first_name || ' ' || last_name "NAME", commission_pct FROM Employees where commission_pct != 0.35;
```

IN definen valores

```sql
SELECT first_name || ' ' || last_name "NAME", department_id FROM employees where department_id IN (10,20,50); 
```
WHERE NOT invierte la busqyeda

```sql
Select first_name, department_id FROm employees where not (department_id >=30);
```
AND
```sql
Select first_name, last_name from employees where first_name = 'Smith'  and salary > 7500;
```

OR
```sql
Select first_name, last_name from employees where first_name = 'Kelly' OR last_name = 'Smith';
```

BETWEEN
```sql
Select first_name, last_name from employees where salary BETWEEN 5000 and 6000;
```

LIKE
```sql
Select first_name, last_name from employees where first_name LIKE 'Su%';
```

```sql
Select first_name, last_name from employees where first_name LIKE '%o';
```

% comodin, reemplaza 0 o mas caracteres

```sql
Select first_name, last_name from employees where first_name LIKE 'C%a';
```
```sql
Select first_name, last_name from employees where first_name LIKE '%m%';
```

ORDER BY

```sql
Select last_name FROM employees ORDER BY last_name DESC, first_name ASC;
```
```sql
Select first_name, hire_date, salary, manager_id mid FROM employees WHERE department_id IN (110,100) ORDER BY 4,2,3;
```
```sql
Select last_name, commission_pct FROM employees WHERE last_name LIKE 'R%' ORDER BY commission_pct ASC, last_name DESC;
```

