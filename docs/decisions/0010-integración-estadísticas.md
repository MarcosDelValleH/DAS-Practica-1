# Integración Estadísticas

* Status: proposed
* Date: 2023-11-03

## Context and Problem Statement

Necesitamos integrar el módulo estadísticas de modo que se comunique con clientes, pedidos y rutas.

## Considered Options

* Crear un gestor de datos
* Comunicarlo directamente con gestor pedidos

## Decision Outcome

Chosen option: "Crear un gestor de datos", because respeta la semántica y favorece la modularización

## Pros and Cons of the Options

### Crear un gestor de datos

Actúa de intermediario entre gestor pedidos y estadísticas

* Good, because siguiendo las relaciones se puede comunicar estadísticas con los módulos requeridos

### Comunicarlo directamente con gestor pedidos

* Good, because comunicamos estadísticas con los módulos requeridos
* Bad, because el gestor pedidos pierde semántica (gestiona pedidos pero también se encarga de mostrar datos)
