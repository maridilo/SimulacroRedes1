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
# Parte II: Capa Física y Ejercicios Prácticos

## Pregunta 7: Cálculo de Tasa de Transmisión Máxima (Fórmula de Shannon)

### Enunciado:
Calcula la tasa de transmisión máxima para un canal con las siguientes características:

- Ancho de banda: 500 MHz
- SNR: 20 dB

### Paso 1: Convertir SNR de dB a escala lineal

La fórmula para pasar de decibelios (dB) a escala lineal es:
SNR(lineal) = 10^(SNR(dB) / 10)

Sustituyendo:

SNR(lineal) = 10^(20 / 10) = 10^2 = 100

### Paso 2: Aplicar la fórmula de Shannon

Fórmula de Shannon:

C = B × log₂(1 + SNR)

Donde:
- C es la capacidad del canal (bps)
- B es el ancho de banda (Hz)
- SNR es la relación señal/ruido en escala lineal

Convertimos 500 MHz a Hz:

B = 500 × 10^6 Hz

Aplicamos la fórmula:

C = 500 × 10^6 × log₂(1 + 100) C = 500 × 10^6 × log₂(101)

Calculamos el logaritmo en base 2:

log₂(101) ≈ log₁₀(101) / log₁₀(2) ≈ 2.004 / 0.3010 ≈ 6.6582

Entonces:

C ≈ 500 × 10^6 × 6.6582 ≈ 3.329 × 10^9 bps = 3.33 Gbps

**Resultado final:** La tasa máxima de transmisión es aproximadamente **3.33 Gbps**.

---

## Pregunta 8: Ubicación de Portadoras para Eficiencia Espectral

### Enunciado:
- Primera portadora: 1.2 GHz
- Ancho de banda en banda base de cada canal: 300 MHz

### a) Frecuencia de la portadora anterior

Si el ancho de banda de cada canal es de 300 MHz, para evitar solapamientos y optimizar la eficiencia espectral, la separación entre portadoras debe ser de 300 MHz.

Frecuencia de la portadora anterior:

1.2 GHz - 300 MHz = 0.9 GHz

### b) Frecuencia de la portadora posterior

Frecuencia de la portadora posterior:

1.2 GHz + 300 MHz = 1.5 GHz

### Justificación:

La **ubicación adecuada de las portadoras** garantiza que los canales no interfieran entre sí, especialmente en sistemas de multiplexación por frecuencia (FDM). Ubicar las portadoras separadas exactamente por el ancho de banda de cada canal maximiza la **eficiencia espectral**, permitiendo más canales en menos espacio del espectro sin interferencias.

---

## Pregunta 9: Identificación de Modulación en Función del BER

### Enunciado:
Ordena las siguientes modulaciones de mayor a menor robustez ante el ruido (misma SNR):

- BPSK
- QPSK
- 16-QAM
- 64-QAM
- 256-QAM

### Respuesta:

1. **BPSK** (2 símbolos): Más robusta. Cada símbolo representa 1 bit, muy separadas en el espacio de constelación, muy tolerante al ruido.
2. **QPSK** (4 símbolos): Menos robusta que BPSK, pero duplica la eficiencia. 2 bits por símbolo.
3. **16-QAM** (16 símbolos): Cada símbolo representa 4 bits. Mayor eficiencia, menor robustez.
4. **64-QAM** (64 símbolos): 6 bits por símbolo. Muy sensible al ruido.
5. **256-QAM** (256 símbolos): 8 bits por símbolo. Máxima eficiencia, mínima tolerancia al ruido.

### Justificación:

A mayor número de símbolos por baudio (por unidad de tiempo), **menor separación** entre puntos de la constelación y **mayor probabilidad de error** ante ruido. Por tanto, la eficiencia espectral mejora, pero la **robustez disminuye**.

---

## Pregunta 10: Eficiencia del Sistema de Encapsulamiento

### a) Tamaño del mensaje tras añadir cabeceras

- Datos originales (Capa 5): 1.5 KB = 1.5 × 1024 = **1536 bytes**
- Cabecera de Capa 4: 40 bytes
- Cabecera de Capa 3: 40 bytes

**Total:**

1536 + 40 + 40 = 1616 bytes

---

### b) Fragmentación en tramas de 400 bytes

La Capa 2 permite tramas de 400 bytes. Suponiendo que cada trama incluye cabeceras, el total de 1616 bytes debe fragmentarse:

1616 / 400 = 4.04 → Se necesitan 5 tramas

(4 tramas completas y una con el resto)

---

### c) Sobrecarga de la Capa 1 por trama

Cada 2 bytes de datos agregan:

- 1 byte de inicio
- 1 byte de parada
- 1 byte de CRC

Es decir, por cada 2 bytes útiles se transmiten **3 bytes de sobrecarga**.

Para una trama de 400 bytes:

- Número de bloques de 2 bytes: 400 / 2 = 200 bloques
- Sobrexarga total por trama: 200 × 3 = **600 bytes adicionales**

---

### d) Eficiencia del sistema

#### Datos transmitidos totales:

- 5 tramas × 400 bytes = 2000 bytes (datos sin capa física)
- Sobrecarga de capa 1: 5 tramas × 600 bytes = 3000 bytes

**Total transmitido:**  
2000 + 3000 = 5000 bytes

#### Datos útiles originales:

1536 bytes (bloque inicial de Capa 5)

#### Eficiencia:

Eficiencia (%) = (Datos útiles / Total transmitido) × 100 Eficiencia = (1536 / 5000) × 100 ≈ 30.72%

**Resultado final:** La eficiencia del sistema es aproximadamente **30.72%**.

---
