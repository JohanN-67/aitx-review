**Core Objective:** To develop and evaluate a pre‑operative machine learning model that predicts 1‑year post‑transplant mortality in adult heart transplant recipients bridged with temporary mechanical circulatory support (tMCS).

**Patient Cohort & Study Scope:** 1,584 patients (median age 56 years, IQR 46–62; 74% male) undergoing isolated heart transplantation while on tMCS between 01/2009 and 12/2017 in the UNOS database.

**AI/ML Approach:** Extreme Gradient Boosting (XGBoost) classifier trained on 498 pre‑transplant variables; 70 %/30 % train‑test split with class‑weighting (scale_pos_weight = 7.8). Input data were tabular EMR variables; feature selection reduced to 43 predictors via gain importance. Model interpretability employed SHAP values.

**Key Findings:** The XGBoost model achieved an AUC of **0.71 (95 % CI 0.62–0.78)** for 1‑year mortality prediction; precision‑recall AUC = 0.357. Important predictors (SHAP) included recipient functional status, age, pulmonary capillary wedge pressure, cardiac output, ECMO usage, and serum creatinine. Actual 1‑year mortality in the cohort was 12.1 %.

**Main Limitations:** Retrospective single‑center design with class imbalance and lack of external validation in post‑2018 UNOS policy era.