# Setup de Cuenta Meta — Checklist España

## Business Manager

### Creación
- [ ] Ir a business.facebook.com/overview
- [ ] Máximo 2 BM por persona
- [ ] NUNCA usar cuenta personal para ads
- [ ] Si aparece Business Suite simplificado: All Tools > Settings > Business Settings

### Seguridad
- [ ] 2FA activado en Security Center (obligatorio para funciones avanzadas)
- [ ] 2+ admins siempre (backup si te banean). Añadir socio de confianza o familiar
- [ ] Rellenar TODA la info de negocio: nombre, web, teléfono, dirección
- [ ] Esto construye trust con Meta → desbloquea funciones y mayor gasto

### Propiedad
- [ ] El BM del CLIENTE debe ser propietario de la cuenta publicitaria
- [ ] El BM del CLIENTE debe ser propietario de la Página
- [ ] La agencia recibe acceso como partner, NUNCA propietaria
- [ ] Si agencia anterior es propietaria → transferir. Si se niega → escalar

## Cuenta Publicitaria

### Configuración inicial (IRREVERSIBLE)
- [ ] **Timezone:** CET (Europa/Madrid). Algoritmo resetea a medianoche de esta zona
- [ ] **Moneda:** EUR. Debe coincidir con moneda bancaria (evitar comisiones conversión)
- [ ] **País facturación:** España. Debe coincidir con ubicación real (flags seguridad)

### Facturación
- [ ] Tarjeta virtual: **1 tarjeta por cuenta**. NUNCA compartir entre cuentas
- [ ] Si una cuenta se banea o falla pago → todas las cuentas con misma tarjeta en riesgo
- [ ] Tarjeta backup configurada (evitar pausas por pago fallido)
- [ ] Verificar que no hay spend limit antiguo → bloqueador silencioso #1

### Account Quality
- [ ] Revisar Account Quality dashboard
- [ ] Sin restricciones activas
- [ ] <5% anuncios rechazados

## Página de Facebook

### Requisitos mínimos
- [ ] Bio/about completo
- [ ] Dirección funcional
- [ ] Teléfono
- [ ] Links web y redes sociales
- [ ] Foto perfil y cover profesionales

### Mantenimiento
- [ ] Publicar contenido orgánico mínimo 1x/semana
- [ ] Páginas vacías = CPMs altos + mayor riesgo rechazo
- [ ] El coste de mantener actividad orgánica se recupera en menores CPMs

## Pixel (Dataset) Setup

### Instalación
- [ ] Business Settings > Data Sources > **Datasets** (ya no se llama "Pixel")
- [ ] Crear dataset → ir a **Connected Assets** → vincular a Ad Account
- [ ] Instalar código base en TODAS las páginas del sitio web
- [ ] Verificar con **Meta Pixel Helper** (extensión Chrome)

### Eventos
- [ ] Usar **Standard Events** (purchase, complete_registration, lead) > Custom Events
- [ ] Meta tiene más datos sobre Standard Events → optimización más efectiva
- [ ] Instalar pixel lo antes posible — Meta necesita masa crítica de datos (100+ conversiones)

### Pasar valor
- [ ] En eventos purchase/registration: pasar `currency` (EUR), `value`, `predicted_ltv`
- [ ] Predicted LTV ayuda al algoritmo a entender valor real, no solo transacción inicial

## CAPI (Conversions API)

### Implementación
- [ ] OBLIGATORIO — sin CAPI pierdes 10-30% conversiones
- [ ] Implementar vía: GTM Server-Side (preferido) o integración nativa CRM (Zapier, Make, n8n)
- [ ] Verificar con Test Events en Events Manager

### Event Match Quality (EMQ)
- [ ] Objetivo: **EMQ >6.0** por evento principal
- [ ] Parámetros a enviar: email (hashed), teléfono (hashed), fbp, fbc, external_id
- [ ] Rating "Good" o "Great" = OK. "Poor" o "OK" = mejorar

### Deduplicación
- [ ] Implementar `event_id` entre browser y servidor
- [ ] Sin deduplicación = conversiones duplicadas (2× real)
- [ ] Test: disparar conversión → verificar en Events Manager que aparece UNA sola

### Latencia
- [ ] Eventos servidor deben llegar en minutos (no horas)
- [ ] Eventos retrasados >1h = señal de optimización retrasada
- [ ] Batch uploads >24h = datos basura para optimización

## AEM (Aggregated Event Measurement)

### Configuración
- [ ] Events Manager > Aggregated Event Measurement > Configure Web Events
- [ ] Dominio verificado previamente (requisito)
- [ ] Configurar prioridad de 8 eventos por dominio

### Prioridad recomendada (lead gen España)

| Prioridad | Evento |
|---|---|
| 1 | Purchase / Closed Deal |
| 2 | Qualified Lead / Engaged Lead |
| 3 | Schedule / Book Call |
| 4 | Lead / Form Submit |
| 5 | ViewContent |
| 6 | PageView |

### Errores comunes
- Prioridades por defecto (nunca configuradas)
- PageView por encima de Lead (orden incorrecto)
- Solo 1 evento configurado (Lead) — configurar 3-5 mínimo

## Verificación de Dominio

- [ ] Business Settings > Brand Safety > Domains
- [ ] Verificar vía DNS TXT record o meta tag
- [ ] Necesario para AEM y tracking completo
- [ ] Sin verificación → funcionalidad limitada

## Tracking Operativo Completo

Antes de gastar €1, verificar que TODOS los métodos de conversión están trackeados:

| Método | Herramienta | Setup |
|---|---|---|
| Formularios web | Pixel + CAPI | Standard |
| Llamadas (+34 XXX XXX XXX) | CallRail / WhatConverts | 30-60s mínimo |
| WhatsApp | WhatsApp API → CAPI | Evento personalizado |
| Chat en vivo / chatbot | Platform webhook → CAPI | Integración |
| Reservas calendario | Calendly/GHL webhook → pixel/CAPI | Webhook |
| Email reply | CRM automation → CAPI | Automation |

**Test final:** para cada método, disparar conversión test → verificar en Events Manager > Test Events.
