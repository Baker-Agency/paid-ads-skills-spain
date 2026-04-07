# Cadencia de Optimización — Reddit Ads España

## Primeros 14 Días (Learning Phase)

| Día | Acción | Criterio Decisión |
|---|---|---|
| 1 | Lanzar Campaign 1 (prospecting). Verificar ads aprobados <4h | Si no aprobados EOD → revisar policy violations |
| 2 | Solo monitorizar: ¿ads entregando? ¿pixel firing? ¿gasto ok? | Si €0 gasto → targeting estrecho o pujas bajas |
| 3 | Solo monitorizar. NO TOCAR NADA | Utilización >30% = ramp normal. <10% = problema |
| 4 | Primer pacing check: ¿utilización >50%? | <50% → ampliar targeting o subir pujas 15-20% |
| 5-6 | Seguir monitorizando. Anotar CTR por ad group y ad | Sin acción — datos insuficientes |
| 7 | **Primera lectura.** CTR y CPC (sin suficientes datos conversión) | Kill claros: >500 impresiones Y CTR <0,15% |
| 8-10 | Más datos. Check ad disapprovals, sentimiento comentarios | Si comments negativos → problema tono creativo |
| 11-13 | Check datos conversión si hay. ¿Leads llegando? Quality check CRM | Si 0 conversiones tras 200+ clics → LP o tracking, no Reddit |
| 14 | **Segunda lectura.** CTR, CPC, CVR, CPL por ad group | Pausar ad groups con CPL >3x target tras 15+ clics a LP |

**Regla fundamental:** NO tocar pujas, presupuestos ni estructura los primeros 7 días.

## Cadencia Ongoing

### Diaria (5 minutos)

- [ ] ¿Todas las campañas activas y entregando?
- [ ] ¿Ads desaprobados o policy flags?
- [ ] ¿Gasto pacing ±20% del target diario?
- [ ] ¿Anomalías? (CPM spike >50%, zero impresiones, CPC duplicado)
- [ ] ¿Pixel firing? (Events Manager → último evento recibido)

**REGLA: NO reaccionar a 1 día malo.** Esperar 3 días consecutivos malos antes de cambiar. Varianza single-day en Reddit es alta por menor volumen subasta vs Meta/Google.

### Semanal (30-60 minutos)

- Revisar métricas 7 días blended: campaña, ad group, ad level
- **Pausar ads:** CTR <0,15% tras 500+ impresiones
- **Pausar ad groups:** CPA >2x target tras 15+ conversiones
- **Aumentar budget:** Ad groups con CPA <0,8x target y >95% utilización → +20%
- Check fatiga creativa: CTR declinando >15% por 3 semanas consecutivas → nuevo creativo
- Revisar rendimiento subreddit: Breakdown → Community. Pausar CPA >2x avg tras 500+ impr
- Pool retargeting: ¿creciendo semana a semana? Si encogiendo → problema prospecting o pixel
- Sentimiento comentarios: si overwhelmingly negativo → ajustar tono creativo

### Mensual

- Full performance report: CPC, CTR, CVR, CPL, CPA — 30 días + MoM
- Creative demand planning: ¿cuántos nuevos ads necesarios?
  - €5-15K gasto → 3-6 nuevos/mes
  - €15-50K gasto → 10-20 nuevos/mes
- Ranking subreddits: kill bottom 20% por CPA, double down top 20%
- Budget reasignación: grade A/B/C/D/F por eficiencia CPA
- Attribution audit: GA4 → CRM → deals cerrados. ¿Reddit genera leads que cierran?
- Competitor check: Ad Library + Reddit Pro
- Plan testing: ¿qué 1-2 nuevos ángulos/formatos/ofertas testear next month?

### Trimestral

- Channel mix evaluation: ¿% Reddit justificado por % pipeline/revenue?
- Full funnel analysis: ¿dónde están los bottlenecks?
- LTV analysis: ¿clientes Reddit valen igual que otros canales?
- Pregunta fiduciaria: "Si gastáramos nuestro propio dinero, ¿seguiríamos invirtiendo en Reddit a este nivel?"

## Diagnóstico Avanzado

### Performance Drop Protocol

| Paso | Check | Umbral | Acción |
|---|---|---|---|
| 1 | ¿Pixel sigue firing? | Sin eventos 24h o bajada >50% | Fix pixel/CAPI inmediatamente |
| 2 | Factores externos | Festivo o evento en últimos 7 días | Esperar 3-5 días normalización |
| 3 | Policy/disapprovals | >30% ads rechazados | Fix violations. Si account-level → contactar Reddit rep |
| 4 | Competencia | CPM subió >25% sin cambios targeting | Expandir a subreddits menos competidos |
| 5 | Fatiga creativa | CTR bajó >20% en 3 semanas en mismo ad | Lanzar 3-5 variantes nuevas |
| 6 | Saturación audiencia | Frequency >5x/semana (prosp) o >8x (RTG) | Expandir targeting o reducir budget |
| 7 | Bid landscape | CPC subió >30% e impresiones bajaron >20% | Probar pujas más altas o targeting diferente |

### Saturación por Tipo Campaña

| Tipo | Frequency sana | Warning | Saturada |
|---|---|---|---|
| Prospecting broad | 1-2x por 7 días | 3-4x | >5x |
| Prospecting nicho | 2-3x por 7 días | 4-5x | >6x |
| RTG site visitors | 3-5x por 7 días | 6-8x | >8x |
| RTG engaged users | 2-4x por 7 días | 5-7x | >7x |

### Budget Efficiency — CPA Marginal

| Budget diario (múltiplo CPA target) | CPA marginal esperado | Veredicto |
|---|---|---|
| 1-3x CPA | 0,8-1,0x target | Learning phase — datos mínimos |
| 3-5x CPA | 1,0-1,2x target | **Sweet spot** para mayoría cuentas |
| 5-10x CPA | 1,2-1,5x target | Buen volumen, ligera inflación |
| 10-15x CPA | 1,5-2,0x target | Diminishing returns zone |
| >15x CPA | 2,0x+ target | Dividir en ad groups paralelos con targeting diferente |

### Rendimiento por Placement

| Placement | CPM típico | CTR típico | Mejor para |
|---|---|---|---|
| Feed (home + popular) | €4,60-9,20 | 0,3-0,8% | Awareness, prospecting, volumen |
| Subreddit feeds | €5,50-11 | 0,4-1,0% | Targeting contextual, mayor relevancia |
| Conversation threads | €3,70-7,40 | 0,2-0,5% | Deep engagement, long-form |
| Search results | €7,40-14 | 0,5-1,2% | Intent-based, similar a Google |
| Desktop right rail | €2,80-5,50 | 0,1-0,3% | Impresiones baratas, retargeting |

### Funnel Drop-off Benchmarks

| Etapa | Benchmark | Warning | Root Cause | Fix |
|---|---|---|---|---|
| Impresión → Click | 0,4-0,8% | <0,20% | Creativo no resuena, audiencia equivocada | Nuevos ángulos, tighten targeting |
| Click → LP Visit | >90% | <80% | Carga lenta, redirect issues | Fix velocidad (<3s), check redirects |
| LP Visit → Form Start | 30-50% | <20% | Contenido above-fold débil | Mejorar headline, social proof |
| Form Start → Complete | 60-80% | <50% | Muchos campos, errores técnicos | Reducir a 3-5 campos TOFU |
| Lead → MQL | 30-50% | <20% | Audiencia equivocada, oferta tire-kickers | Tighten targeting, qualifying Qs |
