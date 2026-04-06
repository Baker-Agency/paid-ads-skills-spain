# Paid Ads Skills for AI Agents — Spanish Market

A collection of AI agent skills for managing paid advertising campaigns in the Spanish market (Spain). Built for agencies, freelancers, and in-house marketers managing PPC for lead gen, SaaS, and services businesses.

Works with Claude Code, OpenAI Codex, Cursor, Windsurf, and any agent that supports the [Agent Skills spec](https://agentskills.io).

Built by [Baker Agency](https://github.com/Baker-Agency).

## What are Skills?

Skills are markdown files that give AI agents specialized knowledge and workflows for specific tasks. When you add these to your project, your agent can recognize when you're working on a paid ads task and apply the right frameworks, benchmarks, and best practices — specifically adapted for the Spanish market.

## Available Skills

| Skill | Description |
|-------|-------------|
| [google-ads-spain](skills/google-ads-spain/) | Complete Google Ads management for Spain. Setup, optimize, scale, and audit campaigns for lead gen, SaaS, and services. Includes bidding progression, Quality Score optimization, Spanish ad copy, GDPR/LOPD tracking, seasonality calendar, and CC.AA. targeting. |

### Coming Soon

- `meta-ads-spain` — Meta Ads (Facebook/Instagram) for the Spanish market
- `linkedin-ads-spain` — LinkedIn Ads for B2B in Spain
- `tiktok-ads-spain` — TikTok Ads for the Spanish market

## Installation

### Option 1: CLI Install (Recommended)

Use [npx skills](https://github.com/vercel-labs/skills) to install skills directly:

```bash
# Install all skills
npx skills add Baker-Agency/paid-ads-skills-spain

# Install specific skills
npx skills add Baker-Agency/paid-ads-skills-spain --skill google-ads-spain

# List available skills
npx skills add Baker-Agency/paid-ads-skills-spain --list
```

This automatically installs to your `.agents/skills/` directory (and symlinks into `.claude/skills/` for Claude Code compatibility).

### Option 2: Claude Code Plugin

Install via Claude Code's built-in plugin system:

```bash
# Add the marketplace
/plugin marketplace add Baker-Agency/paid-ads-skills-spain

# Install all skills
/plugin install paid-ads-skills-spain
```

### Option 3: Manual Install

```bash
# Clone the repo
git clone https://github.com/Baker-Agency/paid-ads-skills-spain.git

# Copy the skill you want
cp -r paid-ads-skills-spain/skills/google-ads-spain .agents/skills/

# Create symlink for Claude Code
ln -sf ../../.agents/skills/google-ads-spain .claude/skills/google-ads-spain
```

## What's Inside `google-ads-spain`

The skill covers the **complete lifecycle** of Google Ads management for Spain:

| Phase | What it covers |
|-------|---------------|
| **Fase 0** | Viabilidad — Rule of Two (EUR), CAC framework, "Winnable Fight" |
| **Fase 1** | Setup — Account architecture, Spain settings, negative keywords (Spanish) |
| **Fase 2** | Pujas — Max Clicks → Max Conversions → tCPA → tROAS progression |
| **Fase 3** | Copy — RSA framework, tú vs usted guide, PAS in Spanish |
| **Fase 4** | Optimización — Daily/weekly/monthly/quarterly cadence |
| **Fase 5** | Escalado — Vertical/horizontal scaling, impression share triggers |
| **Fase 6** | Campañas avanzadas — PMax, Demand Gen, B2B, 7 Search strategies |
| **Fase 7** | Tracking — Tiers, GDPR/LOPD, consent mode, OCI |
| **Fase 8** | Auditoría — Complete audit framework for Spanish accounts |

### Spain-Specific Content

- **IVA 21%** impact on unit economics and margins
- **LOPD/GDPR** compliance for tracking (high cookie rejection rates in Spain)
- **Seasonality calendar** — national holidays + Comunidades Autónomas holidays
- **Consumer behavior** — WhatsApp preference, Bizum, financing, horario partido
- **Regional targeting** — 17 CC.AA., vocabulary differences, CPC by region
- **Payroll patterns** — 3rd week weak, end-of-month + Sunday = best push day
- **Benchmarks** — CPL/CPC by vertical in Spain (clinics, legal, dental, SaaS, etc.)
- **Spanish experts** — Enrique del Valle, Rafa Madorran, Miriam Navas, and more

### Reference Files (14)

| File | Content |
|------|---------|
| `unit-economics-spain.md` | Rule of Two EUR, CAC, IVA 21% |
| `campaign-setup-checklist.md` | Step-by-step setup for Spain |
| `negative-keywords-spanish.md` | Pre-built negative keyword lists in Spanish |
| `bidding-progression.md` | Complete bidding strategy progression |
| `spanish-ad-copy.md` | Spanish ad copy, tú vs usted, PAS |
| `optimization-cadence.md` | Daily/weekly/monthly optimization |
| `scaling-framework.md` | Vertical/horizontal scaling |
| `campaign-types.md` | Search, PMax, Demand Gen, B2B, AI Max, YouTube |
| `tracking-spain.md` | Tracking tiers, GDPR/LOPD, OCI |
| `audit-checklist.md` | Complete audit for Spanish accounts |
| `automation-scripts.md` | Ninja Scripts, 8020 Agent, AI agents |
| `spain-market-guide.md` | Holidays, CC.AA., consumer behavior |
| `quality-score.md` | Quality Score deep dive |
| `diagnostics.md` | Troubleshooting guide |

### Case Studies (4)

| Example | Results |
|---------|---------|
| `clinica-estetica-madrid.md` | €15K+/month extra revenue, CPL €2-4 |
| `clinica-huelva-8.5x-roas.md` | €2,105 spend → €17K revenue (8.5x ROAS) |
| `b2b-saas-search-framework.md` | 4-layer prioritization framework |
| `servicio-local-spain.md` | 0 to 30 conversions/month playbook |

## Contributing

Found a way to improve a skill or have a new one to add? [Open a PR](https://github.com/Baker-Agency/paid-ads-skills-spain/pulls). See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Run into a problem or have a question? [Open an issue](https://github.com/Baker-Agency/paid-ads-skills-spain/issues).

## License

MIT — see [LICENSE](LICENSE).
