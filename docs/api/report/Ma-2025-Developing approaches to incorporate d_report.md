# Data Extraction Report: Ma-2025-Developing approaches to incorporate d
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study involves adult lung transplant recipients and uses deep learning (non‑linear AI) to predict severe primary graft dysfunction, an important post‑transplant outcome, and is a peer‑reviewed article published after 2018.

## Identification & Methods
- **Sponsorship source**: Health Resources and Services Administration contract HHSH250-2019-00001C; Mid-America Transplant Foundation grant #07202001
- **Country**: USA
- **Setting**: Single-center tertiary academic center (Washington University in St. Louis)
- **Comments**: Retrospective cohort study of first-time bilateral lung transplants with donor CT scans over a 10‑year period.
- **Author_name**: Andrew P. Michelson
- **Institution**: Washington University School of Medicine, St. Louis
- **Email**: amichels@wustl.edu
- **Address**: 660 S. Euclid Ave., Campus Box 8030, St. Louis, MO 63110, USA
- **Country of Data Origin**: USA
- **Dataset Source**: UNOS registry combined with donor CT scans from Mid‑America Transplant and other organ procurement organizations, stored in REDCap
- **Organ Focus**: Lung
- **Study Period End**: 2019
- **Study Period Start**: 2010
- **Identification Notes**: Adults ≥18 years, first-time bilateral lung transplantation at Washington University between Jan 1 2010 and Dec 31 2019, donors with available lung CT scans; excluded multiorgan or single‑lung transplants.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: 3D ResNet (SE‑ResNet50 3D), EfficientNet‑B7 for feature extraction, ResNet‑50 for montage approaches
- **Class Imbalance**: NR
- **Comparator**: Clinical data‑only model (baseline) and imaging‑only approaches
- **Input Variables**: Donor lung CT images plus 13 selected clinical phenotype features extracted from EHR/UNOS data
- **ML Primary Component**: Yes
- **Missing Data Handling**: Median imputation for missing clinical variables
- **Validation Method**: Stratified train/validation/test split (75%/12.5%/12.5%) with 7‑fold cross‑validation and bootstrap analysis (100 iterations)
- **Methods Notes**: Three‑step gated process: (1) identify optimal imaging method via transfer learning; (2) feature reduction using LASSO with AIC; (3) fuse imaging and clinical data using early, joint, and late fusion—late fusion yielded best performance.

## Population Characteristics
- **Inclusion criteria**: Adults ≥18 years who underwent first-time bilateral lung transplantation between Jan 1, 2010 and Dec 31, 2019 at Washington University with donor lung CT scans available
- **Exclusion criteria**: Simultaneous multiorgan transplantation, single lung transplantation, retransplantation (only first transplant included)
- **Sample Size Total**: 160
- **Target Population**: Recipients
- **Population Notes**: Single-center cohort of first-time bilateral lung transplant recipients with donor CT scans; 160 patients included
- **Recipient Mean Age**: 61
- **Recipient Mean Age Overall**: 61
- **Recipient Female Sex Pct**: 41.88
- **Recipient Female Sex Pct Overall**: 41.88
- **Mean BMI**: 25.1
- **Mean BMI Overall**: 25.1
- **Diagnosis**: Interstitial lung disease (most common primary diagnosis)
- **Diagnosis Overall**: Interstitial lung disease most common overall
- **Diabetes Pct**: NR
- **Diabetes Pct Overall**: NR
- **Pre-transplant Support**: NR
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: 34
- **Donor Mean Age Overall**: 34
- **Ischemic Time**: NR
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: 3D ResNet (SE-ResNet50 3D) for imaging; EfficientNet B7 used in fusion
- **Intervention Input Data Modality**: Donor-lung computed tomography images and electronic health record clinical data
- **Number of Predictors**: 13 selected clinical features after LASSO reduction
- **Feature Selection Method**: LASSO regression with Akaike's information criterion, repeated 100 times
- **Temporal Handling**: Static baseline data (CT and clinical variables at time of donor offer)
- **Interventions Notes**: Four imaging approaches evaluated; best imaging-only model was 3D ResNet; late fusion of imaging and clinical data yielded highest performance
- **Reported outcomes in study**: Severe primary graft dysfunction (grade 3) within 72 hours; AUROC, AUPRC, accuracy, F1 score, PPV, NPV
- **Outcomes Notes**: Primary outcome is binary classification of severe PGD within first 72 hours post‑transplant
- **Result data Notes**: Imaging-only best AUROC 0.63 (0.49‑0.72); late fusion AUROC 0.74 (0.59‑0.85) with higher AUPRC and PPV
- **Primary Outcome Reported name**: Severe primary graft dysfunction (grade 3) within 72 hours
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Clinical‑data‑only model (baseline)
- **Primary Outcome Reported as**: Area under the receiver operating characteristic curve (AUROC) and area under precision‑recall curve (AUPRC)
- **Primary Outcome Reference arm**: Clinical data only AUROC 0.64 (0.54‑0.72)
- **Primary Outcome group**: All lung transplant recipients in the cohort (n=160)
- **Primary Outcome Reporting**: AUROC 0.74 (0.59‑0.85) for late fusion
- **Primary Outcome Point Estimate**: 0.74
- **Primary Outcome 95 CI Lower**: 0.59
- **Primary Outcome 95 CI Upper**: 0.85
- **Primary Outcome p-value**: <0.001
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: Probability >0.5 considered positive for PGD
- **Primary Outcome Metric Definition**: AUROC calculated on held‑out test set aggregated over 100 bootstrap iterations
- **Primary Outcome Timepoints**: Within 72 hours post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Late fusion of imaging and clinical data provided the best predictive performance for severe PGD
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: 0.74 (0.59-0.85)
- **Res_Primary Late Accuracy**: 0.7 (0.65-0.8)
- **Res_Primary Late Sens_Spec**: NR
