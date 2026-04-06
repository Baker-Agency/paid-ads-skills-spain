# Tracking de Conversiones — España

## El problema: pérdida de conversiones

- Tracking estándar (GA4, Google Ads pixel) pierde 10-30% de conversiones
- Causas: borrado cookies, navegación privada, ad blockers
- En España: tasa alta de rechazo de cookies por GDPR + LOPD → pérdida MAYOR que US/UK
- Cada conversión perdida = una señal menos para Smart Bidding

## Tiers de tracking (coste vs recuperación)

| Tier | Qué hace | Coste | Recuperación |
|---|---|---|---|
| **Básico** (GA4/Google Ads tag) | Tracking browser-side con cookies | Gratis | Baseline — pierde 10-30% |
| **Enhanced conversions** | Match usuarios Google logueados | Gratis | Recupera ~5% (~mitad de la pérdida) |
| **Google Tag Gateway** | JS vía tu CDN → bypass ad blockers | Gratis | Recuperación adicional |
| **Server-side (GTM SS)** | Tracking desde tu servidor | €50+/mes (escala con tráfico) + horas setup + mantenimiento | Recupera 10-30% (full) |
| **Third-party tools** | Server-side vía proveedor externo | Varios cientos €/mes mínimo | Similar a server-side |

### Recomendación por presupuesto ads

| Presupuesto ads | Tier recomendado |
|---|---|
| <€2.000/mes | Básico + Enhanced conversions |
| €2.000-5.000/mes | + Google Tag Gateway |
| >€5.000/mes | Server-side tagging (GTM SS) |

## GDPR + LOPD en España

### Qué es la LOPD
- Ley Orgánica de Protección de Datos (LOPD-GDD)
- Refuerza GDPR con requisitos adicionales para España
- Aplica a cualquier negocio que opere en España
- Multas: hasta €20M o 4% facturación global

### Impacto en tracking

- GA4 consent mode: NO cuenta sesión/usuario/visitante si no aceptó cookies
- En España: ~40-60% de usuarios rechazan cookies (estimación de mercado)
- Implicación: GA4 puede infracontar tráfico real un 40-60%
- Si importas eventos GA4 a Google Ads → conversiones de usuarios sin consent son INVISIBLES

### Consent mode v2

- Obligatorio en EEE desde marzo 2024
- Dos tipos de señales: ad_storage y analytics_storage
- Sin consent: Google usa modeling para estimar conversiones (pero menos preciso)
- Enhanced conversions ayuda a compensar parcialmente

### Requisitos prácticos

1. Banner de cookies conforme a LOPD/GDPR (CMP certificado)
2. Consent mode v2 implementado en GTM
3. Registro actividades de tratamiento
4. Política de privacidad actualizada
5. Delegado de Protección de Datos (DPO) si aplica

### Soluciones para recuperar datos

1. **Enhanced conversions** (gratis) — match por email/teléfono
2. **Google Tag Gateway** (gratis con Cloudflare) — bypass ad blockers
3. **Server-side tagging** — captura datos antes de que consent mode los bloquee
4. **Microsoft Clarity** como tercer punto de datos para triangular discrepancias

## Google Tag Gateway setup

- Requiere: Google Tag Manager
- Cloudflare users: GTM → Admin → Google Tag Gateway → login Cloudflare → aprobar → listo (1 clic)
- Otros CDNs: soportado pero más configuración
- Cloudflare tier gratis es suficiente
- NO reemplaza server-side — solo addresses ad blockers/navegación privada

## Tracking operativo completo

### Métodos comunes no rastreados

| Método | Excusa típica | Impacto |
|---|---|---|
| Llamadas telefónicas | "No podemos rastrearlo" | 10-20% leads |
| Chat / live chat | "Sin integración premium" | 5-20% leads |
| Reservas calendario | "El tier premium cuesta €100/año" | 10-20% leads |
| Clicks email | "Solo miramos inbox" | 5-10% leads |
| WhatsApp | "No se puede trackear" | 10-30% leads en España |

### Fix
Trackear TODOS los métodos de conversión en tu web:
- Formularios web (standard)
- Teléfono +34 con call tracking (30-60s mínimo)
- Chat/chatbot
- Reservas calendario
- WhatsApp clicks (evento personalizado)
- Email clicks

