# verse-assets

Downloadable asset packs (voices, Bibles) for the Mannael iOS app. Release assets only — no code.

Each pack is published as a GitHub Release asset. The app checks every download against a SHA-256 hash pinned in the app before installing it.

## Packs

| Release | File | Contents |
|---|---|---|
| [`voice-claude-high-1`](https://github.com/Gvindor/verse-assets/releases/tag/voice-claude-high-1) | `voice-claude-high-1.zip` (58 MB) | Mexican Spanish text-to-speech voice, high quality (Piper / VITS, fp32 ONNX) |

## Credits and licenses

### "Claude" Spanish voice (`voice-claude-high-1`)

- **Voice:** `es_MX-claude-high`, a Piper (VITS) voice by **HirCoir**. Source: https://huggingface.co/spaces/HirCoir/Piper-TTS-Spanish
- **License:** Apache License 2.0 — https://www.apache.org/licenses/LICENSE-2.0
- **Packaged from:** the sherpa-onnx TTS model release (k2-fsa/sherpa-onnx, Apache License 2.0) — https://github.com/k2-fsa/sherpa-onnx/releases/tag/tts-models
- **Changes:** repackaged unmodified into a zip for download; no retraining or edits to the model.

### Software used to run the voice (inside the app, not in this repo)

- **Piper** — MIT License — https://github.com/rhasspy/piper
- **sherpa-onnx** — Apache License 2.0 — https://github.com/k2-fsa/sherpa-onnx
- **ONNX Runtime** — MIT License — https://github.com/microsoft/onnxruntime

### Bible texts used by the app (bundled in the app, not in this repo)

| Text | Status | Source |
|---|---|---|
| King James Version (1769 Blayney text) | Public domain | https://github.com/aruljohn/Bible-kjv |
| Berean Standard Bible | Public domain (dedicated 2023-04-30) | https://berean.bible/terms.htm |
| Santa Biblia — Reina-Valera 1909 | Public domain (*Dominio Público*) | https://ebible.org/details.php?id=spaRV1909 |
| La Biblia en Español Sencillo — translated and edited by Irma Flores, AudioBiblia.org | Public domain | https://ebible.org/details.php?id=spabes · https://audiobiblia.org |

Full app acknowledgements: https://mannael.netlify.app/acknowledgements.html
