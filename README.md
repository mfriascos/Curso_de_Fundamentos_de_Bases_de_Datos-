# Curso_de_Fundamentos_de_Bases_de_Datos

<h2>Content List</h2>

- [Introducción a las Bases de Datos Relacionales](#introducción-a-las-bases-de-datos-relacionales)
- [Qué son entidades y atributos](#qué-son-entidades-y-atributos)

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




