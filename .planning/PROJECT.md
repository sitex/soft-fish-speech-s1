# soft-fish-speech-s1

## What This Is

`soft-fish-speech-s1` is the personal standalone repository for the OpenAudio S1 generation of Fish Speech. It preserves the vendor codebase and local lockfile history while keeping `fishaudio/fish-speech` as `upstream`.

## Core Value

The operator can reproduce dependency and model-free CLI readiness before making any S1 inference claim.

## Requirements

### Validated

- ✓ OpenAudio S1/S1-mini package, inference-engine, CLI, API, WebUI, and server surfaces exist — repository inspection.
- ✓ Commit `63433c7` preserves the dependency lock change and passed `uv lock --check --offline` — local evidence.
- ✓ Personal history is published to standalone `sitex/soft-fish-speech-s1` while vendor history remains under `upstream` — onboarding.

### Active

- [ ] Reproduce dependency-lock integrity without network access.
- [ ] Exercise deterministic package and CLI boundaries without downloading a checkpoint.
- [ ] Add one project verification command that reports model-backed checks as explicit skips.

### Out of Scope

- Downloading S1/S1-mini checkpoints during onboarding.
- Claiming speech generation, cloning quality, WebUI, or API readiness from metadata checks.
- Committing existing untracked `src/` and `tests/` without provenance review.

## Context

GitHub permits only one fork per account in a fork network, and `sitex/soft-fish-speech` already occupies the Fish Speech network. This project is therefore a standalone public repository rather than a fork. The checked-out `portfolio` branch preserves the older OpenAudio S1 baseline and local lockfile commit without rewriting vendor history.

## Constraints

- **Runtime**: Python 3.10+, optional PyTorch 2.5.1+, audio tooling, and external checkpoints.
- **Licensing**: code and model weights have separate terms recorded in project documentation.
- **Assets**: model weights remain external and operator-controlled.
- **Verification**: no `scripts/verify` exists; Phase 1 must add a deterministic no-download gate.

## Key Decisions

| Decision | Rationale | Outcome |
|----------|-----------|---------|
| Use a standalone personal repository | GitHub allows only one fork in the same network per account | ✓ Good |
| Keep vendor history as `upstream` | Preserve a clear source boundary | ✓ Good |
| Publish local history through `origin/portfolio` | Avoid rewriting or conflating vendor branches | ✓ Good |
| Preserve untracked `src/` and `tests/` | Their provenance is unresolved | — Pending |

## Evolution

Update this document at phase transitions and milestone boundaries. Move requirements to Validated only with reproducible evidence, keep model-free and model-backed claims separate, and recheck upstream and licensing constraints before releases.

---
*Last updated: 2026-09-06 after brownfield initialization*
