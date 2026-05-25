# 📋 Terminología Clave en Entornos Industriales 📚

**Terminología** 🛠️
* **Activo (Asset):** Cualquier elemento físico, lógico o humano que tiene valor para la organización y que forma parte del sistema de control (ej. PLCs, SCADAs, redes, ingenieros). 🎛️
* **Vulnerabilidad (Vulnerability):** Debilidad o fallo en el diseño, implementación o configuración de un sistema que puede ser explotada por una amenaza para causar un impacto negativo. 🕳️
* **Amenaza (Threat):** Causa potencial de un incidente no deseado, que puede dañar un sistema u organización (ej. cibercriminales, malware, fallos de hardware). ⚡
* **Riesgo (Risk):** Posibilidad de que una amenaza concreta explote una vulnerabilidad específica, calculada en función de la probabilidad de ocurrencia y el impacto del daño. 📊
* **Impacto (Impact):** Consecuencia o gravedad del daño físico, económico o humano resultante de la materialización de un ataque. 💥

## El Modelo de Referencia de Niveles Purdue 🏛️

**Modelo Purdue (ISA-95 / IEC 62443)** 📶
El Modelo Purdue es el estándar clásico de arquitectura que segmenta las redes industriales en niveles lógicos para proteger el flujo de datos:
* **Nivel 4/5 (Red Corporativa / IT):** Gestión empresarial, ERP, correos y servicios de Internet. 💻
* **Nivel 3 (Sistemas de Operación / OT de Planta):** Monitorización general del sitio, servidores SCADA e históricos de datos (Historians). 🖥️
* **Nivel 2 (Control de Procesos):** Estaciones de Ingeniería, pantallas HMI y consolas de operación local. 📺
* **Nivel 1 (Dispositivos de Control):** Autómatas Programables (PLCs), PACs y controladores lógicos avanzados encargados de la ejecución directa. 🎛️
* **Nivel 0 (Proceso Físico):** Sensores, actuadores, motores y válvulas de campo en contacto real con la producción. ⚙️
* **DMZ (Zona Desmilitarizada Industrial):** Frontera y barrera cortafuegos (Firewall) entre el mundo IT y el mundo OT para el intercambio seguro de datos. 🚧

## Ciberseguridad Industrial: Arquitectura Segura 🧱

**Principios de Red Industrial Protegida** 🛡️
Un entorno industrial moderno requiere que no existan conexiones directas entre la red corporativa y los dispositivos de campo. 🛑 
La infraestructura debe basarse en la **Segmentación de Red**, dividiendo el sistema en "Zonas" (conjuntos de activos con requerimientos de seguridad similares) y "Conductos" (canales de comunicación blindados con firewalls industriales que regulan el tráfico autorizado entre zonas). 🔒📡

## El Cubo de McCumber 🧊

**Cubo de McCumber (Cubo de Seguridad de la Información)** 📐
Es un modelo conceptual tridimensional desarrollado por John McCumber para evaluar y gestionar la seguridad integral de cualquier infraestructura:
1. **Dimensión 1 - Objetivos de Seguridad (La Triada CIA):** Confidencialidad, Integridad y Disponibilidad. 🎯
2. **Dimensión 2 - Estados de la Información:** Datos en Reposo (Almacenamiento), Datos en Tránsito (Transmisión) y Datos en Uso (Procesamiento). 💾📡⚙️
3. **Dimensión 3 - Salvaguardas de Seguridad:** Tecnología (Hardware/Software), Políticas y Prácticas (Normas), y Personas (Educación/Concienciación). 🛠️📜👤

---

# 🧠 Análisis Técnico Estructurado 📊

## 🛡️ 1. Mapeo de la Triada OT (Disponibilidad) en el Cubo de McCumber 🧊

El **Cubo de McCumber** nos permite visualizar de forma integral las debilidades del ecosistema industrial. Mientras que en IT la información se protege principalmente en estado de reposo (cifrando bases de datos), en los sistemas industriales (**OT**) el peligro máximo radica en los **Datos en Tránsito y en Uso** dentro del **Nivel 1 y 2 del Modelo Purdue**:

* **Datos en Tránsito (Modbus TCP, PROFINET):** Históricamente los protocolos industriales carecen de autenticación o cifrado. Si un atacante intercepta el tráfico del *Nivel 1*, puede inyectar falsos comandos de apagado o modificar los setpoints de los procesos. 📉
* **La Salvaguarda Humana:** El cubo demuestra que la tecnología por sí sola (instalar un Firewall en la DMZ) falla si las *Personas* (los operadores de planta) conectan un USB infectado directamente en la estación de ingeniería del *Nivel 2*. 🔌🛑

---

## 🏛️ 2. Zonas, Conductos y la Anatomía de un Ataque según Purdue 📶

El **Modelo Purdue** ya no es solo un mapa de automatización, hoy en día es la base indispensable de la estrategia de **Defensa en Profundidad (IEC 62443)**:

```
[Nivel 4/5: Red IT] ---> Internet / Correos corporativos (Vulnerables a Phishing)
        |
====================== [ INDUSTRIAL DMZ (Firewalls & Proxies) ] ======================
        |
[Nivel 3: SCADA / OT] -> Servidores comprometidos si no hay segmentación dura.
        |
[Nivel 2: HMI / Eng.] -> Estaciones de ingeniería (Riesgo de reprogramación de PLCs).
        |
[Nivel 1: PLCs / RTU] -> Ejecución de lógicas alteradas.
        |
[Nivel 0: Físico]    -> ¡Daño catastrófico en válvulas, motores y reactores! 💥
```

1. **El Aislamiento de la DMZ:** La Zona Desmilitarizada Industrial funciona como un filtro estricto. Si un malware de minería o una APT penetra en la red administrativa corporativa (Nivel 4), la DMZ impide el salto directo hacia la planta de producción. 🛑
2. **Control por Conductos:** Al estructurar la red mediante zonas y conductos, si el panel HMI local (Nivel 2) es infectado por un virus mediante ingeniería social, las reglas estrictas del conducto hacia los PLCs (Nivel 1) evitan el movimiento lateral de la amenaza, confinando el problema y salvando la continuidad del proceso físico (Nivel 0). 🛡️⚙️
