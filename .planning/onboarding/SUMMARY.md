# Brownfield onboarding summary

- Repository: `soft-fish-speech-s1`
- Mode: fast brownfield onboarding
- Sources: canonical shared baseline, `GSD-BOOTSTRAP.md`, README, project goal, package metadata, repository tree, and Git history
- Codebase map: fast map complete (`STACK.md`, `INTEGRATIONS.md`, `ARCHITECTURE.md`, `STRUCTURE.md`)
- Existing capabilities validated: package, model, inference-engine, CLI, API, WebUI, and server surfaces are present; no model-backed runtime claim is made
- Preserved evidence: commit `63433c7` and a passed `uv lock --check --offline`
- Active milestone: v1 dependency and model-free CLI baseline
- Active requirements: S1-01 through S1-03 map to Phase 1
- Next action: discuss and plan the dependency and model-free CLI baseline
- Verification gap: no `scripts/verify`; no checkpoint download or S1 inference performed
