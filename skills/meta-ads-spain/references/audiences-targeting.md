# Audiencias y Targeting — Meta Ads España

## Principio Andromeda: Creative = Targeting

En la era Andromeda, el creativo hace el targeting. Meta ya no segmenta por audiencias masivas — hace matching individual. Intereses y demographics son señales iniciales, no filtros.

## Árbol de Decisión

| Situación | Enfoque | Por qué |
|---|---|---|
| Pixel maduro (200+ conv) | **Broad** (zero interests, solo ubicación + edad) | Algoritmo conoce tu cliente mejor que stacks de intereses |
| Cuenta nueva, sin data | **Stacked broad interests** (3-4 intereses masivos, 20M-40M+) | Da al algoritmo señal inicial. Cambiar a broad tras 200+ conv |
| Broad falla tras 7 días + €400 | Testear 2-3 combinaciones de intereses | Algunos verticales necesitan dirección inicial |
| B2B con ICP muy específico | Stacked B2B interests + Value Rules | Broad puede derivar a consumidores. Intereses como guardrails |
| High-ticket (€5K+), <50 conv/mes | ABO con LALs de CRM seed (clientes/llamadas) | Precisión necesaria cuando datos son escasos y cada conversión es cara |

## Audiencia Broad

**Según Unnamed Marketing Coach:**
- La mejor para escalar. Zero interests, zero lookalikes, sin restricciones demográficas más allá de ubicación y edad básica
- El creativo hace el targeting (quién para de scrollear)
- Mínimo 100.000+ para entrega estable (retargeting puede ser menor)

## Stacked Broad Interests

**Según Unnamed Marketing Coach:**
- Agrupar 3-4 intereses masivos semi-relacionados en 1 ad set
- Ejemplo: Target + Walmart + Home Depot → audiencia 20M-40M+
- NO usar nichos estrechos
- Ideal para volumen inicial si broad falla inicialmente

## Custom Audience Stack (Retargeting/LAL hybrid)

**Según Unnamed Marketing Coach:**
- Combinar TODAS las custom audiences en 1 ad set:
  - Visitantes web
  - Engagers IG/FB
  - Video viewers
  - + Lookalike 1-5% de mejores clientes/leads
- Algoritmo optimiza entrega dentro del stack

## Lookalike Strategy

### Jerarquía calidad seeds

| Calidad | Fuente seed | Tamaño mínimo |
|---|---|---|
| 1 (mejor) | Clientes que pagan / deals cerrados | 1.000+ |
| 2 | Llamadas reservadas / leads cualificados | 1.000+ |
| 3 | Todos los leads / envíos formulario | 1.000+ |
| 4 | Visitantes web (páginas intent: pricing, demo) | 1.000+ |
| 5 (peor) | Engagers página/post | 1.000+ |

**Mínimo seed:** 1.000+ para LALs útiles. 5.000+ ideal. <200 = NO usar LALs, ir broad.

### Guía % LAL

| LAL % | Mejor para | Audiencia |
|---|---|---|
| 1% | Testing inicial, precisión | Más pequeña, mayor match |
| 1-3% | Escalar 1% tras saturación | Equilibrado |
| 3-5% | Escalado alto volumen | Broad, menos preciso |
| 5-10% | Raramente útil para lead gen | Esencialmente broad |

**Best practice:** stackear múltiples LALs 1-2% de seeds de alta calidad en 1 ad set > un único LAL 5%.

**Según Dr. Matt:** combinar hard limits (España, 25+) con Broad Lookalike Stack. Upload seeds de CRM: Stripe exports, llamadas reservadas, clientes. DMs de IG = calidad baja.

## Value Rules

**Según Dr. Matt:**
- NO excluir demographics en duro. Usar **Value Rules** para disminuir pujas 90% en segmentos no ideales
- Permite que Advantage+ AI encuentre excepciones
- Solo hard limits para: edad mínima, restricciones país/radio, constraints absolutos

## Advantage+ Audience Migration

Meta está deprecando targeting manual de intereses → Advantage+ Audience.

- **Intereses son "sugerencias"** — Meta los usa como señal inicial, luego expande
- **Impacto práctico:** menos control, pero mejores resultados si creativo es fuerte
- **Migración:** interests → broad con creativo fuerte. Test 80/20: 80% broad, 20% interest-guided
- **Lo que permanece:** ubicación, edad mínima, idioma, exclusiones custom audience = hard constraints

