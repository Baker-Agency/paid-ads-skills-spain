---
name: meta-ads-spain
description: Meta Ads (Facebook/Instagram) campaign management for the Spanish market (Spain). Setup, optimize, scale, and audit Meta Ads campaigns for lead gen, SaaS, and services targeting Spain. Use when managing Meta Ads for Spanish clients, launching Facebook/Instagram campaigns in Spain, auditing Spanish Meta Ads accounts, configuring Business Manager, setting up Meta Pixel and CAPI, building audiences, creating creativos, optimizing formularios instantáneos, or adapting Meta Ads strategy for the Spanish/European market. Covers Andromeda algorithm, Advantage+ Sales, CBO/ABO structure, Instant Forms, lead gen optimization, creative diversity, signal & trust, ENCAC tracking, and automated rules for Spain. Also use when dealing with Meta account bans, SAC (Special Ad Categories), or LOPD/GDPR compliance for Meta campaigns in Spain.
---

# Meta Ads España — Skill de Gestión Completa

Gestión integral de Meta Ads (Facebook + Instagram) para lead gen, SaaS y servicios en el mercado español. NO e-commerce.

**Todo el contenido está adaptado al mercado español:** benchmarks en EUR, IVA 21%, LOPD/GDPR, estacionalidad española, copy en español, WhatsApp como canal clave.

## Quick Reference — España

| Métrica | Valor España |
|---|---|
| CPL servicios locales | €8-25 |
| CPL coaching/formación B2C | €4-16 |
| CPL B2B SaaS | €25-65 |
| CPL clínicas estéticas | €3-8 (Meta) |
| CPM rango normal | €12-40 (lead gen) |
| IVA | 21% (incluir en cálculos unit economics) |
| Learning phase | ~50 conversiones desde última edición significativa |
| Presupuesto mínimo viable | €1.500-2.500/mes (Andromeda necesita datos) |
| Frecuencia sana prospecting | <2-3 (30 días) |
| Frecuencia sana retargeting | <3-5 (30 días) |
| Consent mode España | 40-60% rechazo cookies (GDPR + LOPD) |
| EMQ objetivo CAPI | >6.0 |
| Umbral creative fatigue | Frecuencia >1.15 en demand creation |
| Audiencia mínima broad | 100.000+ para entrega estable |

---

## Fase 0: Evaluación de Viabilidad

### Framework CAC para servicios (EUR)

1. **Valor del deal × margen × tasa cierre** = CAC permisible
2. **CAC ÷ show rate** = coste por llamada reservada
3. **Coste por llamada ÷ tasa de booking** = CPL objetivo

**Ejemplo (coaching high-ticket, España):**

| Paso | Métrica | Valor |
|---|---|---|
| 1 | Deal €10.000 × 3x ROAS | CAC permisible = €3.333 |
| 2 | Tasa cierre 20%, show rate 50% | 10 calls para cerrar = €333/call |
| 3 | Booking rate 30% | CPL objetivo = ~€100 |

Incluir IVA 21% en cálculos: servicio factura €1.000 → neto sin IVA = €826,45.

**Cuentas nuevas:** CPMs más altos inicialmente — el pixel carece de datos. Costes bajan conforme la cuenta aprende.

→ Detalle completo: [references/unit-economics-spain.md](./references/unit-economics-spain.md)

---

## Fase 1: Setup de Cuenta

### Business Manager

- Crear en business.facebook.com/overview. Máximo 2 BM por persona
- **NUNCA** correr ads desde cuentas personales → usar siempre Business Manager
- Invitar admin de respaldo (si te banean, pierdes acceso sin backup)
- Activar 2FA en Security Center (obligatorio para ciertas funciones)
- Rellenar toda la info de negocio (nombre, web, teléfono) → builds trust, desbloquea funciones

### Cuenta publicitaria

