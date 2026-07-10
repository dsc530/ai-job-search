# Interview Preparation Guide

## STAR Format

Structure answers as: **Situation** (context), **Task** (your responsibility), **Action** (what you did), **Result** (outcome).

Keep answers to 1-2 minutes. Be specific. End with what you learned or would do differently.

## STAR Candidates (Complete Manually)

These stubs were identified from your CV, LinkedIn, and reference letter. Fill in the S/T/A/R details before using in interviews.

---

### 1. Proyecto DGRC — capacitación y mesas de prueba para reducir incidencias (Uniscan)
**Source:** CV / LinkedIn / Carta de referencia — Uniscan Cia. Ltda. (2017–2019)
**What happened:** En el marco del contrato con el Registro Civil, implementaste mesas de prueba para ajustar configuraciones de impresoras Zebra ZXP7 y capacitaste sucursales a nivel nacional, reduciendo incidencias de forma sostenida en un proceso crítico para una institución pública.
**Honesty note:** No fue iniciativa propia — fue parte del rol asignado. Enmarcar como "ejecución efectiva dentro de un proyecto institucional complejo."
**Why it matters:** Responde a: "Cuéntame de un proyecto de alta responsabilidad", "¿Has trabajado con clientes institucionales?", "¿Cómo manejas problemas que siguen surgiendo a lo largo del tiempo?"
**S/T/A/R:**
- **Situation:** Uniscan tenía un contrato de ~3 años con el Registro Civil (DGRC) para mantenimiento de impresoras de carnets Zebra ZXP7 — institución pública crítica. Desde el inicio del contrato surgían constantemente problemas de calidad en la impresión que generaban incidencias y afectaban la operación.
- **Task:** Como ingeniero de soporte asignado al proyecto, debía garantizar el funcionamiento continuo de los equipos y reducir las incidencias, incluyendo capacitar a sucursales de todo el país en el uso y configuración correcta de las impresoras.
- **Action:** Implementamos mesas de prueba para identificar y ajustar las configuraciones específicas que requería el trabajo del DGRC. Con esas configuraciones validadas, capacité a usuarios en sucursales a nivel nacional. A medida que surgían nuevos problemas, se repetía el ciclo: diagnóstico, ajuste en mesa de prueba, actualización de la capacitación.
- **Result:** Reducción sostenida de incidencias a lo largo del contrato. Proyecto ejecutado durante 3 años, contrato valorado en $207.503,46 USD, cumpliendo los tiempos de servicio establecidos contractualmente.

---

### 2. Reemplazo preventivo de baterías en equipos open box — Smartbuy
**Source:** CV / experiencia directa — Smartbuy (Oct 2022 – Sep 2023)
**What happened:** El equipo técnico identificó que los teléfonos open box se vendían con datos de batería adulterados (aparentaban 100% cuando era menos), generando una avalancha de tickets de garantía en la primera semana. El equipo propuso a gerencia implementar reemplazo preventivo de baterías antes de la venta.
**Honesty note:** Fue iniciativa del equipo técnico en conjunto, propuesta a gerencia y ejecutada en grupo. Enmarcar como "contribuí como parte del equipo técnico que identificó y resolvió el problema."
**Why it matters:** Responde a: "Cuéntame de una mejora de proceso que propusiste", "¿Cómo identificas la raíz de un problema?", "Trabajo en equipo para resolver un problema recurrente"
**S/T/A/R:**
- **Situation:** Smartbuy vendía teléfonos open box (usados en EEUU, devueltos por cambio de plan, menos de 1 año de uso). Estos llegaban con datos de batería adulterados que mostraban 100% de salud, cuando en realidad era menor. Los clientes notaban la degradación acelerada en la primera semana (caídas de 5–20%), lo que generaba la mayoría de los tickets de garantía y consumía gran parte del tiempo del equipo técnico.
- **Task:** Como parte del equipo técnico, contribuir a encontrar una solución que redujera estos tickets de forma estructural, no caso por caso.
- **Action:** El equipo técnico identificó el patrón analizando los tickets recurrentes y propuso a gerencia implementar un protocolo de revisión y reemplazo preventivo de batería en todos los equipos open box antes de su venta. Gerencia aprobó la medida. Ejecutamos el protocolo como equipo: cada equipo open box pasaba por revisión de batería y reemplazo si no cumplía el estándar, sin costo adicional al cliente (procedimiento de garantía).
- **Result:** Reducción significativa de tickets por degradación de batería, que representaban la mayoría de las reclamaciones. Los técnicos recuperaron tiempo que antes se destinaba a reparaciones bajo garantía, redirigiéndolo a reparaciones con costo.

---

