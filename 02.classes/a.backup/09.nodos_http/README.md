
# Taller: Introducción a Automatizaciones con n8n usando Nodos Code y HTTP Request

Este taller está diseñado para personas que están dando sus primeros pasos en automatización y desean entender cómo construir flujos utilizando **n8n**, una potente herramienta de automatización de código abierto. En este taller nos enfocaremos en dos tipos de nodos clave: **Code** (para lógica personalizada en JavaScript) y **HTTP Request** (para conectar con APIs externas).

---

## 🧩 ¿Qué es n8n?

- **n8n** (pronunciado *"n-eight-n"*) es una plataforma de automatización de flujos de trabajo.
- Permite conectar aplicaciones y servicios para automatizar tareas sin necesidad de programar (aunque ofrece nodos para hacerlo si lo necesitás).
- Es auto-hosteable, extensible y open source.
- Ideal para tareas repetitivas, flujos inteligentes, y conectores API.

---

## 🔧 ¿Qué es un Nodo?

- Los flujos en n8n se componen de **nodos**, que representan acciones o pasos.
- Un nodo puede:
  - Transformar datos.
  - Realizar cálculos.
  - Conectarse a una API.
  - Enviar mensajes o correos.
  - Ejecutar lógica condicional.
- Ejemplo: un nodo que lee datos de Google Sheets, otro que los filtra y otro que los envía por email.

---

## 👨‍💻 Nodo `Code`

El nodo `Code` permite ejecutar JavaScript personalizado dentro del flujo. Ideal para:

- Manipular datos complejos.
- Aplicar lógica condicional avanzada.
- Preparar estructuras antes de enviarlas a otras APIs.

### 🧪 Ejemplo de uso

```javascript
return items.map(item => ({
  json: {
    mensaje: `Hola, ${item.json.nombre}!`
  }
}));
```

Este código toma una lista de nombres y devuelve un saludo personalizado para cada uno.

---

## 🌐 Nodo `HTTP Request`

Este nodo se usa para conectarte con cualquier API o servicio que acepte solicitudes HTTP.

- Métodos soportados: `GET`, `POST`, `PUT`, `DELETE`, etc.
- Puedes enviar headers, autenticarte y trabajar con el cuerpo de la respuesta.

### 🧪 Ejemplo de uso

**API pública**: [https://api.chucknorris.io/jokes/random](https://api.chucknorris.io)

Parámetros:
- Método: `GET`
- No requiere autenticación
- Devuelve un chiste aleatorio de Chuck Norris en formato JSON

---

## 🎯 Ejercicios

### 🧩 Ejercicio 1: Saludo Personalizado

**Objetivo**: Usar el nodo `Code` para generar un mensaje personalizado para cada nombre.

#### Pasos:
1. Agregar un nodo `Code` con una lista de nombres.
2. Usar un nodo `Code` que recorra los nombres y devuelva un saludo.
3. Verificar resultados.

#### Solución:

1. Node Code Set

```javascript
return [
  { json: { nombre: "Ale" } },
  { json: { nombre: "Feli" } },
  { json: { nombre: "Sofi" } },
  { json: { nombre: "Lucas" } },
  { json: { nombre: "Martina" } }
];
```

2. Node Code Salida

```javascript
return items.map(item => ({
  json: {
    saludo: `Hola, ${item.json.nombre}!`
  }
}));
```

---

### 🧩 Ejercicio 2: Obtener un chiste desde una API

**Objetivo**: Usar el nodo `HTTP Request` para consumir una API pública.

#### Pasos:
1. Usar un nodo `HTTP Request` con método `GET`.
2. URL: `https://api.chucknorris.io/jokes/random`
3. Conectarlo a un nodo `Code` que devuelva solo el texto del chiste.

#### Solución:

```javascript
return [{
  json: {
    chiste: $input.first().json.value
  }
}];
```

---

## 📚 Recursos Recomendados

- 🌐 [Documentación oficial de n8n](https://docs.n8n.io/)
- ⚙️ [Editor visual de flujos - Playground](https://n8n.io/workflows)
- 📘 [Introducción a APIs RESTful](https://developer.mozilla.org/es/docs/Learn/JavaScript/Client-side_web_APIs/Introduction)
- 📺 [Curso gratuito de n8n en YouTube (ESP)](https://www.youtube.com/results?search_query=n8n+automatizaciones)
- 📕 [API pública de Chuck Norris](https://api.chucknorris.io/)

---

## 🛠 Requisitos

- Cuenta gratuita en [n8n.cloud](https://n8n.cloud/)
- Alternativamente, podés instalar n8n localmente con Docker.
- Conocimientos básicos de lógica y estructuras JSON.
- Muchas ganas de aprender e iterar.

---

## 🚀 Próximos pasos sugeridos

- Probar otras APIs públicas como OpenWeather, Advice Slip, o JSONPlaceholder.
- Usar el nodo `IF` para agregar lógica condicional.
- Combinar n8n con Google Sheets, Telegram, Slack o Gmail.
- Explorar la autenticación con tokens y headers personalizados.

---

## ✨ Tip Final

Recordá: podés **probar y equivocarte** dentro de n8n todo lo que necesites. Cada nodo muestra su resultado intermedio, lo que facilita el debugging. La automatización no se trata solo de ahorrar tiempo, sino de **crear soluciones inteligentes** que trabajen por vos.


---

[⬅ Back to Course Home](../../README.md)
