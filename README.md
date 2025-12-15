# Tennis_Analytics
GitHub Repository - Nicholas Condos: Tennis Analytics (ATP) &amp; Performance Metrics Overview/Analyzation


**ATP Match Outcomes: Modeling Serve–Return Efficiency (2008–2024)**

---

## Project Overview
This project analyzes professional men’s tennis matches to identify which performance metrics most strongly predict match outcomes. Using ATP match data from 2008–2024, the analysis focuses on serve–return efficiency, return quality, and pressure performance to build interpretable predictive models. The goal is to understand the factors that drive winning in professional tennis rather than simply predicting match results.

---

## Problem Statement & Stakeholder
Tennis outcomes are often attributed to serving power or player rankings, but these explanations overlook the importance of return quality and point-level efficiency. This project examines which match statistics best explain a player’s probability of winning.

**Primary stakeholders include:**
- Tennis coaches and performance analysts  
- Player development and performance staff  
- Sports analytics teams  
- Analysts interested in interpretable sports models  

---

## Dataset Overview
- **Source:** Jeff Sackmann ATP match database  
- **Time span:** 2008–2024  
- **Match type:** Completed ATP singles matches only  
- **Row definition:** One row per match in the cleaned dataset; expanded to one row per player-match for modeling  

**Key filters applied:**
- Removed doubles and qualifying rounds  
- Excluded incomplete matches (walkovers, retirements)  
- Standardized surface labels  

---

## Methodology & Analytical Approach
The project was developed iteratively across multiple checkpoints:

1. **Data Preparation (CP4)**  
   - Merged 17 seasons of ATP data  
   - Engineered serve–return efficiency metrics  
   - Created a clean, reproducible dataset  

2. **Exploratory Data Analysis (CP5)**  
   - Compared winners and losers across serve, return, and pressure metrics  
   - Identified efficiency and return quality as key differentiators  

3. **Modeling (CP6–CP7)**  
   - Built logistic regression models at the player-match level  
   - Incrementally added predictors including serve–return efficiency, return quality, pressure metrics, and surface interactions  

4. **Executive Summary (CP8)**  
   - Presented a single interpretable model with clear, actionable takeaways  

---

## Key Results
- Serve–return efficiency is the strongest predictor of match outcomes  
- First-serve return percentage provides significant explanatory power beyond serving metrics  
- Break-point performance improves prediction in high-pressure situations  
- The final model achieved **0.882 accuracy** while remaining interpretable
- ### Final Model (Model 3 – Logistic Regression)

- Accuracy: approximately **0.88**
- Balanced precision and recall across winners and losers
- Model remains fully interpretable via coefficients

![Model 3 Coefficients – Logistic Regression](figures/BarChartModel3.png)

**One-line takeaway:** Serve–return efficiency and first-serve return percentage are the strongest predictors of match outcomes, with break-point save percentage providing additional explanatory power.

---

## How to Reproduce This Project
1. Open `/notebooks/FinalTennisAnalyticsProject.ipynb`  
2. Run the notebook from top to bottom  
3. The notebook performs data cleaning, exploratory analysis, model fitting, and evaluation  

All required datasets are stored locally in the `/data` folder.

---

## Repository Structure
Tennis_Analytics/
├── data/
├── figures/
├── notebooks/
├── project_notes/
├── reports/
└── README.md

---

## Limitations & Future Work
- The analysis does not include rally-level or tracking data  
- Contextual factors such as fatigue and injury are not captured  
- Future work could explore nonlinear models or incorporate point-by-point data  

---

## Author & Acknowledgments
**Author:** Nicholas Condos  
**Course:** DATA 6560 – Sports Analytics  
**Data Source:** Jeff Sackmann ATP Tennis Database  
**Tools:** Python, pandas, NumPy, seaborn, scikit-learn
