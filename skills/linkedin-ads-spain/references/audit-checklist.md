# Checklist de Auditoría — LinkedIn Ads España

## 1. Pre-Auditoría: Discovery

### Preguntas de negocio

| Categoría | Preguntas | Por qué importa |
|---|---|---|
| **Producto/Servicio** | ¿Qué venden? ¿ACV? ¿Ciclo de venta? | Viabilidad presupuesto y paciencia necesaria |
| **ICP** | Company size, industry, job titles, seniority, geo? | Mapea directamente a filtros LinkedIn |
| **Pipeline** | ¿Stages CRM definidos? (MQL, SQL, SAO, Won) | Necesario para OCI y atribución |
| **Unit Economics** | ¿Close rate? ¿Deal size medio? ¿LTV? | "Winnable fight" math |
| **Proceso ventas** | ¿Quién hace follow-up? ¿En cuánto tiempo? | Speed to lead impacta ROI directamente |
| **Otros canales** | ¿Google/Meta/otro paid? ¿Qué funciona? | Oportunidades cross-channel RTG |

### Preguntas LinkedIn-específicas

- ¿Quién tiene Campaign Manager access? ¿Qué niveles?
- ¿Company Page conectada? ¿Quién administra?
- ¿TLAs activos? ¿Desde qué perfiles?
- ¿Insight Tag instalado? ¿CAPI configurado?
- ¿Presupuesto mensual? ¿Cuánto tiempo llevan?
- ¿Qué CRM? ¿Synced a LinkedIn (Revenue Attribution)?
- ¿Sales Navigator? ¿Overlap con targeting ads?
- ¿Campo "¿Cómo nos conociste?" en formularios? (libre, no dropdown)

### Alineación de expectativas

| Cliente dice | Reality check | Acción |
|---|---|---|
| "Queremos leads ya" | Ciclo compra B2B = 192 días, 62+ touchpoints | Expectativa mín 3 meses |
| "Tenemos €2K/mes" | €5K = mínimo para full-funnel. €2K = 1 campaña, solo data | Ser transparente |
| "Queremos 50 leads/mes" | A €12 CPC y 3% CVR = €20K/mes para 50 leads | Hacer las matemáticas |
| "LinkedIn no funciona" | ¿Cuándo? ¿Cómo? ¿Datos? La mayoría de "fracasos" = setup incorrecto | Auditar intento previo |

---

## 2. Auditoría de Cuenta

### 2.1 Access y Permisos

- [ ] Owner claro identificado
- [ ] Agency tiene Campaign Manager role
- [ ] Billing admin identificado
- [ ] Ex-empleados/agencias anteriores eliminados
- [ ] Company Page conectada con admin apropiado

### 2.2 Settings de Cuenta

| Check | Correcto | Incorrecto |
|---|---|---|
| Location targeting | **Permanent** | "Recent or permanent" (default) |
| Audience expansion | **OFF** | ON (LinkedIn expande fuera ICP) |
| Audience Network (LAN) | **OFF** | ON (60% budget drain a apps fraud) |
| Connected TV | **OFF** | ON (solo si >€10K/mes con budget marca) |
| UTM parameters | Configurados a nivel cuenta | Sin UTMs o solo a nivel campaña |

---

## 3. Auditoría de Estructura

### Campaign architecture

- [ ] Campaign groups por etapa funnel (Cold, RTG, HI-RTG, Acceleration)
- [ ] Naming conventions consistentes
- [ ] Presupuesto por campaign group (no fragmentado)
- [ ] Exclusiones entre stages (RTG excluido de Cold)

### Viabilidad presupuesto

| Presupuesto/mes | Máx campañas | ¿Viable full-funnel? |
|---|---|---|
| <€3K | 1 | No. Solo data collection |
| €3-5K | 1-2 | Limitado. 1 cold + 1 RTG |
| €5-10K | 2-3 | Sí. Cold + RTG + HI-RTG |
| >€10K | 3+ | Full-funnel + ABM |

### Distribución presupuesto

| Etapa | % recomendado | Red flag |
|---|---|---|
| Cold | 60-70% | <40% = insuficiente awareness |
| RTG | 20-30% | 0% = no retargeting |
| HI-RTG / Acceleration | 5-10% | — |

