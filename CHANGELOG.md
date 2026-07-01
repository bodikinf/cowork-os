# Changelog

All notable changes to cowork-os are documented here. Format loosely based on Keep a Changelog; versioning follows SemVer (pre-1.0, so minor versions add features).

## [0.2.0] - 2026-07-01 — Build a company brain your team owns

cowork-os grows from "a Cowork workspace with memory" into what it was always for: a **company brain your team owns**, the decisions, context and processes your work runs on, in plain Markdown you can read, correct and govern. Not a memory engine, not a vendor you rent.

### Added
- **Knowledge Transfer skill** and `/cowork-os:knowledge-transfer` command: an objective-first interview that captures the tacit know-how in a person's head (the exceptions, the decision criteria, the unwritten rules) and writes it into the workspace as processes, rules with a source, a glossary and open questions. This is how the company brain gets built from people, not only from files.
- **A real elicitation engine, not a questionnaire.** After a few standard questions it generates each follow-up from your last answer: starts from a real case, pounces on hedge words ("usually", "it depends"), contrasts with a novice, separates the official process from the real one, and reconstructs the workflow for you to correct.
- **Process capture in onboarding.** `/cowork-os:install` now ends by offering to capture your most at-risk process with a bus-factor question ("if your most experienced person were away a week, what breaks first?"). About 15 minutes, skippable, and the brain grows over time.
- **`context/processes/`**, the home for how work actually gets done, with a template.
- **Proactive by default.** The core now offers to turn recurring work into a scheduled routine, and repeatable multi-step jobs into a reusable custom skill, because most users do not know these exist.

### Changed
- **Repositioned to "build a company brain you own":** README, banner, demo GIF, social preview, plugin description and topics.
- Plugin manifest bumped to `0.2.0`.

## [0.1.1] - 2026-06

- Plugin manifest fix and guided installer hardening (stop rule, inline routing, organic-marketing shape, connector checks).

## [0.1.0] - 2026-06

- Initial release: the cowork-os workspace (folder conventions + Memory Update protocol), Project Instructions, the Relentless Outcome Workflow, LinkedIn Growth OS, mission mode, and recurring scheduled routines.
