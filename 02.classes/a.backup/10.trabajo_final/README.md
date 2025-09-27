
# 🤖 Examen Final Grupal - Agente de IA con Google Sheets (n8n)

Este repositorio contiene el enunciado del examen práctico final del curso **Productividad con IA usando n8n**. En esta edición, el desafío es construir un **Agente de IA** que consulte una hoja de cálculo con datos de clientes y actúe en consecuencia.

---

## 🎯 Objetivo del Proyecto

Desarrollar un **agente automatizado en n8n** que:

1. Reciba una consulta con el nombre o ID de un cliente.
2. Busque los datos correspondientes en una hoja de cálculo de Google Sheets.
3. Devuelva información útil sobre ese cliente (por ejemplo: nombre, email, estado, plan contratado, etc.).
4. Si el cliente **no existe**, ofrezca registrarlo o enviar una respuesta personalizada.


---

## 📋 Requisitos Mínimos

- ✅ Usar el nodo `Google Sheets` para leer datos desde una hoja con información de clientes.
- ✅ Utilizar un nodo de entrada (`Webhook`, `Telegram`, `Formulario`, etc.).
- ✅ Buscar un cliente por nombre o ID utilizando `Code` o `IF`.
- ✅ Enviar una respuesta informativa como salida.

---

## 🧠 Lógica Esperada

1. **Entrada del usuario:** `"Consultar cliente ID123"` o `"Buscar María González"`
2. **Leer hoja de cálculo:** estructura ejemplo:

| ID    | Nombre           | Email              | Estado   | Plan     |Gasto acumulado (USD)|
|-------|------------------|--------------------|----------|----------|---------------------|
| ID123 | María González   | maria@mail.com     | Activo   | Premium  | 1000                |
| ID456 | Juan Pérez       | juan@mail.com      | Inactivo | Básico   | 500                 |

3. **Condición:**
   - Si el cliente **existe**:
     - Mostrar: `"Cliente encontrado: María González - Estado: Activo - Plan: Premium"`
   - Si **no existe**:
     - Mostrar: `"No se encontró el cliente."`

---

## 📚 Recursos Útiles

- [n8n + Google Sheets](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.googleSheets/)
- [Credenciales de Google](https://docs.n8n.io/credentials/google/)
- [Uso de Webhooks en n8n](https://docs.n8n.io/nodes/n8n-nodes-base.webhook/)
- [n8n Playground](https://n8n.io/workflows)

---

## ✅ Criterios de Evaluación

| Criterio                             | Peso  |
|-------------------------------------|-------|
| Flujo funcional completo             | 40%   |
| Consulta dinámica de cliente         | 20%   |
| Respuesta clara e informativa        | 15%   |
| Integración creativa con IA (opcional) | 15%   |
| Presentación y documentación         | 10%   |

---

## 🧠 Ideas para Expandir

- Agregar resúmenes de cliente usando OpenAI o Cohere.
- Predecir la probabilidad de churn en base al plan o estado.
- Generar un informe PDF con la información del cliente.
- Automatizar respuestas frecuentes vía Telegram o WhatsApp.

---

## 🤝 Trabajo en equipo

- Dividan tareas por función: búsqueda, presentación, integración con IA, etc.
- Documenten cada paso, flujos y decisiones.
- Sean creativos: ¡el agente puede seguir creciendo!

---

¡A construir su primer agente inteligente con datos reales! 📊🤖

---

[⬅ Back to Course Home](../../README.md)