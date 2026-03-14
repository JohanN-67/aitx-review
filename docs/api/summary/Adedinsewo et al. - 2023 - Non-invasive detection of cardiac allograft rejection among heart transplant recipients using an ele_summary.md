**Core Objective:**  
Develop and validate a deep‑learning model using 12‑lead electrocardiograms (AI‑ECG) to non‑invasively detect moderate‑to‑severe acute cellular rejection (ACR) in heart transplant recipients.

**Patient Cohort & Study Scope:**  
- Total patients: 1,427 heart transplant recipients (no lung transplants).  
- Age: median 58.3 years at last biopsy (Q1 48.7–Q3 65.2); 28.9% female.  
- Study period: ECGs and biopsies collected from 1998 to 2021 (retrospective) plus a prospective proof‑of‑concept cohort enrolled Oct–Dec 2021.  
- Data: 7,590 unique ECG‑biopsy pairs (retrospective); test set = 140 patients (758 pairs). Prospective cohort: 56 patients, 97 pairs.

**AI/ML Approach:**  
- Model: Convolutional neural network (39‑layer CNN) implemented in Keras/TensorFlow.  
- Input: Raw 12‑lead ECG signals (12 × 5,000 array; 10 s at 500 Hz).  
- Training/validation/test split: 80 %/10 %/10 % patient‑wise.

**Key Findings:**  
- Retrospective test set AUC = 0.84 (95 % CI 0.78–0.90).  
- Sensitivity = 95 % (19/20; 95 % CI 75.1–99.9), specificity = 52.6 % (388/738).  
- Positive predictive value = 5.1 %, negative predictive value = 99.7 %.  
- Prospective proof‑of‑concept AUC = 0.78 (95 % CI 0.61–0.96); sensitivity = 100 % (2/2), specificity = 60 % (57/95).  
- Model outperformed conventional ECG feature logistic regression (AUC ≈ 0.58) and comparable or superior to blood‑based non‑invasive tests (AUC 0.64–0.70).

**Main Limitations:**  
Retrospective derivation from a single‑center cohort (n = 1,427) with limited external validation and exclusion of antibody‑mediated rejection.