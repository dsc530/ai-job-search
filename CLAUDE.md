# Job Application Assistant for Daniel Cumbal

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for Daniel Cumbal, helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

### Identity
- **Name:** Daniel Steven Cumbal Suárez Avilés
- **Location:** Quito, Ecuador
- **Email:** dsc_530@hotmail.com
- **Phone:** +593984256115
- **LinkedIn:** https://www.linkedin.com/in/daniel-cumbal/
- **GitHub:** https://github.com/dsc530
- **Portfolio:** https://dsc530.github.io/
- **Languages:** Español (nativo), Inglés (Full Professional — TOEFL IBT 94, 2022)
- **Status:** Activo — Administrador General, Itecnologia EC (negocio propio)
- **LinkedIn headline:** "Ing. Electrónico | Data Scientist | Machine Learning | Python & SQL | Automatización"

### Education
- **Data Scientist Bootcamp** (completado Mar 2025) - TripleTen (Online, 9 meses) — Cert. #202501DSES0000904
  - Topics: Python, SQL, ML supervisado/no supervisado, series temporales, NLP, visión artificial, álgebra lineal, métodos numéricos
- **Ingeniero en Electrónica, Automatización y Control** (2009–2015) - Universidad de las Fuerzas Armadas ESPE
  - Registro SNIESE N° 1079-15-1405298, fecha 2015-09-17

### Professional Experience
- **General Manager** (Oct 2023 – Actual) - **Itecnologia EC / Negocio Propio** (Quito)
  - Migración a SQL Server + automatización con n8n
  - Desarrollo de e-commerce con Claude Code (en producción)
  - Gestión de clientes y análisis de ingresos/gastos
- **Cell Repair Technician** (Oct 2022 – Sep 2023) - **Smartbuy** (Quito)
  - Análisis de fallos recurrentes, guías para clientes, informes para dirección
- **Support Engineer** (Oct 2015 – Ene 2020) - **Uniscan Cia. Ltda.** (Quito)
  - Reducción del 50% en tickets mediante programa de capacitación
  - Proyecto DGRC 2017–2019: mantenimiento Zebra ZXP7, contrato $207.503 USD

### Technical Skills
- **Primary:** Python (Pandas, NumPy, Scikit-learn, LightGBM, XGBoost, CatBoost), SQL/SQL Server, Power BI
- **Secondary:** Matplotlib, Seaborn, Plotly, n8n, Git, TensorFlow, Java, HTML/CSS
- **Domain:** Soporte técnico hardware/software, gestión de contratos gubernamentales, análisis de negocio en PyMEs
- **Software:** Microsoft Office, LabVIEW

### Certifications
- **Data Scientist Bootcamp** - TripleTen - completado Mar 2025
- **PCAP Python Programming** - Python Institute / ESPOL
- **Introduction to IoT** - Cisco Networking Academy
- **Data Science Orientation** - IBM
- **Introduction to Cybersecurity** - Cisco
- **HarvardX PH125.1x** - edX (R Basics / Data Science)
- Git & GitHub, HTML/CSS, Java, Lógica de Programación (Platzi/otros)

### Publications
- Ninguna hasta la fecha.

### Awards
- Ninguno hasta la fecha.

### Behavioral Profile
- **Autodidacta** - Realizó transición de carrera de soporte técnico a Data Science de forma independiente
- **Orientado a negocio** - Enfoca soluciones técnicas en impacto medible en decisiones empresariales
- **Resolutivo** - Historial consistente de resolución de problemas complejos en contextos técnicos y operativos
- **Strengths:** Aprendizaje autónomo, comunicación con usuarios no técnicos, gestión de proyectos con restricciones reales
- **Growth areas:** Experiencia formal en datos (en construcción), herramientas cloud (AWS/Azure/Databricks)
- **Thrives in:** Entornos donde los datos tienen impacto en decisiones reales, roles con autonomía técnica, equipos pequeños

### What Excites You
- Aplicar ML y análisis de datos a problemas concretos de negocio con impacto medible
- Automatización de procesos y construcción de pipelines de datos
- Crecer hacia Data Engineering y arquitecturas de datos más complejas

### Target Sectors
- **Banca / Fintech:** Banco Pichincha, Produbanco, Banco del Pacífico, startups fintech ecuatorianas
- **Tecnología / Startups:** Empresas tech con operaciones en Ecuador o remotas para LATAM
- **Deportes:** Cualquier organización deportiva con operaciones de datos (preferentemente remoto)

### Deal-breakers
- Posiciones presenciales fuera de Ecuador (evaluable si la remuneración es excepcional)
- Salario inferior a USD 700/mes
- Roles puramente de soporte técnico sin componente analítico (retroceso en carrera)

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
- `.agents/skills/` - Job search CLI tools

## Workflow for New Job Applications
1. User provides a job posting (URL or text)
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and your strengths

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Claude Code** by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims (partnerships, products, technology, expansions) have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 2-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Claude Code** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output. "Looks fine in the .tex" is not acceptable - LaTeX page-break decisions are unpredictable. Iterate until these all pass:
- [ ] CV compiled with **lualatex** (pdflatex often fails on modern MiKTeX with fontawesome5 font-expansion errors). Cover letter compiled with **xelatex** (cover.cls requires fontspec).
- [ ] **CV is exactly 2 pages** - not 1, not 3
- [ ] **No orphaned `\cventry` titles** - a job/education title must never sit at the bottom of a page with its bullets spilling to the next page. Use `\needspace{5\baselineskip}` before each `\cventry` to prevent this, and `\enlargethispage{2-3\baselineskip}` to rescue a trailing section that just barely spills
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - `\lettercontent{}` must not wrap `\begin{itemize}...\end{itemize}` (the command's trailing `\\` errors on `\end{itemize}`, and moving itemize outside loses the Raleway font). Standard pattern: close `\lettercontent{}`, then wrap the list in `{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont \begin{itemize}...\end{itemize}\par}`

### ATS & keyword verification (CV)
ATS parsers read the PDF's embedded text layer, not the rendered page. Extract it with `pdftotext -layout` and verify what a parser sees. `pdftotext` (poppler) is optional - if missing, skip the parseability items with a warning and check keyword coverage from the visual PDF read instead.
- [ ] CV text layer extracts cleanly - no `(cid:*)` markers, `�` replacement characters, or text visible in the PDF but absent from the extraction
- [ ] Email and phone appear as **literal text** in the extraction (icon-glyph noise like `MOBILE-ALT`/`Envelope` is harmless, but a contact detail carried only by an icon or hyperlink is invisible to ATS)
- [ ] Reading order of the extracted text matches the visual order (single-column stock template is safe; multi-column custom templates are where this breaks)
- [ ] Posting keywords covered or honestly absent - synonym-only matches tightened to the posting's exact term where truthfully applicable, keywords the profile genuinely supports added to experience bullets, genuine gaps left visible and **never stuffed**
