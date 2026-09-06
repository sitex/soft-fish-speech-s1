# Architecture

Text and reference inputs pass through preprocessing and a text-to-semantic model, then through DAC/audio decoding. The inference engine coordinates checkpoints, references, and generation. API and WebUI layers expose the same model-backed pipeline; dependency and CLI metadata can be checked separately without loading a checkpoint.

Sources: `fish_speech/text`, `fish_speech/models`, `fish_speech/inference_engine`, and `tools/server`.
