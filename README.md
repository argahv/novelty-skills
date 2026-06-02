<div align="center">

# AGORA — 11 ways to see what everyone missed

**Thinking patterns that catch each other's blind spots — for every decision, design, and disaster you'll face today.**

[![CI](https://github.com/argahv/novelty-skills/actions/workflows/ci.yml/badge.svg)](https://github.com/argahv/novelty-skills/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Install via npx](https://img.shields.io/badge/install-npx_skills_add-blue)](https://github.com/argahv/novelty-skills)

</div>

Most bad decisions don't look bad at the time. They look like consensus. They look like "everyone knows." They look like the obvious choice that the whole team agrees on — because the whole team shares the same blind spots.

AGORA breaks that reflex.

It gives your AI 11 different ways to see each problem — not one. Each pattern inverts assumptions, imports solutions from distant fields, generates ideas nobody asked for, and stress-tests every output against the other 10. When they converge, you can trust it. When they fight, the tension is where breakthroughs live.

Works with Claude Code, Codex, Cursor, Gemini CLI, and any AI that reads SKILL.md. Installs in 5 seconds.

```bash
npx skills add argahv/novelty-skills
```

---

## Why you'll use this

**The contrarian** — You know that thing "everyone knows" is true? What if it isn't? It'll flip your most settled belief and see if the inversion holds together.

**The assumption-excavator** — You're about to commit to something. It'll surface the 1-3 hidden assumptions that will kill you if they're wrong — and design the cheapest test for each.

**The cross-pollinator** — You're stuck on a problem. It'll pull solutions from 15 fields you've never touched — how does an immunologist solve this? A military strategist? A jazz musician?

**The heretic** — You need a breakthrough, not an improvement. It'll generate 50 wild hypotheses, score each one, and find the idea that's weird enough to work.

**The counterfactual** — Everyone uses X. But what if X never existed? It'll find the road not taken — the approach abandoned because attention flowed elsewhere, not because it was worse.

**The paradox-sifter** — Three sources say three different things. It'll cross-reference all of them and find the contradiction nobody resolved.

**The theorist** — Someone claims something is "provably true." It'll check the proof for the hidden constant, the unstated assumption, the edge case that breaks everything.

**The empiricist** — Someone shows you results. It'll audit the baselines, check the error bars, and ask the question nobody asked: "would this survive a different random seed?"

**The skeptic** — Everything could be wrong. It'll demand the specific evidence that would prove it — and tell you what grade the current evidence earns.

**The pragmatist** — Someone proposes a solution. It'll calculate the real cost — hardware, ops complexity, maintenance burden — and ask the most dangerous question: "so what?"

**The dreamer** — The team stopped at "good enough." It'll push every dimension to 10× and find the one extension that would be disproportionately impactful if it worked.

---

## The AGORA effect

Use any one pattern and you'll see things your peers miss. Use all 11 together and something else happens.

```
Pass 1 — DIVERGE
  All 6 generators fire in parallel. Each sees a different angle.
  Assumption-Excavator finds what nobody stated.
  Contrarian inverts what "everyone knows."
  Heretic pushes past the first 30 safe ideas into the breakthrough zone.
  Cross-Pollinator imports mechanisms from immunology, strategy, music.
  Counterfactual finds the road not taken.
  Dreamer pushes every dimension to 10×.

  Each output feeds every other output.
  Heretic's wild idea becomes Contrarian's next inversion target.
  Cross-Pollinator's imported mechanism becomes Dreamer's pushed dimension.

Pass 2 — EMERGE
  Paradox-Sifter cross-references all 6 outputs looking for:
  • Convergences (3+ patterns found the same thing → high confidence)
  • Creative tensions (Dreamer says 10×, Pragmatist says "so what?" → 
    the exact frontier of feasible ambition)
  • Suppressed alternatives resurrected (Counterfactual + Heretic agree 
    → might be the real breakthrough)

Pass 3 — CONVERGE
  All 5 reviewers stress-test every surviving output:
  • Theorist: formal soundness
  • Empiricist: what experiment confirms or falsifies this?
  • Skeptic: what would prove this wrong?
  • Pragmatist: does this matter in practice?
  • Dreamer: if this works, what's next?

Pass 4 — SYNTHESIS
  A structured answer, not a single guess:
  • The consensus view (survived all 5, high confidence)
  • The contrarian view (might be true, everyone ignores it)
  • The suppressed alternative (the road not taken, documented with 
    trigger conditions for when it becomes the right choice)
  • The haunting idea (what this should really be about)
  • The critical assumptions (what everything rests on, cheapest 
    way to test each)
  • The dangerous paradox (contradiction everyone missed)
```

**11 patterns = 55 bidirectional cross-checks + 1 paradox matrix + 1 synthesis pass.** A reasoning system with no single point of failure and no cognitive blind spot.

---

## Where it hits hardest

### Post-mortems that find root causes, not symptoms

**Without AGORA:** "The DB connection pool ran out." Fix: increase pool size. Repeat next month.

**With AGORA:** The assumption-excavator catches that the pool limit was a symptom. The cross-pollinator imports contact tracing from epidemiology — connection spikes follow disease outbreak patterns. The heretic generates "Hypothesis #31: the outage was a monitoring artifact." Result: you fix the actual root cause (retry storm with no circuit breaker) instead of treating the symptom.

### Architecture decisions that don't age into regrets

**Without AGORA:** "We chose Kafka because scalability." Six months later, nobody remembers why. You're paying for a distributed system on a 3-node cluster.

**With AGORA:** The counterfactual removes Kafka's canonical papers from history — you'd use SQS + partitioning. The pragmatist calculates ops cost against your actual throughput. The result isn't "Kafka is wrong" — it's a decision tree with explicit thresholds: "Kafka now, revisit at 20 engineers. If latency <10ms matters, lean SQS." The road not taken is documented with the conditions that make it the right choice.

### Startups that don't build things nobody wants

**Without AGORA:** Founders build what they believe. Investors fund what they believe. ~90% fail.

**With AGORA:** The assumption-excavator surfaces "you assume engineering teams can buy tools without security review." They can't — 70% of enterprises require VP approval. The heretic finds the pivot before you write code: "sell to security teams, not engineering." The pragmatist prices by fix count, not seat. Result: you identify the real buyer and price correctly before building.

### Acquisitions where you don't overpay for hype

**Without AGORA:** "Codebase looks clean. Team seems solid." — said before every failed acquisition.

**With AGORA:** The paradox-sifter cross-references the target's claims against their own earlier work — finds a contradiction (claimed CPU-only, earlier paper used GPU clusters). The empiricist audits their benchmarks (synthetic data, not real distributions). You negotiate 40% off and acquire the dataset (valuable) while replacing the model (broken).

### Security audits that find zero-days, not known CVEs

**Without AGORA:** CVE scanner checks known patterns. Novel vulns stay hidden until exploited.

**With AGORA:** The counterfactual removes JWT as the canonical auth solution — you'd use HTTP-only session cookies with a smaller attack surface. The heretic generates "Hypothesis #37: the JWT library accepts 'none' algorithm from a version mismatch." The cross-pollinator imports immunology's autoimmune model: one service impersonating another via shared JWT trust. Zero-days found before any attacker.

---

## Install

```bash
# Install all patterns — browse and select interactively
npx skills add argahv/novelty-skills

# Install a specific pattern
npx skills add argahv/novelty-skills --skill contrarian

# Install globally (available across all projects)
npx skills add argahv/novelty-skills -g -y -s '*'
```

Or clone manually:

```bash
git clone https://github.com/argahv/novelty-skills ~/.claude/skills/novelty-skills
```

Then use any pattern as a slash command:

```
/contrarian "Claim: Microservices improve velocity"
/assumption-excavator "Plan: Launch in 6 weeks"
/cross-pollinator "Stuck on cache invalidation"
/heretic "Paper: Attention is All You Need"
```

Or run all 11 in parallel for the full AGORA treatment. See [AGENTS.md](AGENTS.md) for the execution loop.

---

## Why this exists

Most agent skills teach process — how to deploy, how to test, how to review. These teach thinking — how to see what everyone else missed, challenge what everyone else accepts, and find the breakthrough that everyone else walked past.

Part of the [Sisyphus Academica](https://github.com/argahv/sisyphus-academica) project.

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). New thinking patterns that survive the existing 11 are always welcome — that's how AGORA evolves. If your pattern finds something the others miss, it belongs here.

---

## License

MIT — see [LICENSE](LICENSE).
