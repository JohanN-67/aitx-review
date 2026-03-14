**Core Objective:**  
Evaluate whether alternative statistical and machine learning models can improve discrimination of the Composite Allocation Score (CAS) waitlist (WL) and post‑transplant (PT) survival predictions for lung transplant candidates.

**Patient Cohort & Study Scope:**  
- WL cohort: 13,204 adult lung transplant candidates (age ≥ 18) listed between Feb 2015 and May 2020.  
- PT cohort: 20,763 adult lung transplant recipients transplanted between Jan 2010 and May 2020.  
- Organ type: Lung only.  
- Study design: Retrospective SRTR data, single‑nation (U.S.) registry.

**AI/ML Approach:**  
Seven models per outcome:  
1. Current LAS/CAS Cox model (weighted).  
2. Re‑estimated Cox on updated cohort.  
3. Cox with cubic splines (non‑linear).  
4. Random Survival Forests.  
5. Logistic regression on stacked survival data.  
6. Linear Discriminant Analysis (stacked).  
7. Gradient‑Boosted Trees (XGBoost) on stacked data.  

All models used the same tabular EMR variables employed in the official LAS/CAS (demographics, diagnosis group, pulmonary function, support devices, ADI, insurance, etc.).

**Key Findings:**  
- **Waitlist models:** AUC ≈ 0.92–0.93 for 1‑month prediction (baseline), declining to 0.84–0.85 at 6 months. No model outperformed the baseline LAS/CAS; best median AUCs were 0.93 (model II–III) vs 0.92 (model I).  
- **Post‑transplant models:** Consistently low discrimination, median AUC 0.58–0.61 across 1‑, 3‑, and 5‑year horizons; e.g., baseline 1‑yr AUC 0.61 (model I) vs 0.58 (model II). Gradient‑boosted tree (model VII) achieved 0.60 at 1 yr, not superior to Cox.  
- Subgroup analysis showed poorer WL discrimination for Medicaid patients and females; PT models performed worst for non‑Hispanic Black, Hispanic, younger recipients, and higher ADI quintiles.  
- Overall, advanced ML (random forests, gradient boosting) did **not** improve AUC over traditional Cox models.

**Main Limitations:**  
Retrospective single‑center (SRTR) design with no external validation cohort.