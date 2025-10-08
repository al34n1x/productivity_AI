# 🎥 Clase 9 — Creación de Avatares y Voz con IA (HeyGen + ElevenLabs)

**Parte del curso:** Productividad con IA  
**Formato sugerido:** 1 sesión de 90 min + práctica guiada  
**Objetivo:** Aprender a crear videos profesionales combinando **avatares digitales** (HeyGen) y **voz sintética** (ElevenLabs), con foco en ética, calidad y flujo de trabajo reproducible. :contentReference[oaicite:0]{index=0}



## 🧠 Objetivos de Aprendizaje
1. **Fundamentos de IA audiovisual:** entender la base técnica de avatares y síntesis de voz. :contentReference[oaicite:1]{index=1}  
2. **Dominar HeyGen:** generar videos con avatares, control de expresiones y sincronización labial. :contentReference[oaicite:2]{index=2}  
3. **Explorar ElevenLabs:** producir y (cuando apliquen los permisos) clonar voces realistas con control de tono/ritmo/emoción. :contentReference[oaicite:3]{index=3}  
4. **Integración práctica:** unir audio + avatar para obtener un resultado final pulido. :contentReference[oaicite:4]{index=4}  
5. **Ética y responsabilidad:** aplicar buenas prácticas y entender límites legales/éticos. :contentReference[oaicite:5]{index=5}



## 📚 Agenda resumida
- **Panorama**: ¿por qué esta tecnología es transformadora? (5’) :contentReference[oaicite:6]{index=6}  
- **Fundamentos técnicos**: texto → fonemas → onda sonora; lip-sync y motion capture facial. (10’) :contentReference[oaicite:7]{index=7}  
- **HeyGen**: flujo de creación con audio propio. (20’) :contentReference[oaicite:8]{index=8}  
- **ElevenLabs**: TTS y Voice Cloning con control de prosodia. (20’) :contentReference[oaicite:9]{index=9}  
- **Integración**: audio (WAV/MP3) → HeyGen → subtítulos → export final. (15’) :contentReference[oaicite:10]{index=10}  
- **Ética/Marco legal**: consentimiento, transparencia, AI Act/GDPR y políticas de uso. (10’) :contentReference[oaicite:11]{index=11}  
- **Lab**: “Video de Introducción Personal”. (10’) :contentReference[oaicite:12]{index=12}



## 🔬 Fundamentos (versión simple y accionable)
### Avatares digitales
- Personajes virtuales generados por IA que replican **expresiones** y **sincronización labial** con modelos de lip-sync y captura de movimiento facial (motion capture). 

### Síntesis de voz
- **Text-to-Speech (TTS)** convierte texto en audio; **Voice Cloning** aprende el timbre a partir de muestras autorizadas.  
- Pipeline típico: **texto → fonemas → onda sonora** con prosodia (ritmo, entonación, pausas) para sonar natural. 

### ¿Para qué sirve hoy?
- Educación en línea, marketing multilingüe, atención al cliente, contenido para redes y presentaciones corporativas — **sin** estudio, cámara ni actores. Democratiza la producción audiovisual. 



## 🧩 Herramientas y enlaces
- **HeyGen (plataforma):** https://www.heygen.com/  — Términos de Servicio: https://www.heygen.com/terms  
- **ElevenLabs (plataforma):** https://elevenlabs.io/  — Uso responsable/políticas: https://elevenlabs.io/terms  
- **Ayudas para subtítulos/edición (opcionales):**  
  - CapCut Web: https://www.capcut.com/  
  - VEED: https://www.veed.io/  
  - Descript: https://www.descript.com/  
- **Más sobre ética/regulación:**  
  - UNESCO – IA generativa (orientaciones): https://unesdoc.unesco.org/  
  - AI Act (UE) — visión general: https://digital-strategy.ec.europa.eu/  
  - GDPR (UE): https://gdpr.eu/



## 🛠️ Flujo de trabajo recomendado (end-to-end)

### 1) Planificación (guion de 45–60 s)
- Estructura: **presentación (nombre/rol)** → **dos usos concretos de IA** → **cierre con CTA**.  
- Pro tip: pedí a ChatGPT que mejore claridad/ritmo y marque pausas (“…”) para ayudar a TTS.

