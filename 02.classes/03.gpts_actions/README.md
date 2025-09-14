# 🚀 Clase: GPTs + Actions e Introducción a la API de OpenAI

## 🎯 Objetivos de la clase
Al finalizar esta clase, los participantes podrán:
- Entender qué son los **GPTs personalizados**.  
- Conocer el concepto de **Actions** (conexión con APIs y servicios externos).  
- Identificar qué tipo de cuenta y qué requisitos se necesitan para usar GPTs y la API de OpenAI.  
- Hacer sus primeras pruebas con la **API de OpenAI** (ejemplo en Python y en cURL).  
- Visualizar casos simples de productividad con IA aplicados a su día a día.  

---

## 1. Introducción a GPTs

Un **GPT** es un modelo de lenguaje de OpenAI que podés personalizar para distintos usos.  
Dentro de ChatGPT, ahora se pueden crear **GPTs personalizados** sin necesidad de programar, definiendo:

- **Rol y personalidad** del asistente.  
- **Instrucciones** específicas (qué hacer y qué no hacer).  
- **Herramientas** que puede usar (Actions).  
- **Archivos** de referencia (subida de PDFs, docs).  

👉 Ejemplo:  
- GPT para **atención al cliente** de una tienda online.  
- GPT para **resúmenes ejecutivos** de reuniones.  
- GPT como **coach de productividad** que organiza tu agenda.

---

## 2. Qué son las Actions

Las **Actions** permiten que un GPT se conecte a servicios externos a través de **APIs**.  
Es decir, tu GPT no se limita a “responder texto”, sino que puede **ejecutar acciones** en otras aplicaciones.

### Ejemplos de Actions
- Conectar un GPT con Google Calendar → para crear o leer eventos.  
- Conectar un GPT con un CRM → para consultar clientes o actualizar registros.  
- Conectar un GPT con una API de clima → para dar reportes del tiempo en tiempo real.  

👉 **Ejemplo práctico:**  
Un GPT con Action conectada a una API de tareas puede recibir el prompt:  
*"Agendá una reunión con María mañana a las 15hs"*  
y automáticamente crear el evento en tu calendario.

---

## 3. Requerimientos para acceder a GPTs y la API de OpenAI

### a) Cuentas necesarias
1. **ChatGPT gratuito (plan Free)**  
   - Permite usar GPT-3.5.  
   - Se puede acceder al creador de GPTs personalizados, pero con limitaciones.  
   - No incluye acceso completo a modelos avanzados ni a la API.

2. **ChatGPT Plus (20 USD/mes)**  
   - Permite usar **GPT-4o** (modelo más avanzado).  
   - Habilita acceso prioritario y más rápido.  
   - Recomendado para usuarios que quieran trabajar en productividad con IA.  

