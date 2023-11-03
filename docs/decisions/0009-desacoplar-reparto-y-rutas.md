# Desacoplar Reparto y rutas

* Status: proposed
* Date: 2023-11-03

## Context and Problem Statement

Necesitamos desacoplar el módulo "Reparto y rutas" en dos: "Reparto", "Rutas".

## Considered Options

* Mantener una relación entre ambos módulos
* Intermediar la relación mediante un gestor

## Decision Outcome

Chosen option: "Mantener una relación entre ambos módulos"

## Pros and Cons of the Options

### Mantener una relación entre ambos módulos

Una vez el modulo Reparto elige una flota de transporte para los pedidos de unos determinados clientes, llama al módulo Rutas para calcular la ruta óptima de los camiones

* Good, because tiene la misma función que antes del desacople pero con la ventaja de que está modularizado

### Intermediar la relación mediante un gestor

El módulo reparto se comunica con el módulo ruta a través de gestor pedidos

* Bad, because al ser un proceso secuencial, no tiene sentido meter a un intermediario
