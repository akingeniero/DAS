# [ADD-0003 Sistema de mensajería interna]

* Status: [proposed]
* Deciders: [Brais Cabo Felpete]
* Date: [2022-11-02]

## Context and Problem Statement

[Los operarios de la factoria deben estar permanentemente notificados a través de un sistema de mensajería interno y deben poder suscribirse a diferentes eventos y notificaciones.]

## Decision Drivers

* [RF-007](../requisitos/RF-007.md)

## Considered Options

* [option 1] : Se usa un protocolo de mensajes para IoT de libre elección (MQTT, Apache Kafka, etc).
* [option 2] : se usa una comunicación mediante un HTTP polling.

## Decision Outcome

Chosen option: "[option 1]", because[son protocolos ya implementados, y ligeros, los cuáles nos permitirán una comunicación efectiva]

### Positive Consequences <!-- optional -->

* [Es el deseado por el cliente.]
* [Ya está implementado por lo que nos supondrá menos esfuerzo.]
* [Sencillez en su utilización.]
* [Escalabilidad.]

### Consecuencias negativas <!-- optional -->

* [No es un protocolo hecho a medida para nuestro sistema.]

## Pros and Cons of the Options

### [option 1]

* Good, beacause [es el que nos ha pedido el cliente.]
* Good, beacause [son protocolos testeados.]

## Decisión final tomada

Opción elegida: [option 1]

## UML de la decisión

Por hacer