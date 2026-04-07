# Campaign Setup Checklist — Reddit Ads España

## Pre-Launch

### Cuenta y Billing
- [ ] Cuenta creada en ads.reddit.com
- [ ] Método de pago configurado (tarjeta crédito o facturación para €10K+/mes)
- [ ] Moneda: USD (Reddit no soporta EUR nativo — reportar internamente en EUR)

### Tracking
- [ ] Reddit Pixel instalado en TODAS las páginas (GTM o hardcoded en `<head>`)
- [ ] Reddit Pixel Helper extension instalada → verificar "Pixel Found" en cada página
- [ ] Evento PageVisit: auto con base pixel → verificar en Events Manager
- [ ] Evento Lead/SignUp: disparar en form submit → verificar con test form
- [ ] UTMs configurados: `utm_source=reddit&utm_medium=paid_social&utm_campaign={{campaign_name}}&utm_content={{ad_name}}`
- [ ] CRM recibe test lead con source attribution correcta
- [ ] `rdt_cid` (click ID) sobrevive cadena de redirects → verificar en URL final
- [ ] Consent mode configurado (GDPR/LOPD obligatorio en España)

### Investigación
- [ ] Reddit Pro activado y monitorizando keywords marca + industria
- [ ] 10-20 subreddits candidatos identificados y evaluados (scoring ≥25)
- [ ] Competidores auditados en Reddit Ad Library
- [ ] Gap matrix de subreddits completada

### Exclusiones (6 obligatorias — configurar ANTES del lanzamiento)
- [ ] Lista empleados (emails dominio empresa)
- [ ] Clientes existentes (upload CRM)
- [ ] Pipeline actual (leads en proceso)
- [ ] Empleados competencia (si posible)
- [ ] Geos irrelevantes (bulk upload zip codes si aplica)
- [ ] Subreddits spam/low-intent excluidos

### Creativos
- [ ] 3-5 ads por ad group preparados
- [ ] Mín 1 free-form text ad por grupo (formato nativo Reddit)
- [ ] Score natividad >18/30 en cada ad
- [ ] Landing pages con message match verificado
- [ ] PageSpeed >80 en todas las LPs (<3s load time)

## Settings de Campaña

| Setting | Valor |
|---|---|
| Objetivo | Conversiones (para lead gen) |
| Inventory type | **Standard** |
| Automated Targeting | **DESACTIVAR** (activar solo tras baseline) |
| Attribution window click | **28 días** (máximo) |
| Attribution window view | **1-7 días** (según objetivo) |
| Bid strategy | **Lowest Cost** (inicio) |
| Demografía género | **Todos** (muchos usuarios no declaran) |
| Schedule | Todas las horas inicialmente. B2B test: 18:00-21:00 CET |
| Daily budget mínimo | **€28/ad group** (~$30) |

## Naming Conventions

### Campañas
```
[TIPO] - [FECHA] - [OBJETIVO] - [NOTAS]
```
Ejemplos:
- `PROSP - 2026-04-06 - Conversiones - B2B SaaS`
- `RTG - 2026-04-06 - Conversiones - Site Visitors`
- `TEST - 2026-04-06 - Traffic - Creative Testing`

### Ad Groups
```
[TIPO] - [AUDIENCIA] - [DEVICE] - [FECHA]
```
Ejemplos:
- `PROSP - r/SaaS r/startups r/Entrepreneur - All Devices - 2026-04-06`
- `RTG - Site Visitors 30d - Desktop - 2026-04-06`
- `PROSP - Keywords Intent Alto - All Devices - 2026-04-06`

## Arquitectura por Presupuesto

### €3-5K/mes (Scenario A: Primera vez)

| Campaña | Budget % | Ad Groups |
|---|---|---|
| PROSP - Conversiones | 70% | 2-3 ad groups: cluster subreddits A, cluster B, keywords |
| RTG - Conversiones | 30% | 1-2 ad groups: site visitors desktop, site visitors all |

### €10K+/mes (Scenario B: Escalando)

| Campaña | Budget % | Ad Groups |
|---|---|---|
| PROSP-COLD - Conversiones | 50% | 3-5 ad groups: clusters subreddits + keywords |
| RTG-WARM - Conversiones | 20% | 2-3 ad groups: visitors 7d, visitors 8-30d, ad engagers |
| RTG-BOT - Conversiones | 15% | 1-2 ad groups: guide downloaders, email list |
| TEST - Traffic | 15% | 2-3 ad groups: mirror top prospecting para test |

### High-Ticket (€25K+ deals, €5-10K/mes budget)

3 fases secuenciales con overlap:

| Fase | Semanas | Budget % | Objetivo |
|---|---|---|---|
| AWARE - Traffic | 1-4 | 50% | Thought leadership a subreddits nicho |
| MID - Conversiones | 3-8 | 30% | Retarget Fase 1 engagers con workshop/assessment |
| BOT - Conversiones | 6+ | 20% | Retarget Fase 2 con strategy session |

Split evoluciona: 50/30/20 → 30/30/40 según crecen pools retargeting.

## Post-Launch Calendar

| Día | Acción |
|---|---|
| 1 | Lanzar. Verificar ads aprobados <4h |
| 2-3 | Solo monitorizar. NO tocar nada |
| 4 | Check pacing (utilización >50%) |
| 7 | Primera lectura: CTR y CPC. Kill CTR <0,15% tras 500 impr |
| 14 | Segunda lectura: CVR, CPL. Pausar CPL >3x target |
| 15-17 | Lanzar retargeting si pixel audience >300 usuarios |
| 18-20 | Segundo batch creativos basado en learnings |
| 21 | Primera optimización targeting: ranking subreddits por CPA |
| 30 | Review Month 1 completa. Decisión: continuar/overhaul/pausar |
