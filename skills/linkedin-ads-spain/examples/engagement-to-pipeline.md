# Case Study: De Ad Engagement a Pipeline — Intent Data First-Party

**Fuente:** Adam (Fibbler)
**Resultado:** 1 SDR reservó 3 demos → €10K pipeline en 1 semana
**Coste:** €0 adicional (usando data de ads que ya corren)

---

## El Concepto

Empresas gastan **€50K+** en herramientas de intent data third-party. Mientras tanto, las señales de intención más fuertes — actividad en web y ad engagement — son datos que **ya tienes**.

---

## Workflow de 5 Pasos

### 1. Lanzar ads LinkedIn a ICP

Targeting estándar: company size + industry + job titles. Nada especial.

### 2. Trackear qué empresas engagean

No solo 1 clic aislado. Buscar **múltiples engagements** de la misma empresa:
- Likes en TLAs
- Clicks en image ads
- Document views
- Video watches
- Company page visits

Enviar engagement data a CRM (vía Fibbler, Zapier, o export manual).

### 3. Crear lista CRM con criterios

**Criterio de activación:**
- **100+ impresiones** de la empresa en últimos **30 días**
- **5+ engagements** de la empresa en últimos **30 días** (o 7 días para trigger más rápido)

### 4. Enviar lista a sales

- **Automatizado (ideal):** workflow CRM → alerta Slack cuando empresa cumple criterios
- **Manual:** export semanal de lista y envío a SDR team
- **Clave:** flujo **continuo**, no batch mensual

### 5. Sales hace outreach en LinkedIn

Los prospects **no son fríos**:
- Ya vieron tu contenido múltiples veces
- Conocen tu narrative y marca
- El SDR puede referenciar el contenido que vieron
- Open rates de outreach significativamente más altos

---

## Case Study Detallado

### Setup

1. Fibbler conectado a LinkedIn Campaign Manager
2. Engagement data routeado a HubSpot
3. Workflow HubSpot: cuando empresa hit 5+ ad engagements en 7 días → alerta automática a SDR asignado

### Resultado

- **1 SDR** recibió alerta sobre varias empresas
- Hizo outreach personalizado en LinkedIn
- **3 demos reservadas** esa semana
- **€10K pipeline value** generado

### Timeline

- Semana 1: workflow configurado
- Semana 2: primeras alertas empiezan a llegar
- Semana 3: SDR actúa sobre alertas → demos → pipeline

---

## Por Qué Funciona

| Factor | Sin intent data | Con intent data (engagement) |
|---|---|---|
| **SDR efficiency** | Outreach frío a lista fría | Outreach warm a empresas que ya interactúan |
| **Prospect receptividad** | Baja (no conocen la marca) | Alta (ya vieron contenido múltiples veces) |
| **Connect rate** | 15-25% | 30-50% (estimado) |
| **Coste herramienta** | €50K+/año (6sense, Bombora, etc.) | €0 adicional (data de ads existentes) |

---

## Implementación en España

### CRM setup (HubSpot ejemplo)

1. Integrar LinkedIn engagement data (vía Fibbler, Zapier, o API)
2. Crear property custom: "LinkedIn Engagement Score"
3. Crear workflow: IF engagement score > threshold → notificación SDR
4. SDR ve: empresa, engagement count, qué contenido vieron

### Sin herramienta automatizada

1. Export semanal: Campaign Manager → Company Engagement Report → CSV
2. Filtrar: empresas con >5 engagements en últimos 7-30 días
3. Cross-reference con target account list en CRM
4. Enviar lista filtrada a sales team vía Slack/email

### Canales de outreach España

- **LinkedIn DM** (primario) — referenciando contenido que vieron
- **Email** — con contexto de engagement
- **WhatsApp** (si B2B SMB España) — canal preferido para comunicación rápida

---

## Métricas a Trackear

| Métrica | Qué medir |
|---|---|
| Alertas generadas/semana | ¿Suficiente volumen de empresas engaged? |
| SDR action rate | ¿% de alertas que resultan en outreach? |
| Connect/response rate | ¿Mejor que outreach frío estándar? |
| Demos booked | ¿Pipeline generado desde intent data? |
| Pipeline value | €€€ |
| Time to pipeline | ¿Más rápido que proceso normal? |

---

## Escalado

- Más ads → más engagement data → más alertas → más pipeline
- Funciona mejor con volumen: necesitas suficientes impresiones para que empresas acumulen 5+ engagements
- Presupuesto mínimo para generar suficiente engagement: ~€3K/mes
- A €10K+/mes: flujo constante de empresas warm para sales
