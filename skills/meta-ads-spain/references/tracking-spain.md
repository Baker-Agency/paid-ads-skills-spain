# Tracking y Atribución — Meta Ads España

## El Problema: Pérdida de Conversiones

- Tracking estándar (pixel browser-side) pierde 10-30% conversiones
- Causas: borrado cookies, navegación privada, ad blockers, iOS ATT
- **En España:** tasa alta rechazo cookies (GDPR + LOPD) → pérdida MAYOR que US/UK
- Estimación: 40-60% usuarios españoles rechazan cookies
- Cada conversión perdida = señal menos para el algoritmo → optimización degrada

## Meta Pixel (Dataset)

### Setup básico
- Ubicación: Business Settings > Data Sources > **Datasets** (ya no "Pixel")
- Crear dataset → **Connected Assets** → vincular Ad Account
- Instalar código base en TODAS las páginas web
- Verificar con **Meta Pixel Helper** (extensión Chrome)

### Standard vs Custom Events
- **SIEMPRE usar Standard Events** (purchase, complete_registration, lead, initiate_checkout, view_content)
- Meta tiene datos extensos sobre Standard Events → optimización significativamente mejor
- Custom Events solo cuando no existe Standard Event equivalente

### Pasar valor
- En eventos purchase/registration: pasar `currency` (EUR), `value`, `predicted_ltv`
- Predicted LTV ayuda al algoritmo a entender valor real, no solo transacción inicial
- Ejemplo: suscripción €200/mes → pasar predicted_ltv = €4.800 (24 meses LTV)

## CAPI (Conversions API)

### Por qué es obligatorio
- Sin CAPI: 10-30% conversiones invisibles
- Con CAPI: servidor envía datos a Meta independientemente de cookies/blockers
- EMQ (Event Match Quality) mejora → mejor optimización

### Implementación
| Método | Complejidad | Coste | Recomendado para |
|---|---|---|---|
| Partner integration (Zapier, Make) | Baja | €20-50/mes | Presupuestos <€5.000 |
| Integración nativa CRM (HubSpot, GHL) | Media | Incluido en CRM | CRM ya implementado |
| GTM Server-Side | Alta | €50+/mes + setup | Presupuestos >€5.000 |

### Event Match Quality (EMQ)
- Objetivo: **>6.0** por evento principal
- Rating "Good" o "Great" = OK
- Rating "Poor" o "OK" = mejorar inmediatamente
- Parámetros a enviar (hashed): email, teléfono, fbp, fbc, external_id
- Cuantos más parámetros → mayor EMQ → mejor matching

### Deduplicación
- Implementar `event_id` entre browser y servidor = **imprescindible**
- Sin deduplicación: conversiones contadas 2× (browser + server)
- Test: disparar conversión → Events Manager → debe aparecer UNA sola
- Error común: formularios que disparan pixel en cada cambio estado (reschedules, cancelaciones) → deduplicar a nivel CRM/web

### Latencia
- Eventos servidor: <minutos (ideal)
- >1 hora: señal optimización retrasada
- Batch uploads >24 horas: datos basura para optimización en tiempo real

## AEM (Aggregated Event Measurement)

### Qué es
Sistema Meta para tracking post-iOS 14.5. Prioriza 8 eventos por dominio verificado.

### Configuración
- Events Manager > Aggregated Event Measurement > Configure Web Events
- Requisito previo: dominio verificado
- Configurar prioridad de eventos

### Prioridad recomendada (lead gen)

| Prioridad | Evento | Razón |
|---|---|---|
| 1 | Purchase / Closed Deal | Máximo valor negocio |
| 2 | Qualified Lead / Engaged Lead | Lead de calidad |
| 3 | Schedule / Book Call | Acción concreta |
| 4 | Lead / Form Submit | Volumen |
| 5 | ViewContent | Señal intent |
| 6 | PageView | Baseline |

### Errores comunes
- Prioridades por defecto nunca configuradas → PageView por encima de Lead
- Solo 1 evento configurado → configurar 3-5 mínimo
- Dominio no verificado → AEM no funciona

## GDPR + LOPD en España

### LOPD-GDD
- Refuerza GDPR con requisitos adicionales para España
- Aplica a todo negocio que opere en España
- Multas: hasta €20M o 4% facturación global
- Agencia reguladora: AEPD (Agencia Española de Protección de Datos)

### Impacto en tracking Meta
- ~40-60% usuarios españoles rechazan cookies
- Eventos de usuarios sin consent = señal limitada para Meta
- iOS ATT opt-outs + cookie rejection = doble pérdida en España

