# Mercado Español — Reddit Ads

## Penetración Reddit en España

- Reddit significativamente menos penetrado en España que en US/UK/CA/AU
- Perfil usuario español Reddit:
  - Técnico, joven (18-35), nivel educativo alto
  - Consume contenido mayoritariamente en inglés
  - Activo en subreddits temáticos internacionales más que locales
- Subreddits locales (r/spain, r/es, r/askspain) = audiencias pequeñas pero relevantes para servicios locales

### Implicaciones para Publicidad

| Aspecto | Impacto | Acción |
|---|---|---|
| Audiencias más pequeñas | Techo de escala más bajo | Monitorizar frequency de cerca. Saturación antes |
| Menor competencia publicitaria | CPCs potencialmente más bajos | Ventaja para early adopters |
| ICP técnico/educado | Encaja con perfil Reddit | B2B SaaS/tech = mejor fit |
| Consumo en inglés | Subreddits EN más efectivos para B2B | Ads en inglés para tech, español para local |

## Adaptación por Idioma

| Tipo negocio | Idioma ads recomendado | Por qué |
|---|---|---|
| B2B SaaS internacional | Inglés | Audiencia Reddit España consume EN. Subreddits EN más grandes |
| B2B SaaS local | Test ambos (A/B) | Depende del ICP específico |
| Developer tools | Inglés | Devs españoles en subreddits EN |
| Servicios profesionales local | Español | Audiencia local, subreddits ES |
| Info products español | Español | Mercado específicamente hispanohablante |

## IVA 21%

- **Reddit cobra en USD.** IVA se añade al billing
- CPC real = CPC × 1,21 = **€6,05** por cada €5 de CPC
- Incluir SIEMPRE IVA en cálculos unit economics
- Presupuesto €5.000/mes = ~€4.132 neto disponible para ads

## LOPD / GDPR

### Requisitos Específicos España

- **GDPR** (Regulación europea) + **LOPD** (Ley Orgánica Protección Datos española)
- **AEPD** (Agencia Española Protección Datos) = órgano supervisor. Multas hasta €20M o 4% facturación global
- **Tasa rechazo cookies España:** 40-60% de usuarios
- Consent Mode v2 obligatorio desde marzo 2024

### Impacto en Tracking Reddit

```
Alta tasa rechazo cookies en España
→ Reddit Pixel pierde 40-60% señales
→ Smart optimization degrada significativamente
→ CAPI server-side ESENCIAL (no optional) en España
```

### Checklist Compliance

- [ ] Cookie banner con opciones granulares (no dark patterns)
- [ ] Reddit Pixel condicional a consentimiento
- [ ] Consent Mode v2 implementado
- [ ] CAPI server-side configurado
- [ ] Privacy policy menciona Reddit como procesador datos
- [ ] PII siempre hasheado antes de enviar a Reddit
- [ ] Registro actividades tratamiento actualizado (AEPD)

## Estacionalidad España

| Período | Impacto Reddit | Acción |
|---|---|---|
| Enero (post-Navidad/Rebajas) | Nuevos presupuestos empresas. Tráfico recupera | Buen momento para lanzar |
| Febrero-Marzo | Normal-alto. Pre-Semana Santa | Ejecutar normalmente |
| Semana Santa | Variable. Turismo ↑, servicios B2B ↓ | Monitorizar, posible pausa B2B local |
| Abril-Junio | Normal-alto. Mejor trimestre para muchos sectores | Escalar si unit economics OK |
| Julio (rebajas verano) | Consumo sube, B2B empieza a bajar | Últimas semanas óptimas |
| **Agosto** | **BAJÓN FUERTE** — vacaciones masivas | **Reducir budget 30-50%.** Muchas empresas cierran |
| Septiembre ("vuelta al cole") | Recuperación fuerte post-vacaciones | Preparar campañas en agosto para lanzar septiembre |
| Octubre-Noviembre | Normal-alto. Pre-Black Friday | Incrementar gradualmente |
| Black Friday (último viernes nov) | CPMs suben por competencia ads | Aumentar budget si economics aguantan |
| Diciembre (Navidad) | Pico máximo consumo. B2B baja última semana | Máximo budget primeras 3 semanas |

### Festivos Nacionales España

