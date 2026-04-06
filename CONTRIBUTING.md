# Contributing

Thanks for your interest in contributing to Paid Ads Skills Spain!

## Adding a New Skill

### 1. Create the skill directory

```bash
mkdir -p skills/your-skill-name
```

### 2. Create the SKILL.md file

Every skill needs a `SKILL.md` file with YAML frontmatter:

```yaml
---
name: your-skill-name
description: When to use this skill. Include trigger phrases and keywords.
---

# Your Skill Name

Instructions for the agent go here...
```

### 3. Follow the naming conventions

- **Directory name**: lowercase, hyphens only (e.g., `meta-ads-spain`)
- **Name field**: must match directory name exactly
- **Description**: 1-1024 characters, include trigger phrases
- **Language**: content in Spanish/English mix (headers Spanish, technical terms English)

### 4. Structure your skill

```
skills/your-skill-name/
├── SKILL.md          # Required — main skill file
├── references/       # Optional — detailed reference docs
│   └── *.md
└── examples/         # Optional — case studies and examples
    └── *.md
```

### 5. Update marketplace.json

Add your skill path to `.claude-plugin/marketplace.json` in the `skills` array.

### 6. Update VERSIONS.md

Add your skill to the versions table.

### 7. Submit a PR

Open a pull request with your changes.

## Skill Guidelines

- **Focus**: paid ads for lead gen, SaaS, and services in the Spanish market (NOT e-commerce)
- **Style**: extreme brevity — bullets, tables, numbered steps. No paragraphs, no filler
- **Attribution**: cite sources when including benchmarks or specific tactics
- **Self-contained**: each skill must work independently with all references included
