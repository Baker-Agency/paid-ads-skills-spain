<p align="center">
  <img src="header-readme.gif" alt="Baker Agency" width="100%">
</p>

# Skills de Paid Ads para Agentes IA — Mercado Español

Colección de skills para agentes IA especializadas en gestión de campañas de publicidad de pago en el mercado español (España). Para agencias, freelancers y equipos in-house que gestionan PPC para lead gen, SaaS y servicios.

Compatible con Claude Code, OpenAI Codex, Cursor, Windsurf y cualquier agente que soporte la [Agent Skills spec](https://agentskills.io).

Creado por [Baker Agency](https://withbaker.com).

## ¿Qué son las Skills?

Las skills son archivos markdown que dan a los agentes IA conocimiento especializado y workflows para tareas específicas. Al añadirlas a tu proyecto, tu agente reconoce cuándo estás trabajando en paid ads y aplica los frameworks, benchmarks y mejores prácticas correctos — adaptados al mercado español.

## Skills Disponibles

| Skill | Descripción |
|-------|-------------|
| [google-ads-spain](skills/google-ads-spain/) | Gestión completa de Google Ads para España. Setup, optimización, escalado y auditoría de campañas para lead gen, SaaS y servicios. Incluye progresión de pujas, Quality Score, copy en español, tracking GDPR/LOPD, calendario estacional y targeting por CC.AA. |

### Próximamente

- `meta-ads-spain` — Meta Ads (Facebook/Instagram) para el mercado español
- `linkedin-ads-spain` — LinkedIn Ads para B2B en España
- `tiktok-ads-spain` — TikTok Ads para el mercado español

## Instalación

### Opción 1: CLI (Recomendado)

Usa [npx skills](https://github.com/vercel-labs/skills) para instalar directamente:

```bash
# Instalar todas las skills
npx skills add Baker-Agency/paid-ads-skills-spain

# Instalar una skill específica
npx skills add Baker-Agency/paid-ads-skills-spain --skill google-ads-spain

# Listar skills disponibles
npx skills add Baker-Agency/paid-ads-skills-spain --list
```

Se instala automáticamente en `.agents/skills/` (y crea symlinks en `.claude/skills/` para compatibilidad con Claude Code).

### Opción 2: Plugin de Claude Code

Instalar vía el sistema de plugins de Claude Code:

```bash
# Añadir el marketplace
/plugin marketplace add Baker-Agency/paid-ads-skills-spain

# Instalar todas las skills
/plugin install paid-ads-skills-spain
```

### Opción 3: Instalación Manual

```bash
# Clonar el repo
git clone https://github.com/Baker-Agency/paid-ads-skills-spain.git

# Copiar la skill que quieras
cp -r paid-ads-skills-spain/skills/google-ads-spain .agents/skills/

# Crear symlink para Claude Code
ln -sf ../../.agents/skills/google-ads-spain .claude/skills/google-ads-spain
```

## Qué incluye `google-ads-spain`

La skill cubre el **ciclo de vida completo** de gestión de Google Ads para España:

| Fase | Qué cubre |
|------|-----------|
| **Fase 0** | Viabilidad — Rule of Two (EUR), framework CAC, "Winnable Fight" |
| **Fase 1** | Setup — Arquitectura de cuenta, settings España, negativas en español |
| **Fase 2** | Pujas — Progresión Max Clicks → Max Conversions → tCPA → tROAS |
| **Fase 3** | Copy — Framework RSA, guía tú vs usted, PAS en español |
| **Fase 4** | Optimización — Cadencia diaria/semanal/mensual/trimestral |
| **Fase 5** | Escalado — Vertical/horizontal, triggers de impression share |
| **Fase 6** | Campañas avanzadas — PMax, Demand Gen, B2B, 7 estrategias Search |
| **Fase 7** | Tracking — Tiers, GDPR/LOPD, consent mode, OCI |
| **Fase 8** | Auditoría — Framework completo para cuentas españolas |

### Contenido Específico España

- **IVA 21%** — impacto en unit economics y márgenes
- **LOPD/GDPR** — compliance para tracking (alta tasa rechazo cookies en España)
- **Calendario estacional** — festivos nacionales + festivos por Comunidades Autónomas
- **Comportamiento consumidor** — preferencia WhatsApp, Bizum, financiación, horario partido
- **Targeting regional** — 17 CC.AA., diferencias vocabulario, CPC por región
- **Patrones nómina** — 3ª semana débil, fin de mes + domingo = mejor día para push
- **Benchmarks** — CPL/CPC por vertical en España (clínicas, legal, dental, SaaS, etc.)
- **Expertos españoles** — Enrique del Valle, Rafa Madorran, Miriam Navas, y más

### Archivos de Referencia (14)

| Archivo | Contenido |
|---------|-----------|
| `unit-economics-spain.md` | Rule of Two EUR, CAC, IVA 21% |
| `campaign-setup-checklist.md` | Setup paso a paso para España |
| `negative-keywords-spanish.md` | Listas de negativas pre-hechas en español |
| `bidding-progression.md` | Progresión completa de estrategia de pujas |
| `spanish-ad-copy.md` | Copy en español, tú vs usted, PAS |
| `optimization-cadence.md` | Optimización diaria/semanal/mensual |
| `scaling-framework.md` | Escalado vertical/horizontal |
| `campaign-types.md` | Search, PMax, Demand Gen, B2B, AI Max, YouTube |
| `tracking-spain.md` | Tiers de tracking, GDPR/LOPD, OCI |
| `audit-checklist.md` | Auditoría completa para cuentas españolas |
| `automation-scripts.md` | Ninja Scripts, 8020 Agent, agentes IA |
| `spain-market-guide.md` | Festivos, CC.AA., comportamiento consumidor |
| `quality-score.md` | Quality Score en profundidad |
| `diagnostics.md` | Guía de troubleshooting |

### Casos de Éxito (4)

| Ejemplo | Resultados |
|---------|------------|
| `clinica-estetica-madrid.md` | €15K+/mes revenue extra, CPL €2-4 |
| `clinica-huelva-8.5x-roas.md` | €2.105 gasto → €17K revenue (8.5x ROAS) |
| `b2b-saas-search-framework.md` | Framework 4 capas de priorización |
| `servicio-local-spain.md` | De 0 a 30 conversiones/mes |

## Contribuir

¿Quieres mejorar una skill o añadir una nueva? [Abre un PR](https://github.com/Baker-Agency/paid-ads-skills-spain/pulls). Consulta [CONTRIBUTING.md](CONTRIBUTING.md) para las guías.

¿Tienes un problema o una pregunta? [Abre un issue](https://github.com/Baker-Agency/paid-ads-skills-spain/issues).

## Licencia

MIT — ver [LICENSE](LICENSE).
