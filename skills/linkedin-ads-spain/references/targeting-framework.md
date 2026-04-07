# Framework de Targeting — LinkedIn Ads

## Filtros Core (Lógica AND)

**Mínimo 3 filtros combinados con AND.** Nunca un solo filtro.

| Filtro | Descripción | Ejemplo |
|---|---|---|
| **Company size** | Rango empleados | 11-200 (SMB SaaS) |
| **Industry** | Sector empresa | Technology, Information |
| **Job titles** | Títulos profesionales | Growth, Demand Gen, Marketing Ops |

### Lógica AND vs OR

- **Dentro de un facet (OR):** seleccionar múltiples job titles = target Title A OR B OR C
- **Entre facets (AND):** Company Size + Job Title = debe cumplir AMBOS
- **"Narrow audience further":** AND explícito dentro del mismo tipo (ej: Skill A AND Skill B)
- **Exclude (NOT):** elimina valores específicos de cualquier facet

**Regla:** siempre AND entre facets. Nunca depender de un solo filtro → demasiado broad.

---

## Super Titles — Verificar SIEMPRE

LinkedIn agrupa títulos bajo "super titles" genéricos:
- "Head of Marketing" → incluye Growth Marketing Lead, Brand Strategist, Marketing Ops Coordinator
- **SIEMPRE verificar Demographics post-lanzamiento** para confirmar títulos reales

### Proceso de verificación

1. **Pre-lanzamiento:** revisar segment breakdown window durante setup
2. **Post-lanzamiento (día 3-5):** Campaign Manager → Demographics tab
3. Verificar: Job titles, Companies, Industries, Company sizes, Seniority
4. Si títulos/empresas incorrectas → exclusiones inmediatas

---

## Tamaño de Audiencia

| Presupuesto | Tamaño target |
|---|---|
| <€10K/mes | 20K-50K |
| €10K-30K/mes | 50K-100K |
| >€30K/mes | 100K+ |

Demasiado grande = baja penetración (la mayoría no verá tus ads). Demasiado pequeño = budget burn.

---

## Matched Audiences

### Qué son
Custom audiences de listas de empresas/contactos subidas directamente.

### Setup
1. Subir CSV con emails o company names + domains
2. LinkedIn matchea contra perfiles
3. Mínimo **300 miembros matched** para permitir targeting
4. Añadir filtros de job title/seniority **encima** de la lista

### Fuentes
- CRM (mejores listas)
- Apollo, ZoomInfo, Cognism
- Sales Navigator

### Mantenimiento
- Refresh cada **90 días** (personas cambian de trabajo/email)
- Automatizar vía CRM → Zapier → LinkedIn
- Match rate esperado: >30% = bueno, <10% = revisar formato CSV

### Matched Audience bypass
La mejor forma de superar las limitaciones de matching nativo de LinkedIn es bypass con herramientas third-party. Build listas exactas basadas en revenue o tech stack off-platform → subir como Matched Audience → layer filtros LinkedIn encima.

---

## Predictive Audiences (Lookalikes de LinkedIn)

- Build desde Matched Audiences (listas, web visitors, conversion events)
- Mínimo 300 miembros en audiencia fuente
- **First-party CRM lists > website visitors** como fuente
- Revisar Demographics post-launch — pueden drift del ICP
- Usar como expansión cuando targeting directo está saturado

---

## Exclusiones — La Lista Más Importante

| Categoría | Qué excluir |
|---|---|
| Competidores | Company names de competidores |
| Empleadores anteriores | Ex-empresas del equipo |
| Clientes actuales | Sign-ups + paying customers |
| Enterprise fuera de ICP | Empresas demasiado grandes/pequeñas |
| Industrias irrelevantes | Industrias adyacentes que LinkedIn filtra mal |
| Edades extremas | <24 (si no target junior), >55 (según ICP) |
| Job titles irrelevantes | Interns, students, roles no-target |
| RTG audience en Cold | Excluir retargeting audience de campañas cold |
| Customers de todo | Excluir clientes de TODAS las campañas |

