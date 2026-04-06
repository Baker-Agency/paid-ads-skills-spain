# Cadencia de Optimización

## Primeros 7 Días: SOLO Monitorizar

### Día 1-2 (check fundacional)
- ¿Tags de conversión activos y configurados correctamente?
- ¿Anuncios aprobados y elegibles?
- ¿Se gasta el presupuesto? Si €100/día y solo €20 tras 2 días → problema de bid strategy o targeting demasiado restrictivo
- ¿Mínimo 10 clics/día para Search? Si gasta todo pero <10 clics → pujando demasiado agresivo por clic

### Días 3-7 (cadencia diaria)
- **Search terms:** revisar diario. Añadir negativas = ÚNICA optimización permitida primera semana
- **CTR check:** tras 50-100 clics (~1 semana). Si <2% (o peor, <1%) → mismatch keywords/ad copy. Buscar tráfico irrelevante en search terms
- **Conversiones:** tras 50-100+ clics de alta intención, 1-2 conversiones deberían empezar. Si 0 tras 100 clics de alta intención → revisar tracking, oferta vs competencia, landing page

### ERROR MÁS GRANDE: optimizar demasiado pronto
- Ajustar pujas/presupuestos los primeros días = resetear learning = matar campaña antes de empezar
- Reducir frecuencia de cambios un 50% puede reducir CPAs un 25%

## Check Diario (post primera semana)

### Qué es un check diario
- Buscar "hiccups y anomalías", NO optimizar
- Últimos 7 días vs ayer
- ¿Campañas corriendo? ¿Desaprobaciones raras? ¿Gasto alineado con media histórica diaria?
- Patrones normales (bajón fin de semana) → ignorar
- NO cambiar pujas/presupuestos por fluctuación normal

### Cadencia por rol
| Rol | Check | Optimizar |
|---|---|---|
| Agencia | Diario (solo monitorizar) | Semanal máximo (salvo presupuesto muy grande) |
| Dueño negocio (cuenta estable) | Semanal | Mensual |
| Campaña nueva (primeros días) | Diario (asegurar serving) | NO optimizar — no hay datos suficientes |

## Optimización Semanal

### Search terms review
1. Filtrar últimos 7 días
2. Ordenar por gasto (top 5-10 terms)
3. "Seguir el dinero" — no perder tiempo con terms de 1 impresión
4. Negativizar temas que nunca convertirán (no terms individuales)
5. Solo negativizar lo que SABES que no convierte (servicios que no ofreces, temas irrelevantes)

### Pacing check
- ¿Gasto vs presupuesto mensual va en línea?
- Día 10 del mes con €3.000/mes → deberías llevar ~€1.000
- Si muy por encima → contener; si muy por debajo → investigar

### Métricas competitivas
- Search Impression Share: ¿estás ganando las subastas que deberías?
- Absolute Top IS: ¿apareces en primera posición?
- Si IS cae de 80% a 70% → investigar (nuevo competidor, necesitas pujar más)

## Optimización Mensual

### N-gram analysis
- Romper search terms en secuencias de 2/3/4 palabras
- High CPA n-grams → segmentar en campaña separada o negativizar
- Low CPA n-grams → expandir y asignar presupuesto dedicado
- Herramientas: 8020 Agent (Mike Rhodes), scripts públicos, Gemini
- Google tiene "Words" card nativa para análisis 1-gram básico

### Auditoría Quality Score
- Filtrar keywords con QS 1-3 → prioridad máxima de fix
- 3 componentes: CTR esperado, relevancia anuncio, experiencia LP
- Mejora QS = 20-30% ahorro CPC
- QS en UI solo refleja ~1% queries (exact match). Resto tiene QS oculto

### Reasignación presupuesto
- Mover presupuesto de campañas peores a mejores
- Es la optimización MÁS FÁCIL y de mayor impacto
- Jerarquía de optimización: gasto → targeting → ads/LPs → pujas

