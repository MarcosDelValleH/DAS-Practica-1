# Estilo arquitectónico

* Status: proposed
* Date: 2023-10-18

## Context and Problem Statement

Para responder a las necesidades de migrar un sistema de arquitectura monolítica a una basada en microservicios hemos decidido emplear un estilo Cliente-Servidor estructurado en lo que llamamos Layared-SOA. Las peticiones realizadas por los clientes se procesan a traves de distintas capas. Se adapta una de las capas con un estilo SOA para poder tratar como servicios los distintos módulos proporcionados por la empresa. Los módulos no interactuarán entre ellos directamente. Lo harán a traves de las capas superiores e inferiores.

## Considered Options

* Por capas
* SOA
* Microservicios
* Cliente servidor
* Layered (por capas)
* Layered-SOA

## Decision Outcome

Chosen option: "Layered-SOA", because Es una arquitectura que respeta la independencia de los módulos (SOA nos permite utilizar los módulos como servicios), permite seguir desarrollandolos de manera independiente y es sencilla de programar (el estilo por capas es fácil de aplicar y muchos programadores estan muy familiarizados).