- [ ] Timezone: **CET (España)** — el algoritmo resetea a medianoche de la zona seleccionada. NO se puede cambiar después
- [ ] Moneda: **EUR** — debe coincidir con la moneda de tu cuenta bancaria
- [ ] País facturación: debe coincidir con tu ubicación real (evitar flags de seguridad)
- [ ] Tarjeta virtual: **UNA tarjeta por cuenta publicitaria**. Nunca compartir tarjeta entre cuentas → si una se banea, todas caen
- [ ] Verificar dominio: Business Settings > Brand Safety > Domains (necesario para AEM y tracking completo)

### Página de Facebook

- Rellenar TODO: bio, dirección, teléfono, enlaces → páginas vacías = CPMs altos + rechazos
- Publicar contenido orgánico mínimo 1x/semana → el coste de mantener la página se recupera en menores CPMs

→ Detalle completo: [references/account-setup-checklist.md](./references/account-setup-checklist.md)

---

## Fase 2: Estructura de Campañas (Era Andromeda)

### Andromeda: el cambio de paradigma (2025-2026)

El algoritmo de Meta ahora hace matching individual usuario↔anuncio. Ya no es segmentación por audiencia, sino matching 1:1. Consecuencia: **diversidad creativa** es la palanca principal. Sin diversidad → frecuencia alta → audiencia reducida.

### Estructura por presupuesto

| Presupuesto/mes | Pixel | Estructura recomendada |
|---|---|---|
| <€2.500 | Nuevo (0-50 conv) | 1 ABO, 3-5 ad sets, audiencia broad |
| €2.500-8.000 | Algo de data (50-200 conv) | Testing ABO (20%) + Scaling CBO (80%) |
| €8.000-25.000 | Maduro (200+ conv) | Testing ABO (15%) + TOFU CBO (60%) + Retargeting CBO (25%) |
| €25.000+ | Fuerte (500+ conv) | Portfolio: CBOs por persona/concepto + diversificación pujas |

### CBO vs ABO

| Usar CBO cuando | Usar ABO cuando |
|---|---|
| Escalando ads/audiencias probadas | Testeando nuevos conceptos (necesitas control por test) |
| 3+ ad sets con presupuesto suficiente | Aislando variables (1 concepto por ad set a presupuesto fijo) |
| Quieres que el algoritmo distribuya gasto | B2B high-ticket con control preciso de audiencia |

### Estrategia "One CBO + Flex Ads" (Andromeda)

- **1 CBO** (Advantage Campaign Budget) para toda la cuenta. Objetivo "Sales"
- **1 ad set.** Dentro: **1 Flex Ad** con 2-3 variaciones creativas
- **No tocar.** Ediciones = reshuffling → learning phase de nuevo
- Solo añadir ad sets por razón estratégica (nuevo persona, nueva oferta)
- Ideal: presupuestos €2.500-12.000/mes con volumen creativo limitado

### Framework TPS: Test → Prove → Scale

1. **Test** (€40-50/día por ad set): 5 campañas ABO, cada una = 1 concepto
2. **Prove** (€150-200/día): Ganadores duplicados con post ID a 4× presupuesto. Mínimo 48-72h
3. **Scale** (CBO €400-8.000+/día): 3-5 ads probados en CBO

→ Detalle completo: [references/campaign-structure.md](./references/campaign-structure.md)

---

## Fase 3: Audiencias y Segmentación

### Árbol de decisión targeting (Era Andromeda)

| Situación | Enfoque |
|---|---|
| Pixel maduro (200+ conv) | **Broad** (zero interests, solo ubicación + edad) — el algoritmo conoce a tu cliente |
| Cuenta nueva, sin data pixel | **Stacked broad interests** (3-4 intereses masivos, 20M-40M+) → cambiar a broad tras 200+ conv |
| Broad falla tras 7 días + €400 gasto | Testear 2-3 combinaciones de intereses |
| B2B con ICP específico | Stacked B2B interests + Value Rules |
| High-ticket (€5K+), <50 conv/mes | ABO con LALs de CRM seed (clientes/llamadas) |

### Jerarquía calidad de seeds (LAL)

1. Clientes que pagan / deals cerrados (mejor)
2. Llamadas reservadas / leads cualificados
3. Todos los leads / envíos de formulario
4. Visitantes web (páginas de intención: pricing, demo)
5. Engagers página/post (señal débil)

