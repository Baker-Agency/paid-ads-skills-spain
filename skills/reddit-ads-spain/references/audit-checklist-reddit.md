# Audit Checklist — Reddit Ads España

## Orden de Auditoría (Top-Down)

1. Tracking de conversiones
2. Estructura de cuenta
3. Targeting
4. Creativos
5. Pujas y presupuesto
6. Landing pages
7. Competencia
8. Compliance

## 1. Tracking

| Check | Bien | Mal | Acción |
|---|---|---|---|
| Pixel en todas las páginas | Pixel Helper green en cada página | Falta en páginas clave | Añadir pixel a todas las páginas/templates |
| Eventos conversión | Lead/SignUp disparando correctamente | Sin eventos o disparando en página equivocada | Configurar eventos, verificar triggers |
| UTMs | 5 UTMs + rdt_cid presentes en URL final | UTMs faltantes o stripeados por redirects | Fix UTM template, verificar redirect chain |
| CAPI | EMQ >6,0, eventos fluyendo | Sin CAPI o EMQ <4,0 | Implementar server-side tracking |
| CRM integration | Leads aparecen <24h con source "reddit" | Sin leads Reddit en CRM | Check form fields, CRM mapping |
| Consent mode (LOPD) | Pixel respeta consentimiento, banner OK | Pixel dispara sin consentimiento | Implementar OneTrust/Cookiebot |

## 2. Estructura Cuenta

| Check | Bien | Mal | Acción |
|---|---|---|---|
| Campañas vs budget | Cada campaña >€28/día | Campañas con <€14/día | Consolidar. Mín €28/día |
| Objetivo alineado | Conversiones para lead gen | Lead gen en "Brand Awareness" | Reconstruir con objetivo correcto |
| Funnel separado | Prospecting y retargeting en campañas distintas | Mezclados | Separar inmediatamente |
| Naming conventions | Estructurado: `[TIPO] - [AUDIENCIA] - [DEVICE] - [FECHA]` | "Campaign 1", "test new" | Implementar convención |
| Budget distribution | 60-70% prosp, 20-30% RTG, 10% testing | >50% RTG (pool pequeño) o 0% RTG | Rebalancear |
| Duplicados | Zero overlap entre campañas | Campañas compitiendo mismos subreddits | Merge duplicados |
| Ad groups/campaña | 3-8 por campaña | 1 (sin segmentación) o 15+ (fragmentado) | Consolidar a 3-8 |
| Ads/ad group | 3-6 activos | 1 (sin testing) o 10+ (diluidos) | Target 3-6 |

## 3. Targeting

| Check | Bien | Mal | Acción |
|---|---|---|---|
| Relevancia subreddits | Score avg >3,5 | Targeting subreddits irrelevantes | Reemplazar con Reddit Pro research |
| Interest breadth | 3-8 categorías relacionadas | >15 (broad) o 1 (narrow) | Ajustar a 3-8 high-relevance |
| Keyword quality | Keywords específicos product/solution | Keywords genéricos ("business", "software") | Rebuild desde Reddit Pro trends |
| Custom audience freshness | Lists <90 días, pixel refreshing diario | List 12+ meses, sin pixel audiences | Re-upload CRM quarterly |
| 6 exclusiones | Todas presentes | Missing >2 | Implementar todas inmediatamente |
| Geo alineado | Targeting match mercado serviceable | Targeting países sin presencia | Restringir a geos serviceable |
| Device split | Ambos devices, data para optimizar | Todo en mobile para B2B | Desktop-only RTG para B2B |
| Audience overlap | <20% entre ad groups | >40% — campañas compitiendo | Reestructurar targeting |

## 4. Creativos — Scoring Natividad

| Señal | 1 (Malo) | 3 (OK) | 5 (Bueno) |
|---|---|---|---|
| **Tono** | Jerga corporativa, nota prensa | Profesional pero rígido | Conversacional, suena como Redditor |
| **Headline** | "Transforma Tu Negocio" | "Reduce Costes CRM 40%" | "Cambié de Salesforce el mes pasado — esto pasó" |
| **Social proof** | Zero | Claims sin especificidad | "4,8/5 en G2 de 2.300 reviews" |
| **Visual** | Stock photo + logo | Gráfico custom branded | Screenshot-style, meme, free-form text |
| **CTA** | "¡Compra Ahora!" | "Saber Más" | "Link en comentarios" |
| **Comments** | Desactivados o negativos | Mixto | Discusión positiva, marca respondiendo |

