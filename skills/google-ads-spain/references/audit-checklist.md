# Auditoría de Cuentas Google Ads — España

## Orden de Auditoría (top-down)

Siempre auditar en este orden. No saltar a LPs antes de verificar tracking.

### 1. Tracking de Conversiones
- [ ] GA4 vinculado y datos fluyendo
- [ ] Google Ads conversion tag directo (mejor que importar GA4)
- [ ] Auto-tagging activado
- [ ] Enhanced conversions activado
- [ ] Conversión counting: "Una" para lead gen
- [ ] Call tracking configurado (duración mínima 30-60s, formato +34)
- [ ] OCI configurado (si aplica — >€5K/mes gasto)
- [ ] Todos los métodos trackeados (forms, calls, chat, calendar, WhatsApp)
- [ ] Consent mode v2 implementado (obligatorio EEE)
- [ ] Sin conversiones duplicadas
- [ ] Tag Assistant verifica disparo correcto
- [ ] Microsoft Clarity instalado (triangulación)

### 2. Settings de Cuenta
- [ ] Location targeting: "Presencia" only (NO "Presencia o interés")
- [ ] Auto-Apply Recommendations: DESACTIVADO
- [ ] Search Partners: verificar rendimiento (apagar si malo; siempre off en Microsoft Ads)
- [ ] Display Network: DESACTIVADO en campañas Search
- [ ] Inventory type: "Limited inventory" para brand safety
- [ ] Content exclusions: sensitive categories excluidas
- [ ] Idioma: solo español (uno por campaña)
- [ ] Zona horaria: Madrid (CET/CEST)

### 3. Estructura de Campañas
- [ ] ¿Demasiadas campañas fragmentando datos? → consolidar
- [ ] ¿Campañas con <15 conversiones/mes? → combinar
- [ ] ¿SKAGs? → migrar a Single Keyword Themes
- [ ] ¿Campañas por dispositivo? → eliminar (fragmenta Smart Bidding)
- [ ] 4 razones válidas para campañas separadas: diferente ubicación, presupuesto, objetivo conversión, bid strategy. Todo igual → consolidar
- [ ] Shared budget + shared bid strategy: considerar como alternativa a consolidación total

### 4. Pujas y Estrategia
- [ ] ¿Bid strategy alineada con volumen conversiones? (ver progresión pujas)
- [ ] ¿Brand campaign en Manual CPC o Target IS? (NO Smart Bidding)
- [ ] ¿Portfolio bidding con Max CPC cap? (si tCPA)
- [ ] ¿PMax con Search Themes? → verificar que no canibaliza Search campaigns
- [ ] ¿PMax sin OCI? → red flag para lead gen

### 5. Keywords y Negativas
- [ ] 3 listas negativas configuradas (basura, competidores, marca)
- [ ] Negativas actualizadas (no meses sin revisar)
- [ ] Match types apropiados para volumen/presupuesto
- [ ] Search terms report: ¿tráfico relevante?
- [ ] ¿Broad match sin Smart Bidding? → red flag

### 6. Anuncios
- [ ] Mínimo 3 variaciones RSA por ad group
- [ ] Pinning correcto (H1=intent, H2=diferenciador, H3=CTA)
- [ ] Extensions/assets: sitelinks, callouts, structured snippets, call, location
- [ ] ¿Assets automáticos activados sin revisión? → desactivar o revisar

### 7. Landing Pages
- [ ] Velocidad: <3 segundos carga (idealmente <2s)
- [ ] Alineación keyword → anuncio → LP (trinidad coherente)
- [ ] Formulario visible above the fold
- [ ] Teléfono +34 visible y clickable
- [ ] WhatsApp button (España: muy usado)
- [ ] Responsive mobile
- [ ] Prueba social (testimonios, logos, números)

## Red Flags Inmediatos

Cosas que NUNCA deberían estar así:
- Location "Presencia o interés" (defecto Google → clicks fuera de zona)
- Search Partners ON sin análisis rendimiento
- Auto-Apply Recommendations ON
- Conversiones contando "Todas" (lead gen solo "Una")
- Sin listas keywords negativas
- PMax sin OCI para lead gen
- Múltiples conversiones duplicadas contando
- Manual CPC + Search Partners = spam trap
- Broad match + zero datos conversión = quemando presupuesto

## Discovery Questions (Cliente Español)

### Negocio
- ¿Qué servicios/productos ofreces?
- ¿En qué zonas de España operas? ¿Nacional o local?
- ¿Cuál es tu ticket medio? ¿Con o sin IVA?
- ¿Tasa de cierre lead → cliente?
- ¿CRM usado? ¿Integrado con Google Ads?
- ¿Financiación para clientes? (común en España)

### Marketing actual
- ¿Presupuesto mensual ads? ¿Incluye gestión o solo media?
- ¿Quién gestiona actualmente? (in-house, agencia, freelance)
- ¿Otros canales activos? (Meta, LinkedIn, SEO)
- ¿Estacionalidad de tu negocio? ¿Agosto = bajón?
- ¿Competidores principales?

### Tracking y tech
- ¿CMS de la web? (WordPress, Webflow, custom)
- ¿Formulario de contacto tool? (CF7, Typeform, nativo)
- ¿Call tracking implementado?
- ¿WhatsApp Business API o solo link?
- ¿GA4 configurado?
- ¿Consent mode / banner cookies LOPD?
- ¿Google Business Profile verificado? (si local)

## Google Ads Link Checker

- Herramienta built-in en Google Ads Editor (menú Tools)
- Testea todas las final URLs activas de la cuenta
- Settings: check "active items only" para evitar falsos positivos de ads pausados
- Limitación: no dice QUÉ anuncio/sitelink tiene la URL rota — filtrar manualmente por "final URL = X"
- Ejecutar mensualmente

## Competitive Intelligence

- Auction Insights: quién compite contigo, su IS, overlap rate
- Google Ads Transparency Center: ver anuncios activos de competidores
- SpyFu para dominios .es: keywords y estimaciones gasto competidores
- Incognito search: verificar si competidores pujan por tu marca
- Si zero competidores en brand → testear pausar campaña brand 4 semanas

## Triage STAB Framework

Clasificar hallazgos de auditoría:

| Color | Significado | Acción |
|---|---|---|
| 🔴 Rojo | Problema crítico que daña rendimiento activamente | Fix inmediato (tracking roto, settings incorrectos) |
| 🟠 Naranja | Oportunidad perdida significativa | Fix en primera semana |
| 🟢 Verde | Mejora incremental | Implementar cuando haya bandwidth |

## Auditoría de Cuenta Existente (Onboarding)

### Paso 1: Acceso y datos históricos
- Solicitar acceso admin a Google Ads + GA4
- Exportar últimos 6-12 meses de datos
- Revisar change history (¿quién hizo qué, cuándo?)

### Paso 2: Snapshot rápido
- Performance últimos 30/90/365 días
- Top campañas por gasto y por conversiones
- CPA trend: ¿mejorando o empeorando?
- Impression share: ¿margen de crecimiento?

### Paso 3: Auditoría completa (checklist arriba)

### Paso 4: Presentar hallazgos
- Usar triage STAB
- Priorizar rojos primero
- Dar timeline estimado de implementación
- Alinear expectativas con cliente
