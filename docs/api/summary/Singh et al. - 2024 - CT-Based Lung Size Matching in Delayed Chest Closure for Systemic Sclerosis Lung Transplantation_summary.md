**Core Objective:** To determine pre‑operative clinical and CT‑derived lung size–matching predictors of delayed chest closure (DCC) versus primary chest closure (PCC) in systemic sclerosis (SSc) patients undergoing bilateral lung transplantation, and to assess the impact of DCC on postoperative outcomes.

**Patient Cohort & Study Scope:** 92 SSc recipients (mean age 51 ± 10 years; 61% female) undergoing bilateral lung transplantation from 2007 to 2020 at a single U.S. center; 32 (34.8%) received DCC.

**AI/ML Approach:** Multivariate logistic regression model trained on pre‑operative variables (clinical + two CT‑derived volumetric ratios). Input modalities: tabular EMR data and quantitative CT measurements obtained via an in‑house 3‑D CNN (U‑Net) for lung and chest cavity segmentation.

**Key Findings:**  
- The logistic regression model achieved a mean AUC of **0.82 (95% CI 0.70–0.94)** and mean accuracy of **0.73 (range 0.60–0.86)** in predicting DCC occurrence (5‑fold cross‑validation).  
- Significant predictors: previous chest operation (β = 2.08, p = 0.004), atrial fibrillation (β = 1.82, p = 0.006), BMI > 30 kg/m² (β = 1.92, p = 0.011), tracheostomy (β = 1.36, p = 0.018), ACE‑inhibitor therapy (β = −2.87, p = 0.017), and donor age (β = −0.67, p = 0.045).  
- Two CT‑based size‑matching ratios were independently associated with DCC (DpTLC/RCT Lung Vol ratio, p = 0.021; DpTLC/RCT Chest Cavity Vol ratio, p = 0.050).  
- Survival at 30 days, 90 days, 1 year, and 5 years did not differ between DCC and PCC (all p > 0.65).  
- DCC recipients experienced longer total ventilation time, higher postoperative mechanical support use, and longer ICU stay (all p < 0.01), but a lower incidence of postoperative pneumonia (p = 0.031).

**Main Limitations:** Retrospective single‑center design with a modest sample size and no external validation cohort.