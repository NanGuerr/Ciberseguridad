# GitHub Zero Trust

GitHub mediante los principios de **Zero Trust** (confianza cero) y una autenticación robusta es fundamental para proteger el código fuente y la propiedad intelectual.

Aquí tienes una guía estratégica para fortalecer tu postura de seguridad:

---

## 1. Implementación de Autenticación de 2 Factores (2FA) y Más Allá

La autenticación de doble factor es la primera línea de defensa. No basta con activarla; hay que priorizar los métodos más seguros.

* **Exige 2FA para toda tu organización:** Si eres administrador de una organización, ve a *Settings > Security* y marca la opción **"Require two-factor authentication for all members of this organization"**.
* **Prioriza Llaves de Seguridad (FIDO2/WebAuthn):** Los SMS son vulnerables al *SIM swapping*. Utiliza llaves físicas (como YubiKey) o biometría integrada en tu dispositivo (TouchID/Windows Hello). Son resistentes al *phishing*.
* **Gestión de Sesiones:** Revisa regularmente los dispositivos autorizados y revoca el acceso a aquellos que ya no utilices.

---

## 2. Aplicando los Principios "Zero Trust" en GitHub

El concepto "Zero Trust" se resume en: **"Nunca confíes, siempre verifica"**. En el contexto de GitHub, esto implica restringir el acceso al mínimo necesario.

* **Principio de Privilegio Mínimo (Least Privilege):**
* No otorgues acceso de "Admin" a todos los desarrolladores.
* Utiliza **Roles personalizados** para limitar quién puede borrar repositorios, gestionar etiquetas o aprobar *Pull Requests* críticos.


* **Entornos de Despliegue (Environment Protection):**
* Para repositorios críticos, utiliza **"Required reviewers"** en los entornos de despliegue. Esto asegura que nadie pueda desplegar código a producción sin que otro desarrollador autorizado haya verificado los cambios.


* **Segmentación y Visibilidad:**
* Mantén los repositorios privados por defecto.
* Utiliza **GitHub Teams** para granular el acceso a repositorios específicos en lugar de dar acceso a toda la organización.



---

## 3. Seguridad en el Ciclo de Vida del Código

La seguridad no termina con el acceso; el código mismo debe ser auditado automáticamente.

* **GitHub Advanced Security (GHAS):** Si tu empresa cuenta con ella, activa obligatoriamente:
* **Secret Scanning:** Detecta automáticamente si has subido llaves API, tokens o credenciales por error al código.
* **CodeQL:** Analiza el código en busca de vulnerabilidades lógicas (SQL Injection, XSS, etc.).


* **Dependabot:** Automatiza la actualización de dependencias. Muchas brechas ocurren por librerías desactualizadas con vulnerabilidades conocidas.
* **Branch Protection Rules:**
* Configura reglas estrictas: **Requerir aprobación de Pull Request**, **requerir que las comprobaciones de CI pasen** antes de hacer *merge*, y **prohibir el empuje directo (force push)** a ramas protegidas (como `main` o `master`).



---

## 4. Auditoría y Monitoreo Continuo

* **GitHub Audit Logs:** Revisa los logs regularmente. Busca actividades inusuales, como cambios masivos en permisos o accesos desde IPs geográficamente sospechosas.
* **PATs (Personal Access Tokens) vs. Fine-grained Tokens:**
* Deja de usar los antiguos PATs de alcance amplio.
* Migra a **Fine-grained personal access tokens**, que permiten definir exactamente a qué repositorios puede acceder el token y qué permisos específicos (lectura/escritura) tiene.



---

## Resumen de Mejores Prácticas

| Área | Acción Prioritaria |
| --- | --- |
| **Acceso** | Forzar llaves de seguridad físicas (WebAuthn). |
| **Permisos** | Auditoría trimestral de acceso a repositorios (Least Privilege). |
| **Código** | Activar Secret Scanning y Branch Protection. |
| **Dependencias** | Mantener Dependabot activo y configurado. |

---

¿Te gustaría que profundizara en cómo configurar las reglas de protección de ramas o en cómo gestionar los tokens de acceso de manera más segura para flujos de automatización (CI/CD)?
