# Diseño capa Lógica de negocio

* Status: proposed
* Date: 2023-10-25

## Context and Problem Statement

Tenemos una capa que tiene que ejecutar la mayor parte de las operaciones. No solo hay que coordinar los distintos módulos proporcionados por la empresa sino que además hay que coordinar llamadas a los distintos módulos y llamadas de los distintos módulos a la capa base de datos. Esta capa tambien tiene que transmitir a capas superiores mensajes procesados por los módulos de la empresa.

## Decision Drivers

* No generar una arquitectura monolítica

## Considered Options

* Patrón mediador

## Decision Outcome

Chosen option: "Patrón mediador", because por los motivos expuestos

## Pros and Cons of the Options

### Patrón mediador

Para implementar este patrón vamos a crear un módulo dividido en 4 partes.
La primera es la encargada de recibir los mensajes de la capa superior.
Esta primera parte le transmite a la siguiente parte los mensajes recibidos.
La segunda parte decide a que servicio llamar segun el mensaje. Tambien gestiona la comunicación entre servicios, si fuera necesario, y con una tercera parte que se encargará de enlazarse con la capa de base de datos. 
Cuando los servicios han realizado una operación que se tiene que transmitir a capas superiores existe una cuarta parte que envía los mensajes que los servicios transmiten a través de la segunda parte. Esta cuarta parte tiene que terminar de implementar el patron observador desarrollado en la capa cliente. Tiene que implemenar el "publisher" de dicho patrón.

* Good, because Podemos coordinar la acción de los módulos de la empresa
