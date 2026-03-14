**Core Objective:**  
Develop and evaluate a calibrated risk‑prediction framework using focal loss–aware gradient‑boosted trees (GBDT) to predict post‑transplant malignancy (PTLD) in lung transplant recipients and diabetes status in a population survey.

**Patient Cohort & Study Scope:**  
- Lung transplant dataset: 33,244 adult recipients (age ≈ 55 ± 13 years) from the SRTR, transplanted 1 Jan 1988 – 28 Nov 2020; PTLD events = 984 (2.96%).  
- Diabetes dataset: 229,474 survey participants (age range 18‑85 years) from the 2015 BRFSS; diabetes prevalence = 15.29%.  

**AI/ML Approach:**  
- Models: XGBoost and LightGBM GBDT trained with focal loss (γ tuned via Bayesian optimization) and standard cross‑entropy loss for comparison.  
- Calibration: Closed‑form Ψγ transformation applied to focal‑loss scores; also evaluated Platt scaling and isotonic regression.  
- Input modalities: Tabular electronic health record features (54 variables for PTLD; 21 variables for diabetes).  

**Key Findings:**  
- **Lung transplant (10‑yr PTLD):** Calibrated XGBoost‑Focal (Ψγ) achieved AUROC = 0.700, Brier score = 0.128, calibration slope = 0.968; miscalibrated XGBoost‑Focal (no Ψγ) had identical AUROC but Brier = 0.140 and slope = 1.579. Standard XGBoost (cross‑entropy) AUROC = 0.736, Brier ≈ 0.129.  
- **1‑yr PTLD:** XGBoost‑Focal AUROC = 0.755 vs. standard XGBoost AUROC = 0.736; calibrated version retained AUROC = 0.755 with improved sensitivity (0.631) at prevalence‑based threshold.  
- **Diabetes prediction:** XGBoost‑Focal (Ψγ) AUROC = 0.818, Brier score = 0.1052, matching standard XGBoost; calibration plots showed accurate probability estimates after Ψγ/Platt scaling.  
- Overall, focal loss improved discrimination for rare PTLD events without degrading AUROC, and Ψγ transformation markedly reduced Brier scores (e.g., from 0.140 to 0.128 for 10‑yr PTLD).  

**Main Limitations:**  
Retrospective single‑center SRTR data with heterogeneous transplant eras and no external validation cohort.