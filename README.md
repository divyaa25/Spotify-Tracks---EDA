# 🎧 Spotify Tracks — Exploratory Data Analysis

## Overview

This project presents an exploratory data analysis (EDA) of a large Spotify tracks dataset sourced from Kaggle. The goal of the analysis is to understand how audio features, track characteristics, and basic metadata relate to track popularity on the platform.

Rather than building predictive models, this notebook focuses on:

* rigorous data cleaning and validation
* feature engineering for interpretability
* exploratory visual analysis
* uncovering structural patterns and limitations in platform-defined popularity metrics

The project was completed as an independent data analysis exercise to strengthen skills in data exploration, documentation, and analytical reasoning.

---

## Dataset

- **Source:** Kaggle – [Spotify Tracks Dataset](https://www.kaggle.com/datasets/maharshipandya/spotify-tracks-dataset)
* **Observations:** ~110k tracks (varies slightly by dataset version)
* **Key variables include:**

  * `popularity` (0–100)
  * `duration_ms`
  * Audio features such as `danceability`, `energy`, `loudness`, `speechiness`,
    `acousticness`, `instrumentalness`, `liveness`, `valence`, `tempo`
  * Metadata including `explicit`, `key`, `mode`, `time_signature` (if available)

> Note: Column names may vary slightly across Kaggle versions. The notebook includes safeguards to handle missing or renamed columns.

---

## Project Structure

```
.
├── Spotify_Tracks_EDA_Sample.ipynb
├── README.md
└── spotify_tracks.csv   # not included; download separately from Kaggle
```

---

## Analysis Highlights

### 1. Data Quality & Cleaning

* Schema inspection, missingness analysis, and duplicate checks
* Standardization of numeric fields and categorical flags
* Filtering of extreme outliers (e.g., implausible track durations or tempos)

### 2. Feature Engineering

* Conversion of duration to minutes
* Popularity tiering for segmented analysis
* Exploratory composite indices (e.g., “hype” and “chill” proxies)

### 3. Exploratory Insights

* Popularity exhibits a highly skewed, winner-take-most distribution
* Highly popular tracks tend to cluster within a narrow duration range
* Instrumental tracks are significantly less popular on average
* Emotional tone (energy × valence) shows clearer structure than individual audio features
* No single audio feature strongly explains popularity on its own

### 4. Multivariate Structure

* PCA used to visualize high-dimensional audio feature space
* KMeans clustering applied for exploratory segmentation
* Results suggest continuous “vibe” gradients rather than discrete categories

---

## Key Takeaways

* Track popularity is unevenly distributed and influenced by more than audio features alone
* Duration and emotional tone appear more informative than technical musical attributes
* Instrumental and niche tracks are structurally disadvantaged in popularity metrics
* Popularity should be treated as a platform-dependent outcome, not an intrinsic measure of quality

---

## What Can Be Done With This Data

* **Predictive modeling** of popularity tiers or relative performance
* **Content segmentation** for recommendation or playlist generation
* **Exploratory clustering** to identify latent musical “vibes”
* **Longitudinal analysis** of popularity trajectories over time
* **Ethical analysis** of how platform dynamics shape visibility and engagement

---

## How to Run

1. Download a Spotify tracks dataset from Kaggle
2. Rename the CSV to `spotify_tracks.csv`
3. Place it in the root directory
4. Open and run `Spotify_Tracks_EDA.ipynb`

---

## Tools & Libraries

* Python
* pandas, numpy
* matplotlib
* scikit-learn (PCA, KMeans)

---

## Notes & Limitations

* This is a descriptive analysis; no causal claims are made
* Popularity is influenced by non-audio factors such as promotion, artist reputation, and algorithmic exposure
* Audio feature estimates may contain noise or platform-specific artifacts

---

## License

This project is for educational and exploratory purposes. Dataset licensing is governed by the original Kaggle source.

This repo + PDF combo will look *very strong* on applications.
