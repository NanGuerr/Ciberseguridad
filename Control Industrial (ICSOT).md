# 🏭 Seguridad en Sistemas de Control Industrial (ICS/OT) 🛡️

La **Seguridad en Sistemas de Control Industrial (ICS)**. El contenido aborda los desafíos de la convergencia IT/OT, las vulnerabilidades nativas de los dispositivos de campo y las mejores prácticas para establecer perímetros de defensa en infraestructuras críticas.

---

## 🌐 1. La Convergencia IT/OT y sus Desafíos

Tradicionalmente, las redes de **Tecnologías de la Información (IT)** y las de **Tecnologías de Operación (OT)** operaban en mundos completamente aislados (*Air-Gapped*). Las láminas analizan los impactos de la interconexión moderna (Industria 4.0):

* **💻 Entorno IT (Corporativo):** Enfocado en la gestión de datos, servidores de correo, ERPs y confidencialidad. Los ciclos de actualización de hardware y software son rápidos (meses o pocos años).
* **🏭 Entorno OT (Industrial):** Enfocado en el control en tiempo real de procesos físicos (plantas químicas, energía, manufactura). La prioridad absoluta es la **Disponibilidad** y la **Seguridad Física (Safety)**. Los activos (PLCs, DCS, HMIs) tienen ciclos de vida de 15 a 30 años.
* **⚠️ El Riesgo de la Interconexión:** Al conectar la planta a la red corporativa o a internet para obtener métricas de negocio, se abren vectores de ataque que exponen protocolos industriales inseguros a amenazas externas (como ransomware).

---

## 🔍 2. Vulnerabilidades Críticas en Dispositivos ICS

Las imágenes detallan los puntos débiles más comunes en las arquitecturas ICS tradicionales, los cuales suelen ser aprovechados por los atacantes:

* **🗣️ Protocolos sin Cifrado ni Autenticación:** Protocolos como Modbus TCP, EtherNet/IP o PROFINET clásico transmiten sus comandos en texto plano. Cualquier atacante con acceso a la red puede inyectar comandos falsos de parada o arranque (*False Command Injection*).
* **🔑 Credenciales por Defecto y Hardcoded:** Muchos PLCs y controladores de campo antiguos conservan contraseñas de fábrica imposibles de cambiar en el firmware, facilitando el acceso no autorizado.
* **🩹 Dificultad para el Parcheo (Patch Management):** Actualizar el firmware de un dispositivo crítico requiere detener la producción de la planta, lo que genera grandes pérdidas económicas. Por ello, muchos sistemas operan con vulnerabilidades conocidas públicamente durante años.
* **💻 Sistemas Operativos Heredados (Legacy):** Estaciones de ingeniería y servidores SCADA que aún corren sobre Windows XP, Windows 7 o sistemas embebidos obsoletos sin soporte de seguridad.

---

## 🛡️ 3. Estrategias de Defensa y Buenas Prácticas

Para mitigar los riesgos descritos, las láminas proponen un enfoque defensivo adaptado a las restricciones de los entornos industriales:

* **🧱 Segmentación Estricta (Modelo Purdue):** Separar las funciones de la red en niveles claros. Ningún dispositivo de la zona de procesos (Niveles 1 y 2) debe comunicarse directamente con la red corporativa (Nivel 4) o el internet exterior sin pasar por una **DMZ Industrial (Nivel 3.5)**.
* **🚦 Firewalls de Inspección Profunda de Paquetes (DPI):** Utilizar firewalls capaces de entender protocolos industriales. No basta con permitir el puerto TCP 502 (Modbus); el firewall debe validar si el comando específico enviado (ej. *Write Single Register*) está autorizado para ese usuario.
* **👁️ Monitoreo Pasivo y Detección de Intrusiones (IDS):** Dado que el escaneo activo (como `nmap`) puede congelar o tumbar un PLC sensible en funcionamiento, se deben usar herramientas de escucha pasiva en los puertos espejo (*SPAN ports*) de los switches para detectar anomalías de red sin alterar el tráfico.
* **🚫 Control de Accesos Remotos Seguros:** Implementación de autenticación multifactor (MFA) junto con VPNs dedicadas y túneles cifrados para contratistas o ingenieros de soporte que requieran realizar mantenimiento a distancia.

---

## ⚖️ Tabla Comparativa de Prioridades de Seguridad

| Característica | Seguridad IT (Corporativa) 💻 | Seguridad OT / ICS (Industrial) 🏭 |
| :--- | :--- | :--- |
| **Prioridad Principal** | Confidencialidad 🔒 | Disponibilidad e Integridad (Safety) ⚡ |
| **Tiempo de Respuesta** | Tolerancia a retardos (Best-effort) ⏱️ | Tiempo real estricto (Milisegundos) 🚀 |
| **Ciclo de Vida** | Corto (3 - 5 años) 📅 | Largo (15 - 30 años) ⏳ |
| **Estrategia de Pruebas**| Parcheo centralizado inmediato 🛠️ | Pruebas exhaustivas previas en laboratorios aislados 🔬 |

---
*Nota: Proteger un sistema ICS requiere un cambio de paradigma; la ciberseguridad industrial busca garantizar que el proceso físico nunca se detenga de forma imprevista ni ponga en peligro el entorno.* 🏭🛡️

