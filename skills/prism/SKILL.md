---
name: prism
description: "Orchestrate all 11 thinking patterns into a single adversarial reasoning pipeline. Runs DIVERGE → EMERGE → CONVERGE → SYNTHESIS on any problem."
tags: [prism, orchestration, synthesis, meta]
difficulty: advanced
argument-hint: "Any problem, decision, claim, plan, or design to analyze"
---

# PRISM — The Full Pipeline

You are the PRISM orchestrator. Your job is not to analyze the problem directly — it is to **run all 11 patterns as a pipeline** and synthesize their outputs into a structured possibility space.

When invoked, you will:

1. Decompose the input for each pattern
2. Execute all 6 generators in parallel (DIVERGE)
3. Cross-reference all outputs (EMERGE)
4. Stress-test everything with all 5 reviewers (CONVERGE)
5. Synthesize a 7-part structured answer (SYNTHESIS)

---

## Execution Protocol

### Phase 1 — DIVERGE: Run all 6 generators in parallel

Invoke every generator on the same input. Each must produce **structured findings** — not free-form prose.

For each finding, enforce this output structure:

```yaml
pattern: <generator-name>
input: <original problem>
findings:
  - claim: "<the specific finding>"
    type: <see below>
    confidence: <HIGH | MEDIUM | LOW | EXPLORATION>
    supports_patterns: []
    contradicts_patterns: []
```

**Finding types by generator:**

| Generator | Produces | Finding type |
|-----------|----------|--------------|
| **contrarian** | 10 counter-hypotheses from 6 inversion axes | `inversion` |
| **assumption-excavator** | 3-5 critical assumptions with falsification tests | `assumption` |
| **cross-pollinator** | 3+ imported mechanisms from distant fields | `mechanism` |
| **heretic** | 50 hypotheses, scored, haunting idea identified | `hypothesis` |
| **counterfactual** | 1 suppressed alternative with ripple effects | `alternative` |
| **dreamer** | 3 10× pushes with first experiment | `push` |

**Confidence calibration:**

| Label | When to use |
|-------|-------------|
| `HIGH` | Supported by evidence outside the current frame. Multiple sources agree. |
| `MEDIUM` | Plausible, coherent, but not independently verified. |
| `LOW` | Interesting speculation. No evidence either way. |
| `EXPLORATION` | Wild but high-impact if true. Heretic #30+ territory. |

---

### Phase 2 — EMERGE: Cross-reference all findings

Feed **all** structured findings from Phase 1 into **paradox-sifter**. Its job is no longer to analyze paper limitations — it must cross-reference the generators' findings.

Paradox-sifter looks for:

1. **Convergences** — 3+ generators made the same finding independently
   → Promote confidence by one level. Mark as `consensus_view`.

2. **Contradictions** — Two generators produced incompatible findings
   → Surface both. Note the tension. This is a research opportunity.

3. **Creative tensions** — Dreamer says "10× on dimension D" but Pragmatist says "cost prohibitive"
   → This is the feasibility frontier. Document both.

4. **Suppressed alternatives resurrected** — Counterfactual's alternative matches Heretic's wild hypothesis
   → High signal. Promote to `consensus_view` for the "road not taken."

5. **Assumption cascades** — Assumption-Excavator's critical assumption is exactly what Contrarian inverted
   → If the assumption is false, the Contrarian's inversion is likely partially true.

**Output from this phase:**

A cross-reference matrix:

```yaml
cross_references:
  convergences:
    - claim: "..."
      sources: [pattern_a, pattern_b, pattern_c]
      confidence: HIGH
  contradictions:
    - claim_a: "..."
      claim_b: "..."
      source_a: pattern_x
      source_b: pattern_y
      potential_resolution: "..."
  creative_tensions:
    - dimension: "..."
      dreamer_claim: "..."
      pragmatist_assessment: "..."
      frontier: "..."
```

---

### Phase 3 — CONVERGE: Stress-test with all 5 reviewers

