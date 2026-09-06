<!-- GSD:project-start source:PROJECT.md -->

## Project

**soft-fish-speech-s1**

`soft-fish-speech-s1` is the personal standalone repository for the OpenAudio S1 generation of Fish Speech. It preserves the vendor codebase and local lockfile history while keeping `fishaudio/fish-speech` as `upstream`.

**Core Value:** The operator can reproduce dependency and model-free CLI readiness before making any S1 inference claim.

### Constraints

- **Runtime**: Python 3.10+, optional PyTorch 2.5.1+, audio tooling, and external checkpoints.
- **Licensing**: code and model weights have separate terms recorded in project documentation.
- **Assets**: model weights remain external and operator-controlled.
- **Verification**: no `scripts/verify` exists; Phase 1 must add a deterministic no-download gate.

<!-- GSD:project-end -->

<!-- GSD:stack-start source:codebase/STACK.md -->

## Technology Stack

- Python >=3.10 package built with setuptools and managed by `pyproject.toml` and `uv.lock`.
- Optional PyTorch >=2.5.1 and torchaudio, plus Transformers, Lightning, Gradio, Uvicorn, ModelScope, and audio-processing dependencies.
- Package code lives in `fish_speech`; existing untracked `src/` and `tests/` are preserved outside onboarding.
- Real OpenAudio S1 inference requires external checkpoints and suitable compute resources.

<!-- GSD:stack-end -->

<!-- GSD:conventions-start source:CONVENTIONS.md -->

## Conventions

Conventions not yet established. Will populate as patterns emerge during development.
<!-- GSD:conventions-end -->

<!-- GSD:architecture-start source:ARCHITECTURE.md -->

## Architecture

# Architecture

Text and reference inputs pass through preprocessing and a text-to-semantic model, then through DAC/audio decoding. The inference engine coordinates checkpoints, references, and generation. API and WebUI layers expose the same model-backed pipeline; dependency and CLI metadata can be checked separately without loading a checkpoint.

Sources: `fish_speech/text`, `fish_speech/models`, `fish_speech/inference_engine`, and `tools/server`.
<!-- GSD:architecture-end -->

<!-- GSD:skills-start source:skills/ -->

## Project Skills

No project skills found. Add skills to any of: `.claude/skills/`, `.agents/skills/`, `.cursor/skills/`, `.github/skills/`, or `.codex/skills/` with a `SKILL.md` index file.
<!-- GSD:skills-end -->

<!-- GSD:workflow-start source:GSD defaults -->

## GSD Workflow Enforcement

Before using Edit, Write, or other file-changing tools, start work through a GSD command so planning artifacts and execution context stay in sync.

Use these entry points:

- `$gsd-quick` for small fixes, doc updates, and ad-hoc tasks
- `$gsd-debug` for investigation and bug fixing
- `$gsd-execute-phase` for planned phase work

Do not make direct repo edits outside a GSD workflow unless the user explicitly asks to bypass it.
<!-- GSD:workflow-end -->

<!-- GSD:profile-start -->

## Developer Profile

> Profile not yet configured. Run `$gsd-profile-user` to generate your developer profile.
> This section is managed by `generate-claude-profile` -- do not edit manually.
<!-- GSD:profile-end -->
