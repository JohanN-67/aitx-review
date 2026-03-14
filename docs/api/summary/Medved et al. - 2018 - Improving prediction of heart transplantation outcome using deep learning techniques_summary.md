**Core Objective:** To compare the predictive performance of a deep‑learning based International Heart Transplantation Survival Algorithm (IHTSA) versus the logistic‑regression Index for Mortality Prediction After Cardiac Transplantation (IMPACT) for forecasting one‑year mortality after adult heart transplantation.  

**Patient Cohort & Study Scope:** 27,860 transplant events (27,705 unique adult recipients) from the UNOS registry, ages 18–78 (mean 52 ± 13 years), heart only transplants performed between January 1997 and December 2011. Derivation cohort: 22,263 transplants (≤2008); test cohort: 5,597 transplants (2009–2011).  

**AI/ML Approach:** IHTSA – ensemble of artificial neural networks (deep learning) using 43 variables (32 recipient, 11 donor). IMPACT – logistic regression model using 18 recipient‑only variables. Input data: tabular UNOS registry fields (demographics, clinical, donor characteristics).  

**Key Findings:**  
- Test‑cohort AUROC for one‑year mortality: IHTSA 0.643 (95% CI 0.619–0.667) vs IMPACT 0.608 (0.583–0.634); ΔAUROC ≈ 11.7% error reduction (p=0.004).  
- Recalibrated IHTSA AUROC 0.65 (0.63–0.68) vs IMPACT 0.61 (0.58–0.63); p=0.001.  
- Harrell’s C‑index (long‑term survival) in test cohort: IHTSA 0.61 (0.59–0.63) vs IMPACT 0.58 (0.56–0.61); ΔC‑index ≈ 10.3% (p=0.002).  
- Predicted one‑year mortality rates: IHTSA 12% vs IMPACT 22% (actual 10%).  
- Correctly classified patients in test cohort (one‑year mortality): IHTSA 4,812/5,597 vs IMPACT 4,539/5,597 at 25% sensitivity threshold.  

**Main Limitations:** Retrospective single‑registry analysis with potential overfitting and missing data imputation.