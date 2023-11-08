#EngineeringSoftware
# Conceptos Básicos:
## Que es Maven?
[Apache Maven](https://maven.apache.org/) es una potente herramienta de gestión de proyectos que se utiliza para gestión de dependencias, como herramienta de compilación e incluso como herramienta de documentación. Es de código abierto y gratuita.
## Que es JPA?
JPA significa **"Java Persistence API" (API de Persistencia de Java)** y es una especificación estándar de Java para la gestión de la persistencia de datos en aplicaciones Java. La JPA permite a los desarrolladores trabajar con datos persistentes en bases de datos relacionales de una manera más orientada a objetos, abstracta y portátil.

En lugar de escribir consultas SQL directamente para interactuar con la base de datos, los desarrolladores pueden utilizar JPA para representar las relaciones entre objetos y tablas en la base de datos en forma de entidades y realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar) en estas entidades de manera más natural y legible.

A la hora de desarrollar, los programas modernos modelan su **información utilizando objetos** ([Programación Orientada a Objetos](https://www.campusmvp.es/recursos/post/los-conceptos-fundamentales-sobre-programacion-orientada-objetos-explicados-de-manera-simple.aspx)), pero **las bases de datos utilizan otros paradigmas**: las relaciones (también llamadas a veces "Tablas") y las claves externas que las relacionan. Esta diferencia entre la forma de programar y la forma de almacenar da lugar a lo que se llama **"desfase de impedancia"** y complica la persistencia de los objetos

**Mas info:** https://www.campusmvp.es/recursos/post/la-api-de-persistencia-de-java-que-es-jpa-jpa-vs-hibernate-vs-eclipselink-vs-spring-jpa.aspx
## Que es ORM?
*Un ORM (Object-Relational Mapping) es una técnica o un conjunto de herramientas que permite a los desarrolladores mapear objetos de un lenguaje de programación orientado a objetos (como Java, Python, C#) a tablas y registros de una base de datos relacional.* El objetivo principal de un ORM es facilitar y automatizar la interacción entre la representación de objetos en la aplicación y los datos almacenados en una base de datos.

En esencia, un ORM actúa como un puente entre el mundo de la programación orientada a objetos y el mundo de las bases de datos relacionales. En lugar de escribir consultas SQL directamente para acceder y manipular los datos en la base de datos, los desarrolladores pueden trabajar con objetos en el lenguaje de programación que son mapeados automáticamente a tablas en la base de datos.

Las principales funciones de un ORM incluyen:

1. **Mapeo de objetos a tablas:** El ORM define cómo los objetos en el código se relacionan con las tablas en la base de datos. Esto incluye la definición de propiedades, relaciones y restricciones.
    
2. **Gestión de relaciones:** Los ORM permiten definir y manejar relaciones entre objetos en el código, como relaciones uno a uno, uno a muchos y muchos a muchos, que luego se reflejan en las relaciones de las tablas en la base de datos.
    
3. **Generación de consultas:** En lugar de escribir consultas SQL a mano, los ORM generan automáticamente las consultas necesarias para realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar) en la base de datos.
    
4. **Optimización de consultas:** Los ORM pueden optimizar las consultas generadas para mejorar el rendimiento y reducir la cantidad de consultas ejecutadas.
    
5. **Control de transacciones:** Los ORM pueden administrar automáticamente las transacciones de la base de datos, asegurando que las operaciones se realicen de manera consistente y segura.
    
6. **Portabilidad:** Los ORM permiten escribir código independiente de la base de datos, lo que facilita el cambio de base de datos sin tener que reescribir gran parte de la lógica de acceso a datos.
    

Ejemplos populares de ORM incluyen Hibernate para Java, Entity Framework para .NET, SQLAlchemy para Python y Sequelize para JavaScript. Estos frameworks facilitan la tarea de manejar datos persistentes y reducen la cantidad de código repetitivo necesario para interactuar con bases de datos relacionales.


# Frameworks
- [[Spring Boot]]

# Curso
## Conceptos:
- Que es un Artefacto?
- Que es una Dependencia?
- Que es una Libreria?
- Que es Compilar?
- Que es un archivo Jar?
- Que es el archivo manifest.mf?
- Control de Versiones.
- Creacion de Librerias.
- Miembro de Clase
## Patrones:
### Singleton: 
