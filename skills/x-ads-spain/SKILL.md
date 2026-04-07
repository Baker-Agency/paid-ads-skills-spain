---
name: x-ads-spain
description: X (formerly Twitter) Ads campaign management for the Spanish market (Spain). Setup, optimize, scale, and audit X Ads campaigns for lead gen, SaaS, and services targeting Spain. Use when managing X Ads for Spanish clients, launching campaigns on X/Twitter in Spain, auditing X Ads accounts, optimizing pujas en X, creating promoted posts, managing keyword targeting, or adapting X Ads strategy for the Spanish/European market. Covers Promoted Ads, Vertical Video, Takeovers, X Amplify, Dynamic Product Ads, Collection Ads, conversion tracking with X Pixel and CAPI, and audience targeting for Spain.
---

# X (Twitter) Ads Espana — Skill de Gestion Completa

Gestion integral de X Ads para lead gen, SaaS y servicios en el mercado espanol. NO e-commerce.

**Todo el contenido esta adaptado al mercado espanol:** benchmarks en EUR, IVA 21%, LOPD/GDPR, estacionalidad espanola, copy en espanol.

## Quick Reference — Espana

| Metrica | Valor Espana |
|---|---|
| Audiencia publicitaria Espana | ~9,8M usuarios (nucleo activo ~6M) |
| Penetracion X en Espana | 38% poblacion |
| Perfil demografico | 61,7% hombres / 38,3% mujeres |
| Edad principal | 25-34 anos (38,5% audiencia) |
| Tiempo medio diario | 48 minutos |
| CPC medio (global) | $0,50-2,00 (€0,45-1,80) |
| CPM medio (global) | $2,09-3,11 (€1,90-2,80) |
| CTR medio promoted ads | 0,86%-3% |
| ROI medio X Ads | $2,70 por $1 invertido (~2,7x) |
| IVA | 21% (incluir en calculos de unit economics) |

---

## Fase 0: Evaluacion de Viabilidad

### X Ads vs otras plataformas — cuando tiene sentido

**Usar X Ads cuando:**
- Audiencia activa en conversaciones de actualidad, tecnologia, B2B, finanzas, politica
- Producto/servicio que se beneficia de contexto en tiempo real (eventos, lanzamientos, noticias)
- CPM bajo es prioridad (X = ~€1,90-2,80 vs Meta ~€2,30+)
- Lead gen B2B donde la audiencia es profesional/informada
- Quieres keyword targeting basado en conversaciones (unico de X)

**NO usar X Ads cuando:**
- Audiencia objetivo es +55 anos (baja presencia en X)
- Producto requiere alta segmentacion demografica granular (Meta es superior)
- No tienes capacidad de crear contenido tipo "conversacion nativa"
- Presupuesto < €500/mes (poca masa critica para optimizar)

### Framework CAC para X Ads (EUR)

1. **CPC medio × 100** = gasto por 100 clics
2. **Aplicar tasa de conversion** = leads de esos 100 clics
3. **Aplicar tasa de cierre** (lead → cliente) = clientes reales
4. **Gasto / clientes** = CAC

**Ejemplo (SaaS B2B, Espana):**

| Paso | Metrica | Valor |
|---|---|---|
| 1 | CPC × 100 | €1,50 × 100 = **€150** |
| 2 | CVR 2% | 2 leads |
| 3 | Tasa cierre 25% | 0,5 clientes |
| 4 | €150 / 0,5 | **CAC = €300** |

Incluir fee de gestion. Con volumen mayor, CPC baja a €0,50-0,80.

→ Detalle completo: [references/unit-economics-spain.md](./references/unit-economics-spain.md)

---

## Fase 1: Setup de Cuenta y Lanzamiento

### Requisitos previos

