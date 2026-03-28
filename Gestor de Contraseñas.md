## 🛠️ Parte 1: Configuración de un Gestor de Contraseñas (Bitwarden / KeePassXC)

Un gestor de contraseñas no solo guarda tus claves; las **genera** de forma aleatoria (ej. `f7!zP9&Lq@2mXv*S`) para que cada sitio tenga una llave distinta.

### Pasos para un despliegue seguro:
1.  **La Contraseña Maestra (Master Password):** Es la única que memorizarás. Debe ser una **frase** larga (4-5 palabras aleatorias) como `Gato-Azul-Salta-2026!`. No la anotes en digital, solo en papel físico guardado en un lugar seguro.
2.  **Importación y Limpieza:** Instala la extensión en tu navegador. Ve a la configuración de Chrome/Edge/Safari, exporta tus contraseñas guardadas (si tienes) al gestor y luego **bórralas del navegador**. Los navegadores son menos seguros que un gestor dedicado.
3.  **Doble Factor (2FA) en el Gestor:** Esto es vital. Si alguien adivina tu contraseña maestra, aún necesitará tu código de Google Authenticator o tu YubiKey para entrar.
4.  **Autocompletado:** El gestor detecta la URL exacta. Si estás en una página falsa (ej. `g00gle.com`), el gestor **no autocompletará** tus datos. Esto es una defensa automática contra el phishing.

---

## 🎣 Parte 2: Cómo detectar Phishing Profesional

Hoy en día, los correos falsos no tienen mala ortografía; usan IA para sonar perfectos. Aquí es donde debes aplicar la "Duda Metódica":

### 1. La técnica del "Hover" (Pasar el ratón)
Antes de hacer clic en cualquier botón de "Restablecer contraseña" o "Ver factura":
* **En PC:** Pasa el cursor sobre el enlace (sin hacer clic). Mira la esquina inferior izquierda de tu navegador. Si el texto del botón dice `Seguridad-Apple.com` pero el enlace real apunta a `bit.ly/xyz` o `servidor-ruso.net`, es un ataque.
* **En Móvil:** Mantén presionado el enlace para que aparezca la vista previa de la URL real.

### 2. Remitente vs. Dominio
No te fíes del nombre que aparece (ej. "Soporte de Microsoft"). Haz clic en la dirección de correo para verla completa:
* ✅ **Real:** `support@microsoft.com`
* ❌ **Falso:** `support@microsoft-security-update.com` (Usa un subdominio engañoso).
* ❌ **Falso:** `no-reply@micosoft.com` (Typosquatting: falta una "r").

### 3. El Sentido de Urgencia Artificial
El phishing siempre intenta que entres en pánico para que no pienses:
* *"Tu cuenta será bloqueada en 2 horas".*
* *"Se ha realizado una compra de $2,000, haz clic aquí si no fuiste tú".*
* *"Último aviso de la Agencia Tributaria".*

> [!IMPORTANT]
> **Regla de Oro:** Si recibes un correo alarmante de tu banco o de Google, **nunca** hagas clic en el enlace del correo. Cierra el email, abre tu navegador, escribe manualmente la dirección oficial (ej. `bbva.com`) e inicia sesión desde ahí.

---

## 🚀 Próximo Paso Recomendado

Para ver qué tan expuesto estás ahora mismo, **¿te gustaría que te explique cómo usar herramientas como `Have I Been Pwned` para ver si tus datos ya están en la Dark Web?**

Por cierto, para desbloquear la funcionalidad completa de todas las aplicaciones, habilita la [actividad en las aplicaciones de Gemini](https://myactivity.google.com/product/gemini).