### Dashboard: columnas recomendadas (método Groma)
Configurar vista personalizada:
1. **Sin clics aún:** Impressions, Search top IS, Search abs. top IS
2. **Con clics:** Clicks, Avg CPC, CTR
3. **Con conversiones:** Conversions, Cost/conv, Conv rate, columnas custom por etapa funnel

## Optimización Trimestral

### Revisión geo targeting
- Rendimiento por comunidad autónoma
- ¿Hay CC.AA. con CPA disparado? → excluir o ajustar
- ¿Hay CC.AA. con buen rendimiento infraexplotadas? → aumentar presupuesto

### Auditoría horarios
- Day of week analysis: identificar peores y mejores días
- España: 3ª semana del mes = siempre más débil (antes de nómina)
- Fines de semana: variable por sector. Servicios B2C puede funcionar, B2B raramente
- Considerar reducir presupuesto viernes-domingo si no convierte
- Considerar horario partido español (9-14, 16-21)

### Refresh listas negativas
- Revisar y ampliar las 3 listas
- Añadir nuevos competidores que hayan aparecido
- Revisar si hay negativas bloqueando tráfico bueno (especialmente con broad match)

### Revisión estacional
- ¿Se acercan rebajas (enero, julio)?
- ¿Agosto? → preparar reducción presupuesto
- ¿Vuelta al cole (septiembre)? → preparar aumento
- ¿Black Friday / Navidad? → preparar desde octubre

## Cuándo Preocuparse (y cuándo no)

### NO preocuparse
- 1 día malo → ruido normal. NO tocar nada
- ROAS fluctúa entre 3 y 7 esta semana → normal si promedio semanal OK
- Fin de semana peor que entre semana → patrón estándar
- 3ª semana del mes floja → patrón salarial universal

### PREOCUPARSE
- 3 días consecutivos malos → investigar:
  1. ¿Tracking roto? (form, teléfono, chat)
  2. ¿Anuncios rechazados?
  3. ¿Merchant center desconectado?
  4. ¿LP caída o lenta?
  5. Si nada roto → esperar. Usuarios simplemente no compran ese día
- 1-2 semanas de caída sostenida → optimizar con datos reales
- Search IS cae bruscamente → nuevo competidor o problema de pujas

### Campañas no-Search (Display, Demand Gen, Video)
- Horizonte temporal DIFERENTE a Search/Shopping
- Más volátiles inherentemente
- 3-5 días de caída = fluctuación, NO tendencia
- Esperar 1-2 semanas mínimo antes de decidir que hay caída real
- NUNCA duplicar campaña para "arreglar" caída → divide datos + descarta learning

## Jerarquía de Optimización (en orden de impacto)

1. **Gasto/Segmentación** (MÁS FÁCIL, MAYOR IMPACTO)
   - Mover presupuesto a campañas/grupos ganadoras
   - Ejemplo: subir servicio A a €200/día, mantener B en €90/día
   
2. **Targeting**
   - Ajustar keywords, ubicaciones, audiencias, demografía
   - Basado en datos de observation mode recogidos
   
3. **Anuncios/Landing Pages**
   - Mejorar triggers emocionales, USPs, velocidad página
   - CRO de landing page
   
4. **Pujas** (ÚLTIMO RECURSO)
   - Ajustar pujas solo con volumen base conseguido
   - Si no tienes datos → optimizar arriba primero

## Principio de "No Tocar"

Si campañas van bien → NO TOCAR. Historial de cambios vacío no significa que no estés trabajando.

### Qué hacer en vez de tocar
- Si todo va bien → inventar y testear cosas nuevas (en campañas SEPARADAS)
- Dejar lo que funciona en paz. Testear en paralelo
- "La jugada más inteligente a veces es no hacer nada" — Miriam Navas

## R&D Budget

- Dedicar 20% del presupuesto a campañas experimentales (Enrique del Valle)
- Estas campañas se ESPERA que fallen — ese es el punto
- Cuando un experimento tiene éxito → añadir al 80% que rinde
- Alternativa conservadora: 5% para tests (Lauren Petrullo, presupuestos <€6K)
- El % correcto depende de: tamaño cuenta, tolerancia riesgo cliente, madurez cuenta
