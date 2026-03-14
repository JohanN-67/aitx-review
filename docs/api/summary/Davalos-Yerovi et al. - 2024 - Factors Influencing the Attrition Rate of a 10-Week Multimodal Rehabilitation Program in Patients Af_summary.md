**Core Objective:** To assess whether an artificial neural network (ANN) can identify baseline clinical factors that predict high attrition (>10% missing data) during a 10‑week multimodal rehabilitation program in lung transplant (LT) recipients.

**Patient Cohort & Study Scope:** 41 first‑time LT patients (mean age 55.8 ± 9.7 y; 22 men), all receiving lung transplants (90% double, 10% single) between January 2022 and September 2023 in a single tertiary center in Barcelona, Spain.

**AI/ML Approach:** Feed‑forward ANN implemented with the R `nnet` package (30 input neurons, tanh activation, decay 0.001). Input: 23 complete baseline variables (demographics, BMI, handgrip strength, sarcopenia/malnutrition indices, HRQoL, comorbidities, transplant indication). No external validation set.

**Key Findings:**  
- High attrition observed in 17/41 (41.4%).  
- ANN Garson importance identified low age‑dependent BMI, end‑stage respiratory disease (COPD), low health‑related quality of life (EQ‑5D VAS), and low handgrip strength as the strongest predictors (relative importance > 0.5).  
- Subsequent ordinal logistic regression confirmed statistical significance: low BMI (p = 7.08×10⁻⁵), COPD indication (p = 0.000111), HRQoL (p = 0.0009078), low handgrip strength (<80% Mediterranean reference, p = 0.023) and EWGSOP2 cutoff (p = 0.0456).  
- No performance metrics such as AUC, accuracy, or C‑statistic were reported for the ANN model. **Not explicitly reported.**

**Main Limitations:** Retrospective‑like single‑center design with a small sample and no external validation, limiting generalizability.