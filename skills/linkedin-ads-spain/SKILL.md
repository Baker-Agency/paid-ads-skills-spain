---
name: linkedin-ads-spain
description: LinkedIn Ads campaign management for the Spanish market (Spain). Setup, optimize, scale, and audit LinkedIn Ads campaigns for lead gen, SaaS, and services targeting Spain. Use when managing LinkedIn Ads for Spanish B2B clients, launching campaigns in Spain, auditing Spanish LinkedIn Ads accounts, creating Thought Leader Ads, managing conversation ads, targeting audiencias B2B, or adapting LinkedIn strategy for the Spanish/European market. Covers all ad formats (TLA, Image, Video, Document, Carousel, Conversation, Spotlight, Text), targeting, bidding, Lead Gen Forms, ABM, CAPI tracking, and Revenue Attribution for Spain.
---

# LinkedIn Ads España — Skill de Gestión Completa

Gestión integral de LinkedIn Ads para lead gen, SaaS y servicios B2B en el mercado español. NO e-commerce.

**Todo el contenido está adaptado al mercado español:** benchmarks en EUR, IVA 21%, LOPD/GDPR, estacionalidad española, copy en español.

## Quick Reference — España

| Métrica | Valor España |
|---|---|
| CPC estimado España | €8-14 (inferior a Norteamérica) |
| Presupuesto mínimo recomendado | €3.000-5.000/mes |
| Nº máximo campañas | presupuesto diario ÷ €100 |
| Ciclo compra B2B medio | 192 días, 62+ touchpoints |
| CTR medio LinkedIn | 0,4% (>0,7% bueno, >1% excelente) |
| Engagement rate TLA | 5-15% |
| Open rate Conversation Ads | 30-40% (50-70% con buen subject line) |
| Lead Gen Forms vs web | 2-5x más conversión, menor calidad |
| Usuarios que clican en ads | 0,04% — el 99%+ es invisible si mides solo clics |
| Audience Network (LAN) | **DESACTIVAR siempre** |
| IVA | 21% (incluir en cálculos de unit economics) |
| GDPR + LOPD | Aplicable. Consent checkbox obligatorio en LGF |
| LinkedIn ROI vs Facebook (B2B) | 2x ROI a deal cerrado (pese a 3-5x más CPC) |
| Solo ~5% cold audience | está en mercado en cualquier momento |

---

## Fase 0: Evaluación de Viabilidad

### Fórmula de viabilidad de presupuesto

Presupuesto mensual ÷ 30,4 = presupuesto diario. Presupuesto diario ÷ €100 (mín €50) = máx campañas activas.

| Presupuesto/mes | Diario | Máx campañas |
|---|---|---|
| €3.000 | €99 | 1 |
| €5.000 | €164 | 1-2 |
| €10.000 | €329 | 3 |
| €30.000 | €987 | 9-10 |

**Nunca** bajar de €50/día por campaña. A €12 CPC = ~4 clics/día. Por debajo = learning phase perpetua.

### Scorecard de viabilidad Greenfield

| Factor | 1 (Malo) | 3 (Aceptable) | 5 (Excelente) |
|---|---|---|---|
| ACV | <€3K | €5-25K | >€25K |
| Ciclo de venta | >12 meses | 3-6 meses | 1-3 meses |
| Claridad ICP | Vago ("todas las empresas") | Definido (industria + tamaño) | Preciso (títulos + empresas + tech stack) |
| Presupuesto | <€3K/mes | €3-10K/mes | >€10K/mes |
| Presencia orgánica LinkedIn | Sin presencia | Posts ocasionales | Liderazgo activo con engagement |
| Madurez CRM | Hojas de cálculo | CRM básico | CRM limpio con lifecycle stages + scoring |
| Biblioteca de contenido | Nada | Solo blog | Case studies + webinars + demos |

- **25-35:** Excelente candidato. Proceder.
- **15-24:** Viable con caveats. Resolver gaps primero.
- **<15:** LinkedIn probablemente no es el canal adecuado aún.

### Cuándo LinkedIn NO es el canal correcto

- ACV <€3K sin upsell path → CPC demasiado alto para unit economics
- Audiencia no está en LinkedIn (blue collar, retail, consumidor local)
- Zero contenido o presencia orgánica y sin presupuesto para crearlo
- Sin CRM ni infraestructura de tracking → no se pueden medir resultados
- Equipo de ventas no hará follow-up de leads en <24h

### Unit economics LinkedIn vs Meta (B2B)

