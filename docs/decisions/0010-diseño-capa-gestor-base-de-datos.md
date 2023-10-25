# Diseño capa gestor base de datos

* Status: proposed
* Date: 2023-10-25

## Context and Problem Statement

Hay varios servicios intentando accedeer a varias bases de datos que tienen datos muy diversos. Necesitamos que haya una estructura que nos permita controlar y coordinar los accesos a la base de datos. Dichos datos aparecen tambien en formatos variados.

## Considered Options

* Patrón adapter

## Decision Outcome

Chosen option: "Patron adaper"

## Pros and Cons of the Options

### Patrón adapter

Es una clase que adapta la información de la base de datos al formato necesitado por los clientes y maneja las distintas peticiones de información.
