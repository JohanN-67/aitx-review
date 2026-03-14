**Core Objective:** To identify pre‑transplant variables that predict 1‑year mortality after adult cardiac retransplantation using a machine‑learning (random survival forests) approach.

**Patient Cohort & Study Scope:** 1,294 adult heart retransplant recipients from the UNOS registry (age median 45 years, IQR 30–57); 137 underwent early retransplantation (≤1 yr after first transplant) and 1,157 late retransplantation (>1 yr). Study period January 2000 – March 2020.

**AI/ML Approach:** Random Survival Forests (RSF) applied to a Cox‑type survival model; input variables were tabular pre‑operative donor and recipient characteristics (e.g., bilirubin, BMI, ventilator dependence, dialysis status, etc.). No external validation set was used.

**Key Findings:**  
- Early retransplantation 1‑year mortality = 40.6% vs. late = 13.6% (log‑rank P < 0.001).  
- RSF variable importance (VIMP): total bilirubin >2 mg/dL (VIMP 2.99%) predicted 1‑year mortality in early retransplantation; BMI >30 kg/m² (VIMP 1.43%) and ventilator dependence (VIMP 1.47%) predicted mortality in late retransplantation.  
- No conventional performance metrics (AUC, C‑statistic, accuracy) were reported; **Not explicitly reported**.

**Main Limitations:** Retrospective single‑registry design with substantial missing data and no external validation.