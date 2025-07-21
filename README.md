
# AF Diagnosis Using Physiological Signals by Applying Deep Learning Algorithms

**Student Name**: Rukaiya Rafique  
**Student Number**: 20110592  
**Supervisor**: Ruth Barry  
**MSc in Computer Science (Enterprise Software Systems)**  
**South East Technological University, Ireland**

---

## Description

**Experimental Data Source**: [MIMIC-PERFORM-AF Dataset](https://ppg-beats.readthedocs.io/en/latest/datasets/mimic_perform_af/)

This repository contains the codebase for the MSc thesis project focused on diagnosing Atrial Fibrillation (AF) using physiological signals and deep learning algorithms. The signals used are:

- Electrocardiogram (ECG)
- Photoplethysmogram (PPG)
- Respiratory signals

Three individual deep learning models were developed, one for each signal. The project evaluates and compares the performance of:

1. **Individual models** (trained separately on ECG, PPG, and respiratory data)
2. **Early fusion** (combining all signals before model training)
3. **Late fusion** (combining the outputs of the individual models for final classification)

Performance in AF detection is compared across these approaches.

---

## Setup

Install required dependencies:

```bash
pip install -r requirements.txt
```

---

## Scripts

### `experimental-data-preparation.ipynb`

Prepares data for model training and testing for all experiments.

---

### `experiment-one-signal.ipynb`

Used to train and test individual models using a single type of physiological signal.

Before each run, update the following variables:

```python
data_name = "resp"  # Options: "ECG", "PPG", "resp"
dataset_number = 5  # Range: 0 to 5
```

---

### `experiment-more-signals.ipynb`

Used for early fusion experiments, where multiple signals are combined before training.

Update the following lines before each run:

```python
data_name = "ECG_PPG"  # Options: "ECG_PPG", "ECG_resp", "PPG_resp", "all"
dataset_number = 5     # Range: 0 to 5
```

---

### `experiment-late-fusion.ipynb`

Implements late fusion, where final predictions are made based on the outputs of the three individual models.

---

### Plotting Scripts

These notebooks generate performance visualizations:

- `plot-accuracy.ipynb`: For individual signal models
- `plot-accuracy-early-fusion.ipynb`: For early fusion results
- `plot-accuracy-late-fusion.ipynb`: For late fusion results


---

**Note**: The empty folders will have files once the scripts are executed.
