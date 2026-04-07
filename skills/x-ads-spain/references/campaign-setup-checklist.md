# Campaign Setup Checklist — X Ads Espana

## Pre-lanzamiento (antes de activar)

### 1. Tracking

- [ ] X Pixel instalado en web (via GTM o directo)
- [ ] Eventos configurados: PageView, Lead, SignUp, Purchase (los que apliquen)
- [ ] Pixel verificado con X Pixel Helper (extension Chrome)
- [ ] CAPI configurado (recomendado para Espana por alta tasa rechazo cookies)
- [ ] Deduplicacion Pixel/CAPI con `conversion_id` coincidente
- [ ] UTMs definidos para analytics: `utm_source=x&utm_medium=paid&utm_campaign=[nombre]`
- [ ] Google Analytics / GA4 recibiendo trafico de test

### 2. Cuenta

- [ ] Autenticacion 2FA activada
- [ ] Metodo de pago en EUR
- [ ] Zona horaria: CET (Europe/Madrid)
- [ ] Accesos de equipo configurados (roles: Admin, Campaign Manager, Analyst)

### 3. Nomenclatura

**Formato:** `[Objetivo]_[Audiencia]_[Ubicacion]_[Formato]_[Fecha]`

Ejemplos:
- `LeadGen_SaaS-B2B_Spain_Image_202604`
- `Awareness_Tech-Keywords_Madrid_Video_202604`
- `Retargeting_WebVisitors_Spain_Carousel_202604`

### 4. Estructura inicial

```
Cuenta
└── Campana 1: [Objetivo principal]
    ├── Ad Group A: [Audiencia 1 — ej. keyword targeting]
    │   ├── Anuncio 1 (imagen)
    │   ├── Anuncio 2 (video)
    │   └── Anuncio 3 (texto nativo)
    ├── Ad Group B: [Audiencia 2 — ej. follower look-alikes]
    │   ├── Anuncio 1
    │   ├── Anuncio 2
    │   └── Anuncio 3
    └── Ad Group C: [Retargeting — website visitors]
        ├── Anuncio 1
        └── Anuncio 2
```

## Settings de campana

### Modo Simple vs Avanzado

| Setting | Simple | Avanzado |
|---|---|---|
| Objetivos | Reach, Engagement, Traffic, Keywords | Awareness, Consideration, Conversion |
| Control pujas | No | Si (auto, manual, target) |
| Placement control | No | Si |
| Frequency cap | No | Si |
| Programacion horaria | No | Si |
| Recomendado para | Testing rapido, principiantes | Control total, campanas maduras |

### Checklist de settings (Avanzado)

- [ ] **Objetivo:** alineado con funnel
  - Awareness → brand reach
  - Consideration → trafico web, video views, engagement
  - Conversion → leads, signups, app installs
- [ ] **Ubicacion:** Espana (o CC.AA. especificas)
- [ ] **Idioma:** Espanol
- [ ] **Edad:** 25-54 (ajustar segun sector)
- [ ] **Dispositivos:** Todos (a menos que haya razon para filtrar)
- [ ] **Placement:** Home Timeline + Search Results (excluir Profiles si presupuesto bajo)
- [ ] **Presupuesto diario:** minimo €20-50/dia para datos suficientes
- [ ] **Puja:** Automatica al inicio
- [ ] **Programacion horaria:** Lun-Vie 9:00-23:00 CET (o 24/7 si presupuesto permite)
- [ ] **Frequency cap:** 3-5 impresiones/usuario/dia (evitar fatiga)

## Keywords negativas (dia 1)

Si usas keyword targeting, preparar ANTES de activar:

### Lista 1: Terminos basura (espanol)

gratis, free, crack, pirata, descargar, torrent, tutorial basico, que es, como hacer, wikipedia, empleo, trabajo, becas, practicas, sueldo, salario, oposiciones

### Lista 2: Competidores (si no quieres aparecer)

Nombres de marca de competidores directos

### Lista 3: Terminos no comerciales

meme, broma, chiste, troll, hate, queja, estafa, timo, fraude

## Creativos minimos para lanzar

| Formato | Minimo | Recomendado |
|---|---|---|
| Variaciones de copy | 2 | 3-5 |
| Imagenes unicas | 2 | 3-4 |
| Videos (si aplica) | 1 | 2-3 |
| Formatos distintos | 1 | 2 (ej. imagen + video) |

**Regla:** nunca lanzar con un solo creativo. Minimo 3 variaciones para A/B testing.
