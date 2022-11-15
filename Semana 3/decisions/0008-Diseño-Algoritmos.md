# [ADD-0003 Algoritmo-de-predicción-de-fallos]

* Status: [acepted]
* Date: [2022-11-10]

## Contexto y problemas a resolver

* La selección del algoritmo adecuado

## Requisitio de decisión

* [RF-010](../requisitos/RF-010.md)
* [RF-011](../requisitos/RF-011.md)

## Opciones consideradas

* [Strategy]: " Strategy es un patrón de diseño de comportamiento que te permite definir una familia de algoritmos, colocar cada uno de ellos en una clase separada y hacer sus objetos intercambiables"

* [Chain_of_Responsibility] : "es un patrón de diseño de comportamiento que te permite pasar solicitudes a lo largo de una cadena de manejadores"

## Decisiones tomadas

Opción elegida: "[Strategy]" porque cubre lo solicitado por la documentacion.

### Consecuencias positivas <!-- optional -->

* Te permite alternar.
* Es un patron de diseño y esta testeado.

### Consecuencias negativas <!-- optional -->

* no se intercala informacion entre los algoritmos

## Pros y Contras de las Opciones

### [Strategy]

* Bueno, porque no te limita a un algoritmo
* Malo, porque porque no se pasa informacion

### [Chain_of_Responsibility]

* Bueno, porque porque se pasa informacion
* Malo, porque  te limita a un algoritmo

## UML de la decisión

![ADMentor](../uml/ADMentor.PNG)
