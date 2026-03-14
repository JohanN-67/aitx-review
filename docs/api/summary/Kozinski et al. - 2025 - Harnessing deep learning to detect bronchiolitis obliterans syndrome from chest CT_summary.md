**Core Objective:** Develop a deep neural network (DNN) to detect bronchiolitis obliterans syndrome (BOS) from thoracic CT scans of lung transplant recipients, enabling diagnosis without dedicated high‑resolution or expiratory imaging and assessing early‑stage risk prediction.

**Patient Cohort & Study Scope:** 75 lung transplant patients (26 BOS, 49 non‑BOS) scanned between 1990 and 2020; mean age ≈ 47 years (range not specified); all participants received lung transplants (no heart transplants).

**AI/ML Approach:** Late‑fusion 2‑D convolutional DNN trained with co‑training (auxiliary task: predict temporal order of scan pairs) and slice dropout; input = raw CT slices (any reconstruction: high‑resolution lung kernel, thin standard kernel, or standard‑resolution). No other modalities used.

**Key Findings:**  
- Overall BOS vs. non‑BOS detection: ROC‑AUC 0.90 (95% CI 0.840–0.953).  
- Stage‑specific AUCs: stage I 0.88, stage II 0.91, stage III 0.94.  
- Early‑risk prediction (FEV1 80–90%): aggregated AUC 0.87 (95% CI 0.735–0.974).  
- Performance consistent across scan types: high‑resolution AUC 0.90, thin‑slice AUC 0.91, standard‑resolution AUC 0.90.  
- Ablation without overfitting controls reduced AUC to 0.74, confirming importance of co‑training and slice dropout.

**Main Limitations:** Retrospective single‑center design with modest sample size; lack of external validation and limited assessment of confounding diseases.