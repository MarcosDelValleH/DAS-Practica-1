# Capa Gateway

* Status: proposed
* Date: 2023-10-24

## Context and Problem Statement

Tenemos un gateway por implementar y queremos introducirlo en nuestra estructura por capas.

## Considered Options

* Capa independiente
* Módulo dentro de otra capa

## Decision Outcome

Chosen option: "Capa independiente", because respeta la estructura y actúa con independencia y modularidad

## Pros and Cons of the Options

### Capa independiente

* Good, because Mejora la mantenibilidad

### Módulo dentro de otra capa

* Bad, because dependiente de los cambios en la capa en la que se encuentre