---

## 4. Auditoría de Audiencias

### Targeting

- [ ] Filtros AND (no OR) entre company size + industry + job titles
- [ ] Tamaño audiencia 20K-50K para <€10K/mes
- [ ] Demographics verificados post-lanzamiento
- [ ] Exclusiones configuradas (competidores, customers, irrelevantes)
- [ ] Location = "Permanent" only

### Matched Audiences

- [ ] Listas subidas y match rate >30%
- [ ] Mínimo 300 members matched
- [ ] Refresh <90 días (listas no stale)
- [ ] Job titles/seniority layered on top

### Retargeting

- [ ] Mínimo 3 fuentes activas (web traffic, company page, ad engagement)
- [ ] Lookback windows configurados (90d standard)
- [ ] High-intent URLs separados (/demo, /pricing)
- [ ] Exclusion URLs activos (/login, /careers)

---

## 5. Auditoría de Creativos

### Formatos activos

- [ ] Más de 1 formato en uso (no solo image ads)
- [ ] TLAs activos con organic testing previo
- [ ] Text Ads como capa de impresiones gratuita
- [ ] Creative refresh <6 semanas para image ads

### Calidad

- [ ] Distinctive brand assets consistentes en todos los ads
- [ ] Copy emotion-first (no feature-first)
- [ ] Variaciones suficientes (mín 20 variaciones en image ads)
- [ ] Video con subtítulos si aplica
- [ ] CTAs claros y apropiados por etapa funnel

### Bidding

| Check | Correcto | Red flag |
|---|---|---|
| Estrategia | Manual CPC | Maximum Delivery |
| Bid inicial | ~2/3 del recomendado | Bid máximo automático |
| High-value clicks | OFF | ON |

---

## 6. Auditoría de Tracking y Atribución

### Tracking

- [ ] Insight Tag activo en TODAS las páginas
- [ ] CAPI configurado (complementario a Insight Tag)
- [ ] Conversion events creados para acciones clave
- [ ] Deduplicación habilitada (li_fat_id)

### Offline Conversions

- [ ] OCI configurado (MQL, SQL, Opp, Won)
- [ ] Revenue Attribution Report activo (si CRM compatible)
- [ ] Volumen suficiente para optimización (>15 eventos/mes)

### Self-reported attribution

- [ ] Campo "¿Cómo nos conociste?" en formularios
- [ ] Formato libre (no dropdown)

---

## 7. Red Flags Inmediatos

Lista de problemas que **NUNCA** deberían existir:

- [ ] Audience Network (LAN) activado
- [ ] Audience expansion activado
- [ ] Location "Recent or permanent" (defecto LinkedIn)
- [ ] Sin exclusiones configuradas
- [ ] Maximum Delivery como estrategia de puja
- [ ] Sin UTM parameters
- [ ] Insight Tag no instalado o no verificado
- [ ] CAPI no configurado
- [ ] Lead Gen Forms sin sync CRM (datos se pierden a 90 días)
- [ ] Un solo formato de anuncio activo
- [ ] Sin retargeting audiences configuradas
- [ ] Budget <€50/día por campaña

---

## 8. Greenfield Scorecard

Para cuentas que **nunca** han corrido LinkedIn Ads:

| Factor | Peso | Evaluar |
|---|---|---|
| ACV | Alto | ¿Justifica CPC €8-14? |
| Ciclo venta | Alto | ¿Paciencia para 3+ meses? |
| ICP clarity | Alto | ¿Mapeable a filtros LinkedIn? |
| Presupuesto | Alto | ¿≥€3K/mes? |
| Organic presence | Medio | ¿Inventory para TLAs? |
| CRM maturity | Medio | ¿OCI posible? |
| Content library | Medio | ¿Hay qué promover? |
| Sales capacity | Alto | ¿Follow-up <24h? |

### Secuencia de lanzamiento Greenfield

1. Text Ads (impresiones gratuitas, datos iniciales)
2. Image Ads (cold, validar targeting y copy)
3. TLAs (cuando hay organic inventory)
4. RTG campaigns (cuando hay suficiente tráfico)
5. Conversation Ads (cuando RTG pool suficiente)
6. Acceleration (cuando pipeline abierto)
