Ciberseguridad Industrial (OT) 🛡️

¡Bienvenido al repositorio central de **Ciberseguridad en Entornos Industriales**! Este espacio está diseñado para consolidar documentación técnica, marcos de referencia arquitectónicos, guías de robustecimiento (*hardening*) y herramientas de auditoría destinadas a proteger Sistemas de Control Industrial (ICS), SCADA y redes de Tecnologías de la Operación (OT).

---

## 📂 Estructura del Repositorio y Contenidos 🗂️

A continuación, se detallan los archivos clave que componen este repositorio, su propósito técnico y su estado de actualización:

### 📑 Marcos Teóricos y Pilares Fundamentales
* **`Pilares fundamentales.md`** 🧱  
  Explica los conceptos de base de la ciberseguridad industrial. Se enfoca en la inversión de la Triada de Seguridad (CIA), donde la **Disponibilidad** y la **Integridad** física de los procesos tienen prioridad absoluta sobre la Confidencialidad de los datos.
* **`Ciberseguridad Industrial.md`** 🔒  
  Documento maestro introductorio sobre la convergencia IT/OT, los riesgos de la transformación digital (Industria 4.0) y el impacto de los incidentes digitales en el mundo físico.
* **`Purdue y McCumber.md`** 🧊🧪  
  Análisis cruzado que vincula el modelo dimensional de seguridad del **Cubo de McCumber** con la segmentación de redes industriales.
* **`PURDUE.png`** 📶🗺️  
  Diagrama arquitectónico oficial que ilustra el **Modelo de Referencia Purdue (ISA-95 / IEC 62443)**, segmentando desde la Red Corporativa (Niveles 4/5) hasta los dispositivos de campo y sensores del proceso físico (Niveles 1/0).

### 🦠 Gestión de Amenazas y Vulnerabilidades
* **`Amenazas en Ciberseguridad.md`** 🦠🦅  
  Catálogo detallado y taxonomía de vectores de ataque específicos: Malware, Virus, Gusanos, Troyanos, RATs, Ransomware, Spyware, Keyloggers, Adware, Cryptojacking y Amenazas Persistentes Avanzadas (APTs) orientadas a infraestructuras críticas.

### 🛡️ Operaciones, Auditoría y Robustecimiento (Hardening)
* **`Auditoría de exposición.md`** 🔍🌐  
  Metodologías para evaluar la superficie de ataque expuesta a Internet (por ejemplo, mediante Shodan o Censys), detectando PLCs, HMIs o protocolos industriales (Modbus, BACnet, EtherNet/IP) accesibles de forma insegura.
* **`Guía de Hardening.md`** 🧱🛠️  
  Manual práctico de endurecimiento para activos industriales: deshabilitación de servicios innecesarios, cierre de puertos, firma digital de firmwares y configuración segura de controladores de automatización (como familias Siemens S7-1500).
* **`Checklist de Seguridad.md`** 📋✅  
  Lista de verificación rápida para auditorías en planta basadas en las normas internacionales **IEC 62443** y **NIST SP 800-82**.
* **`Gestor de Contraseñas.md`** 🔑🎛️  
  Directrices para mitigar uno de los mayores problemas en OT: las credenciales por defecto o *hardcodeadas*. Propone políticas de rotación de claves para cuentas de mantenimiento en el Nivel 1 y 2 de Purdue.

---

## 🏛️ Arquitectura de Seguridad Implementada 📶

El repositorio promueve el diseño de estrategias basadas en la **Defensa en Profundidad**:

1. **Segmentación Estricta (Modelo Purdue):** Ningún dispositivo de campo (Nivel 1/0) debe comunicarse de forma directa con la red IT corporativa (Nivel 4).
2. **Zonas y Conductos (IEC 62443):** Agrupación de activos con criticidad similar y blindaje de los canales de comunicación inter-zona mediante firewalls industriales y zonas desmilitarizadas (**Industrial DMZ**).
3. **Determinismo en Tiempo Real:** Las salvaguardas tecnológicas y de escaneo implementadas nunca deben interferir con los ciclos de reloj críticos de los lazo de control PID de la planta.

---

## 📜 Estándares de Referencia Utilizados 📚
* **ISA/IEC 62443:** Seguridad de sistemas de automatización y control industrial.
* **NIST SP 800-82:** Guía de seguridad para Sistemas de Control Industrial (ICS).
* **ISO/IEC 27001:** (Adaptado en el perímetro IT) Gestión de la seguridad de la información.

---

## 👥 Contribuciones y Buenas Prácticas 🛠️
Si deseas colaborar añadiendo nuevas guías de hardening para marcas específicas (Rockwell, Schneider, Siemens) o nuevos vectores de amenaza identificados en la industria:
1. Haz un **Fork** del proyecto.
2. Crea una rama dedicada a la característica (`git checkout -b feature/NuevaAmenaza`).
3. Sube tus cambios estructurados en Markdown (`.md`).
4. Abre un **Pull Request** detallando el impacto del cambio en entornos de producción física (OT).

---
*Nota: La seguridad física de los operadores humanos y la protección del medio ambiente son los objetivos finales de cada línea de configuración documentada en este repositorio.* 👷‍♂️🌳🛡️
