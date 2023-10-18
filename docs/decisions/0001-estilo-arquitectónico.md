# Estilo arquitectónico

* Status: proposed
* Date: 2023-10-18

## Context and Problem Statement

Necesitamos migrar de un sistema de arquitectura monolítica a uno basado en microservicios.

## Considered Options

* Por capas
* SOA
* Microservicios
* Cliente-servidor
* Layered-SOA

## Decision Outcome

Chosen option: "Layered-SOA", because se adapta a nuestras necesidades ya que el estilo por capas nos permite procesar las peticiones realizadas por los clientes y con SOA especializamos una de las capas para poder tratar como servicios los distintos módulos proporcionados por la empresa.

### Positive Consequences

* Respeta la independencia de los módulos permitiendo seguir desarrollando los módulos de manera independiente
* SOA nos permite utilizar los módulos como servicios
* Sencilla de programar, el estilo por capas es fácil de aplicar y muchos programadores estan muy familiarizados

## Pros and Cons of the Options

### Cliente-servidor

* Bad, because Muy genérica
