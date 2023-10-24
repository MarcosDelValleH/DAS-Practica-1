# Capa clientes

* Status: proposed
* Date: 2023-10-24

## Context and Problem Statement

Para implementar el estilo cliente-servidor vamos a definir una primera capa que contenga lo necesario para permitir al cliente acceder a los servicios proporcionados por la empresa. Se comunica exclusivamente con la capa Gateway mandando peticiones.

## Decision Drivers

* Que el modulo que se cominica con los clientes para mandar peticiones a los servidores de la empresa funcione de forma desacoplada e independiente.

## Considered Options

* Modulo independiente
* Que fuera una capa

## Decision Outcome

Chosen option: "Que fuera una capa", because sigue manteniendo la independencia y la modularidad que se buscaba.

### Positive Consequences

* Se puede desarrollar este modulo de forma independiente.

## Pros and Cons of the Options

### Modulo independiente

Que no fuera una capa sino un modulo independiente

* Good, because Refuerza la modularidad
* Bad, because Rompe la estructura del estilo por capas

### Que fuera una capa

* Good, because Mantiene la estructura del estilo elegido
