# Search Queries for Job Scraper — Daniel Cumbal

## Context

Daniel is based in **Quito, Ecuador**. He is open to:
- Presencial en Quito (ideal)
- Remoto desde Ecuador (excelente)
- Fuera de Quito presencial (evaluable si la remuneración lo justifica)
- Guayaquil presencial (posible si el salario es significativamente superior)

**Salary floor:** USD 700/month minimum.
**Search languages:** Spanish AND English.
**Target sectors:** Banking/fintech, technology/startups, sports (especially remote).

## Search Sites

Primary portals to check:
- **linkedin.com/jobs** — mayor alcance internacional y remoto
- **computrabajo.com.ec** — principal bolsa de empleo Ecuador
- **hiringroom.com** — bolsa latinoamericana con foco en tech
- **indeed.com** — buscar con filtro Ecuador o Remote/Latin America
- **glassdoor.com** — útil para investigar empresas + algunas ofertas

Note: Los portales daneses (jobindex.dk, etc.) del framework original no aplican para Ecuador. Usar los portales arriba en su lugar.

## Query Categories

### Priority 1: Data Scientist / Científico de Datos (meta principal)

Rol deseado a mediano plazo. Aplicar cuando los requisitos de experiencia sean razonables (0-2 años o "recién graduados bienvenidos").

```
site:linkedin.com/jobs "data scientist" Ecuador
site:linkedin.com/jobs "científico de datos" Ecuador
site:linkedin.com/jobs "junior data scientist" remote Latin America
site:computrabajo.com.ec "data scientist" Quito
site:computrabajo.com.ec "científico de datos"
site:hiringroom.com "data scientist"
site:indeed.com "data scientist" Ecuador
```

### Priority 2: Data Analyst / Analista de Datos (entrada más realista ahora)

Rol con menor barrera de entrada. Priorizar para candidaturas inmediatas.

```
site:linkedin.com/jobs "data analyst" Ecuador
site:linkedin.com/jobs "analista de datos" Quito
site:linkedin.com/jobs "junior data analyst" remote
site:computrabajo.com.ec "analista de datos" Quito
site:computrabajo.com.ec "analista de datos junior"
site:hiringroom.com "data analyst"
site:indeed.com "analista de datos" Ecuador
site:glassdoor.com "data analyst" Ecuador
```

### Priority 3: BI Analyst / Business Intelligence

Encaje fuerte dado el dominio de Power BI y SQL. Buen punto de entrada con clara ruta hacia Data Science.

```
site:linkedin.com/jobs "BI analyst" Ecuador
site:linkedin.com/jobs "business intelligence" Quito
site:linkedin.com/jobs "analista de inteligencia de negocios" Ecuador
site:computrabajo.com.ec "business intelligence" Quito
site:computrabajo.com.ec "analista BI"
site:hiringroom.com "business intelligence"
site:indeed.com "Power BI" analyst Ecuador
```

### Priority 4: Data Engineer Junior / Ingeniero de Datos (meta a largo plazo)

Meta de carrera a mediano-largo plazo. Aplicar solo si los requisitos técnicos son alcanzables con el perfil actual (Python + SQL + pipelines básicos).

```
site:linkedin.com/jobs "junior data engineer" remote Latin America
site:linkedin.com/jobs "ingeniero de datos" Ecuador
site:linkedin.com/jobs "data engineer" Ecuador entry level
site:computrabajo.com.ec "ingeniero de datos" Quito
site:hiringroom.com "data engineer" junior
```

### Priority 5: Skill-based searches (red amplia)

Búsquedas por habilidades específicas para capturar ofertas con títulos distintos.

```
site:linkedin.com/jobs "Python" "machine learning" Ecuador
site:linkedin.com/jobs "Python" "SQL" "Power BI" Ecuador remote
site:linkedin.com/jobs "scikit-learn" OR "LightGBM" Ecuador
site:computrabajo.com.ec "Python" "datos" Quito
site:hiringroom.com "Python" "machine learning"
site:indeed.com "Python" "SQL" "datos" Ecuador
```

### Priority 6: Sector deportivo (remoto — baja frecuencia en Ecuador)

Nicho de interés personal. Buscar principalmente en plataformas con alcance internacional.

```
site:linkedin.com/jobs "data analyst" sports remote
site:linkedin.com/jobs "sports analytics" remote Latin America
site:linkedin.com/jobs "data scientist" sports remote
site:linkedin.com/jobs "analista de datos" deporte remote
```

## Location Filter

When evaluating results, classify location as:
- **Ideal:** Quito presencial o remoto desde Ecuador
- **Aceptable:** Híbrido Quito, remoto América Latina
- **Evaluar:** Otra ciudad Ecuador presencial (depende de salario)
- **Flag:** Requiere reubicación fuera de Ecuador (discutir con usuario)

## Salary Filter

Descartar ofertas donde el rango salarial indicado sea claramente inferior a USD 700/mes. Si el salario no está indicado, incluir la oferta pero marcar como "salario no especificado".

## Date Filter

Solo incluir ofertas publicadas en los últimos 14 días, o con fecha límite de postulación aún vigente. Si no se puede determinar la fecha, incluir pero marcar como "fecha desconocida".

## Adapting Queries

Si el usuario especifica un foco con `/scrape [focus]`, seleccionar las queries de la categoría correspondiente y generar 2-3 queries adicionales específicas para ese foco. Ejemplos:
- `/scrape remoto` → priorizar queries con "remote" / "remoto"
- `/scrape banca` → añadir queries con "banco", "fintech", "financiero"
- `/scrape deportes` → usar Priority 6 + custom queries
