**Core Objective:** To evaluate how maintenance immunosuppressive regimens influence the risk of post‑transplant malignancy across adult solid organ transplant (SOT) recipients using machine‑learning–derived variable importance and time‑dependent Cox modeling.

**Patient Cohort & Study Scope:** 5,591 adult SOT patients (median age 54 years, range 18‑91) receiving 6,142 transplanted organs (kidney 2,986; liver 1,298; lung 1,024; heart 723; pancreas 106; intestine 5) from 2000 to March 2021 across three Chicago‑area academic centers.

**AI/ML Approach:** Random forest classifier (bootstrapped 10×, stratified by malignancy outcome; hyperparameter search via Latin hypercube, Gini impurity for variable importance). Input features: one‑hot encoded immunosuppressive agents (induction + maintenance), demographic variables, organ type; numeric features normalized. No performance metrics (e.g., AUC, accuracy) reported.

**Key Findings:**  
- Variable importance: age at transplant (most predictive), total number of immunosuppressive agents, and specific drugs (sirolimus > azathioprine > tacrolimus).  
- Time‑dependent multivariate Cox HRs (reference = no exposure): sirolimus HR 1.41 (95% CI 1.05‑1.90, p = 0.04); azathioprine HR 2.10 (1.58‑2.79, p < 0.001); cyclosporine HR 1.59 (1.17‑2.17, p = 0.007); tacrolimus HR 0.59 (0.44‑0.81, p < 0.001).  
- Overall malignancy incidence: 517 events (8.25%); skin cancer most common (52.8%). Heart and lung recipients showed highest crude malignancy rates, but organ type lost significance after adjusting for immunosuppression (heart HR 0.96, lung HR 1.01).

**Main Limitations:** Retrospective single‑region design with reliance on ICD coding and no external validation of the random forest model.