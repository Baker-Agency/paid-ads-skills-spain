---
name: google-ads-spain
description: Google Ads campaign management for the Spanish market (Spain). Setup, optimize, scale, and audit Google Ads campaigns for lead gen, SaaS, and services targeting Spain. Use when managing Google Ads for Spanish clients, launching campaigns in Spain, auditing Spanish Google Ads accounts, optimizing pujas, creating anuncios, managing palabras clave negativas, or adapting Google Ads strategy for the Spanish/European market. Covers Search, PMax, Demand Gen, YouTube ads, Smart Bidding, Quality Score, conversion tracking, and automation scripts for Spain.
---

# Google Ads España — Skill de Gestión Completa

Gestión integral de Google Ads para lead gen, SaaS y servicios en el mercado español. NO e-commerce.

**Todo el contenido está adaptado al mercado español:** benchmarks en EUR, IVA 21%, LOPD/GDPR, estacionalidad española, copy en español.

## Quick Reference — España

| Métrica | Valor España |
|---|---|
| Presupuesto mínimo recomendado | €2.000-3.000/mes (Enrique del Valle) |
| ROAS Europa (primera compra) | 3-5x (convergiendo hacia niveles US) |
| CPL clínicas estéticas | €2-4 |
| IVA | 21% (incluir en cálculos de unit economics) |
| Pérdida tracking estándar | 10-30% conversiones |
| Consent mode España | Tasa alta de rechazo de cookies (GDPR + LOPD) |
| Smart Bidding mínimo técnico | 15 conversiones/30 días |
| Smart Bidding práctico | 30 conversiones/30 días |
| Smart Bidding estadístico | 50+ conversiones/30 días |
| Quality Score 1 vs 10 | QS 1 paga hasta 10x más que QS 10 |

---

## Fase 0: Evaluación de Viabilidad

### Test "Rule of Two" (adaptado a EUR)

**Tasa de conversión × Valor medio del pedido ≥ €2** (= revenue por sesión)

| Escenario | CR | AOV | Revenue/sesión | ¿Viable? |
|---|---|---|---|---|
| Bueno | 2% | €100 | €2,00 | Sí |
| AOV bajo | 2% | €20 | €0,40 | No |
| CR bajo | 0,01% | €1.000 | €0,10 | No |

Si revenue/sesión < CPC → invertir primero en orgánico.

### Framework CAC para servicios (EUR)

1. **CPC × 100** = gasto por 100 clics
2. **Aplicar tasa de conversión** = leads de esos 100 clics
3. **Aplicar tasa de cierre** (lead → cliente) = clientes reales
4. **Gasto ÷ clientes** = CAC

**Ejemplo (clínica dental, España):**

| Paso | Métrica | Valor |
|---|---|---|
| 1 | CPC × 100 | €3 × 100 = **€300** |
| 2 | CVR 5% | 5 leads |
| 3 | Tasa cierre 40% | 2 clientes |
| 4 | €300 ÷ 2 | **CAC = €150** |

Incluir fee de gestión: €300 ads + €200 gestión = €500 ÷ 2 = **€250 CAC real**.

→ Detalle completo: [references/unit-economics-spain.md](./references/unit-economics-spain.md)

### Framework "Winnable Fight"

Usa Google Keyword Planner con tu dominio. Calcula si el coste tiene sentido:

1. Buscar volumen mensual (1.000-10.000 = zona óptima)
2. CPC estimado: **Top of page bid (high range) + 20%**
3. Calcular presupuesto: worst/moderate/best case con 3 tasas de conversión

---

## Fase 1: Setup de Cuenta y Lanzamiento

### Arquitectura de cuenta (2026)

- **Minimalismo estructural:** empieza con 1 campaña y 1 grupo de anuncios. Solo añadir campañas cuando hay razón válida (presupuesto, ubicación, audiencias distintas)
- **SKAGs están muertos.** Agrupar por tema de intención, no por keyword individual
- **Inserción dinámica de keywords** en headlines de match exacto

### Checklist de settings para España

- [ ] Objetivo: "Leads" (o sin objetivo si B2B)
- [ ] Red de Display: **DESACTIVAR**
- [ ] Search Partners: **DESACTIVAR** al inicio
- [ ] Ubicación: **"Presencia"** solamente, NO "Presencia o interés"
- [ ] Idioma: Español (una campaña por idioma)
- [ ] Moneda: EUR
- [ ] Programación horaria: Lun-Vie 9:00-21:00 CET (ajustar según sector)
- [ ] Duración mínima llamada: 30-60 segundos
- [ ] Conteo conversiones: **"Una"** (no "Todas")
- [ ] Auto-apply recommendations: **DESACTIVAR**
- [ ] Audiencias: añadir 20-30 segmentos en modo **"Observación"**
- [ ] Assets automáticos / AI guidance: **DESACTIVAR** al inicio

