# [ADD-0003 Mensajería y análisis]

* Status: [acepted]
* Deciders: [Brais Cabo Felpete]
* Date: [2022-11-02]

## Context and Problem Statement

[Los operarios de la factoria deben estar permanentemente notificados a través de un sistema de mensajería interno y deben poder suscribirse a diferentes eventos y notificaciones. También deben poder enviar órdenes de trabajo a las distintas máquinas. Se necesita que se muestren las analísticas en tiempo real del proceso
productivo y las órdenes de trabajo. Necesitamos saber si se van a agrupar las funcionalidades en un único módulo o en módulos de microservicios separados]

## Decision Drivers

* [RF-001](../requisitos/RF-001.md)
* [RF-002](../requisitos/RF-002.md)
* [RF-001](../requisitos/RF-007.md)

## Considered Options

* [Módulo Separado] : Se usa un protocolo de mensajes para IoT de libre elección (MQTT, Apache Kafka, etc).
* [Módulo Conjunto] : se usa una comunicación mediante un HTTP polling.
* [Módulo Conjunto]

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
