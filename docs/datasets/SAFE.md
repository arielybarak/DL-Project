# SAFE (Sound Analysis for Fall Events)

## Overview
- **Source:** [Kaggle](https://www.kaggle.com/datasets/antonygarciag/fall-audio-detection-dataset)
- **License:** Refer to Kaggle source
- **Primary Use Case:** Additional fall simulations; increasing "Thud" variety
- **Dataset Size:** ~273 MB (950 files)

## Raw Format Structure
```text
SAFE/
├── ADL/
└── Falls/
```

## Quantitative Audio/Video Metrics
*(Populate this section using findings from `03_dataset_profiling.ipynb`)*
- **Total Duration:** 
- **Number of Expected Files:** 950
- **Sample Rate Distribution:** 
- **Bit Depth:** 
- **Channels (Mono/Stereo):** 
- **Clip Length Distribution:** 

## Label/Class Distribution
- **Annotation Format:** Directory-based labeling (Falls vs. ADL)
- **Included Classes:**
  - Falls
  - ADL (Activities of Daily Living - e.g., walking, dropping objects)
- **Class Balance:** To be checked.

## Data Quality & Known Pitfalls
- Small physical size. Good for fine-tuning.
- Needs analysis of whether simulated falls sound natural or staged.
- The "ADL" class might contain sounds we consider positive/ambiguous, requiring manual review.

## Standard Preprocessing Requirements
**To standardize this dataset for training, we will need to:**
- [ ] Resample to `[Target Sample Rate]`
- [ ] Convert stereo to mono (if applicable)
- [ ] Pad or truncate files to `[Target Length]`
