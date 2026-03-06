# Human Screaming Detection

## Overview
- **Source:** [Kaggle](https://www.kaggle.com/datasets/whats2000/human-screaming-detection-dataset)
- **License:** Refer to Kaggle source
- **Primary Use Case:** Secondary target event (Vocal distress / screams during a fall)
- **Dataset Size:** ~5.68 GB (3,493 files)

## Raw Format Structure
```text
Human_Screaming/
├── Screaming/
├── Non_Screaming/
```

## Quantitative Audio/Video Metrics
*(Populate this section using findings from `03_dataset_profiling.ipynb`)*
- **Total Duration:** 
- **Number of Expected Files:** ~3,493
- **Sample Rate Distribution:** 
- **Bit Depth:** 
- **Channels (Mono/Stereo):** 
- **Clip Length Distribution:** 

## Label/Class Distribution
- **Annotation Format:** Directory-based labeling (Binary: Screaming vs Non-Screaming)
- **Included Classes:**
  - Screaming
  - Non-Screaming (background / talking / noise)
- **Class Balance:** Needs to be checked during profiling.

## Data Quality & Known Pitfalls
- Kaggle datasets often aggregate from YouTube or other unverified sources. Audio quality may vary vastly (clipping, compression artifacts).
- Non-screaming class might overlap with other background classes we have.

## Standard Preprocessing Requirements
**To standardize this dataset for training, we will need to:**
- [ ] Resample to `[Target Sample Rate]`
- [ ] Convert stereo to mono (if applicable)
- [ ] Pad or truncate files to `[Target Length]`
- [ ] Relabel properly to merge with our main dataset pipeline.
