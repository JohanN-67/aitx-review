**Core Objective:** To elucidate time‑varying risk factors and complex interactions influencing post‑heart transplant mortality, using machine‑learning to assess whether sex modifies survival outcomes.

**Patient Cohort & Study Scope:** 30,606 adult heart transplant recipients (7,778 females, 22,828 males) transplanted in the United States from 1 Jan 2004 to 1 Jul 2018; median age 56 y (overall), follow‑up median 3.9 years.

**AI/ML Approach:** Random Survival Forests (RSF) with 500 trees, log‑rank splitting, using 92 pre‑transplant variables (recipient and donor demographics, clinical status, organ support, laboratory values). Temporal decomposition (parametric non‑proportional hazards) was also applied for phase‑specific analysis.

**Key Findings:**  
- RSF identified top predictors across time points (90 d, 1 y, 5 y, 10 y): recipient age, BMI/BSA, total bilirubin, eGFR, dialysis, mechanical ventilation, ECMO, donor age, ischemic time (e.g., “mechanical ventilation + dialysis” and “bilirubin + renal dysfunction” were highest‑importance interactions).  
- No AUC/C‑statistic reported; model performance metrics not explicitly provided.  
- Sex was **not** a significant independent predictor of mortality; few sex‑specific interactions were found (e.g., bilirubin × sex in early phase).  
- Three mortality phases identified: early (≤1 mo), constant (~4%/yr), late (increasing risk, women slightly better survival).  
- Overall mortality: 8,278 deaths (26.1%); unadjusted survival 96% at 1 mo, 89% at 1 y, 50% at 12 y.

**Main Limitations:** Retrospective single‑database analysis limited by missing variables (e.g., natriuretic peptides) and potential data entry errors.