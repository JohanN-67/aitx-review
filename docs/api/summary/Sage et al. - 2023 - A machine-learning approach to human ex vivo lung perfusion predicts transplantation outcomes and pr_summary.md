**Core Objective:**  
Develop and validate a machine‑learning model (InsighTx) to predict ex vivo lung perfusion (EVLP) outcomes and post‑transplant clinical results, enabling rapid decision‑making on lung suitability for transplantation.

**Patient Cohort & Study Scope:**  
- Total EVLP cases: **725** (training = 504; test 1 = 97; test 2 = 124).  
- Mean donor age: **≈ 45–48 years** (SD ≈ 16‑17).  
- Organ type: **lung only** (both DBD and DCD donors).  
- Study period: **2008 – 2022** (development 2008‑2019; validation 2019‑2020 and 2020‑2022).

**AI/ML Approach:**  
- Algorithm: **XGBoost (eXtreme Gradient Boosting)**, class‑weighted.  
- Input modalities: comprehensive EVLP data—including physiological (compliance, airway pressures), biochemical (pH, base excess, lactate, electrolytes), gas exchange (ΔpO₂, ΔpCO₂), and cytokine levels (IL‑6, IL‑8, IL‑10, IL‑1β) collected hourly for up to 4 h.

**Key Findings:**  
- Overall AUROC: **79 ± 3 % (training), 75 ± 4 % (test 1), 85 ± 3 % (test 2)**.  
- Suitability prediction AUROC: **90 ± 4 % (training), 88 ± 4 % (test 1), 95 ± 2 % (test 2)**.  
- Extubation <72 h AUROC: **80 ± 4 % (training), 76 ± 6 % (test 1), 83 ± 4 % (test 2)**.  
- Precision for unsuitable lungs: **81 %**; for suitable lungs (extubation <72 h): **72 %**.  
- Implementation study: odds ratio = 13 (95 % CI 4‑45) for transplanting suitable lungs; odds ratio = 0.4 (95 % CI 0.16‑0.98) for unsuitable lungs when model was available.

**Main Limitations:**  
Retrospective single‑center design with no external validation.