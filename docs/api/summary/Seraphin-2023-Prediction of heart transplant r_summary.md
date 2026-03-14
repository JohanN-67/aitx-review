**Core Objective:**  
To assess whether a self‑supervised, attention‑based deep learning model can predict cellular rejection grade (ISHLT 0R, 1R, 2/3R) from routine H&E‑stained endomyocardial biopsy slides in heart transplant recipients.

**Patient Cohort & Study Scope:**  
Total patients = 325 (107 + 95 + 86 + 37). Median ages: 57, 59, 52, and 55 years respectively. Organ transplanted: heart only. Slides collected from four cohorts spanning 1999–2021 (Cohort 1: 2016‑18; Cohort 2: 2019‑21; Cohort 3: 2019‑21; Cohort 4: 1999‑14). Total slides = 1,079.

**AI/ML Approach:**  
- Model: Attention‑based multiple instance learning (MIL) built on a self‑supervised pre‑trained encoder (RetCCL, 2048‑dim features).  
- Input: Whole‑slide images tessellated into 512 × 512 px patches (≈400 tiles/slide).  
- Comparison: State‑of‑the‑art CRANE pipeline (ResNet‑50 ImageNet features, MIL).

**Key Findings:**  
- Binary rejection (yes/no) cross‑validated AUROC = 0.849 (95% CI 0.822–0.877). External validation AUROCs: Cohort 2 = 0.734, Cohort 3 = 0.729, Cohort 4 = 0.716.  
- ISHLT grade prediction (micro‑averaged) cross‑validated AUROC = 0.814; class‑wise AUROCs: 0R = 0.835, 1R = 0.633, 2/3R = 0.905. External validation AUROCs for 2/3R were highest (Cohort 2 = 0.913, Cohort 4 = 0.805).  
- CRANE baseline: cross‑validated binary AUROC = 0.776; external AUROCs = 0.831, 0.616, 0.483 (Cohorts 2‑4), consistently lower than the SSL‑MIL model.  
- Model interpretability: attention maps highlighted lymphocyte‑rich regions, aligning with pathologist expectations.

**Main Limitations:**  
Retrospective single‑center design with limited patient numbers and underrepresentation of higher rejection grades, leading to modest external generalizability.