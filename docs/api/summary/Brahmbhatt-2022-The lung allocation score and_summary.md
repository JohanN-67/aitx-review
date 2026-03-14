**Core Objective:**  
To evaluate whether machine‑learning models using pre‑transplant recipient data can improve prediction of 1‑year (and 3‑year) post‑lung transplant mortality compared with the Lung Allocation Score (LAS) and a previously published risk model.

**Patient Cohort & Study Scope:**  
19,900 adult lung transplant recipients (≥18 y) from the UNOS/OPTN registry, transplanted between 1 May 2005 and 1 May 2017 (follow‑up through June 2020). Mean age ≈55–56 y. All received lung transplants (single or bilateral).

**AI/ML Approach:**  
- **Clinician model:** Logistic regression with 27 a‑priori selected recipient covariates.  
- **LASSO:** Penalized logistic regression selecting variables from the full UNOS set.  
- **Random Forests:** Ensemble tree model using the same covariates.  
Input data were exclusively tabular pre‑transplant recipient variables (demographics, pulmonary function, labs, functional status, etc.); donor covariates were added in secondary analyses.

**Key Findings:**  
- AUC for all models was low: **0.55–0.62** (LAS = 0.55, clinician ≈ 0.60, Random Forests ≈ 0.62, LASSO ≈ 0.58).  
- Negative predictive value (NPV) ranged **0.87–0.90**; positive predictive value (PPV) was **< 0.25** for every model.  
- Calibration showed LAS consistently over‑estimated mortality, especially in higher deciles; LASSO calibration slope = 1.45 (poor), clinician = 0.85, Random Forests = 0.96 (reasonable).  
- Adding donor covariates, disease‑specific modeling, or extending to 3‑year outcomes did **not** improve AUC (all decreased for 3‑year prediction).  
- The Chan et al. model reproduced in this cohort yielded AUC **0.59**, far below the original report (0.74/0.67).

**Main Limitations:**  
Retrospective single‑registry design limited to available UNOS variables, with potential unmeasured factors affecting post‑transplant survival.