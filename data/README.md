# Local Data Directory – Full Datasets (Not Tracked in GitHub)

This directory stores the **complete datasets** used throughout the project for data preparation, feature engineering, and model training.

## Important

This folder is **excluded from version control** using `.gitignore` and **does not appear in the GitHub repository**.

---

## Contents

Typical contents of this directory include:

| File Name                        | Description |
|----------------------------------|-------------|
| `aviation_df.csv`               | Final cleaned and merged dataset used for modeling |
| `aircraft.csv`                  | Aircraft details (e.g., type, engine, seat capacity) |
| `airports.csv`                  | Airport attributes (elevation, location, etc.) |
| `events.csv`                    | Event-level metadata (date, time, location, light condition) |
| `Findings.csv`                  | Findings from incident investigations |
| `Flight_Crew.csv`               | Crew member details including age and certifications |
| `flight_time.csv`               | Flight duration and departure/arrival times |
| `NTAD_Aviation_Facilities.csv` | Runway and infrastructure attributes from NTAD |
| `encodings.csv`                | Manual mappings for categorical feature encoding |

---

## Data Sources

- **NTSB Aviation Accident Database:** https://www.ntsb.gov/
- **FAA & DOT Data Catalog:** https://catalog.data.gov/
- **NTAD Aviation Facilities:** https://data-usdot.opendata.arcgis.com/

---

## Reproduction Instructions

To recreate the contents of this folder:

1. Download the raw datasets from the above sources.
2. Run the data pipeline in `notebooks/Data_Preparation.ipynb` to preprocess and merge files.
3. Output files will be stored in `data/` for modeling.

---

## Note on Exclusion from Version Control

This folder is intended for local use only and is **not included in the GitHub repository** for the following reasons:

- File size
- Data sensitivity and license restrictions
- Maintain a clean, focused, and lightweight codebase
