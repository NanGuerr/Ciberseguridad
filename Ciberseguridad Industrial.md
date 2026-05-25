# 📋 Transcripción Completa de las Imágenes

## 1. Concepto General 🪓

**¿Qué es el malware?** 🦠
El término "malware" es una abreviatura de "malicious software" (software malicioso). Se refiere a cualquier tipo de software diseñado intencionadamente para causar daños a un ordenador, servidor, cliente o red informática.
Existen muchos tipos diferentes de malware, cada uno con sus propias características y métodos de propagación. 📡

## 2. Virus 🧬

**Virus** 🧫
Un virus informático es un tipo de malware que se replica a sí mismo modificando otros programas informáticos e insertando su propio código. Cuando esta replicación tiene éxito, se dice que las áreas afectadas están "infectadas" con un virus informático. 🧪
Los virus suelen requerir la intervención del usuario para propagarse, como abrir un archivo adjunto infectado en un correo electrónico o ejecutar un programa descargado de Internet. 🖱️

## 3. Gusanos 🪱

**Gusanos (Worms)** 🔌
Un guisano informático es un tipo de malware que se replica a sí mismo para propagarse a otros ordenadores. A diferencia de los virus, los gusanos no necesitan infectar otros programas existentes; en su lugar, son programas independientes que se ejecutan por sí mismos. ⚙️
Los gusanos suelen aprovechar las vulnerabilidades de la red para propagarse de forma automática de un ordenador a otro, lo que les permite extenderse rápidamente por una red informática. 🕳️

## 4. Troyanos 🐴

**Troyano (Trojan Horse)** 🎭
Un troyano es un tipo de malware que se disfraza de software legítimo o útil para engañar a los usuarios y convencerlos de que lo instalen. Una vez instalado, el troyano puede realizar acciones maliciosas en segundo plano, como robar datos, descargar otro malware o dar a un atacante acceso remoto al ordenador infectado. 🕵️‍♂️
A diferencia de los virus y los gusanos, los troyanos no se replican a sí mismos ni infectan otros archivos. 🔒

## 5. Troyanos de Acceso Remoto 🕹️

**RAT (Remote Access Trojan)** 📡
Un RAT (Troyano de Acceso Remoto) es un tipo de malware que permite a un atacante remoto tomar el control total del ordenador infectado. Esto incluye la capacidad de ver la pantalla del usuario, registrar las pulsaciones de teclas (keylogging), acceder a los archivos y carpetas, e incluso activar la cámara web y el micrófono. 👁️
Los RAT se utilizan a menudo para el espionaje, el robo de datos y la realización de ataques dirigidos. 🎯

## 6. Ransomware 🏴‍☠️

**Ransomware** 🔐
El ransomware es un tipo de malware que cifra los archivos del ordenador de la víctima, haciéndolos inaccesibles. A continuación, los atacantes exigen el pago de un rescate (normalmente en criptomonedas) a cambio de la clave de descifrado necesaria para recuperar los archivos. 🪙
El ransomware puede causar graves interrupciones en las empresas y organizaciones, ya que puede bloquear el acceso a sistemas y datos críticos. 📉

## 7. Spyware 🕵️

**Spyware** 🔍
El spyware es un tipo de malware que se instala en el ordenador de un usuario sin su conocimiento y recopila información sobre sus actividades en Internet, hábitos de navegación y datos personales. Esta información se envía luego a un tercero, a menudo con fines publicitarios o de robo de identidad. 💳
El spyware puede ralentizar el rendimiento del ordenador y comprometer la privacidad del usuario. 📉

## 8. Keyloggers ⌨️

**Keylogger** 📝
Un keylogger (registrador de pulsaciones de teclas) es un tipo de software o hardware diseñado para registrar de forma secreta cada tecla que se presiona en un ordenador. Esta información puede incluir contraseñas, números de tarjetas de crédito, mensajes personales y otros datos confidenciales. 🔑
Los keyloggers pueden utilizarse de forma legítima para supervisar la actividad de los empleados o de los hijos, pero los atacantes también los usan con fines maliciosos. 👤

## 9. Contexto Industrial: El Desafío 🏗️

