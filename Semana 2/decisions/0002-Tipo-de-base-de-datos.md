# [ADD-0002 Tipo de base de datos a utilizar]

* Status: [proposed]
* Deciders: [???]
* Date: [2022-11-02]] 

## Context and Problem Statement

[Se necesitan guardar en la base de datos tanto órdenes de trabajo como el inventario del material existente]

## Decision Drivers

* [RF-004](../requisitos/RF-004.md)

## Considered Options

* [option 1] : se implementará una base de datos relacional siguiendo el estandar SQL.
* [option 2: Base de datos No SQL] : se implementará una base de datos no relacional.

## Decision Outcome

Chosen option: "[option 1]", because[permite almacenar de forma eficiente la información que necesitamos sin la complejidad que supone una base de datos no relacional.]

### Positive Consequences <!-- optional -->

* [Más asentado a lo largo del tiempo.]
* [Estándares bien definidos.]
* [Sencillez en su utilización.]
* [Atomicidad.]
* [Escritura simple.]


### Consecuencias negativas <!-- optional -->

* [Posible dificultad a la hora de crecer.]
* [Puede ser un poco más comleja su instalación.]

## Pros and Cons of the Options

### [option 1]

* Bueno, porque todos los datos que tenemos que guardar siguen el modelo relacional
* Bueno, porque es un estándar asentado en el tiempo.
* Bueno, ya que su uso suele estar extendido
* Malo, porque hay que puede provocar problemas de escalabilidad en el futuro.

## Decisión final tomada

Opción elegida: [option 1]

## UML de la decisión

Por hacer