El coste de trackear (€100/año calendario) es despreciable vs €20-50K/año en ads a ciegas.

## Cadena de reacción: tracking roto → Smart Bidding degrada

1. Tags se rompen (update web borra tag de conversión) — puede pasar desapercibido meses
2. Datos conversión a la mitad (ej: solo forms, no llamadas)
3. Smart Bidding optimiza señal parcial → pujas cambian en keywords que sí convertían
4. Tráfico de keywords cambia → peor calidad
5. Conversiones reales caen → espiral descendente

Cuanto más tiempo sin detectar → más daño compuesto.

## OCI — Offline Conversion Import

### Por qué importa para lead gen
- Tracking tradicional (forms, calls) = medición "front-end". Incluye spam
- OCI = medición "back-end". Solo reporta deals cerrados / leads cualificados
- Sin OCI: maximize conversions → Google busca leads baratos y spammy
- PMax sin OCI → "50/50 coin flip" éxito vs spam

### Cuándo invertir en OCI

| Situación | Recomendación |
|---|---|
| 1-2 conversiones form/día | Demasiado pronto (OCI reduciría a ~2-3/semana) |
| Escalando más allá de search (resistencia CPC) | Invertir en OCI ahora (necesario para PMax/AI Max/DG) |
| Search genera suficientes leads | OK sin OCI por ahora |
| PMax ya corriendo + spam | PARAR PMax → setup OCI → relanzar sobre OCI |

### Dos métodos

| Método | Cómo funciona | Uploads históricos | Complejidad |
|---|---|---|---|
| GCLID | Capturar click ID → almacenar en CRM → subir al cerrar deal | Sí (90 días) | CRM/form captura GCLID |
| Enhanced conversions for leads | Capturar email/tel → pass a thank-you → GTM → Google almacena → match al subir | No (solo desde inicio) | Form → thank-you → GTM setup |

### Cadencia upload
- **Mínimo semanal** — gaps más largos = Google sin datos para pujar
- **Ideal:** CRM con integración nativa Google Ads → push automático
- CRMs compatibles: Salesforce, HubSpot, Go High Level, WhatConverts
- **Evitar:** Google Sheets manual (error-prone, clientes nunca mantienen rutina)

### Ventana lookback 90 días
- Google solo mira 90 días hacia atrás
- Ciclos de venta >90 días: subir en etapa pipeline anterior
- Ejemplo: lead inmobiliario → cierre 6-12 meses → subir como "lead cualificado" con valor nominal

### Lead scoring — dos niveles

| Approach | Cómo | Impacto algoritmo |
|---|---|---|
| Custom columns only | Importar data CRM a columnas custom | Algoritmo sigue optimizando forms. TÚ ves data CRM |
| Full lead scoring | Asignar valores por etapa pipeline → feed back | Algoritmo optimiza CALIDAD, no volumen |

4 señales CRM para feed back:
1. Lead (form fill) — valor bajo
2. Lead cualificado — valor medio
3. Oportunidad — valor alto
4. Venta — valor máximo

### Micro-conversiones (cuentas bajo volumen)

Cuando conversiones primarias < 15/mes:
1. Identificar micro-conversiones (tour virtual, descarga, clic direcciones, video views)
2. Asignar valores proporcionales inversos (si cliente = €10K, 25 leads → 1 cliente, lead = €400, micro ~€50-100)
3. GA4 key events con valores → feed a Google Ads
4. Jerarquía: lead cualificado (max) → form fill (medio) → micro (bajo)

## Cross-platform: triangulación con Microsoft Clarity

- Cuando Google Ads clicks y GA4 traffic discrepan (común con privacy issues)
- Añadir Microsoft Clarity como 3er punto de datos (gratis)
- Comparar sesiones GA4 vs Google Ads vs Clarity
- La herramienta que difiere de las otras 2 = la que tiene tracking roto
- Se puede extraer GCLID de Clarity → validar atribución B2B en CRM

## Pixel duplicate firing

- Formularios que disparan pixel en cada cambio de estado (reschedules, cancelaciones)
- Ejemplo real: Facebook reportó 8 calls, Hyros mostró 2 (reschedules contados como nuevos)
- Fix: configurar pixel para disparar UNA VEZ por contacto
- Deduplicar a nivel CRM/web antes de disparar pixel