### 2) Generar voz en ElevenLabs
1. Crear cuenta/iniciar sesión: https://elevenlabs.io/  
2. En **Text-to-Speech**, pegar el guion.  
3. Elegir voz preentrenada **o** (si hay consentimiento) clonar voz con 30–60 s de muestra.  
4. Ajustar **stability**, **style**, **clarity** y **similarity** hasta lograr tono natural.  
5. **Exportar** en **WAV** o **MP3** (44.1 kHz, mono recomendado).  
> Nota ética: **no** clonar voces sin autorización expresa; la plataforma lo prohíbe. 

### 3) Crear avatar en HeyGen con audio propio
1. Entrar: https://www.heygen.com/  
2. Elegir **Avatar Template** o uno neutro; fondo limpio.  
3. **Importar el audio** generado en ElevenLabs (en vez de TTS interno).  
4. Revisar **lip-sync** y gestual; ajustar duración, recortes y subtítulos automáticos.  
5. Añadir rótulo con **nombre + rol** (5–7 s) y colores sobrios.

### 4) Post-producción y export
- Si hace falta, habilitar subtítulos automáticos o exportar **SRT** para editarlos en CapCut/VEED/Descript.  
- Música opcional libre de derechos, **muy baja** (-20 dB) para no competir con la voz.  
- Exportar **1080p (H.264)** con bitrate 8–12 Mbps.  
- Nomenclatura: `intro-<nombre>-1080p.mp4`.



## 🤝 Integración HeyGen + ElevenLabs (resumen operativo)
1) **Preparar audio (11Labs)** → 2) **Importar a HeyGen** → 3) **Sincronización labial automática** → 4) **Personalizar fondo/subtítulos** → 5) **Exportar** en alta calidad. 



## ⚖️ Ética y responsabilidad (checklist rápido)
- **Consentimiento explícito** antes de usar imagen/voz de terceros; debe ser informado y revocable.  
- **Transparencia**: rotular “Voz generada por IA / Avatar digital” cuando corresponda.  
- **Cumplimiento**: revisar AI Act (UE), GDPR, y guías de la FTC/leyes locales sobre deepfakes. 
- **Prohibido**: suplantación, fraude, desinformación, daño reputacional. 



## 🧪 Laboratorio: “Video de Introducción Personal”
**Tema:** “Quién soy y cómo uso (o usaré) la IA en mi trabajo o estudios.”  
**Pasos oficiales del ejercicio (5 etapas):**  
1. **Planificación:** guion breve con nombre, profesión/área y 1 caso específico de IA.  
2. **Producción de voz:** generar el audio en **ElevenLabs** con la voz que represente tu estilo profesional.  
3. **Creación del avatar:** importar el audio a **HeyGen**, elegir avatar y fondo adecuados.  
4. **Post-producción:** subtítulos, duración final y export en alta calidad (1080p).  
5. **Entrega:** subir el video y compartirlo para feedback entre pares.  

**Rúbrica sugerida (10 pts):** claridad del mensaje (3), naturalidad de voz (2), calidad visual/subtítulos (2), coherencia ética (2), entrega correcta (1).



## 🧭 Preguntas de reflexión (para cerrar)
1. **Ventajas estratégicas:** ¿Qué beneficios concretos aporta este flujo a tu área? 
2. **Dilemas éticos:** ¿Qué riesgos identificás y cómo los mitigarías? 
3. **Aplicación práctica:** dos escenarios de uso real en tu trabajo/estudios. 



## 🔗 Recursos rápidos
- HeyGen: https://www.heygen.com/  
- ElevenLabs: https://elevenlabs.io/  
- CapCut Web: https://www.capcut.com/  
- VEED: https://www.veed.io/  
- Descript: https://www.descript.com/  
- UNESCO (orientación ética IA): https://unesdoc.unesco.org/  
- AI Act (panorama): https://digital-strategy.ec.europa.eu/  
- GDPR (protección de datos): https://gdpr.eu/

> “Con gran poder viene gran responsabilidad: la IA amplifica tu alcance creativo y también tu deber de usarla con criterio, transparencia y respeto.” 
