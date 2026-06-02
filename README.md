<div align="center">

# AGORA — The Merged Cognition Engine

**11 thinking patterns + the architecture that fuses them into one unstoppable reasoning system**

[![CI](https://github.com/argahv/novelty-skills/actions/workflows/ci.yml/badge.svg)](https://github.com/argahv/novelty-skills/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Install via npx](https://img.shields.io/badge/install-npx_skills_add-blue)](https://github.com/argahv/novelty-skills)

</div>

Your agent can write code, debug, and deploy. But can it **invent**? Can it see what everyone else missed? Can it stress-test its own best ideas to destruction before they reach production?

These 11 cognitive patterns are the difference between incremental improvements and breakthroughs. Used individually, each pattern generates ideas no engineer would think of. Used together in the **AGORA architecture** — where every output is fed into every other pattern and stress-tested from 11 orthogonal angles simultaneously — they form a reasoning system with no single point of failure and no cognitive blind spot.

Works with Claude Code, Codex, Cursor, Gemini CLI, and any agent that reads SKILL.md.

---

## Quick Install

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

## The AGORA Architecture

A single cognitive pattern is a lens — powerful, but with a blind spot. AGORA fuses all 11 patterns into **one synthetic reasoning engine** where no output is accepted until it has survived adversarial scrutiny from every angle.

```
                     ┌─────────────────────────────┐
                     │      INPUT (any problem)     │
                     └─────────────┬───────────────┘
                                   │
              ┌────────────────────┼────────────────────┐
              │                    │                    │
              ▼                    ▼                    ▼
     ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐
     │   DIVERGE        │  │   EMERGE        │  │   CONVERGE      │
     │ (max surface)   │─▶│ (find patterns) │─▶│ (stress-test)   │
     └─────────────────┘  └─────────────────┘  └─────────────────┘
              │                    │                    │
              └────────────────────┼────────────────────┘
                                   ▼
                     ┌─────────────────────────────┐
                     │   SYNTHESIS (possibility     │
                     │   space with verdict)        │
                     └─────────────────────────────┘
```

### Phase 1: DIVERGE — Maximize Surface Area

All 6 novelty engines fire **in parallel** on the same input. Each sees something the others miss:

| Pattern | Extracts | Unique Signal |
|---------|----------|---------------|
| **Assumption-Excavator** | Hidden premises (resource, behavioral, causal, temporal) | What everyone assumed but nobody stated |
| **Contrarian** | Inverted claims across 6 axes (polarity, direction, scope, relevance, existence, priority) | What's true if the consensus is wrong |
| **Heretic** | 50 hypotheses from 5 categories (extensions → substitutions → inversions → hidden variables → paradigm shifts) | What lives at hypotheses #30-50 where breakthroughs hide |
| **Cross-Pollinator** | Mechanisms from 15 distant fields (astrodynamics, immunology, jurisprudence, music theory, military strategy...) | What the problem looks like to an immune system / astronomer / jurist |
| **Counterfactual** | Suppressed alternatives (approaches abandoned because attention flowed to the canonical solution) | What we'd be doing if the famous paper never existed |
| **Dreamer** | 10× pushes on every dimension (data, scale, scope, constraints, metrics, generalization) | Where we'd be if we hadn't stopped early |

**Key property:** Each output feeds the others. Heretic's wild ideas become Contrarian inversion targets. Cross-Pollinator's imported mechanisms become Dreamer's 10× dimensions. Counterfactual's suppressed alternatives become Assumption-Excavator's hidden premises.

### Phase 2: EMERGE — Find the Patterns No Single Lens Sees

Paradox-Sifter now cross-references **the outputs of Phase 1 itself**, finding:

| Pattern detected | What it means |
|-----------------|---------------|
| **Echo** | 3+ patterns independently converged on same idea → high-confidence signal |
| **Blind spot consensus** | All patterns agree on a gap → something fundamental is being missed |
| **Creative tension** | Dreamer says "10×" while Pragmatist says "so what?" → the exact frontier of feasible ambition |
| **Suppressed alternative resurrected** | Counterfactual's finding matches Heretic's wild hypothesis → might be the real breakthrough |
| **Assumption cascade** | Excavator's critical assumption is exactly what Contrarian inverts → killing one premise kills the whole argument |

### Phase 3: CONVERGE — Stress-Test Everything

All 5 reviewer personas fire on **every** Phase 1 output simultaneously:

```
            ┌─────────── Theorist ───────────┐
            │  "Formal soundness of each?"    │
            ├─────────── Empiricist ──────────┤
            │  "What experiment tests this?"  │
            ├─────────── Skeptic ─────────────┤  Phase 1 outputs
Input ──────┤  "What would prove this wrong?" │─────────────▶ Survivors
            ├─────────── Pragmatist ──────────┤
            │  "Does this matter in practice?"│
            ├─────────── Dreamer ─────────────┤
            │  "Where could this go further?" │
            └─────────────────────────────────┘
```

Each reviewer is made **smarter** by seeing the other reviewers' critiques. The Theorist's formal gap is immediately checked by the Empiricist: "does this gap matter empirically?" The Pragmatist's cost objection is checked by the Dreamer: "what if cost decreases 10×?"

### Phase 4: SYNTHESIZE — The Structured Possibility Space

The final output is not a single answer — it's a **structured topology of the problem** with calibrated confidence:

```
────────────────────────────────────────────────
TOPOLOGY OF THE PROBLEM
────────────────────────────────────────────────

◆ CONSENSUS VIEW (what's likely true)
  - Survived Theorist + Empiricist + Skeptic
  - Probability-weighted confidence: HIGH

◆ CONTRARIAN VIEW (what might be true but everyone ignores)  
  - Generated by Contrarian, survived Pragmatist
  - If true, impact: [assessed]
  - Confidence: MEDIUM

◆ SUPPRESSED ALTERNATIVE (what could have been)
  - Generated by Counterfactual
  - Abandoned not because wrong — because attention flowed elsewhere
  - Confidence: LOW (exploration signal)

◆ HAUNTING IDEA (what SHOULD be investigated)
  - Heretic's highest novelty × evidence gap score
  - "The paper is about X but should have been about Y"

◆ CRAZY NEXT STEP (10× ambition)
  - Dreamer's push after seeing all other outputs
  - First experiment: [minimum falsification test]

◆ CRITICAL ASSUMPTIONS (what everything rests on)
  - Assumption-Excavator's critical few
  - Cheapest test: [falsification experiment]

◆ DANGEROUS PARADOX (contradiction everyone ignored)
  - Paradox-Sifter's richest finding
  - Resolution experiment: [design]
```

---

## The 11 Skills

### Novelty Engines — Generate Ideas No One Has Had

| Skill | What it does | Use when |
|-------|-------------|----------|
| **contrarian** | Inverts every well-established claim along 6 axes (polarity, direction, scope, relevance, existence, priority). Generates 10 specific, falsifiable counter-hypotheses. | "Everyone knows X is true." What if it isn't? |
| **cross-pollinator** | Imports solutions from 15 distant fields — astrodynamics, immunology, monetary policy, military strategy, music theory, jurisprudence, and more. Extracts the mechanism, not the metaphor. | You're stuck in domain-specific thinking. |
| **assumption-excavator** | Surfaces ALL assumptions (resource, behavioral, environmental, temporal, causal, scalability, compositional). Flags the 1-3 critical ones that would kill the project if false. Designs the minimum falsification experiment. | "We assume X." Did you check? |
| **paradox-sifter** | Cross-references "Limitations" across papers on the same topic. Finds contradictions, mutual ignorance, hidden dependencies, and escalation dynamics that everyone missed. | Multiple papers say different things. Who's right? |
| **heretic** | Generates 50 wild hypotheses in 5 tiers (extensions → substitutions → goal inversions → hidden variables → paradigm shifts). Scores each by novelty × evidence gap. Finds the "haunting idea." | You need a breakthrough, not an improvement. |
| **counterfactual** | Removes the most-cited paper and rewrites the field's history. Finds the "suppressed alternative" — the approach abandoned because attention flowed to the canon, not because it was worse. | You need to find the road not taken. |

### Reviewer Personas — Stress-Test Any Idea

| Skill | What it does | Use when |
|-------|-------------|----------|
| **theorist** | Attacks formal proofs, mathematical rigor, theoretical foundations. Finds hidden constants, unrealizable conditions, circular reasoning, missing edge cases. Issues one of four verdicts: formally sound / minor gap / major gap / unsound. | Before submitting any paper or proposal with formal claims. |
| **empiricist** | Audits baselines (SOTA or straw-man?), metrics (variance? effect size? multiple comparisons?), and statistical methodology. Applies the replication test. | Before submitting any empirical results. |
| **skeptic** | Default: everything is wrong. Grades evidence from A (independently replicated, preregistered) to F (contradicts known results without extraordinary evidence). Specifies exactly what evidence would change the verdict. | You need the strongest possible challenge. |
| **pragmatist** | Calculates real cost (hardware, inference, engineering complexity, data requirements, failure modes). Applies the "So What?" test. Compares to the simplest baseline (10-line regex, do nothing). | Evaluating whether something works outside the lab. |
| **dreamer** | Identifies where the work stopped too early (dataset, scale, scope, constraints, metrics, generalization). Pushes each dimension to 10×. Identifies the one extension with disproportionate impact. Sketches the first experiment. | Finding the ambitious edge of any work. |

---

## Real-World Use Cases

### 1. Post-Mortem / Incident Analysis

**Today:** Engineers converge on "the DB connection pool ran out." Fix: increase pool size. Two weeks later, different outage, same pattern.

**With AGORA:** Assumption-Excavator reveals the pool limit was a symptom, not the cause. Cross-Pollinator imports epidemiology's contact tracing — connection spikes are disease outbreaks, you need retry governance, not bigger pools. Heretic generates "Hypothesis #31: the outage was a monitoring artifact." Counterfactual shows what architecture you'd have built without connection pooling (async queues). Pragmatist cost-checks each fix.

**Result:** Root cause found in minutes instead of hours. Fix is systemic (circuit breaker + exponential backoff), not symptomatic (increase pool size).

### 2. Architecture Decision Records (ADRs)

**Today:** "We chose Kafka because scalability." No conditions. No revisit threshold. Six months later, nobody knows why.

**With AGORA:** Contrarian inverts "Kafka is too complex for your 3-node cluster." Counterfactual removes Kafka's canonical papers — you'd use SQS + partitioning. Dreamer pushes to 10×: "what about 1000 nodes?" Pragmatist calculates ops cost. Paradox-Sifter cross-references your own past decisions.

**Result:** An ADR with explicit decision rules: "Kafka now, migrate to SQS if latency < 10ms matters. Revisit when team size exceeds 20." The road not taken is documented, with trigger conditions for when it becomes the right choice.

### 3. Startup / Product Strategy

**Today:** Founders build what they believe. Investors fund what they believe. Both are usually wrong (~90% fail).

**With AGORA:** Assumption-Excavator surfaces "you assume engineering teams can buy tools without security review" (they can't — 70% of enterprises require VP approval). Contrarian inverts "AI code review creates more work, not less." Cross-Pollinator imports predator-prey dynamics from marine biology. Heretic finds the pivot before you build: "sell to security teams, not engineering." Pragmatist prices it by fix count, not seat.

**Result:** Before writing a line of code, you've simulated the market, identified the real buyer, priced correctly, and found the cheapest test (3 LOIs from F500 security engineers in 2 weeks).

### 4. Technical Due Diligence (Acquisitions / Investments)

**Today:** "Codebase looks clean. Team seems solid." — said before every failed acquisition.

**With AGORA:** Paradox-Sifter cross-references the target's published claims against their own earlier papers — finds a contradiction (claimed CPU-only, earlier paper showed GPU clusters). Empiricist audits their benchmarks (synthetic data, not real distributions). Contrarian inverts "the real value isn't the model, it's the labeled dataset." Pragmatist calculates integration cost.

**Result:** 40% reduction in acquisition price justified by evidence. The model doesn't work at claimed latency — but the dataset is worth acquiring.

### 5. Security Vulnerability Discovery

**Today:** CVE scanners check known patterns. Novel vulns stay hidden until exploited.

**With AGORA:** Counterfactual removes JWT as the canonical auth solution — you'd use HTTP-only session cookies, which have a smaller attack surface. Heretic generates "Hypothesis #37: the JWT library accepts 'none' algorithm from a version mismatch" and "Hypothesis #42: SSRF via PDF generation endpoint reaches AWS metadata." Cross-Pollinator imports immunology's autoimmune concept — one service impersonating another via shared JWT trust.

**Result:** Zero-day discovered before any attacker. The vulnerabilities found by AGORA are invisible to standard scanners — they're not known CVEs, they're novel attack paths that no pattern-matching tool would find.

### 6. Research Paper / PhD Dissertation

**Today:** Read 50 papers → find a gap → write paper. Average output: incremental, predictably ignored.

**With AGORA:** Paradox-Sifter cross-references 15 papers on efficient attention — finds a 2-year-old unresolved contradiction (Paper A says linear attention works, Paper B says it loses long-range dependencies, neither cites the other). Heretic generates "your thesis shouldn't be about attention at all — it should be about evaluation methodology." Counterfactual removes the "Attention is All You Need" paper — State Space Models were the suppressed alternative.

**Result:** The student's proposal transforms from "one more attention variant" (2 citations) to "When Does Attention Matter? A Formal Characterization" (paradigm-defining contribution). Saved 2 years of incremental work.

### 7. Incident Command / Crisis Response

**Today:** "Is it the database?" → checks DB → "no" → "Is it the network?" → checks network → "no" — 45 minutes later someone checks DNS, which has been down for 45 minutes.

**With AGORA:** Assumption-Excavator fires in 30 seconds — "you checked DB/CPU/memory/network/DNS. You didn't check: certificate expiry, rate limiter state, feature flag state, third-party dependency health." Certificate expired 4 minutes ago. Cross-Pollinator imports immunology's anaphylaxis — the system overreacted to a localized trigger. Dreamer pushes to 10×: "this was ONE cert. You have 200. When do they expire?"

**Result:** 2-minute diagnosis vs 45-minute sequential debugging. Plus full prevention plan (monitor all 200 certs, isolate edge cert from application, add expiry to on-call runbook).

### 8. Personal / Career Decisions

**Today:** Pros/cons list → gut feeling → hope for the best.

**With AGORA:** Assumption-Excavator surfaces "you assume the equity will be worth something (90% of startups fail)." Contrarian inverts "staying at FAANG is riskier — your specialized skills become less valuable if things change." Cross-Pollinator imports crop rotation from agriculture (8 years in one field depletes it) and bet-hedging from evolutionary biology. Skeptic reframes: "would you do this if equity = $0?" Pragmatist calculates survival runway. Dreamer pushes: "not one startup — join, learn, then start your own."

**Result:** A decision framework, not a binary answer. "Go if: savings cover 2 years, equity = $0 still worth it, you have a 1-year cliff to return to FAANG." The framework is re-usable for every subsequent career decision.

---

## Agent Integration

### As Individual Skills

Each skill is a standalone SKILL.md. Load it when the situation matches its trigger conditions:

```
/contrarian "Claim: Microservices improve velocity"
/assumption-excavator "Plan: Launch in 6 weeks"
/cross-pollinator "Stuck: Need a creative approach to cache invalidation"
```

### As a Merged Agent (AGORA)

Spawn all 11 patterns as parallel subagents. Pass the same input to all. In pass 2, feed each pattern the outputs of all other patterns. Use Paradox-Sifter to cross-reference. Synthesize the structured possibility space.

```yaml
Execution loop:
  1. RECEIVE input
  2. FIRE all 11 patterns as parallel subagents
  3. COLLECT all outputs into shared context
  4. FIRE pass 2: each pattern sees original input + ALL other outputs
     Instruction: "Revise given what others found"
  5. PARADOX-SIFTER cross-references pass-2 outputs for:
     - Convergences (same finding from multiple patterns → high confidence)
     - Contradictions (patterns disagree → exploration needed)
     - Echoes (same idea in different language → surface as distinct)
  6. SYNTHESIZE into structured possibility space
  7. OUTPUT with calibrated confidence
```

### Pipeline Examples

```
🔬 Research: Librarian (gather) → Paradox-Sifter (contradictions) 
   → Heretic (hypotheses) → Empiricist (experiment design)

🏗️ Engineering: Assumption-Excavator (risks) → Contrarian (invert each) 
   → Cross-Pollinator (solutions) → Dreamer (10×) → Pragmatist (reality)

📝 Review: Theorist + Empiricist + Skeptic + Pragmatist + Dreamer 
   → synthesized review from 5 angles simultaneously
```

---

## Why This Exists

Most agent skills teach *process* — how to deploy, how to test, how to review. These teach *thinking* — how to generate ideas that no amount of process optimization will produce.

The AGORA architecture goes further: it fuses all 11 patterns into one adversarial reasoning system where:
- Every idea is seen from 11 orthogonal angles
- No claim is accepted until it survives 5 independent stress tests
- Every output has calibrated confidence, not false certainty
- The group's blind spot is caught by someone who sees differently

**11 patterns = 55 bidirectional cross-checks + 1 paradox matrix + 1 synthesis pass = a reasoning architecture with no single point of failure and no cognitive blind spot.**

Part of the [Sisyphus Academica](https://github.com/argahv/sisyphus-academica) research pipeline project.

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to add a new skill, report a bug, or suggest an improvement. New thinking patterns that survive the existing 11 are always welcome — that's how AGORA evolves.

---

## License

MIT — see [LICENSE](LICENSE).
