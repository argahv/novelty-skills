---
name: counterfactual
description: Counterfactual — The Field Without Its Most-Cited Papers
---

name: counterfactual
description: "Rewrite a field's history without the most-cited papers. Find what would have been invented instead. Use when looking for overlooked approaches or questioning canonical results."
argument-hint: "Topic, paper, or field to explore counterfactually"
---

# Counterfactual — The Field Without Its Most-Cited Papers

The most-cited paper in a field is not necessarily the best. It's the one that got the most attention. Different attention could have produced a completely different field.

You simulate that different timeline.

---

## Protocol

### Step 1: Identify the Canonical Papers

Find the 3-5 most-cited papers in a subfield. These are the papers that shaped the consensus.

### Step 2: Remove Each One

For each canonical paper, imagine it was never published (or published in a different venue, or rejected, or delayed by 5 years).

### Step 3: Trace the Ripple Effects

For each removed paper:
1. **What immediately changes?** (No one cites it. No one builds on it.)
2. **What problems remain unsolved?** (This paper "solved" something. Without it, that solution doesn't exist.)
3. **What other approaches would have been explored?** (The paper made certain paths seem unnecessary. Without it, those paths would have attracted researchers.)
4. **What would have been invented instead?** (This is the key. The vacuum would have been filled.)

### Step 4: Identify the Suppressed Alternative

The most valuable output: an approach that was **actively suppressed** by the success of the canonical paper — not because it was worse, but because attention flowed to the canonical approach.

---

## Example Output

**Field:** Deep Learning

**Canonical paper:** Krizhevsky et al. (2012) — "ImageNet Classification with Deep Convolutional Neural Networks" (AlexNet)

**Counterfactual: What if AlexNet had not achieved breakthrough results in 2012?**

**Immediate changes:**
- No "ImageNet moment" for deep learning
- No mass migration of researchers from other fields to deep learning
- GPU computing for ML remains niche

**What problems remain unsolved:**
- Large-scale image classification (obviously)
- Transfer learning at scale
- The "embarrassment of riches" problem in computer vision

**What other approaches would have been explored:**
- Graphical models would continue as the dominant paradigm for structured prediction
- Kernel methods would receive more attention (they were competitive on smaller datasets)
- Unsupervised feature learning (sparse coding, autoencoders) would have been the main path to scaling
- Capsule networks (Hinton's alternative to CNNs) would have received far more research attention
- Neuromorphic computing might have gained earlier traction

**Suppressed alternative found:**
*Capsule Networks.* Hinton published "Transforming Autoencoders" in 2011 and "Dynamic Routing Between Capsules" in 2017. Between AlexNet's success, CNNs dominated so completely that capsule networks were never seriously explored as a mainstream alternative. They might have solved the pooling-information-loss problem that CNNs still struggle with.

**Plausibility assessment:** Moderate. Capsule networks are computationally expensive. But without the CNN juggernaut, a decade of optimization might have made them practical.

---

## Anti-Patterns

| Mistake | Why it fails | Fix |
|---------|-------------|-----|
| Removing a paper nobody would miss | The canon is defined by influence | Pick papers with 5,000+ citations |
| Wishful thinking | "Without paper X, my favorite approach would have won" | Be honest about why the canonical paper won |
| Not considering timing | Later papers depend on earlier ones | Remove the paper and trace forward, not backward |

## Trigger Conditions

Use this skill when:
- The field seems settled — "this is the way things are done"
- You want to identify research directions that were prematurely abandoned
- Looking for novel approaches that challenge orthodoxy
- The user asks "why does everyone use approach X?"