3. **Cuenta de OpenAI Platform (API)**  
   - Se crea en [https://platform.openai.com](https://platform.openai.com).  
   - Necesitás registrar un método de pago (tarjeta).  
   - Al crear la cuenta obtenés **API Keys**, que son necesarias para conectarte desde código o integraciones externas.  

### b) Herramientas necesarias
- Navegador web → para ChatGPT y GPTs personalizados.  
- Una cuenta en OpenAI con **ChatGPT Plus** (recomendado).  
- Para la API:  
  - **API Key** (desde la consola de OpenAI).  
  - Un entorno de desarrollo básico (ej: Python o terminal con cURL).  

---

## 4. ¿Qué es una API y cómo funciona?

### Definición y conceptos básicos

Una **API** (Application Programming Interface o Interfaz de Programación de Aplicaciones) es un conjunto de reglas y protocolos que permite que diferentes aplicaciones se comuniquen entre sí. Funciona como un "intermediario" que facilita la interacción entre distintos sistemas de software.

Podemos entender una API como:
- Un **camarero** en un restaurante: tú (el cliente/desarrollador) haces un pedido, el camarero (API) lo lleva a la cocina (servidor), y luego te trae lo que pediste (datos/respuesta).
- Un **contrato** entre dos sistemas que define cómo pueden interactuar.

### Componentes principales de una API

1. **Endpoint**: La URL específica a la que envías tus solicitudes (ej: `https://api.openai.com/v1/chat/completions`).
2. **Métodos HTTP**: Definen qué tipo de operación quieres realizar:
   - GET: Obtener datos
   - POST: Enviar datos
   - PUT/PATCH: Actualizar datos
   - DELETE: Eliminar datos
3. **Headers**: Información adicional enviada con la solicitud (ej: API Key, tipo de contenido).
4. **Body/Payload**: Los datos que envías (como el prompt en el caso de OpenAI).
5. **Respuesta**: Lo que el servidor devuelve (datos, códigos de estado, mensajes).

### Cómo funciona una API en la práctica

1. **Autenticación**: Te identificas ante el servicio (generalmente con una API Key).
2. **Solicitud (Request)**: Envías un mensaje estructurado al endpoint correcto.
3. **Procesamiento**: El servidor procesa tu solicitud.
4. **Respuesta (Response)**: Recibes datos en un formato estándar (generalmente JSON).

```
+------------------------+                 +------------------------+
|                        |                 |                        |
|  Cliente/Aplicación    |                 |  Servidor/Servicio     |
|  (Tu código)           |                 |  (OpenAI, etc.)        |
|                        |                 |                        |
+------------+-----------+                 +-----------+------------+
             |                                        |
             |                                        |
             |  1. Solicitud (Request)                |
             |  POST /v1/chat/completions             |
             |  Headers: {API Key, Content-Type}      |
             |  Body: {prompt, modelo, etc.}          |
             |--------------------------------------->|
             |                                        |
             |                                        |
             |  2. Respuesta (Response)               |
             |  Status: 200 OK                        |
             |  Body: {id, choices, usage, etc.}      |
             |<---------------------------------------|
             |                                        |
+------------+-----------+                 +-----------+------------+
|                        |                 |                        |
|  Cliente procesa       |                 |  Servidor procesa      |
|  la respuesta          |                 |  la solicitud         |
|                        |                 |                        |
+------------------------+                 +------------------------+
```

### Tipos de APIs

- **REST**: Las más comunes, basadas en estándares web (HTTP).
- **GraphQL**: Permiten solicitar exactamente los datos que necesitas.
- **SOAP**: Más estructuradas y formales, comunes en entornos empresariales.
- **WebSockets**: Permiten comunicación bidireccional en tiempo real.

### Beneficios de usar APIs

- **Integración**: Conectar diferentes servicios y plataformas.
- **Automatización**: Realizar tareas sin intervención humana.
- **Escalabilidad**: Usar servicios externos sin tener que desarrollarlos.
- **Especialización**: Aprovechar servicios altamente especializados (como IA).

### Ejemplo práctico de API en productividad

Imagina que quieres crear un asistente que resuma automáticamente tus emails largos:

1. **Tu aplicación** envía el contenido del email a la **API de OpenAI**
2. La API procesa el texto y genera un resumen
3. **Tu aplicación** recibe el resumen y lo muestra o lo guarda

Este mismo principio se puede aplicar para:
- Conectar un GPT con tu calendario para crear eventos
- Integrar IA en tu CRM para analizar conversaciones con clientes
- Automatizar la creación de informes basados en datos de tu empresa

---

## 5. Primeros pasos con la API de OpenAI

La API te permite enviar instrucciones (prompts) a un modelo y recibir respuestas en formato texto.

### Ejemplo con **cURL**
```bash
curl https://api.openai.com/v1/chat/completions   -H "Content-Type: application/json"   -H "Authorization: Bearer $OPENAI_API_KEY"   -d '{
    "model": "gpt-4o-mini",
    "messages": [
      {"role": "system", "content": "Sos un coach de productividad."},
      {"role": "user", "content": "Dame 3 consejos rápidos para organizar mi semana."}
    ]
  }'
```

### Ejemplo con **Python**
```python
from openai import OpenAI

client = OpenAI(api_key="TU_API_KEY")

response = client.chat.completions.create(
    model="gpt-4o-mini",
    messages=[
        {"role": "system", "content": "Sos un coach de productividad."},
        {"role": "user", "content": "Dame 3 consejos rápidos para organizar mi semana."}
    ]
)

print(response.choices[0].message.content)
```

👉 Resultado esperado: una lista de 3 consejos prácticos de productividad.  

---

## 6. Ejercicios prácticos para la clase

### Ejercicio 1 – Crear un GPT personalizado
1. Entrar a ChatGPT.  
2. Ir a la opción **Explore GPTs → Create**.  
3. Definir:  
   - Rol: *Asistente de productividad*.  
   - Estilo: *Claro, motivador y breve*.  
   - Ejemplo de tarea: *Organizar agenda semanal*.  
4. Guardarlo y probarlo con la pregunta:  
   *“Ayúdame a planificar mi semana laboral en 5 pasos.”*  


---

## 7. Casos de uso en productividad

- **Resúmenes automáticos**: reuniones, documentos o correos.  
- **Planificación de tareas**: generar un plan diario/semanal.  
- **Comunicación**: redactar emails o mensajes con el tono adecuado.  
- **Automatización**: conectar GPTs con Actions para ejecutar tareas reales en apps (CRM, calendarios, etc.).  

---

## 8. Cierre y recap

- Los **GPTs personalizados** permiten adaptar un modelo a nuestras necesidades sin programar.  
- Las **Actions** llevan esto más allá al conectar con servicios externos.  
- Con la **API de OpenAI** podemos automatizar e integrar la IA en nuestros propios flujos de trabajo.  
- Con práctica, podemos convertir la IA en un **asistente real de productividad**.  

---

## 📌 Recursos
- [ChatGPT](https://chat.openai.com)  
- [OpenAI Platform](https://platform.openai.com)  
- [Documentación oficial de la API](https://platform.openai.com/docs)
