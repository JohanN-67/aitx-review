**Core Objective:** Develop a two‑stage machine learning framework that predicts individualized heart transplant survival probabilities over multiple post‑transplant time points while enforcing monotonic decreasing curves.

**Patient Cohort & Study Scope:** 103,570 heart transplant events from the UNOS registry (1987‑2016); adult recipients; median age not reported (age range not provided).

**AI/ML Approach:** Stage 1 – evaluated seven classifiers (Logistic Regression, LDA, ANN, CART, Random Forest, XGBoost, SVM) on pre‑operative variables (≈90–269 features after cleaning). Best configuration: Logistic Regression with median numeric imputation, “unknown” categorical imputation, one‑hot encoding, LASSO feature selection, and up‑sampling of the minority class. Stage 2 – isotonic regression (pool adjacent violators algorithm) to enforce monotonicity of the predicted survival probabilities across 11 time points (1 month, years 1‑10).

**Key Findings:**  
- Logistic Regression achieved hold‑out AUCs ranging from 0.581 (year 1) to 0.703 (year 10); 10‑year AUC = 0.702, surpassing prior state‑of‑the‑art (e.g., 0.631 reported by Yoon et al.).  
- Corresponding accuracies increased from 0.537 (year 1) to 0.634 (year 10); sensitivities rose from 0.522 to 0.752, specificities declined from 0.590 to 0.533.  
- G‑Mean improved from 0.555 (year 1) to 0.633 (year 10).  
- Isotonic regression yielded ΔAUC improvements up to +0.029 (year 3) and modest gains in G‑Mean (+0.019 year 3), while guaranteeing monotonic decreasing survival curves for each patient.

**Main Limitations:** Retrospective single‑registry analysis with no external validation and limited hyperparameter optimization.