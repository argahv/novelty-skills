# Novelty Skills — CLAUDE.md

You are editing a skills repository. Each skill lives in `skills/<name>/SKILL.md`.

## Structure

- `skills/<name>/SKILL.md` — Each skill is its own directory with a SKILL.md file
- `README.md` — Landing page with skill catalog
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
