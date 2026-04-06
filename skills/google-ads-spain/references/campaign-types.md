# Tipos de Campaña Google Ads

Referencia completa de tipos de campaña para lead gen / SaaS / services. NO e-commerce.

---

## 7 Estrategias Search

| # | Strategy | Description | When to use | Intent level |
|---|----------|-------------|-------------|--------------|
| 1 | **Non-brand** | Bidding en high-intent "money" keywords | Core de mayoría de cuentas. Empezar aquí | High |
| 2 | **Competitive** | Bidding en términos de competidores | Volumen búsqueda bajo (nicho/enterprise). CPCs altos pero ROI alto. Necesita LPs de comparación dedicadas | High |
| 3 | **Brand** | Bidding en tu propia marca | Defensiva. WARNING: no gastar mayoría presupuesto aquí — canibaliza orgánico. Monitorizar si competidores pujan por tu marca | Highest (pero bajo valor incremental) |
| 4 | **RLSA** | Broader keywords SOLO si usuario ya visitó tu web | Marcas establecidas con alto tráfico. No viable startups/bajo tráfico | Medium (elevado por retargeting) |
| 5 | **DSA** | Google crea anuncios automáticos basados en contenido web | Avanzado — descubrimiento keywords. NO usar sin campañas non-brand sólidas primero. Excluir homepage/blog/careers | Variable |
| 6 | **Industry** | Keyword + modificador sectorial (ej: "automatización ads para SaaS") | Intención extrema, volumen bajo. Si estimaciones muestran zero volumen → lanzar igualmente y monitorizar | Very high |
| 7 | **Content** | Bidding en queries informacionales/longtail (ej: "reglas automatizadas") | Early-stage queries significativamente más baratas | Low |

---

## Estructura B2B 4 Capas

| Capa | Tipo | Presupuesto | Función |
|------|------|-------------|---------|
| Layer 1 | High Intent | 58-80% | Captura fondo embudo. Keywords transaccionales. Hard exact/phrase |
| Layer 2 | Competitor | ~15% | Alta intención comparación. LPs dedicadas "[competidor] alternativa" |
| Layer 3 | DSA Search | Bajo | Descubrimiento keywords. Apuntar a páginas producto que convierten. Excluir home/blog/careers |
| Layer 4 | Retargeting | Bajo (€50/día) | Stay top of mind. Remarketing en YouTube/Demand Gen con demos/case studies |

**Match types B2B:** empezar con exact + phrase only. Broad match quema presupuesto sin historial masivo.

---

## PMax para Lead Gen

### Requisitos

- 30+ conversiones/30 días
- €5.000-10.000/mes mínimo
- OCI configurado y acumulando 30-60 días
- Sin OCI → "50/50 coin flip" éxito vs spam

### Setup

- 1 campaña + múltiples asset groups (1 por servicio)
- 10+ headlines, 4 long headlines, 4 descriptions
- Reutilizar headlines top de campañas search
- Testing creativo → hacer en Demand Gen/YouTube separado, no PMax

### Diagnóstico gasto

- 90%+ en search/shopping = PMax saludable
- Heavy display/video = underperforming → investigar
- PMax concentra gasto en top 20-30% keywords → breakout asset groups hambrientos

### Negativas PMax

- Guardrails, NO control granular
- Sí: servicios que no ofreces, términos basura obvios, cross-campaign cannibalization
- No: terms que no han convertido AÚN (PMax convierte en queries inesperadas)
- Usar negative keyword lists (no negativas individuales)

### PMax Local

- Funciona bien para negocios locales con códigos postales
- Diferente use case que PMax estándar
- ~20% fraude en leads PMax. Mantener presupuestos PMax tight como complemento, no escalar PMax — escalar search

### PMax asset headline optimization

1. Assets view → filtrar "headline"
2. Ordenar por impresiones → bottom 3-5 headlines con zero impresiones
3. Eliminar las bottom
4. Reemplazar con nuevos temas y formatos agresivos (no cambios menores de palabras)

---

## Demand Gen

### Qué es

- Reemplazo de YouTube campaigns para lead gen
- Placements: YouTube (in-stream, in-feed, Shorts), Discover, Gmail
- Channel selection a nivel ad group (beta)
- NUNCA Display Network en Demand Gen
- Maps inventory coming Q3/Q4 2025

### Cuándo usar

