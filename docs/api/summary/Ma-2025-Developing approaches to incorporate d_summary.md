**Core Objective:** To develop and evaluate machine‑learning models that incorporate donor‑lung computed tomography (CT) images with clinical data to predict severe primary graft dysfunction (grade 3 PGD) within 72 hours after bilateral lung transplantation.  

**Patient Cohort & Study Scope:** 160 adult recipients of first‑time bilateral lung transplants performed at Washington University, St. Louis between 2010 and 2019 (mean recipient age 61 y; donor age median 34 y). Severe PGD occurred in 44 patients (27.5%).  

**AI/ML Approach:**  
- Imaging‑only models: four CNN architectures evaluated (ResNet50 montage, EfficientNet‑B7 slice‑based, 3D SE‑ResNet50).  
- Best imaging model: **3D ResNet** (Approach 4) using raw DICOM CT volumes.  
- Clinical data: 98 EHR variables reduced to 13 via LASSO (AIC).  
- Fusion strategies: early, joint, and **late fusion** of 3D ResNet features with the 13 selected clinical variables.  

**Key Findings:**  
- Imaging‑only 3D ResNet achieved median AUROC 0.63 (IQR 0.49‑0.72) and AUPRC 0.48 (0.35‑0.60).  
- Late fusion of imaging + clinical data yielded the highest performance: **AUROC 0.74 (0.59‑0.85), AUPRC 0.61 (0.47‑0.72), F1 0.54 (0.36‑0.62), PPV 0.50 (0.33‑0.60), NPV 0.82 (0.77‑0.88)**.  
- Compared with clinical data alone (AUROC 0.64, AUPRC 0.43), late fusion improved AUROC by 0.10 (p < 0.001) and AUPRC by 0.18 (p < 0.001).  

**Main Limitations:** Single‑center, retrospective design with a modest sample size (44 events) and no external validation.