# Scaling Framework — Reddit Ads España

## Decision Gates (Cuándo Escalar)

| Señal | Acción | NO escalar si |
|---|---|---|
| CPA < target 14+ días consecutivos | Budget +20-30% | CPA volátil (>30% swings diarios) |
| Utilización >95% consistente | Campaña capped → aumentar | Utilización alta por audiencia tiny (<50K) |
| Pool retargeting creciendo W/W | Funnel sano → más prospecting | Pool encogiendo → fix tracking/prospecting |
| Nuevos subreddits identificados (Reddit Pro) | Expandir targeting | Ya targeting todos los relevantes |
| Win rate creativo >30% (3/10 nuevos beat baseline) | Pipeline soporta escala | <10% → resolver creative primero |
| CRM confirma calidad leads estable/mejorando | Calidad se mantiene | MQL→SQL rate cayendo → calidad degradando |
| LTV:CAC ratio >3:1 | Unit economics soportan | <2:1 → fix monetización antes de escalar |

## Reglas de Budget

- **Aumentar 20-30% cada 5-7 días** (más conservador que Meta — Reddit tiene subastas más pequeñas)
- **Nunca >50% de golpe**
- Si CPA sube >30% tras aumento → revertir al budget anterior 5 días, luego +15%
- Monitorizar 7 días tras cada aumento antes de decidir next move
- Más allá de **15x CPA diario por ad group** → dividir en paralelos con targeting diferente

## 4 Caminos de Escalado

| Camino | Qué | Cuándo | Ganancia esperada | Riesgo |
|---|---|---|---|---|
| **Vertical** | Más budget a winners | CPA bajo target, utilización capped | 20-40% más conv | Diminishing returns ~15x CPA |
| **Horizontal** | Nuevos subreddit clusters, keywords, interests, geos | Targeting actual performing pero capped | 30-50% más conv | Nuevas audiencias necesitan 2-3 semanas validación |
| **Funnel** | Añadir retargeting, mid-funnel, brand awareness | Funnel single-stage maxed out | 15-30% mejora CPA blended | Más complejidad gestión |
| **Formato** | Test free-form si solo imagen, test vídeo, test lead gen forms | Formatos actuales saturando | 10-25% reach incremental | Coste producción creativa sube |

**Regla consenso:** Escalar in place. NO "graduar" winners de testing a campañas scaling — cambio contexto mata performance. Aumentar budget directamente en ad group performing.

## Equilibrio Natural

Tras meses 2-3, CPA tiende a estabilizar en "equilibrio natural" por dinámicas de subasta.

**Si CPA se estanca, NO luchar contra el precio. Cambiar los inputs:**

| # | Estrategia | Mecanismo | Impacto esperado |
|---|---|---|---|
| 1 | Mejores ads | Mejorar CTR → menor CPC efectivo | 10-30% reducción CPA |
| 2 | Mejor post-click | Mejorar CVR → menor CPL de mismos clics | 20-50% reducción CPL |
| 3 | Nuevas audiencias | Escapar equilibrio fijo → diferentes dinámicas | Nuevo volumen a potencialmente menor CPA |
| 4 | Mejor oferta | Mejorar calidad lead → menor CPQL | 15-40% reducción CPQL |
| 5 | CRM feedback loop | Mejorar señal algoritmo → encuentra mejores usuarios | 10-25% reducción CPA en 30-60 días |
| 6 | Nuevos productos | Diferentes audiencias, value props | Pool volumen totalmente nuevo |

## "Diminishing Returns Are Still Returns"

- En apex: €1M revenue al 40% margen = €400K profit
- Escalado past apex: €5M revenue al 20% margen = **€1M profit (2,5x más)**
- La mayoría de advertisers paran en el apex. La segunda mitad de la curva sigue siendo masivamente profitable

## LTV como Moat de Escalado

| LTV:CAC Ratio | Veredicto | Acción |
|---|---|---|
| <1:1 | Perdiendo dinero por cliente | Stop adquisición. Fix pricing/retención |
| 1:1-2:1 | Insostenible | Reducir CAC o aumentar retención |
| 2:1-3:1 | Supervivencia. Margen error thin | Optimizar agresivamente |
| 3:1-5:1 | Sano. Mínimo para escalar cómodo | **Escalar metódicamente** |
| 5:1+ | Preferido. Funded customer acquisition | **Escalar agresivamente** |
| 10:1+ | Potencialmente bajo-invirtiendo | Aumentar gasto |

## 3-Phase Lifecycle (adaptado Reddit)

| Fase | Objetivo | Tácticas Reddit | Avanzar cuando |
|---|---|---|---|
| **1. Crear flujo** | Llenar pipeline. Volumen > calidad | Ofertas baja fricción. Subreddits amplios. Lowest Cost. Free-form text. 3-5 campos form max | 50+ leads/mes |
| **2. Monetizar** | Aumentar revenue por cliente | Email nurture post-lead, upsells. Optimizar MQLs. CRM feedback loop | 70-80% capacidad. MQL→SQL >25% |
| **3. Añadir fricción** | Mejorar calidad a costa de volumen | Qualifying fields en form. Subreddits estrechos. Optimizar SQL/revenue vía CAPI | Flujo estable + monetización OK |

**NO saltar a Fase 3.** Lanzar con forms largos, cualificación estricta y targeting estrecho = zero volumen = zero datos = zero aprendizaje.

## R&D Budget

| Gasto mensual | R&D % | Budget experimental | Ejemplos |
|---|---|---|---|
| €3-5K | 5% (€150-250) | 1 test/mes | 1 nuevo subreddit cluster o 1 nuevo formato |
| €5-15K | 10% (€500-1.500) | 2-3 tests/mes | Nuevo formato + nueva audiencia + nuevo ángulo |
| €15-50K | 15% (€2.250-7.500) | 4-6 tests/mes | Nuevos verticals, vídeo, LP tests, CAPI optimization |
| €50K+ | 20% (€10K+) | Programa testing estructurado | Campañas testing dedicadas, nuevos modelos funnel |

## Consideraciones España para Escalado

### Limitaciones Audiencia

- Pool total usuarios Reddit en España significativamente menor que US/UK
- **Techo de escala** más bajo: probable saturación antes
- Monitorizar frequency de cerca — audiencias más pequeñas saturan más rápido
- Considerar expandir a subreddits en inglés con targeting geo España

### Estacionalidad

| Período | Impacto | Acción |
|---|---|---|
| Enero (post-Navidad) | Recuperación. Nuevos presupuestos | Buen momento para lanzar |
| Semana Santa | Variable por sector | Monitorizar |
| Agosto | **Bajón fuerte** — vacaciones masivas | Reducir budget 30-50% |
| Septiembre | Recuperación fuerte ("vuelta al cole") | Preparar campañas antes |
| Black Friday/Navidad | Competencia ads sube, CPMs más altos | Aumentar budget si unit economics aguantan |

### Expansión Cross-Border

- Si producto/servicio es international → expandir geo targeting a LATAM (México, Argentina, Colombia)
- Subreddits en español cubren todo Hispanoamérica
- Diferentes unit economics por país (CPCs potencialmente menores en LATAM)
