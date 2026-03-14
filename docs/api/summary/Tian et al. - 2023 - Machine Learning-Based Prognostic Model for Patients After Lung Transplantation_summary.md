**Core Objective:**  
To develop and internally validate a machine‑learning prognostic tool that predicts overall survival (OS) for adult lung transplant recipients using random survival forests (RSF).

**Patient Cohort & Study Scope:**  
- Total patients: 504 lung transplant recipients (training = 353, test = 151).  
- Mean age: 55.6 ± 12.3 years (training = 55.0 ± 12.8, test = 56.8 ± 11.0).  
- Sex: 66.3% male.  
- Organ transplanted: lung only (both single and double).  
- Study period: transplants performed Jan 2017 – Dec 2020; data analyzed Jan 2017 – Dec 2019.

**AI/ML Approach:**  
- Model: Random Survival Forests (RSF) implemented via the `randomForestSRC` R package.  
- Input modalities: 22 pre‑ and post‑transplant clinical variables (demographics, diagnosis, surgical type, ECMO use, ventilator time, ICU stay, pulmonary function tests, etc.); 16 variables with variable importance > 0.01 were retained for the final RSF model.  
- Benchmark: Cox proportional hazards regression using the same 16 variables.

**Key Findings:**  
- RSF discrimination: integrated AUC = 0.879 (95% CI 0.832‑0.921).  
- RSF calibration: integrated Brier score = 0.130 (95% CI 0.106‑0.154).  
- Cox model performance: iAUC = 0.658 (95% CI 0.572‑0.747, *P*<.001 vs RSF); iBS = 0.205 (95% CI 0.176‑0.233, *P*<.001).  
- 1‑month survival prediction (RSF): tAUC = 0.858, PE = 0.123; sensitivity = 86.1%, specificity = 68.7%, accuracy = 72.9%.  
- 1‑year survival prediction (RSF): tAUC = 0.921, PE = 0.115; sensitivity = 88.7%, specificity = 79.6%, accuracy = 82.8%.  
- Risk stratification: optimal RSF cutoff 30.74 split test set into low‑risk (median OS ≈ 52.9 mo) and high‑risk (median OS ≈ 14.8 mo, *log‑rank* P<.001).  
- Subgroup iAUCs: single LTx = 0.861, double LTx = 0.896; IPF = 0.885, COPD = 0.809.

**Main Limitations:**  
Single‑center retrospective design with only internal validation; external multicenter testing is needed.