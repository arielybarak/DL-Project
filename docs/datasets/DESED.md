# DESED (Domestic Environment Sound Event Detection)

## Overview
- **Source:** [Zenodo — record 4560938](https://zenodo.org/records/4560938)
- **License:** CC-BY 4.0
- **Primary Use Case:** Background noise, generic domestic sounds (water, vacuum, dishes, etc.)
- **Dataset Size:** ~10.1 GB (50+ files after extraction)

## Raw Format Structure
```text
DESED/
├── soundbank_validation.tsv
├── audio/           (thousands of WAV files from soundbank + eval archives)
├── jams/            (JAMS annotation files)
└── ...
```

## Quantitative Audio/Video Metrics
*(Populate this section using findings from `03_dataset_profiling.ipynb`)*
- **Total Duration:** 
- **Number of Expected Files:** ~ Thousands of clips (to be analyzed)
- **Sample Rate Distribution:** 
- **Bit Depth:** 
- **Channels (Mono/Stereo):** 
- **Clip Length Distribution:** 

## Label/Class Distribution
- **Annotation Format:** Weak labels in TSV and strong labels (onset/offset) in JAMS files.
- **Included Classes:**
  - Alarm/bell/ringing
  - Blender
  - Cat
  - Dog
  - Dishes
  - Electric shaver/toothbrush
  - Frying
  - Running water
  - Speech
  - Vacuum cleaner
- **Class Balance:** TBD from profiling

## Data Quality & Known Pitfalls
- *Includes synthetic soundscapes and heavily augmented/mixed audio.*
- *Check for overlap in classes and background noise blending.*

## Standard Preprocessing Requirements
**To standardize this dataset for training, we will need to:**
- [ ] Resample to `[Target Sample Rate]`
- [ ] Convert stereo to mono (if applicable)
- [ ] Pad or truncate files to `[Target Length]`
- [ ] Map original labels to our canonical training labels
