# Automatización y Scripts para Google Ads

## Ninja Scripts (Enrique del Valle)

Experto español en Google Ads desde 2004. Filosofía: "algo automático para controlar otra cosa automática" — scripts para mantener algoritmos Google en check.

Panel de control: Google Sheets como interfaz — configurar todo sin editar código. Cada script incluye manual, curso video y comunidad Telegram.

### 1. Script de Negative Keywords (disponible — €97 único)

Mayor ahorro de tiempo. Controla el drift de broad match.

- Corre cada hora
- Negativiza automáticamente search terms irrelevantes
- Crítico porque Google muestra anuncios para terms no relacionados (ej: pujar por "curso Google Ads" dispara "curso TikTok", "curso gratis")
- Impresiones irrelevantes con CTR bajo → daña Quality Score → CPCs más altos
- Funciona en Search y Shopping (Shopping especialmente propenso a matches irrelevantes)
- Incluye 1 año de actualizaciones
- Ahorro estimado: 2-3 horas/día

### 2. Script Guardian / Monitoring (gratis + pro €19)

Detecta el clásico "campaña dejó de convertir porque el formulario se rompió".

- Monitoriza: impresiones, conversiones, URLs landing pages
- Alertas por email cuando umbrales se superan
- Configurable: definir cuántas horas sin impresiones/conversiones antes de alertar
- Versión pro en desarrollo (beta con mejoras)

### 3. Script Smart Bidding + Budget (próximamente)

Automatización diaria de pujas y presupuesto.

**Ajuste Target ROAS/CPA:**
- Corre diario
- Escenario neutral: fija target a lo que campañas realmente consiguieron últimos 30 días
- Si rendimiento mejora vs ayer → recalcula target (sube orgánicamente)
- Puede forzar offset: fijar target 10% por encima de últimos 30 días
- Si rendimiento empeora → baja target a match reality
- Múltiples escenarios: mejora → subir presupuesto; declive → reducir

**Pacing presupuesto mensual:**
- Calcula proporción diaria gastada vs esperada
- Si overspending → contiene ajustes positivos de puja incluso si rendimiento es bueno
- Previene overruns de presupuesto a fin de mes

### 4. Script Display Fraud (planificado — reconstruyendo)

- Originalmente construido hace ~5 años para combatir tráfico bot en Display
- Coste desarrollo original ~€10.000
- Salvó cliente de pérdidas por fraude
- Se rompió cuando Google cambió API — necesita rebuild
- No correr campañas Display prospecting hasta tener este script

## Por Qué Scripts Importan para Quality Score

- Mejorar QS ahorra 20-30% en CPC
- Smart Bidding ahorra 100% en bad clicks (evita subastas) — pero scripts complementan limpiando search terms que Smart Bidding no filtra
- Negativizar terms irrelevantes → menos impresiones con CTR bajo → mejor QS → CPCs más bajos
- QS en interfaz Google Ads es misleading: solo refleja ~1% de queries donde search term = keyword exacto. El otro 99% (variaciones broad match) cada uno tiene su QS oculto

## AI Agents vs Scripts

### Distinción clave
- **Scripts** = deterministas. "Si coste search term > 2× CPA → añadir como negativa." Ejecuta exactamente lo definido, sin juicio
- **AI Agents** = contextuales. Evalúan si un search term es negativa basándose en contexto de negocio, intención del ad group, y semántica — no solo reglas de coste

### Dónde agentes añaden valor sobre scripts
- Identificar negativas antes (antes de desperdiciar gasto) entendiendo intención, no esperando umbrales de coste
- Analizar marketing bias del ad copy — qué ángulos funcionan mejor/peor, comparar con posicionamiento competidor
- Coordinar acciones: "agentes maestros" analizan root cause de cambios rendimiento → triggean agentes especializados (copy, negativas, extensions)
- Auto-corrección: agente A añade negativas → rendimiento cae → agente B revisa y elimina negativas bloqueantes la semana siguiente

### Categorías de agentes (lead gen focus)
- Optimización ad copy — análisis marketing bias, comparación ads competidor, brainstorming headlines
- Finder de negative keywords — context-based, explica razonamiento por keyword por ad group
- Optimización extensions — refresh semanal
- Adición de keywords nuevas

### Limitación
- Agentes no siempre perfectos la primera vez
- Counter-measures suavizan impacto con el tiempo
- Todavía necesita juicio humano para casos ambiguos

## 8020 Agent (Mike Rhodes)

Tool de IA para optimización Google Ads. De pago — requiere onboarding (datos cuenta en Google Sheet, luego refresh hourly).

### Keyword Engram Analysis
- Agrupa todos search terms por palabra individual y agrega métricas rendimiento por palabra
- Revela 3 tipos optimización: negativas, nuevos temas keywords, segmentación campaña/ad group
- Corre en ~10 segundos sobre miles de search terms → 4-5 recomendaciones claras
- Da acciones recomendadas — no implementar a ciegas, investigar cada una
- Caso servicio: cliente aire acondicionado → "calculadora" en search terms tenía métricas conversión significativamente mejores → separar en campaña search dedicada

### Smart Bidding Readiness Prompt
- Framework decisión: ¿cambiar estrategia Smart Bidding o targets?
- Analiza todas las campañas contra checklist 4 pasos yes/no
- Velocidad: 6 campañas en 10-15 segundos (vs 5-10 min/campaña manualmente)
- Da yes/no/wait por campaña + targets recomendados
- Para "yes": verificar últimas 6 semanas de datos antes de aplicar

### PMax Script
- Script más popular Google Ads
- Obligatorio para cualquiera con PMax
- Visibilidad distribución canales (dónde PMax realmente gasta)
- Comparación campañas múltiples PMax
- Datos rendimiento en cuadrantes (high/low performers)

## N-gram Analysis Workflow

### Qué es
Romper search terms en secuencias de 2/3/4 palabras para encontrar patrones en miles de terms.

### Proceso
1. Exportar search terms (último mes o más)
2. Alimentar a herramienta n-gram (8020 Agent, Gemini, script público)
3. Analizar:
   - High CPA n-grams → segmentar en campaña separada o negativizar
   - Low CPA n-grams → expandir y dedicar presupuesto
4. Implementar cambios

### Herramientas
- 8020 Agent (Mike Rhodes) — automático
- Google "Words" card — análisis 1-gram básico nativo
- Gemini — pegar search terms y pedir análisis
- Scripts públicos — varios disponibles en comunidad

## Automation Frameworks (Sammy / Adalysis)

### 3 fases del lifecycle
1. **Launch:** esperar sample size. Regla lead gen: "Si Coste > €500 Y Conversiones < 1 → Pausar Ad". Corre hourly.
2. **Maintenance:** más datos, estabilizar. Regla: "Si Cost/Conv > €500 Y MQLs < 1 en 90 días → Pausar Ad". Corre hourly.
3. **Scale:** reasignar presupuesto winners → losers. "Si pacing bueno Y cost/conv aceptable → Aumentar Budget X%"

### Budget Protection Rule
- Step 1: alertar Slack cuando 80% presupuesto mensual gastado
- Step 2: pausar automáticamente campañas cuando 98% gastado
- Margen 60 minutos entre checks → usar 98% no 100%

### Ad Scheduling Rule
- Pausar campañas off-hours para consolidar gasto en horas prime
- España: 9:00-21:00 CET (considerar horario partido)
- Lógica: pausar a 21:00 UTC, activar a 8:00 UTC
- Alternativa: reducir presupuesto 90% noche en vez de pausar
