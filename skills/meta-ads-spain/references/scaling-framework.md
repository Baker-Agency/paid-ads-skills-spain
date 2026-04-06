# Escalado — Meta Ads España

## Regla del 20%

Incrementos presupuesto diario del **20% máximo** = umbral seguro para no resetear learning phase.

- Aplicar vía regla automatizada (1×/día, solo si CPA bajo target 3 días consecutivos)
- Incrementos mayores → learning phase reset → 1-2 semanas rendimiento inestable
- Excepción: si campaña gasta <50% del presupuesto asignado, puedes subir más agresivo (el algoritmo ya no gasta todo)

## Fases de Escalado

### Fase 1: Validación (€40-80/día)

**Objetivo:** encontrar 1 ángulo ganador
- 5 campañas ABO, cada una = 1 concepto
- Múltiples hooks por concepto
- Presupuesto: €40-50 por ad set
- Criterio avance: CPL bajo target después de €200+ gasto en el ad set

### Fase 2: Proof (€150-200/día)

**Objetivo:** confirmar que el ganador se mantiene
- Duplicar ganadores con **post ID** a 4× presupuesto
- Usar post ID preserva social proof (comments, likes)
- Mínimo 48-72h antes de evaluar
- Criterio avance: rendimiento estable 3+ días

### Fase 3: Scale inicial (€400-800/día)

**Objetivo:** CBO con ads probados
- 3-5 ads probados en CBO
- Usar bid caps si CPL sube al escalar
- Dayparting: concentrar gasto en horas conversión (España: 9-14h + 16-21h)
- Criterio avance: ENCAC estable

### Fase 4: Scale agresivo (€800-8.000+/día)

**Objetivo:** portfolio diversificado
- Portfolio: múltiples CBOs por persona/concepto
- Diversificación bid strategy (Lowest Cost + Cost Cap + Bid Cap)
- Motor producción creativa activo (50-100 ads/mes)
- Monitorizar reach incremental: ¿cuántas personas alcanzadas este mes que NO alcanzamos el anterior?

## ENCAC: Norte Métrico

```
ENCAC = Gasto total ads (todas plataformas) / Nuevos clientes totales (del CRM)
```

### Por qué ENCAC, no CPA in-platform

- Meta se auto-reporta y sobreatribuye
- Con 3% CTR, 97% personas no se pueden trackear por clics
- Porción grande de conversiones son modeladas (iOS opt-outs, ad blockers)
- CAPI puede dar falsa sensación de seguridad
- **Fuente de verdad = CRM/backend, no reporting plataforma**

### Regla de escalado con ENCAC

| Métrica | Evaluación |
|---|---|
| CPA in-platform sube €800→€900 al escalar | OK — ignorar |
| ENCAC sube €50→€55 al escalar | OK — controlable, repetible |
| ENCAC se mantiene estable al subir gasto | **ESCALAR** |
| ENCAC sube >15-20% al escalar | Pausar escalado, investigar |

### Calcular mensualmente

Comparar ENCAC vs Meta-reported CAC:
- Si Meta-CAC << ENCAC: Meta sobreatribuye (común con view-through). Reducir view-through attribution
- Si Meta-CAC >> ENCAC: otros canales canibalizan crédito (raro)

## Signal & Trust (Andromeda)

**Según Manel Gómez:**

Dos conceptos que determinan si un creativo puede escalar bajo Andromeda:

### Signal
- Feedback comportamiento usuario por creativo
- No solo conversiones/clics — incluye QUIÉN compra, QUIÉN clica, y a qué velocidad (1h, 1d, 1 semana para convertir)
- Ayuda a Meta a predecir si mostrar el anuncio de nuevo lleva a resultado valioso

### Trust
- Confianza de Meta en que el anuncio REPETIRÁ la misma señal en el tiempo
- Consistencia: mismo tipo usuario responde, velocidad decisión consistente, sin feedback negativo
- Trust se construye gradualmente — no se puede forzar

### Matriz Signal × Trust

| | Trust alto | Trust bajo |
|---|---|---|
| **Signal alto** | ✅ Escala sin problemas | ⚠️ Rendimiento errático |
| **Signal bajo** | 🔄 Rendimiento estable pero modesto | ❌ No escala |

### Cómo construir Signal
- Volumen conversiones (>50 = mínimo, >200 = fuerte)
- Datos backend alimentados (CAPI, offline conversions)
- Creative que atrae al MISMO tipo de usuario consistentemente

### Cómo construir Trust
- No hacer ediciones frecuentes
- Mantener campaña estable (sin cambios bruscos)
- Landing page y oferta consistentes
- Pixel limpio sin duplicados ni errores

## Creative Scaling

### Escalado por buyer persona

**Según Savannah Sanchez:**
- Escalar = testing diverso por persona y motivador emocional
- Diferentes estilos visuales (lo-fi UGC vs alta producción) = targeting a nivel de ad
- No buscar "bala mágica" — diversificar ángulos

### Cadencia producción para escalado

| Nivel gasto/mes | Ads nuevos/mes | Foco |
|---|---|---|
| <€5.000 | 5-10 | 1-2 conceptos × 3-5 hooks |
| €5.000-15.000 | 15-30 | 3-5 conceptos × 3-5 hooks + iteraciones |
| €15.000-40.000 | 30-50 | Testing continuo + iteraciones ganadores |
| €40.000+ | 50-100 | Motor producción creativa dedicado |

### Iteración de ganadores

**Según Savannah Sanchez:**
1. Variaciones hook visual (mismo creator + mensajes, diferente visual hook)
2. Swap creator (mismo guión, diferente persona)
3. Tests edición (mezclar secuencia clips, condensar 30s → 15s)
4. Cross-platform: testear concepto ganador en todos los formatos (feed, stories, reels)

## Organic to Paid

**Según Blake Driver:**
- Capitalizar presencia orgánica fuerte
- **Retargeting:** campañas dedicadas retargetando engagers orgánicos (video views, interacciones)
- **Top orgánico como ads:** convertir contenido orgánico top en anuncios
- **Post IDs:** correr posts orgánicos usando post ID en vez de recrear → aprovecha social proof existente

## Escalado Horizontal (Multi-canal)

Cuando Meta está saturado (frecuencia sube, ENCAC sube):
1. Google Ads (search intent) — complementa Meta (demand gen)
2. YouTube — visual como Meta pero intent diferente
3. TikTok — audiencia joven, formato similar a Reels
4. LinkedIn — B2B específico

**Regla:** dominar 1 canal antes de diversificar. 5-10% presupuesto para testing nuevos canales.

## Trampas Comunes Escalado España

| Trampa | Fix |
|---|---|
| Escalar en agosto | NO. Bajón vacaciones. Escalar sept-nov o ene-jun |
| Subir presupuesto >20% de golpe | Incrementos 20% diarios máximo |
| Escalar sin CAPI | Instalar CAPI primero. Sin datos → scaling a ciegas |
| Escalar con 1 solo creativo | Diversificar antes de escalar. 5+ conceptos mínimo |
| Ignorar ENCAC | CPA in-platform ≠ realidad. Siempre verificar con CRM |
| Escalar con spend limit olvidado | Revisar Account Settings antes de cualquier escalado |
