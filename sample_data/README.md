# ✈Sample Data – Public Version of Project Datasets

This folder contains **anonymized, small-scale samples** of the datasets used in this project. These are intended for:

- Public reproducibility
- Testing notebooks
- Understanding data structure
- Demonstrating preprocessing steps

---

## Included Files

| File Name                               | Description                                       |
|----------------------------------------|---------------------------------------------------|
| `aviation_df_sample.csv`               | Sample from the final merged dataset              |
| `aircraft_sample.csv`                  | Sample aircraft records from NTSB                 |
| `airports_sample.csv`                  | Sample airport data (elevation, location, etc.)   |
| `events_sample.csv`                    | Sample event logs (times, locations)              |
| `encodings_sample.csv`                 | Categorical encoding mappings                     |
| `NTAD_Aviation_Facilities_sample.csv`  | Sample runway and facility records                |

Each file contains ≤10 rows while retaining full column structure and types.

---

## Notes

- These files are **manually created samples** from the full dataset for safe and responsible public release.
- Full datasets are located in the `data/` folder and excluded from GitHub.

---

## Usage

These files are sufficient for:
- Running pipeline tests
- Previewing preprocessing logic
- Understanding model input structure

For full experiments, run the data preparation notebook with actual datasets stored locally.
