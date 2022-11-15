# [ADD-0003 Algoritmo-de-optimizacion-de-produccion]

* Status: [acepted]
* Date: [2022-11-10]

## Contexto y problemas a resolver

algoritmo para asignar los recursos de la manera mas eficaz

## Requisitio de decisión

* [RF-010](../requisitos/RF-010.md)

## Opciones consideradas

* [PL]: " Realizar un problema de optimizacion dada unas restricciones "
* [Asignacion_fija] : "asignar segun el rendimiento"

## Decisiones tomadas

Opción elegida: "[PL]" Un PL con datos en directo .

### Consecuencias positivas <!-- optional -->

* Administracion de ordenes eficiente en cada instante
* Cumpliria con las restricciones
* Podria actuar ante imprevistos

### Consecuencias negativas <!-- optional -->

* Tener siempre una buena fuente de datos

## Pros y Contras de las Opciones

### [PL]

* Bueno, porque [es capaz de asignar de la manera mas eficiente]
* Bueno, porque [actua ante imprevistos]
* Bueno, ya que [es escalable]

### [Asignacion_fija]

* Malo, porque [puede no se eficaz]
* Malo, porque [no actua ante imprevistos]

## UML de la decisión

![umlmicroservicios](../uml/umlMicroservicios.jpeg)
![ADMentor](../uml/ADMentor.PNG)
