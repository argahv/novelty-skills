<div align="center">

```
╔══════════════════════════════════════════════════╗
║                                                  ║
║     One brain sees what it expects to see.       ║
║                                                  ║
║     AGORA gives you 11.                         ║
║     Each one catches what the others miss.       ║
║                                                  ║
╚══════════════════════════════════════════════════╝
```

**Thinking patterns that break consensus, find hidden assumptions, and stress-test your best ideas before they fail.**

[![CI](https://github.com/argahv/novelty-skills/actions/workflows/ci.yml/badge.svg)](https://github.com/argahv/novelty-skills/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Install via npx](https://img.shields.io/badge/install-npx_skills_add-blue)](https://github.com/argahv/novelty-skills)

</div>

```bash
npx skills add argahv/novelty-skills      # ← 5 seconds. Works with any AI.
```

<br>

```
┌─ Every team has blind spots ──────────────────────┐
│                                                    │
│  ✓ "We know this space"                            │
│  ✓ "Industry standard approach"                    │
│  ✓ "Everyone agrees"                               │
│                                                    │
│  ✗ That's where the failures live.                 │
│    The consensus is where the overlooked           │
│    assumption, the missing angle, the road         │
│    not taken — all hide in plain sight.            │
│                                                    │
└────────────────────────────────────────────────────┘

     ┌───────────────────────────────────────────┐
     │  AGORA doesn't replace your judgment.     │
     │  It arm-wrestles it from 11 angles until  │
     │  only the truth survives.                 │
     └───────────────────────────────────────────┘
```

---

## The 11 patterns

Each one is a distinct cognitive superpower. Use any one and you'll see things your peers miss. Use all 11 together and they cross-check each other into a reasoning system with no blind spot.

|  | Pattern | Strikes from | Use when |
|---|---------|-------------|----------|
| ⚡ | **contrarian** | The opposite direction | "Everyone knows X." What if that's wrong? |
| 🕳️ | **assumption-excavator** | What nobody said aloud | Before committing to any plan. |
| 🧬 | **cross-pollinator** | 15 distant fields | You're stuck and same-domain thinking isn't helping. |
| 🔥 | **heretic** | Hypothesis #30+ (the breakthrough zone) | You need a breakthrough, not an improvement. |
| ⏮️ | **counterfactual** | What if the canonical solution never existed? | "Why does everyone use X?" |
| 🔀 | **paradox-sifter** | Contradictions across sources | Different sources say different things. |
| 📐 | **theorist** | Formal proofs, hidden assumptions | Someone claims something is "provably true." |
| 📊 | **empiricist** | Baselines, error bars, methodology | Someone shows you impressive results. |
| ❓ | **skeptic** | Everything. Prove it. | You need the strongest possible challenge. |
| 💰 | **pragmatist** | Real-world cost, "so what?" | "SOTA" at what cost? Does it matter outside the lab? |
| 🚀 | **dreamer** | The 10× boundary | The team agreed on "good enough." |

---

## How they merge (the AGORA effect)

Use one pattern = you get one angle. Use all 11 = each output feeds every other, and nothing survives until it's been attacked from every side.

```
                    ┌─────────────────────┐
                    │    YOUR PROBLEM      │
                    └──────────┬──────────┘
                               │
           ┌───────────────────┼───────────────────┐
           │                   │                   │
           ▼                   ▼                   ▼
   ┌───────────────┐   ┌───────────────┐   ┌───────────────┐
   │   DIVERGE     │──▶│   EMERGE      │──▶│   CONVERGE    │
   │ 6 generators  │   │ paradox-sifter│   │ 5 reviewers   │
   │ (all angles)  │   │ (find patterns)│  │ (stress-test) │
   └───────────────┘   └───────────────┘   └───────────────┘
           │                   │                   │
           └───────────────────┼───────────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    SYNTHESIS        │
                    │ 7-part structured   │
                    │ possibility space   │
                    └─────────────────────┘
```

**Pass 1 — DIVERGE** All 6 generators fire in parallel. Assumption-Excavator finds what nobody stated. Contrarian inverts consensus. Heretic pushes to hypothesis #37 (where breakthroughs hide). Cross-Pollinator imports from immunology, strategy, music. Counterfactual finds the road not taken. Dreamer pushes every dimension to 10×.

**Each output feeds every other.** Heretic's wild idea becomes Contrarian's next inversion. Cross-Pollinator's mechanism becomes Dreamer's pushed dimension. Counterfactual's finding becomes Assumption-Excavator's new premise to check.

**Pass 2 — EMERGE** Paradox-Sifter cross-references all 6 outputs for convergences (3+ patterns agreed → high confidence), creative tensions (Dreamer says 10×, Pragmatist says "so what?" → the exact ambition frontier), and suppressed alternatives resurrected (Counterfactual + Heretic agree → likely breakthrough).

**Pass 3 — CONVERGE** All 5 reviewers fire on every survivor. Theorist checks formal soundness. Empiricist designs the experiment. Skeptic demands what would prove it wrong. Pragmatist calculates real cost. Dreamer asks what's next.

**Pass 4 — SYNTHESIS** Output: a 7-part possibility space, not a single guess. Consensus view. Contrarian view. Suppressed alternative. Haunting idea. Crazy next step. Critical assumptions. Dangerous paradox. Each with calibrated confidence.

```
11 patterns = 55 bidirectional cross-checks + 1 paradox matrix
          = a reasoning system with no single point of failure
```

---

## Where it hits

<br>

```
  Post-mortem                 ❌ "The DB pool ran out" → increase pool → repeat next month
                              ✅ assumption-excavator: pool limit was symptom, not cause
                                 cross-pollinator: retry storms = disease outbreaks
                                 → circuit breaker + exponential backoff
                                 → root cause found in minutes

  Architecture decision      ❌ "We chose Kafka for scalability" → nobody knows why
                              ✅ counterfactual: without Kafka, you'd use SQS + partitioning
                                 pragmatist: ops cost vs actual throughput
                                 → decision tree with explicit thresholds
                                 → the road not taken, with trigger conditions

  Startup strategy           ❌ Build what you believe → ~90% fail
                              ✅ assumption-excavator: "enterprises can't buy without VP approval"
                                 heretic: "sell to security teams, not engineering"
                                 pragmatist: price by fix count, not seat
                                 → real buyer identified before writing code

  Acquisition due diligence  ❌ "Code looks clean, team seems solid" → overpay
                              ✅ paradox-sifter: claimed CPU-only, earlier paper used GPU
                                 empiricist: benchmark data was synthetic
                                 → negotiate 40% off, acquire dataset (not model)

  Security audit             ❌ CVE scanner finds known patterns → novel vulns stay hidden
                              ✅ counterfactual: without JWT, you'd use session cookies
                                 heretic #37: "JWT library accepts 'none' algorithm"
                                 → zero-day found before any attacker
```

<br>

```
  ┌────────────────────────────────────────────────────────────┐
  │  The pattern: AGORA doesn't just answer your question.     │
  │  It shows you the question you SHOULD have asked.          │
  └────────────────────────────────────────────────────────────┘
```

---

## Install

```bash
# Everything — browse and select interactively
npx skills add argahv/novelty-skills

# Just one
npx skills add argahv/novelty-skills --skill contrarian

# Global (available across all projects)
npx skills add argahv/novelty-skills -g -y -s '*'
```

Or clone:

```bash
git clone https://github.com/argahv/novelty-skills ~/.claude/skills/novelty-skills
```

Then use any pattern:

```
/contrarian "Claim: Microservices improve velocity"
/assumption-excavator "Plan: Launch in 6 weeks"
/cross-pollinator "Stuck on cache invalidation"
```

Run all 11 in parallel for the full AGORA treatment ([AGENTS.md](AGENTS.md)).

---

## Why

Most agent skills teach process (how to deploy, test, review). These teach thinking — how to see what everyone else missed, challenge what everyone else accepts, and find the breakthrough everyone else walked past.

Part of the [Sisyphus Academica](https://github.com/argahv/sisyphus-academica) project.

New pattern that survives the existing 11? [Contribute it.](CONTRIBUTING.md) If it finds something the others miss, it belongs here.

MIT license.
