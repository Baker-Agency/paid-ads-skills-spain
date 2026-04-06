# Estructura de Campañas Meta — Era Andromeda

## Andromeda: Contexto

Algoritmo Meta (2025-2026). Matching individual usuario↔anuncio. Ya no es segmentación por audiencia masiva, sino matching 1:1 mediante deep neural network.

**Consecuencia práctica:** creatividad diversa = palanca #1. Estructura de cuenta = secundaria (cómo fluye el presupuesto, no cómo funciona el rendimiento).

**Advantage+ = Andromeda.** Cualquier campaña con Advantage+ activo ya usa Andromeda.

## Estructura por Presupuesto y Madurez Pixel

| Presupuesto/mes | Pixel | Estructura | Notas |
|---|---|---|---|
| <€2.500 | Nuevo (0-50 conv) | 1 ABO, 3-5 ad sets, broad | No se puede dividir. Foco: encontrar 1 ángulo ganador |
| €2.500-8.000 | Algo de data (50-200 conv) | Testing ABO (20%) + Scaling CBO (80%) | Graduar ganadores de testing → scaling. Retargeting solo con >1K visitantes LP/semana |
| €8.000-25.000 | Maduro (200+ conv) | Testing ABO (15%) + TOFU CBO (60%) + Retargeting CBO (25%) | Funnel completo viable. Refresh creativo semanal |
| €25.000+ | Fuerte (500+ conv) | Testing ABO (15%) + TOFU CBO (50%) + MOFU/BOFU CBO (20%) + Retargeting (15%) | Portfolio: CBOs por persona/concepto |
| €40.000+ | Fuerte | Portfolio: múltiples CBOs + diversificación bid strategy | Ver framework escalado |

## CBO vs ABO — Cuándo Usar Cada Uno

| Usar CBO | Usar ABO |
|---|---|
| Escalando ads/audiencias probadas | Testeando nuevos conceptos |
| 3+ ad sets con presupuesto suficiente | Aislando variables (1 concepto por ad set a presupuesto fijo) |
| Quieres que algoritmo distribuya gasto a mejores | Necesitas gasto igual por ad set independientemente de rendimiento |
| Presupuesto > CPL target × 10 por día | B2B high-ticket (€1K+ deals) con control preciso audiencia |

## Estructura Persona-Based (Andromeda)

**Según Josh (Motion) / Samuel:**

- Abandonar estructura rígida TOFU/MOFU/BOFU o por formato
- Organizar ad sets por persona o concepto core (ej: 9 personas = 9 ad sets)

### Setup
- **Campaña Testing:** Ad sets por persona. Anuncios visualmente diversos por persona
- **Campaña Evergreen:** Ad sets que replican los de testing

### Workflow
1. Identificar ad ganador en testing para una persona
2. Mover (post ID) al ad set correspondiente en evergreen
3. Mantener testing alimentando evergreen constantemente

## One CBO + Flex Ads (Andromeda)

**Según Charley T (Disruptor School) / Meta MBA grad Tikis:**

- **1 CBO** (Advantage Campaign Budget) para toda la cuenta. Objetivo "Sales"
- **1 ad set.** Dentro: **1 Flex Ad** con 2-3 variaciones creativas
- **No tocar.** Ediciones = reshuffling → learning phase
- Solo añadir ad set por razón estratégica específica
- Ideal para: presupuestos pequeños-medianos (€2.500-12.000/mes) con volumen creativo limitado

## High-Volume Campaign Structure (Andromeda)

**Según Kale Cruz:**

- Estructura importa para flujo de presupuesto, no rendimiento. Andromeda es horizontal
- **Budget liquidity:** dejar que Meta distribuya gasto automáticamente
- Framework: 1 CBO. Ad sets por concepto/persona. 10-20 variaciones por ad set

### Cadencia producción (para 50-100 ads/mes)
- Semana 1: 3-5 conceptos × 3-5 hooks = 15-20 ads
- Semana 2: Iterar ganadores (nuevos hooks, mismo body) = 10-15 ads
- Semana 3: 2-3 conceptos nuevos + iteraciones = 15-20 ads
- Semana 4: Review, kill losers, planificar siguiente mes

Ideal para: €12.000+/mes con motor producción creativa activo

## Framework TPS: Test → Prove → Scale

**Según Thomas Owen:**

| Fase | Presupuesto/día | Setup | Criterio avance |
|---|---|---|---|
| **Test** | €40-50 por ad set | 5 campañas ABO, cada una = 1 concepto. Múltiples hooks por concepto | CPL bajo target después de €200+ gasto |
| **Prove** | €150-200 | Ganadores duplicados con post ID a 4× presupuesto | Mantiene rendimiento 48-72h+ |
| **Scale** | CBO €400-8.000+/día | 3-5 ads probados en CBO. Usar bid caps + dayparting | ENCAC estable al escalar |

Trayectoria: €40/día → €150/día → €400-800/día → €8.000+/día

## Señales de Consolidación

**Consolidar cuando:**
- >4 campañas activas (excluyendo retargeting)
- Múltiples campañas targetando audiencias similares (>30% overlap)
- Cualquier campaña gastando <€40/día con <10 conversiones semanales
- 5+ ad sets por campaña, cada uno con <10 conversiones
- >50% presupuesto en Learning o Learning Limited

**Estado objetivo mayoría cuentas:** 1 CBO scaling + 1 ABO testing + 1 retargeting. Top operators: 2-3 ad sets máx por campaña, 5-6 ads por ad set.

## Learning Phase

### Qué es
Sistema entrega ads aleatoriamente para encontrar mejor audiencia/placement/puja. Entrega y ROAS inconsistentes durante esta fase.

### Salir del learning phase
- ~50 conversiones desde la **última edición significativa**
- Ediciones significativas: cambios budget grandes, cambios audiencia, cambios creative sustanciales
- **El "7 días" es un mito:** puedes salir aunque tardes 25-30 días, siempre que no hagas ediciones significativas

### % Budget en learning
- **Sano:** <25-30% del presupuesto en learning
- **Normal durante rebuild/testing:** 60-70%
- Si >70% permanente → estructura rota, consolidar

### Tips
- Agrupar 3-10 ads por ad set para estabilidad
- Campañas scaling deben tener MAYORÍA del presupuesto
- Si testing consume 70%, el % learning global mata consistencia

## Advantage+ Leads

### Qué es
Tipo campaña Meta optimizado para lead gen. Distinto de Advantage+ Sales (ASC). Mayor automatización: Meta controla audiencia, placements, algo de optimización creativa.

### Cuándo usar

| Factor | Advantage+ Leads | Lead Gen manual |
|---|---|---|
| Data pixel | Fuerte (500+ conv/mes) | Nuevo o <50 conv/mes |
| Control audiencia | Bajo (broad funciona) | Alto (B2B, SAC) |
| Volumen creativos | 10+ creativos diversos | <5 creativos |
| Presupuesto | €80+/día | Cualquiera |

### Limitaciones
- Menos control targeting — no se pueden excluir ciertas custom audiences
- Requiere diversidad creativa (algoritmo necesita opciones)
- Reporting más agregado
- **NO usar en Special Ad Categories** (SAC) — controles limitados conflictan
- Siempre mantener campaña manual paralela (10-20% presupuesto) para comparación
