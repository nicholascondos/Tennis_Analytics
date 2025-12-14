# Project Notes – Tennis Analytics Final Project

## Purpose of This Folder
This folder contains brief documentation notes describing key analytical decisions, modeling iterations, and project organization choices made throughout the semester. These notes support transparency and reproducibility but are not intended as a formal report.

---

## Data Preparation Notes
- ATP match data was sourced from the Jeff Sackmann ATP database covering seasons 2008–2024.
- Only completed singles matches were retained; doubles, qualifying rounds, and incomplete matches (walkovers or retirements) were excluded.
- Surface labels were standardized to ensure consistency across seasons.
- A unique match identifier was created using tournament ID and match number.
- A cleaned dataset and accompanying data dictionary were produced and stored in the `/data` folder.

---

## Feature Engineering Decisions
- Serve–return efficiency was calculated as total service points won divided by total service points played.
- Return performance was captured using first-serve return percentage rather than raw return points to normalize across match lengths.
- Break-point save percentage was included to capture performance under pressure.
- Surface interaction terms were added to test whether efficiency effects varied by court type.

---

## Modeling Notes
- Logistic regression was chosen to maintain interpretability and align with the project’s emphasis on explainability.
- Models were built incrementally:
  - Model 1: Serve–return efficiency only
  - Model 2: Efficiency plus return quality and first-serve points won
  - Model 3: Added break-point performance and surface interaction terms
- Player-level modeling was used, with one row per player-match observation.
- Train/test splits were stratified to preserve winner/loser balance.

---

## Validation and Interpretation
- Model performance was evaluated using accuracy, confusion matrices, and classification reports.
- Coefficients were examined to assess relative predictor influence rather than focusing solely on prediction accuracy.
- Surface-specific interaction terms showed consistent positive effects across court types.

---

## Repository Organization Notes
- `/data` contains merged and cleaned datasets along with the data dictionary.
- `/notebooks` contains the final, fully reproducible Colab notebook.
- `/figures` stores exploratory and model-related visualizations.
- `/reports` includes all checkpoint memos (CP1–CP8).
- The README serves as the primary entry point for navigating the project.

---

## Final Remarks
These notes summarize the key decisions made during development of the Tennis Analytics project. The goal was to prioritize clarity, reproducibility, and interpretability while building a professional-quality analytics portfolio.
