# ADD-0006 Familia-Sensores

* Status: acepted
* Date: 2022-11-16

## Contexto y problemas a resolver

* Se requiere organizar las familias de sensores. Se tratan de familias con un tratado de datos distintos entre ellos, es necesario un componente que organice y normalice los datos para que se puedan tratar.

## Requisitio de decisión

* [RF-005](../requisitos/RF-005.md)

## Opciones consideradas

* [Adapter](https://refactoring.guru/es/design-patterns/adapter): " Adapter es un patrón de diseño estructural que permite la colaboración entre objetos con informacion incompatibles."

* Tratarlos_por_canales_distintos : " Manejar cada informacion por un canal distinto y tener un procesado de datos distinto"

## Decisiones tomadas

Opción elegida: "Adapter" porque optimizarias los recursos teniendo que tratar los datos solo de una manera, sin necesidad de gestionar distintos tipos de datos.

### Consecuencias positivas <!-- optional -->

* Te permite ahorrar en recursos.
* Es un patron de diseño y esta testeado.
* Facilita el tratado de datos .

### Consecuencias negativas <!-- optional -->

* La complejidad general del código aumenta.

## Pros y Contras de las Opciones

### Adapter

* Bueno, puedes introducir nuevos tipos de adaptadores al programa.
* Bueno, crear una clase intermedia que sirva como traductora.
* Malo, la complejidad general del código aumenta.

### Tratarlos_por_canales_distintos

* Bueno, la complejidad general del código no aumenta.
* Malo, tengo generaria complejidad al tratar los datos
* Malo, porque no es escalable.

## UML de la decisión

![ADMentor](../uml/ADMentor.PNG)