- Meta CPC/CPL = ~1/3 de LinkedIn
- Pero **90% de leads de Meta descartados** en B2B — personas incorrectas
- LinkedIn leads raramente descartados
- Medido hasta deal cerrado: LinkedIn ROI = **2x Facebook**
- Razón: LinkedIn tiene monopolio en datos profesionales (título, empresa, industria, seniority)

---

## Fase 1: Setup de Cuenta y Lanzamiento

### Arquitectura de cuenta

Campaign Groups por etapa de funnel:

| Campaign Group | Propósito | % Presupuesto |
|---|---|---|
| **Cold** | Awareness, llegar a ICP frío | 60-70% |
| **Retargeting** | Nutrición web visitors + ad engagers | 20-30% |
| **High-Intent RTG** | Conversation ads, últimos empujones | 5-10% |
| **Acceleration** | Ads contra oportunidades abiertas en CRM | 5-10% |

### Naming conventions

- **Campaign Group:** `[Estrategia] - [Objetivo]` (ej: `RTG - Lead Gen`)
- **Campaign:** `[Estrategia] [Timeframe] [Audiencia] [Ubicación] [Industria] [Fecha]`
- **Ad:** descriptivo por formato y mensaje

### Checklist de settings para España

- [ ] Objetivo: **Website Visits** (default). Solo Engagement para TLAs
- [ ] Location targeting: **"Permanent"** solamente, NO "Recent or permanent"
- [ ] Audience Network (LAN): **DESACTIVAR**
- [ ] Audience expansion: **DESACTIVAR**
- [ ] Connected TV (CTV): **DESACTIVAR**
- [ ] Bidding: **Manual SIEMPRE** (empezar a 2/3 del bid recomendado)
- [ ] "Enable bid adjustment for high-value clicks": **DESACTIVAR**
- [ ] Tamaño audiencia: 20K-50K para presupuestos <€10K/mes
- [ ] Filtros core: company size + industry + job titles (lógica AND, NO OR)
- [ ] UTM parameters a nivel cuenta: `utm_source=linkedin`, `utm_medium=paid_social`

### Exclusiones (día 1)

- Competidores
- Empleadores anteriores
- Clientes actuales (sign-ups + customers)
- Empresas enterprise fuera de ICP
- Industrias irrelevantes adyacentes

La lista de exclusiones suele ser **más larga que la de inclusiones** — LinkedIn filtra tanto que necesitas exclusiones agresivas.

→ Detalle completo: [references/campaign-setup-checklist.md](./references/campaign-setup-checklist.md)

---

## Fase 2: Formatos de Anuncio

| Formato | Engagement/CTR | Coste | Mejor para | Nota clave |
|---|---|---|---|---|
| **Text Ads** | Casi 0 clics | Near-free (19K imp/€0 en 7 días) | Capa de impresiones gratuita | Usar en COLD y RTG |
| **Image Ads** | CTR 0,4% avg, >0,7% bueno, >1% excelente | CPC €8-14 | Core del funnel | Lanzar mín 20 variaciones |
| **Thought Leader Ads** | 5-15% engagement | CPC ~€1 | Formato estrella — orgánico → paid | Test orgánico primero, 100+ likes → promover |
| **Conversation Ads** | 30-40% open rate | Bajo por send | Solo retargeting high-intent | Subject line es todo |
| **Document Ads** | ~6% engagement | Medio | Content offers, gated/ungated | Cover page = thumbnail |
| **Video Ads** | Medir por watch time, NO CTR | CPV €0,05-0,15 | Brand awareness, retargeting pools | Subtítulos OBLIGATORIOS |
| **Carousel Ads** | Entre image y document | Medio | Storytelling, features | 3-5 cards óptimo |
| **Spotlight Ads** | Casi 0 CTR | ~€90 por 86K impresiones | Capa ultra-barata desktop | NO optimizar por CTR |
| **Lead Gen Forms** | 2-5x conversión vs web | Variable | TOFU content offers, móvil | Datos se borran a 90 días |
| **Partnership Ads** | Alto engagement | Variable | Social proof, reviews | Solo Awareness/Engagement |

→ Detalle completo: [references/ad-formats-guide.md](./references/ad-formats-guide.md)

---

## Fase 3: Copy y Creativos (Mercado Español)

### Tú vs Usted en LinkedIn España