1 enero, 6 enero (Reyes), Viernes Santo, 1 mayo, 15 agosto, 12 octubre (Fiesta Nacional), 1 noviembre, 6 diciembre (Constitución), 8 diciembre (Inmaculada), 25 diciembre

**Cada Comunidad Autónoma tiene 2-3 festivos adicionales propios.**

### Patrones de Comportamiento Semanal

- **3ª semana del mes = más débil** (antes de cobrar nómina)
- **Fin de mes + domingos = mejores para push** (post-cobro, tiempo libre)
- **Horario partido español:** 9:00-14:00 + 16:00-21:00 → reddit uso pico nocturno (21:00-01:00)

## Comportamiento del Consumidor Español

| Aspecto | Detalle | Impacto Reddit Ads |
|---|---|---|
| **WhatsApp > Email** | Preferencia comunicación comercial | Para local services, tracking WhatsApp clicks como conversión |
| **Bizum** | Creciente como método pago rápido | Relevante para servicios low-ticket |
| **Sensibilidad precio** | Alta en España. Precio = factor decisivo | Ofertas gratuitas funcionan especialmente bien |
| **Financiación** | 40-60% pagos en clínicas financiados | Mencionar opciones financiación en LPs |
| **Desconfianza publicidad** | Escépticos naturales (amplificado en Reddit) | Más razón para formato nativo, prueba por adelantado |

## Targeting Regional (Comunidades Autónomas)

- Reddit NO tiene geo-targeting granular por CC.AA.
- Solo targeting a nivel país (España) o exclusión por región
- Para servicios locales: Reddit NO es canal primario
- Madrid y Barcelona concentran mayor % usuarios Reddit España
- Si producto es nacional → Spain completa sin segmentar

## Benchmarks Estimados España (EUR)

| Vertical | CPC | CPL (frío) | CPL (RTG) | Notas |
|---|---|---|---|---|
| B2B SaaS self-serve | €3-5 | €40-80 | €15-35 | Sweet spot Reddit |
| B2B SaaS sales-led | €5-7 | €65-150 | €25-55 | Multi-touch necesario |
| Servicios profesionales | €5-7 | €85-200 | €30-70 | Solo si subreddits nicho existen |
| Info products | €3-5 | €25-70 | €12-35 | Reddit users consumen long-form |
| Consultoría high-ticket | €5-8 | €100-250 | €40-80 | Justificable si ACV >€25K |
| Developer tools | €2-4 | €30-60 | €10-25 | Mejor fit Reddit por audiencia |
| Fintech | €4-7 | €50-120 | €20-50 | Subreddits grandes y activos |

**Caveat:** Benchmarks son direccionales adaptados de datos US/global. Reddit no publica benchmarks específicos por país. Verificar contra rendimiento real tras 30 días. Menor competencia en España puede resultar en CPCs significativamente menores.

## Cross-Platform Comparación España

| Métrica | Reddit | LinkedIn | Meta | Google Search |
|---|---|---|---|---|
| CPC medio B2B | €4-6 | €8-18 | €2-4 | €3-15 |
| CPM medio | €4-10 | €28-55 | €7-14 | N/A |
| CTR medio | 0,3-0,8% | 0,4-0,7% | 0,8-1,5% | 3-8% |
| Lead quality (MQL→SQL) | 15-25% | 25-40% | 10-20% | 30-50% |
| Reach único B2B | 40% NO en LinkedIn | Standard | Más amplio | Intent-based |
| Mejor uso | Mid-funnel research, decision-makers anónimos, tech | ABM, enterprise, job-title targeting | Volumen, RTG, lookalikes | Bottom-funnel, intent alto |

## Expertos Referenciados

| Experto | Especialidad | Fuente |
|---|---|---|
| Cole (InterTeam Marketing) | Reddit Ads setup y ad groups | YouTube |
| Grace Close (Reddit) | B2B strategy, free-form ads, attribution | YouTube / Reddit oficial |
| Kevin Lord Barry (Right Percent) | SMB Reddit Ads strategy | YouTube |
| Nick Andrews (Marketing QL) | Creative testing vía Reddit | YouTube |
| Roman (Goji Berry AI) | Reddit organic marketing, SaaS growth | Starter Story |
| Brennan Tobin (Odd Duck Marketing) | Reddit market research con LLMs | YouTube |
| Paid Media Pros | Reddit 6-second video views | YouTube |
