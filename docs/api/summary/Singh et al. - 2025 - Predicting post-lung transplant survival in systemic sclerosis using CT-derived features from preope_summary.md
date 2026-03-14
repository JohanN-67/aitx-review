**Core Objective:** To develop and evaluate pre‑operative chest CT–derived imaging biomarkers for predicting post‑lung transplant survival in patients with systemic sclerosis (SSc).

**Patient Cohort & Study Scope:** 102 SSc patients who underwent lung transplantation at a single U.S. center between 2004 and 2020 (mean age 50 ± 10 years; 61% female).

**AI/ML Approach:** Automated 3‑D convolutional neural networks (Unet‐based) segmented five body‑composition tissues and three cardiopulmonary structures on non‑contrast chest CTs. Features (e.g., bone density, muscle volume/ratio, artery–vein volume ratio, heart‑to‑chest volume ratio) were entered into Cox proportional hazards (CPH) regression models; performance assessed via 5‑fold cross‑validation ROC‑AUC, c‑index and Brier score.

**Key Findings:**  
- CT‑only model (CT‑features) achieved AUC 0.77 (95% CI 0.67–0.86) at 1‑yr, 0.85 (0.77–0.93) at 3‑yr, and 0.86 (0.77–0.94) at 5‑yr survival; c‑indices 0.737, 0.767, 0.767 respectively.  
- Adding CT features to demographic/clinical data (aggregate model) yielded the highest AUC 0.90 (95% CI 0.83–0.97) at 5‑yr, c‑index 0.752, Brier 0.134.  
- Significant predictors: bone density (HR 0.70, p = 0.027), muscle ratio (HR 0.71, p = 0.033), artery–vein volume ratio (HR 1.48, p = 0.0002), heart ratio (HR 1.53, p = 0.005).  
- Models using only CT features outperformed traditional demographic (AUC 0.61–0.70) and clinical (AUC 0.62–0.81) models.

**Main Limitations:** Retrospective single‑center design with a modest sample size (n = 102) and no external validation.