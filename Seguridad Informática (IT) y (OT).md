# Ciberseguridad Industrial (OT) vs. Seguridad Informática (IT) 🛡️🏭

## 1. Definiciones Fundamentales y Pirámide de Seguridad 📐
La relación entre los distintos entornos de seguridad se estructura en forma de pirámide dependiente, donde la base sostiene las capas superiores:

* **Seguridad Física 🏢 (Base):** La protección del entorno e infraestructura tangible. Sin seguridad física, las capas lógicas pierden efectividad.
* **Seguridad IT 💻 (Medio):** *Information Technology*. Enfocada en tecnologías y aplicaciones convencionales para el manejo, almacenamiento y transmisión de la información corporativa.
* **Seguridad OT ⚙️ (Cúspide):** *Operations Technology*. Enfocada en tecnologías y aplicaciones directamente relacionadas con los **Sistemas de Control Industrial (ICS)** que interactúan con el mundo físico.

---

## 2. Diferencias Críticas entre IT y OT 📊

| Criterio | Tecnologías de la Información (IT) 💻 | Tecnologías de la Operación (OT) ⚙️ |
| :--- | :--- | :--- |
| **Mayor Riesgo** | Pérdida de datos corporativos y demoras/pausas en los procesos administrativos. | **Pérdida de vidas humanas**, impactos ambientales catastróficos, daños severos a equipos físicos y parada total de producción. |
| **Recursos** | Alta disponibilidad de recursos de hardware (memoria, capacidad de procesamiento, ancho de banda escalable). | Hardware específico de los ICS con **recursos limitados** y ciclos de vida muy largos. |
| **Sistemas y Protocolos** | Sistemas operativos comerciales y protocolos de red completamente estándar. | Sistemas operativos y protocolos estándar combinados con **protocolos propietarios y específicos de ICS**. |

---

## 3. Pirámide de Automatización Industrial (Modelo de Referencia) 🏗️
El entorno industrial se segmenta tradicionalmente en 5 niveles de criticidad y operación (asociados comúnmente al modelo de Purdue):

* **Nivel 4: Red de Información (ERP)** 👔 -> Tecnologías de Información superiores (Gestión empresarial).
* **Nivel 3: Red de Operación (MES)** 📈 -> Tecnologías de Operación (Gestión y ejecución de la producción).
* **Nivel 2: Red de Supervisión (SCADA, HMI)** 🖥️ -> Monitorización y control visual del estado de la planta.
* **Nivel 1: Red de Control (PLC, DCS)** 🎛️ -> Cerebros lógicos que ejecutan las instrucciones de automatización.
* **Nivel 0: Red de Campo (Instrumentación)** 🔌 -> Sensores, válvulas y motores (actuación física).

---

## 4. Impactos en la Ciberseguridad Industrial ⚠️
Los incidentes en OT se miden bajo una escala de **gravedad creciente**, donde las consecuencias digitales escalan hacia daños físicos severos:

1.  🔓 Acceso no autorizado, robo o uso indebido de información.
2.  📉 Pérdida de integridad, disponibilidad o confiabilidad del sistema de control.
3.  💥 Daño directo a los equipos e infraestructura de la planta.
4.  🏢 Afectación severa a la imagen y reputación de la empresa.
5.  ⚖️ Violación de normas legales y regulaciones ambientales/industriales.
6.  🌱 Daños y desastres ambientales en el entorno de la planta.
7.  💀 **Lesiones graves o muerte de personas** (Máximo nivel de gravedad).

---

## 5. Estrategia de Mitigación: Defensa en Profundidad (DiD) 🏰
Para abordar de manera integral las vulnerabilidades en IT y OT se utiliza un enfoque de **Protección en Capas**:

* **Capa de Gestión 📋:** Políticas de seguridad corporativas, auditorías periódicas y cumplimiento estricto de normativas internacionales.
* **Capa en la Nube ☁️:** Definición clara de la matriz de responsabilidad compartida entre el proveedor cloud y el usuario final.
* **Capa de Usuario 👤:** Autenticación fuerte (MFA / 2FA), programas continuos de educación y concienciación sobre ingeniería social y buenas prácticas.
* **Capa de Aplicación y Endpoints 🛡️:** Firewalls basados en software, soluciones antimalware avanzadas y políticas estrictas de control de accesos a aplicaciones.
* **Capa de Datos 🔒:** Encriptación de datos tanto en reposo como en tránsito, sumado a un estricto control de privilegios de acceso.
* **Capa de Red 🌐:** Implementación de Firewalls industriales, sistemas de detección/prevención de intrusiones (IDS/IPS) y una rigurosa **segmentación de redes** (aislando IT de OT).
* **Capa Física 🔑:** Barreras de seguridad física, control de accesos biométrico y resguardo de servidores y salas de control.

---

## 6. Ciclo de Gestión de Vulnerabilidades y Control de Daños 🔄
Cuando las defensas preventivas fallan, se debe activar un marco de resiliencia operativa:

### Abordaje de Vulnerabilidades Preventivas 🔍
* **Monitorización Continua 👁️:** Detección de actividades anómalas en la red industrial en tiempo real.
* **Gestión de Accesos 🆔:** Controles estrictos tanto lógicos como físicos para asegurar que solo personal autorizado manipule activos críticos.
* **Pruebas de Penetración 🛠️:** Realización de auditorías y pentesting adaptados a entornos industriales para identificar y remediar brechas de manera segura.

### Plan de Control de Daños ante Incidentes 🚨
1.  📄 **Planes de Respuesta a Incidentes:** Activación inmediata de los manuales de procedimiento detallados.
2.  🚧 **Contención:** Aislar y detener el ataque en curso de manera inmediata para evitar su propagación horizontal.
3.  🔄 **Recuperación:** Restauración segura de los sistemas operativos y datos afectados a su estado óptimo de operación.
4.  🗣️ **Comunicación:** Notificación transparente a las partes interesadas (empleados, clientes, entes reguladores).
5.  🕵️‍♂️ **Investigación:** Análisis forense detallado del incidente para determinar la causa raíz y el alcance real.
6.  🧠 **Lecciones Aprendidas:** Documentación rigurosa de los hallazgos para robustecer la arquitectura de seguridad de cara al futuro.
