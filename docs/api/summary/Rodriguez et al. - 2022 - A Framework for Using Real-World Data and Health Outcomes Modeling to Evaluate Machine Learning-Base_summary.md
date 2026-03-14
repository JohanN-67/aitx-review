**Core Objective:**  
Evaluate the real‑world clinical utility of a machine‑learning (ML) mortality risk model for deciding lung transplant (LTx) referral in adults with cystic fibrosis, comparing it to FEV₁‑based referral and usual care (UC).

**Patient Cohort & Study Scope:**  
- Total patients analyzed: 4,247 (validation subset of a larger adult CF cohort; overall cohort n = 10,615).  
- Mean age: ≈33 years (range 18–?); similar across policies.  
- Organ transplanted: Lung only.  
- Study period: Baseline 1 Jan 2012 with follow‑up through 31 Dec 2016 (5‑year horizon).

**AI/ML Approach:**  
- Model: Super Learner ensemble combining lasso, elastic net, ridge, XGBoost, random forest, and support vector machine.  
- Input data: Longitudinal electronic medical record variables from the Cystic Fibrosis Foundation Patient Registry (demographics, pulmonary function, biomarkers, visit history) used to predict 2‑year mortality risk at each clinic encounter.

**Key Findings:**  
- Baseline discrimination: ML AUC = 0.914 (95% CI 0.898‑0.929); FEV₁ AUC = 0.876 (95% CI 0.858‑0.895); UC – no model AUC reported.  
- Referral rates over 5 years: ML 20.4% (95% CI 19.1‑21.6), FEV₁ 19.2% (18.0‑20.4), UC 12.4% (11.4‑13.4).  
- Earlier referral: ML referrals occurred on average 129 days earlier than UC (when both referred).  
- Pre‑transplant deaths among patients not referred under UC: ML would have referred 40.0% (35.3‑44.5) vs. FEV₁ 31.2% (26.9‑35.6).  
- Transplant numbers unchanged due to fixed organ supply; 5‑year overall survival ≈4.75 years for all policies (ML 4.75, FEV₁ 4.74, UC 4.73).  
- In a doubled‑organ scenario, ML yielded more transplants (441 vs. 367 UC) and slightly higher 5‑year survival (4.77 vs. 4.74 years).

**Main Limitations:**  
Retrospective single‑center simulation using real‑world data without external validation of the ML model.