# Data Directory

This directory stores all datasets used in the project.

## Structure
- **`raw/`** — The original, immutable data dump (stored on Google Drive, not in Git).
- **`processed/`** — The final, canonical data sets for modeling.
- **`DATASET_MANIFEST.md`** — Source-verified specifications for every dataset:
  file counts, sizes, MD5 checksums, directory structures, and licenses.

> **Note:** Actual data files are ignored by Git to prevent bloating the repository.
> Data lives on Google Drive at `MyDrive/DL-Project/raw/`.

## Datasets (quick reference)

| # | Dataset | Source | Files | Size | Format |
|---|---------|--------|-------|------|--------|
| 1 | DESED | Zenodo | 50+ | ≥5 GB | WAV, JAMS |
| 2 | CAUCAFall | Mendeley | 100+ | ≥6 GB | AVI, PNG, TXT |
| 3 | WaterLeakage | GitHub | 30+ | ≥5 MB | WAV |
| 4 | HumanScreaming | Kaggle | 3,493 | 5.68 GB | WAV |
| 5 | FSD50K | Zenodo | 51,197 | ≥20 GB | WAV |
| 6 | SAFE | Kaggle | 950 | 273 MB | WAV |
| 7 | AudioSet | YouTube/yt-dlp | 10+ (variable) | Variable | WAV |

See [`DATASET_MANIFEST.md`](DATASET_MANIFEST.md) for full details.

## Verification

Run `notebooks/02_data_verify.ipynb` in Colab to check all downloads against
the source-verified thresholds above, including MD5 checksums for Zenodo archives.