### 3 listas de keywords negativas (día 1)

Crear ANTES de activar campañas:

1. **Términos basura (español):** gratis, curso, empleo, salario, sueldo, becas, prácticas, wikipedia, youtube, reddit, pdf, qué es, cómo hacer, tutorial, plantilla, ejemplo
2. **Competidores:** nombres de marca competidora (evitar canibalización)
3. **Marca propia:** nombre de tu marca (aislar en campaña de marca separada)

→ Lista completa: [references/negative-keywords-spanish.md](./references/negative-keywords-spanish.md)

### Match types por presupuesto

| Presupuesto | Match type recomendado |
|---|---|
| <€1.000/mes | Exacto solamente |
| €1.000-5.000/mes | Exacto + frase |
| €5.000-10.000/mes | Exacto + broad (con datos) |
| >€10.000/mes | Broad predominante (con 50+ conversiones) |

→ Detalle completo: [references/campaign-setup-checklist.md](./references/campaign-setup-checklist.md)

---

## Fase 2: Progresión de Pujas

### Secuencia de estrategia de pujas

```
Maximize Clicks → Maximize Conversions → Target CPA → Target ROAS
    (0-15 conv)      (15-30 conv)         (30+ conv)     (50+ conv)
```

**Reglas clave:**

- **Cuenta nueva:** Maximize Clicks (sin bid cap). Obtener datos
- **15+ conversiones/30 días:** cambiar a Maximize Conversions (incluso con zero data es mejor que Manual para alimentar señales)
- **30+ conversiones/30 días:** Target CPA con método "escalera"
  1. Revisar CPA actual últimos 30 días
  2. Fijar tCPA **ligeramente SUPERIOR** al actual (si actual = €50, fijar €55)
  3. Esperar 1 semana
  4. Bajar gradualmente hacia objetivo real
- **Campaña de marca:** Manual CPC o Target Impression Share (NO Smart Bidding)

### La regla de presupuesto para 30 conversiones

Smart Bidding necesita 30 conversiones/30 días. Calcula:

- CVR esperado 3% → necesitas ~1.000 clics/mes
- Si CPC medio = €3 → presupuesto mínimo = €3.000/mes (€100/día)
- Si no llegas a 30 conversiones: **consolidar campañas**

### Learning period: lo que realmente importa

- Status "Aprendizaje" en UI = **5 días exactos** (cosmético, no refleja realidad)
- Lo que importa: **volumen de conversiones + conversion lag**, no tiempo
- Copiar/mover assets entre grupos de anuncios **NO resetea** aprendizaje (semántico, no sintáctico)
- Cambiar estrategia de puja o acción de conversión **SÍ resetea**

→ Detalle completo: [references/bidding-progression.md](./references/bidding-progression.md)

---

## Fase 3: Copy y Creativos (Mercado Español)

### Framework RSA

| Posición | Contenido | Pin |
|---|---|---|
| Headline 1 | Intención exacta del usuario | Pin 1 |
| Headline 2 | Diferenciación vs competencia | Pin 2 |
| Headline 3 | CTA claro | Pin 3 |

**Ignorar "Ad Strength"** — no tiene correlación con Ad Rank ni rendimiento real.

### Tú vs Usted en anuncios españoles

| Sector | Tratamiento | Ejemplo |
|---|---|---|
| Servicios locales | Tú | "Pide tu presupuesto gratis" |
| Fitness, coaching | Tú | "Transforma tu cuerpo en 90 días" |
| Legal, financiero (formal) | Usted | "Solicite su consulta gratuita" |
| Médico/estético (web) | Tú | "Descubre nuestros tratamientos" |
| B2B / enterprise | Usted | "Agende una demo personalizada" |
| Seguros, banca | Usted | "Compare nuestras ofertas" |

### Estructura PAS en español

1. **Problema:** "¿Cansado de [dolor específico]?"
2. **Agitación:** "Cada día que pasa, [consecuencia]..."
3. **Solución:** "[Tu servicio] te ayuda a [resultado] en [plazo]"

→ Detalle completo: [references/spanish-ad-copy.md](./references/spanish-ad-copy.md)

---

## Fase 4: Cadencia de Optimización

