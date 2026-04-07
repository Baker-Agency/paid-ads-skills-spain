# Tracking y Atribución — Reddit Ads España

## Reddit Pixel — Verificación 5 Pasos

1. **Instalar Reddit Pixel Helper** (Chrome) → navegar al site → green checkmark con pixel ID
2. **Reddit Events Manager** → Test Events → disparar cada evento → verificar aparece <5 min
3. **Browser console** → filtrar "reddit" → confirmar sin errores JS relacionados con `rdt()`
4. **Verificar TODAS las páginas** → homepage, LPs, thank-you, pricing → Pixel Helper "active" en cada una
5. **GTM Debug** (si GTM) → Preview mode → disparar eventos → confirmar tags Reddit disparan en orden correcto

## Eventos de Tracking

| Evento | Cuándo implementar | Impacto si falta |
|---|---|---|
| **PageVisit** | Día 0 (auto con base pixel) | Sin audiencias retargeting, sin datos funnel |
| **ViewContent** | Día 0 — en pricing, features, case studies | No se puede construir audiencias mid-funnel |
| **Lead** | Día 0 — en form submit | No se puede optimizar para leads, sin CPA data |
| **SignUp** | Día 0 — en creación cuenta / trial start | Sin tracking registros |
| **Purchase** | Día 0 — en confirmación pago | Sin datos ROAS |
| **Custom** | 30 días — BookDemo, StartTrial, etc. | Opciones optimización limitadas |

**Mínimo viable:** PageVisit + Lead (o SignUp). Sin estos, NO lanzar.

## CAPI (Server-Side Tracking)

| Check | Bien | Mal | Red Flag |
|---|---|---|---|
| Implementación | Eventos server fluyendo | Sin eventos CAPI | "Activado" pero zero eventos |
| EMQ (Event Match Quality) | >6,0 (bueno), >8,0 (excelente) | 4,0-6,0 (mejorar) | <4,0 — Reddit no puede matchear |
| Deduplicación | Counts pixel vs CAPI ±5% | >10% varianza | 2x eventos (sin dedup ID) |
| Identificadores | ≥2 por evento (email + click_id) | Solo 1 | Zero — eventos no matcheables |
| Latencia | <5 min | 5-30 min delay | >1 hora — fuera ventana atribución |
| Error rate | <1% | 1-5% | >5% — data loss |

## UTM Parameters

| Parámetro | Esperado | Error común |
|---|---|---|
| `utm_source` | `reddit` | `Reddit`, `reddit_ads` (casing inconsistente) |
| `utm_medium` | `paid` o `cpc` | `social`, `paid-social` (no estándar) |
| `utm_campaign` | `{{campaign_name}}` dinámico | Nombre hardcoded (no actualiza al duplicar) |
| `utm_content` | `{{ad_name}}` dinámico | Falta completamente |
| `utm_term` | `{{adgroup_name}}` | Falta completamente |

### rdt_cid Survival Check

- Reddit auto-añade `rdt_cid` (click ID) a URLs destino
- **Verificar:** clic ad → check URL → `rdt_cid` presente
- Si cadena redirects stripea query params → `rdt_cid` se pierde → CAPI matching se rompe
- **Testear con:** redirects, URL shorteners, Unbounce/Instapage — TODOS deben preservar `rdt_cid`

## Ventanas de Atribución

### Configuración Recomendada

| Setting | B2B | B2C | Awareness |
|---|---|---|---|
| Click-through | 28 días (máximo) | 7-14 días | 28 días |
| View-through | 7 días | 1 día | 7 días |

**Por qué 28 días para B2B:** Redditors tienen ciclo consideración largo para view-throughs vs click-throughs. Siempre medir ambos views y clicks para obtener imagen precisa de rendimiento.

### Si Ciclo Venta >28 Días

- Suplementar con offline conversion import para capturar conversiones delayed
- Upload CRM data (CSV o API) dentro de 48h de conversión
- Incluir valor de conversión en upload para datos ROAS

## GDPR + LOPD en España

### Requisitos

- **GDPR:** Regulación europea obligatoria
- **LOPD (Ley Orgánica de Protección de Datos):** Refuerza GDPR con requisitos adicionales
- **AEPD (Agencia Española de Protección de Datos):** Órgano supervisor
- España tiene **tasa alta de rechazo de cookies** (40-60% usuarios)

### Implementación

- [ ] Cookie banner implementado (OneTrust, Cookiebot, etc.)
- [ ] Reddit Pixel dispara SOLO tras consentimiento otorgado
- [ ] Consent Mode v2 configurado
- [ ] CAPI respeta señales consentimiento
- [ ] Privacy policy actualizada mencionando Reddit
- [ ] PII pasado al CAPI siempre hasheado

### Impacto en Tracking

```
Sin consent management → Pixel dispara sin consentimiento → Violación LOPD → Multa AEPD
Con consent management → 40-60% rechazan cookies → Pixel pierde esos datos → Smart optimization degrada
Solución → CAPI server-side → Recupera señal incluso con cookies rechazadas
```

## Integration Matrix

| Sistema | Qué verificar | Bien | Mal |
|---|---|---|---|
| **GA4** | Tráfico Reddit clasificado correctamente | Sesiones match clicks ±15% | >30% discrepancia |
| **Salesforce** | Leads con Reddit UTMs fluyendo | Leads aparecen <24h, UTMs poblados | Sin leads Reddit o UTMs faltantes |
| **HubSpot** | Contact properties capturando Reddit data | UTMs en propiedades, lifecycle tracked | UTMs no capturados |
| **GTM** | Tags Reddit disparando correctamente | Tags disparan en triggers correctos | Tags misfiring, triggers equivocados |
| **Looker/Tableau** | Reddit data fluyendo a dashboards | Refresh diario, métricas match UI ±5% | Datos >48h, discrepancias |

### CRM — Salesforce

| Check | Bien | Mal | Fix |
|---|---|---|---|
| UTM capture en Lead | 5 UTMs + rdt_cid guardados | UTMs faltantes | Añadir hidden form fields |
| Campaign Member mapping | Leads Reddit auto-asociados a Campaign | Sin asociación | Crear automation rule |
| Opportunity attribution | Campaign Influence visible | Sin campaign influence | Habilitar Campaign Influence |
| Offline conversion feedback | Status Won/Lost fluyendo a Reddit <48h | Sin feedback loop | Setup CSV export o CAPI |

### CRM — HubSpot

| Check | Bien | Mal | Fix |
|---|---|---|---|
| UTM capture en Contact | utm_source, utm_medium, utm_campaign | "Direct Traffic" o "(not set)" | Check form embed, habilitar URL param tracking |
| Lifecycle stage | Progresión Subscriber → Lead → MQL → SQL | Todos stuck en "Lead" | Configurar lifecycle automation |
| Deal attribution | Deal muestra Reddit como source | Sin source en Deal | Configurar Deal herencia Contact source |

## Reporting Tools Connectors

| Tool | Connector | Refresh | Limitación |
|---|---|---|---|
| Looker Studio | Supermetrics / Funnel.io | Diario | Sin datos nivel subreddit vía API |
| Tableau | Supermetrics / custom API | Diario / on-demand | Requiere licencia Supermetrics |
| Google Sheets | Supermetrics sidebar / Zapier | Scheduled | Límites filas para cuentas grandes |
| Databox | Native Reddit connector | Diario | Dimensiones breakdown limitadas |
