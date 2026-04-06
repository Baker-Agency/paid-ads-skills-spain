# Progresión de Estrategia de Pujas

## Secuencia completa

```
Manual CPC → Maximize Clicks → Maximize Conversions → Target CPA → Target ROAS
```

### Cuándo usar cada una

| Estrategia | Cuándo | Conversiones necesarias | Caso de uso |
|---|---|---|---|
| Manual CPC | Cuentas nuevas B2B, campañas de marca, presupuesto muy bajo | 0 | Control total, datos iniciales |
| Maximize Clicks | Cuenta nueva, sin historial conversiones | 0 | Obtener tráfico y datos. Sin bid cap |
| Maximize Conversions | 15+ conversiones/30 días | 15+ | Alimentar señales al algoritmo desde día 1 |
| Target CPA | 30+ conversiones/30 días, CPA estable | 30+ | Estabilizar y escalar |
| Target ROAS | 50+ conversiones/30 días, valores asignados | 50+ | Optimizar por valor, no volumen |

## Umbrales de Smart Bidding

- Mínimo técnico (Google oficial): 15 conv/30 días
- Medio práctico (Jill Saskin Gales): 30 conv/30 días
- Consistencia estadística: 50+ conv/30 días
- Alto gasto (millones/mes): 1-2 días de learning
- Bajo gasto (5-6 conv/mes): 3-4 meses de learning

## Transición Max Conversions → Target CPA ("método escalera")

### Prerrequisitos

- Mínimo 30 conversiones en 30 días
- CPA semanal estable (variación <20% en 4 semanas)
- NO cambiar si CPA sigue bajando rápidamente

### Pasos

1. Revisar CPA real últimos 30 días (ejemplo: €50)
2. Fijar tCPA LIGERAMENTE SUPERIOR (ejemplo: €55 — NO tu objetivo ideal)
3. Esperar 1 semana — verificar volumen estable
4. Bajar tCPA gradualmente (€55 → €52 → €50 → €48)
5. Cada bajada: esperar 1 semana antes del siguiente paso

### Por qué no fijar objetivo directamente

- Fijar €35 cuando actual es €50 → algoritmo excluido del 80% de subastas
- Volumen colapsa → campaña "se ahoga"
- Siempre empezar por encima de lo actual y bajar

## Max Conversions vs Target CPA: mecánicas

- **Max Conversions:** sin techo. Google busca gastar TODO el presupuesto, entrando en subastas caras si cree que convertirá. CPA fluctúa salvajemente
- **Target CPA:** crea techo. Google rechaza subastas que arruinarían el target promedio. Estabiliza CPA pero reduce elegibilidad en subastas
- **SIEMPRE** usar bid cap con tCPA → evitar clics individuales disparados

## Campaña de marca: estrategia de pujas

### Debate entre expertos

| Posición | Estrategia | Razón |
|---|---|---|
| Chris Schaefer | Manual CPC / Target IS | Marca = visibilidad, no conversiones. IS automatiza sin métricas de conversión |
| Gonzalo & Zach (AC Conversion) | Manual CPC | Testearon vs Smart Bidding en PLG SaaS ($100K/mes brand) → Manual ganó en IS, CPCs y cost per trial |
| Joey Bidner | Manual CPC | Toda intención de marca es BOFU. Goal = dominar top of page al menor coste |
| Jill Saskin Gales | Target CPA/ROAS | Manual CPC falla en muchas campañas de marca. Smart Bidding ajusta por query, no keyword |

### KPIs para marca

- Solo medir: Impression Share + Absolute Top IS
- NO usar: maximize conversions, target CPA, max clicks para marca
- Si no hay competidores pujando por tu marca → considerar pausar marca y testear

## Bidding para Demand Gen / YouTube

### Demand Gen

| Propósito | Estrategia inicio | Progresión |
|---|---|---|
| Prospecting (frío) | Maximize clicks | Target CPC |
| Remarketing | Max conversions / max conv value | Target CPA / Target ROAS |

### YouTube video

- No existe "maximize views"
- Empezar con target CPV alto (~€0,10-0,15) → dar espacio
- Bajar target CPV después si necesario
- Alternativa: YouTube Promote desde YouTube Studio

## Learning period: lo que importa

### Lo que NO resetea aprendizaje (semántico)

- Copiar/mover assets entre ad groups
- Cambios menores en keywords dentro del mismo tema
- Shared budgets / Portfolio bidding

### Lo que SÍ resetea aprendizaje

- Cambiar acción de conversión (cambiar qué optimiza)
- Cambiar estrategia de puja completamente (Max Conv → tCPA)

### Velocidad de learning

- Dictada por volumen de conversiones + conversion lag
- E-commerce rápido: horas/días
- B2B SaaS con lag 14-40 días: semanas/meses
- La etiqueta "Aprendizaje" en UI = 5 días fijos (cosmético)

## Fases de cuenta (Grow My Ads)

1. **Fase 1 (Datos):** cuenta/campaña nueva. Paciencia. No rentable inherentemente
2. **Fase 2 (Volumen):** acumulando historial de conversiones
3. **Fase 3 (Eficiencia):** dial in smart bidding (de max conversions hacia tCPA)
4. **Fase 4 (Escalado):** crecimiento progresivo

## Portfolio Bid Strategies

- Permite agrupar campañas bajo una estrategia de puja compartida
- Consolida densidad de datos sin reestructurar campañas
- Permite fijar **Max CPC cap** (no disponible en tCPA estándar sin portfolio)
- Workaround para el problema de clics individuales disparados con tCPA

## Value-Based Bidding (tROAS)

- Solo estrategias ROAS/value reconocen valores de conversión
- Max Conversions y tCPA IGNORAN valores completamente
- Requisitos: asignar valores a conversiones + suficiente volumen
- Para lead gen: usar scoring (1-10) o valores nominales por etapa pipeline
- OCI con valores reales de venta → Google aprende qué leads son más valiosos

## Errores comunes

1. Empezar con tCPA sin datos → campaña muere en 2 días
2. Fijar tCPA muy agresivo desde el inicio → se ahoga
3. Escalar presupuesto 10x de golpe → retornos marginales decrecientes inmediatos
4. Cambiar pujas a diario → learning period infinito
5. Mezclar Manual CPC con Search Partners → spam trap
6. No usar bid cap con tCPA → clics individuales de €50+
