# Auditoría Meta Ads — Checklist España

## Pre-Auditoría

### Cuestionario cliente

| # | Pregunta | Por qué |
|---|---|---|
| 1 | ¿Qué vendes y a qué precio? | Determina CAC permisible |
| 2 | ¿Valor medio deal / LTV? | Techo CAC = Deal Value × Margen |
| 3 | ¿Tasa cierre (lead → cliente)? | CPL permisible = CAC × Tasa cierre |
| 4 | ¿Show rate (llamadas/demos)? | Si 40%, la mitad de "booked calls" nunca pasa |
| 5 | ¿CPL / CPA / CAC objetivo? | Expectativa vs realidad |
| 6 | ¿Proceso de venta? | Determina qué eventos optimizar |
| 7 | ¿CRM + flujo leads? | HubSpot, Salesforce, GHL, spreadsheet |
| 8 | ¿Speed to lead (minutos)? | <5 min = best practice. >1h = leads mueren |
| 9 | ¿Historial bans/restricciones? | Afecta trust score cuenta |
| 10 | ¿Presupuesto mensual? | Determina arquitectura campaña |
| 11 | ¿Qué ha funcionado antes? | No matar lo que funciona |
| 12 | ¿Quién gestionaba antes? | Explica estructura actual |
| 13 | ¿Picos estacionales? | Ajustar estrategia budget/creativos |
| 14 | ¿Otros canales activos? | Afecta atribución |

**Cuenta nueva:** foco en preguntas 1-8 y 10. Reemplazar 11-12 con: "¿Qué marketing habéis hecho? ¿Fuente actual de leads?"

### Accesos necesarios

| Servicio | Nivel acceso | Coste |
|---|---|---|
| Meta Business Suite | Admin | Gratis |
| Meta Ads Manager | Admin (preferido) | Gratis |
| Meta Events Manager | Pixel Admin | Gratis |
| Google Analytics 4 | Analyst | Gratis |
| Google Tag Manager | Read | Gratis |
| CRM cliente | Read-only | Varía |
| Landing page platform | Analyst | Varía |
| Call tracking | Viewer | €40+/mes |
| Microsoft Clarity | Viewer | Gratis |

## 1. Salud Cuenta y Técnica

### Business Manager

| Check | Bien | Mal | Acción |
|---|---|---|---|
| Propiedad cuenta | BM del cliente es propietario | BM agencia anterior es propietario | Transferir |
| 2FA | Obligatorio todos admins | Sin 2FA | Activar inmediatamente |
| Admin backup | 2+ admins del cliente | 1 solo admin | Añadir backup |
| Propiedad página | Cliente es propietario | Agencia anterior/empleado | Reclamar |
| Dominio verificado | ✅ Verde | No verificado | Verificar DNS TXT |

### Pixel y CAPI

| Check | Bien | Mal | Acción |
|---|---|---|---|
| Pixel instalado | Dispara en todas las páginas clave | Falta en algunas páginas | Instalar/fix |
| CAPI activo | Eventos Server visibles en Events Manager | Solo eventos Browser | Implementar CAPI |
| EMQ | >6.0 "Good"/"Great" | <4.0 "Poor"/"OK" | Enviar más parámetros |
| Deduplicación | 1 conversión registrada (browser+server) | Conversiones duplicadas | Implementar event_id |
| Latencia eventos | <minutos | >1 hora | Fix pipeline automation |

### AEM

| Check | Bien | Mal | Acción |
|---|---|---|---|
| Eventos priorizados | Orden = valor negocio | Default o PageView arriba | Reconfigurar |
| Dominio verificado | ✅ | No | Verificar primero |
| Nº eventos | 3-5 cubriendo funnel | Solo 1 (Lead) | Añadir |

### Completitud tracking

| Método | ¿Trackeado? | ¿Envía a Meta? | ¿Dispara correcto? |
|---|---|---|---|
| Formularios web | | | |
| WhatsApp | | | |
| Llamadas (+34) | | | |
| Chat | | | |
| Calendario | | | |
| Email | | | |

**Pregunta crítica:** ¿Meta optimiza por el evento CORRECTO? Si optimiza "Lead" pero negocio valora "Booked Call" → cambiar optimization event.

### Historial cuenta

