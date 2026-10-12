# Voice Conversion Demo

This is a static site for GitHub Pages. It uses only `index.html` and the WAV files under `audios/`; no Python or build step is needed. Keep `index.html` and `audios/` together so their relative links work.

- Monolingual: 10 pairs for each of Telugu, Tamil, Hindi, Punjabi, and Bengali.
- Cross-lingual: 5 pairs, one per language above.
- LibriSpeech Test-Clean: 5 pairs with different source speakers.
- SEED-TTS-VC English: 5 pairs with different target speakers.

Each pair displays source and target clips, a collapsed source transcript, and model outputs in the requested order. The cross-lingual section omits kNN-VC because no cross-lingual kNN-VC output directory was provided.

Monolingual samples are balanced across the gender labels present in each test manifest. Telugu, Punjabi, and Bengali include female and male pairs. Tamil includes female and unlabeled IVR pairs; Hindi includes male and unlabeled IVR pairs. Unlabeled IVR clips are shown as **Unspecified**, since their filenames do not establish gender.

Audio filenames are unchanged. `audios/models/` retains each model's directory structure. Ground-truth clips are grouped under `audios/groundtruth/INDIC_TEST_SETS/`, `audios/groundtruth/LibriSpeech/`, and `audios/groundtruth/seedtts_testset/`, retaining their paths within each dataset.

For GitHub Pages branch publishing, upload the **contents** of this folder to the repository root or its `docs/` folder, then select that folder in the repository's Pages settings. A dedicated `gh-pages` branch should contain these files at its root.