### Primeros 7 días: SOLO monitorizar

| Día | Acción |
|---|---|
| 1-2 | ¿Tracking activo? ¿Anuncios aprobados? ¿Se gasta presupuesto? ¿Min 10 clics/día? |
| 3-7 | Search terms diario → añadir negativas (ÚNICA optimización permitida). CTR check tras 50-100 clics |

**NO tocar pujas, presupuestos ni estructura la primera semana.**

### Cadencia post-lanzamiento

| Frecuencia | Acción |
|---|---|
| **Diaria** | Check anomalías (¿campañas activas? ¿desaprobaciones? ¿gasto normal?) — NO optimizar |
| **Semanal** | Search terms (top 5-10 por gasto), pacing check, métricas competitivas |
| **Mensual** | N-gram analysis, auditoría Quality Score, reasignación presupuesto entre campañas |
| **Trimestral** | Revisión geo targeting, auditoría horarios, refresh listas negativas, revisión CC.AA. |

### Cuándo preocuparse

- **1 día malo:** ruido normal. No tocar
- **3 días consecutivos malos:** investigar (tracking roto, anuncios rechazados, merchant desconectado)
- **1-2 semanas de caída:** optimizar con datos reales

### Jerarquía de optimización (en orden)

1. **Gasto/Segmentación** — mover presupuesto a campañas ganadoras (MÁS FÁCIL)
2. **Targeting** — keywords, ubicaciones, audiencias, demografía
3. **Anuncios/Landing pages** — mejorar triggers emocionales, USPs
4. **Pujas** — ajustar solo con volumen base conseguido (ÚLTIMO RECURSO)

→ Detalle completo: [references/optimization-cadence.md](./references/optimization-cadence.md)

---

## Fase 5: Escalado

### Escalado vertical (segmentación)

Cuando el presupuesto se concentra en el 20-30% de keywords/productos:

1. Exportar search terms → n-gram analysis (Gemini o 8020 Agent)
2. Identificar keywords "sidekick" que convierten pero no reciben gasto
3. Mover a campañas dedicadas para forzar entrega de presupuesto

### Escalado horizontal (expansión)

Cuando Search Impression Share > 60%:

1. Expandir a temas de keywords de resolución de problemas
2. Añadir YouTube / Demand Gen / GDN
3. PMax con OCI como capa adicional

### Secuencia de escalado recomendada

```
Search → RLSA/DSA → PMax (con OCI) → Demand Gen → YouTube CPM/CPV
```

### Presupuesto para diversificación

- **5-10% del gasto total** como presupuesto de testing para video/nuevos canales
- Prerequisito: ya rentable en search
- B2B: <5% funciona (caso: €500/mes en video → mejoras CPL en search)

→ Detalle completo: [references/scaling-framework.md](./references/scaling-framework.md)

---

## Fase 6: Tipos de Campaña Avanzados

### 7 estrategias Search

| Estrategia | Cuándo usar | Intent |
|---|---|---|
| **Non-brand** | Core de la cuenta | Alto |
| **Competidores** | Bajo volumen de búsqueda en tu categoría | Alto |
| **Marca** | Siempre (defensiva) | Máximo |
| **RLSA** | Marcas establecidas con alto tráfico | Medio-Alto |
| **DSA** | Descubrimiento de keywords (avanzado) | Variable |
| **Industria** | Keyword + modificador sectorial | Muy alto |
| **Contenido** | Keywords informacionales baratas | Bajo-Medio |

### PMax para lead gen en España

**Requisitos:**
- 30+ conversiones/30 días
- €5.000-10.000/mes mínimo
- OCI configurado (sin OCI → spam garantizado)
- Tracking completo de conversiones

**NO usar PMax:**
- Sin datos de conversión
- Sin OCI para lead gen
- Presupuesto < €5.000/mes
- Como primera campaña

### Demand Gen

- Presupuesto mínimo: **€100/día o 20× coste por conversión**
- Empezar con Maximize Clicks (prospecting)
- Retargeting: €30-40/día viable con audiencia conocida
- **NUNCA** seleccionar Display Network en Demand Gen
- Compromiso mínimo: **3 meses**

→ Detalle completo: [references/campaign-types.md](./references/campaign-types.md)

---

## Fase 7: Tracking y Atribución

### Tiers de tracking

