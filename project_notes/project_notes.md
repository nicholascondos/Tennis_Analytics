# Project Notes – Tennis Analytics Final Project


## Repository Purpose
This repository contains the full end-to-end workflow for my DATA 6560 Sports Analytics semester project:
- Source selection and validation (Sackmann ATP match database)
- Data merging (2008–2024), filtering, and cleaning
- Feature engineering aligned to CP1–CP8 research questions
- Exploratory analysis (figures saved to /figures)
- Logistic regression modeling (Models 1–3)
- Final deliverables (CP memos, executive summary, reflection)

---

## Folder Guide
- **/data**
  - `atp_matches_2008_2024_merged.csv` (raw merged dataset, post-merge + basic completion filters)
  - `atp_matches_2008_2024_clean.csv` (cleaned dataset used for EDA + modeling)
  - `Data Dictionary Tennis Analytics.xlsx` (data dictionary for final/cleaned fields)

- **/figures**
  - Saved plots used in CP5 and referenced in later checkpoints (PNG exports)

- **/notebooks**
  - `FinalTennisAnalyticsProject.ipynb` (complete pipeline: merge → clean → EDA → modeling)

- **/reports**
  - Checkpoint memos (CP1–CP8) and final reflection/submission PDFs

- **/project_notes**
  - This file (high-level run instructions + key decisions)

---

## Key Data Decisions (Aligned to CP4)
- Time range: **2008–2024**
- Match type: **ATP singles only**
- Completed matches only (non-null score; removes walkovers/retirements when available)
- Removed **doubles**, **qualifying rounds**, and **round-robin**
- Created unique match identifier: `tourney_id + match_num`
- Standardized surface labels (and excluded “Carpet” in the surface comparison figure)

---

## How to Reproduce Results
1. Open `notebooks/FinalTennisAnalyticsProject.ipynb` in Google Colab.
2. Run cells top-to-bottom.
3. Outputs generated:
   - Merged dataset exported to `/data`
   - Clean dataset exported to `/data`
   - Figures exported to `/figures`
   - Model outputs printed in notebook (accuracy, confusion matrices, coefficients)

---

## Modeling Notes (Aligned to CP6–CP8)
- **Model 1**: Logistic regression using serve/return efficiency only.
- **Model 2**: Adds first-serve return % and first-serve points won.
- **Model 3**: Adds break-point save % and surface-adjusted efficiency interaction terms.
- A hard-court-only check is included to validate robustness on a single surface.

---

## Final Remarks
These notes summarize the key decisions made during development of the Tennis Analytics project. The goal was to prioritize clarity, reproducibility, and interpretability while building a professional-quality analytics portfolio.