| Check | Bien | Mal |
|---|---|---|
| Account Quality | Sin restricciones | Restringida o calidad reducida |
| Policy violations | <5% ads rechazados | Rechazos repetidos mismo motivo |
| Change history (90 días) | Cambios estructurados, intencionales | Caos: cambios diarios, ediciones conflictivas |

### Facturación

| Check | Bien | Mal |
|---|---|---|
| Spend limit | Sin límite (o intencional) | Límite antiguo olvidado (€500 de test previo) |
| Método pago | Tarjeta válida, no expira pronto | Tarjeta a punto de expirar |
| Billing threshold | Alineado con gasto diario | Muy bajo generando cargos diarios |

## 2. Arquitectura Campañas

| Check | Bien | Mal | Acción |
|---|---|---|---|
| Nº campañas | 2-3 (testing + scaling + retargeting) | >6 compitiendo entre sí | Consolidar |
| % budget en learning | <25-30% | >50% permanente | Consolidar ad sets |
| Overlap audiencias | <30% entre campañas | >30% (compiten) | Separar o consolidar |
| Ad sets por campaña | 2-3 máx | >5 con <10 conv cada uno | Consolidar |
| Ads por ad set | 5-6 | >15 o <2 | Ajustar |
| Estructura Andromeda | Persona/concepto based | Formato based (video set, image set) | Reestructurar |

## 3. Audiencias

| Check | Bien | Mal | Acción |
|---|---|---|---|
| Tipo targeting | Broad (pixel maduro) | Intereses estrechos <100K | Broadening |
| Seeds LAL | Clientes/qualified leads, >1.000 | Page engagers o <200 | Mejorar seeds |
| LAL frescura | CRM actualizado <30 días | Upload de hace 6+ meses | Refrescar |
| Custom audiences | Auto-updating (pixel) | Solo listas estáticas | Configurar audiences dinámicas |
| Exclusiones | Clientes excluidos de prospecting | Sin exclusiones | Añadir |
| Advantage Detailed | OFF en B2B tight | ON cuando debería estar OFF | Ajustar |

## 4. Creativos

| Check | Bien | Mal | Acción |
|---|---|---|---|
| Diversidad formatos | Mix statics + video + carousel | 100% un formato | Diversificar |
| Related Media | OFF | ON | Desactivar |
| AI enhancements | OFF | ON | Desactivar |
| Frecuencia ads | <3 (prospecting 30d) | >3 | Nuevos creativos |
| Aspect ratios | 4:5 + 9:16 | Solo 1:1 | Crear versiones |
| Comentarios | Limpios o positivos | Negativos acumulados sin limpiar | Limpiar |
| Frescura | Creativos nuevos últimos 30 días | Mismos ads 3+ meses | Refresh |

## 5. Métricas

| Métrica | Evaluar | Bien | Mal |
|---|---|---|---|
| CPL | vs benchmark vertical España | En rango | >2× benchmark |
| ENCAC | vs Meta-reported CAC | Alineados (±20%) | Divergencia >50% |
| Frecuencia cuenta | 30 días | <2 | >3 |
| CPM | vs rango normal | €12-40 | >€80 o <€8 |
| CTR | Link clicks | >1% | <0.5% |
| Calidad leads (CRM) | Close rate real | >10% | <5% sin razón |
| Show rate | Calls booked → attended | >50% | <30% |

## 6. Funnel Post-Clic

| Check | Bien | Mal | Acción |
|---|---|---|---|
| Landing page speed | <3s load | >5s | Optimizar |
| Mobile responsive | Perfecto | Formulario roto en móvil | Fix urgente |
| Form length | 3-5 campos | >8 campos | Reducir |
| Speed to lead | <5 minutos | >1 hora | Configurar automation |
| Nurture sequence | Email/WhatsApp activada | Sin follow-up | Implementar |
| Show rate coaching | >50% | <30% | Mejorar confirmación/reminders |

## Red Flags — Acción Inmediata

- [ ] Spend limit antiguo bloqueando escalado
- [ ] Related Media ON (datos creativos ocultos)
- [ ] AI enhancements ON (rendimiento real oculto)
- [ ] Sin CAPI (10-30% señales perdidas)
- [ ] Optimizando evento equivocado (Lead vs Booked Call)
- [ ] Múltiples admins haciendo ediciones conflictivas sin protocolo
- [ ] Pixel duplicando conversiones
- [ ] Account quality reducida sin apelar
- [ ] WhatsApp no trackeado (10-30% leads España)
- [ ] Sin deduplicación browser/server
