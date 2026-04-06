# Quality Score — Deep Dive

## Impacto en CPC

- QS 1 paga hasta **10x más** que QS 10
- QS es multiplicador del CPC: mismo Ad Rank, QS más alto = CPC más bajo
- Diferencia del 50% en CPC entre puntuaciones
- Mejora QS = **20-30% ahorro en CPC** (Enrique del Valle)

### Techo realista
- QS 7-8 para non-brand = realista y bueno
- QS 10 solo en brand (intención perfecta)
- QS 9-10 en non-brand = excepcional, no esperarlo

### Priorización
- Arreglar QS 1-3 primero → mayor ROI de mejora (de pagar 10x a pagar 3x)
- QS 4-6 → mejora moderada
- QS 7-8 → fine-tuning, menor impacto marginal
- NO obsesionarse con subir de 8 a 10

## 3 Componentes

| Componente | Peso relativo | Qué mide |
|---|---|---|
| Expected CTR | Alto | ¿Usuarios clickan tu anuncio para esta keyword? |
| Ad Relevance | Medio | ¿Tu anuncio es relevante para la keyword? |
| Landing Page Experience | Medio | ¿Tu LP es relevante, rápida y útil? |

### Cómo mejorar cada uno

**Expected CTR:**
- Mejorar headlines (más específicos, incluir keyword)
- Negativizar terms irrelevantes (scripts de negativas = más eficaz)
- Eliminar impresiones con CTR bajo → CTR promedio sube

**Ad Relevance:**
- Alineación keyword → ad copy (trinidad coherente)
- DKI (Dynamic Keyword Insertion) en headlines exactos
- Temas de keywords coherentes en ad group

**Landing Page Experience:**
- Velocidad: target <2 segundos carga
- Relevancia: LP debe coincidir con intención del keyword
- Contenido útil y original
- Mobile-friendly
- HTTPS obligatorio

## QS en Interfaz vs QS Real

### El problema (Enrique del Valle)
- QS en interfaz Google Ads solo refleja ~1% de queries
- Solo muestra QS donde search term = keyword exactamente
- El otro 99% de queries (variaciones broad match) tiene QS oculto individual
- Cada search term tiene su propio QS detrás
- Implicación: puedes tener QS 7 visible pero QS 3 real en la mayoría de tráfico

### Actualización QS
- Rolling window de 90 días
- No se actualiza instantáneamente
- Cambios en LP o ads tardan semanas en reflejarse en QS visible

## Scripts de Negativas y QS

- Smart Bidding ahorra 100% en bad clicks (evita subastas)
- PERO no filtra search terms irrelevantes que SÍ muestran anuncios
- Scripts de negativas complementan: eliminan impresiones con CTR bajo
- Menos impresiones irrelevantes → CTR promedio sube → Expected CTR mejora → QS sube
- Es un ciclo virtuoso: scripts → menos basura → mejor QS → CPCs más bajos

## Broad Match y QS

- Con broad match, cada search term tiene su QS individual (oculto)
- QS interfaz es misleading para campañas broad match
- No confundir QS visible (keyword-level) con rendimiento real (query-level)
- Mejorar LP relevancia = impacta TODOS los QS ocultos simultáneamente

## Caso de Estudio

- Cuenta con QS promedio 4 → optimización LP + ads + negativas
- Tras 3 meses: QS promedio subió a 7
- CPCs bajaron ~25%
- Misma posición, mismo gasto → más clics → más conversiones
- ROI de la optimización QS pagó los 3 meses de trabajo
