# AudioSet

## Overview
- **Source:** [Google AudioSet index](https://research.google.com/audioset/ontology/index.html)
- **License:** CC-BY 4.0 (for annotations); Audio is YouTube standard license
- **Primary Use Case:** Supplemental extraction if other datasets lack specific variety (e.g., specific shower loops).
- **Dataset Size:** Variable (Extracting specific segments based on needs)

## Raw Format Structure
```text
AudioSet_extracted/
├── shower/
├── thud/
└── ...
```

## Quantitative Audio/Video Metrics
*(Populate this section using findings from `03_dataset_profiling.ipynb`)*
- **Total Duration:** 
- **Number of Expected Files:** 
- **Sample Rate Distribution:** 
- **Bit Depth:** 
- **Channels (Mono/Stereo):** 
- **Clip Length Distribution:** Usually 10 seconds.

## Label/Class Distribution
- **Annotation Format:** Onset/Offset CSVs referencing YouTube IDs.
- **Included Classes:**
  - Water/Shower
  - Splashing
  - Screaming
  - Thuds/Impacts
- **Class Balance:** Very unbalanced, depends entirely on what we download.

## Data Quality & Known Pitfalls
- **Dead links:** Many YouTube videos might be deleted or made private. We only get a fraction of the index.
- Heavy compression artifacts from YouTube.
- Can have background music or overlapping classes not marked in annotations.

## Standard Preprocessing Requirements
**To standardize this dataset for training, we will need to:**
- [ ] Run scripts (e.g., `yt-dlp`) to fetch the exact 10s intervals.
- [ ] Resample to `[Target Sample Rate]`
- [ ] Convert stereo to mono (if applicable)
- [ ] Pad or truncate if downloaded segments slightly differ from 10s.
