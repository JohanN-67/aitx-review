# Data Extraction Report: Chao et al. - 2024 - Improving prognostic accuracy in lung transplantation using unique features of isolated human lung r
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The 2024 peer‑reviewed study applies a convolutional neural network (non‑linear AI) to adult donor lung radiographs during EVLP and predicts post‑transplant outcomes, meeting all population, intervention, comparator, outcome, and study design criteria.

## Identification & Methods
- **Sponsorship source**: UHN Foundation and T-CAIREM (Temerty Center for AI Research and Education in Medicine) Innovation Grant
- **Country**: Canada
- **Setting**: University Health Network, Toronto General Hospital (tertiary academic center)
- **Comments**: Retrospective analysis of clinical EVLP cases from 2008-2022.
- **Author_name**: Bonnie T. Chao
- **Institution**: University Health Network, Toronto, Canada
- **Email**: shaf.keshavjee@uhn.ca
- **Address**: Toronto, ON, Canada
- **Country of Data Origin**: Canada
- **Dataset Source**: EVLP radiographs and tabular physiological/biological data from Toronto General Hospital
- **Organ Focus**: Lung
- **Study Period End**: 2022
- **Study Period Start**: 2008
- **Identification Notes**: All bilateral EVLP cases with both 1 h and 3 h radiographs included (n=650 cases, 1300 images).
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Convolutional Neural Network (ResNet-50, ResNeXt-50, RexNet-100, EfficientNet-B2/B3, DenseNet-121) with PCA of latent features
- **Class Imbalance**: NR
- **Comparator**: Manual radiographic labeling and XGBoost model using manual labels
- **Input Variables**: Longitudinal EVLP radiographs, physiological parameters, biological markers
- **ML Primary Component**: Yes
- **Missing Data Handling**: NR
- **Validation Method**: Temporal split 80:20 (training 2008‑2020, validation 2020‑2022); internal validation on held‑out set
- **Methods Notes**: Pretraining on public ChestX-ray datasets, fine‑tuning on EVLP images; GradCAM for interpretability; PCA to reduce 4096 latent features to ten principal components

## Population Characteristics
- **Inclusion criteria**: All bilateral ex vivo lung perfusion (EVLP) cases performed at Toronto General Hospital from 2008 to 2022 with both 1‑hour and 3‑hour radiographs
- **Exclusion criteria**: NR
- **Sample Size Total**: 650
- **Target Population**: Donor lungs undergoing ex vivo lung perfusion (EVLP)
- **Population Notes**: Cohort split temporally into training set (n=520, 2008‑2020) and validation set (n=130, 2020‑2022) in an 80:20 ratio
- **Recipient Mean Age**: NR
- **Recipient Mean Age Overall**: NR
- **Recipient Female Sex Pct**: NR
- **Recipient Female Sex Pct Overall**: NR
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: NR
- **Diagnosis Overall**: NR
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
- **Specific Algorithm Name**: ResNet-50 convolutional neural network
- **Intervention Input Data Modality**: Isolated ex vivo lung radiographs (X‑ray images) with optional physiological data
- **Number of Predictors**: 4096 latent image features reduced to the top 10 principal components
- **Feature Selection Method**: Principal Component Analysis (PCA) on CNN latent features
- **Temporal Handling**: Longitudinal radiographs taken at multiple timepoints (e.g., 1 h and 3 h) processed together
- **Interventions Notes**: CNN pretrained on public chest X‑ray datasets then fine‑tuned on 1300 EVLP radiographs from 650 cases; ResNet-50 achieved best validation performance
- **Reported outcomes in study**: Recipient ventilation time <72 h, ≥72 h, and lungs deemed unsuitable for transplantation
- **Outcomes Notes**: Three‑class classification of donor lung outcomes based on EVLP radiographs and physiological data
- **Result data Notes**: CNN accuracy 66.9% (AUROC 78.4%) vs manual XGBoost 56% accuracy; multimodal model (physiology + radiographic PCs) improved accuracy to 78% and AUROC to 94% (p=0.014, p<0.0001)
- **Primary Outcome Reported name**: Donor lung outcome classification (suitability / recipient ventilation <72 h vs ≥72 h)
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Manual radiographic labeling (XGBoost baseline)
- **Primary Outcome Reported as**: Accuracy and AUROC
- **Primary Outcome Reference arm**: Manual XGBoost accuracy 56% (AUROC 76%)
- **Primary Outcome group**: All EVLP cases in validation set (n≈130)
- **Primary Outcome Reporting**: Accuracy 78% (AUROC 94%) for multimodal model
- **Primary Outcome Point Estimate**: 78% accuracy
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: 0.014 (accuracy improvement), <0.0001 (AUROC improvement)
- **Primary Outcome Test Set Size**: 130
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Proportion correctly classified (accuracy) and area under ROC curve on held‑out validation cohort
- **Primary Outcome Timepoints**: Radiographs at 1 h and 3 h; outcome measured as post‑transplant ventilation time
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Improvement achieved by adding radiographic principal components to the existing InsighTx physiological model
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
