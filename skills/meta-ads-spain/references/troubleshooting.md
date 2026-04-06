# Troubleshooting — Meta Ads

## Zero o Baja Entrega — Checklist 9 Pasos

**Según AdKit:**

### 1. Status Jerarquía
- **Campaign:** debe ser "Active" (no Off, Paused, Error)
- **Ad Set:** activo, con schedule vivo y presupuesto
- **Ad:** aprobado y activo (no Disapproved, In Review, Paused)
- Un problema a cualquier nivel para entrega downstream

### 2. Audiencia Demasiado Pequeña
- **Síntomas:** ad set "Active" pero zero/low impressions
- **Causa:** targeting (demographics, interests, custom audiences, exclusiones) demasiado estrecho
- **Fix:** ampliar geo, eliminar intereses restrictivos, reducir exclusiones
- **Mínimo:** 100.000+ para entrega estable (retargeting puede ser menor)

### 3. Puja Demasiado Baja (Pujas Manuales)
- **Síntomas:** low/zero impressions sin warnings targeting
- **Causa:** cost cap, bid cap o minimum ROAS demasiado bajo para ganar subastas
- **Fix:** cambiar a Advantage Campaign Budget o Lowest Cost temporalmente. Si entrega, incrementar cost cap gradualmente

### 4. Anuncio Rechazado
- **Síntomas:** status "Disapproved"
- **Causa:** violación políticas en creativo o landing page
- **Fix:** ver razón clic en badge. Editar ad (auto-resubmit). "Request Review" si es false positive

### 5. Cuenta Restringida
- **Síntomas:** zero entrega en TODAS las campañas + warning nivel cuenta
- **Causa:** policy violations, problemas pago, actividad sospechosa
- **Fix:** ver Account Quality. Fix issues + apelar. Ver sección Bans abajo

### 6. Campaña/Ad Set Pausado Accidentalmente
- **Síntomas:** status "Off" cuando debería correr
- **Causa:** error humano, bulk edits, reglas automatizadas pausando
- **Fix:** verificar toggle en Campaign level (no solo Ad Set). Revisar Automated Rules. Verificar end date

### 7. Learning Phase Estancada
- **Síntomas:** "Learning" status 7+ días con entrega muy baja
- **Causa:** algoritmo necesita ~50 optimization events/semana. Budget bajo, audiencia pequeña, evento raro
- **Fix:**
  - Aumentar presupuesto diario
  - Optimizar por evento mayor volumen (clicks, add-to-cart) si conversiones muy caras
  - Consolidar ad sets (menos = más data por ad set)
  - **NO editar** campañas activas — cambios resetean learning

### 8. Presupuesto Bajo para el Evento
- **Síntomas:** "Learning Limited" o entrega escasa
- **Causa:** presupuesto muy bajo vs coste del evento (€20/día para CPA €200 = 1 conversión cada 10 días)
- **Fix:**
  - Presupuesto diario = 2-3× CPA objetivo (ej: €400-600/día para CPA €200)
  - O optimizar por evento más alto en funnel

### 9. Problemas Facturación
- **Síntomas:** caída repentina a zero en todas las campañas + warning billing
- **Causa:** tarjeta rechazada, límite crédito, umbral impagado
- **Fix:** actualizar método pago en Billing. Añadir tarjeta backup. Pagar balance. Ads se reactivan automáticamente en horas

### 10. Pérdida Señal iOS
- **Síntomas:** menor eficiencia entrega + conversiones perdidas post-iOS ATT
- **Causa:** opt-outs iOS restringen tracking conversión Meta
- **Fix:**
  - Implementar CAPI
  - Verificar dominio en Business Manager
  - Configurar top 8 eventos en AEM

## Bans de Cuenta Meta

### Triggers Principales (2026)

**Según Unknown (March 2026 update):**
- Meta reemplaza equipos review humanos con AI → oleadas de false positive bans