### 3. Scraper SERCOP + pipeline de análisis con IA — Itecnologia EC
**Source:** Proyecto propio en producción — Itecnologia EC (2024–Actual)
**What happened:** Desarrollaste en Python una herramienta local que automatiza el análisis de contratos de ínfima cuantía publicados en el portal SERCOP, integrando scraping, filtrado inteligente, extracción de TDRs con Claude CLI y generación de PDFs de oferta — reduciendo drásticamente el tiempo de análisis de oportunidades de contratación pública.
**Why it matters:** Responde a: "Cuéntame de un proyecto técnico que hayas construido desde cero", "¿Has trabajado con scraping o automatización?", "¿Tienes experiencia integrando IA en flujos de trabajo?", "Iniciativa propia con impacto real"
**S/T/A/R:**
- **Situation:** Itecnologia EC participa en procesos de contratación pública (ínfima cuantía) a través del portal SERCOP. Analizar manualmente las necesidades publicadas diariamente era muy lento: había que abrir cada publicación, leer la descripción, descargar los TDRs y decidir si valía la pena investigar más — la mayoría no eran relevantes para el negocio.
- **Task:** Construir una herramienta que automatizara ese proceso de filtrado y análisis, dejando solo las oportunidades realmente relevantes para revisión manual.
- **Action:** Desarrollé en Python una herramienta local con interfaz estilizada en CSS que: (1) hace scraping del portal SERCOP, (2) filtra las publicaciones por palabras clave, fecha y lugar, (3) muestra una preview con la descripción completa para tomar decisiones rápidas sin abrir el portal, (4) descarga los TDRs adjuntos y los pasa a Claude CLI con un prompt estructurado que extrae los requisitos clave y los adapta a una plantilla de oferta, generando un `.json` editable, y (5) genera un PDF final de la oferta a partir de ese JSON, que reviso y ajusto antes de enviar. Actualmente estoy desarrollando un módulo de seguimiento para registrar a cuáles apliqué, resultados, competidores y ganadores.
- **Result:** Reducción significativa del tiempo dedicado a analizar oportunidades del SERCOP. El pipeline completo — desde la publicación hasta tener un borrador de oferta listo para revisar — se ejecuta en minutos en lugar de horas. Herramienta en uso activo en el negocio.

---

### 4. Customer Churn Prediction — Random Forest AUC-ROC 0.86
**Source:** TripleTen Bootcamp project (guiado) — github.com/dsc530/tasa_cancelacion
**Honesty note:** Proyecto de formación guiado por TripleTen con datos proporcionados por el bootcamp. Las decisiones técnicas clave (selección del modelo, ajuste de hiperparámetros, interpretación de resultados) fueron propias. Presentar como "proyecto de formación" — no como trabajo para un cliente real.
**Why it matters:** Responde a: "Cuéntame de un proyecto de ML", "¿Cómo seleccionas un modelo?", "¿Cómo manejas datos desbalanceados?"
**S/T/A/R:**
- **Situation:** Proyecto de formación en TripleTen: dataset de empresa de telecomunicaciones con problema de churn — predecir qué clientes cancelarían el servicio para habilitar acciones de retención.
- **Task:** Construir un modelo predictivo end-to-end: desde el preprocesamiento de 3 datasets hasta la selección y justificación del modelo final.
- **Action:** Preprocesé los datos (eliminación de redundancias, ingeniería de variables clave, One-Hot Encoding, Min-Max scaling, SMOTE para manejar el desbalance de clases). Comparé Logistic Regression, Decision Tree, Random Forest y XGBoost en base a costo computacional y métricas de rendimiento. Ajusté hiperparámetros del modelo ganador. Analicé la importancia de características para orientar las acciones de retención hacia las variables de mayor peso.
- **Result:** Random Forest seleccionado como modelo final — AUC-ROC 0.86, accuracy 0.77. El análisis de importancia de variables identificó los factores de mayor riesgo de churn para priorizar acciones de retención.

---

### 5. E-commerce Itecnologia EC — full-stack con Claude Code
**Source:** Proyecto propio en producción — itecnologiaec.com
**What happened:** Construiste desde cero una tienda en línea completa para tu negocio usando Next.js, Supabase, Prisma, Vercel y pasarela de pagos, con asistencia de Claude Code — sin experiencia previa en desarrollo web full-stack.
**Why it matters:** Responde a: "¿Tienes experiencia con herramientas de IA en desarrollo?", "Cuéntame de un proyecto que hayas llevado a producción", "¿Has trabajado con bases de datos en aplicaciones reales?", "Iniciativa emprendedora y capacidad de aprendizaje autónomo"
**S/T/A/R:**
- **Situation:** Itecnologia EC operaba con una cartera de clientes limitada y conocida, sin presencia digital. Para crecer necesitaba un canal de ventas en línea que conectara con redes sociales y permitiera ventas directas.
- **Task:** Construir y publicar una tienda en línea funcional con catálogo de productos, pasarela de pagos y presencia de marca — sin equipo de desarrollo.
- **Action:** Desarrollé la solución completa con asistencia de Claude Code: frontend en Next.js, base de datos en Supabase administrada con Prisma, repositorio en GitHub conectado a Vercel para deployment continuo con variables de entorno configuradas en la plataforma. Integré pasarela de pagos con tarjeta de un proveedor externo. Añadí un módulo que genera automáticamente un PDF con el catálogo de productos. Registré dominio propio (itecnologiaec.com).
- **Result:** E-commerce en producción y en línea en itecnologiaec.com. Canal de ventas directas operativo, presencia digital establecida, catálogo en PDF generado automáticamente. Primer proyecto full-stack llevado a producción de forma autónoma.

