**Core Objective:** Develop an artificial neural network model to predict short‑term survival (graft success vs failure) after thoracic (heart/lung) transplantation using UNOS data.

**Patient Cohort & Study Scope:** 485 adult thoracic transplant recipients (231 F, 254 M) extracted from the UNOS database; age range 17–68 years (mean ≈ 51 y). Transplants performed between 1994‑10‑01 and 1999‑10‑25 (data collection period). Only heart transplants were analyzed.

**AI/ML Approach:**  
- Models: Multi‑layer Perceptron (MLP) ANN with back‑propagation; Radial Basis Function (RBF) ANN for validation.  
- Input modality: Tabular clinical variables (24 selected attributes covering donor, recipient, and procedural factors).  
- Validation: 10‑fold cross‑validation.

**Key Findings:**  
- MLP achieved **accuracy 97.1%**, sensitivity 0.966, specificity 0.984, precision 0.972, recall 0.971, F‑measure 0.971, ROC AUC **0.918**.  
- RBF yielded lower performance: accuracy 92.37%, sensitivity 0.935, specificity 0.893, ROC AUC **0.95** (reported but not directly linked to survival prediction).  
- Error metrics for MLP: MAE 0.0309, RMSE 0.165, RAE 7.515%, RRSE 36.423%; for RBF: MAE 0.1149, RMSE 0.2501.  
- Compared to prior work (Oztekin et al., 2009 MLP accuracy 85.9%), the proposed MLP improved accuracy by ~11 percentage points.

**Main Limitations:** Retrospective single‑center design with no external validation cohort.