# ☣️ Amenazas Derivadas e Impactos en Sistemas de Control Industrial 💥

**Amenazas Derivadas**. El contenido se enfoca en clasificar la naturaleza de los ataques informáticos, las técnicas de alteración de datos (Falsificación) y las consecuencias operativas de un ciberincidente en entornos de automatización.

---

## 🎭 1. Clasificación Fundamental de los Ataques

Las láminas diferencian claramente los dos tipos primarios de comportamiento ofensivo que un adversario puede desplegar contra las redes industriales:

### 📥 A. Ataques Pasivos
* **Definición:** Su propósito es la interceptación de datos y el monitoreo de las comunicaciones sin alterar los recursos del sistema.
* **Acciones Típicas:** *Eavesdropping* (escucha furtiva), análisis del perfil de tráfico, captura de credenciales y descubrimiento de la topología de red.
* **Características:** Son extremadamente difíciles de detectar porque no alteran el funcionamiento operacional ni inyectan paquetes anómalos. Su peligro radica en que actúan como la fase de reconocimiento de un ataque mayor.

### 📤 B. Ataques Activos
* **Definición:** Implican la alteración directa de los recursos del sistema, la inyección de datos modificados o la interrupción deliberada del flujo normal de operación.
* **Acciones Típicas:** Suplantación de identidad (*Masquerade*), retransmisión de mensajes viejos (*Replay Attacks*), modificación del código del PLC o ataques de Denegación de Servicio (DoS).
* **Características:** Tienen un impacto físico inmediato, provocando desde la parada no programada de una línea de producción hasta daños mecánicos catastróficos.

---

## 🧠 2. Amenazas Derivadas en la Integridad de Datos

Las láminas analizan con detalle el fenómeno de la **Falsificación de Información (Falsification)**, dividiéndolo en tres vertientes de alto riesgo para los lazos de control PID y sistemas SCADA:

1.  **📊 Falsificación de Datos del Proceso (False Data Injection):** El atacante altera las lecturas que envían los sensores hacia el PLC. Por ejemplo, modifica la señal de un sensor de temperatura para hacerle creer al controlador que el sistema está frío, induciendo un sobrecalentamiento real.
2.  **🎮 Falsificación de Comandos de Control (False Command Injection):** Modificación del tráfico legítimo para enviar instrucciones no autorizadas directas a los actuadores. Un ejemplo es forzar la apertura de una válvula de alivio de presión o detener un motor crítico de forma abrupta.
3.  **📺 Falsificación del Estado de la Planta (Feedback Spoofing):** Inyección de datos manipulados hacia la HMI del operador humano. Mientras la planta está siendo saboteada físicamente en el campo, el operador ve gráficos normales en sus pantallas, retrasando la activación de paradas de emergencia manuales (estrategia idéntica a la usada por *Stuxnet*).

---

## 📉 3. Consecuencias e Impactos en el Entorno Operacional (OT)

A diferencia del entorno IT tradicional, donde el impacto se mide en pérdida de datos o de privacidad, las consecuencias en sistemas ICS impactan el mundo físico:

* **⛔ Parada de Producción (Downtime):** Interrupción de los servicios o líneas de manufactura que provoca pérdidas económicas masivas por cada minuto fuera de servicio.
* **⚙️ Daños Físicos a Activos Críticos:** Destrucción física de turbinas, compresores, calderas o reactores debido a la manipulación maliciosa de sus umbrales de seguridad operativos (*Safety Interlocks*).
* **☣️ Desastres Medioambientales:** Fugas de químicos tóxicos, derrames de petróleo o emisiones incontroladas de gases debido a fallos inducidos en los lazos automáticos de control ambiental.
* **⚠️ Riesgos contra la Vida Humana (Safety):** El impacto más severo de un ciberataque industrial es la posibilidad de generar explosiones, incendios o liberaciones de energía que atenten directamente contra la vida de los operadores de planta.

---

## ⚖️ Matriz de Mitigación para Amenazas Derivadas

| Tipo de Amenaza Derivada | Impacto Técnico | Contramedida de Ingeniería |
| :--- | :--- | :--- |
| **Ataque Pasivo (Escucha) 📥** | Pérdida de Confidencialidad / Espionaje. | Implementación de protocolos cifrados (ej. OPC UA con firmas digitales). |
| **Inyección de Comandos Falsos 🎮**| Acciones no autorizadas sobre actuadores. | Autenticación a nivel de red y segmentación estricta por zonas. |
| **Feedback Spoofing (Falsificación HMI) 📺**| Cegado de los operadores humanos. | Sistemas redundantes de validación cruzada e IDS de comportamiento de planta. |
| **Denegación de Servicio (DoS) 🛑** | Pérdida de visibilidad y control en tiempo real. | Configuración de límites de tasa (*Rate Limiting*) en switches y firewalls industriales. |

---
*Nota: Este análisis técnico concluye que las amenazas derivadas en entornos industriales representan un riesgo multidimensional donde la ciberseguridad se intersecta directamente con la seguridad industrial y física (Safety).* 💥🏭🛡️
