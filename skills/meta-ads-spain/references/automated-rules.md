# Reglas Automatizadas — Meta Ads

## Dónde encontrar

Ads Manager > Rules > Create New Rule (o Manage Rules)

## Tipos de Regla

| Tipo | Qué hace | Uso |
|---|---|---|
| Budget rule | Aumentar/disminuir presupuesto por % o cantidad fija | Auto-escalar ganadoras, auto-reducir perdedoras |
| Pause rule | Pausar ad, ad set o campaña cuando condición se cumple | Safety net: pausar si CPA excede techo |
| Notification rule | Enviar email alerta cuando condición se cumple | Alerta temprana: spike CPM, umbral frecuencia |
| Enable rule | Reactivar ad/ad set pausado cuando condición se cumple | Re-habilitar ad sets cuando coste baja |

## Templates Esenciales (Agencia)

### 1. CPA Ceiling (Crítica)

| Campo | Valor |
|---|---|
| Condición | Coste por resultado > 2× CPA objetivo últimos 3 días |
| Acción | Pausar ad set |
| Frecuencia | Cada 12 horas |
| Por qué | Previene gasto desbocado en ad sets rotos overnight/fines de semana |

### 2. Alerta Frecuencia

| Campo | Valor |
|---|---|
| Condición | Frecuencia > 3 (prospecting) o > 5 (retargeting) últimos 7 días |
| Acción | Enviar notificación |
| Frecuencia | Diaria |
| Por qué | Señal temprana saturación audiencia antes de que CPL suba |

### 3. Escalado Presupuesto (Conservador)

| Campo | Valor |
|---|---|
| Condición | Coste por resultado < CPA objetivo 3 días consecutivos Y 20+ resultados |
| Acción | Incrementar presupuesto diario 20% |
| Frecuencia | 1×/día, máx 1× por campaña |
| Por qué | Auto-escala ganadoras sin resetear learning (20% = umbral seguro) |

### 4. Spend Cap Diario

| Campo | Valor |
|---|---|
| Condición | Gasto hoy > 1.5× presupuesto diario |
| Acción | Enviar notificación |
| Frecuencia | Cada 6 horas |
| Por qué | Detecta comportamiento occasional de Meta de gastar de más |

### 5. CPM Anomalía (Opcional)

| Campo | Valor |
|---|---|
| Condición | CPM > €80 últimas 24 horas |
| Acción | Enviar notificación |
| Frecuencia | Diaria |
| Por qué | CPMs anormalmente altos pueden indicar problemas cuenta o policy |

## Naming Convention

```
[Acción]_[Métrica]_[Umbral]_[Scope]
```

**Ejemplos:**
- `Pausar_CPA_2x_AdSet`
- `Escalar_CPA_BajoTarget_Campaña`
- `Alerta_Frec_3_Prospecting`
- `Alerta_Frec_5_Retargeting`
- `Alerta_SpendCap_150pct_Diario`

## Limitaciones y Trampas

### Evaluación
- Reglas evalúan cada **30 minutos** mínimo — no tiempo real
- No depender de reglas para detectar issues en <1 hora
- Rango temporal importa: "últimos 3 días" más seguro que "hoy" (hoy resetea a medianoche, muestra pequeña)

### Scope
- Reglas aplican a TODAS las entidades que cumplen condición
- "Pausar si CPA > €100" en 20 ad sets → las pausa TODAS, no solo la peor
- Solución: crear reglas específicas por campaña/ad set cuando sea crítico

### Learning Phase
- Reglas NO se activan en campañas en Learning Phase (Meta las salta)
- No depender de reglas como safety net durante learning

### Timezone
- Reglas usan timezone de la **cuenta publicitaria**, no tu hora local
- En España: asegurarse que cuenta está en CET (Europa/Madrid)

### Conflictos
- Múltiples reglas conflictivas (una escala, otra pausa misma entidad) = caos
- Auditar interacciones entre reglas trimestralmente
- Documentar todas las reglas activas y su lógica

## Reglas para España — Consideraciones

### Horarios
- Reglas de alerta: considerar horario español (9:00-14:00 + 16:00-21:00)
- Notificaciones nocturnas: útiles solo si alguien las monitoriza

### Estacionalidad
- Agosto: considerar reglas de reducción presupuesto automática
- Black Friday / Navidad: relajar umbrales CPA (CPMs suben naturalmente)
- Verificar reglas antes de cada período estacional

### Multi-cuenta (agencias)
- Estandarizar naming convention entre todas las cuentas
- Documentar reglas por cliente
- Revisión trimestral de reglas por cuenta
