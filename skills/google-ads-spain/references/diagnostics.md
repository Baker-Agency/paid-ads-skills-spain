# Diagnóstico y Troubleshooting

## Zero Conversiones — Diagnóstico en 3 Pasos

Verificar en ESTE ORDEN tras esperar 6+ semanas:

### 1. Tracking roto (causa más común)
- Verificar que tracking realmente dispara con Tag Assistant
- Errores comunes: update de web borró tag, form plugin cambió, redirect roto
- Para coaching clients: esta es la causa #1 de zero conversiones

### 2. Personas equivocadas al sitio web
- Revisar search terms report
- Red flag: keyword non-brand con CTR absurdamente alto (ej: 75% en miles de impresiones) → tráfico Search Partners spam
- Manual CPC + Search Partners = spam trap clásica

### 3. Personas correctas, ruta conversión incorrecta
- SOLO mirar landing page y oferta si pasos 1 y 2 están perfectos
- Error de agencias: culpar LP inmediatamente ("problema de conversion rate"). NUNCA hacer esto sin descartar 1 y 2

## Search Partners + Manual CPC = Spam Trap

Combinación que genera muchos clics con zero conversiones:
- Bid strategy: Manual CPC o Maximize Clicks (optimiza tráfico más barato, ignorando conversiones)
- Network: Search Partners activado
- Resultado: algoritmo fuerza gasto hacia clics spam más baratos en red partners
- Verás search terms relevantes pero con CTRs imposibles (75%)
- Fix: desactivar Search Partners inmediatamente + cambiar a Maximize Conversions

## CPA Alto — Framework 6 Factores

| Factor | Diagnóstico | Fix |
|---|---|---|
| CPC subió | Competencia nueva, QS bajó, estacionalidad | QS optimization, negative keywords, bid adjustment |
| CVR bajó | LP rota, oferta débil, tracking parcial | Verificar tracking primero, luego LP/offer |
| Tráfico irrelevante | Broad match drift, negativas insuficientes | Search terms review, añadir negativas |
| Search Partners | Tráfico spam barato, zero conversiones | Desactivar Search Partners |
| Learning period | <7 días desde cambio significativo | Esperar. No tocar |
| Conversion lag | Datos no completos (conversiones tardan días/semanas en reportarse) | Revisar con ventana adecuada (14-30 días, no 2 días) |

## Caída de Rendimiento — Triage 3 Pasos

### Paso 1: ¿Algo está roto?
- [ ] ¿Tracking funciona? (Tag Assistant)
- [ ] ¿Anuncios aprobados y sirviendo?
- [ ] ¿Landing page carga correctamente?
- [ ] ¿Formularios/teléfono/chat funcionan?
- [ ] ¿Merchant Center conectado? (si aplica)
- [ ] ¿Budget limitado? ¿Overspent?

### Paso 2: ¿Es ruido o tendencia?
- 1 día malo → RUIDO. No tocar
- 3 días consecutivos → INVESTIGAR (paso 1)
- 1-2 semanas sostenidas → TENDENCIA REAL. Optimizar
- Display/Demand Gen/Video: esperar 1-2 semanas MÍNIMO antes de decidir

### Paso 3: ¿Qué cambió?
- Revisar change history en Google Ads
- ¿Alguien tocó pujas/presupuesto/keywords?
- ¿Competidor nuevo? (Auction Insights)
- ¿Estacionalidad? (3ª semana mes, festivo, agosto)
- ¿Update algorítmico de Google?
- ¿Cambio en web/LP sin avisar?

## Cadena de Reacción Tracking Roto

```
Tags rotos → Datos conversión a la mitad → Smart Bidding optimiza señal parcial
→ Pujas cambian en keywords incorrectas → Tráfico peor → Conversiones reales caen
→ Smart Bidding degrada más → Espiral descendente
```

- Cada día sin detectar → más daño compuesto
- Fix: auditar TODOS los métodos conversión regularmente
- Implementar Guardian script (Enrique del Valle) como alerta

## Keyword Creep / Drift

### Síntomas
- Search terms cada vez menos relevantes
- CPA subiendo gradualmente sin cambios obvios
- CTR bajando
- Broad match mostrando terms cada vez más alejados

### Causas
- Listas negativas no actualizadas
- Broad match sin suficientes señales de conversión
- Smart Bidding sin datos suficientes (< 30 conv/mes)
- Ad group con keywords no coherentes temáticamente

### Fix
1. Revisar search terms últimas 4 semanas
2. N-gram analysis para patrones
3. Actualizar listas negativas agresivamente
4. Verificar coherencia temática ad groups
5. Si broad match → ¿hay suficientes conversiones para Smart Bidding?

## PMax Remarketing Diagnostic

- PMax puede gastar mayoría del presupuesto en remarketing (audiencia conocida)
- Síntoma: alto ROAS pero no crecimiento de nuevos clientes
- Verificar: Insights → distribución audiencia (new vs returning)
- Fix: customer match exclusions, audience signals más específicos

## Click Fraud — Perspectiva España

### Estimación
- Enrique del Valle: 5-20% fraude en campañas lead gen PMax
- Display: tráfico bot significativo (por eso script de fraud en desarrollo)
- Search: menor fraude pero existe (competidores clicking)

### Señales
- Picos anómalos de clics sin conversiones
- Misma IP/device repitiendo clics
- Bounce rate 100% en segmentos específicos
- Clics desde geos inesperados

### Protección
- Google automatic invalid click protection (basic)
- ClickCease, Lunio, TrafficGuard (herramientas third-party)
- Script Display fraud (Ninja Scripts, en desarrollo)
- Monitorizar Auction Insights para comportamiento anómalo competidores

## Throttling (Cuentas Nuevas)

### Qué es
- Campaña nueva con settings correctos recibe zero/mínimas impresiones durante días
- Duración: 1-2 semanas hasta serving normal

### Cuándo ocurre
| Trigger | Detalle |
|---|---|
| Cuentas nuevas | Primeras campañas throttled ~1-2 semanas |
| Reestructura masiva | Pausar todo + lanzar todo nuevo → throttling |
| Industrias sensibles | Finanzas, pharma, cualquier sector que requiere certificaciones |

### Prevención
- En cuentas maduras: lanzar pocas campañas a la vez. NUNCA scorched-earth
- No hay fix fiable una vez throttled — soporte da respuestas genéricas
- Microsoft Ads: throttling MUCHO más agresivo que Google en cuentas nuevas

## Conversion Lag como Falsa Caída

- Conversiones tardan días (a veces semanas) en reportarse
- Datos últimos 2-3 días SIEMPRE parecen peores de lo que realmente son
- Fix: comparar con ventana de 14 o 30 días, no últimos 2 días
- Especialmente relevante para B2B con ciclos de venta largos
- Google Ads UI: columna "Conversions" muestra datos con delay
