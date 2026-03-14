**Core Objective:** To develop and evaluate a machine learning (ML) ensemble model that predicts 1‑year post‑transplant survival in adult orthotopic heart transplantation (OHT) recipients using pre‑operative variables.

**Patient Cohort & Study Scope:** 33,657 primary OHT patients from the UNOS registry (2000‑2019); mean age 52.8 ± 12.4 years; 75% male; all received isolated heart transplants; data split 80% training (n = 26,926) and 20% validation (n = 6,731).

**AI/ML Approach:** Ensemble of 400 algorithms comprising deep neural network, logistic regression, AdaBoost, random forest, and additional resampling techniques (SMOTE, Edited Nearest Neighbors). Input: 47 selected pre‑operative features (demographics, labs, donor characteristics, support devices). Feature selection combined manual clinical review and random‑forest importance ranking.

**Key Findings:**  
- Ensemble model AUROC = 0.764 (95% CI 0.745–0.782) in validation set, significantly higher than logistic regression AUROC = 0.649 (95% CI 0.628–0.670).  
- Net reclassification index improvement over logistic regression: 72.9 % ± 3.8 % (p < 0.001).  
- Decision curve analysis showed superior net benefit across all risk thresholds (p < 0.001).  
- Comparative AUROCs for individual models: random forest 0.691, deep neural network 0.691, AdaBoost 0.653.

**Main Limitations:** Retrospective single‑registry design without external validation cohort.