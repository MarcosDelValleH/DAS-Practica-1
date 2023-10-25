# Diseño capa clientes

* Status: proposed
* Date: 2023-10-25

## Context and Problem Statement

Necesitamos que el cliente pueda interactuar con nuestro sistea. Necesitamos un diseño que permita al cliente enviar peticiones al servidor y recibir la información mostrada por la interfaz.

## Decision Drivers

* Respetar el diseño actual
* Mantener la capa Clientes independiente

## Considered Options

* MVC
* Patrón "front Controller"

## Decision Outcome

Chosen option: "MVC", because resuelve el problema de tener una manera de comunicar al cliente y al servidor.

## Pros and Cons of the Options

### MVC

Definimos una interfaz que muestre los datos al cliente. Un controlador maneja las peticiones del cliente para transmitirselas al gateway y recibe la información que tiene que mostrar la interfaz. El modelo esta compuesto por las siguientes capas.

* Good, because Es flexible
* Good, because Es sencillo de implementar
* Bad, because El modelo se desarrolla fuera de la capa cliente

### Patrón "front Controller"

Intercepta las peticiones del cliente antes de que lleguen al gateway

* Bad, because No resuelve el problema de diseño de integrar una interfaz que interactue con el cliente.
