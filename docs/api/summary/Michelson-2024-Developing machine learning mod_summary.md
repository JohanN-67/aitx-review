**Core Objective:**  
To develop and evaluate a machine‑learning model that predicts the occurrence of primary graft dysfunction (PGD) grade 3 within 72 hours after lung transplantation using donor and recipient variables available at the time of donor offer acceptance.

**Patient Cohort & Study Scope:**  
576 adult bilateral lung transplant recipients (median age 59 years, IQR 48‑65) transplanted at a single center between 1 Jan 2010 and 31 Dec 2019. All received lung (no heart) transplants; 173 (30%) developed PGD grade 3.

**AI/ML Approach:**  
Four classifiers were trained on 11 lasso‑selected pre‑transplant features (e.g., LAS, donor PaCO₂, recipient ICU admission). Models: Logistic Regression, K‑Nearest Neighbors (KNN), Extreme Gradient Boosting (XGB), Support Vector Classifier. Input data were tabular EMR variables merged from UNOS, UNet, and local EHR. Hyperparameters optimized via 5‑fold CV; performance assessed on a held‑out 25% test set with bootstrapping (50 iterations).

**Key Findings:**  
- **KNN (calibrated)** was chosen for deployment: AUROC 0.65, AUPRC 0.45, F1 0.62 (median values; narrow IQR).  
- **XGB (calibrated)** achieved the highest raw AUROC 0.69 but showed wider confidence intervals, indicating less stability.  
- Pre‑calibrated KNN AUROC 0.64, AUPRC 0.43, F1 0.63; calibrated KNN slightly improved calibration (intercept 0.075, slope 1.152).  
- Model calibration was acceptable overall; SHAP analysis identified LAS, donor PaCO₂, and recipient ICU status as top contributors.  

**Main Limitations:**  
Retrospective single‑center design with no external validation and limited to variables known before donor acceptance.