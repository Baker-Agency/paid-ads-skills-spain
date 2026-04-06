# Checklist de Setup de Campañas — España

## Pre-lanzamiento

### Cuenta nueva
- Crear cuenta con zona horaria Madrid (CET/CEST)
- Moneda: EUR
- Vincular GA4
- Auto-tagging: activar
- Auto-apply recommendations: DESACTIVAR

### Tracking (antes de activar campañas)
- Google Ads conversion tag directa (mejor que importar desde GA4)
- Enhanced conversions: activar (gratis, recupera ~5% conversiones)
- Google Tag Gateway (si usas Cloudflare → setup 1 clic)
- Conversión counting: "Una" para lead gen
- Call tracking: configurar con duración mínima 30-60s, formato +34
- Verificar disparo correcto con Tag Assistant

## Estructura de campaña

### Minimalismo estructural
- Empezar con 1 campaña, 1 grupo de anuncios
- Solo crear campañas separadas cuando hay razón válida:
  - Presupuestos diferentes
  - Ubicaciones diferentes
  - Audiencias completamente distintas
  - Objetivos de conversión diferentes
- NO separar por dispositivo (fragmenta datos de Smart Bidding)

### Naming convention recomendada
```
[País]_[Tipo]_[Servicio]_[Match]_[Audiencia]
ES_Search_Dental_Exact_Madrid
ES_PMax_Clinica_AllAssets
ES_DemandGen_Coaching_Remarketing
```

### Grupos de anuncios
- Agrupar por tema de intención, NO por keyword individual (SKAGs muertos)
- 2-5 grupos de anuncios al inicio
- Cada grupo = un tema semántico coherente
- Broad match: incluir múltiples keywords en el grupo para dar contexto al algoritmo

## Settings de campaña (España)

### Obligatorios
- [ ] Objetivo: "Leads" (o "Sin objetivo" para B2B con control total)
- [ ] Red de Display: DESACTIVAR
- [ ] Search Partners: DESACTIVAR al inicio
- [ ] Location: "Presencia" only (NO "Presencia o interés")
- [ ] Idioma: Español
- [ ] Moneda: EUR
- [ ] Auto-applied recommendations: DESACTIVAR

### Recomendados
- [ ] Programación: Lun-Vie 9:00-21:00 CET (ajustar según sector)
  - España tiene horario partido: 9-14 + 16-21
  - Fines de semana: reducir presupuesto 50-75% (salvo turismo/ocio)
- [ ] Audiencias: 20-30 segmentos en modo "Observación" (no restringe, solo datos)
- [ ] Assets automáticos: DESACTIVAR al inicio
- [ ] Desktop only: considerar para B2B high-ticket (móvil = research, no compra)

### B2B específico
- Crear campaña "Sin objetivo" para evitar auto-broadening
- Desktop only para high ACV
- Empezar con Manual CPC o Maximize Clicks con bid cap
- 15-20 conversiones/mes antes de Smart Bidding

## Keywords

### Match types por presupuesto
| Presupuesto | Match type | Razón |
|---|---|---|
| <€1.000/mes | Exacto | Control total, presupuesto limitado |
| €1.000-3.000/mes | Exacto + frase | Algo de expansión controlada |
| €3.000-10.000/mes | Exacto + broad | Broad con datos suficientes |
| >€10.000/mes | Broad predominante | 50+ conversiones, señales completas |

### Inserción dinámica de keywords (DKI)
- Usar en headlines de match exacto
- Formato: {KeyWord:Texto por defecto}
- NO usar con broad match (mostraría search terms irrelevantes)

### 3 listas de negativas (crear ANTES de activar)

**Lista 1 — Términos basura (español):**
gratis, gratuito, curso, cursos, empleo, trabajo, sueldo, salario, becas, prácticas, oposiciones, wikipedia, youtube, reddit, pdf, qué es, cómo hacer, cómo se hace, tutorial, plantilla, ejemplo, definición, significado, precio (a veces), barato

**Lista 2 — Competidores:**
[Nombres de marcas competidoras] — evitar canibalización en campañas genéricas

**Lista 3 — Marca propia:**
[Tu marca y variaciones] — aislar en campaña de marca separada

## RSA (Responsive Search Ads)

### Mínimo por grupo de anuncios
- 3 variaciones de anuncio con copy diferente
- 10+ headlines (hasta 15), 4 long headlines, 4 descriptions

### Framework de pinning
| Posición | Pin | Contenido |
|---|---|---|
| H1 | Pin 1 | Intención del usuario (keyword/problema) |
| H2 | Pin 2 | Diferenciador (por qué tú, no competencia) |
| H3 | Pin 3 | CTA claro (Pide presupuesto, Reserva cita, etc.) |

### Ad Strength
- IGNORAR completamente
- No correlaciona con Ad Rank ni CPA
- Ads con "Poor" routinariamente superan a "Excellent"

## Extensions/Assets

### Mínimo recomendado
- Sitelinks: 4+ (servicios principales, contacto, sobre nosotros, casos)
- Callouts: 4+ (envío gratis, sin compromiso, presupuesto en 24h)
- Structured snippets: tipos de servicio
- Call extension: +34 XXX XXX XXX
- Location extension: si negocio local (vincular Google Business Profile)
- Image extensions: logo + fotos servicio

## Conversiones

### Setup para lead gen
- Acción primaria: formulario completado
- Acción primaria: llamada 30-60s mínimo
- Acción secundaria (observe): click en WhatsApp, descarga PDF
- Counting: "Una" (no "Todas")
- Ventana conversión: 30 días click, 1 día view

### Micro-conversiones (cuentas bajo volumen)
Cuando conversiones primarias < 15/mes:
1. Identificar micro-conversiones upstream (visita virtual, descarga brochure, clic direcciones)
2. Asignar valores proporcionales (si cliente = €10K, necesitas 25 leads → lead value = €400, micro ~€50-100)
3. Configurar como key events en GA4 con valores
4. Jerarquía: lead cualificado (máximo valor) → micro-conversiones (menor)

## Post-lanzamiento inmediato

### Día 0 (verificación)
- [ ] Anuncios aprobados y elegibles
- [ ] Tags de conversión disparando (verificar con Tag Assistant)
- [ ] Presupuesto gastándose
- [ ] Previews de anuncios correctas
- [ ] Landing pages cargando correctamente y rápido (<3s)
- [ ] Teléfono +34 correcto y contesta

### Día 1-7 (solo monitorizar)
- NO optimizar pujas ni presupuestos
- Revisar search terms diario → añadir negativas
- Verificar mínimo 10 clics/día
- Check CTR tras 50-100 clics (objetivo >2%)
