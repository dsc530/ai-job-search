# CV Templates and Tailoring Guide

## Template: LaTeX moderncv (Banking Style)

All CVs use the moderncv LaTeX package with the "banking" style and "blue" color scheme.

**Output file:** `cv/main_<company>.tex`
**Compile with:** **lualatex** on MiKTeX/TeX Live. pdflatex often fails on modern MiKTeX installs with `fontawesome5` font-expansion errors; lualatex handles the same sources cleanly.
**Master reference:** `cv/main_example.tex` (comprehensive CV with all competencies, experience, and achievements - use as source when building targeted CVs)

### Compile command

```bash
cd cv && lualatex -interaction=nonstopmode main_<company>.tex
```

Expected output: `Output written on main_<company>.pdf (2 pages, ...)`. Any page count other than 2 is a failure that must be fixed before presenting to the user.

## Document Structure

```latex
\documentclass[11pt,a4paper,sans]{moderncv}
\moderncvstyle{banking}
\moderncvcolor{blue}

\renewcommand*{\firstnamestyle}[1]{{\fontsize{34}{36}\bfseries\upshape\color{color1}#1}}
\renewcommand*{\lastnamestyle}[1]{{\fontsize{34}{36}\bfseries\upshape\color{color1}#1}}
\renewcommand*{\sectionstyle}[1]{{\sectionfont\color{color1}#1}}

\usepackage[utf8]{inputenc}
\usepackage{hyperref}
\hypersetup{
    colorlinks=true,
    linkcolor=blue,
    filecolor=magenta,
    urlcolor=blue,
    pdftitle={Daniel Cumbal - CV},
    pdfpagemode=FullScreen,
}
\usepackage[scale=0.77]{geometry}
\usepackage{import}

% Personal data
\name{Daniel}{Cumbal}
\address{Quito, Ecuador}{}{}
\phone[mobile]{+593984256115}
\email{dsc\_530@hotmail.com}
\extrainfo{\href{https://www.linkedin.com/in/daniel-cumbal/}{LinkedIn} | \href{https://github.com/dsc530}{GitHub} | \href{https://dsc530.github.io/}{Portfolio}}

\begin{document}
\makecvtitle

% 1. Profile statement (1-3 sentences, tailored per role)
% 2. Skills section
% 3. Professional Experience section
% 4. Independent Projects section
% 5. Education section
% 6. Certifications
% 7. Languages
% 8. References

\end{document}
```

### Color overrides

