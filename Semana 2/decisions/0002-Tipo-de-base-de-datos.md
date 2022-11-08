# [ADD-0002 Tipo de base de datos a utilizar]

* Status: [proposed]
* Deciders: [Brais Cabo Felpete]
* Date: [2022-11-02]]

## Context and Problem Statement

[Se necesitan guardar en la base de datos tanto órdenes de trabajo como el inventario del material existente]

## Decision Drivers

* [RF-004](../requisitos/RF-004.md)

## Considered Options

* [Database-per-service](https://docs.aws.amazon.com/es_es/prescriptive-guidance/latest/modernization-data-persistence/database-per-service.html) : se usará el patrón Database-per-service, en el que cada microservicio tiene una base de datos independiente.
* [Shared-database-per-service](https://docs.aws.amazon.com/es_es/prescriptive-guidance/latest/modernization-data-persistence/shared-database.html): se usará el patrón Shared-database-per-service, en el que los microservicios comparten una base de datos.

## Decision Outcome

Chosen option: "[Shared-database-per-service]", because[queremos garantizar la coherencia de los datos, y utilizar transacciones uniformes, ya que todos los microservicios operan sobre los mismos datos, por lo que nos ahorramos tener bases de datos repetidas.]

### Positive Consequences <!-- optional -->

* [Garantizar la coherencia de los datos]
* [Mantener y operar solo una base de datos.]
* [Utilizar transacciones que proporcionan atomicidad, uniformidad, aislamiento y durabilidad (ACID, por sus siglas en inglés).]

### Negative Consequences <!-- optional -->

* [Posible dificultad a la hora de crecer.]
* [Patrón difícil debido a las interdependencias entre sus microservicios existentes.]

## Pros and Cons of the Options

### [Shared-database-per-service]

* Good, because [Permite mantener una sola base de datos]
* Good, because [Permite garantizar la coherencia de los datos]
* Good, because [Proporciona atomizidad]
* Bad, because [Es más dificil de implementar]

### [Database-per-service]

* Good, because [Permite descentralizar completamente los microservicios]
* Bad, because [Debe administrar varias bases de datos relacionales y no relacionales]
