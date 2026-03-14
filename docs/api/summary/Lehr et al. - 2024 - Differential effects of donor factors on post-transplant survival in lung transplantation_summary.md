**Core Objective:** To assess how donor characteristics influence post‑transplant survival in adult bilateral lung transplant recipients and whether incorporating these factors improves prediction beyond the existing post‑transplant Composite Allocation Score (PT‑CAS).

**Patient Cohort & Study Scope:** 7,609 bilateral lung transplant recipients; median age 59 years (IQR 49‑64); lung transplants only; data from the US Scientific Registry of Transplant Recipients between 19 Feb 2015 and 1 Feb 2020.

**AI/ML Approach:**  
- Cox proportional hazards multivariable model incorporating donor factors and interactions (COX).  
- Random survival forest (RF).  
- Both models evaluated alone and combined with PT‑CAS variables (COX + PT‑CAS, RF + PT‑CAS).  
- Input data: tabular donor and recipient variables from SRTR (demographics, clinical history, organ‑specific metrics).

**Key Findings:**  
- COX model alone: 1‑year AUC 0.606 (≈ PT‑CAS AUC 0.609).  
- COX + PT‑CAS: 1‑year AUC 0.626, a modest improvement (ΔAUC +0.02).  
- RF model alone: 1‑year AUC 0.604; RF + PT‑CAS: 1‑year AUC 0.614.  
- Similar discrimination trends observed at 3 and 5 years.  
- Calibration improved markedly for the combined COX + PT‑CAS model across a broader risk range.  
- Interaction analysis revealed age‑, sex‑, and diagnosis‑specific donor effects (e.g., donor smoking reduced survival for recipients 31‑54 y and ≥70 y; CMV mismatch detrimental for male recipients).

**Main Limitations:** Retrospective single‑nation design with no external validation cohort.