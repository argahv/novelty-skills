# PRISM / Novelty Skills — CLAUDE.md

You are editing the PRISM cognition engine repository. Each skill lives in `skills/<name>/SKILL.md`. The PRISM architecture fuses all 11 patterns into one adversarial reasoning system, orchestrated by `skills/prism/SKILL.md`.

## Structure

- `skills/<name>/SKILL.md` — Each skill is its own directory with a SKILL.md file
- `skills/prism/SKILL.md` — The PRISM orchestrator (4-phase pipeline execution protocol)
- `README.md` — Landing page: 12 skills + PRISM merged architecture + use cases
- `AGENTS.md` — Agent onboarding with PRISM execution instructions
- `CONTRIBUTING.md` — Guide for adding new skills
- `CHANGELOG.md` — Version history
- `.github/ISSUE_TEMPLATE/` — Issue templates for bug reports and feature requests

## Key Rules

- Skills must have `name`, `description`, `tags`, `difficulty`, and `argument-hint` in YAML frontmatter
- Keep each skill focused on one thinking pattern
- No code, no dependencies — pure markdown instructions
- Every skill must include:
  - Protocol (≥3 clear steps)
  - Example Output (realistic I/O)
  - Anti-Patterns (≥3 entries)
  - Trigger Conditions (recommended)
  - PRISM Integration section (required) — structured output format + cross-pattern dependencies
- Validate YAML frontmatter before committing
- Update README.md skill table when adding or modifying a skill
- New skills should document their PRISM Integration (output format, consumed by, consumes from)
