# 💡 Introducción a n8n y la API de OpenAI

Este documento contiene el contenido completo de una clase/taller de nivel inicial sobre automatizaciones con **n8n** y el uso de la **API de OpenAI (GPT)**. Aprenderás qué es una API, cómo funciona n8n, y cómo crear flujos que conectan servicios sin necesidad de programar.

---

## 🌟 Objetivo de la clase
- Comprender qué es una API.
- Explorar la interfaz de n8n.
- Conectarse a OpenAI desde n8n.
- Crear un flujo automatizado que interactúe con GPT.

---

## 🔌 ¿Qué es una API?

### 📘 Definición sencilla:
Una **API** es una forma de comunicación entre programas. Permite hacer pedidos y obtener respuestas sin conocer el "código interno" del otro sistema.

### 🍼 Analogía: El restaurante
- Vos = el cliente.
- El mozo = la API.
- La cocina = el sistema (ej: OpenAI).

✉️ Pedís una pizza → El mozo lleva el pedido a la cocina → Vuelve con la pizza.

### ⚙️ Ejemplo con OpenAI
- Pedido: "¿Cuál es la capital de Francia?"
- API procesa y devuelve: "París"

---

## 📦 ¿Qué es un archivo JSON?

**JSON (JavaScript Object Notation)** es un formato ligero de intercambio de datos.
Se utiliza para representar información estructurada como texto.

### 🔍 Características:
- Usa llaves `{}` para agrupar datos.
- Usa pares "clave: valor"
- Es legible para humanos y máquinas.

### 🧾 Ejemplo:
```json
{
  "nombre": "Ale",
  "edad": 43,
  "intereses": ["videojuegos", "AI", "ciencia", "Taekwondo"]
}
```

---

## 📡 ¿Cómo se estructura una llamada a una API?

Cuando usamos una API, hacemos una **solicitud (request)** con un **contenido (payload)** y recibimos una **respuesta (response)**.

### ✉️ Ejemplo:
#### Request:
- **Método:** `POST`
- **URL:** `https://api.openai.com/v1/chat/completions`
- **Headers:**
```json
{
  "Authorization": "Bearer TU_API_KEY",
  "Content-Type": "application/json"
}
```
- **Payload (Body):**
```json
{
  "model": "gpt-3.5-turbo",
  "messages": [
    { "role": "user", "content": "¿Qué es una célula?" }
  ]
}
```

#### Response (respuesta de la API):
```json
{
  "id": "chatcmpl-abc123",
  "object": "chat.completion",
  "choices": [
    {
      "index": 0,
      "message": {
        "role": "assistant",
        "content": "Una célula es la unidad básica de la vida..."
      },
      "finish_reason": "stop"
    }
  ]
}
```

---

## 🤖 ¿Qué es n8n?

### ✅ Ventajas
- Open Source
- Interfaz visual sin programación
- Flexible y potente para automatizaciones

### 📊 Caso de uso:
- Conectar apps
- Automatizar tareas
- Hacer workflows con IA

---

## 🗺️ Explorando la interfaz de n8n

### 📌 3 áreas principales:
- **Canvas (centro):** Donde están los nodos
- **Panel izquierdo:** Nodos disponibles (HTTP, Gmail, etc.)
- **Panel derecho:** Configuración del nodo

---


## 🎨 Actividad Práctica

### Crea un flujo que:
- Pregunte: "¿Cuál es el país más poblado del mundo?"
- Devuelva la respuesta de GPT
- Envie la respuesta al chat

---

## 💡 Ideas de proyectos con n8n + OpenAI
- Resumen de correos
- Generador de ideas para redes sociales
- Clasificador de mensajes positivos/negativos
- Bot que contesta preguntas frecuentes

---

## 📚 Recursos útiles
- https://docs.n8n.io
- https://platform.openai.com/docs
- https://platform.openai.com/playground
- https://github.com/n8n-io/n8n

---

## 🚀 ¡Gracias y manos a la obra! ✨

[⬅ Back to Course Home](../../README.md)