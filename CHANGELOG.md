# Changelog

All notable changes to this project will be documented in this file.

## [2.0.0] — 2026-06-03

### Added

- **PRISM architecture**: Merged cognition engine that fuses all 11 patterns into one adversarial reasoning system with 4 phases (DIVERGE → EMERGE → CONVERGE → SYNTHESIS)
- **PRISM orchestrator skill** (`skills/prism/SKILL.md`): Full pipeline specification with structured YAML output templates, confidence calibration rules, and 7-part synthesis format
- **PRISM Integration sections** in all 11 skills: standardized output schemas, finding type taxonomy, cross-pattern dependency declarations
- **Cross-feed mechanism**: Each pattern's output has a defined format that other patterns can consume (consumed_by / consumes_from)
- **Calibrated confidence system**: 4-tier (HIGH / MEDIUM / LOW / EXPLORATION) with exact promotion rules based on cross-pattern convergence
- **AGENTS.md rewritten**: From 4-line handwave to full execution protocol with all 4 phases, dependency graph, and confidence calibration table
- **README rebrand**: Visual overhaul with box-drawing hero, compact skill grid, pipeline diagram, diff-format use cases

### Changed

- **Rebrand**: Renamed from AGORA to PRISM across all documentation
- All 5 reviewer persona descriptions rewritten to be decision-focused, not academic
- All 5 reviewer personas now have `argument-hint` in YAML frontmatter for consistency
- `counterfactual`, `paradox-sifter`, `heretic`, `theorist`, `empiricist` descriptions updated for broader applicability

## [1.0.0] — 2026-06-01

### Added

- 11 thinking-pattern skills for AI agents:
  - 6 novelty engines: contrarian, cross-pollinator, assumption-excavator,
    paradox-sifter, heretic, counterfactual
  - 5 reviewer personas: dreamer, empiricist, pragmatist, skeptic, theorist
- `npx skills add argahv/novelty-skills` install support
- CI workflow for skill structure validation
- README with install instructions and skill catalog
