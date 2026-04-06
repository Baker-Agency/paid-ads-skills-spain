# Framework de Escalado

## Dos Tipos de Escalado

### 1. Escalado Vertical (Segmentación)
Cuando el presupuesto se concentra en 20-30% (a veces 40%) de keywords/productos top y el resto no recibe gasto.

**Proceso:**
1. Exportar search terms → pedir n-gram analysis a Gemini o usar 8020 Agent
2. Identificar keywords "sidekick" que convierten pero no reciben gasto
3. Mover sidekicks a campañas dedicadas propias para forzar entrega de presupuesto
4. No tocar la campaña original que funciona

**Por qué funciona:** Google concentra gasto en lo que conoce. Sin campañas separadas, los sidekicks nunca reciben presupuesto suficiente para escalar.

### 2. Escalado Horizontal (Bridging the Intent Gap)
Cuando bottom-of-funnel impression share topa (>60% Search IS o Click Share).

**Proceso:**
1. Expandir a keywords de resolución de problemas / beneficios (en vez de producto exacto)
2. Alcanzar tráfico más frío con YouTube, Demand Gen, GDN
3. Añadir PMax sobre search exhaustado para gasto adicional rentable

## Triggers de Escalado

| Señal | Acción |
|---|---|
| Search IS > 60% | Iniciar escalado horizontal (nuevos canales) |
| CPC resistance (+15% presupuesto → +25-30% CPCs) | Investigar antes: ¿hay sidekicks sin gasto? Si sí → vertical primero |
| Presupuesto consistentemente infrautilizado | Expandir keywords o audiencias |
| CPA estable 4+ semanas | Safe to increase budget 15-20% |
| 30+ conversiones/mes estables | Ready for tCPA/tROAS |

## Secuencia de Escalado Recomendada

```
Search (exact) → Search (broad) → RLSA/DSA → PMax (con OCI) → Demand Gen → YouTube CPM/CPV
```

### Notas por etapa
- **Search exact → broad:** cuando IS > 60% en exact, 50+ conversiones, datos suficientes
- **RLSA:** remarketing en search — solo viable con alto tráfico web
- **DSA:** descubrimiento keywords — avanzado, necesita buenas campañas non-brand primero
- **PMax:** SOLO con OCI para lead gen. 30+ conversiones, €5-10K/mes mínimo
- **Demand Gen:** €100/día mínimo o 20× cost per conversion. Compromiso 3 meses
- **YouTube CPM/CPV:** tras tener datos de Demand Gen. Empezar con 5-10% del gasto total

## Presupuesto para Diversificación

- 5-10% del gasto total Google Ads como testing para video/nuevos canales
- Prerequisito: ya rentable en search/shopping
- B2B approach: <5% funciona. Caso: €500/mes video → mejoras dramáticas CPL en search
- Más presupuesto → aprendizaje más rápido (si se hace estratégicamente)

## Escalado de Presupuesto: Reglas

### NO hacer
- Subir presupuesto 10x de golpe → hits diminishing returns inmediatos
- De 100 búsquedas de alta intención/día, máximo 20-50 tomarán acción ese día
- Escalar demasiado rápido = pagar más por los mismos clics

### SÍ hacer
- Subir progresivamente: 15-20% cada 5-7 días
- Verificar que volumen extra viene con CPA aceptable
- Si CPA sube >20% tras incremento → pausar incremento, estabilizar

### Fase 3: Acquisition Lifecycle (Rafa Madorran — servicios locales España)

Secuencia para negocios nuevos — NO saltar pasos:

| Fase | Objetivo | Tácticas | Trigger avance |
|---|---|---|---|
| 1. Crear flujo | Llenar agenda rápido | Tratamientos entrada con descuento, diagnósticos gratis, forms baja fricción | — |
| 2. Monetizar flujo | Aumentar revenue/cliente | Upsell (entrada €50-100 → packs €1.000+), financiación, coreografía venta en clínica | 70-80% capacidad |
| 3. Añadir fricción | Mejorar calidad leads | Forms más largos, mover presupuesto a Google Ads (mayor intención), foco retención | Flujo estable + monetización funcionando |

