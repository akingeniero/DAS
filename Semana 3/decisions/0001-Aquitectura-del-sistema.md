# [ADD-0001 Arquitectura del sistema]

* Status: [acepted]
* Deciders: [Daniel Gallardo, Sergio Pérez]
* Date: [2022-11-02]

## Contexto y problemas a resolver

[Necesitamos diseñar un estructura para organizar el planteamiento del sistema requerido.]

## Requisitio de decisión

* [RF-010](../requisitos/RF-010.md)

## Opciones consideradas

* [PL] : "Es la programación matemática dedicado a maximizar o minimizar (optimizar) una función lineal, denominada función objetivo, de tal forma que las variables de dicha función estén sujetas a una serie de restricciones expresadas mediante un sistema de ecuaciones o inecuaciones también lineales"

* [Regresión_lineal]: " es un modelo matemático usado para aproximar la relación de dependencia entre una variable dependiente Y, m variables independientes X"

## Decisiones tomadas

Opción elegida: "[PL]" porque el sistema requiere distribuir las ordenes de trabajo para que no se solapen y que dependiendo de una variables de eficacia se distribuiran de manera eficiente.

### Consecuencias positivas <!-- optional -->

* [Mejoras en la escalabilidad.]
* [Simple de realizar ]
* [Código y mantenimiento más legible.]

### Consecuencias negativas <!-- optional -->

* [Refresecar las variables dependiendo de los datos en directo es costoso]

## Pros y Contras de las Opciones

* [la prediccion se debe dejar en un segundo plano ]


### [Arquitectura de microservicios]

* Bueno, porque [es la arquitectura que ha solicitado el cliente]
* Bueno, porque [los microservicios son más fáciles de mantener y testear, puesto que son servicios pequeños que hacen una sóla cosa, pero la hacen bien]
* Bueno, ya que [al no estar integrados en el sistema principal, son de fácil despliegue]
* Bueno, ya que [pueden tener una escalabilidad independiente y es más sencillo aislar fallos a un microservicio concreto, en vez de una sección o funcionalidad de la aplicación]
* Malo, porque [hay que lidiar con la complejidad adicional de los sistemas distribuidos]
* Malo, porque [hay que implementar dependencias de un servicio a otro, comunicación interna entre servicios, etc.]
* Malo, porque [implica un mayor consumo de recursos, puesto que cada microservicio tiene su propio SO y dependencias]

### [Arquitectura por capas]

* Bueno, porque [existe una jerarquía bien marcada entre elementos]
* Malo, porque [ciertos elementos se quedarian fuera de esta jerarquía]
* Malo, porque [no existe una escalabilidad independiente]

## UML de la decisión

![umlmicroservicios](../uml/umlMicroservicios.jpeg)
![ADMentor](../uml/ADMentor.PNG)