| Sector | Tratamiento | Ejemplo |
|---|---|---|
| B2B Enterprise / Corporate | Usted | "Descubra cómo optimizar su pipeline" |
| Legal, financiero, banca | Usted | "Solicite una consulta personalizada" |
| SaaS / Startups / Tech | Tú | "Descubre cómo escalar tu equipo" |
| Agencias, marketing, coaching | Tú | "Transforma tu estrategia de captación" |
| Consultoría | Usted (formal) | "Mejore sus resultados comerciales" |

### Approach emotion-first

- **Mal:** "Nuestra plataforma te ayuda a rastrear ROI de LinkedIn"
- **Bien:** "Tu jefe cree que LinkedIn no funciona porque [pain point]. Así se demuestra lo contrario."

Primero = emoción/reconocimiento. Producto después.

### Frameworks de copy

| Framework | Estructura | Ejemplo (español) |
|---|---|---|
| **Problem-Authority** | Problema → Tu autoridad → Solución | "El 77% de los marketers miden mal el ROI de LinkedIn. Llevamos 5 años resolviendo esto." |
| **Data Shock** | Dato sorprendente → Implicación → Acción | "Solo el 0,04% de usuarios clica en ads de LinkedIn. ¿Tu estrategia depende de ese 0,04%?" |
| **Contrarian** | Opinión contra-corriente → Por qué → Prueba | "Los Lead Gen Forms están saboteando tu pipeline. Aquí los datos." |
| **Empathy** | Empatizar con dolor → Agitar → Resolver | "¿Otro trimestre justificando el gasto en LinkedIn sin datos reales?" |

### Estructura PAS para B2B español

1. **Problema:** "¿Tu equipo de ventas descarta el 90% de los leads de paid?"
2. **Agitación:** "Cada lead malo consume tiempo de SDRs que podrían cerrar deals reales..."
3. **Solución:** "[Tu servicio] conecta marketing con pipeline real en [plazo]"

### Distinctive brand assets

Incluir logo, colores, estilo visual o mascota en **CADA anuncio**. La consistencia visual = recall. Las personas recuerdan patrones visuales, no headlines individuales.

### Conversation Ads — Subject lines que abren

| Tipo | Ejemplo (español) | Efecto |
|---|---|---|
| **Incentivo** | "¿Te invito a un café virtual?" | Curiosidad por la oferta |
| **Provocativo** | "El 90% de las estrategias B2B en LinkedIn son humo" | Atención por atrevimiento |
| **Problem-led** | "¿Harto de leads que nunca contestan al teléfono?" | Identificación con dolor |

Subject lines genéricos ("Te ayudamos con X") = campaña muerta.

### Video en LinkedIn

- Subtítulos **OBLIGATORIOS** — 80%+ ven sin sonido
- Hook en primeros 3 segundos (text overlay con declaración bold)
- Formato: 1:1 o 9:16 > 16:9 en móvil
- Persona hablando a cámara > motion graphics

→ Detalle completo: [references/thought-leader-ads.md](./references/thought-leader-ads.md) · [references/conversation-ads.md](./references/conversation-ads.md)

---

## Fase 4: Estrategia Full-Funnel

### 3 capas + Acceleration

```
Cold (60-70%) → Retargeting (20-30%) → High-Intent RTG (5-10%) → Acceleration (5-10%)
```

### Cold campaigns

| Formato | Propósito | Métrica clave |
|---|---|---|
| Text Ads | Impresiones near-free | Coste ≈ €0 |
| Image Ads | Mostrar distinctive brand assets | CTR >0,7% |
| Thought Leader Ads | Posts orgánicos patrocinados — máx engagement | Engagement >10% |

**NO** poner demos/CTAs directos en cold. Solo ~5% está en mercado. Cold = ser recordado, no vender.

### Retargeting campaigns

Audiencias: web traffic 90d + company page 90d + ad engagement 90d.

| Formato | Propósito | Métrica clave |
|---|---|---|
| Text Ads | Impresiones RTG near-free | Coste ≈ €0 |
| TLAs | Contenido producto, customer stories | Engagement 10-15% |
| Image Ads | USP / beneficio claro | CTR >1% |

### High-Intent RTG

- **Conversation Ads** desde founder/exec, mensaje personal
- Open rate objetivo: 50%+
- Clicked-open: 5% (target 6-7%)
- Solo para personas que ya interactuaron con retargeting

### Modelo "Sushi Conveyor Belt"

NO usar flowcharts secuenciales de retargeting (Ad 1 → Ad 2 → Ad 3). Poner 4 tipos de contenido simultáneamente y dejar que el usuario elija:

