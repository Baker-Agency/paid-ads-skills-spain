# Tracking LinkedIn Ads — España

## Stack de Tracking Recomendado

| Capa | Función | Coste | Recuperación |
|---|---|---|---|
| **Insight Tag** | Pixel JS browser-side | Gratis | Baseline — pierde 10-30% |
| **CAPI** | Server-side complementario | Gratis-bajo (depende método) | Recupera 10-30% |
| **OCI** | CRM → LinkedIn (MQL/SQL/Won) | Gratis | Señal optimización downstream |
| **Revenue Attribution** | CRM sync nativo | Gratis | Pipeline y revenue atribuidos |

---

## Insight Tag — Instalación

### Métodos

| Método | Pros | Contras | Mejor para |
|---|---|---|---|
| **GTM** | Sin cambios código, version control | Bloqueado por algunos ad blockers | Mayoría de cuentas (recomendado) |
| **Hardcoded** | Funciona si GTM bloqueado | Requiere developer para cambios | Sites sin GTM, audiences tech |
| **Third-party** | Setup 1-click (WordPress, HubSpot) | Control limitado | Sites simples, equipos no-técnicos |

### Setup GTM

1. Campaign Manager → Account Assets → Insight Tag → copiar Partner ID
2. GTM → Tags → New → LinkedIn Insight Tag → pegar Partner ID
3. Trigger: **All Pages**
4. Submit/publish container
5. Verificar

### Setup Hardcoded

1. Campaign Manager → Insight Tag → "I will install the tag myself"
2. Copiar script completo
3. Pegar en `<head>` de **TODAS** las páginas
4. Deploy a producción
5. Verificar

**Crítico:** instalar en TODAS las páginas, no solo landing pages. Full-site coverage habilita:
- Website Demographics reporting
- Retargeting audiences desde cualquier página
- Conversion tracking en thank-you pages
- Datos de audiencia más ricos para optimización

### Verificación

| Método | Cómo | Qué verificar |
|---|---|---|
| **LinkedIn Tag Helper** | Extensión Chrome → visitar web | Checkmark verde = disparando |
| **Campaign Manager** | Account Assets → Insight Tag → "Tag status" | "Active" y "Verified" |
| **Browser console** | DevTools → Network → filtrar "linkedin" o "snap.licdn" | Requests a `snap.licdn.com` |
| **GTM Preview** | GTM → Preview → navegar site | "Tag Fired" en cada página |

### Fallos comunes

| Problema | Causa | Fix |
|---|---|---|
| "Unverified" | Tag instalado pero LinkedIn aún no detecta | Esperar 24-48h. Forzar visitando site logueado en Campaign Manager |
| No dispara (GTM) | Trigger incorrecto. Container no publicado | Verificar trigger = All Pages. Publicar container |
| No dispara (hardcoded) | Script en `<body>` en vez de `<head>`. CSP bloquea | Mover a `<head>`. Añadir `snap.licdn.com` a CSP |
| Tags múltiples | Varios Partner IDs (común tras cambio agencia) | Auditar tags. Eliminar duplicados |

---

## CAPI (Conversions API)

### Cuándo usar

- **Siempre** junto al Insight Tag (belt and suspenders)
- **Crítico para:** cuentas >€5K/mes, audiencias tech (alto uso ad blockers), mercados GDPR
- **NO es reemplazo** del Insight Tag — complementario

### Métodos de setup

| Método | Complejidad | Mejor para |
|---|---|---|
| **Partner (HubSpot, Salesforce)** | Baja | CRM-native, control limitado |
| **Zapier / Make** | Media | Flexible, cualquier form/CRM, sin dev |
| **API directa** | Alta | Control total, eventos custom, requiere developer |

### Setup Zapier/Make

1. Campaign Manager → Account Assets → Conversions API → "Connect via API"
2. Obtener API token + conversion rule IDs
3. En Zapier/Make: trigger = form submission → action = LinkedIn CAPI
4. Enviar: email (SHA-256), first/last name (hashed), company, conversion rule ID, timestamp
5. **Deduplicación:** incluir `li_fat_id` de Insight Tag cookie si disponible
6. Test: ejecutar evento test → verificar en Campaign Manager

### Deduplicación con Insight Tag

