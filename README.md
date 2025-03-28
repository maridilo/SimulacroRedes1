# SimulacroRedes1
https://github.com/maridilo/SimulacroRedes1.git

Parte I: Conceptos y Teoría
Pregunta 1: Modelos OSI y TCP/IP
a)	Describe las principales diferencias entre el modelo OSI y el modelo TCP/IP, considerando aspectos como el número de capas, la orientación (teórica vs. práctica) y el manejo de la capa de aplicación.

Numero de capas:
-	OSI: tiene 7 capas -> Fisica, Enlace de Datos, Red, Transporte, Sesión, Presentación y Aplicación.
-	TCP/IP: tiene 4 capas (a veces se representa con 5) -> Acceso a la Red, Internet, Transporte y Aplicación.
Orientación:
-	OSI: su orientación es teórica (modelo de referencia)
-	TCP/IP: su orientación es practica (basado en protocolos reales)
Manejo de la capa de aplicación:
-	OSI: se divide en 3 capas -> aplicación, presentación y sesión.
-	TCP/IP: tiene una sola -> aplicación.

b)	Explica brevemente las ventajas y limitaciones de cada uno de estos modelos.

Ventajas:
-	OSI: esta definido y es modular. Es útil para la enseñanza.
-	TCP/IP: esta basado en protocolos reales (internet) y es altamente implementado.
Desventajas:
-	OSI: no se implementa directamente y es complejo en algunas capas.
-	TCP/IP: es menos modular y menos claro para fines pedagógicos.
________________________________________
Pregunta 2: Función de la Capa de Transporte
Explica el papel de la capa de transporte en ambos modelos (OSI y TCP/IP). En tu respuesta, menciona cómo se garantiza la entrega de datos y da ejemplos de protocolos asociados a esta capa.
La capa de transporte asegura la entrega confiable (o no) de datos entre procesos en dispositivos distintos. Sus funciones incluyen:
•	Segmentación de datos.
•	Control de errores (detección y corrección).
•	Control de flujo (para evitar saturar al receptor).
•	Multiplexación (varios procesos pueden usar la red al mismo tiempo).
•	Reensamblaje de los datos en el receptor.
Protocolos asociados:
•	TCP (Transmission Control Protocol): Protocolo confiable, orientado a conexión.
•	UDP (User Datagram Protocol): No confiable, sin conexión.
Tanto el modelo OSI como TCP/IP tienen una capa de transporte, aunque en OSI es más conceptual y en TCP/IP está más centrada en TCP y UDP.
________________________________________
Pregunta 3: TCP vs. UDP
Compara y contrasta TCP y UDP en términos de:
•	Orientación a conexión
•	Fiabilidad y control de errores
•	Velocidad y orden de entrega
•	Ejemplos de aplicaciones en las que se emplea cada uno
Característica	TCP	UDP
Orientación a conexión	Sí	No
Fiabilidad	Alta (usa ACKs, control de errores, retransmisión)	Baja (no garantiza entrega ni orden)
Velocidad	Más lento	Más rápido
Orden de entrega	Garantizado	No garantizado
Ejemplos de uso	HTTP, HTTPS, FTP, SMTP	DNS, VoIP, streaming, juegos online

Pregunta 4: Protocolo para Transferencia de Archivos
a)	¿Qué protocolo de la capa de aplicación se utiliza tradicionalmente para la transferencia de archivos en redes TCP/IP?
El protocolo tradicional es FTP (File Transfer Protocol).

b)	Menciona al menos dos alternativas a este protocolo, resaltando sus diferencias principales en cuanto a seguridad o funcionalidad.

________________________________________
Pregunta 5: Resolución de Nombres en DNS
Describe detalladamente el proceso de resolución de nombres en DNS, desde que un usuario ingresa una URL en el navegador hasta que se establece la conexión con el servidor web. Incluye en tu respuesta el rol de la caché y de los servidores raíz.
________________________________________
Pregunta 6: Comunicación en el Modelo TCP/IP
Explica el proceso de comunicación entre dos dispositivos en una red utilizando el modelo TCP/IP. Describe el rol y la función de cada capa (Aplicación, Transporte, Internet y Acceso a Red) durante el envío y recepción de datos.
