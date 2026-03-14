**Core Objective:** To evaluate whether an AI algorithm that predicts physiological age from 12‑lead ECG can identify heart transplant recipients at higher risk of major adverse cardiovascular events (MACE) post‑transplantation.  

**Patient Cohort & Study Scope:** 540 heart transplant patients (mean recipient age 49 ± 14 y; donor age 32 ± 13 y) with pre‑ and post‑transplant ECGs; transplants performed between 1990 and 2018; median follow‑up 8.8 years.  

**AI/ML Approach:** Convolutional neural network (CNN) trained on raw 12‑lead ECGs to output continuous age estimate; applied without retraining to the study cohort. Input modality: standard 12‑lead ECG recordings.  

**Key Findings:**  
- Mean pre‑HTx AI‑ECG age 63 ± 11 y (age gap +13.3 y) and post‑HTx AI‑ECG age 54 ± 10 y.  
- ΔECG age ≥0 (increase after transplant) occurred in 135 patients (25%).  
- ΔECG age ≥0 associated with higher MACE risk: HR 1.58 (95% CI 1.24–2.01, P=0.0002) unadjusted; HR 1.58 (95% CI 1.18–2.10, P=0.002) after multivariable adjustment (including recipient/donor age, CAV grade, triglycerides).  
- Continuous ΔECG age also predictive: HR per year increase 1.02 (95% CI 1.00–1.03, P=0.008).  
- No AUC/C‑statistic reported for the AI‑ECG age prediction of MACE.  

**Main Limitations:** Retrospective single‑center design with limited external validation and missing donor‑specific antibody data.