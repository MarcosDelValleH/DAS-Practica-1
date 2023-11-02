# Acceso Base de Datos

* Status: proposed
* Date: 2023-11-02

## Context and Problem Statement

Necesitamos gestionar el acceso de los servicios a la base de datos. Por ello nuestro gestor de base de datos necesitará un driver que se encargué de la comunicación con dichas bases de datos de una forma segura.

## Decision Drivers

* Tenemos dos bases de datos SQL
* Necesitamos un acceso seguro

## Considered Options

* SQL Server Native Client
* Open Database Connectivity

## Decision Outcome

Chosen option: "SQL Server Native Client", because no se plantea usar una base de datos no SQL

## Pros and Cons of the Options

### SQL Server Native Client

* Good, because tiene un muy buen rendimiento al estar diseñado específicamente para SQL Server
* Good, because nativo de Microsoft, luego facilita la autenticación de Windows integrada
* Bad, because limitado a SQL Server
* Bad, because puede requerir que los usuarios finales instalen componentes adicionales

### Open Database Connectivity

* Good, because es un estándar abierto, por lo tanto, en caso de un cambio de base de datos, facilitaría la migración
* Good, because ofrece compatibilidad con numerosos lenguajes de programación
* Bad, because no está optimizado para SQL Server
* Bad, because se necesitan drivers adicionales
