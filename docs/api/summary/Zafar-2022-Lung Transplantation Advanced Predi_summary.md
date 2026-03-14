**Core Objective:** Develop a comprehensive risk‑scoring tool that predicts long‑term (1‑, 5‑, 10‑year) survival for lung transplant recipients by integrating recipient, donor, and transplant variables to guide optimal recipient‑donor matching.

**Patient Cohort & Study Scope:** 15 124 double lung transplant recipients (age ≥12 y, median age 57 y) from the UNOS registry, transplants performed between January 2005 and March 2020 (derivation n=10 660; validation n=4 464).

**AI/ML Approach:** Cox proportional‑hazards model with LASSO (Cox‑Lasso) for variable selection (42 candidate variables); risk scores clustered into three groups using expectation‑maximization (EM) algorithm. Competing models (Cox backward elimination, random‑forest Cox) were evaluated but performed inferiorly.

**Key Findings:**  
- Final model retained 13 recipient, 4 donor, 2 transplant variables.  
- C‑statistics for mortality prediction: 1‑year 0.67, 5‑year 0.64, 10‑year 0.72 (logistic models using the total risk score).  
- Validation cohort survival estimates matched observed outcomes: low‑risk 1‑yr 91.4% (obs 91.4%), 5‑yr 71.3% (obs 70.6%), 10‑yr 51.9% (obs 54.7%); medium‑risk 1‑yr 87.9%/89.0%, 5‑yr 61.6%/61.3%, 10‑yr 39.1%/38.3%; high‑risk 1‑yr 83.7%/81.6%, 5‑yr 51.3%/52.6%, 10‑yr 27.4%/27.6%.  
- Hazard ratios (validation) vs. low‑risk: medium 1.43 (95% CI 1.22–1.68), high 1.97 (1.67–2.33) (p < 0.0001).  
- Web‑based calculator provides individualized survival probabilities and median graft half‑life.

**Main Limitations:** Retrospective single‑nation (U.S.) design with no external validation outside UNOS data.