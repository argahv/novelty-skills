# PRISM — Execution Protocol

11 thinking patterns + the PRISM orchestrator that fuses them into one adversarial reasoning engine. Works with any agent that reads SKILL.md.

## Quick Install

```bash
npx skills add argahv/novelty-skills
```

## Structure

```
skills/
├── prism/                  # PRISM orchestrator (the merge pipeline)
├── contrarian/             # Invert any well-established claim
├── cross-pollinator/       # Import solutions from distant fields
├── assumption-excavator/   # Find unstated assumptions
├── paradox-sifter/         # Cross-reference findings from all patterns
├── heretic/                # Generate 50 wild hypotheses
├── counterfactual/         # Rewrite a field's history
├── theorist/               # Reviewer: formal rigor
├── empiricist/             # Reviewer: experimental design
├── skeptic/                # Reviewer: maximum doubt
├── pragmatist/             # Reviewer: practical applicability
└── dreamer/                # Reviewer: push further
```

## PRISM — Merged Execution

Run all 11 patterns as a 4-phase pipeline. Each phase feeds the next.

### Phase 1 — DIVERGE

Fire all 6 generators in parallel on the same input. Each produces structured YAML findings.

```
contrarian ──────────┐
assumption-excavator ─┤
cross-pollinator ─────┤  same input  ┌─────────────────┐
heretic ──────────────┤─────────────▶│ 6 sets of       │
counterfactual ───────┤              │ structured       │
dreamer ──────────────┘              │ findings (YAML)  │
                                     └─────────────────┘
```

**Constraints:**
- Each generator MUST use its PRISM Integration output format
- No generator sees another's output during this phase
- Default all confidence to LOW or EXPLORATION — it must be earned later

### Phase 2 — EMERGE

Feed all 6 structured finding sets into paradox-sifter. It cross-references for:

```
┌──────────────────┐    ┌──────────────────┐    ┌──────────────────────┐
│ 6 generator      │───▶│ paradox-sifter   │───▶│ cross-reference      │
│ finding sets     │    │ cross-references  │    │ matrix with          │
│                  │    │ all findings      │    │ convergences,        │
│                  │    │                   │    │ contradictions,      │
│                  │    │                   │    │ tensions, cascades   │
└──────────────────┘    └──────────────────┘    └──────────────────────┘
```

**Rules:**
- 3+ patterns converged → promote confidence to HIGH, mark as `consensus_view`
- Patterns contradict → surface both, note tension
- Dreamer vs Pragmatist tension → document the feasibility frontier
- Counterfactual + Heretic agree → promote to exploration signal

### Phase 3 — CONVERGE

Feed ALL findings (generator outputs + cross-reference matrix) to all 5 reviewers in parallel.

```
┌──────────────────┐    ┌──────────────┐
│ All findings     │───▶│ theorist     │── formal gaps
│ from phases      │    ├──────────────┤
│ 1-2              │    │ empiricist   │── experiment designs
│                  │    ├──────────────┤
│                  │    │ skeptic      │── evidence grades
│                  │    ├──────────────┤
│                  │    │ pragmatist   │── cost assessments
│                  │    ├──────────────┤
│                  │    │ dreamer (v2) │── 10× pushes on survivors
│                  │    └──────────────┘
└──────────────────┘
```

**Each reviewer must cite exactly which findings they're assessing** using `targets_finding` field.

### Phase 4 — SYNTHESIZE

Combine ALL structured outputs into the 7-part possibility space.

```yaml
synthesis:
  consensus_view:       # survived all 5 reviewers, found by 3+ generators
  contrarian_view:      # what everyone ignores, with cheapest test
  suppressed_alternative: # road not taken, with trigger conditions
  haunting_idea:        # heretic's highest novelty × evidence gap
  crazy_next_step:      # dreamer's most impactful 10× push
  critical_assumptions: # will kill you if false
  dangerous_paradox:    # contradiction everyone missed
  recommendation:       # what to do, with if_wrong fallback
```

**Confidence calibration:**

| Condition | Confidence |
|-----------|-----------|
| Survived all 5 reviewers + found by 3+ generators | HIGH |
| Survived 3+ reviewers + found by 2 generators | MEDIUM |
| Found by 1 generator, not contradicted | LOW |
| Found by 1 generator, contradicted by another | EXPLORATION |

## PRISM Orchestrator Skill

For detailed step-by-step instructions including example output, output format schemas, and anti-patterns for each phase, run the PRISM orchestrator skill:

```
/prism "Should we adopt microservices for 5-person startup?"
```

This loads `skills/prism/SKILL.md` which contains the full pipeline specification with structured output templates for every phase.

## Individual Pattern Use

Each pattern also works standalone via its trigger conditions:

```
/contrarian "Claim: Microservices improve velocity"
/assumption-excavator "Plan: Launch in 6 weeks"
/cross-pollinator "Stuck on cache invalidation"
/heretic "Paper: Attention is All You Need"
```

## Skill Format

Each skill is markdown with YAML frontmatter:

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
- Every skill must have a PRISM Integration section documenting its structured output format and cross-pattern dependencies
- The PRISM orchestrator skill (`skills/prism/SKILL.md`) is the canonical reference for the merged execution protocol
