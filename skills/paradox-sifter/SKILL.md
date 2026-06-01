---
name: paradox-sifter
description: Paradox Sifter — Find the Contradictions Everyone Ignored
---

name: paradox-sifter
description: "Cross-reference every 'Limitations' section across papers on the same topic to find contradictions and ignored tensions. Use when doing literature review, identifying research gaps, or writing a paper."
argument-hint: "Topic or set of papers to analyze"
---

# Paradox Sifter — Find the Contradictions Everyone Ignored

Every paper has a "Limitations" section. Nobody cross-references them. You do.

When you collect limitations from N papers on the same topic, contradictions emerge. Paper A's limitation is paper B's claimed advantage. Paper C's "future work" was already done by paper D and it didn't work.

These contradictions are where unsolved problems live.

---

## Protocol

### Step 1: Collect Limitations

Find 5-10 papers on the same topic. Extract the exact limitation statements. Include the paper's own words.

### Step 2: Cross-Reference

Create a matrix. For each pair of limitations, ask:
1. **Do these contradict each other?** (A says X causes Y, B says X does not cause Y)
2. **Do these ignore each other?** (A flags a problem, B claims to solve it without citing A)
3. **Do these compound?** (A's limitation + B's limitation = a harder problem than either alone)

### Step 3: Classify Each Paradox

| Type | Description | Opportunity |
|------|-------------|-------------|
| **Direct contradiction** | A says X, B says not-X | One of them is wrong. Find out which. |
| **Mutual ignorance** | A and B solved the same problem in incompatible ways | A synthesis could be novel. |
| **Hidden dependency** | A's solution only works if B's assumption holds | The combined system is fragile. |
| **Escalation** | Solving A's limitation exacerbates B's | Trade-off space needs mapping. |

### Step 4: Identify the Richest Paradox

The paradox with the highest combination of:
- **Ignored duration** (how long have these papers coexisted without anyone resolving this?)
- **Impact if resolved** (what would change?)
- **Testability** (can we design an experiment?)

---

## Example Output

**Topic:** "Chain-of-Thought Prompting"

**Papers:** Wei et al. (2022), Wang et al. (2023), Kojima et al. (2022), Creswell et al. (2023), Madaan et al. (2024)

**Cross-referenced limitations:**

| Paper | Limitation |
|-------|-----------|
| Wei et al. | "CoT only helps above a certain model scale (~100B parameters)" |
| Wang et al. | "Self-consistency improves CoT but requires multiple samples" |
| Kojima et al. | "Zero-shot CoT works with models as small as 7B" |
| Creswell et al. | "CoT can amplify errors — wrong reasoning chains produce wrong answers with higher confidence" |
| Madaan et al. | "Self-refinement improves CoT but benefits from external feedback" |

**Paradox found — Direct Contradiction:**

*Wei et al. (2022) claims CoT only works at ≥100B parameters. Kojima et al. (2022) shows zero-shot CoT works at 7B. Both published in the same year. Neither cites the other's limitation. The contradiction has been ignored for 3+ years.*

**Root cause:** They tested different tasks (math vs common sense) and different CoT variants (few-shot vs zero-shot). The real limitation is task-dependent, not scale-dependent.

**Resolution experiment:** Test few-shot CoT vs zero-shot CoT across 10 tasks at model sizes from 1B-100B. Find the crossover point where each variant starts working. Publish the full surface.

---

## Anti-Patterns

| Mistake | Why it fails | Fix |
|---------|-------------|-----|
| Superficial comparison | "Paper A and B are different" | Find the specific contradiction in their claims |
| Not citing sources | Claims without evidence | Quote the exact limitation statement |
| Ignoring temporal context | Older papers couldn't know | Account for when each paper was published |

## Trigger Conditions

Use this skill when:
- Asked to find "research gaps" or "future work"
- Reviewing multiple papers on the same topic
- Writing a "Related Work" section
- The user says "there's a contradiction in the literature"