**Mínimo seed:** 1.000+ para LALs útiles. 5.000+ ideal. <200 = no usar LALs, ir broad.

### Ventana retargeting por ciclo de venta

| Ciclo venta | Hot | Warm | Cool |
|---|---|---|---|
| <7 días (servicio local) | 1-3 días | 3-7 días | 7-14 días |
| 7-30 días (coaching B2C) | 1-7 días | 7-14 días | 14-30 días |
| 30-90 días (B2B SaaS) | 1-14 días | 14-30 días | 30-60 días |

Adaptar creativo por ventana: hot = CTA directo, warm = prueba social, cool = nuevo ángulo.

→ Detalle completo: [references/audiences-targeting.md](./references/audiences-targeting.md)

---

## Fase 4: Creativos y Formatos

### Settings a nivel de anuncio — DESACTIVAR todo

- [ ] Multi-advertiser ads: **OFF**
- [ ] Browser add-ons: **OFF**
- [ ] Translate text: **OFF**
- [ ] Add overlays: **OFF**
- [ ] AI enhancements (Advantage+): **OFF**
- [ ] Related Media: **OFF** (esconde datos de rendimiento — imposible saber qué creativo funciona)

### Mix de formatos recomendado

| Formato | % de ads activos | Mejor para |
|---|---|---|
| Imagen estática (4:5) | 30-40% | Producción rápida, test de ángulos |
| Video (talking head / UGC) | 30-40% | Construcción confianza, TOFU/MOFU |
| Carrusel | 10-15% | Ofertas con texto, paso a paso |
| Collection / Instant Experience | 5-10% | Catálogo multi-oferta |

### Specs por placement

| Placement | Aspect ratio | Resolución mín | Video óptimo |
|---|---|---|---|
| Feed (FB + IG) | 4:5 (mejor), 1:1 | 1080×1350 | 15-60s |
| Stories / Reels | 9:16 | 1080×1920 | 15-30s (frío), 30-60s (warm) |
| Right column | 1:1 | 1080×1080 | Solo imagen |

**Siempre** proporcionar versiones 4:5 Y 9:16. Sin 9:16 → Meta auto-recorta → texto/logos cortados.

### Diversidad > Volumen

16 anuncios completamente distintos > 50 anuncios que se parecen. Meta trata anuncios visualmente similares como el mismo anuncio.

**Test "3 pasos atrás":** pon todos tus creativos en pantalla y da 3 pasos atrás. Si todos se ven iguales → el algoritmo y el consumidor los ven iguales.

### Copy en español — Tú vs Usted

| Sector | Tratamiento | Ejemplo |
|---|---|---|
| Servicios locales | Tú | "Pide tu presupuesto gratis" |
| Fitness, coaching | Tú | "Transforma tu cuerpo en 90 días" |
| Legal, financiero | Usted | "Solicite su consulta gratuita" |
| Médico/estético (web) | Tú | "Descubre nuestros tratamientos" |
| B2B / enterprise | Usted | "Agende una demo personalizada" |

→ Detalle completo: [references/creative-formats.md](./references/creative-formats.md) y [references/spanish-ad-copy.md](./references/spanish-ad-copy.md)

---

## Fase 5: Lead Generation

### Formularios instantáneos — configuración

- [ ] Tipo formulario: **Higher Intent** (desbloquea verificación OTP)
- [ ] Verificación SMS (OTP): **ACTIVAR** — filtra números falsos y leads de baja intención
- [ ] Autofill: **DESACTIVAR** — forzar entrada manual para datos precisos
- [ ] Orden campos: Nombre → Apellidos → Email → Teléfono (separar nombre y apellidos para CRM)
- [ ] Sharing: **"Open"** para que la gente pueda compartir el anuncio
- [ ] Headline del form: framing como cualificador ("Descubre si cualificas para...")

### Routing post-formulario (Two-Step)

Usar pantalla de confirmación para dirigir a acción secundaria inmediata:
- **WhatsApp** (preferido en España — 96% penetración)
- **Messenger**
- **Calendario de reservas**

