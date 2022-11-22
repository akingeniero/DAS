# ADD-0007 Intentos-De-Conexion

* Status: acepted
* Date: 2022-11-21

## Contexto y problemas a resolver

* si el número de intentos de conectar con un dispositivo que falla supera un
umbral entonces se deberán suspender los intentos de conexión y considerar al
dispositivo fuera de servicio.

## Requisitio de decisión

* [RF-012](../requisitos/RF-012.md)

## Opciones consideradas

* Retry: "Reintenta automáticamente las operaciones cuyo fallo se espera bajo ciertas condiciones definidas.Este patrón permite la tolerancia a fallos en las operaciones de acceso a datos."

* [Proxy](https://refactoring.guru/es/design-patterns/proxy): "Un proxy controla el acceso al objeto original, permitiéndote hacer algo antes o después de que la solicitud llegue al objeto original."

* Funcion del emisor: " el emisor controle si se ha pasado el umbral de intetos de conexiones"

## Decisiones tomadas

Opción elegida: "Retry" es mas especifica que el proxy, las dos opciones son muy parecidas y en el fondo siguen la misma filosofia de intermediario. Las dos opcionen existe una clase intermedia que realizaria conexion con el dispositivo. Esto nos permite liberar de carga  al dispositivo. El Retry es más especifico y cuenta con unos metodos  Attempt para enviar y  Recover para que terminar un intento.

### Consecuencias positivas <!-- optional -->

* Te permite ahorrar en recursos.
* Es un patron de diseño y esta testeado.
* Facilita el tratado de datos .
* Facilita el cambio del umbral de intentos.
* Facilita el cambio del umbral de espera para considear que termina un inteto.

### Consecuencias negativas <!-- optional -->

* La complejidad general del código aumenta.

## Pros y Contras de las Opciones

### Retry

* Bueno, permite reintentar de manera autamatica la conexion.
* Bueno, no saturariamos al emisor ya que este solo envia una vez.
* Bueno, ya que podemos modificar el umbral de intentos.
* Bueno, ya que soporta fallos a la hora de la conexion.
* Malo,La respuesta del servicio puede retrasarse.

### Proxy

* Bueno, porque Puedes controlar el objeto de servicio sin que los clientes lo sepan.
* Bueno, porque Puedes gestionar el ciclo de vida del objeto de servicio cuando a los clientes no les importa.
* Bueno, porque El proxy funciona incluso si el objeto de servicio no está listo o no está disponible.
* Malo, porque La respuesta del servicio puede retrasarse.

### Funcion del emisor

* Malo, porque saturamos al emisor.
* Malo, porque bloqueamos de la ralizacion de otra funcionalidad.
