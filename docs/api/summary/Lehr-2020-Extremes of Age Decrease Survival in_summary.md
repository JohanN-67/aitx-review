**Core Objective:** To quantify how recipient age influences long‑term survival after adult lung transplantation and to identify age‑specific risk factors using machine‑learning modeling.

**Patient Cohort & Study Scope:** 14,253 adult lung transplant recipients (age ≥ 18) from the US Scientific Registry of Transplant Recipients, transplanted between 1 Jan 2006 and 19 Feb 2015. Median age 59 y (range 18‑?); subgroups: <30 y (n=1,098; 7.7%), 30‑55 y (n=4,201; 29.5%), >55 y (n=8,954; 62.8%).

**AI/ML Approach:** Random Survival Forest (RSF) non‑parametric survival modeling with 96 donor/recipient variables (tabular EMR data). Model built with 500 trees; variable importance measured via VIMP. Bootstrap aggregation (1,000 samples) used for variable selection.

**Key Findings:**  
- Age was the most reliable predictor of death across all time points; extremes (<30 y and >55 y) had lowest survival. Predicted 5‑yr survival: 20‑y = 64.5%, 45‑y = 81.2%, 65‑y = 71.5%.  
- RSF identified top five mortality predictors (overall): extreme age, higher creatinine, single‑lung transplant, pre‑transplant hospitalization, higher bilirubin.  
- Age‑specific top predictors: <30 y – lower education, older donor age, Medicaid/Medicare, higher bilirubin, dialysis; 30‑55 y – higher creatinine, non‑CF diagnosis, BMI, recipient/donor race; >55 y – higher creatinine, bilirubin, hospitalization, donor‑recipient TLC ratio, CO₂ levels.  
- Model performance metrics (e.g., AUC/C‑statistic) were **Not explicitly reported**.

**Main Limitations:** Retrospective registry design with limited granularity and missing socioeconomic variables, and no external validation.