**La lista de exclusiones suele ser MÁS LARGA que la de inclusiones.** Construir y mantener una master exclusion list actualizada.

---

## Audiencias de Retargeting

### Fuentes y lookbacks

| Fuente | Lookback | Uso |
|---|---|---|
| Website traffic (all) | 90 días | RTG general |
| Company page visits | 90 días | RTG general |
| Ad engagement (cold) | 90 días | RTG general |
| High-intent URLs (/demo, /pricing, /signup) | 30-90 días | **High-intent RTG** |
| Exclusion URLs (/login, /careers, /partners) | 30-180 días | **EXCLUSIÓN** |
| Video 25% viewers | 30-90 días | RTG broad |
| Video 50% viewers | 30-90 días | Mid-funnel offers |
| Video 75% viewers | 30-90 días | Demos/trials |
| Document ad engagers | 90 días | RTG engagement |
| Lead Gen Form openers (no completaron) | 90 días | Re-engagement |
| Conversation ad openers | 90 días | Re-engagement |

### Estrategia por volumen de tráfico

- **Startup / bajo tráfico:** cluster todo (web + ad engagers + video views) en una sola audiencia 90 días. Escalar a 50K+ para poder layer job functions/seniority
- **Enterprise / alto tráfico:** segmentar por timeframe (30d → 90d → 180d), excluir timeframes previos para graduar usuarios

---

## Targeting Avanzado

### Skills Targeting

- Target por skills en perfil (ej: "Salesforce", "HubSpot", "Python")
- **Potente para SaaS:** target usuarios de herramientas competidoras o complementarias
- Caveat: skills son auto-reportadas, pueden estar desactualizadas. Layer con job title

### Company Revenue

- Segmentar por brackets de facturación anual
- Employee count no siempre correlaciona con budget (startup 50 personas funded > nonprofit 500 personas)
- No todas las empresas tienen revenue data en LinkedIn

### Company Growth Rate

- Segmentar por trayectoria: negativa, 0-3%, 3-10%, 10-20%, 20%+
- Empresas crecimiento rápido (>20%) = más probable que inviertan en herramientas
- Combinar: high growth + industria relevante + decision-maker titles = alta intención

### Technologies Used (Technographic)

- Target por tecnologías que usa la empresa ("Uses Salesforce", "Uses AWS")
- Cobertura y precisión variable. Cross-reference con Apollo, BuiltWith

### Member Groups

- Filtrar por grupos de LinkedIn = señal de intención alta
- Ej: grupos de "payroll", "HR technology", grupos de competidores
- Uno de los filtros más fuertes para leads high-intent

### Member Interests & Traits

- LinkedIn infiere intereses de engagement en contenido y grupos
- Menos preciso que job title o company targeting
- Usar como lever de expansión, no como filtro primario

### Device Preference: Desktop

- LinkedIn no permite targeting directo por dispositivo
- Pero se puede usar filtro **"Device preference: Desktop"** en member traits
- Desktop = mayor conversión B2B, menor CPL
- Históricamente mejores resultados que mobile para B2B lead gen

---

## Industry Matching — Limitaciones

LinkedIn mapea empresas a una sola industria (la que eligieron al crear la página):
- Fintech puede estar bajo "Financial Services", "Software Development" o "Technology"
- Con filtros precisos de industria, ads seguirán "leaking" a industrias adyacentes
- **Solución:** Company Engagement Breakdown audit + master exclusion list

### Auditoría de Company Engagement Breakdown

1. Check "Company Engagement Breakdown" y "Professional Demographics" tabs
2. Identificar empresas irrelevantes (massive enterprises, competidores, interns)
3. Añadir a master exclusion list (actualizar continuamente)

---

## Audience Templates

- LinkedIn ofrece templates pre-built (ej: "IT Decision Makers", "CMOs")
- **Solo como punto de partida.** Nunca correr un template sin modificar → demasiado broad
- Campaign Manager → Audience → Saved Audiences → LinkedIn Templates
- Siempre customizar añadiendo filtros específicos
