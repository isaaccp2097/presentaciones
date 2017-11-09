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
Las cabeceras de este protocolo han conseguido que este sea más fácil de ampliar y de experimentar con él. Nuevas funcionalidades pueden desarrollarse, sin más que un cliente y su servidor, comprendan la misma forma de hablar sobre las características de HTTP.
Mediante dichas cabeceras se puede flexibilizar o relajar la división entre cliente y servidor
Un ejemplo común sería ### WWW-Autenticate

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