### Optimizar para Purchases (no Leads)

**El problema:** optimizar por "Leads" o "Schedules" → CPLs baratos pero leads que no se presentan. El algoritmo encuentra "rellenadores de formularios", no compradores.

**La solución:** cambiar objetivo a Purchases. Crear evento de conversión personalizado para transacción real (ej: cargo en tarjeta tras llamada exitosa). Alimentar este evento a Meta.

**Resultado:** show rates suben drásticamente, calidad de leads mejora, revenue bottom-line sube.

### Estrategia pixel "engaged lead"

Evento genérico de lead = cualquiera que envía formulario. Evento "engaged lead" = solo quien toma acción de alta intención post-envío (ej: clic en link del primer email de confirmación → VSL o página de reserva).

→ Detalle completo: [references/lead-gen-forms.md](./references/lead-gen-forms.md)

---

## Fase 6: Cadencia de Optimización

### Primeros 7 días: SOLO monitorizar

| Día | Acción |
|---|---|
| 1-2 | ¿Pixel dispara? ¿Anuncios aprobados? ¿Se gasta presupuesto? |
| 3-7 | Check entrega, CPMs. ÚNICA optimización: pausar anuncios rechazados |

**NO tocar presupuestos, audiencias ni estructura la primera semana.**

### Cadencia post-lanzamiento

| Frecuencia | Acción |
|---|---|
| **Diaria** | Check anomalías (¿campañas activas? ¿desaprobaciones? ¿gasto normal?) — NO optimizar |
| **Semanal** | Frecuencia por anuncio, pacing, métricas por placement, calidad leads (CRM) |
| **Mensual** | Creative refresh, reasignación presupuesto, auditoría audiencias, revisión ENCAC |
| **Trimestral** | Auditoría completa cuenta, revisión estructura, refresh estrategia oferta |

### Cuándo preocuparse

- **1 día malo:** ruido normal. No tocar
- **3 días consecutivos malos:** investigar (tracking, rechazos, problemas entrega)
- **1-2 semanas de caída:** optimizar con datos reales

### Jerarquía de optimización

1. **Creativos** — probar nuevos conceptos y hooks (MAYOR IMPACTO en Meta)
2. **Oferta/LP** — mejorar oferta, formulario, página de destino
3. **Presupuesto** — mover gasto a campañas ganadoras
4. **Audiencias** — ajustar targeting, exclusiones
5. **Pujas** — último recurso, solo con datos suficientes

→ Detalle completo: [references/optimization-cadence.md](./references/optimization-cadence.md)

---

## Fase 7: Escalado

### Regla del 20%

Incrementos de presupuesto diario del 20% = umbral seguro para no resetear learning phase.

### Fases de escalado

| Fase | Presupuesto/día | Foco |
|---|---|---|
| Validación | €40-80 | Encontrar 1 ángulo ganador |
| Proof | €150-200 | Duplicar ganadores a 4× budget |
| Scale inicial | €400-800 | CBO con 3-5 ads probados |
| Scale agresivo | €800-8.000+ | Portfolio CBOs, diversificación |

### ENCAC como norte

```
ENCAC = Gasto total ads (todas plataformas) / Nuevos clientes totales (del CRM)
```

- Meta se auto-reporta. ENCAC = verdad independiente
- Si CAC Meta << ENCAC: Meta sobreatribuye (común con view-through)
- Si ENCAC es estable al escalar → ESCALAR. Ignorar CPA in-platform

### Signal & Trust (predictor de escalabilidad bajo Andromeda)

- **Signal** = feedback de comportamiento usuario por creativo. No solo conversiones — incluye QUIÉN compra y a qué velocidad
- **Trust** = confianza de Meta en que el anuncio REPETIRÁ la misma señal. Consistencia: mismo tipo de usuario responde, velocidad consistente, sin feedback negativo

→ Detalle completo: [references/scaling-framework.md](./references/scaling-framework.md)

---

## Fase 8: Tracking y Atribución

### Meta Pixel (ahora "Datasets")

