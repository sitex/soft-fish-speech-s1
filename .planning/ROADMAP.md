# Roadmap: soft-fish-speech-s1

## Phases

- [ ] **Phase 1: Dependency and Model-Free CLI Baseline** - Turn the verified lockfile state into a deterministic no-download project gate.

## Phase Details

### Phase 1: Dependency and Model-Free CLI Baseline
**Goal:** The operator can reproduce offline dependency and model-free CLI checks through one gate that never implies model inference.
**Mode:** mvp
**Depends on:** Nothing (first phase)
**Requirements:** S1-01, S1-02, S1-03
**Success Criteria:**
1. The repository-owned lockfile integrity check passes offline.
2. Supported package and CLI boundaries return deterministic documented results without loading weights.
3. One verification command runs both groups and exits nonzero on a real failure.
4. Model loading, speech generation, cloning, WebUI, and API checks are visibly reported as skipped.
5. Existing untracked `src/` and `tests/` remain outside the phase commit until separately reviewed.
**Plans:** TBD

## Progress

| Phase | Plans Complete | Status | Completed |
|-------|----------------|--------|-----------|
| 1. Dependency and Model-Free CLI Baseline | 0/TBD | Not started | - |