**Ciberseguridad Industrial** 🏭
**¿Por qué la Ciberseguridad Industrial es diferente?** ⚙️
Tradicionalmente, la seguridad informática (IT) se ha centrado en proteger la **confidencialidad** de los datos. En cambio, en los entornos industriales (OT), la prioridad absoluta es garantizar la **disponibilidad y la seguridad** de los procesos físicos. Un ciberataque a una fábrica no solo puede causar pérdidas económicas, sino que también puede poner en peligro la vida de las personas o causar catástrofes medioambientales. 🌋

## 10. Contexto Industrial: El Impacto 🚨

**Ciberseguridad Industrial** ⚠️
**Impacto de un incidente de Ciberseguridad en OT:** 🔥
* **Parada de producción:** 🛑 Pérdidas económicas masivas por la interrupción de la actividad.
* **Daños a los equipos:** 💥 Destrucción física de maquinaria costosa y difícil de reemplazar.
* **Riesgos para la seguridad de las personas:** 🚑 Lesiones o accidentes laborales debidos al mal funcionamiento de los sistemas de control.
* **Impacto medioambiental:** 🌊 Vertidos químicos, emisiones contaminantes u otros desastres provocados por la manipulación de los procesos.

---

# 🧠 Análisis Técnico 📊

## 🛡️ 1. Taxonomía del Malware (Diferencias Clave) 🧬

El material expone de manera clara las sutiles pero vitales diferencias en el comportamiento del código malicioso, las cuales podemos clasificar según su **método de acción**:

| Tipo de Malware 🦠 | ¿Necesita al Usuario? 👤 | ¿Se Replica / Propaga Solo? 🔄 | Objetivo Principal 🎯 |
| --- | --- | --- | --- |
| **Virus** 🧬 | 🟢 Sí (Abrir archivos) | 🟢 Sí (Infecta otros ejecutables) | Destrucción/Alteración de archivos locales. |
| **Gusano** 🪱 | 🔴 No (Aprovecha la red) | 🟢 Sí (De forma automática) | Saturar redes y saltar de PC a PC. |
| **Troyano** 🐴 | 🟢 Sí (Ingeniería social) | 🔴 No | Abrir puertas traseras silenciosamente. |
| **RAT** 🕹️ | 🟢 Sí (Frecuente en troyanos) | 🔴 No | Control total y espionaje en tiempo real. |
| **Ransomware** 🏴‍☠️ | Variable | Variable | Secuestro de datos y extorsión económica. |
| **Spyware / Keylogger** 🔍 | Variable | 🔴 No | Exfiltración de credenciales y datos privados. |

---

## 🏭 2. El Salto al Entorno Industrial: IT vs. OT 🏢

Las dos últimas láminas marcan el punto de inflexión del módulo: **La seguridad en entornos industriales no se maneja igual que en una oficina.** 🎛️

### La Triada de Seguridad Invertida (CIA Triad) 📐

* En **IT (Tecnologías de la Información)** 💻 se prioriza la **Confidencialidad** (que nadie lea los correos o datos bancarios).
* En **OT (Tecnologías de la Operación / Fábricas)** ⚙️ se prioriza la **Disponibilidad** (que el PLC, la turbina o la planta de agua nunca se detengan).

### 🚨 Consecuencias del Éxito del Malware en la Industria 💥

Si un virus común entra a una oficina corporativa, el daño suele limitarse a la pérdida de archivos informáticos. Sin embargo, si ese mismo malware (o uno diseñado a medida, como el histórico *Stuxnet*) cruza la frontera hacia la red de control de la planta (donde viven los PLCs, los paneles SCADA y los bloques de comunicación que hemos visto en TIA Portal), los efectos pasan del mundo digital al **mundo físico**: 🏗️

1. **La inercia destructiva:** 🌪️ Un cambio malicioso en un lazo de control PID puede forzar la apertura de una válvula de presión o apagar los sistemas de refrigeración de un reactor.
2. **El peligro humano y ambiental:** ☣️ Las variaciones descontroladas de los actuadores pueden provocar explosiones, fugas tóxicas o fallos mecánicos que amenazan vidas y ecosistemas.

---

Este material sirve como un excelente marco teórico 📚 para entender por qué los controladores industriales modernos (como la familia S7-1500 de Siemens) integran hoy en día funciones avanzadas de protección de acceso, contraseñas de bloque y firmas digitales para repeler este tipo de ataques. 🛡️