- Ubicación: Business Settings > Data Sources > **Datasets**
- Tras crear, vincular a Ad Account en **Connected Assets**
- Instalar código base en TODAS las páginas
- Verificar con **Meta Pixel Helper** (extensión Chrome)
- Usar **Standard Events** (purchase, complete_registration) > Custom Events — Meta tiene más datos sobre standard

### CAPI (Conversions API)

- Implementar SIEMPRE — sin CAPI pierdes 10-30% conversiones
- EMQ (Event Match Quality) objetivo: **>6.0** por evento principal
- Parámetros: email (hashed), teléfono (hashed), fbp, fbc, external_id
- Deduplicación: event_id entre browser + servidor = imprescindible
- Implementar vía GTM Server-Side o integración nativa CRM (Zapier, Make)

### AEM (Aggregated Event Measurement)

Prioridad eventos para lead gen:
1. Purchase / Closed Deal
2. Qualified Lead
3. Schedule / Book
4. Lead / Form Submit
5. ViewContent
6. PageView

### GDPR + LOPD en España

- España: **40-60% usuarios rechazan cookies** → pérdida tracking MAYOR que US/UK
- LOPD refuerza GDPR con requisitos adicionales
- Consent mode v2 obligatorio EEE desde marzo 2024
- Banner cookies CMP certificado (CookieYes, Cookiebot, OneTrust)
- Formularios: checkbox opt-in explícito (no pre-marcado)

### Tracking operativo completo (España)

| Método conversión | ¿Trackeado? | Impacto si falta |
|---|---|---|
| Formularios web | Standard | Baseline |
| WhatsApp (+34) | Evento personalizado | 10-30% leads en España |
| Llamadas telefónicas | CallRail/WhatConverts | 10-20% leads |
| Reservas calendario | Webhook → CAPI | 10-20% leads |
| Chat en vivo | Webhook → CAPI | 5-20% leads |

Cada método sin trackear = señales perdidas → algoritmo degrada.

→ Detalle completo: [references/tracking-spain.md](./references/tracking-spain.md)

---

## Fase 9: Reglas Automatizadas

### Templates esenciales

**1. CPA Ceiling (Crítica):**
- Condición: Coste por resultado > 2× CPA objetivo últimos 3 días
- Acción: Pausar ad set
- Frecuencia: Cada 12 horas

**2. Alerta Frecuencia:**
- Condición: Frecuencia > 3 (prospecting) o > 5 (retargeting) últimos 7 días
- Acción: Enviar notificación
- Frecuencia: Diaria

**3. Escalado Presupuesto (Conservador):**
- Condición: Coste por resultado < CPA objetivo 3 días consecutivos Y 20+ resultados
- Acción: Incrementar presupuesto diario 20%
- Frecuencia: 1×/día, máx 1× por campaña

**4. Spend Cap Diario:**
- Condición: Gasto hoy > 1.5× presupuesto diario
- Acción: Enviar notificación
- Frecuencia: Cada 6 horas

### Naming convention

`[Acción]_[Métrica]_[Umbral]_[Scope]` — ej: `Pausar_CPA_2x_AdSet`, `Escalar_CPA_Bajo_Campaña`

### Limitaciones

- Reglas evalúan cada 30 min mínimo — no son tiempo real
- Rango "últimos 3 días" más seguro que "hoy" (hoy resetea a medianoche)
- Reglas no se activan en Learning Phase
- Timezone: usa timezone de la cuenta publicitaria

→ Detalle completo: [references/automated-rules.md](./references/automated-rules.md)

---

## Fase 10: Auditoría de Cuentas

### Orden de auditoría

1. **Pixel + CAPI** — ¿dispara correctamente? ¿EMQ >6.0? ¿Deduplicación activa?
2. **Business Manager** — ¿propiedad correcta? ¿2FA? ¿Admin backup? ¿Dominio verificado?
3. **Estructura campañas** — ¿consolidada o fragmentada? ¿% en learning?
4. **Audiencias** — ¿audiencias frescas? ¿seeds de calidad? ¿exclusiones correctas?
5. **Creativos** — ¿diversidad formatos? ¿frecuencia sana? ¿Related Media OFF?
6. **Métricas** — benchmarks vs sector, ENCAC, calidad leads (CRM)
7. **Funnel post-clic** — LP, speed to lead, nurture, show rates

