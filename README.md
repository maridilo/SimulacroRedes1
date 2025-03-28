# SimulacroRedes1
https://github.com/maridilo/SimulacroRedes1.git

# Redes de Computadoras - Parte I: Conceptos y Teoría

## Pregunta 1: Modelos OSI y TCP/IP

### a) Diferencias principales

El modelo OSI (Open Systems Interconnection) y el modelo TCP/IP (Transmission Control Protocol/Internet Protocol) son dos arquitecturas de red que explican cómo se comunican los sistemas a través de una red.

- El modelo OSI tiene **siete capas**: Física, Enlace de Datos, Red, Transporte, Sesión, Presentación y Aplicación.
- El modelo TCP/IP tiene **cuatro capas principales**: Acceso a la red, Internet, Transporte y Aplicación.

El modelo OSI fue desarrollado por la ISO como un marco teórico, ideal para enseñar y estandarizar. En cambio, el modelo TCP/IP fue diseñado con fines prácticos, basado en protocolos reales que funcionan en Internet.

En el modelo OSI, las funciones de la capa de aplicación están separadas en tres capas: Aplicación, Presentación y Sesión. En TCP/IP, todas estas funciones están integradas en una sola capa de Aplicación.

### b) Ventajas y limitaciones

El modelo OSI es útil para estudiar y entender redes, gracias a su estructura clara y modular. Sin embargo, no se usa directamente en la práctica.

El modelo TCP/IP, por el contrario, se basa en la realidad de las redes y es la base de Internet. Su desventaja es que no separa tan claramente las funciones, lo que puede dificultar el análisis teórico.

---

## Pregunta 2: Función de la Capa de Transporte

La capa de transporte se encarga de garantizar que los datos lleguen correctamente desde una aplicación en un dispositivo hasta otra aplicación en un dispositivo remoto. 

Sus funciones principales son:

- **Segmentación y reensamblaje** de datos.
- **Control de errores** mediante verificación y retransmisión.
- **Control de flujo** para evitar que el emisor sature al receptor.
- **Multiplexación** para permitir varias comunicaciones simultáneas.
- **Control de congestión** para evitar saturar la red.

Los protocolos principales en esta capa son:

- **TCP (Transmission Control Protocol):** proporciona comunicación confiable, orientada a conexión.
- **UDP (User Datagram Protocol):** más rápido, sin conexión y sin garantía de entrega.

---

## Pregunta 3: TCP vs. UDP

**TCP** es un protocolo orientado a la conexión. Antes de enviar datos, se establece una conexión mediante un "handshake". Es confiable: garantiza que los datos lleguen completos y en orden. Además, incluye mecanismos de control de errores, flujo y congestión. Es más lento, pero ideal para aplicaciones como navegación web (HTTP/HTTPS), correo electrónico (SMTP), y transferencia de archivos (FTP).

**UDP**, por otro lado, es un protocolo no orientado a conexión. No establece una conexión previa ni garantiza que los datos lleguen ni que lleguen en orden. Es más rápido y ligero. Se utiliza en aplicaciones donde la velocidad es más importante que la precisión, como juegos en línea, videollamadas (VoIP) o streaming de video.

---

## Pregunta 4: Protocolo para Transferencia de Archivos

### a) Protocolo tradicional

El protocolo tradicional utilizado para la transferencia de archivos en redes TCP/IP es **FTP (File Transfer Protocol)**. Este permite la subida, descarga y gestión de archivos, pero no cifra los datos ni las credenciales, lo que supone un riesgo de seguridad.

### b) Alternativas

1. **SFTP (SSH File Transfer Protocol):** Transfiere archivos de forma segura usando el protocolo SSH. Todo el tráfico se cifra, incluyendo comandos y datos.

2. **FTPS (FTP Secure):** Es una versión de FTP que añade cifrado mediante SSL/TLS. También cifra los datos y credenciales, aunque puede requerir configuraciones adicionales.

---

## Pregunta 5: Resolución de Nombres en DNS

Cuando el usuario escribe una URL en el navegador, el sistema necesita traducir ese nombre de dominio a una dirección IP mediante DNS (Domain Name System).

1. Primero se consulta la **caché local** del sistema o navegador.
2. Si no se encuentra, se consulta al **servidor DNS configurado**.
3. Si este no conoce la respuesta, realiza una **consulta recursiva**:
   - Pregunta a un **servidor raíz**.
   - Este responde con el **servidor TLD** correspondiente (como `.com`).
   - El servidor TLD remite al **servidor autoritativo** para el dominio.
   - Este proporciona la **dirección IP** del dominio buscado.
4. El navegador recibe la IP y establece la conexión con el servidor web.
5. La IP se guarda temporalmente en la caché para futuras consultas.

---

## Pregunta 6: Comunicación en el Modelo TCP/IP

La comunicación entre dos dispositivos en una red siguiendo el modelo TCP/IP implica cuatro capas:

1. **Capa de Aplicación:** Es donde actúan los programas como navegadores y clientes de correo. Utiliza protocolos como HTTP, SMTP o FTP.

2. **Capa de Transporte:** Proporciona la conexión entre procesos. TCP o UDP empaquetan los datos en segmentos.

3. **Capa de Internet:** Se encarga del direccionamiento y enrutamiento. Aquí los datos se encapsulan en paquetes IP con la dirección IP del destino.

4. **Capa de Acceso a Red:** Transmite físicamente los datos por la red (cable, Wi-Fi). Encapsula los paquetes en tramas y los envía al hardware de red.

Cuando los datos llegan al destino, se desencapsulan capa por capa hasta ser entregados a la aplicación receptora.

---

