---
name: assumption-excavator
description: "Find unstated assumptions in any plan, design, or argument. Test what breaks if each assumption is false. Use when reviewing a design, planning a project, or reading a paper."
argument-hint: "The plan, design, or argument to excavate"
---

# Assumption Excavator — Find What Everyone Assumed

Every failed project had a critical assumption that nobody checked. You are the tool that finds them before they fail.

---

## Protocol

### Step 1: Surface Every Assumption

Read the input and list every assumption made — both stated and unstated. Categorize:

| Category | Examples |
|----------|----------|
| **Resource assumptions** | "We have enough GPUs." "The API stays free." |
| **Behavioral assumptions** | "Users will read the instructions." "Engineers will write tests." |
| **Environmental assumptions** | "The network is reliable." "The database is always available." |
| **Temporal assumptions** | "Nothing changes while we build." "The market stays the same." |
| **Causal assumptions** | "X causes Y." "If we build it, they will come." |
| **Scalability assumptions** | "Works at 10 users = works at 10M." "Linear cost growth." |
| **Compositional assumptions** | "Components that work independently work together." |

### Step 2: Test Each Assumption

For each assumption, ask:
1. **What would break if this assumption is false?**
2. **How would we know it's false before it's too late?**
3. **What's the cheapest way to validate this assumption?**

### Step 3: Identify the Critical Few

Most assumptions are safe. 1-3 are dangerous. Flag the ones where:
- Falsehood would be catastrophic
- Falsehood is plausible
- We have no way to detect falsehood early

### Step 4: Design a Test

For each critical assumption, specify the minimum experiment that could falsify it.

---

## Example Output

**Input:** "We're building a code generation agent. We'll sell it to enterprise engineering teams for $50/seat/month. They hook it into their GitHub and it generates PRs automatically."

**Assumptions surfaced:**

1. Engineering teams have authority to buy tools without security review — **Critical**
2. Developers trust AI-generated PRs — **Critical**
3. GitHub API rate limits allow automated PR generation at scale
4. Enterprise codebases are clean enough that AI-generated code integrates cleanly
5. Security teams will approve a tool that writes code
6. $50/seat/month is below the "expenseable without VP approval" threshold
7. The tool works equally well across codebases in different languages
8. Generated code doesn't introduce security vulnerabilities
9. PR review costs are lower than the code-writing costs being saved
10. Teams want more PRs, not fewer

**Critical assumptions:**

**#1 (buying authority):** If VP approval is required, the sales cycle goes from 1 week to 9 months. Most security teams block AI code generation tools.

**Test:** Survey 20 engineering leaders at target companies. Ask: "Could you buy this with a company card or does it need VP+ approval?"

**#2 (trust):** If developers spend as much time reviewing AI-generated PRs as writing code themselves, the value proposition collapses.

**Test:** Run a pilot with 5 engineers. Measure time-to-merge for AI-generated vs human-written PRs. If review time > 0.5x writing time, the value prop is weak.

**#5 (security approval):** If security teams block the tool, enterprise sales are zero regardless of engineering interest.

**Test:** Ask 3 enterprise security engineers: "What would you need to approve an AI that writes production code?" If the answer includes things you can't provide (e.g., SOC2, on-prem deployment, human-in-the-loop for every PR), adjust the product.

---

## Anti-Patterns

| Mistake | Why it fails | Fix |
|---------|-------------|-----|
| Only surfacing obvious assumptions | Stated assumptions are usually fine | Look for the ones nobody says aloud |
| Not differentiating critical from trivial | Everything is an assumption | Flag the 1-3 that would kill the project |
| Not suggesting a test | Assumptions are only dangerous if untested | Always propose the minimum falsification experiment |

## Trigger Conditions

Use this skill when:
- Reviewing a project plan
- Evaluating a proposal
- The user says "it should work because..."
- Before committing to a significant decision
- A project is behind schedule (something was assumed)
