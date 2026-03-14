**Core Objective:**  
To evaluate whether a CALIPER‑based machine learning CT texture analysis can accurately phenotype chronic lung allograft dysfunction (CLAD) and predict graft failure in adult double‑lung transplant recipients.

**Patient Cohort & Study Scope:**  
- Total patients: **88** (57 BOS, 20 RAS/mixed, 11 unclassified/undefined).  
- Mean age at transplant: **≈ 47 years** (range 45–48 y across phenotypes).  
- Organ transplanted: **bilateral lung** only (first transplant).  
- Study period: **January 2010 – December 2015** with CLAD follow‑up censored December 2019; CT performed median **9.5 days** from CLAD onset.

**AI/ML Approach:**  
- Model: **CALIPER (Computer‑Aided Lung Informatics for Pathology Evaluation and Rating)** – a validated texture‑analysis algorithm (not retrained on transplant data).  
- Input modalities: **Inspiratory thin‑section CT** (≤1 mm slices); outputs quantified percentages of ground‑glass opacity, reticulation, hyperlucent lung, and pulmonary vessel volume (PVV).  

**Key Findings:**  
- **Phenotyping performance:**  
  - PVV distinguished RAS/mixed from BOS with **AUC 0.85** (sensitivity 90 %, specificity 70 %).  
  - Hyperlucent lung identified BOS on inspiratory CT with **AUC 0.76** (cut‑point 0.81 %).  
- **Prognostic performance (multivariable Cox, adjusted for age, sex, native disease, CMV serostatus, CLAD phenotype):**  
  - PVV hazard ratio **HR 1.23 (95 % CI 1.05–1.44), p=0.01**.  
  - RETML HR 1.20 (95 % CI 1.05–1.37), p=0.01.  
  - GGOML HR 1.36 (95 % CI 1.00–1.86), p=0.05.  
  - Radiologist scores for GGORAD, RETRAD, CONRAD also independently predicted graft failure (e.g., GGORAD HR 1.14, p<0.001).  
- **Accuracy metrics:** Machine learning hyperlucent lung classification accuracy **76 %**; PVV cut‑point accuracy **75 %**.  

**Main Limitations:**  
Retrospective single‑center design with limited sample size and a machine learning tool not specifically trained on lung‑transplant CT patterns.