1. **Product marketing** — cómo resuelves el problema (UI walkthroughs, demos)
2. **Social proof** — testimonios, case studies, defensores del producto
3. **Thought leadership** — calculadoras, reports, podcasts
4. **Offer/Demo** — capturar cuando estén listos

Cuando alguien clica en temas 1-3 → señal de intento → mover a high-intent RTG con Offer/Demo.

### Exclusion architecture

- RTG excluido de Cold (que gradúen al siguiente nivel)
- Customers excluidos de todo
- Competidores excluidos de todo
- Setup evergreen: siempre activo, no bursts de campaña

---

## Fase 5: Targeting y Audiencias

### Filtros core (lógica AND)

Company size + Industry + Job titles. Mínimo estos tres. Nunca solo un filtro.

### Verificaciones post-lanzamiento

**SIEMPRE** revisar Demographics tab (día 3-5):
- Job titles alcanzados = ¿coinciden con ICP?
- Companies = ¿son las correctas?
- Si hay títulos/empresas irrelevantes → exclusiones inmediatas

### Super titles

LinkedIn agrupa títulos bajo "super titles" genéricos (ej: "Head of Marketing" incluye variantes no obvias). Verificar qué títulos reales se alcanzan en Demographics.

### Matched Audiences

- Subir listas exactas desde Apollo/ZoomInfo/CRM
- Mínimo **300 miembros** matched para que LinkedIn permita targeting
- Añadir filtros de job title/seniority encima de la lista
- Refresh listas cada **90 días** (las personas cambian de trabajo/email)

### Audiencias de retargeting

| Fuente | Lookback | Uso |
|---|---|---|
| Web traffic | 90 días | RTG general |
| Company page visits | 90 días | RTG general |
| Ad engagement | 90 días | RTG general |
| URLs /demo, /pricing, /signup | 30-90 días | High-intent RTG |
| URLs /login, /careers | 30-180 días | **EXCLUSIÓN** (clientes, job seekers) |
| Video views 50%+ | 30-90 días | Mid-funnel offers |
| Video views 75%+ | 30-90 días | Demos/trials |

### Targeting avanzado

- **Skills:** targeting por skills en perfil (ej: "Salesforce" para competidor SaaS)
- **Company revenue:** segmentar por facturación anual
- **Company growth rate:** empresas >20% crecimiento = más probabilidad de invertir
- **Member groups:** filtrar por grupos de LinkedIn = alta intención
- **Device preference: Desktop** → mayor conversión B2B, menor CPL

→ Detalle completo: [references/targeting-framework.md](./references/targeting-framework.md)

---

## Fase 6: Optimización y Cadencia

### Kill rules

| Situación | Acción | Timing |
|---|---|---|
| Campaña underperforming | Matar | 2-3 días |
| Ad con >30 impresiones y 0 clics | Pausar | Inmediato |
| Awareness con >1.000 imp y engagement bajo media | Pausar | Inmediato |
| CPA > target con 0 leads | Pausar | Cuando coste > CPA target |

### Frecuencia

- **Cold:** <7 impresiones/persona/30 días
- **Retargeting:** hasta 15/30 días aceptable
- Si frecuencia muy alta → audiencia demasiado pequeña → expandir o rotar

### Creative refresh cadence

| Formato | Refresh cada |
|---|---|
| Image Ads | 4-6 semanas |
| Carousel Ads | 4-6 semanas |
| Document Ads | 6-8 semanas |
| Video Ads | 8-12 semanas |

### Ad scheduling (dayparting manual)

LinkedIn **NO tiene** dayparting nativo. Presupuestos pequeños 24/7 se agotan a las 12:00.

**Solución:** usar Sammy o automatización para pausar/activar por horas UTC (Lun-Vie 8:00-20:00 UTC). Reducir de 24h a 8h = **200% más poder de compra por hora**.

### Audience penetration targets

- **Cold:** 20-50% del target audience alcanzado
- **Retargeting:** lo más alto posible (grupo pequeño, alta frecuencia)

→ Detalle completo: [references/bidding-optimization.md](./references/bidding-optimization.md)

---

## Fase 7: Escalado

### Escalado vertical

Segmentación por job function o seniority cuando el presupuesto se concentra en ~20-30% de la audiencia.

### Escalado horizontal

Añadir formatos: Text Ads → Image Ads → TLAs → Video → Document → Carousel → Conversation Ads.

