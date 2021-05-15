# Crear archivo XML desde Base de Datos Oracle

## 1. Crear Topologias

### Oracle Data Base
En esta etapa creamos una conexión de datos.
```text
Topologia/Arquitectura fisica/Oracle
```
click secundario/Nuevo Servidor de Datos  con los siguientes datos
```text
Nombre: Nombre que va a tener la conexion (Informátiva)
Instancia/Enlace  de Base de Datos (Servidor de datos): Nombre de la instancia (Informátiva)

Conexion
    Usuario: ejemplo HR
    Contraseña: ejemplo HR
```
En la conexión JDBC 
```text
jdbc:oracle:thin:@localhost:1521/xe
```
Ejecutamos una prueba de conexión.

A continuación click secundario en la conexión y seleccionamos "Nuevo esquema Fisico".

Colocamos la siguiente información.

```text
Nombre: este nombre se selecciona al escojer los 2 esquemas siguientes, deben coincidir en nombre
Esquema: HR
Esquema de trabajo: HR
```
Posteriormente nos dirigimos a la parte inferior de Arquitectura Logica que va a tener reerencia a la Arquitectura fisica.

Seleccionamos Arquitectura Logica/Oracle/Nuevo Esquema Lógico, con la siguiente información:

```text
Nombre: ejemplo HR_L
Conexto: Globa, Esquema Fisico: Referencia a Esquema fisico.
```
### Archivo XML

Topologia/Aqurquitectura Fisica/XML/Nuevo serividor de datos
```Text
Nombre: ejemplo Employee_XML
```
En JDBC la siguiente configuración.
```Text
ControladorJDBC y JDBCURL lo dejamos por default

Propiedades:
    Propiedades de XML
        drop_on_disconnect: true
        dtd: ubicación de la plantilla/estructura que tendrá el documento xml
        file: ubicación del documento xml
        root_elt:employees <- nombre de la estructura(supongamos nombre de la base de datos)
        schema:XMLS <- nombre por el que lo identificaremos en la arquitectura Logica

```

A continuación se muestra una ejemplo de los documentos DTD y XML

Archivo EmployesX.xsd
```xml
<?xml version="1.0" encoding="windows-1252" ?>
<schema xmlns="http://www.w3.org/2001/XMLSchema" elementFormDefault="qualified">
	<element name="employees">
		<complexType>
			<sequence>
				<element name="employee" maxOccurs="unbounded">
					<complexType>
						<sequence>
							<element name="firstname" type="string"/>
							<element name="lastname" type="string"/>
							<element name="email" type="string"/>
						</sequence>
					</complexType>
				</element>
			</sequence>
		</complexType>
	</element>
</schema>
```
Archivo EmployesXL.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<employees>
	<employee>
		<firstname>Ellen</firstname>
		<lastname>Abel</lastname>
		<email>EABEL</email>
	</employee>
</employees>
```

En la arquitectura Lógica seleccionamos XML click secundario nuevo esquema lógico, con los siguientes datos:

```text
Nombre: ejemplo XMLS
Contexto: Global | Esquemas Físicos: EmployeX_XMLS:XMLS
```
## 2. Crear Modelos

## 3. Crear Proyecto

