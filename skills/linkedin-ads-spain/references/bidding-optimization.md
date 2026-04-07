# Pujas y Optimización — LinkedIn Ads

## Manual Bidding — SIEMPRE

**Consenso (Adam/Fibbler, Mark/Winbox):** siempre manual, nunca Maximum Delivery (el default).

### Por qué
- Maximum Delivery = CPM-based. En LinkedIn, CPM significativamente más caro que CPC (a diferencia de otras plataformas)
- Manual bidding = menor CPC = más de tu presupuesto
- Maximum Delivery deja que LinkedIn decida cuánto pagar → overspend garantizado

### Configuración

| Setting | Valor |
|---|---|
| Estrategia | **Manual CPC** |
| Bid inicial | **2/3 del bid recomendado** |
| "Enable bid adjustment for high-value clicks" | **OFF** |
| Delivery | **Classic** (nunca Accelerate) |

### Floor-to-ceiling arbitrage test

1. Empezar bid en el **mínimo absoluto** que permite la plataforma
2. Subir incrementalmente **día a día** hasta encontrar balance delivery/coste
3. Resultado: el CPC más bajo posible con delivery suficiente

### Ajuste si delivery insuficiente
- Subir bid **10-15% por día** hasta que delivery mejore
- Si aun así no gasta: verificar tamaño audiencia (>1K mínimo para delivery)

---

## Campaign Kill Rules

| Situación | Acción | Timing |
|---|---|---|
| Campaña underperforming general | **Matar** | 2-3 días. "Nunca he visto una campaña fallar al inicio y luego recuperarse" |
| Ad con >30 impresiones y 0 clics | **Pausar ad** | Inmediato |
| Awareness con >1.000 imp y engagement bajo media | **Pausar** | Inmediato |
| Coste > CPA target con 0 leads | **Pausar** exactamente cuando coste > target | No dejar que llegue a 3x esperando que "se promedia" |

### Thresholds automatizados

Configurar alertas automáticas por retrasos en checks manuales:
- CPA > target → pausa automática
- Engagement < media histórica a >1.000 imp → alerta

---

## Ad Scheduling (Dayparting Manual)

LinkedIn **NO tiene** dayparting nativo. Problema: presupuestos pequeños 24/7 se agotan por la mañana.

### Solución: automatización externa

Usar Sammy o herramienta de automatización para:
- **Pausar** campañas a las 20:00 UTC
- **Activar** campañas a las 8:00 UTC
- Solo Lunes a Viernes

### Impacto

Reducir de 24h a 8h/día = **200% más poder de compra por hora**. Concentrar presupuesto en horas prime B2B.

### LinkedIn vs Meta: pausar es seguro

A diferencia de Meta, pausar/activar campañas en LinkedIn **NO disrumpe** rendimiento agresivamente. Scheduling diario es seguro.

**Alternativa:** en vez de pausa total, reducir presupuesto 90% fuera de horas.

### Determinar mejor schedule vía CRM data

1. **Exportar datos CRM:** report de leads/signups creados por fecha (incluir timestamp/horas)
2. **Limpiar:** eliminar todo PII (emails, nombres, teléfonos)
3. **Analizar con ChatGPT:** "Analiza este dataset de usuarios trial creados. ¿Qué días de la semana y horas del día generamos más signups?"
4. **Implementar:**
   - Lun-Vie spike + Sáb-Dom caída → pausar weekends
   - Spike 9:00-17:00 → schedule solo esas horas
   - Distribución uniforme → cubrir más horas

---

## Frecuencia

LinkedIn **NO ofrece** frequency capping manual (a diferencia de Meta/Google).

### Monitorización

Campaign Manager → Demographics → columna "Avg frequency"

### Benchmarks

| Tipo campaña | Frecuencia saludable |
|---|---|
| Cold | <7 impresiones/persona/30 días |
| Retargeting | Hasta 15/30 días aceptable |

### Si frecuencia muy alta

- Audiencia demasiado pequeña → expandir targeting
- Pausar y rotar campañas
- Workaround: campaign scheduling para controlar velocidad de acumulación

---

## Creative Refresh Cadence

| Formato | Refresh cada | Razón |
|---|---|---|
| Image Ads | 4-6 semanas | Fatigan rápido por repetición visual |
| Carousel Ads | 4-6 semanas | Similar a image ads |
| Document Ads | 6-8 semanas | El contenido provee valor → fatigan más lento |
| Video Ads | 8-12 semanas | Mayor profundidad de contenido → más lento |
| TLAs | 6-8 semanas | Contenido orgánico = más lento |
| Conversation Ads | 8-12 semanas | Formato personal, inbox delivery |

---

## Learning Phase

### Qué la triggerea
- Lanzamiento nueva campaña
- Cambio significativo presupuesto (>30%)
- Cambio estrategia de puja
- Cambio de audiencia
- Nuevos ads añadidos

### Duración
- 1-7 días según volumen
- Necesita ~15-50 conversion events para salir (varía por objetivo)

### Qué resetea learning
- Cambios mayores en presupuesto (>30%), bid, audiencia u objetivo

### Durante learning phase
- Performance fluctúa — **NO hacer cambios**. Dejar estabilizar
- Si está stuck: presupuesto demasiado bajo para generar suficientes eventos → subir presupuesto o cambiar a evento de conversión de mayor volumen (ej: page view en vez de form submit)

---

## Audience Penetration

| Tipo | Penetración target |
|---|---|
| **Cold** | 20-50% del target audience |
| **Retargeting** | Lo más alto posible (grupo pequeño, alta frecuencia) |

- Imposible alcanzar 100% — no todos entran a LinkedIn regularmente
- Si penetración cold <10% con presupuesto adecuado → bid demasiado bajo, subir

---

## Jerarquía de Optimización (en orden)

1. **Targeting/Exclusiones** — ¿estamos llegando al ICP correcto?
2. **Creativos** — ¿el mensaje resuena? ¿hay suficientes variaciones?
3. **Oferta/Landing** — ¿la propuesta de valor es clara?
4. **Pujas** — ajustar ÚLTIMO, solo cuando lo anterior está resuelto

---

## Presupuesto R&D

- **5-10%** del gasto total como testing para nuevos formatos/audiencias
- Prerequisito: ya rentable en campañas core
- Ej: €500/mes en video → puede mejorar CPL en image ads (efecto halo)
