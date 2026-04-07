# Diagnostico y Troubleshooting — X Ads Espana

## Zero conversiones

### Orden de diagnostico (seguir en secuencia)

#### 1. Tracking roto (causa mas comun)

| Check | Como verificar |
|---|---|
| X Pixel instalado | X Pixel Helper (extension Chrome) |
| Pixel disparando en pagina conversion | Navegar a thank you page → verificar evento |
| Evento correcto configurado | X Ads Manager → Eventos |
| CAPI enviando datos | Verificar en server logs o Ads Manager |
| Consent mode no bloqueando | Probar aceptando cookies → verificar |
| UTMs llegando a GA4 | Revisar Acquisition → Source/Medium |

**Si tracking roto:** arreglar ANTES de cualquier otra optimizacion. Sin datos fiables, todo cambio es a ciegas.

#### 2. Trafico equivocado

| Check | Como verificar |
|---|---|
| Keywords relevantes | Revisar que keywords generan clics |
| Audience demographics | Ads Manager → Analytics → Demographics |
| Landing page alineada | ¿El anuncio promete lo que la LP ofrece? |
| Exclusiones activas | ¿Llegan clics de audiencia no deseada? |

**Senales de trafico equivocado:**
- CTR alto pero 0 conversiones = clics curiosos, no compradores
- Bounce rate >80% en LP = desalineacion anuncio-LP
- Tiempo en pagina <10s = audiencia irrelevante

#### 3. Fatiga creativa

| Check | Como verificar |
|---|---|
| Frequency >5 | Ads Manager → Delivery metrics |
| CTR cayendo vs primera semana | Comparar periodos |
| Creativos >14 dias activos | Revisar fecha de creacion |

**Solucion:** rotar creativos inmediatamente. 5-8 activos minimo.

#### 4. Landing page (solo si 1-3 estan bien)

| Check | Como verificar |
|---|---|
| Velocidad carga <3s | Google PageSpeed Insights |
| Mobile optimizada | Test en movil real |
| Formulario visible above the fold | Test visual |
| CTA claro y unico | Test visual |
| Coherencia anuncio → LP | ¿Mismo mensaje, misma oferta? |

## CPL alto — 5 factores

### 1. CPC alto

| Causa | Diagnostico | Solucion |
|---|---|---|
| Competencia estacional | Octubre-Diciembre = CPM +20-50% | Ajustar expectativas o reducir |
| Audiencia saturada | Frequency >5 | Ampliar audiencia o rotar creativos |
| QS bajo (relevancia) | CTR <0,3% | Mejorar copy y targeting |
| Puja demasiado alta | CPC >> benchmark sector | Bajar target bid gradualmente |

### 2. CTR bajo

| Causa | Diagnostico | Solucion |
|---|---|---|
| Copy debil | CTR <0,5% tras 1.000 impresiones | Rehacer copy: hook + beneficio |
| Formato incorrecto | Video con 0 engagement | Probar imagen o texto |
| Audiencia equivocada | CTR bajo en todos los creativos | Cambiar keywords/intereses |
| Fatiga | CTR bajo este % semana anterior | Rotar creativos |

### 3. CVR landing bajo

| Causa | Diagnostico | Solucion |
|---|---|---|
| Desalineacion | Bounce >80% | Alinear copy LP con anuncio |
| Formulario largo | Abandonos en form | Reducir campos (nombre + email + telefono max) |
| Carga lenta | >3s mobile | Optimizar velocidad |
| Sin prueba social | Visitantes no confian | Anadir testimonios, logos clientes |
| CTA debil | Clicks en LP pero no en form | CTA mas claro, above the fold |

### 4. Targeting demasiado amplio

| Causa | Diagnostico | Solucion |
|---|---|---|
| Sin keywords negativas | Clics irrelevantes | Anadir listas negativas |
| Intereses genericos | Audiencia >2M sin exclusiones | Estrechar con keywords + exclusiones |
| Sin exclusion converters | Pagando por leads existentes | Crear tailored audience exclusion |

### 5. Sin retargeting

- Si solo haces prospecting: pierdes 20-30% conversiones de usuarios warm
- Solucion: crear campana retargeting con website visitors (7-30 dias)
- Presupuesto retargeting: 20-30% del total

## Anuncios rechazados

### Causas comunes en X

| Razon | Solucion |
|---|---|
| Contenido enganoso | Alinear promesa con realidad |
| Claims de salud no aprobados | Eliminar claims medicos directos |
| Lenguaje ofensivo | Revisar copy |
| URL rota | Verificar destino |
| Imagen con texto excesivo | Reducir texto en imagen |
| Sector restringido sin aprobacion | Solicitar aprobacion previa |

### Sectores que requieren aprobacion previa en X

- Salud y farmaceutico
- Servicios financieros
- Politica
- Alcohol
- Apuestas/juegos de azar
- Criptomonedas

## Gasto insuficiente (campana no entrega)

| Causa | Diagnostico | Solucion |
|---|---|---|
| Audiencia muy pequena | <5.000 usuarios | Ampliar targeting |
| Puja demasiado baja | No ganas subastas | Subir puja o cambiar a automatica |
| Creativo rechazado | Ads Manager muestra "Under review" | Esperar o editar y reenviar |
| Presupuesto muy bajo | <€5/dia | Aumentar a minimo €10-20/dia |
| Frequency cap muy estricto | <2 imp/dia | Relajar a 3-5/dia |

## Cadena de reaccion de tracking roto

```
Pixel/CAPI roto → Conversiones reportadas a la mitad
→ Smart Bidding optimiza con senal parcial
→ Pujas se ajustan hacia audiencia incorrecta
→ Trafico peor → Conversiones reales caen
→ CPL sube → Presupuesto parece ineficiente
→ Espiral descendente
```

**Fix:** auditar tracking mensualmente. Verificar que conversiones en X Ads Manager coinciden (±10%) con CRM real.

## Checklist de diagnostico rapido (5 minutos)

1. ¿Pixel/CAPI disparando? → Si no: arreglar ya
2. ¿Gasto = presupuesto diario? → Si no: audiencia o puja
3. ¿CTR > 0,5%? → Si no: creativo
4. ¿Frequency < 5? → Si no: fatiga
5. ¿Conversiones = CRM? → Si no: tracking
6. ¿CPL < objetivo? → Si no: optimizar por jerarquia