| Tier | Qué hace | Coste | Recuperación |
|---|---|---|---|
| Básico (GA4/Google Ads tag) | Tracking browser-side | Gratis | Baseline — pierde 10-30% |
| Enhanced conversions | Match usuarios Google logueados | Gratis | Recupera ~5% |
| Google Tag Gateway | JS vía tu CDN → bypass ad blockers | Gratis | Recuperación adicional |
| Server-side (GTM SS) | Tracking desde tu servidor | €50+/mes | Recupera 10-30% (full) |

### GDPR + LOPD en España

- España tiene **tasa alta de rechazo de cookies** → GA4 consent mode pierde más datos que en otros mercados
- LOPD (Ley Orgánica de Protección de Datos) refuerza GDPR con requisitos adicionales
- GA4 **NO cuenta** sesión/usuario si no aceptó cookies en consent mode
- Solución: Enhanced conversions + Google Tag Gateway como mínimo
- Ideal: Server-side tagging para recuperación completa

### Tracking operativo completo

Rastrear **TODOS** los métodos de conversión:
- Formularios web
- Llamadas (+34 XXX XXX XXX — configurar 30-60s mínimo)
- Chat en vivo
- Reservas de calendario
- WhatsApp (muy relevante en España)
- Emails

Cada método no rastreado = 5-20% señales perdidas → Smart Bidding degrada.

→ Detalle completo: [references/tracking-spain.md](./references/tracking-spain.md)

---

## Fase 8: Auditoría de Cuentas

### Orden de auditoría (top-down)

1. **Tracking de conversiones** — ¿está todo rastreando correctamente?
2. **Settings de cuenta** — ubicación, idioma, auto-apply, search partners
3. **Estructura de campañas** — consolidación vs fragmentación
4. **Grupos de anuncios** — temas coherentes, keywords relevantes
5. **Landing pages** — alineación con intención, velocidad, CRO

### Red flags inmediatos

- [ ] Location targeting en "Presencia o interés" (defecto de Google)
- [ ] Search Partners activos sin análisis de rendimiento
- [ ] Auto-Apply Recommendations activado
- [ ] Conversiones contando "Todas" en vez de "Una"
- [ ] Sin listas de keywords negativas
- [ ] PMax sin OCI para lead gen
- [ ] Multiple conversiones duplicadas

→ Detalle completo: [references/audit-checklist.md](./references/audit-checklist.md)

---

## Automatización y Scripts

### Scripts Ninja (Enrique del Valle)

| Script | Precio | Función |
|---|---|---|
| Negative keyword | €97 (único) | Negativiza términos irrelevantes cada hora |
| Guardian | Gratis + €19 pro | Alerta cuando caen impresiones/conversiones |
| Smart Bidding + Budget | Próximamente | Ajuste diario de pujas + pacing mensual |
| Display fraud | En desarrollo | Combate tráfico bot en Display |

### AI Agents vs Scripts

- **Scripts** = deterministas. "Si coste > 2× CPA → negativizar"
- **AI Agents** = contextuales. Evalúan si un término es negativa basándose en contexto de negocio
- Agentes detectan negativas antes (por intención, no solo coste)
- Auto-corrección: agente A añade negativas → rendimiento cae → agente B revisa y elimina

→ Detalle completo: [references/automation-scripts.md](./references/automation-scripts.md)

---

## Mercado Español — Particularidades

### Estacionalidad España

| Período | Impacto | Acción |
|---|---|---|
| Enero (rebajas) | Alto volumen compras | Aumentar presupuesto |
| Semana Santa | Variable por sector. Turismo ↑, servicios ↓ | Ajustar por vertical |
| Julio (rebajas verano) | Alto volumen | Aumentar presupuesto |
| Agosto | **Bajón generalizado** — vacaciones masivas | Reducir presupuesto 30-50% |
| Septiembre ("vuelta al cole") | Recuperación fuerte | Preparar campañas antes |
| Black Friday (último viernes nov) | Adopción creciente en España | Preparar desde octubre |
| Navidad (dic) | Pico máximo del año | Máximo presupuesto |

### Festivos nacionales

1 enero, 6 enero (Reyes), Viernes Santo, 1 mayo, 15 agosto, 12 octubre (Fiesta Nacional), 1 noviembre, 6 diciembre (Constitución), 8 diciembre (Inmaculada), 25 diciembre

**Importante:** cada comunidad autónoma tiene 2-3 festivos adicionales propios. Ajustar targeting y presupuestos por CC.AA.

### Comportamiento del consumidor español

