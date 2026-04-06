# AGENTS.md

Guidelines for AI agents working in this repository.

## Repository Overview

This repository contains **Agent Skills** for AI agents following the [Agent Skills specification](https://agentskills.io/specification.md). Skills install to `.agents/skills/` (the cross-agent standard). This repo also serves as a **Claude Code plugin marketplace** via `.claude-plugin/marketplace.json`.

- **Name**: Paid Ads Skills Spain
- **GitHub**: [Baker-Agency/paid-ads-skills-spain](https://github.com/Baker-Agency/paid-ads-skills-spain)
- **Creator**: Baker Agency
- **License**: MIT

## Repository Structure

```
paid-ads-skills-spain/
├── .claude-plugin/
│   └── marketplace.json   # Claude Code plugin marketplace manifest
├── skills/                # Agent Skills
│   └── skill-name/
│       ├── SKILL.md       # Required skill file
│       ├── references/    # Detailed reference documentation
│       └── examples/      # Case studies and examples
├── CONTRIBUTING.md
├── LICENSE
├── VERSIONS.md
└── README.md
```

## Skill Focus

All skills in this repository are focused on **paid advertising for the Spanish market (Spain)**:

- Lead generation, SaaS, and services businesses (NOT e-commerce)
- Benchmarks in EUR, IVA 21%, LOPD/GDPR compliance
- Spanish language ad copy, consumer behavior, seasonality
- Regional targeting (Comunidades Autónomas)

## Writing Style

- Extreme brevity: bullets, tables, numbered steps
- No paragraphs, no filler, no intros
- Mix of Spanish headers and English technical terms
- Attribution for all benchmarks and specific tactics
- Self-contained: each skill includes all necessary references
