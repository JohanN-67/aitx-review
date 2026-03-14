# Data Extraction Report: Singh et al. - 2025 - Predicting post-lung transplant survival in systemic sclerosis using CT-derived features from preope
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Requires Human Review (Rejected by LLM)

## Eligibility
- **Eligibility Status**: Not Accepted
- **Eligibility Rationale**: Although the study involves adult lung transplant recipients and uses deep learning for image segmentation, the survival prediction relies on Cox regression (a linear model) rather than a non‑linear AI predictive algorithm, thus failing the intervention criterion.

## Identification & Methods
- **Sponsorship source**: National Institutes of Health
- **Country**: USA
- **Setting**: Single center, University of Pittsburgh Medical Center
- **Comments**: Retrospective cohort study of 102 systemic sclerosis patients who underwent lung transplantation between 2004 and 2020, using preoperative chest CT scans.
- **Author_name**: Jatin Singh
- **Institution**: Department of Radiology, University of Pittsburgh, Pittsburgh, PA, USA
- **Email**: jps162@pitt.edu
- **Address**: Pittsburgh, PA, USA
- **Country of Data Origin**: USA
- **Dataset Source**: Preoperative chest CT scans and clinical data from University of Pittsburgh Medical Center
- **Organ Focus**: Lung
- **Study Period End**: 2020
- **Study Period Start**: 2004
- **Identification Notes**: Included adults with systemic sclerosis, pre‑operative chest CT available, and lung transplant performed at UPMC between 2004–2020.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: 3‑D convolutional neural networks (Unet architecture) for automatic segmentation and feature extraction
- **Class Imbalance**: NR
- **Comparator**: Traditional clinical/demographic models without CT‑derived features
- **Input Variables**: Demographics, clinical variables (e.g., ACCI, tracheostomy, calcinosis, PAH), five CT‑derived body composition features and three cardiopulmonary CT features
- **ML Primary Component**: Yes
- **Missing Data Handling**: Features with missing values were excluded from analysis; no imputation performed
- **Validation Method**: 5‑fold cross‑validation
- **Methods Notes**: Cox proportional hazards regression with backward stepwise selection; performance evaluated using ROC‑AUC, c-index, Brier score; 5‑fold CV applied to all models.

## Population Characteristics
- **Inclusion criteria**: SSc diagnosis, availability of chest CT imaging prior to LTx, and LTx due to SSc complications
- **Exclusion criteria**: NR
- **Sample Size Total**: 102
- **Target Population**: Systemic sclerosis patients undergoing lung transplantation
- **Population Notes**: Retrospective single-center cohort from University of Pittsburgh (2004-2020), IRB approved, 49% mortality during follow-up
- **Recipient Mean Age**: 50
- **Recipient Mean Age Overall**: 50
- **Recipient Female Sex Pct**: 61
- **Recipient Female Sex Pct Overall**: 61
- **Mean BMI**: 24.9
- **Mean BMI Overall**: 24.9
- **Diagnosis**: Systemic sclerosis (SSc)
- **Diagnosis Overall**: Systemic sclerosis (SSc)
- **Diabetes Pct**: NR
- **Diabetes Pct Overall**: NR
- **Pre-transplant Support**: NR
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: NR
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: NR
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: 3-D convolutional neural networks (CNN) with classic Unet architecture
- **Intervention Input Data Modality**: Preoperative chest CT scans (non-contrast)
- **Number of Predictors**: NR
- **Feature Selection Method**: Backward-stepwise regression (Cox proportional hazards model)
- **Temporal Handling**: Static baseline pre‑transplant CT data
- **Interventions Notes**: Automated segmentation and quantification of five body composition tissues and three cardiopulmonary structures using 3‑D CNN Unet models
- **Reported outcomes in study**: Post‑lung transplant survival at 1, 3 and 5 years (ROC‑AUC)
- **Outcomes Notes**: CT‑features model achieved AUCs of 0.77 (1 yr), 0.85 (3 yr) and 0.86 (5 yr); aggregate model achieved AUC 0.90 at 5 yr
- **Result data Notes**: CT‑derived features improved prediction over demographic and clinical models; best performance in 5‑year survival
- **Primary Outcome Reported name**: Post‑lung transplant survival (1‑year)
- **Primary Outcome type**: Time‑to‑event classification
- **Primary Outcome Reported against**: Demographic and clinical baseline models
- **Primary Outcome Reported as**: Area under the receiver operating characteristics curve (ROC‑AUC)
- **Primary Outcome Reference arm**: Demographic model AUC 0.61 (95% CI 0.47–0.74)
- **Primary Outcome group**: All systemic sclerosis lung transplant recipients (n = 102)
- **Primary Outcome Reporting**: AUC 0.77 (95% CI 0.67–0.86)
- **Primary Outcome Point Estimate**: 0.77
- **Primary Outcome 95 CI Lower**: 0.67
- **Primary Outcome 95 CI Upper**: 0.86
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 102
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: ROC‑AUC calculated via 5‑fold cross‑validation on pre‑transplant CT features
- **Primary Outcome Timepoints**: 1 year post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: 5 years
- **Primary Outcome Notes**: CT‑features model outperformed traditional models for 1‑year survival prediction
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.77
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: 0.86
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
