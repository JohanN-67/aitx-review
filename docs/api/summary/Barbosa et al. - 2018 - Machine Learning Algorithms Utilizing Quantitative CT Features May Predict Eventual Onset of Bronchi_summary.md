**Core Objective:** To determine whether machine‑learning analysis of quantitative CT (qCT) features can predict the eventual development of bronchiolitis obliterans syndrome (BOS) in lung transplant recipients.

**Patient Cohort & Study Scope:** 71 lung transplant patients (41 BOS, 30 non‑BOS); age range 25–70 yr (mean 57 yr). Transplant types: 40 bilateral, 14 right unilateral, 17 left unilateral. CT data collected between 2010 and 2018 (retrospective analysis of scans obtained 15 days to 13 yr post‑transplant).

**AI/ML Approach:** Supervised support vector machine (SVM) with radial basis function kernel applied to baseline qCT parameters derived from functional respiratory imaging (FRI). Input modalities: paired inspiratory‑expiratory CT–derived metrics (lung lobar volumes, airway volumes, airway resistance, surface area).

**Key Findings:**  
- 23 baseline qCT features significantly differed between eventual BOS developers and non‑developers (P < 0.05); conventional PFTs did not.  
- SVM using three selected qCT features (right middle‑lobe volume at TLC, right upper‑lobe airway resistance at FRC, central airway surface at FRC) achieved **85 % accuracy**, **73.3 % sensitivity**, and **92.3 % specificity** for predicting BOS onset.  
- Two‑feature models reached up to **83 % accuracy**; single‑feature models up to **76 % accuracy** (central or total airway volume at FRC).  
- Linear mixed‑effects analysis showed BOS patients had increasing lung volume at functional residual capacity (P = 0.027) and central airway volume at FRC (P = 0.018), whereas non‑BOS patients showed decreasing central airway volume at TLC (P = 0.039).

**Main Limitations:** Retrospective single‑center design with heterogeneous CT acquisition timing and no external validation.