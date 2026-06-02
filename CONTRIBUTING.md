# Contributing to Novelty Skills

Thanks for your interest! This project grows through contributions of new thinking patterns, improvements to existing skills, and bug reports.

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
   - Optional: `## Trigger Conditions` for automatic invocation

3. **Update this README** with the new skill added to the appropriate table.

4. **Open a pull request.** CI will validate the structure automatically.

---

## Skill Quality Standards

| Section | Required? | Minimum |
|---------|-----------|---------|
| YAML frontmatter (name, description) | ✅ Yes | Must parse |
| Protocol | ✅ Yes | ≥3 clear steps |
| Example Output | ✅ Yes | Realistic I/O, not placeholder |
| Anti-Patterns | ✅ Yes | ≥3 entries |
| Trigger Conditions | ⬜ Recommended | List of patterns/phrases |

---

## Reporting Issues

- **Bug**: A skill produces wrong or misleading output. Include the input and actual output.
- **Enhancement**: A skill could be improved. Describe what's missing.
- **New skill idea**: Suggest a thinking pattern not yet covered.

---

## Pull Request Process

1. Create a branch from `main`
2. Make your changes
3. Run `python -m pytest` if you've added any tooling
4. Open a PR — a maintainer will review

---

## Code of Conduct

Be respectful. This project spans many fields and backgrounds. Assume good intent. No gatekeeping.
