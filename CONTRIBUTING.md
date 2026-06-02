# Contributing to AGORA / Novelty Skills

Thanks for your interest! This project grows through contributions of new thinking patterns, improvements to existing skills, AGORA integration patterns, and bug reports.

---

## How to Add a New Skill

1. **Create `skills/<skill-name>/SKILL.md`** following the existing pattern:

   ```yaml
   ---
   name: <skill-name>
   description: "<one-line description>"
   tags: [thinking, novelty]
   difficulty: beginner | intermediate | advanced
   ---
   ```

2. **Every skill must have:**
   - A `## Protocol` section with clear steps
   - A `## Example Output` section showing realistic I/O
   - An `## Anti-Patterns` table showing common mistakes
   - `## Trigger Conditions` (recommended) for automatic invocation
   - `## AGORA Integration` (recommended) — how this skill feeds into and benefits from the merged architecture

3. **Update the README** with the new skill added to the appropriate table. If your skill is a new pattern type (not fitting a novelty engine or reviewer persona), add a new table.

4. **Open a pull request.** CI will validate the structure automatically.

---

## How to Contribute AGORA Integration Patterns

Beyond individual skills, AGORA thrives on **cross-pattern workflows**. Contributions in this category:

- **Pipeline recipes**: Document a multi-skill chain for a specific use case (e.g., "post-mortem pipeline: assumption-excavator → contrarían → cross-pollinator → dreamer → pragmatist → synthesis")
- **Cross-feed protocols**: How to structure the pass-2 revision step where each pattern sees all other outputs
- **Weighting schemes**: How to calibrate confidence when patterns converge vs contradict
- **Synthesis templates**: Structured output formats for the possibility space

Add these to a new `docs/` directory or as a section in an existing skill's AGORA Integration section.

---

## Skill Quality Standards

| Section | Required? | Minimum |
|---------|-----------|---------|
| YAML frontmatter (name, description) | ✅ Yes | Must parse |
| Protocol | ✅ Yes | ≥3 clear steps |
| Example Output | ✅ Yes | Realistic I/O, not placeholder |
| Anti-Patterns | ✅ Yes | ≥3 entries |
| Trigger Conditions | ⬜ Recommended | List of patterns/phrases |
| AGORA Integration | ⬜ Recommended | How it feeds the merged architecture |

---

## Reporting Issues

- **Bug**: A skill produces wrong or misleading output. Include the input and actual output.
- **Enhancement**: A skill could be improved. Describe what's missing.
- **New skill idea**: Suggest a thinking pattern not yet covered. Bonus points if you describe how it interacts with existing skills in the AGORA architecture.
- **AGORA workflow bug**: When two patterns produce contradictory outputs and the synthesis fails to resolve them — this is a feature, not a bug, but the resolution protocol may need improvement.

---

## Pull Request Process

1. Create a branch from `main`
2. Make your changes
3. Run `python -m pytest` if you've added any tooling
4. Open a PR — a maintainer will review

---

## Code of Conduct

Be respectful. This project spans many fields and backgrounds. Assume good intent. No gatekeeping. Every new thinking pattern makes AGORA stronger — even the ones that seem wrong at first. (The Contrarian will test them.)