1. Resistencia CPC en search (no puedes escalar rentablemente)
2. Necesitas educar audiencia (USPs complejos)
3. Rendimientos decrecientes en Meta (ya tienes creatives)

### Presupuesto

- Google recomienda ≥€100/día o 20x cost per conversion
- Anti-pattern: €10/día en toda España = demasiado poco para learning
- Remarketing exception: €30-40/día viable con audiencia conocida + geos limitados
- Compromiso mínimo: 3 meses

### Bidding Demand Gen

| Propósito | Inicio | Progresión |
|-----------|--------|------------|
| Prospecting (frío) | Maximize clicks | Target CPC |
| Remarketing | Max conversions / max conv value | Target CPA / Target ROAS |

### Audiencias: volumen es clave

- YouTube necesita audiencias masivas
- Good: URLs, apps, listas de intereses agrupadas grandes, lookalikes amplios
- Bad: intereses pequeños (ej: "curso publicidad digital") → desastre
- Mayor masa crítica → aguanta más gasto sin romperse

### Testing

- Test geo-limitado: 1 ciudad → DG dedicado → 2-3 meses → comparar uplift
- Split ad groups por placement
- 3-5 ads/ad group. Cada 3-4 semanas: winners + iteraciones + nuevos ángulos + ofertas diferentes
- Medir rendimiento TOTAL cuenta, no solo DG → halo effects

### Demand Gen auto-generated video

- Google auto-crea videos desde imágenes/texto si solo tienes images/carousel
- Videos generados son básicos (estilo PowerPoint)
- Opt-out: Ad level → Asset optimization → desmarcar "Video"
- Desmarcar "TV screens" si no tienes video real

---

## AI Max for Search

### Qué es

- NO es tipo de campaña ni match type
- Bundle de 3 features opt-in en search campaigns:
  1. **Text customization** — Google auto-genera headlines/descriptions
  2. **Keywordless targeting** — más broad que broad match
  3. **Final URL expansion** — Google envía tráfico a cualquier página de tu web
- Internamente Google lo llama "search-only PMax"

### Cuándo usar

- Already using broad match, maxed impression share, need more reach
- 50-60 conversiones/30 días mínimo
- Ya en target CPA como bid strategy
- Non-brand IS maxed (30-40%)

### Cuándo NO usar

- Presupuesto €20/día
- Keywords exact match
- Manual bidding
- Presupuesto limitado por budget, no por reach
- Sin OCI para lead gen

### Recomendación actual

- Resultados "subpar" en mayoría de cuentas testeadas
- No expande mucho más allá de lo que broad match ya consigue
- Cuentas grandes con broad → just turn it on (bajo riesgo, ganancias marginales)
- Cuentas medianas → experiment 50/50
- Cuentas pequeñas sin broad → EVITAR. Primero hacer funcionar broad match
- Final URL expansion: DESACTIVAR si LP ya es high-converting

---

## YouTube Video Campaigns

### Budget allocation

- 5-10% del gasto total Google Ads como video testing budget
- Prerequisito: rentable en search/shopping/PMax
- B2B: <5% funciona (€500/mes → halo effect en search)

### Structure

| Campaign type | Budget % | Placements | Role |
|---------------|----------|------------|------|
| CPM campaigns | ~50% | Infeed + CTV | TOFU: impresiones baratas + volumen views |
| CPV campaigns | ~30% | In-stream, Shorts | Mid-reach: video completions |
| Demand Gen | ~20% | YouTube + Discover + Gmail | Retargeting: earned views, website visitors |

### YouTube metrics timeline

| Fase | Timeline | Metrics |
|------|----------|---------|
| Engagement | Semana 1-2 | Engagement rate (10s retention), CTR, click-to-view rate |
| Conversions | +2 semanas | Conversions, cost per conversion |
| Sales | +4 semanas | Calls booked, call quality, cost per sale |

No juzgar YouTube en métricas de ventas antes de 4 semanas.

### Testing cadence

- 2-4 ads (NO estilo Meta con muchas creatives)
- Revisar semanalmente. No tocar diario
- Esperar mínimo 1 semana por ad para datos conclusivos

### YouTube 10-second threshold

- YouTube cuenta 10 segundos para retención (no 3s como Meta)
- Retener ≥50% viewers primeros 10s = hook fuerte
- Producción profesional (audio limpio, iluminación, set limpio) = crítica para pasar threshold
