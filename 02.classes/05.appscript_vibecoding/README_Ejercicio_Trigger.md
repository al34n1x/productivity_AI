
# 🧪 Ejercicio: Notificación automática con Triggers en Apps Script

Este ejercicio forma parte del módulo de automatización con Google Apps Script, y está diseñado para demostrar el uso de **triggers** (`onEdit`) para lanzar acciones automáticas al modificar una hoja de cálculo de Google Sheets.

---

## 🎯 Objetivo

Crear una automatización que envíe un email automáticamente cada vez que se edita una fila de la hoja `Solicitudes`, notificando al responsable del cambio en su solicitud.

---

## 📄 Paso 1: Preparar la hoja de cálculo

Crea una hoja de cálculo en Google Sheets con el nombre `Solicitudes` y la siguiente estructura:

| ID | Nombre | Email | Solicitud | Estado |
|----|--------|-------|-----------|--------|
| 1  | Juan   | juan@email.com | Acceso a Drive | Pendiente |
| 2  | Ana    | ana@email.com  | Creación de cuenta | Aprobado |

---

## 💻 Paso 2: Agregar el script

1. Abrí `Extensiones > Apps Script`
2. Pegá el siguiente código en el editor:

```javascript
function onEdit(e) {
  const hoja = e.source.getActiveSheet();
  if (hoja.getName() !== "Solicitudes") return;

  const fila = e.range.getRow();
  const email = hoja.getRange(fila, 3).getValue();
  const nombre = hoja.getRange(fila, 2).getValue();
  const solicitud = hoja.getRange(fila, 4).getValue();
  const estado = hoja.getRange(fila, 5).getValue();

  if (!email || !nombre) {
    Logger.log("Faltan datos: email o nombre");
    return;
  }

  Logger.log(`Enviando email a ${email}...`);

  MailApp.sendEmail(email, "Edición detectada", `Hola ${nombre}, notamos una actualización en tu respuesta.`);
}
```

---

## ⚙️ Paso 3: Instalar correctamente el Trigger (muy importante)

El trigger `onEdit(e)` debe ser un **trigger instalable** para poder enviar correos.

### 🧩 Pasos:

1. En el editor de Apps Script, hacé clic en el ícono de reloj (⏰) o desde el menú: `Ver > Triggers`
2. Clic en **"+ Agregar Trigger"** (abajo a la derecha)
3. Configurá los siguientes valores:

   - **Función a ejecutar**: `onEdit`
   - **Origen del evento**: `Desde hoja de cálculo`
   - **Tipo de evento**: `Al editar`

4. Hacé clic en guardar.
5. Otorgá los permisos necesarios cuando lo solicite.

---

## 🚀 Paso 4: Probar la automatización

- Completá los datos de ejemplo en la hoja.
- Modificá el valor de la columna `Estado` de alguna fila.
- Verificá si el destinatario recibe el email.

---


## ✅ Qué aprendiste

- Cómo usar `onEdit(e)` para detectar cambios.
- Cómo instalar correctamente triggers con permisos completos.
- Cómo automatizar el envío de correos en base a una lógica personalizada.

---

## 📚 Recursos útiles

- [Referencia de `onEdit`](https://developers.google.com/apps-script/guides/triggers)
- [Documentación de MailApp](https://developers.google.com/apps-script/reference/mail/mail-app)

---

**Este ejercicio fue desarrollado como parte del curso Productividad con IA**
