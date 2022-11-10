# ADD-0005 Familia de dispositivos con 3 sensores

* Status: acepted
* Deciders: Brais Cabo Felpete
* Date: 2022-11-10

## Contexto y problemas a resolver

Los dispositivos de esta familia estan compuestos por tres sensores en los que el primero envía información al segundo y este al tercero que finalmente lo envía al centro de notificaciones. Se busca utilizar un patrón de diseño ya creado capaz de resolver esto o diseñar un estilo propio.

## Requisitio de decisión

* [RF-007](../requisitos/RF-007.md)

## Opciones consideradas

* [Patrón Chain Of Responsability](https://refactoring.guru/es/design-patterns/chain-of-responsibility) : "Patrón de diseño de comportamiento que te permite pasar solicitudes a lo largo de una cadena de manejadores, en este caso, los sensores"
* [Patrón propio]() : "Diseñar el sistema sin tener en cuenta ningún patrón de diseño y hacerlo mediante clases de sensores"

## Decisiones tomadas

Opción elegida: "Patrón Chain Of Responsability" porque este patrón permite liberar a un objeto de tener que saber qué otro objeto maneja una petición, permite que ni el receptor ni el emisor se conozcan ni estos conozcan la estructura de la cadena de objetos. A parte, añade flexibilidad, podemos añadir o cambiar responsabilidades a objetos a la hora de tratar una petición, es decir, en tiempo de ejecución.

### Consecuencias positivas <!-- optional -->

* Reducción de acoplamiento
* Flexibilidad a la hora de asignar responsabilidades a los objetos

### Consecuencias negativas <!-- optional -->

* No garantiza la recepción, no hay receptor explícito

## Pros y Contras de las Opciones

### Patrón Chain Of Responsability

* Bueno, porque reduce el acomplamiento y otorga una mayor flexibilidad a la hora de asignar responsabilidades a los sensores.
* Bueno, porque se ajusta de manera exacta al problema planteado.
* Bueno, ya que es un diseño probado y testeado.
* Bueno, ya que favorece a la encapsulación.
* Malo, porque no garantiza la recepción ya que no hay receptor explícito.

### Diseño Propio

* Bueno, porque cualquier incoveniente que no se resuelva mediante un patrón se puede diseñar.
* Malo, porque no está testeado ni probado, puede dar a fallos que resultarían en futuras actualizaciones de la arquitectura, diseño e implementación.
* Malo, porque no obtenemos el acomplamiento, la felxibilidad y la encapsulación que nos podría ofecer un patrón de diseño