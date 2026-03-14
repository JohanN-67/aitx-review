**Core Objective:**  
To develop and validate a machine‑learning model that predicts 1‑year mortality in adult lung transplant recipients using pre‑transplant variables.

**Patient Cohort & Study Scope:**  
- Total patients: 29,364 lung transplant recipients from the ISHLT registry.  
- Age: mean 53.4 ± 13.4 years (range not specified).  
- Organ: lung only.  
- Study period: June 2009 – June 2018 (registry data) with external validation on 216 patients transplanted Jan 2012 – Mar 2024 at a single Korean center.

**AI/ML Approach:**  
- Algorithms evaluated: Logistic Regression, Support Vector Machine, Random Forest, Gradient Boosting Machine (GBM), Balanced Random Forest, Multilayer Perceptron (MLP).  
- Input data: 25 pre‑transplant clinical variables (tabular EMR); a reduced model used the top 10 features identified by SHAP (e.g., albumin, mean pulmonary artery pressure, creatinine).

**Key Findings:**  
- GBM achieved the highest internal performance with AUC 0.958 ± 0.002 and accuracy 0.949 ± 0.002 (both with 25 and with 10 features).  
- MLP showed the best external generalization: AUC 0.911, accuracy 0.870 on the in‑house dataset (10 features).  
- GBM external validation: AUC 0.852, accuracy 0.764.  
- Sensitivity/specificity for GBM (10‑feature model) were 0.755 and 0.986 respectively; for MLP external: sensitivity 0.886, specificity 0.863.

**Main Limitations:**  
Retrospective registry‑based design with potential data completeness issues and lack of prospective multi‑center external validation.