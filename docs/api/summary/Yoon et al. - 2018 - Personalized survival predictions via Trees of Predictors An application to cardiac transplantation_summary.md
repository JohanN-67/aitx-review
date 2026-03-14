**Core Objective:** Develop an interpretable machine‑learning method (Trees of Predictors, ToPs/R) to predict individual survival probabilities for adult heart‑transplant candidates and recipients, both pre‑ and post‑transplantation.

**Patient Cohort & Study Scope:** 51,971 transplanted adult patients (mean age not reported) and 30,911 wait‑listed adults from the UNOS registry, covering registrations between 1985 and 2015.

**AI/ML Approach:** ToPs/R combines hierarchical clustering of the feature space with cluster‑specific base learners (Cox regression, linear perceptron, logistic regression). Input data: 53 curated clinical variables (33 recipient, 14 donor, 6 compatibility features) derived from the original 504 UNOS fields.

**Key Findings:**  
- Post‑transplant 3‑month survival AUC = 0.660 ± 0.003 (vs. best clinical score RSS AUC = 0.587 ± 0.006).  
- Post‑transplant 3‑month C‑index = 0.577 ± 0.003 (vs. RSS C‑index = 0.544 ± 0.003).  
- Pre‑transplant 3‑month survival AUC = 0.685 ± 0.003 (vs. best ML benchmark AUC = 0.671 ± 0.004).  
- At 3‑year post‑transplant, holding specificity = 80 %, ToPs/R correctly identified 2,442 additional survivors (14.0 % of 17,441) and, holding sensitivity = 80 %, correctly identified 694 additional deaths (13.0 % of 5,339) compared with RSS.  
- When trained on the LVAD era (2005‑2009) and tested on 2010‑2015, AUC for 3‑month post‑transplant rose to 0.688 (vs. 0.660 on the full 1985‑2015 cohort) and to 0.758 for 3‑month pre‑transplant prediction.

**Main Limitations:** Retrospective single‑center analysis of registry data with missing variables and inability to compare pre‑transplant predictions against established clinical scores due to incomplete feature overlap.