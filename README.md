<div align="center">

# Novelty Skills — Thinking Tools for AI Agents

**6 thinking patterns your agent is missing. Generate ideas no engineer would think of.**

[![CI](https://github.com/argahv/novelty-skills/actions/workflows/ci.yml/badge.svg)](https://github.com/argahv/novelty-skills/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Install via npx](https://img.shields.io/badge/install-npx_skills_add-blue)](https://github.com/argahv/novelty-skills)

</div>

Your agent can write code, debug, and deploy. But can it **invent**? These are the cognitive patterns that separate breakthrough ideas from incremental improvements — packaged as agent skills.

Works with Claude Code, Codex, Cursor, Gemini CLI, and any agent that reads SKILL.md.

---

## Install

```bash
# Install all skills — browse and select interactively
npx skills add argahv/novelty-skills

# Install a specific skill
npx skills add argahv/novelty-skills --skill contrarian

# Install globally (available across all projects)
npx skills add argahv/novelty-skills -g -y -s '*'
```

Or clone manually:

```bash
git clone https://github.com/argahv/novelty-skills ~/.claude/skills/novelty-skills
```

---

## The Skills

| Skill | What it does | Use when |
|-------|-------------|----------|
| **contrarian** | Inverts every well-established claim in a field. Generates 10 counter-hypotheses. | "Everyone knows X is true." What if it isn't? |
| **cross-pollinator** | Imports solutions from 15 distant fields (astrodynamics → biology, monetary policy → ML). | You're stuck in domain-specific thinking. |
| **assumption-excavator** | Finds unstated assumptions and tests what breaks if they're false. | "We assume X." Did you check? |
| **paradox-sifter** | Cross-references every "Limitations" section to find ignored contradictions. | Multiple papers say different things. Who's right? |
| **heretic** | Generates 50 wild hypotheses from title+abstract alone. Scores each against reality. | You need a breakthrough, not an improvement. |
| **counterfactual** | Rewrites a field's history without the most-cited papers. | You need to find the road not taken. |

---

## Bonus: Reviewer Personas

5 adversarial reviewer personas in `skills/theorist/`, `skills/empiricist/`, `skills/skeptic/`, `skills/pragmatist/`, `skills/dreamer/` — critique any plan or design from different angles.

---

## Example

```
/contrarian "The claim: 'Microservices improve engineering velocity'"
```

Agent output:
```
1. INVERT: Microservices reduce engineering velocity
   Evidence: Conway's Law, network overhead, cognitive load
2. INVERT: Monoliths improve engineering velocity
   Evidence: Amazon's monolith-to-microservices journey cost 2 years
3. INVERT: Engineering velocity is the wrong metric
```

---

## Why These Exist

Most agent skills teach *process* — how to deploy, how to test, how to review. These teach *thinking* — how to generate ideas that no amount of process optimization will produce.

Part of the [Sisyphus Academica](https://github.com/argahv/sisyphus-academica) research pipeline project.

---

## License

MIT
