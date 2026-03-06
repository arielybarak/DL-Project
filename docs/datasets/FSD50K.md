# FSD50K

## Overview
- **Source:** [Zenodo](https://zenodo.org/records/4060432)
- **License:** CC-BY 4.0
- **Primary Use Case:** Large-scale generic sounds (Good for domestic, splashing, sink variety)
- **Dataset Size:** ~20 GB (51,197 files)

## Raw Format Structure
```text
FSD50K/
├── FSD50K.dev_audio/
├── FSD50K.eval_audio/
├── FSD50K.ground_truth/
└── ...
```

## Quantitative Audio/Video Metrics
*(Populate this section using findings from `03_dataset_profiling.ipynb`)*
- **Total Duration:** ~100 hours
- **Number of Expected Files:** 51,197
- **Sample Rate Distribution:** Mostly 44.1kHz (to be verified)
- **Bit Depth:** 
- **Channels (Mono/Stereo):** 
- **Clip Length Distribution:** 

## Label/Class Distribution
- **Annotation Format:** Multi-label CSV annotations utilizing the AudioSet ontology.
- **Included Classes:**
  - 200 classes (We only need a subset like Water, domestic sounds, thuds).
- **Class Balance:** Often imbalanced, highly tail-heavy.

## Data Quality & Known Pitfalls
- Varying quality (downloaded from Freesound).
- Variable clip lengths (0.3s up to 30s).
- Tags are user-generated originally, though FSD50K cleans them up.

## Standard Preprocessing Requirements
**To standardize this dataset for training, we will need to:**
- [ ] Filter dataset to only extract relevant classes using the provided CSV.
- [ ] Resample to `[Target Sample Rate]`
- [ ] Convert stereo to mono (if applicable)
- [ ] Pad or truncate files to `[Target Length]`
