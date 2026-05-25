# 🛡️ Tipos de Ataques e Interceptación de Datos en Redes 🔐

Este documento contiene técnicas, las cuales describen de manera esquemática los vectores de ataque más comunes en redes, la interceptación de tráfico y las vulnerabilidades de comunicación.

---

## 🥷 1. Ataque de Interceptación / Man-in-the-Middle (MitM)

El núcleo de las imágenes ilustra de manera didáctica el concepto de **Man-in-the-Middle (Hombre en el medio)**, un tipo de ataque diseñado para romper la confidencialidad de una comunicación directa entre dos terminales legítimos.

### 🔄 Mecanismo de Operación
1.  **🗣️ Comunicación Legítima Original:** El **Emisor (Usuario A)** intenta enviar información de forma directa al **Receptor (Usuario B)** (por ejemplo, credenciales de acceso, transacciones bancarias o paquetes de control industrial).
2.  **🕵️ Interceptación de la Línea:** Un **Intruso / Atacante** logra posicionarse físicamente o lógicamente en el canal de comunicación intermedio (mediante técnicas como *ARP Spoofing*, envenenamiento DNS o hackeo de routers).
3.  **📇 Acciones del Atacante:**
    * **Lectura Activa:** Rompe la privacidad visualizando los datos en texto plano.
    * **Alteración de Contenido:** El atacante no solo escucha, sino que puede **modificar la carga útil (*payload*)** del mensaje antes de redirigirlo al receptor real, haciendo que el receptor ejecute órdenes falsas creyendo que provienen de la fuente legítima.

---

## 💻 2. Ataques Pasivos vs. Ataques Activos en Redes

A partir de los esquemas de flujo e interceptación expuestos en las diapositivas, se clasifica el impacto en la seguridad en dos grandes vertientes:

### 📑 A. Ataques Pasivos (Escucha Atenta)
* **🎯 Objetivo:** Obtener información que está siendo transmitida sin alterar los recursos del sistema.
* **🛠️ Métodos Comunes:** *Sniffing* (captura de paquetes de red mediante herramientas como Wireshark), análisis de tráfico para identificar patrones de comportamiento o extracción de contraseñas no cifradas (HTTP, Telnet, FTP).
* **🔍 Dificultad de Detección:** Extremadamente alta debido a que el canal sigue operando de forma normal sin caídas ni retardos notables. Su mitigación principal es el **uso mandatorio de cifrado fuerte (HTTPS, SSH, VPN)**.

### 💥 B. Ataques Activos (Modificación y Daño)
* **🎯 Objetivo:** Alterar intencionalmente el flujo de datos, suplantar identidades o degradar/destruir la disponibilidad de los servicios.
* **🛠️ Métodos Comunes:**
    * **Suplantación de Identidad (Spoofing):** El atacante finge ser un nodo de confianza.
    * **Modificación de Mensajes:** Alteración de los bits en tránsito dentro de la trama de red.
    * **Denegación de Servicio (DoS/DDoS):** Inundación de peticiones para colapsar los servidores legítimos.

---

## ☣️ 3. Vectores de Inyección y Vulnerabilidades de Software

Las imágenes técnicas hacen referencia a los métodos con los cuales un atacante externo logra que el hardware ejecute código malicioso de forma remota:

* **💉 Inyección de Código / SQL Injection:** Aprovecha la falta de validación en los formularios o entradas de texto para inyectar scripts maliciosos directos a la base de datos o sistema operativo.
* **📡 Escaneo de Puertos y Reconocimiento:** Fase previa donde se buscan puertos abiertos vulnerables (ej. Puerto 21-FTP, 23-Telnet, 445-SMB) para explotar fallos conocidos de desbordamiento de búfer (*Buffer Overflow*).

---

## ⚖️ Cuadro Comparativo de los Mecanismos de Ataque Ilustrados

| Tipo de Ataque | Objetivo Principal | Impacto en la Tríada CIA | Ejemplo Técnico | Método de Defensa |
| :--- | :--- | :--- | :--- | :--- |
| **Intercepción (MitM) 🕵️** | Leer y modificar datos en tránsito. | Confidencialidad e Integridad | *ARP Poisoning* / Redes Wi-Fi públicas abiertas. | Cifrado SSL/TLS, Certificados Digitales. |
| **Modificación Activa 💥** | Cambiar el contenido del mensaje. | Integridad | Inserción de comandos falsos en un bus Modbus/TCP. | Firmas digitales, Checksum criptográfico (HMAC). |
| **Interrupción / DoS ❌** | Bloquear el acceso al servicio. | Disponibilidad | Inundación de paquetes SYN (*SYN Flood*). | Firewalls avanzados, IDS/IPS, Balanceadores de carga. |

