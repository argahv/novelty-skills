# Novelty Skills — Agent Onboarding

11 thinking skills for AI agents. Works with any agent that reads SKILL.md.

## Quick Install

```bash
npx skills add argahv/novelty-skills
```

## Structure

```
skills/
├── contrarian/            # Invert any well-established claim
│   └── SKILL.md
├── cross-pollinator/      # Import solutions from distant fields
│   └── SKILL.md
├── assumption-excavator/  # Find unstated assumptions
│   └── SKILL.md
├── paradox-sifter/        # Cross-reference limitations across papers
│   └── SKILL.md
├── heretic/               # Generate 50 wild hypotheses
│   └── SKILL.md
├── counterfactual/        # Rewrite a field's history
│   └── SKILL.md
├── theorist/              # Reviewer: formal rigor
│   └── SKILL.md
├── empiricist/            # Reviewer: experimental design
│   └── SKILL.md
├── skeptic/               # Reviewer: maximum doubt
│   └── SKILL.md
├── pragmatist/            # Reviewer: practical applicability
│   └── SKILL.md
└── dreamer/               # Reviewer: push further
    └── SKILL.md
```

## Skill Format

Each skill is a markdown file with YAML frontmatter:

```yaml
---
name: <skill-name>
description: "<one-line description>"
tags: [thinking, category]
difficulty: beginner | intermediate | advanced
---
```

## Conventions

- Skills are pure markdown — no code, no dependencies
- Each skill must have a Protocol, Example Output, and Anti-Patterns section
- Reviewer personas follow the same format but frame their critique in-character
