## 🕵️‍♂️ Paso 1: El Chequeo de Correo (HIBP)

1.  Ve a [haveibeenpwned.com](https://haveibeenpwned.com).
2.  Introduce tu correo principal.
3.  **Resultados:**
    * **Verde:** Estás limpio (por ahora).
    * **Rojo ("Oh no — pwned!"):** Tus datos han sido filtrados en una o más brechas de seguridad.

### ¿Qué hacer si sale rojo?
No entres en pánico, pero actúa. Baja hasta la sección **"Breaches you were pwned in"**. Ahí verás el nombre de la empresa y, lo más importante, **qué datos se filtraron** (Email, Passwords, Phone numbers). 
> **Acción inmediata:** Si usabas esa misma contraseña en otros sitios (banco, redes sociales), **cámbiala ya** en todos ellos usando el gestor de contraseñas que configuramos antes.

---

## 🔑 Paso 2: El Chequeo de Contraseñas

HIBP tiene una base de datos de casi **mil millones** de contraseñas expuestas.
1.  En el menú superior de la web, haz clic en **"Passwords"**.
2.  Escribe una contraseña que uses habitualmente (es seguro, el sitio usa un método llamado *k-Anonymity* para que ellos nunca vean tu clave real).
3.  Si dice que ha sido vista **"15,234 times"**, esa contraseña es **completamente inútil**. Un hacker la tiene en su "diccionario" de ataques automáticos y entrará en tu cuenta en milisegundos.

---

## 📱 Paso 3: ¿Tu número de teléfono está expuesto?

A veces los hackeos (como el famoso de Facebook de hace unos años) filtran números de teléfono vinculados a nombres reales. 
* En la página principal de HIBP, puedes probar introduciendo tu número en formato internacional (ej. `+34600000000` o `+521...`).
* **Riesgo:** Si tu número está filtrado, eres un blanco perfecto para ataques de **Smishing** (SMS falsos) o intentos de **SIM Swapping**.

---

## 🛡️ Tu Plan de Acción "Post-Filtración"

Si descubres que tus datos están circulando por ahí, sigue este orden:

1.  **Prioridad Alta:** Cambia la contraseña de tu **Correo Electrónico Principal**. Si un hacker tiene tu correo, puede "restablecer" la contraseña de cualquier otra cuenta.
2.  **Activa el 2FA:** Aunque tengan tu contraseña filtrada, el Segundo Factor de Autenticación (la app de códigos) les impedirá entrar.
3.  **Alertas de Google/Apple:** Activa las notificaciones de "Contraseña filtrada" en los ajustes de seguridad de tu cuenta de Google o en el Llavero de iCloud. Ellos te avisarán proactivamente en el futuro.

---

### 💡 Un truco avanzado: "Honey Pots" personales
La próxima vez que te registres en una web que no te de mucha confianza, usa un alias (como vimos en el archivo `.md`). Por ejemplo: `tu-nombre+nombredelaweb@gmail.com`. 
Si de repente empiezas a recibir spam a esa dirección específica, **ya sabes exactamente quién vendió tus datos o quién fue hackeado.**
