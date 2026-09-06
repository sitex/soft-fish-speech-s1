# Requirements: soft-fish-speech-s1

**Defined:** 2026-09-06
**Core Value:** Reproduce dependency and model-free CLI readiness before making S1 inference claims.

## v1 Requirements

### No-Download Baseline

- [ ] **S1-01**: Operator can run the repository lockfile integrity check offline and receive a deterministic result.
- [ ] **S1-02**: Operator can invoke supported package and CLI help or argument-validation boundaries without downloading or loading model weights.
- [ ] **S1-03**: Operator can run one project verification command that distinguishes dependency passes, CLI passes, model-backed skips, and failures.

## v2 Requirements

### Model-Backed Runtime

- **S1-04**: Operator can synthesize valid audio from an approved local OpenAudio S1 or S1-mini checkpoint.
- **S1-05**: Operator can verify voice cloning, expressive controls, WebUI, and API behavior on compatible hardware.

## Out of Scope

| Feature | Reason |
|---------|--------|
| Automatic model downloads | Asset acquisition is operator-controlled. |
| Model-inference claims from dependency checks | Lockfile and CLI boundaries do not execute generation. |
| Existing untracked `src/` and `tests/` | Intent and provenance remain unresolved. |

## Traceability

| Requirement | Phase | Status |
|-------------|-------|--------|
| S1-01 | Phase 1 | Pending |
| S1-02 | Phase 1 | Pending |
| S1-03 | Phase 1 | Pending |

**Coverage:** 3 total, 3 mapped, 0 unmapped ✓

---
*Requirements defined: 2026-09-06*
*Last updated: 2026-09-06 after brownfield initialization*
