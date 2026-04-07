# Case Study: Incrementality Test para Probar ROI de LinkedIn

**Fuente:** Silvio Perez (AdConversion)
**Contexto:** Liderazgo escéptico sobre LinkedIn Ads por limitaciones de atribución
**Solución:** Test controlado 500/500 para demostrar impacto matemáticamente

---

## El Problema

- LinkedIn ads son canal de awareness/pipeline influencer, no last-click
- Solo 0,04% de usuarios clica en ads
- Last-click attribution da ZERO crédito a LinkedIn
- Liderazgo dice: "LinkedIn no funciona, no vemos conversiones directas"
- **Necesidad:** prueba empírica de que las impresiones realmente impactan el negocio

---

## Setup del Test

### Paso 1: Seleccionar lista

- 1.000 target accounts activamente trabajadas por sales
- Mismo ICP, mismo sales effort, mismo período

### Paso 2: Split aleatorio

| Grupo | Tamaño | Tratamiento |
|---|---|---|
| **Exposed** | 500 accounts | Reciben LinkedIn ads (cold + RTG) |
| **Hold-out** | 500 accounts | NO reciben ningún LinkedIn ad |

### Paso 3: Mantener todo lo demás igual

- Mismo equipo de SDRs trabajando ambos grupos
- Mismos emails, mismas cadencias outbound
- Misma oferta, mismos contenidos
- **Única diferencia:** grupo Exposed ve LinkedIn ads, Hold-out no

### Paso 4: Medir durante 3+ meses

Mínimo 1 ciclo de venta completo. Para la mayoría de B2B España: 3-6 meses.

---

## Métricas a Comparar

| Métrica | Exposed (500) | Hold-out (500) | Delta |
|---|---|---|---|
| **Email open rates** | ↑ esperado | Baseline | Δ% |
| **Email response rates** | ↑ esperado | Baseline | Δ% |
| **LinkedIn connect rates** | ↑ esperado | Baseline | Δ% |
| **Meetings booked** | ↑ esperado | Baseline | Δ% |
| **Pipeline created (€)** | ↑ esperado | Baseline | Δ€ |
| **Deals cerrados** | ↑ esperado | Baseline | Δ deals |
| **Revenue generado (€)** | ↑ esperado | Baseline | Δ€ |
| **Velocidad del ciclo (días)** | ↓ esperado | Baseline | Δ días |

---

## Cómo Presentar Resultados

### A liderazgo

> "Dividimos 1.000 target accounts en dos grupos idénticos. El grupo que vio nuestros LinkedIn ads tuvo [X]% más meetings booked y [Y]% más pipeline que el grupo sin ads. La inversión en LinkedIn fue de €[Z] y generó €[W] adicionales en pipeline."

### Dashboard

| Indicador | Exposed | Hold-out | Incremento |
|---|---|---|---|
| Meetings/account | 0,15 | 0,08 | +87% |
| Pipeline/account | €1.200 | €650 | +85% |
| Close rate | 22% | 15% | +47% |
| LinkedIn spend | €15.000 | €0 | — |
| Revenue incremental | €45.000 | — | 3x ROI |

*Números ilustrativos. Resultados reales varían.*

---

## Requisitos para España

### CRM setup

- Tagear accounts preemptivamente: "LinkedIn Test Exposed Q2 2026" vs "LinkedIn Test Hold-out Q2 2026"
- HubSpot o Salesforce con lifecycle stages definidos
- Tracking de all touchpoints (emails, calls, LinkedIn interactions)

### LinkedIn setup

- Subir lista 500 Exposed como Matched Audience
- Correr campañas cold + RTG normales solo contra este grupo
- Verificar que Hold-out NO recibe impresiones (check Demographics)

### Duración recomendada España

| Ciclo venta típico | Duración test |
|---|---|
| 1-3 meses | 3 meses mínimo |
| 3-6 meses | 6 meses ideal |
| >6 meses | 6-9 meses |

---

## Resultado Esperado

La mayoría de tests muestran que el grupo Exposed supera al Hold-out en:
- Email open/response rates (prospects reconocen la marca)
- Connect rates (no es outreach frío, ya vieron contenido)
- Meetings (más disposición a hablar)
- Pipeline y revenue (efecto compounding)

**Insight clave:** LinkedIn ads están haciendo que OTROS canales funcionen mejor. El valor no está solo en conversiones directas de LinkedIn.
