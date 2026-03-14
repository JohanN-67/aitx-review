**Core Objective:** Develop an interpretable AI model to predict 1‑year mortality after heart transplantation and compare its performance with existing deep learning (IHTSA) and traditional scoring (IMPACT) models.

**Patient Cohort & Study Scope:** Total patients = 31,315 (derivation 1997‑2013) + 6,120 (test 2014‑2016) + 4,750 external validation (UNOS 2017‑2018) + 2,293 Scandinavian cohort (1997‑2018). Mean recipient age ≈ 54 years (range 18–≈80). Organ: heart only. Study period spans 1997‑2018.

**AI/ML Approach:** Partial Response Network (PRN) self‑explaining neural network derived from a multilayer perceptron, followed by Lasso regularization (PRN‑Lasso). Input: tabular EMR variables (donor/recipient demographics, labs, ischemic time, ventilator status, diagnosis, etc.). Benchmarked against IHTSA (deep ANN ensemble) and IMPACT (logistic score); also compared with Explainable Boosting Machine (EBM).

**Key Findings:**  
- PRN‑Lasso AUROC in blinded UNOS validation (n = 4,750): **0.628** (95% CI 0.602–0.654).  
- Comparable to IHTSA AUROC **0.635** (0.609–0.662) and recalibrated IHTSA **0.643** (0.617–0.669).  
- EBM AUROC **0.634** (0.607–0.660); IMPACT lower at **0.602** (0.575–0.628).  
- Calibration: PRN‑Lasso Hosmer–Lemeshow χ² = 15.01 (p = 0.135) → good fit; IHTSA and IMPACT showed poor calibration (p < 0.001).  
- PRN‑Lasso identified nine univariate predictors (recipient age, donor age, creatinine, ischemic time, ventilator at OHT, non‑ischemic cardiomyopathy, female sex, infection ≤2 weeks, transplant year) plus one interaction (recipient age × ICM).

**Main Limitations:** Retrospective registry analysis with missing data and lack of prospective external validation.