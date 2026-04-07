# Diagnóstico y Troubleshooting — LinkedIn Ads

## Ads Stuck en Review (>48h)

| Paso | Acción |
|---|---|
| 1 | Revisar contenido del ad: ¿triggers de policy? (personal attributes, claims, restricted terms) |
| 2 | Duplicar y re-submit: crear copia del ad → submit nueva versión. A menudo limpia la cola |
| 3 | Editar y re-guardar: edición menor (añadir punto, ajustar spacing) → triggerea re-review |
| 4 | Contactar soporte: LinkedIn Ads help chat (CM → Help → Contact Us). Mejor en US business hours |
| 5 | LinkedIn rep: si tienes uno, mensaje directo. Normalmente resuelto mismo día |

**Prevención:** cuentas con historial limpio reciben reviews más rápidos. Minimizar rejections.

---

## Low Delivery / No Gasta Presupuesto

### Decision tree

| Síntoma | Check | Fix |
|---|---|---|
| Zero impresiones | ¿Campaign status = Active? ¿Ad aprobado? | Verificar status |
| Zero impresiones, ad aprobado | ¿Audiencia <1K? | Ampliar targeting. Mín ~1K para delivery |
| Impresiones pero muy pocas | ¿Bid demasiado bajo? | Subir bid. +10-15% diario hasta que delivery mejore |
| Impresiones cayendo | ¿Audience exhaustion? Verificar frecuencia | Expandir audiencia o rotar creativos |
| Gasta pero bajo diario | ¿Ad scheduling activo? (Sammy/automation) | Verificar si pausando fuera de horas |
| Gasta pero bajo diario | ¿Bid ceiling? ¿Competencia auction? | Subir bid o cambiar temporalmente a Maximum Delivery para diagnosticar |
| Caída súbita delivery | ¿Competidor entró? ¿Seasonal? | Check day-of-week patterns |

---

## Learning Phase

### Qué la triggerea
- Lanzamiento nueva campaña
- Cambio significativo presupuesto (>30%)
- Cambio estrategia de puja
- Cambio audiencia
- Nuevos ads añadidos

### Duración
- 1-7 días según volumen
- Necesita ~15-50 conversion events para salir

### Qué resetea
- Cambios mayores a budget (>30%), bid, audiencia u objetivo

### Durante learning phase
- Performance fluctúa — **NO hacer cambios**
- Si stuck en learning: presupuesto demasiado bajo → subir o cambiar a evento conversión mayor volumen (page view en vez de form submit)

---

## Audience Matching Failures

| Problema | Causa | Fix |
|---|---|---|
| Match rate <10% | Formato CSV incorrecto, campos required faltantes | Usar template LinkedIn. Required: email O company name + domain |
| "Processing" >48h | Archivo grande, delay servidor | Esperar 72h. Si persiste, re-upload. Máx 300K records/archivo |
| Audience <300 members | Pocos matches para servir ads | Subir lista más grande. Mín **300 matched members** |
| Audience no disponible en targeting | Cuenta incorrecta, audience building | Verificar cuenta correcta. Esperar 48h |
| Calidad declining | Listas stale (personas cambian trabajo/email) | Refresh cada **90 días**. Automatizar CRM → Zapier → LinkedIn |

---

## Frecuencia y Delivery Controls

- LinkedIn **NO ofrece** frequency capping manual
- Default: LinkedIn auto-maneja frecuencia
- **Monitor:** CM → Demographics → "Avg frequency"
- **Cold:** <7 imp/persona/30 días = saludable
- **RTG:** hasta 15/30 días aceptable
- **Frecuencia muy alta:** audiencia demasiado pequeña → expandir o pausar/rotar
- **Workaround:** campaign scheduling para controlar velocidad

---

## Campaign & Ad Status Reference

