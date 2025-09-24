
# 🧠 Appscript + VibeCoding para Automatizar Gsuite

Este repositorio forma parte del curso **Productividad con Inteligencia Artificial**, donde aprenderás a automatizar tareas repetitivas en Google Workspace usando **Google Apps Script** combinado con **Claude** como asistente generativo.

## 📚 Pre-requisitos

- Cuenta en Gsuite (Gmail, Calendar, Drive, Sheets, etc.)
- Acceso a Internet
- Claude Account (https://claude.ai/)

---

## 🎯 Objetivo

Aprender a crear automatizaciones personalizadas en Gsuite (Gmail, Calendar, Drive, Sheets) con código en Apps Script, utilizando VibeCoding para generar y depurar scripts de manera eficiente.

---

## 🛠️ Contenido del Módulo

### 1. Introducción a Google Apps Script
Google Apps Script es un entorno de scripting basado en JavaScript que permite extender y automatizar funcionalidades de Gsuite.

📘 Recurso:  
- [Documentación oficial de Apps Script](https://developers.google.com/apps-script)

---

### 2. Primer script: Enviar emails desde una hoja de cálculo

**Descripción**:  
Script que lee una hoja de cálculo y envía emails a las direcciones de email contenidas.

🧪 **Ejercicio**:  
- Crear una hoja llamada `Respuestas` con columnas `Nombre | Email`.
- Agrega tu nombre y correo en la hoja `Respuestas`
- Abre el panel de Extensiones y selecciona Apps Script.
- Copia y pega el código del script en el editor de Apps Script.
- Dale un nombre al script y guardo el script.
- Ejecutar el script y verificar los emails enviados. (Debes de autorizar la ejecución en la ventana de autorización)

**Código**:

```javascript
function enviarEmails() {
  const sheet = SpreadsheetApp.getActiveSpreadsheet().getSheetByName("Respuestas");
  const data = sheet.getDataRange().getValues();

  for (let i = 1; i < data.length; i++) {
    const nombre = data[i][0];
    const email = data[i][1];
    const mensaje = `Hola ${nombre}, gracias por tu respuesta!`;

    MailApp.sendEmail(email, "Gracias por completar el formulario", mensaje);
  }
}
```

---


## 🧪 Laboratorio Final: "Asistente de Automatización Gsuite"

### Objetivo:
Crear un script que:
- Envíe un email personalizado.
- Cree un evento en Calendar.
- Genere un archivo PDF y lo guarde en Drive.
- Marque la fila como procesada.



### Estructura esperada de la hoja `Tareas`:
| Estado | Tarea | Descripción | Responsable | Email | Fecha Vencimiento |
|--------|-------|---------------|-------|--------|--------|

📌 **Instrucción para VibeCoding**:
> "Generá un script que recorra la hoja 'Tareas' y, si la columna Estado está vacía, haga lo siguiente: enviar email de recordatorio, crear evento en Calendar, generar archivo PDF en Drive con el resumen de la tarea, y marcar la fila como Procesado."

---

## ✅ Recomendaciones

- Usá VibeCoding para mejorar, comentar o depurar tus scripts.
- Activá los permisos necesarios desde el editor de Apps Script.
- Probá con tu cuenta de Gmail, Google Calendar y Drive.
- Usá el depurador para identificar errores.

---

## 📚 Recursos adicionales

- [Curso completo de Apps Script (Google Developers)](https://developers.google.com/apps-script/guides)
- [VibeCoding (Lovable)](https://www.lovable.so/)
- [Documentación de GmailApp](https://developers.google.com/apps-script/reference/gmail/gmail-app)
- [Documentación de CalendarApp](https://developers.google.com/apps-script/reference/calendar/calendar-app)

---

## 🧩 Tareas sugeridas

- Crear un script que te avise por email si un evento está a menos de 24 horas.
- Automatizar reportes semanales con Sheets + PDF + Drive.
- Generar carpetas por cliente o proyecto desde una hoja de cálculo.

---

## ✨ Autor

Este contenido fue desarrollado como parte del curso de **Productividad con IA**.  
Podés usarlo libremente para fines educativos y experimentación.

---

[⬅ Back to Course Home](../../README.md)