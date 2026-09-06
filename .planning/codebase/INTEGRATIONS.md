# Integrations

- Hugging Face, ModelScope, and Fish Audio-hosted model assets are external checkpoint boundaries.
- `tools/api_server.py`, `tools/api_client.py`, `tools/run_webui.py`, and `tools/server/` expose API and UI surfaces.
- `tools/download_models.py` is an explicit network boundary and is excluded from no-download onboarding.
- Vendor history remains at `fishaudio/fish-speech`; personal history is published through standalone `sitex/soft-fish-speech-s1`.

Sources: README.md, `tools/`, `pyproject.toml`, and Git remotes.
