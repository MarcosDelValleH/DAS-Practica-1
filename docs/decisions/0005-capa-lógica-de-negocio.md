# Capa Lógica de Negocio

* Status: proposed
* Date: 2023-10-24

## Context and Problem Statement

La empresa quieren ofrecer unos servicios, los cuales implementaremos como módulos independientes entre ellos. Sin embargo, van a ser agrupados en una misma capa junto con otros módulos que cordinen estos servicios.

## Decision Drivers

* Respetar la estructura por capas
* Modularizar

## Considered Options

* Crear dos capas
* Una única capa

## Decision Outcome

Chosen option: "Una única capa", because simplifica la estructura manteniendo la calidad del diseño.

## Pros and Cons of the Options

### Crear dos capas

Una con los módulos de la lógica de negocio de la empresa y otra que se encarga de gestionar las interacciones entre servicios

* Good, because Hay un intermediario en todas las interacciones
* Bad, because Es una estructura extra con una función que tal vez se podría realizar sin ella

### Una única capa

Sería juntar los módulos de la lógica de negocio de la empresa y el gestor de servicios en una misma capa

* Good, because El grado cohesión es muy alto
* Good, because Es más fácil de desarrollar
* Bad, because Acopla un poco más los módulos de la empresa
