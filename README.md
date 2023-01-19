# Curso_de_Fundamentos_de_Bases_de_Datos

<h2>Content List</h2>

- [Introducción a las Bases de Datos Relacionales](#introducción-a-las-bases-de-datos-relacionales)
- [Qué son entidades y atributos](#qué-son-entidades-y-atributos)
- [Entidades de Platzi Blog](#entidades-de-platzi-blog)
- [Relaciones](#relaciones)
- [Múltiples Muchos](#múltiples-muchos)

## Introducción a las Bases de Datos Relacionales

Las bases de datos surgen de la necesidad de conservar la información más allá de lo que existe en la memoria RAM. 

Las bases de datos **basadas en archivos** eran datos guardados en texto plano, fáciles de guardar pero muy díficiles de consultar y por la necesidad de mejorar esto nacen las **bases de datos relacionales**. Su inventor **Edgar Codd** dejó ciertas reglas para asegurarse de que toda la filosofía de las bases de datos no se perdiera, estandarizando el proceso. 

[Codd's 12 Rules](https://www.mindmeister.com/es/1079684487/las-12-reglas-de-codd-del-modelo-relacional?fullscreen=1)

## Qué son entidades y atributos

En bases de datos, una entidad es la representación de un objeto o concepto del mundo real que se describen en una base de datos. Las entidades se describen en la estructura de la base de datos empleando un modelo de datos. 

<h3>¿Qué es Entidad?</h3>

Una **entidad** es algo similar a un objeto (programación orientada a objetos) y representa algo en el mundo real, incluso algo abstracto. tienen atributos que son las cosas que los hacen ser una entidad y por convecnión se ponen en plural. 

<h3>Ejemplo de Entidad en Bases de Datos</h3>

En la imagen se puede observar como ejemplo ue la entidad *Laptops* posee diferentes atributos como color, pantalla, año, modelo, etc.

<p align="center"><img width=90% src="./Pictures/entidades.webp"></p>

*En el caso de antigüedad es un **atributo derivado** puesto que se puede inferir de acuerdo al año de salida*

<h3>¿Qué es un Atributo?</h3>

Son las características o propiedades que describen a la entidad (Se encieraa en un óvalo). Los atributos se componen de:

* Los **Atributos compuestos** son aquellos que tienen atributos ellos mismos.
* Los **Atributos llave** son aquellos que identifican a la entidad y no pueden ser repetidos. Existen:
    * Naturales: Son inherentes al objeto como el número de serie. 
    * Clave artificial: No es inherente al objeto y se asigna de manera arbitraria. 

<h3>Tipos de Entidades</h3>

* **Entidades fuertes:** Son entidades que pueden sobrevivir por sí solas. 
* **Entidades débiles:** No pueden existir sin una entidad fuerte y se representan con un cuadro con doble línea. 
    * Entidades débiles por identidad: No se difrencian entre sí más que por la clave de su entidad fuerte.
    * Entidades débiles por existencia: Se les asigna una clave propia. 

<h3>Cómo Representar las Entidades en Bases de Datos</h3>

Existen varios tipos de notaciones para los modelos entidad relacionamiento. *Chen* es uno de los más utilizados para diagramar lógicamente la base de datos.

<p align="center"><img width=60% src="./Pictures/Chen.webp"></p>

## Entidades de Platzi Blog

En este caso se hará una base de datos, el cual consiste en un manejador de Blogspot

* Primer paso: Identificar las entidades.
* Segundo paso: Pensar en los atributos.

<h3>Diagrama ER: PlatziBlog</h3>

* Post
    * Título
    * Fecha de publicación 
    * Contenido
    * Estatus
    * Etiquetas (multivaluado)
    * Id Post
* Usuarios
    * Login
    * Password
    * Nickname
    * Email
    * IdUsuario
* Comentarios
    * Contenido
    * Fecha de publicación
    * IdComentario
    * IdUsuario(clave foránea)
* Categorías
    * Nombre de Categoría
    * idCategoría

## Relaciones

Las **Relaciones** nos permiten ligar o unir nuestras diferentes entidades y se representan con rombos. Por convención se definen a través de verbos. 

Las relaciones tienen una propiedad llamada **cardinalidad** y tiene que ver con números. Cuántos de un lado pertenecen a cuántos del otro lado: 

* Cardinalidad: 1 a 1: Persona _ tiene _ datos-contacto, para obtener la cardinalidad se extraen los números mayores de los dos lados. 
* Cardinalidad: 0 a 1: Paciente _ tiene _ hab-hospital, la habitación de hospital puede estar vacía. 
* Cardinalidad: 1 a N: Persona _ tiene _ automovil. Una persona puede tener muchos automóviles, pero, un automovil por cuestión de documentos, sólo puede tener un dueño.
* Cardinalidad: 0 a N

<p align="center"><img width=50% src="./Pictures/Cardinalidad.png"></p>

## Múltiples Muchos

<h3>Cardinalidad Muchos a Muchos</h3>

Alumno _ Pertenece _ Clase

## Diagrama ER

Un diagrama es como un mapa y nos yuda a entender cuáles son las entidades con las que vamos a trabajar, cuáes son sus relaciones y qué papel van a jugar en las aplicaciones de la base de datos. 

[Ejemplo de Diagramas ER Platzi Blogspot](/Diagrams/Diagrama_ER.drawio)

[Ejemplo de Diagramas ER Banda/Género](/Diagrams/DER_Example.drawio)
