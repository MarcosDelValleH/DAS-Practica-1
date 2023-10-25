# Diseño del Gateway

* Status: proposed
* Date: 2023-10-25

## Context and Problem Statement

Necesitamos diseár esta capa para que pueda recibir la información del cliente y pasarsela a la capa inferior para que la procese. Tambien transmite a la capa superior la información de la capa inferior. Dicha inormación sera transmitida en diferentes formatos. Por ello necesitareoms que esta capa sea capaz de traducir la información a los formatos correspondientes.

## Decision Drivers

* Mantener la capa geteway como una capa simple y que no requiera invertir mucho en creación y mantenimiento pero que cumpla su función.

## Considered Options

* Patron Adapter
* Patrón decorator
* Patrón facade

## Decision Outcome

Chosen option: "Patron Adapter", because es lo mejor para el desarrollo futuro ne terminos de costes. (Más facil y barato escalar a nuevos protocolos)

## Pros and Cons of the Options

### Patron Adapter

Hay una clase proporcionada por la empresa encargada de recibir el mensaje del cliente e implementa el acceso actual. Crearemos otra para adaptar al formato correspondiente los mensajes y enviarlos a la capa inferior.
