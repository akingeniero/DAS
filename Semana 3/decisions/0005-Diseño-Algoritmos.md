# ADD-0005 Diseño-Algoritmos

* Status: acepted
* Date: 2022-11-15

## Contexto y problemas a resolver

* Se requiere organizar los algoritmos para que dependiendo de la situacion, se eliga que algoritmo utilizar en cada momento.

## Requisitio de decisión

* [RF-010](../requisitos/RF-010.md)
* [RF-011](../requisitos/RF-011.md)

## Opciones consideradas

* [Strategy](https://refactoring.guru/es/design-patterns/strategy): " Strategy es un patrón de diseño de comportamiento que te permite definir una familia de algoritmos, colocar cada uno de ellos en una clase separada y hacer sus objetos intercambiables"

* [Chain_of_Responsibility](https://refactoring.guru/es/design-patterns/chain-of-responsibility) : " Es un patrón de diseño de comportamiento que te permite pasar solicitudes a lo largo de una cadena de manejadores"

## Decisiones tomadas

Opción elegida: "Strategy" porque cubre lo solicitado por la documentacion. Lo que se pide no es una comunicacion si no elegir dependiendo de la ocasión.

### Consecuencias positivas <!-- optional -->

* Te permite alternar.
* Es un patron de diseño y esta testeado.
* No se pierden recursos.

### Consecuencias negativas <!-- optional -->

* no se intercala informacion entre los algoritmos

## Pros y Contras de las Opciones

### Strategy

* Bueno, porque no te limita a la utilizacion final de un algoritmo.
* Bueno, porque elige el mejor algoritmo para cada ocasion.
* Malo, porque porque no se pasa informacion entre algoritmos.

### Chain_of_Responsibility

* Bueno, porque porque se pasa informacion.
* Malo, porque no te permite elegir el mejor algoritmo.
* Malo, porque  te limita a un algoritmo.

## UML de la decisión

![ADMentor](../uml/ADMentor.PNG)