| Status | Significado | Acción |
|---|---|---|
| **Active** | Corriendo y entregando | Monitorizar |
| **Paused** | Pausado manualmente | Resumir cuando listo |
| **Draft** | Creado pero nunca lanzado | Completar setup |
| **Pending Review** | Enviado, esperando aprobación | Esperar 24-48h |
| **Not Approved** | Rechazado | Leer razón. Editar o apelar |
| **Completed** | End date pasada o presupuesto agotado | Renovar budget o extender fecha |
| **Canceled** | Campaign group cancelado | No se puede reactivar. Crear nueva |
| **Learning** | Optimización en progreso | NO cambiar settings. Esperar 1-7 días |

---

## Rejection Reasons Comunes

| Razón | Qué triggerea | Fix |
|---|---|---|
| **Personal attributes** | "¿Estás luchando con...?" o "Como CEO, sabes..." | Reframe: "Equipos que luchan con..." |
| **Claims sin sustento** | "Mejor del mercado", "#1 plataforma", "Resultados garantizados" | Eliminar superlativos o añadir fuente verificable |
| **Contenido misleading** | Clickbait, bait-and-switch (ad dice "gratis" pero LP cobra) | Ad copy = LP offer exactamente |
| **Profanity** | Palabras malsonantes | Eliminar. Conversation ads edgy → LinkedIn puede rechazar |
| **Imágenes baja calidad** | Borrosas, mucho texto overlay | Imágenes alta resolución, text overlay mínimo |
| **Destination mismatch** | URL rota, redirect chain, contenido no coincide | Verificar LP carga, coincide con ad, sin redirects excesivos |
| **Contenido prohibido** | Tabaco, drogas recreativas, armas, falsificaciones | No anunciar |
| **Data collection violations** | LGF recopilando datos sensibles (salud, etnia, política) | Solo recopilar datos relevantes a la oferta + privacy policy |

---

## Industrias Restringidas (Scrutiny Extra)

| Industria | Restricciones |
|---|---|
| **Servicios financieros** | Disclaimers obligatorios, sin returns garantizados, entidad licenciada |
| **Healthcare / Pharma** | Sin claims de enfermedades, sin curas milagro, limitaciones por geo |
| **Político / Advocacy** | Restringido o prohibido por región. **LinkedIn bloquea ads políticos en EU** |
| **Alcohol** | Permitido en algunos mercados con age-gating |
| **Gambling** | Muy restringido. Requiere licencia |
| **Educación** | For-profit bajo mayor scrutiny |
| **Cryptocurrency** | Varía por región. Requiere entidad registrada |

---

## Proceso de Apelación

1. CM → click ad rechazado → "Request Review" o "Edit Ad"
2. Timeline: 48-72h para review de apelación
3. Si primera apelación falla: editar ad para cumplir → re-submit como nuevo ad (más rápido que segunda apelación)
4. **Escalación:** contactar LinkedIn Ads support (chat o teléfono). Si tienes rep asignado → a través de él (mucho más rápido)
5. **Suspensión de cuenta:** contactar support inmediatamente. Documentación de negocio. Plan backup para continuidad

**Pattern:** múltiples rejections en misma cuenta → scrutiny aumentado en future ads. Mantener rejection rate bajo.

---

## LinkedIn Support Channels

| Canal | Acceso | Mejor para | SLA |
|---|---|---|---|
| **Help Center** | CM → ? → Help Center | Self-service, troubleshooting básico | Inmediato (docs) |
| **Chat Support** | CM → ? → Contact Us → Chat | Ad rejections, billing, bugs técnicos | Minutos a horas (business hours) |
| **Phone Support** | CM → ? → Contact Us → Phone | Suspensiones urgentes, errores billing | Minutos (business hours) |
| **LinkedIn Rep** | Asignado a cuentas >€10K/mes (varía) | Consejo estratégico, escalaciones, beta access | Mismo día |
| **Marketing Partner** | Agencias certificadas third-party | Integraciones avanzadas, API | Variable |

---

## Comparative Advertising

- LinkedIn permite ads comparativos con restricciones
- **Permitido:** comparaciones factuales verificables ("30% más rápido que media industria")
- **No permitido:** disparar competidores por nombre sin base factual, usar logos/marcas competidoras
- **Best practice:** framing "nosotros vs. método antiguo" o "nosotros vs. categoría" en vez de nombrar competidores
