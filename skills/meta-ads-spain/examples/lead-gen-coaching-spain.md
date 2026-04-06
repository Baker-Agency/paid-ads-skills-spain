# Framework: Lead Gen Coaching/Formación B2C — Meta Ads España

**Basado en:** benchmarks ads-playbook, frameworks Charley T (Disruptor School), Dylan Bradley, Dr. Matt

## Contexto Típico

| Parámetro | Valor |
|---|---|
| Tipo negocio | Coaching, formación, mentoring, consultoría B2C |
| Ticket medio | €500-5.000 |
| Modelo venta | Formulario → Llamada → Cierre |
| Presupuesto Meta | €1.500-5.000/mes |
| Mercado | España (nacional o por CC.AA.) |

## Unit Economics (EUR)

### Ejemplo: Programa coaching €2.000

| Paso | Métrica | Valor |
|---|---|---|
| Precio programa | €2.000 (sin IVA: €1.653) |
| Margen bruto | 75% | €1.240 |
| ROAS target 3x | | CAC permisible = **€667** |
| Tasa cierre | 15% | |
| Calls para cerrar | 6.67 | |
| Coste por call | €667 / 6.67 | **€100** |
| Show rate | 50% | |
| Cost per booking | €100 × 50% | **€50** |
| Booking rate (lead → booking) | 30% | |
| **CPL objetivo** | €50 × 30% | **€15** |

### Con fee agencia

- Gasto ads: €3.000/mes
- Fee agencia: €600/mes
- Total: €3.600 / 200 leads = €18 CPL real
- 200 leads × 30% booking = 60 bookings
- 60 bookings × 50% show = 30 calls
- 30 calls × 15% cierre = 4.5 clientes
- Revenue: 4.5 × €2.000 = €9.000
- ROAS: €9.000 / €3.600 = **2.5x** (rentable a 3x target)

## Estructura Campaña Recomendada

### Presupuesto €1.500-3.000/mes

```
1 CBO Scaling (80% presupuesto)
├── Ad Set 1: Broad (España, 25-55, sin intereses)
│   ├── 3-5 ads diversos (static + video + carousel)
│   └── Optimization: Lead o Engaged Lead
│
1 ABO Testing (20% presupuesto)
├── Ad Set A: Concepto 1 (dolor específico)
├── Ad Set B: Concepto 2 (resultado deseado)
└── Ad Set C: Concepto 3 (prueba social)
    └── €40-50/día por ad set
```

### Presupuesto €3.000-8.000/mes

Añadir:
- Retargeting CBO (15%): visitantes LP + engagers video/IG + leads no-show
- Advantage+ Leads (si 500+ conv/mes en pixel)

## Funnel Típico España

### Flujo principal
```
Ad (Meta) → Formulario Instantáneo (Higher Intent + OTP)
→ Thank you screen: "Escríbenos por WhatsApp"
→ WhatsApp auto-respuesta: confirmar datos + link calendario
→ Llamada de cierre
```

### Por qué WhatsApp en España
- 96% penetración smartphones
- Tasa respuesta WhatsApp >> email en España
- Permite cualificar rápido antes de llamada
- Automatizable con WhatsApp Business API (~€0,06/mensaje)

### Formulario Instantáneo — Config

| Campo | Valor |
|---|---|
| Tipo | Higher Intent |
| OTP | Activado |
| Campos | Nombre, Apellidos, Email, Teléfono |
| Pregunta cualificación | "¿Cuál es tu mayor reto ahora mismo?" (dropdown 3-4 opciones) |
| CTA post-submit | "Escríbenos por WhatsApp para confirmar tu plaza" |

## Creativos que Funcionan

### Formatos ganadores coaching España

| Formato | % mix | Ejemplo |
|---|---|---|
| Video talking head (coach) | 40% | Coach explica problema → solución → CTA. 30-60s |
| Testimonio video | 20% | Cliente real cuenta resultado. 15-30s |
| Static "resultado" | 20% | Antes/después, números, transformación visual |
| Carrusel "método" | 10% | Paso 1 → Paso 2 → Paso 3 → CTA |
| Reel estilo orgánico | 10% | Contenido valor disfrazado de orgánico. 15-30s |

### Copy — Hooks que funcionan

**Tú (coaching siempre tú):**
- "¿Tu negocio factura pero no crece?"
- "Esto es lo que nadie te dice sobre [tema]"
- "3 errores que cometen el 90% de [profesión]"
- "De €X a €Y en [plazo] — así lo hice"

### PAS en español (coaching)

**P:** "¿Trabajas 12 horas al día y los beneficios no cambian?"
**A:** "Cada mes que pasa sin sistema, pierdes oportunidades que tu competencia sí aprovecha."
**S:** "En 90 días, te ayudo a montar un sistema que facture sin que tú seas el cuello de botella. Reserva tu sesión de diagnóstico."

## Optimización Específica

### Eventos conversión (en orden de sofisticación)

| Nivel | Evento optimización | Cuándo |
|---|---|---|
| 1 (inicio) | Lead (form submit) | Primeras semanas, sin data |
| 2 | Engaged Lead (clic email confirmación / visita booking page) | Tras 50+ leads |
| 3 | Schedule (booking confirmado) | Tras 30+ bookings |
| 4 | Purchase (pago real) | Tras 15+ pagos — máximo nivel |

Cuanto más abajo en funnel optimices → mejor calidad leads → mayor CAC aparente pero mayor revenue real.

### Cadencia optimización

| Tiempo | Acción |
|---|---|
| Semana 1 | Solo monitorizar. ¿Tracking OK? ¿Leads entran? |
| Semana 2-3 | Evaluar calidad leads en CRM. ¿Se presentan a calls? |
| Semana 4 | Primer review completo. ¿CPL real (con shows) aceptable? |
| Mes 2 | Iterar creativos ganadores. Test nuevos hooks |
| Mes 3 | Considerar cambio optimization event (Lead → Engaged Lead) |

## Métricas de Referencia (Coaching España)

| Métrica | Rango típico | Target óptimo |
|---|---|---|
| CPL (form) | €4-16 | <€12 |
| Cost per booking | €30-80 | <€50 |
| Show rate | 40-60% | >50% |
| Tasa cierre | 10-20% | >15% |
| CPM | €12-25 | €15-20 |
| Frecuencia prospecting | <3 (30d) | <2 |
| Speed to lead | <5 min | <2 min (WhatsApp auto) |

## Errores Comunes

| Error | Consecuencia | Fix |
|---|---|---|
| Optimizar por Lead sin revisar calidad | CPL bajo pero 0 ventas | Migrar a Engaged Lead o Purchase |
| No usar WhatsApp post-form | Leads se enfrían | Routing WhatsApp inmediato |
| Mismo creativo 3+ meses | Frecuencia alta, CPL sube | Refresh mensual, test hooks nuevos |
| No trackear show rate | No sabes si ads o ventas es el problema | Integrar CRM con Meta (CAPI offline) |
| Escalar sin CAPI | Pierdes 10-30% señales → algoritmo degrada | Instalar CAPI antes de escalar |
| Ignorar estacionalidad | Gastar en agosto = tirar dinero | Reducir 30-50% agosto, push sept-nov |
