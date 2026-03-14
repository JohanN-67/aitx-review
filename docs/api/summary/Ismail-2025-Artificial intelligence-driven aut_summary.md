**Core Objective:** Develop an automated deep‑learning system to generate standardized lung size measurements from portable chest radiographs for lung transplant donor/recipient matching.

**Patient Cohort & Study Scope:** 50 lung transplant recipients; mean age 59.4 ± 10.8 years (range not specified); lung transplant only; data collected at the University of Pennsylvania between 2024 and 2025.

**AI/ML Approach:** Two‑step pipeline: (1) lung segmentation on posteroanterior CXRs using PSPNet (Pyramid Scene Parsing Network); (2) computer‑vision feature‑point detection to compute six height/width metrics. Input modality: portable chest radiographs (2D images). Model pretrained on the Darwin CXR dataset (≈6,500 images) with augmentation.

**Key Findings:**  
- Average absolute error vs. radiologist mean < 2.5% (≤ 7 mm).  
- Pearson correlation between AI and radiologist measurements = 0.97.  
- Intraclass correlation coefficients (ICC) for AI vs. radiologists ranged from 0.95 to 0.99 across all six measurements (e.g., R‑ACPA ICC = 0.98, L‑AMD ICC = 0.97).  
- AI performance comparable to inter‑radiologist agreement (ICC ≈ 0.96–0.98).  
- No AUC, C‑statistic, or accuracy reported (Not explicitly reported).

**Main Limitations:** Single‑center retrospective pilot with a small validation cohort and no external validation.