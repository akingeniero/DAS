# ADD-0006 Arquitectura Secundaria para los componentes de visualización

* Status: acepted
* Date: 2022-11-10

## Contexto y problemas a resolver

Necesitamos que el sistema disponga de un centro de notificaciones, el cuál permita gestionar todas las funcionalidades del sistema. También necesitamos una aplicación móvil para que los operadores puedan enviar órdenes de trabajo y recibir notificaciones e informes de los eventos a los que están suscritos.

## Requisitos de decisión

* [RF-004](../requisitos/RF-004.md)
* [RF-008](../requisitos/RF-008.md)

## Opciones consideradas

* [Modelo Vista Controlador](https://www.freecodecamp.org/news/the-model-view-controller-pattern-mvc-architecture-and-frameworks-explained/): "El modelo vista controlador es un estilo arquitectónico que nos permite tener múltiples vistas de los mismos datos."
* [Cliente Servidor](https://docs.microsoft.com/es-es/azure/architecture/guide/architecture-styles/n-tier): "La arquitectura cliente servidor, se basa en un servidor, al que se pueden conectar múltiples clientes para solicitar los datos que necesitan."

## Decisiones tomadas

Opción elegida: "Modelo Visto Controlador" por que permite crear múltiples clientes para visualizar los datos de nuestro sistema, sin la necesidad de aumentar la complejidad de la lógica interna.

### Consecuencias positivas <!-- optional -->

* Separación entre la interfaz de usuario y la lógica de programa.
* Los componentes son reutilizables.
* Posibilidad de múltiples interfaces de usuario sin complicar la lógica interna del programa.

### Consecuencias negativas <!-- optional -->

* Posible dificultad a la hora de diseñar el sistema.

## Pros y Contras de las Opciones

### [Modelo Vista Controlador]

* Bueno, porque permite separar la lógica del programa de la interfaz de usuario.
* Bueno, porque permite mantener la aplicación de forma sencilla.
* Bueno, porque facilita la creación de múltiples interfaces de usuario que usan los mismos datos.
* Malo, porque puede complicar el diseño de la arquitectura.

### [Cliente Servidor]

* Malo, porque complica la creación de múltiples interfaces de usuario.
