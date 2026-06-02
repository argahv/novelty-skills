# Changelog

All notable changes to this project will be documented in this file.

## [2.0.0] — 2026-06-03

### Added

- **PRISM architecture**: Merged cognition engine that fuses all 11 patterns into one adversarial reasoning system with 4 phases (DIVERGE → EMERGE → CONVERGE → SYNTHESIZE)
- **8 real-world use cases**:
  - Post-Mortem / Incident Analysis
  - Architecture Decision Records (ADRs)
  - Startup / Product Strategy
  - Technical Due Diligence
  - Security Vulnerability Discovery
  - Research Paper / PhD Dissertation
  - Incident Command / Crisis Response
  - Personal / Career Decisions
- **Cross-feeding mechanism**: Each pattern's output becomes input for every other pattern in pass 2
- **Calibrated confidence system**: Outputs are structured as a possibility space with per-claim confidence (HIGH / MEDIUM / LOW / exploration signal)
- **Anti-fragile blind spot detection**: The merged system catches its own individual pattern blind spots through cross-referencing
- Agent integration guide: individual skill usage + merged PRISM execution loop + pipeline examples

### Changed

- **Rebrand**: "Novelty Skills" is now **PRISM — 11 ways to see what everyone missed**
- README expanded from 98 lines to full vision document with architecture diagram, phase descriptions, and use cases
- AGENTS.md updated with PRISM merged execution instructions
- CLAUDE.md updated with new scope and contribution guidelines

## [1.0.0] — 2026-06-01

### Added

- 11 thinking-pattern skills for AI agents:
  - 6 novelty engines: contrarian, cross-pollinator, assumption-excavator,
    paradox-sifter, heretic, counterfactual
  - 5 reviewer personas: dreamer, empiricist, pragmatist, skeptic, theorist
- `npx skills add argahv/novelty-skills` install support
- CI workflow for skill structure validation
- README with install instructions and skill catalog