- Cuenta en [business.x.com](https://business.x.com)
- Autenticacion de dos factores activada
- Metodo de pago en EUR configurado
- X Pixel instalado ANTES de lanzar (minimo 24-48h de datos)

### Arquitectura de cuenta

- **Estructura:** Cuenta → Campanas → Grupos de anuncios → Anuncios
- **Nomenclatura:** `Objetivo_Audiencia_Region_Fecha` (ej: `LeadGen_B2B_Madrid_202604`)
- **Empezar con 1 campana, 2-3 grupos de anuncios** con audiencias distintas
- **3-5 variaciones creativas** por grupo de anuncios para A/B testing

### Checklist de settings para Espana

- [ ] Objetivo alineado con funnel (Awareness/Consideration/Conversion)
- [ ] Ubicacion: **Espana** (o CC.AA. especificas si presupuesto lo permite)
- [ ] Idioma: Espanol
- [ ] Dispositivos: Todos (80%+ usuarios son mobile)
- [ ] Presupuesto diario (empezar €20-50/dia minimo para datos)
- [ ] Puja automatica al inicio (dejar que el algoritmo aprenda)
- [ ] X Pixel verificado y disparando correctamente
- [ ] Modo "Simple" para principiantes, "Avanzado" para control total

### Modos de campana

| Modo | Control | Recomendado para |
|---|---|---|
| **Simple** | Reach, Engagement, Traffic, Keywords | Primeras campanas, testing rapido |
| **Avanzado** | Awareness, Consideration, Conversion | Control total de pujas y optimizacion |

→ Detalle completo: [references/campaign-setup-checklist.md](./references/campaign-setup-checklist.md)

---

## Fase 2: Formatos de Anuncio

### Formatos disponibles

| Formato | Descripcion | Mejor para |
|---|---|---|
| **Promoted Ads (Imagen)** | Post con imagen + copy + CTA | Lead gen, trafico web |
| **Promoted Ads (Video)** | Post con video + copy + CTA | Brand awareness, engagement |
| **Promoted Ads (Carousel)** | Hasta 6 tarjetas (imagen o video) | Mostrar multiples servicios/beneficios |
| **Promoted Ads (Texto)** | Solo texto, aspecto organico | Autenticidad, bajo coste |
| **Vertical Video** | Pantalla completa 9:16, sonido on | Engagement maximo (7x mas engagement) |
| **X Amplify** | Pre-roll antes de contenido premium | Brand awareness contexto premium |
| **Takeover (Timeline)** | Primer anuncio al abrir app | Lanzamientos, eventos |
| **Takeover (Trend)** | Junto a trending topics | Branding masivo |
| **Collection Ads** | Hero + thumbnails multiples | Varios servicios/planes |
| **Dynamic Product Ads** | Retargeting automatico | Retargeting visitantes web |

### Especificaciones tecnicas clave

**Imagen:**
- Tamano recomendado: 1200×1200px (1:1) o 1200×628px (1.91:1)
- Max 3MB (imagen unica), 20MB (multi-imagen)

**Video:**
- 1280×720px (16:9) o 720×720px (1:1)
- MP4 o MOV, max 1GB (recomendado <30MB)
- Duracion: 6-15 segundos optimo (max 140s)
- **Hook en primeros 3 segundos obligatorio**
- Subtitulos siempre (80%+ ven sin sonido)

**Vertical Video:**
- 1080×1920px (9:16)
- 6-15 segundos optimo
- **Formato de mayor crecimiento en X** — 20% del tiempo diario de usuarios

**Carousel:**
- 2-6 tarjetas
- Mismo aspect ratio en todo el carousel (1.91:1 o 1:1)
- Puede mezclar imagen y video

**Copy:**
- 280 caracteres max (23 caracteres reservados por cada enlace)
- **Recomendado: <100 caracteres** para maxima visibilidad

→ Detalle completo: [references/ad-formats-specs.md](./references/ad-formats-specs.md)

---

## Fase 3: Targeting y Audiencias

### Opciones de segmentacion

| Tipo | Descripcion | Uso en Espana |
|---|---|---|
| **Demografico** | Edad, genero, idioma, ubicacion | Base: Espana, 25-54, espanol |
| **Keywords** | Terminos que usuarios buscan, publican o interactuan | **Diferenciador clave de X** — segmentar por conversacion |
| **Intereses** | 350+ categorias predefinidas (25 categorias principales) | Tecnologia, finanzas, salud, negocios |
| **Conversation topics** | Temas de conversacion activos | Eventos, tendencias, lanzamientos |
| **Follower look-alikes** | Usuarios similares a seguidores de otra cuenta | Competidores, influencers del sector |
| **Tailored audiences** | Listas propias (email, telefono, user IDs) | Retargeting CRM, clientes existentes |
| **Website visitors** | Via X Pixel | Retargeting visitantes web |
| **Dispositivo** | Tipo, SO, modelo | Filtrar por iOS/Android si relevante |

### Keyword targeting — la joya de X Ads

**Unico en X:** puedes segmentar por lo que la gente DICE, no solo por quien es.

- Targetear keywords que usuarios han buscado, tuiteado o con las que han interactuado
- Soporta **negative keywords** para excluir terminos irrelevantes
- Combinar con intereses para audiencias hiper-relevantes

**Ejemplo para lead gen en Espana:**
- Keywords positivas: "busco CRM", "software gestion", "automatizar ventas", "herramienta marketing"
- Keywords negativas: "gratis", "crack", "tutorial", "curso", "empleo"

### Exclusion targeting

- Excluir clientes existentes (tailored audiences)
- Excluir competidores
- Excluir intereses irrelevantes
- **Critico para eficiencia de presupuesto**

### AI-Optimized Targeting

X tiene targeting optimizado por IA que muestra anuncios mas alla de la segmentacion manual cuando predice mayor probabilidad de conversion. Activar despues de tener datos de conversion suficientes.

→ Detalle completo: [references/targeting-audiences.md](./references/targeting-audiences.md)

---

## Fase 4: Estrategia de Pujas y Presupuesto

### Estrategias de puja

| Estrategia | Descripcion | Cuando usar |
|---|---|---|
| **Automatica** | X optimiza pujas para maximizar acciones | Inicio — fase de aprendizaje |
| **Puja maxima (Manual)** | Tu defines cap por accion | Control de costes, campanas maduras |
| **Puja objetivo (Target)** | Defines coste medio por accion deseado | Cuando tienes benchmark de CPA claro |

### Progresion recomendada

```
Automatica (0-30 dias) → Puja objetivo (30+ dias con datos) → Manual (optimizacion fina)
```

**Regla:** dejar campanas 3-7 dias antes de cualquier cambio de puja.

### Modelos de facturacion

| Modelo | Se paga por | Mejor para |
|---|---|---|
| CPE (Cost per Engagement) | Like, RT, respuesta, clic en perfil | Engagement/awareness |
| CPC (Cost per Click) | Clic en enlace | Trafico web, lead gen |
| CPF (Cost per Follow) | Nuevo seguidor | Crecimiento audiencia |
| CPV (Cost per View) | Vista de video (2s+ o 50%+) | Campanas video |
| CPM (Cost per Mille) | 1.000 impresiones | Brand awareness masivo |
| CPA (Cost per Action) | Conversion (registro, descarga, lead) | Lead gen, SaaS signups |

### Presupuesto recomendado para Espana

| Nivel | Presupuesto mensual | Uso |
|---|---|---|
| Testing | €500-1.000 | Validar audiencia y creativos |
| Escala inicial | €1.000-3.000 | Lead gen activo, 2-3 campanas |
| Escala media | €3.000-10.000 | Multi-campana, retargeting, video |
| Enterprise | €10.000+ | Takeovers, full-funnel, multi-formato |

→ Detalle completo: [references/bidding-budget.md](./references/bidding-budget.md)

---

## Fase 5: Copy y Creativos (Mercado Espanol)

### Principio fundamental: nativo > publicitario

El contenido que parece un tweet organico supera al que parece anuncio. **"Si parece un anuncio, pierde."**

### Framework de copy para X Espana

**Estructura ganadora (< 100 caracteres):**
1. **Gancho:** pregunta o afirmacion provocativa
2. **Beneficio:** resultado concreto
3. **CTA:** accion unica y clara

**Ejemplo lead gen SaaS:**
> ¿Sigues gestionando leads con Excel?
> Automatiza tu pipeline y cierra 3x mas.
> Prueba gratis →

### Tu vs Usted en X Espana

| Sector | Tratamiento | Ejemplo |
|---|---|---|
| Tech/SaaS | Tu | "Automatiza tu negocio en 5 min" |
| Startup/coaching | Tu | "Escala tu agencia sin quemar equipo" |
| Finanzas/legal | Usted | "Solicite su consultoria gratuita" |
| B2B enterprise | Usted | "Descubra como reducir costes un 40%" |
| Salud/clinicas | Tu (web) | "Reserva tu cita sin esperas" |
| Educacion/cursos | Tu | "Aprende a invertir desde cero" |

### Formatos de copy con mejor rendimiento

1. **Tweet-style nativo:** Texto plano que parece post organico. CPL mas bajo
2. **Screenshot de tweet:** Captura de tweet real como imagen. Social proof autentico
3. **Hilo promocionado:** Thread con valor → CTA al final. Engagement alto
4. **Pregunta directa:** "¿Cuanto pagas por lead?" Genera respuestas y engagement
5. **Dato impactante:** "El 73% de las pymes espanolas no automatiza su marketing." Autoridad

### Triggers emocionales mercado espanol

- **Ahorro:** "Ahorra hasta un 40% en..."
- **Urgencia temporal:** "Solo esta semana" / "Ultimas plazas"
- **Prueba social:** "Mas de 500 empresas en Espana ya lo usan"
- **Miedo a perderse:** "Tus competidores ya lo tienen"
- **Resultado concreto:** "De 0 a 50 leads/mes en 60 dias"

→ Detalle completo: [references/spanish-ad-copy.md](./references/spanish-ad-copy.md)

---

## Fase 6: Cadencia de Optimizacion

### Primeros 7 dias: SOLO monitorizar

| Dia | Accion |
|---|---|
| 1-2 | ¿Pixel disparando? ¿Anuncios aprobados? ¿Se gasta presupuesto? |
| 3-7 | Revisar CTR por creativo. Pausar creativos con CTR < 0,5%. UNICA optimizacion permitida |

**NO tocar pujas, presupuestos ni targeting la primera semana.**

### Cadencia post-lanzamiento

| Frecuencia | Accion |
|---|---|
| **Diaria** | Check anomalias (¿campanas activas? ¿desaprobaciones? ¿gasto normal?) — NO optimizar |
| **Semanal** | CTR por creativo, coste por resultado, pacing de presupuesto. Pausar creativos perdedores |
| **Quincenal** | Revisar audiencias: ¿cual convierte mejor? Reasignar presupuesto |
| **Mensual** | Refresh creativos (fatiga creativa es rapida en X). Revisar keyword targeting |
| **Trimestral** | Auditar estructura completa, revisar estacionalidad, actualizar listas de exclusion |

### Cuando preocuparse

- **1 dia malo:** ruido normal. No tocar
- **3 dias consecutivos malos:** investigar (tracking roto, anuncios rechazados, audiencia agotada)
- **1-2 semanas de caida:** optimizar con datos reales — cambiar creativos, ajustar targeting

### Jerarquia de optimizacion (en orden)

1. **Creativos** — en X, el creativo es el targeting. Cambiar copy/visual primero (MAS IMPACTO)
2. **Targeting** — keywords, intereses, exclusiones, audiencias
3. **Presupuesto** — mover dinero a campanas ganadoras
4. **Pujas** — ajustar solo con volumen base conseguido (ULTIMO RECURSO)

→ Detalle completo: [references/optimization-cadence.md](./references/optimization-cadence.md)

---

## Fase 7: Escalado

### Escalado vertical (profundizar)

Cuando una campana funciona:

1. Aumentar presupuesto **20% cada 3-5 dias** (no duplicar de golpe)
2. Anadir variaciones creativas que mantengan el angulo ganador
3. Expandir keywords relacionadas con el tema ganador
4. Crear lookalike audiences desde los mejores converters

### Escalado horizontal (expandir)

Cuando Search/Timeline Impression Share es estable:

1. **Nuevos formatos:** si funciona imagen → probar video → probar vertical video
2. **Nuevas audiencias:** follower look-alikes de cuentas complementarias
3. **Nuevos objetivos:** si awareness funciona → probar conversion directa
4. **Retargeting:** website visitors + engaged users (people who interacted with tus ads)

### Secuencia de escalado recomendada

```
Promoted Ads (texto/imagen) → Video Ads → Vertical Video → Carousel → Amplify → Takeover
```

### Diversificacion de formatos

- **5-10% del gasto total** como presupuesto de testing para nuevos formatos
- Prerequisito: ya rentable en promoted ads basicos
- Vertical Video: **formato de mayor crecimiento** — 7x mas engagement, 20% mas ventas

→ Detalle completo: [references/scaling-framework.md](./references/scaling-framework.md)

---

## Fase 8: Tracking y Atribucion

### X Pixel — obligatorio

**Instalar ANTES de lanzar campanas.** Sin pixel, Smart Bidding no tiene senal.

**Eventos a configurar:**
- Page View (basico)
- Lead/Signup (formulario enviado)
- Content View (pagina clave vista)
- Add to Cart / Start Trial (si aplica)
- Purchase/Conversion (cierre)

### Tiers de tracking

| Tier | Que hace | Coste | Recuperacion |
|---|---|---|---|
| X Pixel (browser) | Tracking client-side basico | Gratis | Baseline — pierde 15-30% por ad blockers |
| X Pixel + Enhanced | Match con datos first-party (email, telefono) | Gratis | Recupera ~5-10% |
| Conversion API (CAPI) | Server-to-server, bypassa ad blockers | Setup tecnico | Recupera 15-30% adicional |
| Pixel + CAPI (dual) | Maxima cobertura con deduplicacion | Setup tecnico | **Recomendado** — recuperacion completa |

### Conversion API (CAPI) — setup

- Conexion servidor-a-servidor directa con X
- Funciona incluso con ad blockers, ITP, y opt-outs de cookies
- **Senales:** X Click ID, email, telefono, IP, user agent
- **Deduplicacion:** usar mismo `conversion_id` en Pixel y CAPI para evitar conteo doble
- Requiere acceso a X Ads API + Developer Account
- Implementable via GTM Server-Side (Stape, Addingwell)

### GDPR + LOPD en Espana

- Espana tiene **tasa alta de rechazo de cookies** → Pixel pierde mas datos que otros mercados
- LOPD refuerza GDPR con requisitos adicionales
- **Solucion minima:** Pixel + CAPI (dual tracking)
- Consent Mode: respetar preferencias del usuario pero maximizar senales server-side
- **30-45% de conversiones pueden perderse** sin tracking server-side en 2026

### Tracking operativo completo

Rastrear **TODOS** los metodos de conversion:
- Formularios web
- Clics en enlace a WhatsApp
- Llamadas (+34 XXX XXX XXX)
- Reservas de calendario
- Descargas de lead magnets
- Signups / free trials

Cada metodo no rastreado = senales perdidas → optimizacion de pujas degrada.

→ Detalle completo: [references/tracking-spain.md](./references/tracking-spain.md)

---

## Fase 9: Auditoria de Cuentas

### Orden de auditoria (top-down)

1. **Tracking** — ¿Pixel + CAPI funcionando? ¿Eventos correctos?
2. **Settings de cuenta** — ubicacion, idioma, modo avanzado
3. **Estructura de campanas** — ¿objetivos correctos por campana?
4. **Grupos de anuncios** — ¿audiencias diferenciadas? ¿sin overlap?
5. **Creativos** — ¿frescos? ¿formato nativo? ¿A/B testing activo?
6. **Targeting** — ¿keywords relevantes? ¿exclusiones configuradas?

### Red flags inmediatos

- [ ] Sin X Pixel instalado
- [ ] CAPI no configurado (perdiendo 15-30% senales)
- [ ] Sin negative keywords en keyword targeting
- [ ] Creativos con mas de 30 dias sin refresh
- [ ] Targeting demasiado amplio sin exclusiones
- [ ] Modo Simple en campanas maduras (deberia ser Avanzado)
- [ ] Sin retargeting de website visitors activo
- [ ] Presupuesto distribuido equitativamente (deberia favorecer ganadores)

→ Detalle completo: [references/audit-checklist.md](./references/audit-checklist.md)

---

## Mercado Espanol — Particularidades

### Audiencia X en Espana

- **9,8M usuarios** alcance publicitario (~6M activos diarios)
- **4a red social mas usada** en Espana (46,7% usuarios activos)
- **Perfil:** 61,7% hombres, 38,3% mujeres
- **Edad dominante:** 25-34 (38,5%), seguido 18-24 (32,1%)
- **Uso principal:** noticias, tendencias, conversacion publica, tech, finanzas, deportes
- **Tiempo medio:** 48 minutos/dia

### Sectores con mejor rendimiento en X Espana

| Sector | Por que funciona | CPL estimado |
|---|---|---|
| SaaS / Tech B2B | Audiencia tech-savvy, decision-makers activos | €15-50 |
| Finanzas / Inversiones | Comunidad activa finanzas espanolas (FinTwit) | €20-60 |
| Formacion / Infoproductos | Audiencia busca conocimiento, engagement alto | €5-20 |
| Servicios profesionales | B2B targeting efectivo via keywords | €20-80 |
| Eventos / Conferencias | Tiempo real = perfect fit | €3-15 |

### Estacionalidad Espana en X

| Periodo | Impacto en X | Accion |
|---|---|---|
| Enero (post-rebajas) | Propositos nuevo ano. Engagement alto | Buenos para SaaS, formacion, fitness |
| Febrero-Marzo | Pre-Semana Santa. Estable | Normal |
| Semana Santa | Menos actividad | Reducir presupuesto 20% |
| Abril-Junio | Estable, buen rendimiento | Periodo optimo para testing |
| Julio | Pre-vacaciones | Ultima ventana antes de agosto |
| **Agosto** | **Caida fuerte** — vacaciones masivas | **Reducir presupuesto 30-50%** |
| Septiembre | Vuelta fuerte | Aumentar presupuesto, lanzar campanas nuevas |
| Octubre-Noviembre | Pico actividad pre-Black Friday | Preparar desde octubre |
| Diciembre | Navidad, fin de ano | Maximo engagement, alto CPM |

### Comportamiento del usuario espanol en X

- **Conversacion > consumo pasivo:** espanoles interactuan mas que media europea
- **Horario pico:** 9:00-10:00, 13:00-15:00, 21:00-23:00 CET
- **Temas trending:** futbol, politica, tech, actualidad — oportunidad para newsjacking
- **WhatsApp como CTA:** incluir enlace directo a WhatsApp funciona mejor que formulario para ciertos sectores
- **Sensibilidad al precio:** ofertas de entrada (€29-99) convierten mejor en X que precios altos directos

→ Detalle completo: [references/spain-market-guide.md](./references/spain-market-guide.md)

---

## Diagnostico y Troubleshooting

### Zero conversiones (orden de diagnostico)

1. **Pixel/CAPI roto** — verificar que dispara correctamente (causa mas comun)
2. **Audiencia equivocada** — revisar keywords y segmentacion. ¿Llegan los clics correctos?
3. **Creative fatigue** — CTR cayendo = audiencia ya vio el anuncio demasiadas veces
4. **Landing page** — solo revisar si pasos 1-3 estan perfectos. ¿Alineada con el anuncio?

### CPL alto — 5 factores

| Factor | Diagnostico |
|---|---|
| CPC subio | Competencia estacional, audiencia agotada |
| CTR bajo | Creativo no resuena, copy debil, formato incorrecto |
| CVR landing bajo | LP no alineada con anuncio, formulario largo, carga lenta |
| Targeting amplio | Demasiados intereses sin exclusiones, keywords genericas |
| Sin retargeting | Perdiendo conversiones de usuarios warm |

### Fatiga creativa — la plaga de X

X tiene **ciclo de fatiga creativa mas corto** que Meta o Google:
- **7-14 dias** para creativos de alto rendimiento
- **3-7 dias** en audiencias pequenas
- **Solucion:** rotar 5-8 creativos activos, refresh quincenal

→ Detalle completo: [references/diagnostics.md](./references/diagnostics.md)

---

## Automatizacion

### X Ads API

- API completa para gestion programatica de campanas
- Crear, pausar, ajustar campanas via codigo
- Reportes automatizados
- Integrable con plataformas de terceros

### Integraciones utiles

| Herramienta | Funcion |
|---|---|
| **GTM Server-Side** | CAPI tracking sin dependencia del navegador |
| **Stape / Addingwell** | Facilitadores de GTM SS para X CAPI |
| **Zapier / Make** | Automatizar leads a CRM |
| **HubSpot / Salesforce** | Sincronizar leads de X con pipeline de ventas |
| **Tweet Hunter** | Crear creativos estilo tweet autentico |
| **Gamma AI** | Carouseles visuales rapidos desde texto |

### Reglas automaticas (en X Ads Manager)

- Pausar campanas si CPA > umbral definido
- Aumentar presupuesto si CTR > benchmark
- Notificaciones de rendimiento anomalo

---

## Referencias

| Archivo | Contenido |
|---|---|
| [unit-economics-spain.md](./references/unit-economics-spain.md) | CAC, ROI, IVA 21%, viabilidad |
| [campaign-setup-checklist.md](./references/campaign-setup-checklist.md) | Setup paso a paso Espana |
| [ad-formats-specs.md](./references/ad-formats-specs.md) | Formatos y especificaciones tecnicas |
| [targeting-audiences.md](./references/targeting-audiences.md) | Segmentacion, keywords, audiencias |
| [bidding-budget.md](./references/bidding-budget.md) | Pujas, presupuestos, facturacion |
| [spanish-ad-copy.md](./references/spanish-ad-copy.md) | Copy en espanol, tu vs usted |
| [optimization-cadence.md](./references/optimization-cadence.md) | Cadencia optimizacion |
| [scaling-framework.md](./references/scaling-framework.md) | Escalado vertical/horizontal |
| [tracking-spain.md](./references/tracking-spain.md) | Pixel, CAPI, GDPR/LOPD |
| [audit-checklist.md](./references/audit-checklist.md) | Auditoria cuentas espanolas |
| [spain-market-guide.md](./references/spain-market-guide.md) | Guia mercado espanol |
| [diagnostics.md](./references/diagnostics.md) | Troubleshooting completo |
