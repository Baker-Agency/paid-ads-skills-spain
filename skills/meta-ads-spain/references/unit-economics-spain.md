# Unit Economics — Meta Ads España

## IVA 21% — Impacto en Cálculos

### Margen real

- Precio al consumidor incluye IVA 21%
- Servicio factura €1.000 → neto sin IVA = €826,45
- Margen real = (Precio sin IVA - Coste) / Precio sin IVA
- Fees agencia también llevan IVA → incluir en cálculo CAC

### IVA por sector

| Sector | Tipo IVA | Nota |
|---|---|---|
| Servicios generales | 21% | Standard |
| Hostelería, reformas vivienda | 10% | Reducido |
| Servicios sanitarios | Exento (muchos casos) | Verificar por actividad |
| Formación reglada | Exento | No aplica a cursos online no reglados |

### Precios en landing pages

- B2C: mostrar precio CON IVA (obligatorio por ley en España)
- B2B: habitual "desde X€ + IVA" (verificar normativa sector)
- Alinear precio en anuncio con precio en LP (discrepancia = rebote)

## Framework CAC Completo

### Fórmula base (lead gen)

```
CAC permisible = Valor deal × Margen bruto
CPL objetivo = CAC permisible × Tasa cierre × Show rate
```

### Ejemplo 1: Clínica dental (España)

| Paso | Métrica | Valor |
|---|---|---|
| Valor medio tratamiento | €800 (sin IVA: €661) | |
| Margen bruto | 60% | €397 margen |
| CAC permisible | | **€397** |
| Tasa cierre (lead → paciente) | 30% | |
| CPL objetivo | €397 × 30% | **€119** |
| Show rate | 70% | |
| CPL ajustado (con no-shows) | €119 × 70% | **€83** |

### Ejemplo 2: Coaching high-ticket (España)

| Paso | Métrica | Valor |
|---|---|---|
| Valor programa | €5.000 (sin IVA: €4.132) | |
| Margen bruto | 80% | €3.306 margen |
| ROAS target 3x | | CAC permisible = **€1.667** |
| Tasa cierre | 15% | |
| Calls para cerrar | 1/0.15 = 6.67 calls | |
| Coste por call permisible | €1.667 / 6.67 | **€250** |
| Show rate | 50% | |
| Cost per booking | €250 × 50% | **€125** |
| Booking rate | 25% | |
| CPL objetivo | €125 × 25% | **€31** |

### Ejemplo 3: SaaS B2B (España)

| Paso | Métrica | Valor |
|---|---|---|
| MRR | €200 (sin IVA: €165) | |
| LTV (24 meses avg) | €3.960 | |
| Margen bruto | 75% | €2.970 |
| CAC permisible (LTV:CAC 3:1) | | **€990** |
| Tasa cierre demo → cliente | 10% | |
| Demos para cerrar | 10 | |
| Coste por demo permisible | €990 / 10 | **€99** |
| Demo booking rate | 20% | |
| CPL objetivo | €99 × 20% | **€20** |

## Incluir Fees de Agencia

- Fee gestión mensual: €500-2.000 (España, según presupuesto)
- CAC real = (Gasto ads + Fee agencia) ÷ Clientes adquiridos
- Ejemplo: €3.000 ads + €800 fee = €3.800 / 10 clientes = **€380 CAC real**

## Benchmarks CPL Meta España (orientativos)

| Vertical | CPL estimado | CPM típico | Notas |
|---|---|---|---|
| Clínicas estéticas | €3-8 | €15-30 | Bajo CPL, alta competencia visual |
| Dental | €10-25 | €15-35 | Variable por tratamiento |
| Coaching / formación B2C | €4-16 | €12-25 | Alto volumen posible |
| Coaching / formación B2B | €20-40 | €20-40 | CPMs más altos, menor volumen |
| SaaS B2B | €25-65 | €25-50 | Ciclo venta largo |
| Servicios locales | €8-25 | €12-30 | Radio local, intent medio |
| Legal / abogados | €25-60 | €20-45 | Sector competitivo |
| Inmobiliaria | €15-45 | €15-35 | Muy estacional, SAC aplica |
| Info products | €3-12 | €10-20 | Alto volumen, bajo ticket |

**Referencia principal:** benchmark del cliente (su mejor período 30 días). Promedios industria = contexto secundario.

## Cuentas Nuevas: Expectativa de Costes

- CPMs iniciales más altos (pixel sin datos)
- Primeras 2-4 semanas: CPLs 30-50% por encima del objetivo
- Mejoría gradual conforme pixel aprende (50+ conversiones)
- NO juzgar rendimiento antes de 50 conversiones + 2 semanas mínimo