- **WhatsApp > Email** para comunicación comercial. Integrar WhatsApp en flujo de leads
- **Bizum** creciendo como método de pago — relevante para servicios locales
- **Sensibilidad al precio** alta — ofertas de entrada funcionan muy bien (€50-120 para servicios)
- **Financiación** muy aceptada — 40-60% de pagos en clínicas financiados
- **Horario comercial:** 9:00-14:00 + 16:00-21:00 (considerar para programación anuncios)
- **3ª semana del mes = más débil** (antes de cobrar nómina, patrón universal pero marcado en España)

### Targeting regional (Comunidades Autónomas)

- Campañas separadas por CC.AA. solo si presupuesto lo permite
- Radio local: 10km para servicios locales (caso Huelva)
- Vocabulario regional: evitar regionalismos excesivos en copy nacional
- Madrid y Barcelona concentran ~40% del mercado publicitario

→ Detalle completo: [references/spain-market-guide.md](./references/spain-market-guide.md)

---

## Diagnóstico y Troubleshooting

### Zero conversiones (orden de diagnóstico)

1. **Tracking roto** — verificar que el tracking dispara correctamente (causa más común)
2. **Tráfico equivocado** — revisar search terms. CTR absurdamente alto en non-brand = Search Partners spam
3. **Ruta de conversión incorrecta** — solo revisar LP/oferta si pasos 1 y 2 están perfectos

### CPA alto — 6 factores

| Factor | Diagnóstico |
|---|---|
| CPC subió | Competencia, Quality Score, estacionalidad |
| CVR bajó | LP rota, oferta débil, tracking parcial |
| Tráfico irrelevante | Broad match drift, negativas insuficientes |
| Search Partners | Tráfico spam barato con zero conversiones |
| Learning period | Menos de 7 días desde cambio — esperar |
| Conversion lag | Datos no completos aún — revisar ventana adecuada |

### Cadena de reacción de tracking roto

```
Tags rotos → Datos conversión a la mitad → Smart Bidding optimiza señal parcial
→ Pujas cambian en keywords incorrectas → Tráfico peor → Conversiones reales caen
→ Espiral descendente
```

**Fix:** auditar todos los métodos de conversión regularmente.

→ Detalle completo: [references/diagnostics.md](./references/diagnostics.md)

---

## Quality Score

- QS 1 paga hasta **10x más** que QS 10
- Techo realista: QS 7-8 para non-brand (solo QS 10 en brand)
- **Priorizar** arreglar QS 1-3 (mayor ROI de mejora)
- 3 componentes: CTR esperado, relevancia del anuncio, experiencia LP
- Scripts de negativas mejoran QS eliminando impresiones con CTR bajo
- Mejora QS = **20-30% ahorro en CPC**

→ Detalle completo: [references/quality-score.md](./references/quality-score.md)

---

## Casos de Éxito España

- [Clínica estética Madrid](./examples/clinica-estetica-madrid.md) — €15K+/mes revenue extra, CPL €2-4
- [Clínica Huelva 8.5x ROAS](./examples/clinica-huelva-8.5x-roas.md) — €2.105 gasto → €17K revenue
- [Framework B2B SaaS](./examples/b2b-saas-search-framework.md) — 4 capas de priorización
- [Servicio local España](./examples/servicio-local-spain.md) — De 0 a 30 conversiones/mes

---

## Referencias

| Archivo | Contenido |
|---|---|
| [unit-economics-spain.md](./references/unit-economics-spain.md) | Rule of Two EUR, CAC, IVA 21% |
| [campaign-setup-checklist.md](./references/campaign-setup-checklist.md) | Setup paso a paso España |
| [negative-keywords-spanish.md](./references/negative-keywords-spanish.md) | Listas negativas en español |
| [bidding-progression.md](./references/bidding-progression.md) | Progresión pujas completa |
| [spanish-ad-copy.md](./references/spanish-ad-copy.md) | Copy en español, tú vs usted |
| [optimization-cadence.md](./references/optimization-cadence.md) | Cadencia optimización |
| [scaling-framework.md](./references/scaling-framework.md) | Escalado vertical/horizontal |
| [campaign-types.md](./references/campaign-types.md) | Search, PMax, Demand Gen, B2B |
| [tracking-spain.md](./references/tracking-spain.md) | Tracking, GDPR/LOPD, consent |
| [audit-checklist.md](./references/audit-checklist.md) | Auditoría cuentas españolas |
| [automation-scripts.md](./references/automation-scripts.md) | Scripts, agentes IA |
| [spain-market-guide.md](./references/spain-market-guide.md) | Guía mercado español |
| [quality-score.md](./references/quality-score.md) | Quality Score deep dive |
| [diagnostics.md](./references/diagnostics.md) | Troubleshooting completo |
