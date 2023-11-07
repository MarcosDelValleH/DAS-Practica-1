# Algoritmo de enrutamiento

* Status: proposed
* Date: 2023-11-07

## Context and Problem Statement

El módulo de rutas necesita aplicar varios algoritmos proporcionados por la empresa en base a la demora del camión. Se necesita una estructura que permita elegir los algoritmos de manera eficiente y que sea mantenible y escalable.

## Considered Options

* Patrón strategy
* Template method

## Decision Outcome

Chosen option: "Patrón strategy", because no tenemos constancia de que los algoritmos compartan código.

### Positive Consequences

* Permite añadir algoritmos simplemente mediante nuevas implementaciones de la interfaz.

## Pros and Cons of the Options

### Patrón strategy

Rutas utiliza una interfaz para calcular rutas. Los distintos algoritmos implementan esta interfaz.

* Good, because permite ampliar los algoritmos a nuevas maneras.

### Template method

* Good, because si los algoritmos son en gran parte similares, puedes colocar el código duplicado dentro de una superclase
* Bad, because el coste de mantenimiento incrementa con el tiempo.
* Bad, because los clientes se pueden ver limitados por las posibilidades ofrecidas por esta estructura.