---
*Nota: Este análisis técnico de ciberseguridad destaca la criticidad de asegurar la capa de enlace y transporte frente a accesos físicos o lógicos no autorizados dentro de la infraestructura de red.* 🛡️💻

## 🛑 4. Ataques de Denegación de Servicio (DoS) y Denegación de Servicio Distribuida (DDoS)

Las imágenes representan el flujo de colapso de infraestructura mediante el envío masivo de tráfico no solicitado.

### 🔌 A. Denegación de Servicio (DoS - Denial of Service)
* **🎯 Mecanismo:** Un único equipo atacante con alta capacidad de procesamiento o ancho de banda inunda directamente a un **Servidor/Víctima** con peticiones falsas (por ejemplo, inundación de paquetes *ICMP Echo Request* o *SYN Flood*).
* **💥 Impacto:** Los recursos del sistema de la víctima (Memoria RAM, CPU, ancho de banda de red) se agotan por completo intentando procesar las solicitudes falsas, provocando el colapso del sistema y dejando fuera de servicio a los usuarios legítimos.

### 🤖 B. Denegación de Servicio Distribuida (DDoS - Distributed Denial of Service)
* **🎯 Mecanismo:** El atacante no opera solo; toma el control de una red de dispositivos previamente infectados conocidos como **Zombis (Bots)**, conformando una **Botnet**.
* **🔀 Flujo del Ataque:** El atacante envía un comando centralizado de ejecución. Cientos o miles de nodos distribuidos geográficamente atacan en simultáneo al mismo servidor objetivo.
* **🔍 Dificultad de Mitigación:** Al provenir de múltiples direcciones IP legítimas dispersas en todo el mundo, bloquear el ataque mediante reglas de firewall tradicionales por IP se vuelve sumamente complejo.

---

## 🎭 5. Ataques de Suplantación de Identidad (Spoofing)

Las láminas esquematizan el fraude de identidad a nivel de red, donde una entidad maliciosa enmascara sus datos para ganarse la confianza del sistema.

* **🌐 IP Spoofing (Suplantación de IP):** El atacante altera el encabezado de los paquetes de red reemplazando su dirección IP real por una IP de confianza perteneciente a la red interna. De este modo, los Firewalls o Listas de Control de Acceso (ACL) permiten el paso del paquete sin restricciones.
* **📬 Correo Electrónico / Email Spoofing:** Alteración de las cabeceras de un correo electrónico para que parezca haber sido enviado por un remitente legítimo conocido (como un administrador de sistemas, soporte técnico o una entidad bancaria).

---

## 🎣 6. Ingeniería Social y Phishing

Varios de los diagramas analizados mapean cómo el factor humano sigue siendo explotado para vulnerar la seguridad técnica.

* **📧 Phishing Tradicional:** Distribución masiva de correos electrónicos falsificados que simulan alertas de seguridad urgentes, links de restablecimiento de contraseñas o facturas pendientes.
* **💾 Carga Útil Maliciosa (Malicious Payload):** El correo convence al usuario de realizar dos acciones críticas:
    1.  **🔗 Hacer clic en un enlace:** Redirige a un portal web clonado diseñado para capturar credenciales de acceso (robo de identidad).
    2.  **📂 Descargar un archivo adjunto:** Comúnmente ejecutables ocultos, macros de Office o scripts que, al ejecutarse, instalan backdoors o troyanos en la estación de trabajo.

---

## 🗄️ 7. Análisis Estructurado de los Vectores de Ataque (5-10)

| Vector de Ataque | Componente Explotado | Objetivo del Atacante | Consecuencia en el Entorno |
| :--- | :--- | :--- | :--- |
| **DoS Individual 🛑** | Recursos de red y CPU del servidor. | Interrumpir el servicio local. | Caída del sistema e inaccesibilidad temporal. |
| **DDoS (Botnets) 🤖** | Ancho de banda de múltiples redes. | Saturar el canal troncal de datos. | Indisponibilidad a gran escala, pérdidas financieras. |
| **IP Spoofing 🎭** | Mecanismos de confianza de capa 3. | Evadir los sistemas de defensa (Firewall). | Acceso no autorizado a segmentos críticos de red. |
| **Phishing / Malware 🎣** | Factor humano (Falta de concientización).| Robo de credenciales e infección inicial. | Compromiso del endpoint y movimiento lateral. |

---
*Nota: Este análisis complementa los conceptos previos de interceptación en tránsito, demostrando que los perímetros de seguridad deben protegerse tanto a nivel logístico-humano como en la resiliencia de la infraestructura ante inundaciones de tráfico.* 🛡️🌐
