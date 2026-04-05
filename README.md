# EEG Emotion Recognition (SEED-IV)

## Overview

This project implements an EEG-based emotion recognition pipeline using the SEED-IV dataset. It processes raw EEG signals, extracts features, applies feature selection, and classifies emotions into four categories: Neutral, Sad, Fear, and Happy.

---

## Dataset

Download the dataset from:
https://www.kaggle.com/datasets/phhasian0710/seed-iv

---

## Requirements

Install the required dependencies:

```bash
pip install kaggle numpy scipy matplotlib seaborn scikit-learn
```

---

## Setup

### Kaggle API

1. Go to Kaggle → Settings → Create API Token
2. Download `kaggle.json`
3. Place it in your working directory or upload it to your environment

---

## Usage

1. Open the notebook:

```
SEED_IV_Implementation.ipynb
```

2. Set the dataset path:

```python
DATASET_PATH = '/path/to/SEED_IV/eeg_raw_data'
```

3. Run all cells in order

---

## Pipeline

* Preprocessing

  * Downsampling (1000 Hz → 200 Hz)
  * Bandpass filtering (1–75 Hz)

* Epoching

  * Non-overlapping segments
  * Fixed number of epochs per trial

* Feature Extraction

  * 14 features per channel (time and frequency domain)

* Feature Selection

  * Attention-based feature selection (AAFST)

* Classification

  * Support Vector Machine (SVM)

---

## Output

* Accuracy score
* Confusion matrix

---

## Notes

* Initial run may take time due to dataset processing
* Processed data can be saved as `.npy` files for faster reuse

---
