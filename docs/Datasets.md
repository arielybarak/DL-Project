# Datasets

> **Documentation Note:** For detailed quantitative metrics, expected formats, and preprocessing requirements, see the respective deep-dive pages in the [`datasets/`](datasets/) directory. The statistics are generated via the [`notebooks/03_dataset_profiling.ipynb`](../notebooks/03_dataset_profiling.ipynb) EDA.

*   **[DESED / DCASE Domestic Sounds](datasets/DESED.md)**
    *   Link: [Zenodo](https://zenodo.org/records/4560938)
    *   Info: Gold standard for domestic noise (Water/Vacuum). Includes synthetic mixtures.

*   **[CAUCAFall Dataset](datasets/CAUCAFall.md)**
    *   Link: [Mendeley](https://data.mendeley.com/datasets/7w7fccy7ky/4)
    *   Info: Best source for high-fidelity human "thuds" and impact sounds.

*   **[aliEmreOzturk Water Leakage](datasets/WaterLeakage.md)**
    *   Link: [GitHub](https://github.com/aliEmreOzturk/water_leakage_voice_data)
    *   Info: Specialized bathroom faucet/toilet sounds. High relevance for background filtering.

*   **[Human Screaming Detection](datasets/HumanScreaming.md)**
    *   Link: [Kaggle](https://www.kaggle.com/datasets/whats2000/human-screaming-detection-dataset)
    *   Info: Vital for detecting the vocal distress component of a fall.

*   **[FSD50K](datasets/FSD50K.md)**
    *   Link: [Zenodo](https://zenodo.org/records/4060432)
    *   Info: Large-scale, high-quality generic sounds. Good for "Splashing" and "Sink" variety.

*   **[SAFE (Sound Analysis for Fall Events)](datasets/SAFE.md)**
    *   Link: [Kaggle](https://www.kaggle.com/datasets/antonygarciag/fall-audio-detection-dataset)
    *   Info: Additional fall simulations; good for increasing "Thud" variety.

*   **[AudioSet (Google)](datasets/AudioSet.md)**
    *   Link: [Index](https://research.google.com/audioset/ontology/index.html)
    *   Info: Use this via extraction script only if the above sources don't provide enough "Shower" variety.



