**Core Objective:** Develop an AI system to automatically detect and classify cardiac allograft rejection—including acute cellular rejection (ACR), antibody‑mediated rejection (AMR), Quilty B lesions, and rejection grade—from H&E‑stained whole‑slide images (WSIs) of endomyocardial biopsies.

**Patient Cohort & Study Scope:** 1,044 patients total (US = 336, Turkey = 585, Switzerland = 123) with heart transplants; biopsy years 2004–2021 (US), 2002–2020 (Turkey), 2014–2020 (Switzerland). Age distribution not explicitly reported.

**AI/ML Approach:** Multitask weakly supervised deep learning (CRANE) using a ResNet‑50 CNN encoder pretrained on ImageNet, followed by attention‑based multiple‑instance learning (MIL) to aggregate 256 × 256 patches. Tasks: binary detection of ACR, AMR, Quilty B; separate binary grade classifier (low vs. high). No handcrafted features.

**Key Findings:**  
- Overall rejection detection AUC = 0.962 (95% CI 0.943–0.980), ACC = 0.899.  
- ACR detection AUC = 0.958 (95% CI 0.940–0.977), ACC = 0.893.  
- AMR detection AUC = 0.874 (95% CI 0.801–0.946), ACC = 0.899.  
- Quilty B lesion detection AUC = 0.939 (95% CI 0.910–0.969), ACC = 0.920.  
- Rejection‑grade discrimination AUC = 0.833 (95% CI 0.764–0.901), ACC = 0.818.  
- External validation showed AUC drops of 0.02–0.13 across cohorts but remained >0.80 for all tasks.  
- Human‑reader study: AI achieved κ = 0.639 vs. pathologists (κ = 0.537) and reduced assessment time when heatmaps were provided.

**Main Limitations:** Retrospective single‑center training with limited AMR cases and no prospective external validation.