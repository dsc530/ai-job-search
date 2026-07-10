# Job Evaluation Framework

## Scoring Dimensions

Evaluate each job posting against these five dimensions:

### 1. Technical Skills Match (0-100)
How well do the required/preferred skills align with the candidate's capabilities?

| Score | Meaning |
|-------|---------|
| 80-100 | Core requirements are primary skills |
| 60-79 | Most requirements match, 1-2 gaps that are learnable |
| 40-59 | Partial match, significant upskilling needed |
| 0-39 | Fundamental mismatch |

**Strong match areas:** Python (Pandas, Scikit-learn, LightGBM, XGBoost), SQL/SQL Server, preprocesamiento de datos, modelos de clasificación y regresión supervisada, visualización (Power BI, Plotly, Matplotlib, Seaborn), Git, automatización (n8n, scripting)
**Moderate match areas:** Álgebra lineal aplicada, series temporales, NLP básico, visión artificial (nivel bootcamp), Java, HTML/CSS, gestión de bases de datos
**Weak match areas:** PySpark/Apache Spark, cloud (AWS, Azure, GCP, Databricks), R/SAS/Matlab, estadística econométrica avanzada, CI/CD, MLOps, experiencia industrial en banca/telco

### 2. Experience Match (0-100)
Does work history align with what they're looking for?

| Score | Meaning |
|-------|---------|
| 80-100 | Direct experience in the same domain and role type |
| 60-79 | Related experience, transferable skills clear |
| 40-59 | Adjacent experience, would need to make the case |
| 0-39 | Unrelated experience |

**Strong:** Soporte técnico y resolución de problemas técnicos complejos, gestión de proyectos con instituciones gubernamentales, automatización de procesos con herramientas de datos, análisis de negocio (ingresos/gastos/operaciones)
**Moderate:** Proyectos de ML aplicados (bootcamp nivel), análisis de datos con Python y SQL en entorno real (negocio propio), dashboards Power BI para comunicación a no técnicos
**Entry-level / gap real:** Experiencia profesional formal en Data Science / Analytics en empresas — todos los proyectos de datos son autónomos o del bootcamp. Este gap es la razón principal de los 6 rechazos previos.

### 3. Behavioral/Culture Fit (0-100)
Does the role and company culture match the behavioral profile?

| Score | Meaning |
|-------|---------|
| 80-100 | Culture strongly matches behavioral preferences |
| 60-79 | Mixed signals but mostly compatible |
| 40-59 | Some friction areas |
| 0-39 | Significant culture mismatch |

**Red flags to research:** Roles que exigen 3+ años de experiencia profesional en datos sin valorar bootcamps o proyectos independientes; empresas sin cultura de onboarding para perfiles en transición; roles puramente de mantenimiento sin componente analítico.

### 4. Location & Logistics (Pass/Fail + Notes)
- Quito (presencial o híbrido): PASS
- Remoto desde Ecuador: PASS
- Guayaquil u otras ciudades (presencial): FAIL — Daniel está basado en Quito
- Requiere viajes frecuentes: FLAG — discutir con usuario

### 5. Career Alignment & Motivation (0-100)
Does this role advance career goals and contain tasks that energize?

| Score | Meaning |
|-------|---------|
| 80-100 | Strongly aligned with career direction, clear growth path |
| 60-79 | Good role but only partially aligned with long-term goals |
| 40-59 | Decent job but doesn't build toward career goals |
| 0-39 | Dead end or backwards step |

**Career goals:**
- Obtener primer rol formal en datos (Data Analyst, Junior Data Scientist, BI Analyst)
- Aplicar ML y análisis de datos a problemas de negocio concretos con impacto medible
- Crecer hacia roles más autónomos en Data Science con mayor componente de ML

**Motivation filter:**
- Tareas que energizan: análisis de datos con impacto en decisiones de negocio, construcción de modelos predictivos, automatización de procesos, visualización de datos para comunicar hallazgos
- Tareas que drenan: soporte técnico puro sin componente analítico, mantenimiento sin desarrollo, trabajo administrativo sin acceso a datos

