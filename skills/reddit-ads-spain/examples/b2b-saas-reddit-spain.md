# Ejemplo: B2B SaaS — Reddit Ads España

## Escenario

- **Producto:** SaaS de automatización de reporting para equipos marketing
- **ACV:** €8.000/año
- **Mercado:** España + LATAM hispanohablante
- **Presupuesto Reddit:** €5.000/mes
- **Canales existentes:** Google Search (€10.000/mes), Meta (€3.000/mes)

## Unit Economics

| Métrica | Valor |
|---|---|
| ACV | €8.000 |
| CAC objetivo (12%) | €960 |
| Tasa cierre (lead → cliente) | 10% |
| CPL max viable | €960 × 10% = **€96** |
| CPC estimado Reddit | €5 |
| CVR LP necesaria | €5 ÷ €96 = **5,2%** |
| Veredicto | Viable con buena oferta |

## Arquitectura Campaña

| Campaña | Budget % | Ad Groups |
|---|---|---|
| PROSP - Conversiones | 65% (€3.250) | AG1: r/marketing r/digital_marketing r/analytics (cluster marketing). AG2: r/SaaS r/startups (cluster SaaS). AG3: Keywords intent alto |
| RTG - Conversiones | 25% (€1.250) | AG1: Site visitors 30d - Desktop. AG2: Site visitors 30d - All |
| TEST - Traffic | 10% (€500) | AG1: Nuevos subreddits / nuevos formatos |

## Estrategia Creativa

### Oferta Principal (Prospecting)
**Free trial 14 días sin tarjeta** — CVR esperada 6-10%

### Ad Free-Form Text (Ejemplo)

> **Hook:** "Si eres CMO o Head of Marketing gastando 5+ horas/semana creando reportes de campaña..."
>
> **Agitación:** "El 73% de los marketers dice que el reporting manual es la tarea que más odian. Y mientras tanto, los datos se quedan obsoletos antes de que lleguen a la reunión."
>
> **Valor:** "Construimos [Producto] después de hablar con 200 marketing managers que tenían el mismo problema. Conecta Google Ads, Meta, LinkedIn, GA4 y tu CRM en un dashboard que se actualiza solo."
>
> **Solución:** "14 días gratis, sin tarjeta. Si no te ahorra al menos 3 horas/semana, no pagues."
>
> **CTA:** "Link en comentarios. Feliz de responder preguntas sobre cómo funciona."

### Variantes a Testear

| Variante | Ángulo | Formato |
|---|---|---|
| V1 | Problem-focused (reporting manual) | Free-form text |
| V2 | Outcome (ahorro 5h/semana) | Free-form text |
| V3 | Social proof (200 equipos usan) | Imagen con dashboard screenshot |
| V4 | Contrarian (por qué los dashboards custom fallan) | Free-form text |
| V5 | Founder story (por qué lo construimos) | Free-form text |

## Targeting

### Subreddits Primarios (AG1 — Cluster Marketing)
- r/PPC (~100K) — Score: 42/50
- r/digital_marketing (~350K) — Score: 38/50
- r/analytics (~200K) — Score: 40/50

### Subreddits Secundarios (AG2 — Cluster SaaS)
- r/SaaS (~50K) — Score: 36/50
- r/startups (~1M) — Score: 35/50
- r/Entrepreneur (~2M) — Score: 30/50

### Keywords (AG3)
- "marketing reporting tool"
- "automated marketing dashboard"
- "alternative to [competidor]"
- "Google Ads + Meta reporting"

## Timeline Esperado

| Semana | Hito | KPIs Esperados |
|---|---|---|
| 1-2 | Setup + launch prospecting | Delivery OK, CTR >0,3%, CPC ~€5 |
| 3-4 | Primera lectura + launch RTG | 15-25 leads, CPL €40-80 |
| 5-8 | Optimización: kill bottom subreddits, nuevo creativo | CPL baja 15-20%, 30-40 leads/mes |
| 9-12 | Escalar: +20% budget, nuevos subreddits | 40-50 leads/mes, CPL estabiliza |

## Métricas Mes 3 (Objetivo)

| Métrica | Target |
|---|---|
| Gasto | €5.000 |
| Impresiones | ~500K |
| Clics | ~1.000 (CTR 0,5%) |
| Leads | 40-50 (CVR LP 4-5%) |
| CPL | €100-125 |
| MQLs | 12-15 (30% MQL rate) |
| SQLs | 4-5 (30% SQL rate) |
| Clientes | 1 (20% close rate) |
| CPA | ~€5.000 |
| ROAS | €8.000 ÷ €5.000 = 1,6x (primer año) |
| LTV:CAC | Con retención 3 años: €24.000 ÷ €5.000 = 4,8x |

## Notas España

- Ads en **inglés** (subreddits internacionales, audiencia técnica española consume EN)
- LP en **español** con opción inglés (el usuario ya está en fase consideración)
- Agosto: reducir budget a €2.500 (vacaciones masivas España)
- WhatsApp como canal soporte post-lead (preferencia española)
- CAPI implementar en mes 2 para recuperar señal perdida por LOPD
