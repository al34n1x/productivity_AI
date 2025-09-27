
# 🧪 Laboratorio: Flujos de Control con Nodos de IA en n8n

Este laboratorio te guiará paso a paso para crear un flujo en n8n que utilice **nodos de control de flujo** combinados con un **agente de IA (ChatGPT)**.

---

## 🎯 Objetivo

Construir un flujo que:
1. Reciba un mensaje del usuario.
2. Use IA para clasificarlo como **positivo** o **negativo**.
3. Utilice un nodo `If` para actuar según el resultado.
4. Espere 10 segundos si es positivo y envíe una respuesta de agradecimiento.
5. Si es negativo, lo reenvíe a un equipo de soporte.

---

## 🧩 Pasos

### 1. Nodo `Chat` (Start)
- Agregar un nodo de Chat para comenzar

### 2. Nodo `ChatGPT` o `OpenAI`
- Agregar como System Message el siguiente Prompt: `"Clasifica el siguiente mensaje como POSITIVO o NEGATIVO:
{{ $json.mensaje }}
Solo responde una palabra."`
- Guardar la respuesta como `sentimiento`.

### 3. Nodo `If`
- Condición: `$json.choices[0].message.content` contiene `"POS"` (para detectar mensaje positivo).

### 4a. Rama positiva
#### Nodo `Wait`
- Tipo: Tiempo fijo
- Esperar: 5 segundos

#### Nodo `Set`
- Contenido: `Gracias por tu mensaje positivo 😊`

### 4b. Rama negativa
#### Nodo `Wait`
- Tipo: Tiempo fijo
- Esperar: 5 segundos

### 4b. Rama negativa
#### Nodo `Set`
- Contenido: `Tu mensaje ha sido reenviado a nuestro equipo de soporte.`


---

## 🛠 Requisitos

- Cuenta activa en [n8n.io](https://n8n.io) o instalación local.
- Credencial configurada de OpenAI (Settings > API Credentials).
- Conocimiento básico del editor visual de n8n.

---

## 🧠 ¿Qué estás practicando?

- Uso de agentes de IA (ChatGPT)
- Nodos `If`, `Wait`, `Set`
- Manejo condicional de flujos
- Control del tiempo con `Wait`

---

## 📦 Importar el flujo

Subí el archivo `lab_flujo_control_ia.json` a tu instancia de n8n:
1. Abrí n8n.
2. Menú > Import workflow.
3. Pegá el JSON o seleccioná el archivo.

---

¡Listo! Ya podés comenzar a crear flujos inteligentes y dinámicos con IA 🤖⚙️

---

[⬅ Back to Course Home](../../README.md)