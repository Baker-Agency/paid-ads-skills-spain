# Modelo de Atribución — LinkedIn Ads B2B

## El Problema

B2B buying journeys = múltiples decision makers, ciclos largos, cross-device, cookie blocking. **Ninguna fuente única da la imagen completa.**

LinkedIn = **pipeline influencer**, no canal last-click. Solo **0,04%** de usuarios clica en ads. El 99%+ de la audiencia es invisible si mides solo clics.

---

## 4 Fuentes Combinadas

### 1. LinkedIn Native Tracking

- Insight Tag + CAPI
- Gratis
- Datos de conversión platform-side
- Limitación: solo captura interacciones directas con ads

### 2. Revenue Attribution Report

- Sync LinkedIn con CRM (Salesforce, HubSpot, D365)
- Muestra qué empresas/individuos que convirtieron también engagearon con ads
- Modelo **any-touch** — cuenta campañas que influenciaron account en cualquier punto
- Un deal puede atribuirse a múltiples campañas (correcto)
- Config: attribution window ajustable, default 90 días

### 3. Cross-Correlation Manual

- Comparar conversiones mensuales web con LinkedIn Companies tab
- Muestra qué empresas convertidoras tuvieron alto ad engagement
- Reportes de Company Engagement: export CSV semanal/mensual para sales

### 4. Self-Reported Attribution

- "¿Cómo nos conociste?" como campo **LIBRE** (no dropdown)
- Captura perceived channel impact, no solo last touch
- **Mejor fuente individual para B2B**
- Caveat: depende de memoria humana
- Siempre cross-reference con datos platform

---

## Any-Touch Attribution Model

Juzgar LinkedIn en **any-touch** — contar todas las conversiones que LinkedIn asistió, no solo last click.

### Setup

- Fire conversion events como **last touch, last campaign** para que una campaña reciba crédito directo
- Otras campañas surfacean la misma conversión como view-through

### Case study

- Cliente veía LinkedIn al **90% de eficiencia** (10% short de breakeven). Quería cortar
- Eliminar LinkedIn causó que otros canales cayeran — LinkedIn estaba educando/calentando prospects
- **Threshold de profitabilidad:** OK correr LinkedIn al **80-90% profitability** si otros canales están **>100%**. Trabajan juntos

---

## 4 Indicadores para Buy-In Ejecutivo

Para conseguir aprobación de liderazgo, combinar 4 indicadores:

1. **Direct signups** — raros desde LinkedIn (awareness channel), pero impresionantes cuando ocurren
2. **"¿Cómo nos conociste?"** — self-reported attribution en forms
3. **Influence pipeline** — cuánto tocan los ads diferentes oportunidades
4. **Customer journeys** — visualización journey mes a mes

Ninguna métrica individual cuenta la historia completa. Las 4 combinadas hacen el caso ante liderazgo.

**Framing clave:** atribución debe explicar momentum, no ganar una guerra de crédito. Trackear para asegurar dirección correcta — no para tomar crédito.

---

## Branded Search como Métrica de Éxito

Trackear crecimiento de branded search en **Google Search Console** (o plataforma analytics) mes a mes.

- Fibbler: branded search creció **5x en 12 meses**
- Si branded searches no crecen mientras corres LinkedIn ads → messaging no memorable, distinctive brand assets no suficientemente fuertes, o no corriendo consistentemente

---

## Incrementality Testing

### Cuándo usar

Cuando liderazgo es escéptico de LinkedIn ads por problemas de atribución.

### Setup

1. Lista 1.000 target accounts trabajadas activamente por sales
2. Split: 500 **Exposed** (reciben ads) + 500 **Hold-out** (sin ads)
3. Medir durante 3+ meses

### Métricas

- Outbound email open rates
- Sales response rates
- Connect rates
- Meetings booked
- Pipeline creado
- Deals cerrados

### Resultado

Estructura matemática para probar si impressions/awareness realmente impactan el negocio.

---

## Demand Strategy Patience

### GetAccept Case Study

Cambiar a demand strategy causó **30% caída en volumen de leads** inicialmente. Equipo entró en pánico. Se mantuvieron → vieron más demo requests high-intent, más deals, más pipeline, más revenue a lo largo del tiempo.

**Lección:** optimización short-term de conversiones = abandonar demasiado pronto. Resultados de LinkedIn compound over time.

---

## Métricas B2B por Stage

### The Three Tiers

1. **Input Metrics** — actividades que controlas (blogs, eventos, pitch decks, TLAs, ABM accounts)
2. **Indicator Metrics** — señales tempranas (social mentions, event signups, demo watches, inquiries)
3. **Output Metrics** — resultados (pipeline, revenue, NPS, win rate, deal duration)

### CAC Trap en ABM

- Email recibe todo el crédito, social media ninguno
- ABM es colaborativo (offense/defense/midfield)
- **No medir CAC por canal.** Usar true CAC incluyendo labor

### Expectativas alineadas con ciclo venta

- Ciclo 3 meses → esperar mínimo 3 meses para ver impacto en pipeline
- **77% de marketers** incorrectamente intentan probar ROI en 1 mes
- Trackear métricas apropiadas a la etapa del buyer journey