- LinkedIn deduplica eventos con user identifiers + timestamp + conversion rule matching
- **Best practice:** enviar eventos por AMBOS canales. LinkedIn maneja dedup automáticamente
- Capturar cookie `li_fat_id` en form submission → pasar vía CAPI para matching más fuerte

### Verificación CAPI

| Check | Dónde | Esperado |
|---|---|---|
| Events received | CM → Account Assets → CAPI → Event log | Events con status "Received" |
| Match rate | Misma ubicación → "Match rate" | >50% = bueno, <30% = problema datos |
| Dedup funciona | Comparar browser-only vs CAPI-only vs total | Total ≠ browser + CAPI (eso significaría no dedup) |
| Attribution | CM → conversion columns | Conversiones +10-30% tras setup CAPI |

---

## Offline Conversion Import (OCI)

### Por qué importa

Sin offline conversions, LinkedIn optimiza para clics o form submissions. Con datos offline, puede aprender qué audiencias y ads generan revenue real — señal de optimización fundamentalmente diferente.

### Métodos

| Método | Mejor para | Latencia |
|---|---|---|
| **CRM native sync** | Salesforce, HubSpot, D365 | ~24h automático |
| **Zapier / Make** | Cualquier CRM, trigger en stage change | 1-5 min |
| **CSV upload** | Backfills, bajo volumen | Manual (batch) |
| **API** | CRM custom, alto volumen | Real-time |

### Eventos a importar

| Evento CRM | Conversion Rule LinkedIn | Uso optimización |
|---|---|---|
| **MQL** | "MQL" | Mid-funnel. "Encuentra más como los que cualifican" |
| **SQL** | "SQL" | High-value. Señal fuerte para bidding |
| **Opportunity** | "Opportunity" | Optimización por pipeline |
| **Closed-Won** | "Closed Won" con valor revenue | Señal definitiva. Necesita >15 eventos/mes |

**Regla:** importar el evento más downstream con volumen suficiente (>15/mes). Para la mayoría, MQL o SQL es el target práctico.

### CSV format

- Columnas requeridas: `email` (o `company_name` + `company_domain`), `conversion_name`, `conversion_time`
- Opcionales: `conversion_value`, `currency`, `first_name`, `last_name`
- Formato tiempo: ISO 8601 (`2026-04-01T14:30:00Z`)
- Processing: 24-48h
- Match rate esperado: 30-60%

---

## GDPR + LOPD España — Tracking

### Lead Gen Forms

- **Privacy policy URL:** obligatoria en cada LGF
- **Consent checkbox:** obligatorio para España (marketing communications)
- **Data retention:** LinkedIn borra datos LGF a **90 días** — descargar o sync CRM antes
- **Legitimate interest vs consent:** LinkedIn provee data pre-filled bajo legitimate interest. Para consent explícito, añadir language de consent

### Derecho de supresión

- CRM workflow debe poder cumplir solicitudes de borrado GDPR
- Documentar proceso de eliminación para auditorías

### Consent mode España

- Tasa alta de rechazo cookies
- CAPI es crucial para recuperar señal perdida por consent denial
- Enhanced conversions como mínimo

---

## Revenue Attribution Report

### Qué es

Report nativo de LinkedIn conectando ad spend con pipeline y revenue del CRM.

### CRMs soportados

- **Salesforce** (nativo)
- **HubSpot** (nativo)
- **Dynamics 365** (nativo)
- Otros: requiere CSV upload manual o Zapier/Make

### Setup

1. Campaign Manager → Account Assets → Connected Data Sources
2. Seleccionar CRM → autorizar → mapear lifecycle stages
3. Mapear stages: cuál = MQL, SQL, Opportunity, Closed-Won
4. Mapear campo revenue/deal value
5. Sync automático ~24h
6. Attribution window: configurable, default 90 días. Ajustar a ciclo de venta
7. Primer report significativo: 30-60 días tras setup

### Cómo leer el report

- Campaign Manager → Reporting → Revenue Attribution
- Columnas: Leads, MQLs, SQLs, Opportunities, Closed-Won, Revenue, ROI
- Modelo: **any-touch** — cuenta campañas que influenciaron account en cualquier punto
- Un deal puede atribuirse a múltiples campañas (correcto — todas contribuyeron)
- Siempre cross-reference con self-reported attribution
