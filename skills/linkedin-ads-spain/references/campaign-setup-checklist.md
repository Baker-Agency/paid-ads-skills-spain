# Checklist de Setup — LinkedIn Ads España

## Pre-lanzamiento

### Cuenta y accesos

- [ ] Campaign Manager creado con billing en EUR
- [ ] Admin roles definidos (owner, agency = Campaign Manager role)
- [ ] Company Page conectada
- [ ] Creative Manager access si se usan TLAs/Partnership Ads

### Insight Tag

- [ ] Insight Tag instalado vía GTM (recomendado) o hardcoded
- [ ] Instalado en **TODAS** las páginas (no solo landing pages)
- [ ] Verificado con LinkedIn Tag Helper (extensión Chrome) — checkmark verde
- [ ] Verificado en Campaign Manager → Account Assets → Insight Tag → "Active"
- [ ] Si GTM: trigger = All Pages, container publicado

### CAPI (Conversions API)

- [ ] Configurado junto al Insight Tag (belt and suspenders)
- [ ] Método elegido: partner (HubSpot/SF), Zapier/Make, o API directa
- [ ] Deduplicación habilitada (capturar `li_fat_id` cookie)
- [ ] Test event enviado y verificado en Campaign Manager

### Conversiones

- [ ] Conversion events creados para cada acción clave (form submit, demo, signup)
- [ ] Offline conversions configurados (MQL, SQL, Opp, Won) si CRM lo permite
- [ ] Revenue Attribution Report activado si usa Salesforce/HubSpot/D365

---

## Estructura de Campaign Groups

### Arquitectura recomendada

```
[Brand] - Cold Awareness
  └── Campaign: Cold TLA [Audiencia] [Ubicación] [Fecha]
  └── Campaign: Cold Image [Audiencia] [Ubicación] [Fecha]
  └── Campaign: Cold Text Ads [Audiencia] [Ubicación] [Fecha]

[Brand] - Retargeting
  └── Campaign: RTG 90d TLA [Fecha]
  └── Campaign: RTG 90d Image [Fecha]
  └── Campaign: RTG 90d Text [Fecha]

[Brand] - High-Intent RTG
  └── Campaign: HI-RTG Conversation Ads [Fecha]

[Brand] - Acceleration (opcional)
  └── Campaign: Accel Open Pipeline [Fecha]
```

### Naming conventions

- **Campaign Group:** `[Brand] - [Etapa funnel]`
- **Campaign:** `[Estrategia] [Timeframe] [Formato] [Audiencia] [Ubicación] [Fecha]`
- **Ad:** `[Mensaje/Tema] - [Formato] - [Variante]`

Ejemplo: `RTG 90d TLA Producto España Mar2026`

---

## Settings obligatorios

| Setting | Valor | Razón |
|---|---|---|
| Objective | **Website Visits** (Engagement solo para TLAs) | CPC real, no vanity clicks |
| Location | **Permanent** only | Evitar pagar €12/clic por viajeros |
| Audience Network | **OFF** | 60% budget drain a apps fraudulentas |
| Audience Expansion | **OFF** | LinkedIn expande a fuera de ICP |
| Connected TV | **OFF** | Solo para cuentas >€10K/mes con budget de marca separado |
| Bidding | **Manual** | Siempre. Empezar 2/3 del bid sugerido |
| Bid adjustment high-value | **OFF** | LinkedIn overbidea a su criterio |

---

## Audiencias — Setup

### Cold audiences

1. **Filtros core (AND):** Company size + Industry + Job titles
2. **Tamaño target:** 20K-50K para <€10K/mes
3. **Exclusiones día 1:**
   - Competidores (company names)
   - Empleadores anteriores
   - Clientes actuales (sign-ups + customers)
   - Enterprise fuera de ICP
   - Industrias irrelevantes
   - Edades extremas (<24 si no target junior)

### Retargeting audiences

Crear ANTES de lanzar cold (se llenarán progresivamente):

- [ ] Website traffic — 90 días
- [ ] Company page visits — 90 días
- [ ] Ad engagement (todos los cold ads) — 90 días
- [ ] High-intent URLs: `/demo`, `/pricing`, `/signup` — 30-90 días
- [ ] Exclusión URLs: `/login`, `/careers`, `/partners` — 30-180 días

### Matched Audiences (si disponibles)

- [ ] Lista de empresas target subida (mín 300 members matched)
- [ ] Lista de contactos CRM subida (email matching)
- [ ] Job titles/seniority layered on top

---

## UTM Parameters

Configurar a **nivel de cuenta** (no campaign):

```
utm_source=linkedin
utm_medium=paid_social
utm_campaign={{CAMPAIGN_NAME}}
utm_content={{CREATIVE_NAME}}
```

Incluir account ID para inserción dinámica de nombres de campaña.

---

## Presupuesto y distribución

| Etapa | % presupuesto | Min diario/campaña |
|---|---|---|
| Cold | 60-70% | €100 (ideal) |
| Retargeting | 20-30% | €50 |
| High-Intent RTG | 5-10% | €50 |
| Acceleration | 5-10% | €30-50 |

**Para Campaign Groups de RTG con múltiples campañas:** usar presupuesto a nivel Campaign Group para distribución fluida.

---

## Post-lanzamiento

### Día 0 — Verificación inmediata

- [ ] Campañas en status "Active"
- [ ] Ads aprobados (no "Pending Review")
- [ ] Insight Tag disparando (verificar con Tag Helper)
- [ ] Presupuesto gastándose (check a las 2-4 horas)
- [ ] UTM parameters funcionando (check en GA4/CRM)

### Días 1-3

- [ ] Impresiones >0 en todas las campañas activas
- [ ] Si 0 impresiones: verificar bid (subir 10-15%), audience size (>1K)
- [ ] Si impresiones pero 0 clics: verificar creativos y copy

### Días 3-7

- [ ] **Demographics check:** Job titles, companies, industries = ¿ICP correcto?
- [ ] Si títulos/empresas irrelevantes → añadir exclusiones inmediatamente
- [ ] Verificar que retargeting audiences empiezan a crecer
- [ ] **NO optimizar nada más** la primera semana — dejar que acumule datos

### Semana 2+

- [ ] Primeros análisis de rendimiento por ad/formato
- [ ] Kill rule: ads con >30 imp y 0 clics → pausar
- [ ] Verificar audience penetration (20-50% cold)
- [ ] Ajustar bids si delivery insuficiente (+10-15% por día hasta delivery correcta)
