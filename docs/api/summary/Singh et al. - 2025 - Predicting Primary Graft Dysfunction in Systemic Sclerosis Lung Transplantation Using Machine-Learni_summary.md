**Core Objective:** To develop and evaluate machine‑learning models that predict grade 3 primary graft dysfunction (PGD) at 72 h after bilateral lung transplantation in patients with systemic sclerosis (SSc) using pre‑operative clinical data and CT‑derived thoracic features.  

**Patient Cohort & Study Scope:** 92 SSc recipients (mean age 51 ± 10 years) undergoing bilateral lung transplantation at a single center from 2007 to 2020; 20 (21.7 %) developed PGD.  

**AI/ML Approach:** Four algorithms were trained on four selected pre‑transplant features (pre‑op FEV1, heart‑to‑chest cavity volume ratio, waitlist time, donor‑to‑recipient chest cavity volume ratio). Models used tabular inputs derived from electronic health records and automatically extracted 3‑D CT features (lung, chest cavity, heart, adipose tissues) via deep learning CNNs (U‑Net and custom 3‑D CNN).  

**Key Findings:**  
- MLP achieved the highest discrimination: AUROC 0.85 (95 % CI 0.81–0.88), AUPRC 0.61 (95 % CI 0.53–0.68).  
- SVM: AUROC 0.83 (0.79–0.86), AUPRC 0.58 (0.49–0.66).  
- Random Forest: AUROC 0.77 (0.73–0.82), AUPRC 0.51 (0.42–0.60).  
- Multivariate logistic regression: AUROC 0.84 (0.81–0.88), AUPRC 0.62 (0.54–0.70).  
- Significant CT predictors of PGD included decreased lung volume, increased heart‑chest cavity ratio, and oversized donor‑to‑recipient chest cavity volume ratio (all p < 0.001).  

**Main Limitations:** Retrospective single‑center design with a modest sample size and no external validation.