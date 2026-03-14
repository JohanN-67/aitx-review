**Core Objective:** To benchmark contemporary survival machine‑learning methods for predicting one‑year all‑cause mortality in adult heart transplant recipients after the 2018 UNOS allocation policy change.

**Patient Cohort & Study Scope:** 7,160 adult heart‑only transplant recipients (age mean 53.5 ± 12.9 years, range 18–76) transplanted between 18 Oct 2018 and 3 Jun 2021 (post‑policy cohort). A seasonally matched pre‑policy cohort (Nov 2014–Oct 2018) was also analyzed.

**AI/ML Approach:** Seven survival models were evaluated on tabular pre‑transplant variables (75 raw features → 114 one‑hot encoded): Lasso Cox, Ridge Cox, Elastic Net Cox, Cox Gradient Boost (Cox Boost), Extreme Gradient Boosting Linear (XGB‑Linear), XGBoost Tree (XGB‑Tree), and Random Survival Forests (RSF). Models were trained with nested 5‑repeat × 5‑fold cross‑validation and hyperparameter tuning via random search (25 iterations).

**Key Findings:**  
- Best holdout performance in the post‑policy cohort: RSF C‑index 0.628; Cox Boost C‑index 0.627.  
- Cox model performed worst (C‑index 0.585).  
- Lasso and Elastic Net achieved holdout C‑indices of 0.613 each, but cross‑validated C‑indices were low (0.516 and 0.508).  
- Pre‑policy models showed similar ranking; Cox Boost held out C‑index 0.633, Cox 0.573.  
- Top predictive variables (post‑policy) included recipient age, total ischemic time, bilirubin, BMI, and ECMO status. Variable importance shifted between eras (e.g., ECMO less important post‑policy).

**Main Limitations:** Retrospective single‑nation registry design with no external validation and limited to pre‑transplant variables only.