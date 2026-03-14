**Core Objective:** Develop a machine‑learning model to predict 5‑year all‑cause mortality and graft failure (GF) in adult orthotopic heart transplant (OHT) recipients.

**Patient Cohort & Study Scope:** 15,236 adult OHT patients (age ≥ 18) from the ISHLT registry; transplants performed between 2005‑2009; median follow‑up 5 years. No lung transplants included.

**AI/ML Approach:** Gradient‑boosted machine (GBM) algorithm implemented in R (caret & gbm packages). Input: 342 extracted variables reduced to 87 after missingness/variance filtering; data split 80 % training / 20 % validation; ten‑fold cross‑validation repeated 5× for hyperparameter tuning.

**Key Findings:**  
- AUC for 5‑year mortality prediction: **0.717 (95 % CI 0.696–0.737)**.  
- AUC for 5‑year graft failure prediction: **0.716 (95 % CI 0.696–0.736)**.  
- Top relative influence variables (both outcomes): hospital length of stay, recipient age, ischemic time, donor age, donor/recipient BMI, immunosuppressive regimen at discharge, graft function at discharge, pre‑transplant bilirubin and creatinine.  
- No other performance metrics (accuracy, sensitivity, specificity) were reported.

**Main Limitations:** Retrospective registry‑based single‑era (2005‑2009) design with potential missing data and lack of external validation.