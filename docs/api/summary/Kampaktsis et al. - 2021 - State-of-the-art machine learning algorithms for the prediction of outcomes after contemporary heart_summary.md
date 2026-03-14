**Core Objective:** Develop and validate machine‑learning models to predict 1‑year mortality (and secondary outcomes) in adult heart transplant recipients using only pre‑transplant variables.

**Patient Cohort & Study Scope:** 18 625 adult heart transplant patients (mean age 53 ± 13 years, 73% male) from the UNOS database transplanted between 2010 and 2018. Cohort split 3:1 into derivation (n = 13 969) and validation (n = 4 656).

**AI/ML Approach:** Five supervised algorithms—Adaboost, Support Vector Machine (SVM), Decision Tree, Logistic Regression, and K‑Nearest Neighbor—trained on 39 selected pre‑transplant features (out of 134) using MATLAB. Feature selection employed the SVM‑FuzCoC method; categorical data were numerically encoded.

**Key Findings:**  
- Best 1‑year mortality model: Adaboost, AUC 0.689 (95% CI 0.665–0.715), Sensitivity 63.0%, Specificity 68.5%, PPV 21.6%, NPV 93.6%.  
- Other models: SVM AUC 0.637, Decision Tree AUC 0.649, Logistic Regression AUC 0.642, KNN AUC 0.526.  
- IMPACT score benchmark: AUC 0.569.  
- Secondary outcomes: 3‑year survival (AUC 0.605, 31 features), 5‑year survival (AUC 0.628, 91 features), acute rejection (AUC 0.629).  
- LIME analysis identified recipient serum creatinine, height, and ischemic time as top predictors.

**Main Limitations:** Retrospective single‑center (UNOS) dataset with no external validation and reliance solely on pre‑transplant variables.