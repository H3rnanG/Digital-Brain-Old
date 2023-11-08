#EngineeringSoftware

*Documentacion completa:* https://www.w3schools.com/sql/sql_backup_db.asp
## Conceptos Basicos
#### Que es Sql?
SQL (Structured Query Language) es un lenguaje de programación diseñado para administrar y manipular bases de datos relacionales. Se utiliza para comunicarse con sistemas de gestión de bases de datos (SGBD) y realizar diversas operaciones en los datos almacenados en ellas.

SQL permite realizar tareas como crear y modificar estructuras de bases de datos, insertar, actualizar y eliminar datos, así como realizar consultas para recuperar información específica de una base de datos. Es ampliamente utilizado en aplicaciones y sistemas que manejan grandes volúmenes de datos, como sistemas de gestión empresarial, sistemas de administración de contenido, sistemas de comercio electrónico y muchos otros.

El lenguaje SQL consta de una serie de comandos y cláusulas que se combinan para formar instrucciones. Algunos comandos comunes de SQL incluyen SELECT (para recuperar datos de una tabla), INSERT (para insertar nuevos datos en una tabla), UPDATE (para actualizar los datos existentes en una tabla) y DELETE (para eliminar datos de una tabla).

SQL es un estándar de facto en el manejo de bases de datos relacionales y es compatible con la mayoría de los sistemas de gestión de bases de datos, como MySQL, Oracle, Microsoft SQL Server, PostgreSQL, SQLite, entre otros.
- - - 
## Sql Basico
#### Crear una Base de Datos:
Para crear una Base de Datos utilizamos la palabra reservada *`CREATE`*
```mysql
CREATE DATABASE Nombre_Data_Base
```

---
#### Eliminar una Base de Datos:
Para descargar una Base de Datos utilizamos la palabra reservada *`DROP`*
```mysql
DROP DATABASE Nombre_Data_Base
```

---
#### Crear una copia de seguridad completa de la Base de Datos:
Para crear una copia de seguridad de una Base de Datos utilizamos la palabra reservada *`BACKUP`*
```mysql
BACKUP DATABASE Nombre_Data_Base
TO DISK = 'filepath'
```

---
#### Crear una Tabla
Para crear una tabla utilizamos la palabra reservada *`CREATE`* 
```mysql
CREATE TABLE nombre_tabla (
	column1 datatype,
	column2 datatype,
	column3 datatype,
)

# Ejemplo
CREATE TABLE Persons (  
    PersonID int,  
    LastName varchar(255),  
    FirstName varchar(255),  
    Address varchar(255),  
    City varchar(255)  
);
```

##### Crear una tabla a partir de una tabla ya existente
Usamos la siguiente sintaxis:
```mysql
CREATE TABLE nueva_nombre_tabla AS  
    SELECT column1, column2,..._  
    FROM existente_nombre_tabla  
    WHERE ....;
```

---
#### Eliminar una Tabla
Para eliminar una tabla utilizamos la palabra reservada *`DROP`*
```mysql
DROP TABLE nombre_tabla;
```

##### Truncar una Tabla
Para eliminar los datos de una tabla pero no la tabla en si usamos la palabra reservada *`TRUNCATE`*
```MySQL
TRUNCATE TABLE nombre_tabla;
```

---
#### 