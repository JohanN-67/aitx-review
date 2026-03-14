**Core Objective:** Develop and validate a machine‑learning model to predict airway stenosis (AS) requiring clinical intervention in lung transplant recipients.

**Patient Cohort & Study Scope:** 381 adult lung transplantation patients (median age 57 years, range 19–82) from January 2017 to December 2019; 40 (10.5%) developed AS. Single‑ and double‑lung transplants were included (52.8% SLTx, 47.2% DLTx).

**AI/ML Approach:** Eight algorithms (LR, DT, KNN, NB, SVM, GBRM, RF, XGB) combined with seven feature‑selection methods (including determination coefficient). The optimal model used a **Random Forest** algorithm with the **determination‑coefficient (DC)** feature selection, based on clinical tabular data (demographics, perioperative variables, postoperative 6‑minute walk test, etc.).

**Key Findings:**  
- Optimal RF model AUC = 0.760 (95% CI 0.666–0.864), Brier score = 0.085 (95% CI 0.058–0.117).  
- Conventional logistic regression AUC = 0.689 (95% CI 0.545–0.803), Brier score = 0.091 (95% CI 0.064–0.125).  
- Sensitivity/Specificity of RF: 0.782 / 0.689; LR: 0.680 / 0.623.  
- Positive predictive value (PPV) RF = 0.252, NPV = 0.965; LR PPV = 0.236, NPV = 0.952.  
- Top predictors: postoperative 6‑minute walk test, diagnosis, sex, ECMO type, preoperative hormone use.

**Main Limitations:** Retrospective single‑center design with internal bootstrap validation only; external validation lacking.