**Scoring:**
- 25-30: Excelente
- 18-24: Buena base, probar variantes
- <18: Overhaul necesario

### Format Utilization

| Formato | ¿Usando? | CTR | CVR | Veredicto |
|---|---|---|---|---|
| Free-form text | [ ] | ___ | ___ | **Obligatorio para B2B** |
| Imagen | [ ] | ___ | ___ | Standard, siempre testear |
| Vídeo | [ ] | ___ | ___ | Awareness/retargeting |
| Carousel | [ ] | ___ | ___ | Multi-feature showcase |

**Red flag:** Solo 1 formato → Reddit recompensa diversidad formato.

### Fatiga

- CTR declinando >15% en 3 semanas consecutivas = fatigado
- Frequency >4x en 7 días (prosp) = demasiado
- CPM subiendo >20% W/W sin cambios subasta = creativo perdiendo relevancia

### Message Match

| Check | Ad dice | LP dice | ¿Match? |
|---|---|---|---|
| Headline promise | ___ | ___ | [ ] |
| Oferta/CTA | ___ | ___ | [ ] |
| Tono/voz | ___ | ___ | [ ] |
| Visual continuidad | ___ | ___ | [ ] |
| Social proof referenciado | ___ | ___ | [ ] |

Mismatch = CVR cae 20-50%.

## 5. Pujas y Presupuesto

| Estrategia | Cuándo correcta | Cuándo incorrecta | Cómo evaluar |
|---|---|---|---|
| Lowest Cost | Nueva, learning, <50 conv/sem | CPA volátil inaceptable | CPA trend 14 días. OK si ≤1,3x target |
| Cost Cap | Madura, 50+ conv/sem | Nueva (<2 sem), datos insuficientes | Utilización >80%. Si <50% → cap demasiado bajo |
| Manual CPC | RTG pequeñas, control estricto | Prospecting a escala | Impression share y utilización budget |

### Utilización Budget

| Nivel | Diagnóstico | Acción |
|---|---|---|
| >95% | Capped — dejando impresiones | +20-30% si CPA OK |
| 80-95% | Sano | Monitorizar |
| 50-80% | Underspending | Check audiencia >50K, bid competitiveness, approvals |
| <50% | Severely underspending | Broaden targeting o subir Cost Cap 25-50% |

## 6. Competitor Intelligence

### Reddit Ad Library

1. ads.reddit.com/library → buscar competidor
2. Filtrar últimos 90 días
3. Para cada ad: formato, copy, CTA, LP URL, duración activa, subreddits, engagement
4. Score natividad cada ad (1-5)
5. Identificar gaps: ¿qué ángulos/ofertas NO están corriendo?

### Reddit Pro Monitoring

- Monitorizar top 5 competidores
- Track volumen menciones, sentimiento, trending topics
- Sentiment score avg <0 = vulnerabilidad a explotar en messaging

## 7. Compliance

| Check | Red Flag | Acción |
|---|---|---|
| Ads rechazados | >10% rechazados, mismo ad rechazado múltiples veces | Revisar Reddit ad policies |
| Categorías restringidas | Cliente en categoría restringida sin disclaimers | Aplicar whitelist, añadir disclaimers |
| Community guidelines | Marca respondiendo agresivamente a negativos, astroturfing | Entrenar en etiqueta Reddit |
| Inventory type | "Expanded" (muestra en NSFW) | Cambiar a **Standard** |
| GDPR/LOPD | Pixel sin consent, sin cookie banner | Implementar consent management |

## Red / Orange / Green Triage

### RED — Fix Inmediatamente (0-7 días)

- Pixel no firing
- Sin eventos conversión
- Objetivo campaña equivocado
- Sin exclusiones
- RTG con <100 usuarios pool
- Todos ads rechazados
- LP rota o >5s carga
- CRM integration rota
- UTMs stripeados por redirects

### ORANGE — Fix Este Mes (7-30 días)

- Solo 1 formato ad (falta free-form text)
- Sin subreddit-level targeting
- Creative score <18/30
- Cost Cap demasiado bajo
- Sin A/B testing structure
- Sin CAPI
- RTG mezclado con prospecting
- Sin dayparting analysis tras 30+ días
- Naming conventions inconsistentes

### GREEN — Optimizar Ongoing (30-90 días)

- Bid strategy testing avanzado
- Subreddit expansion vía Reddit Pro
- Creative testing cadence mensual
- LP A/B testing program
- CRM feedback loop activation
- Cross-platform attribution analysis
- Device segmentation
- Placement optimization
- Quarterly competitive refresh
