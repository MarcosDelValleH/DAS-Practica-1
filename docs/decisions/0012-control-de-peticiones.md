# Control de peticiones

* Status: proposed
* Date: 2023-11-12

## Context and Problem Statement

Se necesita limitar el número de intentos de realización de un pedido para evitar que el sistema colapse.

## Considered Options

* Proxy
* Throttling
* Rate limiting

## Decision Outcome

Chosen option: "Rate limiting", because es justo lo que queremos, limitar el número de solicitudes que llegan al servidor en un tiempo determinado

## Pros and Cons of the Options

### Proxy

Proporciona un objeto representante (proxy) que controla el acceso a otro objeto. Actúa como intermediario entre el cliente y el objeto real, permitiendo al proxy agregar funcionalidades adicionales como control de acceso.

* Good, because puede implementar lógica para verificar si un cliente ha superado el límite de intentos antes de permitir que la solicitud alcance el servidor principal.
* Good, because puede adaptarse a requisitos específicos de limitación de intentos para diferentes clientes o escenarios.
* Bad, because introducir un proxy agrega complejidad al sistema y requiere una gestión adicional.
* Bad, because puede introducir cierta latencia adicional debido al procesamiento adicional de las solicitudes.

### Throttling

Limita la velocidad o la frecuencia con la que se pueden realizar ciertas operaciones o acciones.

* Good, because permite controlar la velocidad de las solicitudes a nivel de usuario o dirección IP.
* Good, because evita que los clientes realicen un número excesivo de intentos en un corto período, lo que ayuda a prevenir abusos y ataques.
* Bad, because si se establecen límites demasiado bajos, podría afectar negativamente la experiencia del usuario legítimo.

### Rate limiting

Controlar la velocidad a la que se pueden realizar ciertas acciones, como solicitudes a un servidor, dentro de un período de tiempo determinado.

* Good, because permite un control más preciso sobre la tasa de solicitudes permitidas.
* Good, because puede ajustarse para adaptarse a diferentes necesidades y perfiles de clientes.
* Bad, because no proporciona la misma granularidad que throttling al limitar a un nivel de servidor.
