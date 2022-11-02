# ADR-0002 Tipo de base de datos a utilizar

* Status: [proposed]
[ADR-0005](0005-example.md)]
* Deciders: [???]

## Contexto y problemas a resolver

[Se necesitan guardar en la base de datos tanto órdenes de trabajo como el inventario del material existente]

## Identificador del Requisito

* [RF-004](../requisitos/RF-004.md)

## Opciones consideradas

* Opcion 1: [Base de datos SQL] : la base de datos a utilizar será una base de datos relacional SQL.
* Opcion 2: [Base de datos NOSQL] : la base de datos a utilizar será una base de datos no relacional.

## Decisiones tomadas

## Decisiones tomadas

Chosen option: "[Opcion 1]", because[permite almacenar de forma eficiente la información que necesitamos sin la complejidad que supone una base de datos no relacional.]

### Consecuencias positivas <!-- optional -->

* [Más asentado a lo largo del tiempo.]
* [Estándares bien definidos.]
* [Sencillez en su utilización.]
* [Atomicidad.]
* [Escritura simple.]


### Consecuencias negativas <!-- optional -->

* [Posible dificultad a la hora de crecer.]
* [Puede ser un poco más comleja su instalación.]

### Discusión ASC: Arquitectura de Microservicios

* Bueno, porque todos los datos que tenemos que guardar siguen el modelo relacional
* Bueno, porque es un estándar asentado en el tiempo.
* Bueno, ya que su uso suele estar extendido
* Malo, porque hay que puede provocar problemas de escalabilidad en el futuro.

**Decisión ASC: pendiente**

## Decisión final tomada

Opción elegida: [Base de datos SQL]

## UML de la decisión

Por hacer