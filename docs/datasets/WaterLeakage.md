# Water Leakage (aliEmreOzturk)

## Overview
- **Source:** [GitHub - aliEmreOzturk/water_leakage_voice_data](https://github.com/aliEmreOzturk/water_leakage_voice_data)
- **License:** See repo
- **Primary Use Case:** Specialized bathroom/faucet/toilet sounds; background hard negatives
- **Dataset Size:** ~5 MB (30+ WAV files)

## Raw Format Structure
```text
water_leakage_voice_data/
├── README.md
├── .wav files
```

## Quantitative Audio/Video Metrics
*(Populate this section using findings from `03_dataset_profiling.ipynb`)*
- **Total Duration:** 
- **Number of Expected Files:** ~30+
- **Sample Rate Distribution:** 
- **Bit Depth:** 
- **Channels (Mono/Stereo):** 
- **Clip Length Distribution:** 

## Label/Class Distribution
- **Annotation Format:** Unspecified/Monolithic (all files roughly represent the same concept)
- **Included Classes:**
  - Water leakage / Sink / Bathroom noise
- **Class Balance:** N/A (single domain)

## Data Quality & Known Pitfalls
- Limited dataset size.
- Needs to be heavily augmented (pitch shift, add noise, variable durations) to generalize well.

## Standard Preprocessing Requirements
**To standardize this dataset for training, we will need to:**
- [ ] Resample to `[Target Sample Rate]`
- [ ] Convert stereo to mono (if applicable)
- [ ] Pad or truncate files to `[Target Length]`
- [ ] Apply augmentations due to the small size.
