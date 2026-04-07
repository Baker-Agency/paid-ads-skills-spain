# Diagnóstico y Troubleshooting — Reddit Ads España

## Zero Conversiones (Orden Diagnóstico)

### Paso 1: Tracking (causa más común)

| Check | Cómo | Fix |
|---|---|---|
| ¿Pixel dispara? | Reddit Pixel Helper en cada página | Reinstalar pixel, check `<head>` placement |
| ¿Eventos llegan? | Events Manager → Test Events | Verificar triggers en GTM |
| ¿Errores JS? | Console → filtrar "reddit" | Debug conflictos JS, check CSP headers |
| ¿rdt_cid sobrevive? | Clic ad → check URL final | Fix redirect chain para preservar params |
| ¿Consent blocking? | Incognito → check si pixel dispara | Implementar consent mode correctamente |

### Paso 2: Audiencia

| Check | Señal | Fix |
|---|---|---|
| Subreddits relevantes | ICP realmente presente | Rescore subreddits con Reddit Pro |
| Demographics | Target todos géneros | Ampliar si restringido |
| Exclusiones implementadas | Sin waste en wrong users | Implementar 6 exclusiones obligatorias |
| Automated targeting | OFF si sin baseline | Desactivar hasta tener datos community |
| Audience size | >50K reachable | Ampliar targeting si muy pequeño |

### Paso 3: Oferta / Landing Page

Solo revisar si pasos 1 y 2 están perfectos.

| Check | Benchmark | Fix |
|---|---|---|
| Message match ad→LP | Headline, oferta, CTA consistentes | Alinear LP con promesa del ad |
| Velocidad carga | <3 segundos | PageSpeed optimización |
| Mobile responsive | 100% funcional | Fix layout, tap targets |
| Form fields | 3-5 para TOFU | Reducir campos |
| CTA visible | Above fold | Mover CTA arriba |
| Social proof | Presente above fold | Añadir logos, testimonials, scores |

### Paso 4: Presupuesto / Pujas

| Check | Señal | Fix |
|---|---|---|
| Min €28/día por ad group | Suficiente para delivery | Aumentar o consolidar |
| Cost Cap demasiado bajo | Utilización <50% | Subir cap o cambiar a Lowest Cost |
| Pujas competitivas | Impresiones fluyendo | Subir pujas 15-20% |

## CPA Alto — 6 Factores

| Factor | Diagnóstico | Fix |
|---|---|---|
| **CPC subió** | Mayor competencia subreddits, calidad creativo baja | Expandir a subreddits menos competidos, mejorar creativo |
| **CVR bajó** | LP rota, oferta débil, message mismatch | Fix LP, test nueva oferta, alinear messaging |
| **Tráfico irrelevante** | Subreddits mal seleccionados, keywords amplios | Revisar targeting, añadir negativos |
| **Frequency alta** | Audiencia saturada, pool muy pequeño | Expandir targeting o reducir budget |
| **Learning phase** | <7 días desde cambio | Esperar. No tocar |
| **Conversion lag** | Datos no completos (B2B ciclo largo) | Esperar 28 días, verificar con CRM data |

## Performance Drop Protocol

| Paso | Check | Umbral | Acción |
|---|---|---|---|
| 1. Tracking | ¿Pixel firing? Events Manager último evento | Sin eventos 24h o bajada >50% | Fix pixel/CAPI INMEDIATO |
| 2. Externos | Festivos, noticias, estacionalidad | Agosto España, festivos nacionales | Esperar 3-5 días |
| 3. Policy | ¿Ads rechazados? ¿Account flagged? | >30% ads rejected | Fix violations, contactar Reddit rep |
| 4. Competencia | ¿Nuevos competidores? ¿CPM subiendo? | CPM +25% sin cambios targeting | Nuevos subreddits, mejorar creative |
| 5. Fatiga | ¿CTR declinando en top ads? | CTR -20% en 3 semanas | 3-5 variantes nuevas inmediato |
| 6. Saturación | ¿Frequency subiendo? ¿Reach plano? | >5x/sem (prosp), >8x (RTG) | Expandir targeting, reducir budget |
| 7. Bid landscape | ¿CPC subió y impresiones bajaron? | CPC +30%, impr -20% | Probar pujas más altas o targeting diferente |

## Problemas Específicos España

### Agosto

- **No es un "performance drop" — es estacional normal**
- Muchas empresas cierran completa o parcialmente
- Reducir budget 30-50% proactivamente
- No hacer cambios estructurales durante agosto
- Preparar campañas para septiembre (vuelta al cole)

### Alta Tasa Rechazo Cookies (LOPD)

```
Síntoma: Conversiones reportadas << conversiones reales en CRM
Causa: 40-60% usuarios España rechazan cookies → pixel no trackea
Fix: CAPI server-side → recupera señal independiente de cookies
Validación: comparar Reddit reported conversions vs CRM leads con utm_source=reddit
```

### Audiencias Pequeñas

```
Síntoma: Budget utilización <50%, impresiones inconsistentes
Causa: Pool usuarios Reddit en España es pequeño para muchos nichos
Fix:
1. Ampliar a subreddits en inglés con geo España
2. Combinar community + interest + keyword targeting
3. Reducir budget a match audience size
4. Considerar Reddit solo para retargeting (no prospecting)
```

### Idioma Ads

```
Síntoma: CTR bajo en ads en español en subreddits inglés
Causa: Usuarios Reddit España consumen contenido en EN en subreddits internacionales
Fix: Test ads en inglés para subreddits EN, español solo para r/spain, r/es, r/askspain
```

## Cadena de Reacción Tracking Roto

```
Reddit Pixel roto o cookies rechazadas
→ Datos conversión a la mitad
→ Reddit optimization optimiza señal parcial
→ Pujas van a audiencias equivocadas
→ Tráfico peor
→ Conversiones reales caen
→ ESPIRAL DESCENDENTE
```

**Fix:** Auditar tracking regularmente. CAPI + UTMs + CRM = triple verificación.

## Keyword Creep / Drift

| Síntoma | Diagnóstico | Fix |
|---|---|---|
| Keywords targeting atrayendo tráfico irrelevante | Revisar Breakdown → Keywords | Añadir negative keywords |
| Subreddits de baja calidad recibiendo impresiones | Breakdown → Community | Excluir subreddits spam |
| Automated Targeting expandiendo demasiado | Audience Expansion activado | Desactivar, volver a manual |

## Bug Conocido: Audience Estimator

- Se rompe si custom audience exclusión > custom audience target (incluso sin overlap)
- **Workaround:** Ignorar estimator. Lanzar. Monitorizar delivery real
- Reddit conoce el bug. No hay fix disponible

## Checklist Rápido: "¿Por qué no funciona?"

```
1. ¿Pixel dispara? (5 min check)
   → No → FIX INMEDIATO

2. ¿Gasto >50% del budget? (1 min check)
   → No → Ampliar targeting o subir pujas

3. ¿CTR >0,15%? (tras 500+ impresiones)
   → No → Problema creativo. Nuevo hook/ángulo

4. ¿CVR LP >2%? (tras 100+ clics)
   → No → Problema LP. Message match, velocidad, form

5. ¿Leads en CRM con source=reddit? (CRM check)
   → No → UTMs rotos o CRM integration broken

6. ¿Calidad leads OK? (CRM data)
   → No → Targeting equivocado. Revisar subreddits
```
