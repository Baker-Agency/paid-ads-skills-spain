# Algoritmo Andromeda — Meta Ads

## Qué es

Algoritmo Meta (2025-2026) que cambia cómo se entregan anuncios. En vez de mostrar el mismo ad a millones, cada usuario recibe el anuncio más relevante basado en intereses y etapa de compra. **Matching individual**, no segmentación por audiencia masiva.

## Timeline

| Fecha | Evento |
|---|---|
| Dic 2024 | Artículo de ingenieros Meta anunciando desarrollo |
| Mar 2025 | Primeros cambios en cuentas seleccionadas |
| Jul 2025 | Rollout completo para todos los anunciantes |
| Sep 2025 | Primeros bugs y problemas graves plataforma |

## Stack Meta AI (4 componentes)

**Según Manel Gómez:**

| Componente | Rol |
|---|---|
| **GEM** (Generative Ads Recommendation Model) | Procesa datos masivos comportamiento usuario → predice qué ad es más relevante por usuario. Unifica IG + FB en un motor. Aprende de todo el ecosistema: orgánico + ads, texto + imagen + video + audio |
| **Lattice** | Ranking unificado — reemplaza muchos modelos pequeños. Comparte aprendizajes entre objetivos (campaña tráfico alimenta campaña purchase y viceversa). GEM vive dentro de Lattice. Lattice hace la **selección final** |
| **Andromeda** | Retrieval/delivery — de millones de ads candidatos, decide cuál mostrar en milisegundos |
| **Sequence Learning** | Trackea acciones antes y después de ver un ad. Permite secuenciación journey (post-purchase: productos complementarios en vez de repetir mismo producto) |

### Pipeline secuencial

**Según Dara Denney:**
1. **Andromeda** reduce millones de ads a pool más pequeño (retrieval)
2. **GEM** reduce pool usando insights profundos comportamiento usuario (recommendation)
3. **Lattice** hace selección final combinando todos los datos y outputs

## Advantage+ = Andromeda

**Según Sam Piliero:**
- El algoritmo Advantage Plus **ES** Andromeda
- Cualquier campaña/audiencia con Advantage+ ON → ya en Andromeda
- Advantage+ OFF + "further limit the reach of ads" → NO en Andromeda (hasta rollout completo)

## Por Qué Importa

### Creative diversity = palanca principal
- Paradigma anterior: "un ad ganador para todos" → podía escalar indefinidamente
- Paradigma Andromeda: "cada usuario recibe el ad más relevante"
- Sin diversidad creativa → frecuencia alta → audiencia reducida
- **Andromeda no subió el listón — quitó la red de seguridad.** Expone cuentas sin diversidad

### Velocidad
- Andromeda deprioritiza y reprioritiza cuentas MUCHO más rápido
- Pixels rotos, flags políticas, comentarios negativos → **deprioritización inmediata** (vs 1-2 semanas pre-Andromeda)
- Recovery de fixes también es más rápida

### Retargeting caveat
- Andromeda no aplica tan fuerte a retargeting/retention (audiencias tight, conocidas)
- Mayor valor = adquirir nuevos clientes net new a escala (prospecting)
- **PERO:** si mezclas cold y warm en misma campaña sin restricciones → algoritmo va a conversiones más fáciles (conocidos). Pixel se entrena en ese cohorte → limita capacidad encontrar nuevos
- **Mantener Prospecting estrictamente separado de Re-engagement**

## Signal y Trust

**Según Manel Gómez:**

### Signal
- Feedback comportamiento usuario al algoritmo POR creativo
- No solo conversiones/clics — incluye:
  - QUIÉN compra
  - QUIÉN clica
  - A qué velocidad (1h, 1d, 1 semana para convertir)
- Ayuda Meta a predecir si mostrar ad de nuevo → resultado valioso

### Trust
- Confianza de Meta en que el ad **REPETIRÁ** la misma señal en el tiempo
- Consistencia:
  - Mismo tipo usuario sigue respondiendo
  - Velocidad decisión consistente
  - Sin feedback negativo
- Trust se construye gradualmente — no se puede forzar

### Matriz Signal × Trust

| | Trust alto | Trust bajo |
|---|---|---|
| **Signal alto** | ✅ Escala sin problemas | ⚠️ Rendimiento errático |
| **Signal bajo** | 🔄 Rendimiento estable pero modesto | ❌ No escala |

### Cómo construir Signal
1. Volumen conversiones (>50 mínimo, >200 fuerte)
2. Datos backend alimentados (CAPI, offline conversions)
3. Creative que atrae al MISMO tipo usuario consistentemente
4. Instalar pixel temprano — Meta necesita masa crítica datos

### Cómo construir Trust
1. No hacer ediciones frecuentes (cada edición = reset parcial)
2. Mantener campaña estable (sin cambios bruscos presupuesto)
3. Landing page y oferta consistentes
4. Pixel limpio sin duplicados ni errores
5. Comentarios ads limpios (negativos matan trust)

## Datos Meta (Dic 2024)

**Según Ben Heath (citando artículo Meta):**

| Métrica | Resultado |
|---|---|
| ROAS de A+ Creative AI-driven targeting | **+22%** |
| Conversiones de image generation | **+7%** |
| Anunciantes usando gen AI tools | 1M+ |
| Ads generados AI por mes | 15M+ |

## Incremental Reach (métrica clave 2026)

**Según Manel Gómez:**
- ¿Cuántas personas alcanzadas este mes que NO alcanzamos el anterior?
- Crítico para diagnosticar si incrementos presupuesto alcanzan gente nueva o solo aumentan frecuencia sobre audiencia existente
- Si incremental reach bajo + presupuesto sube = estás pagando más por las mismas personas

## Demand Compression

**Según Manel Gómez:**
- Caídas ROAS 2025 = combinación Andromeda + demand compression + bugs plataforma
- No solo culpa de Andromeda
- Consumer Sentiment Index en mínimos 3 años → audiencia ready-to-buy se encoge → todos compiten por pool más pequeño

### Bugs plataforma (separados de Andromeda)
- Fake outbound clicks (100 link clicks → 20 LPV)
- Ad set gastando 90% budget diario en 1 hora
- Audiencias excluidas recibiendo 80% del presupuesto
- Errores publicación aleatorios

## Implicaciones para Gestión en España

### Lo que cambia
- Creative diversity ya no es "nice to have" → es **requisito para escalar**
- Estructura cuenta importa para flujo presupuesto, no rendimiento
- Testing constante de conceptos, hooks, formatos = obligatorio
- Monitorizar incremental reach, no solo CPL/ROAS

### Lo que no cambia
- ENCAC sigue siendo norte métrico
- Fundamentals (tracking, oferta, LP) siguen siendo base
- Speed to lead sigue siendo crítico
- WhatsApp sigue siendo canal #1 en España

### Producción creativa mínima (Andromeda)

| Nivel gasto | Ads nuevos/mes |
|---|---|
| <€5.000 | 5-10 (2 conceptos × 3-5 hooks) |
| €5.000-15.000 | 15-30 |
| €15.000-40.000 | 30-50 |
| €40.000+ | 50-100 (motor producción dedicado) |
