<p align="center">
  <img src="outputs/banner.png" width="100%">
</p>

# Predicting Aviation Risk: Explainable Injury and Damage Classification

This project leverages machine learning and deep learning models to classify **aircraft accident severity** based on injury and damage outcomes. Using integrated datasets from NTSB, FAA, and NTAD, we engineered a robust, explainable prediction pipeline centered around **Bayesian Neural Networks (BNNs)** and **ensemble models**.

---

## Project Goals

- By the project completion, how accurately (measured by precision, recall, and F1-score) can machine learning models trained on NTSB aviation data (2008–present) predict:
  - (a) injury severity levels, and
  - (b) aircraft damage severity

- Which predictive factors in the NTSB dataset significantly impact the prediction of injury or damage levels, as identified quantitatively via **LIME/SHAP**?

- How consistent is the performance (via accuracy and confidence intervals) of the best-performing models (macro F1-score) across data stratifications like aircraft types, time periods, and weather?

---

## Project Team

**DATA 606 – Capstone in Data Science**  
Instructor: Prof. Masoud Soroush

- Scott Daniel Ellis  
- Dedeepya Palakurthi  
- Shanmukha Surya Sriteja Doddipatla  

---

## Dataset Overview

We integrated multiple sources:

- **NTSB Accident Data:** Event-level records (time, location, weather, conditions)
- **FAA Aircraft & Crew:** Type, build, age, and crew certifications
- **NTAD Facility Data:** Runway and airport metadata
- **Environmental & Findings Logs**
- **Custom Encodings:** Label mappings and category handling

See [`data/README.md`](data/README.md) and [`sample_data/README.md`](sample_data/README.md) for more.

---

## Feature Engineering

- Encoded multi-category features: `light_cond`, `sky_cond`, `med_certf`
- Combined metadata from aircraft, crew, airport, runway, findings, and environment
- Labeled target variables: `Damage` and `ev_highest_injury`

---

## Modeling Pipeline

### Deep Learning Models
- **DropoutBNN** → selected for Damage
- **AttentionBNN** → selected for Injury


### Explainability
- **LIME** for local instance explanations

---

## BNN Exploration and Tuning

We experimented with:

- **Activation Functions**: ReLU, Leaky ReLU, ELU, Sigmoid, SiLU
- **Learning Rates**: 1, 0.1, 0.01, 0.001, 0.0001
- **Hidden Dimensions**: 10, 50, 100, 500
- **Epochs**: 1000

Evaluation focused on F1 score, confidence calibration, and interpretability.

---

## Final Model Performance

| Target     | Final Model     | Macro F1 Score | Confidence |
|------------|------------------|----------------|------------|
| `Damage`   | DropoutBNN (ELU) | Highest        | Stable     |
| `Injury`   | AttentionBNN     | Highest        | Best       |

---

##  How to Run

1. Clone the repository  
2. Install dependencies:
   ```bash
   pip install -r requirements.yaml
   ```
3. Run:
   - `notebooks/Data_Preparation.ipynb`
   - `notebooks/Modeling-4.ipynb`

Use `sample_data/` for testing.

---

## Project Structure

```
data/             ← Full datasets (excluded from GitHub)
sample_data/      ← Public samples for testing
notebooks/        ← EDA, preprocessing, modeling
models/           ← Trained model weights (.pt)
resources/        ← Presentations and reference docs
outputs/          ← Visual outputs: SHAP, F1 trends, etc.
README.md         ← This file
```

---

## Acknowledgments

- NTSB: https://www.ntsb.gov/  
- FAA & DOT: https://catalog.data.gov/  
- NTAD Facilities: https://data-usdot.opendata.arcgis.com/
