# ADD-0006 Intentos De Conexion

* Date: 2022-11-22

## Contexto y problemas a resolver

* si el número de intentos de conectar con un dispositivo que falla supera un
umbral entonces se deberán suspender los intentos de conexión y considerar al
dispositivo fuera de servicio.

## Requisitio de decisión

* [RF-012](../requisitos/RF-012.md)

## Opciones consideradas

* [Retry](./0006.1-Retry.md): "Reintenta automáticamente las operaciones cuyo fallo se espera bajo ciertas condiciones definidas.Este patrón permite la tolerancia a fallos en las operaciones de acceso a datos."

* [Proxy](./0006.2-Proxy.md): "Un proxy controla el acceso al objeto original, permitiéndote hacer algo antes o después de que la solicitud llegue al objeto original."

* [Funcion del emisor](./0006.3-Funcion-del-Emisor.md): "el emisor controla si se ha pasado el umbral de intetos de conexiones."

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

### Opciones Relacionadas

* [Retry](./0006.1-Retry.md): "Reintenta automáticamente las operaciones cuyo fallo se espera bajo ciertas condiciones definidas.Este patrón permite la tolerancia a fallos en las operaciones de acceso a datos."

* [Proxy](./0006.2-Proxy.md): "Un proxy controla el acceso al objeto original, permitiéndote hacer algo antes o después de que la solicitud llegue al objeto original."

* [Funcion del emisor](./0006.3-Funcion-del-Emisor.md): "el emisor controla si se ha pasado el umbral de intetos de conexiones."