### ABM Pilot (top 30-50 cuentas)

1. Seleccionar 30-50 accounts que justifican la inversión si solo 1 cierra
2. 1 campaña por empresa, $25/día por cuenta, bids CPM ultra-bajos
3. Coste real: ~€6/mes por empresa (audiencia tiny = pocas impresiones necesarias)
4. Creativos con logo/nombre de la empresa target
5. Sales debe hacer outreach simultáneo a las mismas cuentas

### Acceleration campaigns

Ads contra **oportunidades abiertas** en CRM:
- Automatización: Zapier trigger cuando deal stage = "qualified to buy" → push empresa a audiencia LinkedIn
- 2 pilares: social proof (testimonios) + objeciones (precio, experiencia)
- Presupuesto mínimo (audiencia = pipeline abierto = tiny)
- ROI más alto disponible en LinkedIn

### Incrementality testing

Split 1.000 target accounts: 500 Exposed (reciben ads) + 500 Hold-out (sin ads). Medir: email open rates, response rates, connect rates, meetings booked, pipeline, deals cerrados.

### Reglas de escalado de presupuesto

- Incrementos graduales, nunca saltos de 10x
- Nunca bajar de €50/día por campaña
- Path de €3K a €50K: consolidar → validar → expandir formatos → ABM → acceleration

→ Detalle completo: [references/abm-strategy.md](./references/abm-strategy.md)

---

## Fase 8: Tracking y Atribución

### Stack de tracking

| Capa | Qué hace | Recuperación |
|---|---|---|
| **Insight Tag** | Pixel JS en todas las páginas | Baseline — pierde 10-30% |
| **CAPI** | Server-side complementario | Recupera 10-30% conversiones |
| **Offline Conversion Import** | CRM → LinkedIn (MQL, SQL, Opp, Won) | Señal de optimización downstream |
| **Revenue Attribution Report** | CRM sync nativo (SF, HubSpot, D365) | Pipeline y revenue atribuidos |

### Insight Tag — Setup

1. Campaign Manager → Account Assets → Insight Tag
2. Instalar vía **GTM** (recomendado) o hardcoded en `<head>`
3. Instalar en **TODAS** las páginas, no solo landing pages
4. Verificar con LinkedIn Tag Helper (extensión Chrome)

### CAPI — Siempre junto al Insight Tag

- Recupera 10-30% conversiones perdidas (ad blockers, cookies, iOS)
- Setup: partner integration (HubSpot/SF), Zapier/Make, o API directa
- **Deduplicación:** capturar cookie `li_fat_id` en formulario → pasar vía CAPI

### Offline Conversion Import

| Evento CRM | Uso |
|---|---|
| **MQL** | Señal mid-funnel — "encuentra más como los que califican" |
| **SQL** | Señal alta — fuerte para bidding |
| **Opportunity** | Optimización por pipeline |
| **Closed-Won** | Señal definitiva (necesita >15 eventos/mes) |

Regla: importar el evento más downstream con volumen suficiente (>15/mes).

### Atribución — 4 fuentes combinadas

1. **LinkedIn native** — Insight Tag + CAPI
2. **Revenue Attribution Report** — sync CRM
3. **Cross-correlation manual** — comparar conversiones web con LinkedIn Companies tab
4. **Self-reported** — "¿Cómo nos conociste?" como campo **libre** (no dropdown)

### LinkedIn como pipeline influencer

LinkedIn = influenciador de pipeline, NO canal last-click. Solo 0,04% clica en ads. El 99%+ de la audiencia es invisible si mides solo clics. Medir: branded search growth, pipeline influence, self-reported attribution.

### GDPR + LOPD España

- Privacy policy URL **obligatoria** en cada Lead Gen Form
- Consent checkbox **obligatorio** en LGF para España
- Datos LGF se borran automáticamente a **90 días** — sincronizar con CRM antes
- LOPD refuerza GDPR con requisitos adicionales españoles

→ Detalle completo: [references/tracking-spain.md](./references/tracking-spain.md) · [references/attribution-model.md](./references/attribution-model.md)

---

## Fase 9: Auditoría de Cuentas

### Orden de auditoría (top-down)

1. **Tracking** — ¿Insight Tag activo? ¿CAPI configurado? ¿OCI funcionando?
2. **Settings** — location, LAN, audience expansion, CTV, bidding
3. **Estructura** — campaign groups por funnel stage, naming conventions
4. **Audiencias** — filtros AND, exclusiones, tamaño 20K-50K, demographics check
5. **Creativos** — formatos variados, TLAs activos, refresh reciente
6. **Landing pages** — alineación con ad, velocidad, CRO, formulario, WhatsApp

