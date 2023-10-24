# Capa Gestor Base de Datos

* Status: proposed
* Date: 2023-10-24

## Context and Problem Statement

Necesitamos gestionar el acceso de los servicios a la base de datos

## Considered Options

* Capa intermedia entre la capa de lógica de negocio y las bases de datos

## Decision Outcome

Chosen option: "Capa intermedia entre la capa de lógica de negocio y las bases de datos", because mejora la mantenibilidad ya que no tenemos que cambiar la lógica de negocios ni tocar las bases de datos para realizar cambios en como se gestionan los datos