- Fase 1 acepta leads de baja calidad intencionalmente — volumen importa más al empezar de cero
- Fase 3 transiciona de Meta (volumen, menor intención) a Google (menor volumen, mayor intención) como palanca de fricción

## Ley de Rendimientos Decrecientes

### Mental model: curva de campana
- Cada mecanismo de ads sigue una curva de campana de retornos
- Anunciantes llegan al ápice (pico ROAS) y se detienen
- Toda la segunda mitad de la curva sigue siendo rentable

### Ejemplo concreto
| Escenario | Revenue | Margen neto | Profit neto |
|---|---|---|---|
| En ápice | €1M | 40% | €400K |
| Escalado pasado ápice | €5M | 20% | **€1M** |

Margen se reduce a la mitad, pero profit absoluto se multiplica ×2,5.

### Principio
- "Rendimientos decrecientes siguen siendo rendimientos" — Hormozi
- Optimizar % margen vs $ profit absoluto = trampa
- Cada plataforma = su propia curva. Agotar cada una antes de saltar a la siguiente

## PMax: Cuándo y Cómo

### Requisitos para PMax lead gen
- 30+ conversiones/30 días
- €5.000-10.000/mes mínimo
- OCI configurado y acumulando datos 30-60 días
- Tracking completo

### Setup
1. 1 campaña PMax + múltiples asset groups (ej: 5 servicios = 5 asset groups)
2. Monitorizar qué asset groups reciben gasto vs cuáles tienen buenas métricas pero zero gasto
3. Asset groups con potencial pero sin gasto → breakout en campañas separadas
4. Solo expandir estructura cuando datos muestren temas hambrientos

### Diagnóstico distribución gasto
- 90%+ gasto en search/shopping = PMax saludable
- Heavy display o video = PMax underperforming → investigar creatives, tracking, LPs

### PMax negativas: guardrails, no control granular
- Servicios/productos que NO ofreces → negativizar
- Términos de gasto obvio desperdiciado (login, contact, download)
- Cross-campaign cannibalization → negativizar
- NO negativizar solo porque un term no ha convertido aún

## Demand Gen: Entrada a YouTube

### Pre-DG checklist
- ¿Ya rentable en search/shopping?
- ¿Tienes video/image creatives fuertes?
- ¿Presupuesto €100/día o 20× cost per conversion?
- Si no → priorizar inversión en search

### 3 escenarios para usar Demand Gen
1. **Resistencia CPC en search:** no puedes escalar rentablemente
2. **Necesitas educar audiencia:** USPs complejos que requieren explicación
3. **Rendimientos decrecientes en Meta:** Meta tocando techo, ya tienes creatives

### Testing
- Test geo-limitado: 1 ciudad/provincia → presupuesto DG dedicado → 2-3 meses → comparar uplift
- Split ad groups por placement (in-stream, Shorts, in-feed, display)
- 3-5 ads/ad group al inicio. Cada 3-4 semanas: mantener winners + nuevas iteraciones + nuevos ángulos
- Medir rendimiento TOTAL de cuenta, no solo métricas DG → buscar halo effects

### YouTube CPM infeed
- ~€2 CPMs en YouTube infeed vs ~€20 en Meta
- Por cada 1 usuario alcanzado en Meta → ~10 en YouTube infeed
- Incluso con CVR menor, solo necesitas 2 de 10 que muestren interés

## Estacionalidad y Escalado en España

### Cuándo escalar agresivamente
- Enero (rebajas + propósitos año nuevo)
- Septiembre (vuelta al cole, reactivación)
- Noviembre (Black Friday — preparar desde octubre)
- Diciembre (Navidad — pico máximo)

### Cuándo contener
- Agosto (vacaciones masivas — reducir 30-50%)
- Semana Santa (variable por sector)
- 3ª semana de cada mes (antes de nómina)

### Patrón nómina en España
- Mayoría cobra final de mes (día 28-31) o mediados (día 15)
- Fin de mes + domingo = mejor combinación para push presupuesto
- Mitad de mes + martes = peor combinación