### Red flags inmediatos

- [ ] Audience Network (LAN) activado
- [ ] Audience expansion activado
- [ ] Location targeting "Recent or permanent" (defecto de LinkedIn)
- [ ] Sin exclusiones configuradas
- [ ] Maximum Delivery como estrategia de puja
- [ ] Sin UTM parameters
- [ ] Sin Insight Tag o CAPI
- [ ] Lead Gen Forms sin sync CRM (datos se pierden a 90 días)
- [ ] Un solo formato de anuncio activo

→ Detalle completo: [references/audit-checklist.md](./references/audit-checklist.md)

---

## Fase 10: ABM y Estrategia Avanzada

### Five Stages Model (en lugar de TOFU/MOFU/BOFU)

| Stage | Objetivo | Contenido |
|---|---|---|
| **Create** | Brand affinity pre-market | Thought leadership, publicaciones tercer-party |
| **Capture** | Convertir compradores in-market | Testimonios, case studies, demos |
| **Accelerate** | Cerrar deals abiertos | Multi-thread targeting (ops/finance/HR) |
| **Revive** | Recuperar deals estancados/perdidos | Nuevas ofertas, social proof actualizado |
| **Expand** | Más revenue de clientes existentes | Upsell, referral, expansión |

### Account prioritization

Dos factores:
- **Fit:** demographic/firmographic + technographic (qué CRM, tech stack usan)
- **Signal:** triggers de intención directos (ex-cliente en target account, cluster de usuarios en free plan)

### Ad engagement como intent data

1. Lanzar ads LinkedIn a ICP
2. Trackear qué empresas engagean (no solo 1 clic, sino múltiples engagements)
3. Crear lista CRM: empresas con **100+ impresiones** y **5+ engagements** en **30 días**
4. Enviar lista a sales (workflow automático o alerta Slack)
5. Sales hace outreach en LinkedIn — prospects ya no son fríos

### Sales alignment

Zero peleas sobre atribución "marketing vs sales". Todos los touchpoints suman. Ads de marketing mejoran open rates de outbound frío.

→ Detalle completo: [references/abm-strategy.md](./references/abm-strategy.md)

---

## Casos de Éxito

- [B2B SaaS 0→200+ Customers](./examples/b2b-saas-0-200-customers.md) — $75K en 15 meses → 350+ clientes con TLAs
- [ABM Pipeline Acceleration](./examples/abm-pipeline-acceleration.md) — Ads contra oportunidades abiertas, mejor ROI
- [Incrementality Test España](./examples/incrementality-test-spain.md) — Test 500/500 para probar impacto
- [Engagement to Pipeline](./examples/engagement-to-pipeline.md) — Ad engagement → HubSpot → 3 demos → €10K pipeline/semana

---

## Referencias

| Archivo | Contenido |
|---|---|
| [spain-market-linkedin.md](./references/spain-market-linkedin.md) | Mercado español: IVA, LOPD, estacionalidad, comportamiento |
| [campaign-setup-checklist.md](./references/campaign-setup-checklist.md) | Setup paso a paso España |
| [ad-formats-guide.md](./references/ad-formats-guide.md) | Todos los formatos con specs y benchmarks |
| [targeting-framework.md](./references/targeting-framework.md) | Targeting completo: filtros, exclusiones, matched audiences |
| [thought-leader-ads.md](./references/thought-leader-ads.md) | TLA deep dive: selección, bridging, scaling |
| [conversation-ads.md](./references/conversation-ads.md) | Conversation Ads: subject lines, cascada, objeciones |
| [bidding-optimization.md](./references/bidding-optimization.md) | Pujas, kill rules, dayparting, frecuencia |
| [tracking-spain.md](./references/tracking-spain.md) | Insight Tag, CAPI, OCI, GDPR/LOPD |
| [audit-checklist.md](./references/audit-checklist.md) | Auditoría cuentas LinkedIn españolas |
| [abm-strategy.md](./references/abm-strategy.md) | ABM: Five Stages, piloto 1:1, acceleration |
| [attribution-model.md](./references/attribution-model.md) | Atribución B2B: 4 fuentes, any-touch, incrementality |
| [diagnostics.md](./references/diagnostics.md) | Troubleshooting: delivery, review, matching, compliance |