### Advantage Detailed Targeting
- **DESACTIVAR** para campañas prospecting B2B con audiencias tight → evita drift a consumidores irrelevantes
- **ACTIVAR** para campañas broad/scaling → deja que algoritmo encuentre más gente como converters
- NO clickar "further limit the reach of ads" salvo retargeting puro

## Retargeting por Ciclo de Venta

| Ciclo venta | Hot | Warm | Cool |
|---|---|---|---|
| <7 días (servicio local, impulso) | 1-3 días | 3-7 días | 7-14 días |
| 7-30 días (coaching B2C, info products) | 1-7 días | 7-14 días | 14-30 días |
| 30-90 días (B2B SaaS, consulting) | 1-14 días | 14-30 días | 30-60 días |
| 90+ días (enterprise, high-ticket) | 1-30 días | 30-60 días | 60-90 días |

Adaptar creativo por ventana:
- **Hot:** CTA directo, urgencia, oferta
- **Warm:** prueba social, testimonios, caso éxito
- **Cool:** nuevo ángulo, reintroducción, contenido valor

## Salud Custom Audiences

| Factor | Bien | Mal | Acción |
|---|---|---|---|
| Tamaño | >1.000 retargeting, >10.000 seeds prospecting | <500 | Expandir ventana (30→90 días) o combinar fuentes |
| Frescura | Auto-updating (pixel) o CRM <30 días | CRM subido hace 6+ meses | Refrescar o eliminar. Configurar sync CRM automático |
| Calidad fuente | Clientes, llamadas, leads cualificados | "Todos los visitantes" o page engagers | Usar fuente mejor calidad para LAL seeds |

## Separación Prospecting vs Re-engagement (Andromeda)

**Según Sam Piliero:** si mezclas audiencias frías y warm en la MISMA campaña sin restricciones bajo Andromeda:
- Algoritmo va a conversiones más fáciles (clientes conocidos/engagers)
- Pixel se entrena en comportamiento de ese cohorte
- En 30 días, limitas capacidad de AI para encontrar clientes nuevos

**Solución:** mantener Prospecting estrictamente separado de Re-engagement vía exclusiones de audiencia estructuradas.

## Categorías Especiales (SAC) — Workarounds

SAC aplica a: housing, credit, employment, social/political issues.

### Restricciones SAC

| Feature | Sin SAC | Con SAC |
|---|---|---|
| Segmentación edad | Cualquier rango | NO |
| Segmentación género | Masculino/femenino/todos | NO |
| Targeting código postal | Exacto | NO. Mínimo 15 millas radio |
| LALs | Standard (1-10%) | Solo Special Ad Audiences |
| Detailed targeting | Biblioteca completa | Restringido |
| Custom audiences | Completo | **SÍ funciona** — palanca principal |

### Workarounds dentro de SAC

1. **Custom Audiences (palanca principal):** retargeting visitantes, CRM uploads, engagement audiences → NO restringidos
2. **Broad + creativo fuerte:** dejar que creativo haga targeting. Texto del anuncio atrae público correcto naturalmente
3. **Special Ad Audiences:** similar a LALs pero menos precisos. Seed con mejor fuente: deals cerrados > leads cualificados
4. **Geo targeting (15 millas mínimo):** usar city-level o DMA. Para negocios locales: 15 millas desde ubicación
5. **Value Rules:** no puedes excluir demographics pero SÍ pujar diferente por señales

### Compliance copy por sector

**Housing/inmobiliaria:** ✅ "Explora viviendas en [Ciudad]" | ❌ "Perfecto para familias jóvenes" (implica edad/estado familiar)

**Crédito/finanzas:** ✅ "Compara opciones de préstamo" | ❌ "¿Mal crédito? Te ayudamos" (targeting por estado crediticio)

**Empleo:** ✅ "Únete a nuestro equipo" | ❌ "Perfecto para recién graduados" (proxy de edad)

### CPL en SAC
- CPL típicamente 20-40% más alto en verticales SAC por restricciones targeting
- Establecer expectativas con cliente desde el inicio
- Rechazos repetidos en SAC → escalación más rápida a restricciones cuenta