Feed **all** findings from Phase 1 + the cross-reference matrix from Phase 2 to every reviewer.

Each reviewer must produce structured output:

| Reviewer | Produces | Finding type |
|----------|----------|--------------|
| **theorist** | Formal gaps in any claimed guarantees | `formal_gap` |
| **empiricist** | Experiment designs for top claims | `empirical_gap` |
| **skeptic** | Evidence grades for every claim | `evidence_grade` |
| **pragmatist** | Cost assessment + "so what?" verdict | `cost` |
| **dreamer** | Next-step pushes on survivors | `push` |

Each reviewer must cite exactly which findings from Phase 1-2 they are responding to, using the `supports_patterns` / `contradicts_patterns` fields.

---

### Phase 4 — SYNTHESIS: Produce the 7-part possibility space

Combine all outputs from all 3 previous phases into this structure:

```yaml
synthesis:
  problem: "<the original input>"
  timestamp: "<current time>"

  consensus_view:
    claim: "<what survived all 5 reviewers and was found by 3+ generators>"
    confidence: HIGH
    source_patterns: [<generators that found this>]
    verified_by: [<reviewers that confirmed this>]

  contrarian_view:
    claim: "<what Contrarian found that everyone ignores>"
    confidence: <MEDIUM | LOW>
    impact_if_true: "<what changes>"
    cheapest_test: "<minimum experiment to determine truth>"

  suppressed_alternative:
    claim: "<what Counterfactual found — the road not taken>"
    abandoned_because: "<why the canonical won instead>"
    trigger_conditions: "<when this becomes the right choice>"

  haunting_idea:
    claim: "<Heretic's highest novelty × evidence gap finding>"
    novelty_x_evidence_gap: <score>
    minimum_experiment: "<how to test it>"

  crazy_next_step:
    claim: "<Dreamer's most impactful 10× push that survived Pragmatist>"
    first_move: "<the first experiment toward it>"
    feasibility: "<what would need to be true for this to work>"

  critical_assumptions:
    - assumption: "<Assumption-Excavator finding>"
      catastrophic_if_false: <true | false>
      cheapest_test: "<how to falsify>"

  dangerous_paradox:
    description: "<the contradiction across multiple findings>"
    ignored_for: "<how long / context>"
    resolution_experiment: "<how to resolve it>"

  recommendation:
    action: "<what to do>"
    confidence: <HIGH | MEDIUM | LOW>
    if_wrong: "<what to do if this turns out to be wrong>"
```

**Confidence composition rules:**

| Condition | Final confidence |
|-----------|-----------------|
| Survived all 5 reviewers + found by 3+ generators | HIGH |
| Survived 3+ reviewers + found by 2 generators | MEDIUM |
| Found by 1 generator, not contradicted | LOW |
| Found by 1 generator, contradicted by another | EXPLORATION |
| Dreamer/Pragmatist frontier | REPORTED (not scored) |

---

## Example

**Input:** "Should we adopt microservices for our 5-person startup?"

**Output (abbreviated):**

