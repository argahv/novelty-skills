# PRISM — Merged Cognition Engine

11 thinking patterns + the PRISM architecture that fuses them into one adversarial reasoning system. Works with any agent that reads SKILL.md.

## Quick Install

```bash
npx skills add argahv/novelty-skills
```

## Structure

```
skills/
├── contrarian/            # Invert any well-established claim
├── cross-pollinator/      # Import solutions from distant fields
├── assumption-excavator/  # Find unstated assumptions
├── paradox-sifter/        # Cross-reference limitations across papers
├── heretic/               # Generate 50 wild hypotheses
├── counterfactual/        # Rewrite a field's history
├── theorist/              # Reviewer: formal rigor
├── empiricist/            # Reviewer: experimental design
├── skeptic/               # Reviewer: maximum doubt
├── pragmatist/            # Reviewer: practical applicability
└── dreamer/               # Reviewer: push further
```

## PRISM — Merged Execution

For complete cognition, run all 11 as parallel subagents:

```
Pass 1: All patterns fire on the same input (DIVERGE)
Pass 2: Each pattern sees all other patterns' outputs (EMERGE)
Pass 3: All 5 reviewers stress-test all outputs (CONVERGE)
Final: Paradox-Sifter cross-references → Synthesis (SYNTHESIZE)
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
