# Estilo arquitectónico

* Status: proposed
* Date: 2023-10-18

## Context and Problem Statement

Necesitamos migrar de un sistema de arquitectura monolítica a uno basado en microservicios.

## Decision Drivers

* Aplicación para clientes ajenos a la empresa
* Aprovechar los módulos de la empresa
* Usaremos bases de datos existentes

## Considered Options

* Por capas
* SOA
* Microservicios
* Cliente-servidor
* Layered-SOA

## Decision Outcome

Chosen option: "Cliente-servidor", because se adapta a nuestras necesidades ya que este estilo está divido en 3 capas bien diferenciadas, permitiéndonos separar la interfaz (con la que interactuará el cliente) de la lógica de negocio (donde acoplaremos los módulos de la empresa) y de las bases de datos (también alojadas en el servidor)

### Positive Consequences

* Respeta la independencia de los módulos
* Sencillo de programar
* Muchos programadores están muy familiarizados
* Sistema mantenible
* Es posible llevar a cabo un desarrollo paralelo en cada capa.

## Pros and Cons of the Options

### Cliente-servidor

* Bad, because Muy genérica
