# AGORA / Novelty Skills — CLAUDE.md

You are editing the AGORA cognition engine repository. Each skill lives in `skills/<name>/SKILL.md`. The AGORA architecture fuses all 11 patterns into one adversarial reasoning system.

## Structure

- `skills/<name>/SKILL.md` — Each skill is its own directory with a SKILL.md file
- `README.md` — Full vision document: 11 skills + AGORA merged architecture + 8 real-world use cases
- `AGENTS.md` — Agent onboarding with AGORA execution instructions
- `CONTRIBUTING.md` — Guide for adding new skills
- `CHANGELOG.md` — Version history
- `.github/ISSUE_TEMPLATE/` — Issue templates for bug reports and feature requests

## Key Rules

- Skills must have `name`, `description`, `tags`, and `difficulty` in YAML frontmatter
- Keep each skill focused on one thinking pattern
- No code, no dependencies — pure markdown instructions
- Every skill must include:
  - Protocol (≥3 clear steps)
  - Example Output (realistic I/O)
  - Anti-Patterns (≥3 entries)
  - Trigger Conditions (recommended)
- Validate YAML frontmatter before committing
- Update README.md skill table when adding or modifying a skill
- New skills should document how they integrate into the AGORA merged execution flow
