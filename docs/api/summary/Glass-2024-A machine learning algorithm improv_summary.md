**Core Objective:** Develop a deep‑learning model to automatically identify the histologic component of antibody‑mediated rejection (pAMR‑H) in cardiac transplant endomyocardial biopsies and differentiate it from normal myocardium, healing injury, and acute cellular rejection (ACR).

**Patient Cohort & Study Scope:** 300 H&E‑stained endomyocardial biopsy slides from cardiac transplant recipients (2018–2021) at Duke University; annotations derived from 4,212 image patches (1,053 per class). Age distribution not reported. Total patients ≈ 300.

**AI/ML Approach:** Supervised convolutional neural network (ResNet‑50) with transfer learning on 224 × 224 pixel patches; input modality = whole‑slide digital pathology (Leica Aperio GT450, 40×). Training/validation/testing split = 70 %/10 %/20 %.

**Key Findings:** Overall validation accuracy = 98 %; class‑specific accuracies: pAMR‑H vs. normal 99.2 %, vs. healing injury 99.5 %, vs. ACR 99.5 %. Reported AUC for pAMR‑H vs. each comparator = 0.992. Human pathologist κ = 0.10–0.65; concordance 88 % (drops to 70‑65 % with mixed lesions).  

**Main Limitations:** Single‑center development on annotated patches; whole‑slide performance and external generalizability not yet validated.