# Tracking y Atribucion — X Ads Espana

## X Pixel — el basico obligatorio

### Que es

Tag de JavaScript que se instala en tu web para rastrear acciones de usuarios que llegan desde X Ads.

### Eventos disponibles

| Evento | Cuando disparar | Prioridad |
|---|---|---|
| **Page View** | Toda pagina (automatico) | Obligatorio |
| **View Content** | Pagina de servicio/producto clave | Alta |
| **Lead / Sign Up** | Formulario enviado, registro completado | **Critico** |
| **Add to Cart** | Inicio de proceso (solicitud, demo) | Media |
| **Purchase** | Conversion final (compra, contrato) | Alta |
| **Custom** | Clic WhatsApp, descarga PDF, clic telefono | Segun negocio |

### Instalacion via GTM

1. Crear tag de tipo "Custom HTML" en GTM
2. Pegar codigo base del X Pixel
3. Configurar triggers por evento (form submit, page view, etc.)
4. Publicar contenedor GTM
5. Verificar con X Pixel Helper (extension Chrome)

### Instalacion directa

1. Pegar codigo base del X Pixel en `<head>` de todas las paginas
2. Anadir eventos especificos en paginas de conversion
3. Verificar en X Ads Manager → Eventos → X Pixel

## Conversion API (CAPI) — recomendado para Espana

### Por que CAPI es critico en Espana

- **30-45% de conversiones se pierden** sin tracking server-side en 2026
- Espana: alta tasa de rechazo de cookies (GDPR + LOPD)
- Ad blockers prevalentes en audiencia tech (tu audiencia en X)
- ITP (Intelligent Tracking Prevention) en Safari/iOS reduce cookies a 7 dias

### Que es CAPI

Conexion **servidor-a-servidor** directa con X. No depende del navegador del usuario.

### Pixel vs CAPI

| Caracteristica | X Pixel | CAPI |
|---|---|---|
| Tipo | Client-side (navegador) | Server-side (servidor) |
| Afectado por ad blockers | Si | No |
| Afectado por consent opt-out | Si | Parcialmente |
| Afectado por ITP/cookies | Si | No |
| Latencia | Tiempo real | Tiempo real (via webhook) |
| Setup | Facil (tag JS) | Medio-Alto (API + servidor) |
| Coste | Gratis | Coste infra servidor |

### Setup CAPI

**Requisitos:**
- Acceso a X Ads API
- Developer Account en X
- Servidor o GTM Server-Side container

**Senales que enviar:**
- X Click ID (twclid) — **mas importante**, match directo
- Email address (hashed)
- Phone number (hashed, formato +34XXXXXXXXX)
- IP address
- User agent

**Implementacion via GTM Server-Side:**

1. Configurar GTM Server-Side container (Stape o Addingwell)
2. Instalar tag de X Conversion API en server container
3. Mapear eventos (Lead, Purchase, etc.)
4. Configurar deduplicacion con `conversion_id`
5. Verificar en X Ads Manager → Eventos

### Deduplicacion Pixel + CAPI

**Critico:** si usas ambos (recomendado), debes deduplicar para no contar doble.

- Usar **mismo `conversion_id`** en Pixel y CAPI para cada evento
- Deduplicacion ocurre a nivel de evento (mismo nombre + mismo conversion_id)
- Si no deduplicas: conversiones infladas → Smart Bidding optimiza mal

### Configuracion recomendada para Espana

```
Tier 1 (minimo): X Pixel solo
→ Pierdes 15-30% conversiones por ad blockers + cookies

Tier 2 (recomendado): X Pixel + CAPI (dual)
→ Maxima recuperacion con deduplicacion
→ Coste: ~€30-50/mes hosting GTM SS

Tier 3 (avanzado): Pixel + CAPI + Offline Conversion Import
→ Para negocios con ciclo de venta largo (B2B, inmobiliaria)
→ Subir conversiones offline via API
```

## GDPR + LOPD en Espana

### Requisitos legales

- **Consent banner obligatorio** antes de activar tracking
- **LOPD** (Ley Organica de Proteccion de Datos) refuerza GDPR en Espana
- Deber informar sobre uso de cookies publicitarias
- Derecho del usuario a rechazar → se pierde tracking

### Consent Mode

- Respetar la preferencia del usuario
- Si rechaza cookies: Pixel no dispara (normal)
- CAPI puede seguir enviando datos server-side (con limitaciones legales)
- **Consultar con abogado RGPD** para limites exactos de CAPI sin consentimiento

### Impacto en tracking

| Escenario | Conversiones rastreadas |
|---|---|
| Solo Pixel, consent aceptado | ~70-85% |
| Solo Pixel, consent rechazado | 0% |
| Pixel + CAPI, consent aceptado | ~95%+ |
| Pixel + CAPI, consent rechazado | ~40-60% (solo server-side) |

## Offline Conversion Import

### Para que sirve

Subir conversiones que ocurren offline (llamada que cierra, reunion que convierte) a X Ads para que el algoritmo aprenda.

### Como funciona

1. Capturar `twclid` (X Click ID) cuando usuario llega a tu web
2. Almacenar en CRM junto con datos del lead
3. Cuando el lead convierte (cierra venta, asiste a demo): subir a X via API
4. X atribuye la conversion al clic original

### Requisitos

- Acceso a X Ads API
- CRM que capture twclid (HubSpot, Salesforce, custom)
- Subir dentro de 90 dias del clic original
- Minimo semanal (idealmente diario) para que algoritmo aprenda

## Tracking operativo — no olvidar

Metodos de conversion que debes rastrear:

| Metodo | Como rastrear | Prioridad |
|---|---|---|
| Formularios web | Pixel event on submit | Critico |
| Clics WhatsApp | Pixel event on click | Alta (muy usado en Espana) |
| Llamadas | Call tracking (min 30s) | Alta |
| Reservas calendario | Pixel event on confirmation | Alta |
| Chat en vivo | Pixel event on message sent | Media |
| Descargas PDF/lead magnet | Pixel event on download | Media |
| Email | UTM tracking en GA4 | Baja |

**Cada metodo no rastreado = 5-15% senales perdidas → pujas automáticas degradan.**

## UTM parameters

Usar siempre en todos los enlaces:

```
?utm_source=x&utm_medium=paid&utm_campaign=[campana]&utm_content=[adgroup]&utm_term=[keyword]
```

Permite analisis en GA4 independiente de X Ads Manager.

## Verificacion de tracking

### Checklist post-instalacion

- [ ] X Pixel Helper muestra eventos disparando
- [ ] X Ads Manager → Eventos muestra actividad
- [ ] CAPI events aparecen en Ads Manager (si configurado)
- [ ] Conversiones de test llegan en <1h
- [ ] UTMs llegan a GA4 correctamente
- [ ] Deduplicacion Pixel/CAPI verificada (no conteo doble)
- [ ] Consent banner funciona y Pixel respeta preferencia