| Trigger | Riesgo |
|---|---|
| Conectar herramientas automation vía API (Zapier, bots AI) | Alto |
| IPs inconsistentes (VPN on/off frecuente) | Alto |
| 100% contenido generado por AI | Alto |
| Perfiles sin actividad orgánica | Medio-alto |
| Violaciones políticas repetidas | Alto |
| Problemas pago recurrentes | Medio |

### Plantilla Apelación (AI Reviewer)

Primera apelación la lee AI, no humano. NO usar lenguaje emocional o negativo.

> "Creemos que esta restricción puede haber sido aplicada por error. Nos tomamos esto muy en serio. Queremos cumplir con las políticas. Agradeceríamos una revisión manual de esta cuenta. Gracias."

Si conoces la razón exacta (ej: conectar herramienta automation), mencionarlo explícitamente y prometer no repetirlo.

### Escalación (si apelación falla)

| Método | Detalle | Éxito |
|---|---|---|
| Meta Account Rep | Pedir al representante asignado que escale manualmente | Medio (solo escalan, no arreglan) |
| **Meta Verified** | Pagar suscripción → ticket soporte directo | **Más exitoso** |
| Escalación indirecta | Chat soporte por otro problema (billing, cuenta hackeada) → bypass loops automatizados | Medio |

### Mitigación Emergencia

Si perfil completamente restringido y ads siguen corriendo:
- **Backdoor Instagram:** login a Meta Business Suite vía cuenta Instagram → posible acceso para pausar ads
- **Corte financiero:** si ads no rentables y no puedes acceder → cancelar tarjeta asociada para detener gasto inmediatamente

### Prevención

- [ ] No conectar APIs/bots durante oleadas de bans
- [ ] IP consistente (si VPN, mantenerla SIEMPRE ON)
- [ ] Actividad orgánica mínima en perfil personal
- [ ] SIEMPRE 2+ admins en Business Manager
- [ ] Creativos AI < 50% del total de la cuenta
- [ ] No operar BM con solo 1 admin (1 persona se va = account locked)
- [ ] Mantener políticas limpias (no reincidencia)

## Diagnóstico CPM Alto

| CPM rango | Significado | Acción |
|---|---|---|
| €8-12 | Bajo. Audiencias broad en verticales no competitivos | Verificar calidad targeting. CPM bajo + CPL alto = personas equivocadas |
| €12-40 | Normal lead gen España | Baseline. Comparar vs propio histórico |
| €40-80 | Alto. Vertical competitivo (finanzas, legal), Q4, audiencia estrecha | Check si vertical lo justifica. Broadening puede reducir |
| €80-250+ | Muy alto. Posible shadowban, calidad dominio, restricción | Investigar: domain quality, account restrictions, page quality, feedback negativo ads |

## Diagnóstico CPL Alto

### Orden diagnóstico (de más probable a menos)

1. **Tracking roto** — ¿Todos los métodos conversión trackeando? ¿CAPI activo? ¿Deduplicación? (causa #1)
2. **Creativo agotado** — ¿Frecuencia >3? ¿Mismos ads 3+ meses? → refresh creativo
3. **Audiencia saturada** — ¿Reach incremental decayendo? → expandir audiencia o nuevos conceptos
4. **Landing page** — ¿Velocidad >3s? ¿Mobile roto? ¿Form largo? → CRO
5. **Oferta débil** — ¿Competencia tiene mejor propuesta? ¿Pricing fuera de mercado? → revisar oferta
6. **Estacionalidad** — ¿Agosto? ¿3ª semana mes? → ajustar expectativas
7. **Pujas** — ¿Bid cap demasiado bajo/alto? → último recurso

## Frecuencia Alta — Diagnóstico

| Frecuencia | Tipo campaña | Significado | Acción |
|---|---|---|---|
| >3 (30d) | Prospecting | Audiencia agotada o creativos insuficientes | Expandir audiencia + nuevos creativos |
| >5 (30d) | Retargeting | Pool exhausted | Reducir presupuesto retargeting, expandir ventana, nuevos creativos |
| >2 (7d) | Cualquiera | Urgente | Acción inmediata: pausar peores, añadir nuevos |
