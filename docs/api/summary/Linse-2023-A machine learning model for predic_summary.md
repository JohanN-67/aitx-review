**Core Objective:** Develop and internally validate an artificial neural network (ANN) model to predict 30‑day primary graft failure (PGF) after adult heart transplantation.

**Patient Cohort & Study Scope:** 64,964 adult heart transplant recipients (mean age 51 ± 12 years; 22% female) from the ISHLT Registry, transplanted between 1994 and 2013. PGF incidence was 3.7% (2,465 events).

**AI/ML Approach:** Fully‑connected multilayer perceptron (MLP) ANN with up to three hidden layers; best model used one hidden layer (50 nodes, ReLU activation). Input comprised 77 pre‑transplant donor–recipient variables (tabular EMR data) after one‑hot encoding and normalization. Missing data handled by multiple probability imputation (MPI) or mean imputation with extra category marker.

**Key Findings:**  
- Test AUROC = 0.69 (95% CI 0.68–0.71) for the MPI‑trained model; validation AUROC ≈ 0.68.  
- Corresponding C‑index reported as 0.70 (95% CI 0.68–0.71).  
- Model outperformed the RADIAL score (AUROC = 0.53; recalibrated AUROC = 0.61, p < 0.001).  
- Top predictive variables: donor age (EOR 1.22 per 11 yr), recipient diagnosis, mechanical ventilation at transplant (EOR 1.90), female‑donor→male‑recipient sex mismatch (EOR 1.34), ischemic time (EOR 1.12 per 45 min).  

**Main Limitations:** Retrospective single‑registry design with substantial missing data and no external validation.