### Requisitos prácticos
1. Banner cookies conforme CMP certificado (CookieYes, Cookiebot, OneTrust)
2. Consent mode v2 implementado (obligatorio EEE desde marzo 2024)
3. Registro actividades de tratamiento
4. Política privacidad actualizada
5. DPO si aplica
6. Formularios: checkbox opt-in explícito (no pre-marcado)

### Soluciones para recuperar datos
1. **CAPI** (principal) — tracking servidor, independiente de cookies
2. **Enhanced Match** — match usuarios por email/teléfono hashed
3. **Edge tagging** — tracking a nivel DNS/CDN antes de consent mode
4. **Server-side GTM** — captura datos antes de bloqueos

## First-Click Edge Tag CAPI Imports

### El problema

**Según John Moran (Tier 11):**
- Pixel Meta cubre TODO el tráfico web (directo, orgánico, email, otros paid)
- Meta atribuye cualquier conversión a sí mismo — incluso sin clic — vía datos modelados
- Resultado: algoritmo optimiza para conversiones que NUNCA vinieron de Meta
- Más gasto → plataforma atribuye más → métricas parecen escalar → pero nuevos clientes NO crecen

### La solución: 3 capas

**1. First click:** solo contar conversiones donde primera visita vino del canal vía clic real. Sin view-through, sin crédito cross-channel.

**2. Edge tag:** taggear usuarios a nivel DNS/CDN ANTES de la web. Antes de consent mode, cookie blockers, ad blockers, iOS. Datos más limpios posibles.

**3. CAPI imports filtrados:** importar SOLO las conversiones filtradas como optimization event. El negocio decide qué cuenta:
- Solo nuevos clientes → campañas crecimiento
- Solo leads cualificados → calidad sobre volumen
- Por producto/servicio → push específico

### Resultados esperados
- CPA in-platform parecerá terrible (normal — solo cuentas first-click new customers)
- ENCAC mejora significativamente (señal más limpia → audiencia más precisa)
- Primeras 2-3 semanas: difíciles. Algoritmo aprendiendo
- Caso: ENCAC pasó de $26-27 → $6.73 en 6 semanas

### Requisitos técnicos
- Proveedor edge tag
- Herramienta medición third-party
- Data warehouse para lógica first-click attribution
- Integración CAPI con Meta
- No es DIY — requiere infraestructura técnica

## ENCAC Tracking

### Fórmula

```
ENCAC = Gasto total ads (todas plataformas) / Nuevos clientes totales (del CRM)
```

### Implementación
- Calcular mensualmente
- Fuente: CRM (no plataformas ad)
- Comparar vs Meta-reported CAC
- Si Meta-CAC << ENCAC: sobreatribución → investigar view-through
- Si Meta-CAC >> ENCAC: canibalización por otros canales (raro)

### Atribución recomendada en Meta
| Escenario | Ventana | Razón |
|---|---|---|
| Mayoría lead gen | 7-day click | Standard. Captura leads que clican y convierten en 1 semana |
| Ciclo venta corto (<3 días) | 1-day click | Conservador. Evita sobreatribución |
| High-ticket, larga consideración | 7-day click | Necesita ventana completa |
| Comparación con GA4 | 1-day click (en Meta) | Más cercano al last-click de GA4 |

**Eliminar view-through attribution** salvo necesidad específica. 1-day view cuenta gente que vio pero no clicó → infla conversiones para lead gen.

## Tracking Operativo Completo — España

| Método conversión | Herramienta | Impacto si falta |
|---|---|---|
| Formularios web | Pixel + CAPI | Baseline |
| WhatsApp (+34) | WhatsApp API → CAPI | 10-30% leads España |
| Llamadas telefónicas | CallRail / WhatConverts | 10-20% leads |
| Chat en vivo | Platform webhook → CAPI | 5-20% leads |
| Reservas calendario | Webhook → pixel/CAPI | 10-20% leads |
| Email reply | CRM automation → CAPI | 5-10% leads |

**WhatsApp especialmente crítico en España** — 96% penetración. No trackearlo = 10-30% señales invisibles.

### Cadena reacción tracking roto
```
Pixel/CAPI se rompen → Conversiones a la mitad → Algoritmo optimiza señal parcial
→ Muestra ads a audiencia incorrecta → Calidad leads baja → ENCAC sube
→ Espiral descendente
```

Fix: auditar TODOS los métodos conversión regularmente. Verificar Events Manager mensualmente.

## Pixel Duplicate Firing

### Problema
- Formularios que disparan pixel en cada cambio estado (reschedules, cancelaciones)
- Ejemplo: Meta reporta 8 calls, CRM muestra 2 (reschedules contados como nuevos)
- Infla datos → algoritmo aprende de señales falsas

### Fix
- Configurar pixel para disparar UNA VEZ por contacto
- Deduplicar a nivel CRM/web antes de disparar pixel
- Implementar event_id para deduplicación browser↔server
