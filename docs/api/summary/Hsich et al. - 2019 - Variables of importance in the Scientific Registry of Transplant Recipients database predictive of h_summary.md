**Core Objective:** To identify which pre‑listing variables in the Scientific Registry of Transplant Recipients (SRTR) most strongly predict mortality among adult heart transplant candidates, informing a data‑driven allocation score.

**Patient Cohort & Study Scope:** 33 069 adult heart transplant candidates listed on the active waitlist from 1 Jan 2004 to 31 Aug 2015 (median follow‑up 4.3 months). Mean/median age ≈55 years; 73% male; all received heart transplants (no lung cases). UNOS status distribution: 7 681 Status 1A, 13 027 Status 1B, 12 361 Status 2.

**AI/ML Approach:** Random Survival Forests (RSF) applied separately within each UNOS status using baseline tabular EMR variables (demographics, labs [eGFR, albumin], hemodynamics, device support [ECMO, VAD, IABP], functional capacity [pVO₂], medication use). Variable importance (VIMP) derived from out‑of‑bag Harrell’s C‑index.

**Key Findings:**  
- eGFR was the top predictor of waitlist mortality (VIMP ≈ 1.5% for UNOS 1A), followed by serum albumin, ECMO, VADs, mechanical ventilation, and pVO₂.  
- Survival declined sharply when eGFR < 80 mL/min/1.73 m² and albumin < 3.0 g/dL; sex modified the eGFR effect (worse survival for women with eGFR 40‑80).  
- Current UNOS tiered allocation captures most high‑importance variables except eGFR and albumin, which showed additive risk and complex interactions.  
- Weak predictors included anti‑arrhythmic use, prior stroke, vascular disease, malignancy, blood type, and BMI.  

**Performance Metrics:**  
- Model discrimination: Not explicitly reported (no AUC or C‑statistic provided).  
- Sample Size Total: 33 069.  
- Specific Algorithm: Random Survival Forest (RSF).  

**Main Limitations:** Retrospective single‑national‑registry design with limited variable granularity and missingness, lacking external validation.