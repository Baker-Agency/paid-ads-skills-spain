# ABM (Account-Based Marketing) — LinkedIn Ads

## Five Stages Model

En lugar de TOFU/MOFU/BOFU (built para B2C/SMB con ciclos cortos), mapear el journey ABM en 5 stages:

| Stage | Objetivo | Acción | Contenido |
|---|---|---|---|
| **Create** | Brand affinity pre-market | Awareness amplio a target accounts | Thought leadership, publicaciones tercer-party |
| **Capture** | Convertir compradores in-market | Capturar interés activo | Testimonios, case studies, awards, demos |
| **Accelerate** | Cerrar deals abiertos | Multi-thread (ops/finance/HR) | Social proof + objeciones |
| **Revive** | Recuperar deals stalled/lost | Re-engagement | Nuevas ofertas, social proof actualizado |
| **Expand** | Revenue de clientes existentes | Upsell, cross-sell | ABM, referral requests, expansion |

---

## Account Prioritization

### Dos factores

1. **Fit:** Demographic/firmographic (industry, size) + technographic (CRM, tech stack)
2. **Signal:** Triggers de intención directos:
   - Ex-cliente ahora trabaja en target account
   - Cluster de usuarios en free plan (ej: "8 miembros de tu equipo ya usan [Producto]")
   - Acquisition reciente
   - Deals perdidos previamente

### Reglas

- NO outsourcear priorización solo a herramientas dinámicas sin review manual
- Evitar intent tools a nivel account (ej: 6sense) que seleccionan enterprise enteras basándose en 1-2 personas
- Filtrar por contact-level signals para encontrar "pockets" de alta conversión
- **Trampa:** crear wish lists con logos grandes que quedan bien internamente pero no se pueden servir ni si cierran

### CRM tagging preemptivo

Si ejecutando tema específico (ej: competitor takedown), tagear todas target accounts en CRM con año, mes y tema para routing pipeline y attribution más fácil.

---

## ABM Pilot 1:1 (Top 30-50 Cuentas)

### Setup

1. Seleccionar 30-50 accounts que **matemáticamente justifican** toda la inversión si solo 1 cierra
2. 1 campaña por empresa
3. Daily budget: €25/cuenta, bids CPM **ultra-bajos**
4. Coste real: ~€6/mes por empresa (audiencia tiny = pocas impresiones necesarias)
5. Creativos: llamar a la empresa target directamente en el ad
6. Sales **DEBE** hacer outreach simultáneo a las mismas cuentas

### Over-personalization trap

- NO construir campañas 1:1 para 100 cuentas inmediatamente → burnout creativo
- Solo 1:1 personalización (dynamic logos, LP dedicada) para **top 10 cuentas** con más signal
- La mejor personalización NO es "Hola [Empresa]". Es surfacer un data point propietario
  - Ejemplo: "8 miembros de tu equipo ya usan [Producto] en el free plan"

---

## Acceleration Campaigns

### Concepto

Ads contra **oportunidades abiertas** (deals ya en pipeline de ventas). Mejorar win rates y acortar ciclos desde abajo.

### Setup automatizado

1. **Trigger Zapier/Make:** cuando deal stage = "qualified to buy" en CRM
2. **Action:** push empresa a audiencia LinkedIn dinámicamente
3. Si audiencia demasiado pequeña para automatización: campañas 1:1 manuales

### 2 pilares de contenido

1. **Social proof:** mejorar percepción de valor. Testimonios, case studies. TLAs con post orgánico de cliente real = formato más potente
2. **Objeciones:** superar blockers. Trabajar backwards desde objeciones más comunes de ventas:
   - Precio → calculadora de pricing
   - Experiencia → awards de industria
   - Complejidad → demo walkthrough

### Presupuesto

Muy bajo (audiencia = pipeline abierto = tiny). Algunos de los mejores ROI disponibles en LinkedIn.

---

## Ad Engagement como Intent Data

### El workflow de 5 pasos

1. **Lanzar ads LinkedIn a ICP** — targeting estándar
2. **Trackear qué empresas engagean** — no solo 1 clic, sino múltiples engagements → enviar data a CRM
3. **Crear lista CRM:** empresas con **100+ impresiones** y **5+ engagements** en últimos **30 días**
4. **Enviar lista a sales** — workflows automáticos CRM o alerta Slack (continuo, no batch)
5. **Sales hace outreach en LinkedIn** — prospects no son fríos, ya han visto tu contenido

### Case study

Fibbler: routing engagement data a HubSpot → workflow alerta SDRs cuando empresa hit 5+ ad engagements en 7 días. **1 SDR reservó 3 demos → €10K pipeline en 1 semana.**

### Por qué importa

- Reemplaza intent tools third-party caros (empresas gastan €50K+) con first-party ad data
- Bridge entre marketing (awareness) y sales (outreach)
- Prospects están warm — ya vieron tu contenido múltiples veces antes del touch de ventas

---

## Incrementality Testing

### Setup

1. Tomar lista de 1.000 target accounts activamente trabajadas por sales
2. Split 500/500: **Exposed** (recibe ads) vs **Hold-out** (sin ads)
3. Medir durante 3+ meses

### Métricas a comparar

| Métrica | Exposed | Hold-out | Delta |
|---|---|---|---|
| Email open rates | ? | ? | ? |
| Response rates | ? | ? | ? |
| Connect rates | ? | ? | ? |
| Meetings booked | ? | ? | ? |
| Pipeline created | ? | ? | ? |
| Deals closed | ? | ? | ? |

### Resultado

Estructura matemática para probar si brand awareness/impresiones realmente impactan el negocio. Supera las limitaciones de atribución de LinkedIn.

---

## Sales Alignment

### Principios

- **Zero fighting** sobre atribución "marketing vs sales". Todos los touchpoints suman
- ABM = alineación de sales y marketing para penetrar lista de target accounts
- NO es marketing sirviendo ads a 10K accounts (eso es awareness) ni sales haciendo cold outbound en aislamiento

### Nurture Sequences

- NO pitch-slap inmediato a quien descargó contenido TOFU
- Construir "Open Loops" en follow-ups: "Este es el email 1 de 17"
- Incluso si no se leen, el prospect registra percepción de valor ongoing

### Estructuración de personas target

Dos approaches:

1. **Por Job Function:** Departamento (Marketing, Sales, HR). Requiere budgets y creativos separados por función
2. **Por Seniority:** Decision Maker vs Champion. Mensajes diferentes:
   - Champion: cómo resuelve su dolor día a día
   - Ejecutivo: impacto macro nivel

**Constraint de recursos:** si budget bajo, priorizar UNA persona. Multi-thread solo en stage Accelerate.

---

## Media Budgeting para ABM 1:1

- Daily budget por account alto (ej: €25)
- CPM bids **extremadamente bajos**
- Audiencia tiny (una empresa) → hit toda la empresa cuesta muy poco (~€6/mes)
- Resultado: coste por oportunidad muy bajo en ad spend
