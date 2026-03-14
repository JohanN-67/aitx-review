**Core Objective:**  
To develop and internally validate an explainable machine‑learning model that predicts failure of UNOS Status 2 listing (death, inactivation, or upgrade) among heart transplant candidates supported with intra‑aortic balloon pump (IABP) or Impella devices.

**Patient Cohort & Study Scope:**  
4,178 adult heart transplant candidates listed as UNOS Status 2 and supported with IABP or Impella between 2018 and 2022 (mean age ≈ 53 years; BMI ≈ 27.5). All patients were from the United States (UNOS registry); no lung transplants were included.

**AI/ML Approach:**  
Extreme Gradient Boosting (XGBoost) ensemble trees applied to 19 tabular variables derived from UNOS data (demographics, labs, hemodynamics, device type, medication use, UNOS region). Two model sets: (1) a comprehensive national model and (2) separate regional models for the 10 regions with ≥150 patients.

**Key Findings:**  
- Comprehensive model AUC = 0.71 ± 0.03; region‑specific AUC ranged 0.44 ± 0.08 to 0.74 ± 0.01.  
- Overall accuracy = 0.72 ± 0.02; balanced accuracy = 0.65 ± 0.02.  
- Sensitivity low (overall 0.54 ± 0.04); specificity high (overall 0.75 ± 0.02, up to 0.96 in Region 5).  
- Top predictors (overall SHAP ranking): number of inotropes, serum creatinine, sodium, BMI, and blood group.  
- Device type ranked 15th of 19 variables, indicating lower importance than patient factors.

**Main Limitations:**  
Retrospective single‑registry design with high missingness and no external validation.