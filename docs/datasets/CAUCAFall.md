# CAUCAFall

## Overview
- **Source:** [Mendeley Data — 7w7fccy7ky/4](https://data.mendeley.com/datasets/7w7fccy7ky/4)
- **License:** CC-BY 4.0
- **Primary Use Case:** Primary target events (Thuds, Falls, Impacts)
- **Dataset Size:** ~6 GB (100+ files)

## Raw Format Structure
```text
CAUCAFall/
├── Dataset details.xlsx
└── Subject_01/ ... Subject_10/
    └── Activity_01/ ... Activity_10/
        ├── video.avi
        ├── frame_0001.png ...
        └── label_0001.txt ...
```

## Quantitative Audio/Video Metrics
*(Populate this section using findings from `03_dataset_profiling.ipynb`)*
- **Total Duration:** 
- **Number of Expected Files:** 100 AVI files (to extract audio from)
- **Sample Rate Distribution:** 
- **Bit Depth:** 
- **Channels (Mono/Stereo):** 
- **Clip Length Distribution:** 

## Label/Class Distribution
- **Annotation Format:** `.txt` segmentation labels and folder structures.
- **Included Classes:**
  - Forward fall
  - Backward fall
  - Lateral fall
  - ADL (Activities of Daily Living)
- **Class Balance:** Balanced across 10 activities for 10 subjects.

## Data Quality & Known Pitfalls
- **Video First:** This is primarily a video dataset. Action is needed to confirm the presence and quality of the audio track in the `video.avi` files.
- Audio synchronization and recording quality may vary. Needs verification if thuds are loud enough to be isolated.

## Standard Preprocessing Requirements
**To standardize this dataset for training, we will need to:**
- [ ] **Crucial:** Extract audio track from `.avi` files (e.g., via `ffmpeg`).
- [ ] Resample to `[Target Sample Rate]`
- [ ] Convert stereo to mono (if applicable)
- [ ] Isolate "thud" sound events using the segmentation labels.