**Life situation alignment:**
- **Seguridad:** Tiene negocio propio activo como respaldo — puede ser selectivo, no necesita aceptar cualquier oferta
- **Flexibilidad:** Modalidad híbrida o remota preferible para gestionar el negocio propio
- **Desarrollo profesional:** Prioridad alta — primer rol en datos es el objetivo principal

### 6. Salary Benchmark (Optional)
Si el salary lookup tool está configurado (`salary_data.json` existe), consultarlo. Si no, omitir esta sección.

## Output Format

```
## Job Fit Evaluation: [Role] at [Company]

| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Skills | XX/100 | [brief note] |
| Experience Match | XX/100 | [brief note] |
| Behavioral Fit | XX/100 | [brief note] |
| Location | PASS/FAIL | [brief note] |
| Career Alignment | XX/100 | [brief note] |

**Overall Score: XX/100** (weighted average of scored dimensions)

### Verdict: [Strong Fit / Good Fit / Moderate Fit / Weak Fit / Poor Fit]

### Key Strengths for This Role
- [bullet points]

### Gaps to Address
- [bullet points]

### Recommendation
[1-2 sentences: apply/skip/apply with caveats]

### Company Research Checklist
- [ ] Checked company website (mission, values, recent news)
- [ ] Checked review sites (Glassdoor, Jobindex, etc.)
- [ ] Checked LinkedIn for team size, recent hires, connections
- [ ] Checked media for restructuring, growth, or workplace issues
- [ ] Identified network contacts who may know the team/manager
```

## Weighting
- Technical Skills: 30%
- Experience Match: 25%
- Behavioral Fit: 15%
- Career Alignment: 30%

(Location is pass/fail, not weighted)

## Thresholds
- **Strong Fit** (75+): Definitely apply, tailor everything
- **Good Fit** (60-74): Apply, address gaps in cover letter
- **Moderate Fit** (45-59): Consider carefully, discuss with user
- **Weak Fit** (30-44): Probably skip unless strategic reasons
- **Poor Fit** (<30): Skip

## Calibration from Past Applications

**6 aplicaciones previas, todas rechazadas — sin ninguna entrevista:**

| Empresa | Rol | Resultado |
|---------|-----|-----------|
| Neoris | Data Quality Engineer | Rechazado |
| Management Solutions | Data Science Consultant | Rechazado |
| Confidential | Business Intelligence Analyst | Rechazado |
| Banco Pichincha | Junior Data Analyst | Rechazado |
| Mardis Cia. Ltda. | Asistente de BI | Rechazado |
| AEBE | Analista de Datos Junior | Rechazado |

**Patrones identificados:**
- La mayoría de ofertas exigían 1–4 años de experiencia profesional formal en datos — gap estructural en el perfil actual
- Varias requerían títulos en estadística, economía o matemáticas — perfil de ingeniería electrónica genera fricción en filtros ATS
- Banco Pichincha y Management Solutions requerían experiencia en industria de alta intensidad de datos (banca, consultoría) — demasiado exigentes para primer rol
- AEBE (Guayaquil): location fail
- **Implicación:** Priorizar ofertas que mencionen explícitamente "recién graduados", "bootcamp", "proyectos", o que no exijan experiencia previa en datos. Roles en startups, PyMEs o consultoras pequeñas tienen menor filtro de experiencia.

## Pre-Application: Call the Employer (Best Practice)

Before writing the application, consider whether the candidate should call the contact person listed in the posting. **Only call if there are substantive questions** - never call just to "be remembered."

### When to Suggest Calling
- The posting has unclear or ambiguous requirements
- It's unclear which competencies are essential vs. nice-to-have
- The role description is vague about day-to-day tasks
- There's a named contact person who invites questions

### Good Questions to Ask
- "What are the primary challenges in this role?"
- "How is time typically divided across the listed responsibilities?"
- "Which competencies are most critical for success in this position?"
- "What does success look like in the first 6-12 months?"

### Rules for the Call
- Prepare a 30-second "elevator pitch" about your background in case they ask
- The call's purpose is **gathering information**, not delivering a pitch
- Take notes - use what you learn to tailor the application
- Reference the conversation naturally in the cover letter ("After speaking with [name], I was especially drawn to...")
