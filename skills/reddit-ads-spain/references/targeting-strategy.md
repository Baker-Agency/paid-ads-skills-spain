# Targeting Strategy — Reddit Ads España

## Proceso Investigación Subreddits

### Paso a Paso

1. **Reddit Pro:** Introducir marca + 5-10 keywords industria → top 20 subreddits por keyword
2. **Visitar manualmente:** Evaluar cada subreddit con scoring table
3. **Google search:** `site:reddit.com [categoría producto]`
4. **Competidores:** Buscar nombres competencia en subreddits
5. **Leer 20-30 posts recientes** en cada candidato → anotar lenguaje, pain points, sentimiento
6. **Puntuar:** Weighted scoring (ver abajo)
7. **Agrupar:** Clusters temáticos de 3-5 subreddits por ad group

### Scoring Table

| Criterio | 1 (Malo) | 3 (Aceptable) | 5 (Excelente) | Peso |
|---|---|---|---|---|
| Match ICP | Tangencialmente relacionado | Mixta | Core ICP | 3x |
| Tamaño (suscriptores) | <10K | 10-100K | 100K-1M | 2x |
| Actividad | <5 posts/día | 5-20 posts/día | 20+ posts/día | 2x |
| Tolerancia ads | Hostil | Neutral | Ads presentes, engagement positivo | 1x |
| Fit contenido | Oferta fuera de lugar | Relevancia tangencial | Resuelve problemas discutidos diario | 2x |

- **≥35:** Ad groups primarios
- **25-34:** Ad groups testing
- **<25:** Excluir

### Subreddits por Vertical

| Vertical | Subreddits Ejemplo |
|---|---|
| B2B SaaS | r/SaaS, r/startups, r/Entrepreneur, r/smallbusiness, r/sysadmin, r/devops |
| Developer tools | r/programming, r/webdev, r/javascript, r/python, r/selfhosted |
| Marketing SaaS | r/PPC, r/digital_marketing, r/marketing, r/SEO, r/analytics |
| Fintech | r/personalfinance, r/investing, r/FinancialPlanning |
| Servicios profesionales | r/smallbusiness, r/Accounting, r/legaladvice, r/consulting |

### Subreddits España-Específicos

| Subreddit | Suscriptores (aprox) | Idioma | Uso |
|---|---|---|---|
| r/spain | ~300K | EN/ES | General España — audiencia amplia |
| r/es | ~100K | ES | Comunidad hispanohablante |
| r/askspain | ~50K | EN/ES | Preguntas sobre España — turismo, vida |
| r/SpainPolitics | ~30K | ES | Política — evitar para B2B |
| r/Barcelona | ~100K | EN/ES | Local Barcelona |
| r/Madrid | ~80K | EN/ES | Local Madrid |

**Nota:** Subreddits españoles son significativamente más pequeños que equivalentes US. Para B2B/SaaS, subreddits en inglés suelen ser más efectivos (profesionales técnicos españoles consumen en inglés).

## Tipos de Targeting

### Community (Subreddit) — Siempre Empezar Aquí

- Más preciso. Match ICP directo
- Agrupar por tema, NO por tamaño
- Cada ad group = 3-5 subreddits con intent similar
- Ejemplo:
  - AG "Technical Decision Makers": r/sysadmin, r/devops, r/networking
  - AG "Business Buyers": r/startups, r/smallbusiness, r/Entrepreneur

### Keyword Targeting — Complementar Communities

**Buenos keywords (intent alto):**
- "best CRM for startups"
- "alternative to [competidor]"
- "[competidor] vs [competidor]"
- "how to automate [proceso específico]"

**Malos keywords (demasiado amplios):**
- "software", "business", "help", "tool", "app"

**Keywords negativos (añadir inmediatamente):**
- Términos empleados competencia (hiring, salary, interview, glassdoor)
- Términos estudiantes (homework, assignment, ELI5 si irrelevante)
- NSFW si requiere brand safety

### Interest Targeting — Tras Plateau Communities

- Más escala, menos precisión
- 3-8 categorías interest, lógicamente relacionadas al ICP
- Separar en ad groups diferentes para testing
- Activar Audience Expansion SOLO tras baseline community targeting establecido

## Custom Audiences — Cronología

| Semana | Audiencia | Uso | Pool mínimo |
|---|---|---|---|
| 1 | Ninguna (pixel recién instalado) | Solo prospecting | N/A |
| 2-3 | Visitantes web 7-14d | Retargeting: test desktop-only vs all-devices | 1.000 mín |
| 4 | Visitantes 30d + ad engagers | Split: 7d hot vs 8-30d warm | 1.000 por segmento |
| Mes 2 | Visitantes página pricing/demo, form abandoners | Retargeting high-intent con CTA directo | 500 mín |
| Mes 2-3 | CRM list upload | Excluir clientes. Crear "customer lookalike" | 1.000 emails mín |
| Mes 3+ | Lookalike de converters | Layer sobre community targeting | Seed 100+ converters ideal |

## 6 Exclusiones Obligatorias

| # | Exclusión | Impacto si falta |
|---|---|---|
| 1 | Empleados (emails dominio) | 3-10% budget desperdiciado |
| 2 | Clientes existentes (CRM upload) | Budget adquisición en gente ya comprada |
| 3 | Retargeting excluido de prospecting | Frequency overload, canibalización |
| 4 | Geos sin valor (bulk upload zips) | Gasto en zonas que nunca convierten |
| 5 | Usuarios convertidos | Pagar por re-convertir |
| 6 | Subreddits spam/low-intent | CTR alto pero zero conversiones |

**Bug Audience Estimator:** Se rompe si audiencia exclusión > audiencia target (incluso sin overlap). Ignorar estimator, lanzar, monitorizar delivery real.

## Geographic, Device & Dayparting

### Geo Targeting España

- Empezar con España completa (país nivel)
- Reddit NO tiene geo-targeting granular (metro/ciudad no disponible)
- Usar exclusiones estado/región si servicios son locales
- **Servicios locales → Reddit NO recomendado** como canal primario (Google Local + Meta mejor)

### Device

| Escenario | Setting |
|---|---|
| Prospecting frío | All devices (Reddit móvil ~70% uso) |
| Retargeting | Desktop-only inicialmente (B2B convierte mejor desktop) |
| B2B SaaS | Test desktop-only AG vs all-devices AG |

### Dayparting

| Escenario | Schedule |
|---|---|
| Default (campañas nuevas) | Todas las horas, todos los días |
| B2B tras 2 semanas datos | Test 18:00-21:00 CET (post-trabajo España) |
| B2B fines de semana | Mantener pero monitorizar separado (usage alto pero intent puede diferir) |

### Género

- Target TODOS los géneros. Muchos usuarios Reddit no declaran género
- Restringir género = excluir gran porción de audiencia sin beneficio

## Gap Matrix Competitiva

| Subreddit | Suscriptores | Posts/día | Competidor A? | Competidor B? | Nosotros? | ¿Oportunidad? |
|---|---|---|---|---|---|---|
| r/[ejemplo1] | ___K | ___ | Sí/No | Sí/No | Sí/No | [ ] |
| r/[ejemplo2] | ___K | ___ | Sí/No | Sí/No | Sí/No | [ ] |

**Gap = subreddit con >50K suscriptores, >10 posts/día, competidores ausentes, ICP relevante.** Priorizar gaps para targeting inicial — menos competencia = CPCs más bajos.
