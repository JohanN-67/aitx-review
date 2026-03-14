**Core Objective:** Develop a convolutional neural network (CNN) to automatically interpret ex‑vivo lung perfusion (EVLP) radiographs and integrate extracted image features with physiological data to improve prediction of lung transplant outcomes (extubation <72 h, ≥72 h, or organ unsuitability).

**Patient Cohort & Study Scope:** 650 bilateral EVLP cases (1300 radiographs) from a single center (Toronto General Hospital) collected between 2008 and 2022. Mean/median age not reported; all cases involved lung transplantation (no heart transplants).

**AI/ML Approach:**  
- Image model: ResNet‑50 (pretrained on public chest X‑ray datasets, then fine‑tuned on EVLP radiographs).  
- Input modality: longitudinal isolated lung X‑ray images (1 h and 3 h time points).  
- Tabular model: XGBoost‑based “InsighTx” using physiological/biochemical EVLP data.  
- Fusion: Ten principal components (PCs) derived from the 4096‑dim latent vector of ResNet‑50 combined with InsighTx features.

**Key Findings:**  
- CNN alone (ResNet‑50) achieved **Accuracy 66.9%**, **AUROC 78.4%** on the validation set.  
- Compared with manual radiographic labeling, CNN‑derived features yielded **Accuracy 62.7 ± 1.8%** vs **56.0 ± 3.7%** (p = 0.0007); AUROC both ≈ 76% (no significant difference).  
- Adding the ten image PCs to InsighTx improved performance from **Accuracy 73 ± 5%**, **AUROC 88 ± 2%** to **Accuracy 78 ± 4%** (p = 0.014) and **AUROC 94 ± 2%** (p < 0.0001).  
- Precision rose from 64% to 73% (p = 0.02) and recall from 72% to 79% (p = 0.009).  
- PC #1 correlated strongly with radiographic consolidation/infiltration (Spearman R = 0.68–0.72, p < 0.0001) and was the most impactful feature in the fused model.

**Main Limitations:** Retrospective single‑center design with no external validation and limited interpretability of deep‑learning saliency maps.