### Red flags inmediatos

- [ ] Account spend limit olvidado (bloqueador silencioso #1 de escalado)
- [ ] Advantage+ AI enhancements activados (esconde rendimiento real)
- [ ] Related Media ON (esconde datos creativos)
- [ ] Sin CAPI (pérdida 10-30% conversiones)
- [ ] Optimizando por "Lead" cuando el negocio valora "Booked Call"
- [ ] Multiple admins haciendo ediciones conflictivas
- [ ] PMax o Advantage+ Leads en categorías especiales (SAC)

→ Detalle completo: [references/audit-checklist.md](./references/audit-checklist.md)

---

## Fase 11: Troubleshooting

### Zero/baja entrega — checklist 9 pasos

1. **Status jerarquía** — Campaign, Ad Set, Ad: todos "Active"?
2. **Audiencia demasiado pequeña** — mínimo 100.000+ para entrega estable
3. **Puja demasiado baja** — si usas cost cap/bid cap, probar Lowest Cost
4. **Anuncio rechazado** — revisar razón, editar y resubmitir
5. **Cuenta restringida** — Account Quality, apelar si false positive
6. **Campaña/ad set pausado accidentalmente** — revisar toggle + automated rules
7. **Learning phase estancada** — 50+ conversiones necesarias. Consolidar ad sets
8. **Presupuesto bajo para el evento** — mínimo 2-3× CPA objetivo por día
9. **Problemas de facturación** — tarjeta rechazada, límite crédito

### Bans de cuenta Meta

**Triggers principales (2026):**
- Conectar herramientas automation vía API (Zapier, bots)
- IPs inconsistentes (VPN on/off)
- 100% contenido generado por AI
- Perfiles sin actividad orgánica

**Plantilla apelación (para AI reviewer):**
> "Creemos que esta restricción puede haber sido aplicada por error. Nos tomamos esto muy en serio. Queremos cumplir con las políticas. Agradeceríamos una revisión manual de esta cuenta. Gracias."

**Escalación si apelación falla:**
1. Meta Account Rep → escalar caso
2. **Meta Verified** (suscripción de pago → ticket soporte directo — método más exitoso)
3. Chat soporte por otro problema (billing, cuenta hackeada) → bypass loops automatizados

**Prevención:**
- No conectar APIs durante olas de bans
- IP consistente (si VPN, mantenerla ON)
- Actividad orgánica mínima en perfil
- Siempre 2+ admins en Business Manager
- Creativos AI < 50% del total

→ Detalle completo: [references/troubleshooting.md](./references/troubleshooting.md)

---

## Mercado Español — Particularidades

### Estacionalidad España

| Período | Impacto | Acción |
|---|---|---|
| Enero (rebajas) | Alto volumen | Aumentar presupuesto |
| Semana Santa | Turismo ↑, servicios ↓ | Ajustar por vertical |
| Julio (rebajas verano) | Alto volumen | Aumentar si aplica |
| Agosto | **Bajón generalizado** | **Reducir 30-50%** |
| Septiembre (vuelta al cole) | Recuperación fuerte | Preparar antes |
| Black Friday (nov) | Pico + CPMs altos | Preparar desde octubre |
| Navidad + Reyes (dic-ene) | Pico máximo | Máximo presupuesto |

### Comportamiento consumidor español

- **WhatsApp > Email** — 96% smartphones tienen WhatsApp. Integrar en flujo leads
- **Bizum** — 25M+ usuarios. Relevante servicios locales
- **Sensibilidad precio alta** — ofertas entrada €50-120 funcionan muy bien
- **Financiación** aceptada — 40-60% pagos en clínicas financiados
- **Horario comercial:** 9:00-14:00 + 16:00-21:00 (horario partido)
- **3ª semana mes = más débil** (antes de nómina). Fin de mes + domingo = mejor
- **Paga extra** junio y diciembre → push presupuesto

### Targeting regional

- Madrid y Barcelona = ~40% mercado publicitario
- Campañas separadas por CC.AA. solo si presupuesto lo permite
- Idiomas cooficiales: catalán (Catalunya, Valencia), euskera (País Vasco), gallego (Galicia)
- CPMs Madrid/Barcelona > resto España

→ Detalle completo: [references/spain-market-guide.md](./references/spain-market-guide.md)

---

## Categorías Especiales (SAC)

Aplica a: housing, credit, employment, social/political issues.

**Restricciones:** sin segmentación por edad/género, radio mínimo 15 millas, sin LALs estándar (solo Special Ad Audiences), intereses limitados.

**Workarounds:**
1. Custom Audiences (retargeting, CRM) — NO restringidos
2. Broad + creativo fuerte — dejar que el creativo haga el targeting
3. Special Ad Audiences (menos precisos que LALs)
4. Value Rules para pujar diferente por señales
5. **NO usar Advantage+ Leads** en SAC

→ Detalle completo en [references/audiences-targeting.md](./references/audiences-targeting.md)

---

## Algoritmo Andromeda

Componentes del stack Meta AI:

| Componente | Rol |
|---|---|
| **GEM** | Procesa datos comportamiento → predice ad más relevante por usuario |
| **Lattice** | Ranking unificado — comparte aprendizajes entre objetivos de campaña |
| **Andromeda** | Retrieval/delivery — decide qué anuncio mostrar en milisegundos |
| **Sequence Learning** | Trackea acciones pre/post anuncio. Secuenciación journey |

**Pipeline:** Andromeda (millones → pool) → GEM (pool → shortlist) → Lattice (selección final)

**Implicación clave:** Andromeda no subió el listón — quitó la red de seguridad. El sistema antiguo toleraba poca diversidad creativa. Andromeda expone cuentas sin diversidad.

→ Detalle completo: [references/andromeda-algorithm.md](./references/andromeda-algorithm.md)

---

## Casos de Éxito España

- [Clínica estética Huelva 8.5x ROAS](./examples/clinica-estetica-huelva-8.5x-roas.md) — €2.105 gasto → €17K revenue
- [Lead gen coaching España](./examples/lead-gen-coaching-spain.md) — Framework coaching/formación B2C

---

## Referencias

| Archivo | Contenido |
|---|---|
| [unit-economics-spain.md](./references/unit-economics-spain.md) | CAC EUR, IVA 21%, márgenes |
| [account-setup-checklist.md](./references/account-setup-checklist.md) | BM, cuenta publicitaria, pixel, CAPI |
| [campaign-structure.md](./references/campaign-structure.md) | CBO/ABO, Andromeda, TPS, consolidación |
| [audiences-targeting.md](./references/audiences-targeting.md) | Broad, LAL, retargeting, SAC |
| [creative-formats.md](./references/creative-formats.md) | Specs, formatos, placements, AI features |
| [spanish-ad-copy.md](./references/spanish-ad-copy.md) | Copy español, tú vs usted, PAS |
| [lead-gen-forms.md](./references/lead-gen-forms.md) | Instant Forms, routing, engaged leads |
| [optimization-cadence.md](./references/optimization-cadence.md) | Cadencia optimización |
| [scaling-framework.md](./references/scaling-framework.md) | Escalado, ENCAC, signal & trust |
| [tracking-spain.md](./references/tracking-spain.md) | Pixel, CAPI, AEM, GDPR/LOPD |
| [automated-rules.md](./references/automated-rules.md) | Reglas automatizadas, templates |
| [audit-checklist.md](./references/audit-checklist.md) | Auditoría cuentas españolas |
| [troubleshooting.md](./references/troubleshooting.md) | Entrega, bans, apelaciones |
| [spain-market-guide.md](./references/spain-market-guide.md) | Guía mercado español |
| [andromeda-algorithm.md](./references/andromeda-algorithm.md) | GEM, Lattice, Andromeda, signal & trust |
