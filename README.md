# verse-assets

Downloadable asset packs (voices, Bibles) for the Mannael iOS app. Release assets only — no code.

Each pack is published as a GitHub Release asset. The app checks every download against a SHA-256 hash pinned in the app before installing it. Every pack zip contains its own `LICENSE.txt` (full licence text + copyright notice) and, for Bibles, `CHANGES.txt` (what was changed from the source). Full licence texts are also in [`licenses/`](licenses/).

## Packs

| Release | File | Contents | Licence |
|---|---|---|---|
| [`voice-claude-high-1`](https://github.com/Gvindor/verse-assets/releases/tag/voice-claude-high-1) | `voice-claude-high-1.zip` (58 MB) | Mexican Spanish text-to-speech voice, high quality (Piper / VITS, fp32 ONNX) | Apache-2.0 |
| [`bible-PDPT-1`](https://github.com/Gvindor/verse-assets/releases/tag/bible-PDPT-1) | `bible-PDPT-1.zip` (1.4 MB) | *Palabra de Dios para ti* — Spanish Bible text | CC BY 4.0 |

## Credits and licenses

### "Claude" Spanish voice (`voice-claude-high-1`)

- **Voice:** `es_MX-claude-high`, a Piper (VITS) voice by **HirCoir**. Source: https://huggingface.co/spaces/HirCoir/Piper-TTS-Spanish
- **License:** Apache License 2.0 — https://www.apache.org/licenses/LICENSE-2.0 · [full text](licenses/Apache-2.0.txt)
- **Packaged from:** the sherpa-onnx TTS model release (k2-fsa/sherpa-onnx, Apache License 2.0) — https://github.com/k2-fsa/sherpa-onnx/releases/tag/tts-models
- **Changes:** repackaged unmodified into a zip for download; no retraining or edits to the model.

### *Palabra de Dios para ti* ([`bible-PDPT-1`](https://github.com/Gvindor/verse-assets/releases/tag/bible-PDPT-1))

- **Text:** *Palabra de Dios para ti* (Biblia Latinoamericana Textual). Translation: Asociación Bíblica Latinoamericana; collaborator: Latinamerican Textual Bible Foundation, Inc.
- **Copyright:** © 2020 Asociación Bíblica Latinoamericana.
- **License:** Creative Commons Attribution 4.0 International (CC BY 4.0) — https://creativecommons.org/licenses/by/4.0/ · [full text](licenses/CC-BY-4.0.txt)
- **Source:** https://ebible.org/spapddpt/ (`spapddpt_usfm.zip`)
- **Note:** the source preamble also mentions CC BY-SA 4.0 and says *"Si altera el texto, es obligatorio cambiar el nombre de la obra."* The Bible text is **not altered** and keeps its name. Our own contributions (format changes) are additionally offered under CC BY-SA 4.0 ([full text](licenses/CC-BY-SA-4.0.txt)), so both readings are met.
- **Changes:** converted from USFM to JSON (one file per book) plus `meta.json`; footnotes, cross-references, section headings, introductions and Strong's tags omitted. **Verse text unchanged.** The maps (© Biblica, Inc.) are **not** included.
- Not to be confused with *Palabra de Dios para Todos* (PDT, © Bible League), which is a different translation and is not used.

### For all Bible packs

- The original copyright holders **do not endorse** these packs or the Mannael app.
- The material is provided **"as is", without warranties** — see Section 5 of each licence.
- Names of the translations are used only to credit them; no trademarks or logos are used.
- Each zip's `CHANGES.txt` records the exact source URL, the SHA-256 of the source file and the snapshot date.

### Software used to run the voices (inside the app, not in this repo)

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

Questions about a pack's licence or credit: open an issue in this repository.