The three `\renewcommand*` lines in the preamble are required on lualatex+MiKTeX. Without them the firstname, lastname, and section headings render in black even though `\moderncvcolor{blue}` is set. The override forces all three to use `color1` (moderncv's accent colour).

### Spacing inside itemize lists (important)

**Do not place `\vspace{...}` between `\item` entries in an `itemize` list.** This pattern occasionally produces an oversized gap. Use native `itemsep` spacing instead.

```latex
% RIGHT
\begin{itemize}
\item \textbf{Foo}: ...
\item \textbf{Bar}: ...
\item \textbf{Baz}: ...
\end{itemize}
```

Two patterns are fine:
- `\vspace{1pt}` immediately after `\section{...}`
- `\vspace{3pt}` between top-level `\cventry` blocks

## Profile Statement Templates

### For Data Analyst / Junior Data Scientist roles:
> Electronic Engineer with a 9-month Data Science bootcamp (TripleTen, 2025) and hands-on experience applying supervised ML models — classification and regression — to real business problems. Proficient in Python (Pandas, Scikit-learn, LightGBM), SQL, and Power BI. Background in technical support and process automation provides a practical understanding of how data solutions integrate into business operations. Seeking a first formal role in data to apply and grow these skills in a collaborative environment.

*(Versión en español para ofertas en español:)*
> Ingeniero electrónico con bootcamp de Data Science de 9 meses (TripleTen, 2025) y experiencia práctica aplicando modelos de ML supervisado — clasificación y regresión — a problemas reales de negocio. Dominio de Python (Pandas, Scikit-learn, LightGBM), SQL y Power BI. Mi trayectoria en soporte técnico y automatización de procesos aporta comprensión práctica de cómo las soluciones de datos se integran en las operaciones empresariales.

### For BI Analyst / Reporting / Dashboard roles:
> Data-oriented professional with a background in technical systems and a completed Data Science bootcamp (TripleTen, 2025). Experienced in building interactive dashboards in Power BI and automating data extraction and reporting workflows using Python and SQL. Combines analytical skills with the ability to communicate findings clearly to non-technical stakeholders — developed through years of client-facing technical support and business management.

*(Versión en español:)*
> Profesional orientado a datos con formación técnica en sistemas y bootcamp de Data Science completado (TripleTen, 2025). Experiencia en construcción de dashboards interactivos en Power BI y automatización de flujos de extracción y reporte de datos con Python y SQL. Combina capacidad analítica con habilidad para comunicar hallazgos a stakeholders no técnicos.

### For Automation / Data Engineering adjacent roles:
> Electronic Engineer with strong technical foundations and a Data Science bootcamp (TripleTen, 2025). Practical experience automating business data flows using SQL Server and n8n, and developing Python scripts for data extraction, transformation, and reporting. Brings a systems-thinking approach to data pipeline problems, grounded in 10+ years of technical implementation and process optimization experience.

## Section-by-Section Tailoring

### Profile Statement / Elevator Pitch (Best Practice)
This is the most important section to customize. Write 5-7 lines that function as an "elevator pitch." Focus on what the employer gains from hiring you.

**Key framing principle for Daniel's profile:** Always lead with the concrete bootcamp + projects combination, not just the degree. The Electronic Engineering degree alone does not signal data skills to ATS filters.

### Core Competencies / Skills Section

For **Data Analyst roles**, emphasize:
- Python: Pandas, Scikit-learn, LightGBM
- SQL / SQL Server
- Power BI / Plotly / Matplotlib
- Preprocesamiento y limpieza de datos
- Modelos de clasificación y regresión supervisada

For **BI / Reporting roles**, emphasize:
- Power BI (dashboards interactivos)
- SQL (consultas, modelado de datos)
- Python (automatización, scraping, reportes)
- Comunicación de hallazgos a áreas no técnicas
- Excel avanzado

For **Automation-adjacent roles**, emphasize:
- n8n (automatización de flujos de datos)
- SQL Server
- Python scripting
- Git / control de versiones
- Experiencia en implementación tecnológica

### Education
- Always include ESPE degree (it signals engineering rigor) + TripleTen bootcamp
- For data roles: mention TripleTen curriculum highlights (ML supervisado, series temporales, NLP, visión artificial)
- Official SNIESE registration available if required

### Professional Experience

**Uniscan (Oct 2015 – Ene 2020):** Bullet más valioso = reducción 50% tickets + proyecto DGRC ($207K). Siempre incluirlos.

**Itecnologia EC (Oct 2023 – Actual):** Enfatizar la migración SQL Server + n8n como experiencia real de automatización de datos. Para roles de BI, añadir el e-commerce desarrollado con Claude Code.

**Smartbuy (Oct 2022 – Sep 2023):** Menor relevancia para roles de datos. Condensar a 2 bullets o combinar cronológicamente si el espacio es ajustado.

### Independent Projects
Siempre incluir los 3 proyectos de TripleTen con las métricas concretas. Son el núcleo de la evidencia de habilidades en datos.

### Handling the Experience Gap (Best Practice)
El gap entre ingeniería + soporte y datos es real. No ocultarlo — enmarcarlo:
- En el profile statement: "bootcamp de 9 meses + proyectos aplicados"
- En experience bullets: resaltar componentes analíticos de roles anteriores (informes para dirección, análisis de ingresos/gastos, reducción de tickets)
- En cover letter: narrativa de transición genuina y motivada

### References
- Ing. Jose Luis Trujillo — Uniscan Cia. Ltda. (carta disponible)
- "More references available upon request."

## Compile-and-Inspect Loop (MANDATORY)

After writing the CV and before presenting to the user, always compile and visually inspect the PDF. Iterate until the layout is clean. Workflow:

1. Run `lualatex -interaction=nonstopmode main_<company>.tex`
2. Check the output page count: must be exactly 2
3. Read the PDF via the Read tool and visually inspect both pages
4. Check for **orphaned entries**: a `\cventry` title line must never sit alone at the bottom of page 1

### Fixing common page-break problems

**Problem: entry title on page 1, bullets orphaned to page 2**
Add `\needspace{5\baselineskip}` immediately before the problematic `\cventry`. Include `\usepackage{needspace}` in the preamble.

**Problem: one trailing section spills to page 3**
Add `\enlargethispage{2-3\baselineskip}` before a late section.

**Problem: 3 pages with significant content on page 3**
Cut content — do not compress geometry or `\vspace`.

## ATS Parseability

```bash
cd cv && pdftotext -layout main_<company>.pdf main_<company>.txt
```

`pdftotext` is optional. If not installed, skip with a warning and rely on visual PDF read.

What to check: contact details as literal text, no garbled output, reading order matches visual, keyword coverage from posting.

## Page Budget - Hard 2-Page Limit

| Section | Max budget |
|---------|-----------|
| Profile statement | 3-4 lines |
| Skills | 5 items, each 1-2 lines |
| Most recent role | 4-5 bullets |
| Previous role | 2-3 bullets |
| Older roles | 2 bullets (1 line each) |
| Projects | 3 projects, 2-3 bullets each |
| Education | 2 entries |
| Certifications | condensed list, 1-2 lines |
| Languages | 1 line |
| References | "Available upon request." |

## Recommended Section Order

**For Data Analyst / Junior Data Scientist roles:**
1. Profile statement
2. Core competencies / Skills
3. Professional Experience (reverse chronological)
4. Independent Projects (TripleTen + e-commerce)
5. Education
6. Certifications (condensed)
7. Languages
8. References

**For BI / Reporting roles:**
1. Profile statement
2. Core competencies / Skills
3. Professional Experience
4. Independent Projects
5. Education
6. Languages
7. References
