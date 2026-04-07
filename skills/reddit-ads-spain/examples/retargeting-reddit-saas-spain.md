# Ejemplo: Retargeting Reddit para SaaS — España

## Escenario

- **Producto:** SaaS de gestión de proyectos para agencias
- **ACV:** €3.600/año (€300/mes)
- **Situación:** Ya tiene Google Ads + Meta funcionando. 5.000 visitantes web/mes
- **Objetivo:** Usar Reddit SOLO como retargeting barato (no prospecting)
- **Presupuesto Reddit:** €1.500/mes

## Por Qué Solo Retargeting

- ACV €3.600 con tasa cierre 8% → CPL max €288 × 8% = **€23** (muy ajustado para prospecting frío)
- Reddit prospecting CPC ~€5 con CVR 4% = CPL €125 (>5x el max viable)
- **Pero:** Retargeting CVR 10-18% → CPL €28-50 → €28 está casi dentro de target
- Con audiencia warm de 5.000 visitantes/mes → pool retargeting Reddit ~750-1.250 usuarios

## Arquitectura Mínima

| Campaña | Budget | Ad Groups |
|---|---|---|
| RTG - Conversiones | €1.500/mes (€50/día) | AG1: Site visitors 7d - Desktop (€25/día). AG2: Site visitors 8-30d - All Devices (€25/día) |

## Creativos Retargeting (diferentes a prospecting)

### Ad 1: Case Study (Imagen)
- Headline: "Cómo [Agencia Cliente] redujo el tiempo de gestión proyectos un 40%"
- Imagen: Screenshot dashboard con métricas reales
- CTA: "Ver caso de estudio completo"

### Ad 2: Social Proof (Free-form text)
- "Más de 500 agencias en España usan [Producto] para gestionar sus proyectos. Aquí van los 3 features que más les sorprenden..."
- Listar features con datos específicos
- CTA: "Si ya lo viste en nuestra web, pruébalo gratis 14 días"

### Ad 3: Objeción Handler (Free-form text)
- "Las 5 excusas más comunes para NO cambiar de herramienta de gestión de proyectos (y por qué no aplican)"
- Abordar objeciones: migración datos, curva aprendizaje, precio, "ya tenemos Excel", integrations
- CTA soft: "Link en comentarios si quieres probar sin compromiso"

## Ventajas Retargeting Reddit vs Meta

| Aspecto | Reddit | Meta |
|---|---|---|
| CPC retargeting | €2-4 | €1-3 |
| CVR retargeting | 10-18% | 8-15% |
| CPL retargeting | €15-35 | €10-25 |
| Diferenciador | Audiencia ya investigando, formato nativo, comentarios activos | Mayor reach, mejor frequency control |
| Complementariedad | Reddit captura research phase post-web visit | Meta captura social browsing phase |

## Métricas Esperadas

| Métrica | Target Mensual |
|---|---|
| Gasto | €1.500 |
| Impresiones RTG | ~50K-80K |
| Clics | ~200-350 |
| CVR LP | 12-15% |
| Leads | 25-40 |
| CPL | €38-60 |
| CPA (con 8% close) | €475-750 |

## Notas

- **Conversations placement:** Testear "conversations only" para retargeting — per Cole, delivery suele ser mejor para audiencias pequeñas
- **Desktop-only AG1:** B2B convierte 2-3x mejor en desktop en Reddit
- **Frequency cap:** Monitorizar de cerca. Con pool ~1.000 usuarios, frequency sube rápido. Cap mental: <8x por 7 días
- **Refrescar creativos:** Cada 2-3 semanas. Pool pequeño = fatiga rápida
- **CAPI esencial:** Con pool pequeño, cada conversión perdida por cookies rechazadas pesa mucho. Implementar CAPI desde el día 1
