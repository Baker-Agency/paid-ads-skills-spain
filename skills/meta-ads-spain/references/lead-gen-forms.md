# Lead Generation — Formularios y Estrategias Meta Ads España

## Formularios Instantáneos — Configuración

### Settings críticos

**Consenso (Ben Heath, Matt Shiver, Ryan Pineda):**

| Setting | Valor | Por qué |
|---|---|---|
| Tipo formulario | **Higher Intent** | Desbloquea verificación OTP |
| Verificación SMS (OTP) | **ACTIVAR** | Filtra números falsos y leads baja intención |
| Autofill | **DESACTIVAR** | Forzar entrada manual = datos precisos y actuales |
| Sharing | **"Open"** | Permite compartir el ad orgánicamente |

### Orden de campos

**Según Ryan Pineda:**
1. Nombre (separado de Apellidos → evita problemas mapping CRM)
2. Apellidos
3. Email
4. Teléfono

Preguntas fáciles primero. No pedir crédito, ingresos exactos, estado civil en formulario (triggers SAC en finanzas/hipotecas).

### Framing del formulario

- NO es un formulario genérico de captación
- Framear como **cualificador**: "Descubre si cualificas para reducir tu pago mensual"
- Body: "Pedimos esta información para no hacerte perder el tiempo"
- Establece expectativas y aumenta intent percibido

### Campos a evitar (compliance)

En sectores finanzas/hipotecas:
- ❌ Credit score / puntuación crédito
- ❌ Dirección exacta
- ❌ Ingresos exactos
- ❌ Timeline compra
- ✅ Recoger esta info DESPUÉS via Messenger/WhatsApp/llamada

## Routing Post-Formulario (Two-Step)

**Consenso (Ben Heath, Matt Shiver, Ryan Pineda):**

Usar pantalla de confirmación/revisión para dirigir a acción secundaria inmediata.

### Opciones de routing (orden recomendado para España)

| Canal | Por qué | Cuándo usar |
|---|---|---|
| **WhatsApp** | 96% penetración España. Canal preferido | Default para España |
| **Messenger** | Dentro del ecosistema Meta | Backup si WhatsApp no viable |
| **Calendario** | Reserva directa | Servicios con agenda (clínicas, coaching) |
| **Llamada** | Contacto inmediato | Urgencia (legal, emergencias) |

**Según Ryan Pineda:**
- CTA post-submit: "Escríbenos por WhatsApp" / "Envíanos un mensaje por Facebook"
- **Bridging the data gap:** si no pudiste preguntar algo en formulario (compliance), recógelo en WhatsApp/Messenger DESPUÉS

### Cuándo abandonar forms

Si tu nicho requiere cualificación pesada (crédito detallado, encuestas multi-paso que violan políticas Meta) → mover a landing page.

Instant Forms = para testing rápido de volumen y captura simple.

## Optimizar por Purchases (no Leads)

### El problema

**Según Charley T (Disruptor School) / Meta MBA grad Tikis:**
- Optimizar por "Leads" o "Schedules" → CPLs baratos pero leads no se presentan
- Algoritmo encuentra "rellenadores de formularios" y "clickeadores de calendario", no compradores
- CPL bajo + 0 ventas = peor que CPL alto + ventas

### La solución: objetivo Purchases

- Cambiar objetivo campaña a **Purchases**
- Crear evento conversión personalizado para transacción real
  - Ejemplo: cargo tarjeta tras llamada exitosa
  - Ejemplo: pago consulta después de reserva
- Alimentar este purchase event a Meta

### Implementación

1. Definir qué cuenta como "purchase" en tu embudo (pago real, no booking)
2. Configurar evento custom en pixel/CAPI
3. Cambiar optimization event del ad set a este evento
4. Esperar 1 semana completa antes de evaluar impacto

### Resultados esperados
- CPL puede parecer diferente inicialmente
- Show rates suben drásticamente
- Calidad leads mejora sustancialmente
- Revenue bottom-line sube
- Caso: cuenta escalada a $1M/mes con menor gasto en ads

## Estrategia Pixel "Engaged Lead"

**Según Dylan Bradley:**

### Problema
Evento genérico "Lead" = cualquiera que envía formulario. Meta optimiza para envío de formulario, no intención.

### Solución: evento "Engaged Lead"
- Dispara SOLO cuando usuario toma acción de alta intención post-envío
- Ejemplo: clic en link del primer email de confirmación → visita VSL o página reserva
- Solo quienes realmente están interesados completan este paso adicional

### Implementación
1. Hardcodear evento custom "engaged_lead" en pixel
2. O crear custom conversion basada en page views desde link del email
3. Configurar optimización del ad set a este evento `engaged_lead`

### Nivel avanzado: Purchase Optimization para leads
- Tratar leads cualificados como purchases
- Asignar al engaged/qualified lead un valor = Average Lead Value (ALV)
- Configurar optimización campaña a Purchases
- Fuerza al algoritmo a abandonar form-fillers y buscar compradores
- Resultado: CAC verdadero significativamente menor pese a CPL más alto

## Offline Conversion Tracking

### Vía Zapier (más accesible)

**Según Charley T (Disruptor School):**
- Asignar valores a leads desde respuestas del funnel
- Enviar eventos "good lead" / "great lead" custom a Facebook con valores en EUR
- Asignar valor menor a leads malos/descalificados (no omitirlos — ayuda al algoritmo)
- Optimizar por Complete Registration en funnels de descalificación

### Speed to lead — España

| Tiempo respuesta | Impacto |
|---|---|
| <5 minutos | Best practice. Tasa contacto máxima |
| 5-30 minutos | Aceptable. Cada minuto cuenta |
| >1 hora | Leads decaen rápidamente |
| >24 horas | Lead prácticamente perdido |

En España: integrar respuesta automática WhatsApp + llamada manual <5 min = combo ideal.

## Advantage+ Leads

### Qué es
Tipo campaña Meta para lead gen con mayor automatización (audience, placements, creative optimization).

### Cuándo usar vs manual

| Factor | Advantage+ Leads | Lead Gen manual |
|---|---|---|
| Data pixel | Fuerte (500+ conv/mes) | Nuevo o <50 conv/mes |
| Control audiencia necesario | Bajo (broad funciona) | Alto (B2B, SAC) |
| Volumen creativos | 10+ diversos | <5 |
| Presupuesto | €80+/día | Cualquiera |

### Limitaciones
- Menos control targeting
- Requiere diversidad creativa
- Reporting más agregado
- **NO usar en SAC** (controles limitados conflictan)
- Siempre campaña manual paralela (10-20% presupuesto) para comparación
- Monitorizar calidad leads de cerca — Advantage+ optimiza por volumen por defecto

### Setup
1. Empezar con campañas Lead Gen manuales
2. Mover a Advantage+ Leads SOLO tras encontrar creativo + oferta probados
3. Mantener manual corriendo en paralelo
