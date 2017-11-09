# HTTP 

Presentación de HTTP

---

### Características HTTP

Este protocolo se establece sobre la capa de conexión TCP/IP, y funciona de la misma forma que el resto de los servicios comunes en entorno UNIX.
- Toda la comunicación se realiza con caracteres US-ASCII de 7 bits
- Permite transferencia de objetos multimedia
- Hay 8 verbos que permiten al cliente dialogar con el servidor
- Cada operación implica una conexión con el servidor que es liberada cuando se termina esta
- No mantiene el estado
- Cada objeto está identificado a través de un localizador uniforme de recurso único

---
### Típica sesión HTTP
En los protocolos que están basados en el modelo cliente-servidor, una sesión consta de las siguientes fases en HTTP
- El cliente establece una conexión TCP
- El cliente manda su petición y espera la respuesta oportuna
- El servidor procesa la petición y responde con un código de estado y con los datos correspondientes

---
### Cabeceras HTTP
Permite que el cliente y el servidor pasen información adicional con la solicitud o la respuesta.
Un encabezado de solicitud consiste en un nombre sensible a mayúsculas y minúsculas seguido de dos puntos y luego por su valor

Los encabezados patentados personalizados se pueden agregar usando el prefijo 'X’, otros se enumeran en un registro de IANA.

---
### Cabeceras HTTP
- Encabezado general: Encabezados que se aplican tanto a las solicitudes como a las respuestas, pero sin relación con los datos que finalmente se transmiten en el cuerpo.
- Encabezado de solicitud: encabezados que contienen más información sobre el recurso que se va a buscar o sobre el propio cliente.
- Encabezado de respuesta: Encabezados con información adicional sobre la respuesta, como su ubicación o sobre el servidor en sí (nombre y versión, etc.).
- Encabezado de entidad: Encabezados que contienen más información sobre el cuerpo de la entidad, como su longitud de contenido o su tipo MIME.



---
### Peticiones HTTP
Una vez la conexión se establece, el cliente es capaz de mandar una petición de datos. La petición de datos de un cliente HTTP, consiste en directivas de texto separadas por CRLF
Se divide en:
- Primera parte, consiste en una línea, que contiene un método, seguido de sus parámetros
- Segunda parte, está fomada por un bloque de lÍneas consecutivas que son las cabeceras de la petición y dan información al servidor.
- La tercera parte es un bloque de datos opcional, que puede contener más datos para ser usados por el método POST

---
### Peticiones HTTP
### Un ejemplo sería
   GET / HTTP/1.1
   Host: developer.mozilla.org
   Accept-Language: fr

---
### Respuestas HTTP
Cuando el servidor procesa la petición enviada por el usuario responde de una forma muy parecida a la petición del servidor, la respuesta del servidor está formada por directivas de texto separadas por el carácter CRLF y se divide en
- La primera parte, es la línea de estado, es una confirmación de la versión de HTTP usado y seguido por el estado de la petición
- La segunda parte representa las cabeceras HTTP concretas, dando al cliente la información sobre los datos enviados
- La tercera y última parte es en donde se pueden contener opcionalmente los datos

---
### Cookies
Cuando se recibe una solicitud HTTP un servidor puede enviar un Set-Cookie con las respuestas. Las cookies normalmente son almacenadas por el navegador y luego se envía con las solicitudes hechas al mismo servidor dentro de una cookie HTTP
Los distintos tipos de cookies que hay son
- Cookies de sesión
- Cookies permanentes


---
### Cookies
### Gestión de sesiones
Inicios de sesión, carritos de compras, puntajes de juegos o cualquier otra cosa que el servidor deba recordar
### Personalización
Preferencias de usuario, temas y otras configuraciones
### Rastreo
Grabar y analizar el comportamiento del usuario


---
### Evolución de HTTP
La versión 0.9 fue la primera y fue extremadamente simple. Las solicitudes consisten en una sola línea y comienzan con el único método posible GET seguido de la ruta al recurso

---
### Evolución de HTTP
Mejoras v 1.0
- La información del control de versiones se envía ahora dentro da solicitud
- También se envía una línea de código de estado al comienzo de respuesta.
- Se ha introducido la noción de encabezados HTTP
- Con la ayuda de los nuevos encabezados HTTP se ha agregado la capacidad de transmitir otros documentos aparte de los archivos HTML simples

---
### Evolución de HTTP
Nuevas mejoras v 1.1
Se puede reutilizar una conexión, ahorrarle tiempo a reabrirla numerosas veces para mostrar los recursos incrustados en el único documento original
Se ha agregado la canalización
Las respuestas fragmentadas ahora son compatibles
Se han introducido mecanismos adicionales de control de cache
Se ha introducido la negociación de contenido

---

### Características de HTTP 2.0
El protocolo HTTP 2.0 tiene varias diferencias principales de la versión
- Es un protocolo binario en lugar de texto.
- Es un protocolo multiplexado
- Comprime encabezados
- Permite a un servidor completar los datos en un caché del cliente.
