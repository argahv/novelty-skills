# Novelty Skills — Thinking Tools for AI Agents

**6 thinking patterns your agent is missing. Generate ideas no engineer would think of.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Your agent can write code, debug, and deploy. But can it **invent**? These are the cognitive patterns that separate breakthrough ideas from incremental improvements — packaged as agent skills.

Works with Claude Code, Codex, Cursor, Gemini CLI, and any agent that reads SKILL.md.

---

## The Skills

| Skill | What it does | Use when |
|-------|-------------|----------|
| **contrarian** | Inverts every well-established claim in a field. Generates 10 counter-hypotheses. | "Everyone knows X is true." What if it isn't? |
| **cross-pollinator** | Imports solutions from 15 distant fields (astrodynamics → biology, monetary policy → ML). | You're stuck in domain-specific thinking. |
| **assumption-excavator** | Finds unstated assumptions and tests what breaks if they're false. | "We assume X." Did you check? |
| **paradox-sifter** | Cross-references every "Limitations" section to find ignored contradictions. | Multiple papers say different things. Who's right? |
| **heretic** | Generates 50 wild hypotheses from title+abstract alone. Scores each against reality. | You need a breakthrough, not an improvement. |
| **counterfactual** | Rewrites a field's history without the most-cited papers. What would have been invented? | You need to find the road not taken. |

---

## Quick Start

```bash
# Clone anywhere
git clone https://github.com/argahv/novelty-skills ~/.claude/skills/novelty-skills

# Or just pick one file:
cp contrarian.md ~/.claude/skills/contrarian.md
```

Then invoke in any agent:

```
/contrarian "The claim: 'Attention is all you need'"
/cross-pollinator "Problem: How to reduce LLM hallucination"
/heretic "Paper: 'Scaling Laws for Neural Language Models'"
```

---

## Why These Exist

Most agent skills teach *process* — how to deploy, how to test, how to review.

These teach *thinking* — how to generate ideas that no amount of process optimization will produce.

They're the cognitive equivalent of brute-force search: instead of converging on the obvious answer, they explore the space of **answers nobody has considered**.

---

## How They Work

Each skill is a single markdown file with:

1. **A structured thinking protocol** — step-by-step instructions the agent follows
2. **Example outputs** — what good looks like
3. **Anti-patterns** — common failures and how to avoid them
4. **Trigger conditions** — when to use this skill automatically

No code. No dependencies. No API keys. Pure thinking, encoded for agents.

---

## Bonus: Reviewer Personas

The `reviewers/` directory contains 5 adversarial reviewer personas that critique any plan, design, or paper from different angles:

- **theorist** — "Where's the formal proof?"
- **empiricist** — "Your baseline is wrong"
- **skeptic** — "Show me error bars"
- **pragmatist** — "Does this matter in practice?"
- **dreamer** — "You stopped too early"

Combine with any skill for built-in quality control.

---

## Example

```bash
/contrarian "The claim: 'Microservices improve engineering velocity'"
```

Agent output:
```
1. INVERT: Microservices reduce engineering velocity
   Evidence: Conway's Law, network overhead, cognitive load
2. INVERT: Monoliths improve engineering velocity
   Evidence: Amazon's monolith-to-microservices journey cost 2 years
3. INVERT: Engineering velocity is the wrong metric
   Evidence: Maybe we want correctness, not speed
...
```

---

## License

MIT
