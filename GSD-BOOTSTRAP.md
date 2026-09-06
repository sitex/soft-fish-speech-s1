---
document: gsd-brownfield-bootstrap
project: soft-fish-speech-s1
git_root: /home/rocky/projects/soft-fish-speech-s1
github_repository: sitex/soft-fish-speech-s1
generated_at: 2026-09-06T04:16:43Z
thoughts_status: canonical baseline and plan available
github_status: repository resolved; no project issues returned
include_personal: false
---

# Purpose

Standalone personal baseline for the OpenAudio S1 generation of Fish Speech, retaining the vendor repository as `upstream`. [T1][R1]

# Implemented Capabilities

- `fish_speech` contains text, inference-engine, text-to-semantic, DAC, configuration, and utility modules. [R2]
- API, server, WebUI, model-download, and client entry points exist under `tools/`. [R2]
- The upstream README documents OpenAudio S1/S1-mini, voice cloning, expressive markers, WebUI, and server surfaces. [R1]
- Commit `63433c7` preserves the local dependency lock baseline and passed `uv lock --check --offline`. [T1]

# Current Milestone

Active v1: a reproducible dependency and model-free CLI baseline. No model-backed behavior is claimed. [T1]

# Open Requirements

- Reproduce the offline lockfile integrity check.
- Verify deterministic package and CLI boundaries without downloading weights.
- Add one repository verification command that distinguishes model-free checks from model-backed skips.

# Accepted Decisions

- Use a standalone `sitex/soft-fish-speech-s1` repository because GitHub permits one fork per account in the Fish Speech fork network.
- Preserve `fishaudio/fish-speech` as `upstream` and publish personal work through `origin/portfolio`.
- Keep existing untracked `src/` and `tests/` outside onboarding.

# Constraints

- Python 3.10+, optional PyTorch 2.5.1+, audio dependencies, and external checkpoints are required for real inference. [R3]
- Code and model assets have distinct license terms. [R1][R4]

# Unresolved Conflicts

None identified from available sources.

# Source Thoughts

- T1: `/home/rocky/thoughts/repos/soft-fish-speech-s1/shared/research/2026-09-06-project-baseline.md`
- T2: `/home/rocky/thoughts/repos/soft-fish-speech-s1/shared/plans/2026-09-06-gsd-onboarding.md`

# Source Issues

No project issues were returned by GitHub during onboarding.

# Source Limitations

No checkpoint download, S1 inference, audio generation, cloning, WebUI, or API execution was performed.

Sources: [R1] README.md; [R2] repository tree; [R3] pyproject.toml and uv.lock; [R4] PROJECT_GOAL.md.
