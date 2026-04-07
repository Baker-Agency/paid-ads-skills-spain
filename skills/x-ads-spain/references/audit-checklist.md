# Auditoria de Cuentas — X Ads Espana

## Orden de auditoria (top-down)

Siempre auditar en este orden. No saltarse pasos.

### 1. Tracking de conversiones

| Check | Estado | Accion si falla |
|---|---|---|
| X Pixel instalado | ☐ | Instalar inmediatamente |
| Pixel disparando correctamente | ☐ | Verificar con X Pixel Helper |
| Eventos correctos configurados | ☐ | Mapear Lead/SignUp/Purchase |
| CAPI configurado | ☐ | Implementar (critico en Espana) |
| Deduplicacion Pixel/CAPI | ☐ | Configurar conversion_id |
| UTMs en todos los enlaces | ☐ | Anadir utm_source=x a todos |
| Conversiones llegando a Ads Manager | ☐ | Si no: revisar eventos y triggers |
| Conversiones coinciden con CRM | ☐ | Si no: tracking roto o incompleto |

**Si tracking esta roto, NO seguir auditando.** Arreglar tracking primero — todo lo demas es irrelevante sin datos fiables.

### 2. Settings de cuenta

| Check | Estado | Accion si falla |
|---|---|---|
| Modo Avanzado (no Simple) para campanas maduras | ☐ | Migrar a Avanzado |
| Ubicacion correcta (Espana / CC.AA.) | ☐ | Corregir geo-targeting |
| Idioma: Espanol | ☐ | Ajustar |
| Zona horaria: CET | ☐ | Corregir |
| 2FA activado | ☐ | Activar inmediatamente |
| Nomenclatura consistente | ☐ | Estandarizar nombres |

### 3. Estructura de campanas

| Check | Estado | Accion si falla |
|---|---|---|
| Objetivos correctos por campana | ☐ | Alinear objetivo con funnel stage |
| No duplicar audiencias entre campanas | ☐ | Diferenciar o fusionar |
| Retargeting activo | ☐ | Crear campana retargeting |
| Presupuesto distribuido segun rendimiento | ☐ | 70% a ganadoras, reducir perdedoras |
| Campanas con <7 dias no evaluadas prematuramente | ☐ | Esperar antes de decidir |

### 4. Grupos de anuncios

| Check | Estado | Accion si falla |
|---|---|---|
| Audiencias diferenciadas entre ad groups | ☐ | Evitar overlap |
| Keywords relevantes (si aplica) | ☐ | Revisar y limpiar |
| Negative keywords configuradas | ☐ | Anadir listas dia 1 |
| Exclusiones de audiencia activas | ☐ | Excluir clientes, converters |
| Tamano audiencia adecuado (20K-2M) | ☐ | Ajustar si muy grande o muy pequena |

### 5. Creativos

| Check | Estado | Accion si falla |
|---|---|---|
| Min 3 creativos activos por ad group | ☐ | Crear mas variaciones |
| Creativos con <30 dias de antiguedad | ☐ | **Refresh urgente** (fatiga) |
| Formato nativo (no parece anuncio) | ☐ | Rehacer en estilo tweet |
| Copy <100 caracteres | ☐ | Acortar |
| CTA unico y claro | ☐ | Simplificar |
| Video con subtitulos | ☐ | Anadir subtitulos |
| A/B testing activo | ☐ | Crear variaciones |
| CTR > 0,5% en todos los activos | ☐ | Pausar los que no, crear nuevos |

### 6. Pujas y presupuesto

| Check | Estado | Accion si falla |
|---|---|---|
| Puja alineada con fase de campana | ☐ | Auto al inicio, Target/Manual despues |
| Presupuesto diario se gasta (>80%) | ☐ | Si no: ampliar audiencia o subir puja |
| Sin sobregasto (>120% diario) | ☐ | Reducir puja o estrechar audiencia |
| CPC dentro de benchmark del sector | ☐ | Si no: revisar QS de anuncios |
| Sin campanas "zombi" (activas sin gasto) | ☐ | Pausar o diagnosticar |

## Red flags inmediatos

Cualquiera de estos requiere accion inmediata:

- [ ] **Sin X Pixel instalado** → todo el tracking esta ciego
- [ ] **Sin CAPI** → perdiendo 15-30% senales (critico en Espana)
- [ ] **Sin negative keywords** → gasto en clics irrelevantes
- [ ] **Creativos >30 dias sin refresh** → fatiga creativa segura
- [ ] **Targeting sin exclusiones** → pagando por audiencia que ya convirtio
- [ ] **Modo Simple en campanas maduras** → sin control de pujas ni frequency
- [ ] **Sin retargeting activo** → perdiendo conversiones warm
- [ ] **Presupuesto 50/50 entre campanas** → no aprovecha ganadores
- [ ] **Frequency >7 sin rotacion creativa** → quemando audiencia
- [ ] **0 conversiones en 7+ dias con gasto** → tracking roto o funnel roto

## Scoring de auditoria

| Area | Peso | Puntuacion |
|---|---|---|
| Tracking | 30% | /10 |
| Estructura campanas | 20% | /10 |
| Creativos | 25% | /10 |
| Targeting | 15% | /10 |
| Pujas/Presupuesto | 10% | /10 |
| **Total** | **100%** | **/10** |

**Interpretacion:**
- 8-10: Cuenta bien gestionada. Optimizacion fina
- 5-7: Oportunidades claras de mejora. Implementar cambios
- <5: Problemas estructurales. Reconstruir desde tracking

## Post-auditoria: plan de accion

### Prioridad 1 (esta semana)
- Arreglar tracking roto
- Instalar CAPI si no existe
- Crear negative keywords si no existen
- Pausar creativos con >30 dias

### Prioridad 2 (proximas 2 semanas)
- Restructurar campanas si necesario
- Crear nuevos creativos
- Configurar retargeting
- Implementar exclusiones

### Prioridad 3 (proximo mes)
- Optimizar pujas
- Probar nuevos formatos
- A/B testing sistematico
- Revisar estrategia de escalado