```yaml
synthesis:
  problem: "Should we adopt microservices for our 5-person startup?"
  timestamp: "2026-06-03"

  consensus_view:
    claim: "Not yet. The operational complexity of microservices exceeds the needs of a 5-person team. Start monolithic with well-defined modules."
    confidence: HIGH
    source_patterns: [contrarian, pragmatist, assumption-excavator]
    verified_by: [theorist, skeptic, empiricist]

  contrarian_view:
    claim: "Microservices could improve velocity even for 5 people by enforcing strict API contracts that force clean separation from day one."
    confidence: MEDIUM
    impact_if_true: "The team grows into the architecture instead of migrating to it."
    cheapest_test: "Define API contracts first. If the team can ship features using only the contracts (no internal knowledge of other modules), the modular approach works regardless of deployment topology."

  suppressed_alternative:
    claim: "Without the microservices hype cycle, you'd use a modular monolith with process boundaries — Domain-Driven Design bounded contexts deployed as separate processes but sharing a database."
    abandoned_because: "Microservices were marketed as the only path to scalability. Modular monoliths were positioned as 'legacy' even for greenfield projects."
    trigger_conditions: "If team exceeds 15 people OR two services need independent deploy schedules OR a single feature requires 3+ teams to coordinate."

  haunting_idea:
    claim: "The real question isn't monolith vs microservices — it's whether you've designed bounded contexts at all. Without that, microservices are just a distributed monolith."
    novelty_x_evidence_gap: 81
    minimum_experiment: "Ask the team to define the bounded contexts without mentioning deployment topology. If they can't, microservices will fail regardless of choice."

  crazy_next_step:
    claim: "Don't choose. Run BOTH. Keep the monolith in production. Build one critical feature as a microservice alongside it. Learn from the real operational cost before committing."
    first_move: "Identify one feature that has different scaling or deploy requirements. Extract it as a separate service. Measure: deploy time, error rate, developer overhead."
    feasibility: "Requires CI/CD maturity and containerization. Feasible for most startups with basic DevOps."

  critical_assumptions:
    - assumption: "5-person team can manage N+1 services."
      catastrophic_if_false: true
      cheapest_test: "Run one service for 2 weeks. Measure: how much of the team's time went to ops vs feature work."
    - assumption: "Microservices improve developer velocity."
      catastrophic_if_false: true
      cheapest_test: "Benchmark: build a feature in the monolith, then build the same feature in a microservice. Compare total time from idea to production."

  dangerous_paradox:
    description: "Conventional wisdom says microservices improve velocity. The empiricist finds that most studies compare well-run microservices to poorly-maintained monoliths. The contrarian finds the real variable is team size, not architecture."
    ignored_for: "15+ years of industry debate without controlling for team size × architecture interaction."
    resolution_experiment: "A controlled study: 10 teams of 5, randomly assigned to monolith vs microservices. Measure velocity, quality, and developer satisfaction over 6 months."

  recommendation:
    action: "Start monolithic with strict bounded contexts. Migrate to services when any single context requires 3+ developers."
    confidence: HIGH
    if_wrong: "If the team struggles with modular discipline in a monolith, microservices won't help — the discipline issue will compound."
```

---

## Required Setup

Before running PRISM for the first time:

1. All 11 skills must be installed (`npx skills add argahv/novelty-skills -g -y -s '*'`)
2. Each skill must have its `## PRISM Integration` section populated
3. The executor (AI or human) must be capable of parallel subagent invocation

---

## Anti-Patterns

| Mistake | Why it fails | Fix |
|---------|-------------|-----|
| Running patterns sequentially, not in parallel | Phase 1 requires genuine simultaneity — each pattern must NOT see other outputs until Phase 2 | Enforce parallelism in DIVERGE. Cross-feeding only starts in EMERGE. |
| Letting any pattern produce free-form prose | Without structured findings, Paradox-Sifter can't cross-reference and Synthesis can't compose | Enforce the YAML finding format. Reject free-text outputs. |
| Skipping a pattern because "it doesn't apply" | Each pattern sees a different angle. Skipping one creates a blind spot. | Run all 11 every time. A pattern that "doesn't apply" is itself a finding. |
| Using default confidence = HIGH | Everything starts at EXPLORATION. Confidence must be EARNED through convergence. | Default every finding to LOW or EXPLORATION. Promote only when cross-referencing confirms. |
| Synthesis without recommendations | A possibility space without an action is just intellectual exercise | Always end with a `recommendation` block with `if_wrong` fallback. |

## Trigger Conditions

Use this skill when:
- The user asks for "the full PRISM treatment"
- The problem is high-stakes and needs maximum scrutiny
- A decision involves multiple competing factors
- You need the structured 7-part possibility space
- Before committing to a significant architecture, strategy, or product decision
