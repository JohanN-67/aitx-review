**Core Objective:** Develop and validate a machine‑learning model to predict post‑transplant mortality in adult congenital heart disease (ACHD) patients undergoing isolated heart transplantation.

**Patient Cohort & Study Scope:** 1,033 ACHD recipients (median age 34 years, IQR 23–45; 61% male) who received isolated heart transplants in the United States from 2000 to 2020 (UNOS database).  

**AI/ML Approach:** CatBoost gradient‑boosting decision‑tree model trained on 10 selected variables (eGFR, ischemic time, post‑operative hemodialysis, days in UNOS 1A status, post‑op stroke, HIV+, HCV+, age, total bilirubin, functional status). Input data were tabular clinical variables from donor, recipient, procedural and post‑transplant records; feature selection performed with SHAP.

**Key Findings:**  
- 1‑year mortality AUC 0.80 (95% CI 0.687–0.811), accuracy 75.2%, sensitivity 75%, specificity 75%, PPV 42%, NPV 93%.  
- 3‑year mortality AUC 0.69, accuracy 74.2%, sensitivity 51%, specificity 85%, PPV 63%, NPV 78%.  
- SHAP identified post‑operative hemodialysis, eGFR, age and ischemic time as the strongest predictors of 1‑year mortality.

**Main Limitations:** Retrospective single‑nation UNOS analysis lacking detailed CHD anatomy, inclusion of post‑operative complications unavailable at baseline, and no external validation.