---

## Common Tough Questions

### "¿Por qué cambiaste de ingeniería de soporte a Data Science?"
> Preparar una narrativa honesta y forward-looking: el interés por los datos surgió al trabajar con sistemas automatizados y ver cómo los patrones en la información podían optimizar procesos. El bootcamp de TripleTen fue la decisión deliberada de formalizar esa transición. No negatividad sobre roles anteriores.

### "No tienes experiencia profesional formal en datos."
> Reconocer el gap con seguridad: "Es correcto — mis proyectos de datos han sido en contexto de bootcamp y aplicación en mi propio negocio. Lo que traigo es un sólido dominio técnico de Python, SQL y ML aplicado, más 10 años de experiencia entendiendo cómo los sistemas técnicos sirven a operaciones reales. Estoy buscando este rol precisamente para construir esa experiencia formal."

### "¿Dónde te ves en 5 años?"
> Mostrar ambición alineada con el rol: crecer hacia roles más autónomos en Data Science, desarrollar capacidad en ML aplicado a problemas de negocio, eventualmente poder liderar iniciativas de datos en equipos pequeños.

### "¿Cuál es tu mayor debilidad?"
> Debilidad genuina con mitigación concreta: "Mi experiencia con herramientas cloud (AWS, Databricks, Spark) es aún limitada. Tengo la base técnica en Python y SQL para aprender rápido — lo demostré en el bootcamp completando módulos nuevos semana a semana."

### "¿Por qué esta empresa específicamente?"
> Siempre personalizar. Nunca dar respuesta genérica. Investigar misión, productos, noticias recientes antes de cada entrevista.

## Questions You Should Ask Interviewers

### About the Role
- "¿Cómo es una semana típica en este rol?"
- "¿Qué métricas definen el éxito en los primeros 6 meses?"
- "¿Cuál es el mayor desafío que enfrenta el equipo ahora mismo?"

### About the Team
- "¿Cómo está compuesto el equipo y cómo se divide el trabajo?"
- "¿Cómo es el proceso de onboarding para alguien nuevo en el área de datos?"
- "¿Qué herramientas y stack de datos usa el equipo?"

### About Growth
- "¿Hay oportunidad de trabajar con modelos más avanzados o proyectos de ML en el futuro?"
- "¿Cómo apoya la empresa el desarrollo profesional continuo?"
- "¿El rol tiene espacio para proponer mejoras o nuevos análisis?"

### About Culture
- "¿Cómo describirían la cultura del equipo?"
- "¿Cuál es el balance entre trabajo remoto y presencial?"
- "¿Qué tienen en común las personas que se desempeñan mejor aquí?"

## Phone/Video Interview Tips
- Ten los ejemplos STAR escritos (usa este archivo)
- Ten agua cerca
- Sonríe al hablar — cambia el tono
- Pide clarificación si una pregunta es vaga
- Está bien tomarse 5 segundos antes de responder
- Termina con: "¿Hay algo más que quisieran saber sobre mi perfil?"

## After the Application (Best Practice)

### Follow-Up Etiquette
- No llamar solo para "hacerse notar" — genera impresión negativa
- Si el empleador indicó un plazo, respetarlo
- Si no indicaron plazo y han pasado 2+ semanas, una llamada breve para preguntar el estado es aceptable
- Si tienes información genuinamente nueva y relevante, un seguimiento breve está bien

### Thank-You Notes
- Cuando recibas cualquier actualización (invitación a entrevista, rechazo, o actualización de estado), envía un mensaje breve de agradecimiento
- 2-3 oraciones, expresando aprecio por su tiempo y el proceso

## Roleplay Guidelines
When the user asks for interview practice:
1. Ask which role/company to simulate
2. Start with warm-up: "Cuéntame sobre ti"
3. Progress to role-specific technical questions
4. Include 1-2 behavioral questions using competencies from the job posting
5. End with a tough question or curveball
6. After each answer, give brief feedback: what worked, what to sharpen
7. Suggest which STAR example would work best for each question
