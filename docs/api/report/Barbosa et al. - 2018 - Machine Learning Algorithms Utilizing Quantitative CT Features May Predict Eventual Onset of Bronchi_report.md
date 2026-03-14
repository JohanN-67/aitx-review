# Data Extraction Report: Barbosa et al. - 2018 - Machine Learning Algorithms Utilizing Quantitative CT Features May Predict Eventual Onset of Bronchi
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study involves adult lung transplant recipients and uses a non‑linear machine learning model (support vector machine) to predict bronchiolitis obliterans syndrome, an important post‑transplant complication, and was published as a peer‑reviewed article in 2018.

## Identification & Methods
- **Sponsorship source**: NR
- **Country**: NR
- **Setting**: NR
- **Comments**: Retrospective analysis of paired inspiratory‑expiratory CT scans and pulmonary function tests from 71 lung transplant patients (41 BOS, 30 non‑BOS).
- **Author_name**: Eduardo J. Mortani Barbosa Jr
- **Institution**: Perelman School of Medicine, University of Pennsylvania
- **Email**: Eduardo.Barbosa@uphs.upenn.edu
- **Address**: 3400 Spruce Street, Philadelphia, PA 19104
- **Country of Data Origin**: NR
- **Dataset Source**: Retrospective clinical CT and PFT data from lung transplant recipients.
- **Organ Focus**: Lung
- **Study Period End**: NR
- **Study Period Start**: NR
- **Identification Notes**: 71 LTx patients with paired inspiratory‑expiratory CT scans; BOS defined by >10% sustained FEV1 decline.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Support Vector Machine with radial basis function kernel (cost=1, gamma=1/feature dimension).
- **Class Imbalance**: NR
- **Comparator**: Standard clinical parameters (e.g., FEV1) used as reference.
- **Input Variables**: Baseline quantitative CT (qCT) features: imaging lobar volume, airway volume, airway resistance, airway surface, etc.
- **ML Primary Component**: Yes
- **Missing Data Handling**: Scans of poor quality excluded; patients with missing regional parameters were omitted from feature‑selection.
- **Validation Method**: Random training/test splits: 90%/10% for 1‑ and 2‑feature models (500 repetitions), 80%/20% for 3‑feature model (100 repetitions).
- **Methods Notes**: Linear mixed‑effects analysis, Student t tests for individual biomarkers, followed by supervised SVM classification; multiple random partitions used to estimate accuracy.

## Population Characteristics
- **Inclusion criteria**: Status post unilateral or bilateral lung transplantation, availability of at least two chest CTs performed ≥3 months apart, pulmonary function testing within 2 weeks of each CT, and volumetric paired inspiratory and expiratory thin-section CTs
- **Exclusion criteria**: Poor quality CT scans were excluded
- **Sample Size Total**: 71
- **Target Population**: Lung transplant recipients
- **Population Notes**: Retrospective analysis of paired inspiratory‑expiratory CT scans; 41 patients developed BOS and 30 did not; data include baseline and follow‑up imaging and pulmonary function tests
- **Recipient Mean Age**: 57
- **Recipient Mean Age Overall**: 57
- **Recipient Female Sex Pct**: 25.4
- **Recipient Female Sex Pct Overall**: 25.4
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Pre‑transplant diagnoses: idiopathic pulmonary fibrosis (26), chronic obstructive pulmonary disease (23), cystic fibrosis (7), alpha‑1 antitrypsin deficiency (5), other (10)
- **Diagnosis Overall**: Same as Diagnosis
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
- **Specific Algorithm Name**: Support Vector Machine (SVM) with radial basis function kernel
- **Intervention Input Data Modality**: Quantitative CT (qCT) features from paired inspiratory‑expiratory scans
- **Number of Predictors**: Three qCT parameters used in the final model
- **Feature Selection Method**: Student t test to identify significant baseline features, then SVM classification
- **Temporal Handling**: Baseline (static) prediction of eventual BOS development
- **Interventions Notes**: SVM models optimized for accuracy; training‑test split of 80%‑20% for three‑feature model, default cost=1 and gamma=1/number of features
- **Reported outcomes in study**: Prediction of eventual bronchiolitis obliterans syndrome (BOS) development
- **Outcomes Notes**: Accuracy, sensitivity and specificity reported for SVM classifier
- **Result data Notes**: Focus on SVM performance in classifying BOS developers vs non‑developers
- **Primary Outcome Reported name**: BOS development prediction
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: NR
- **Primary Outcome Reported as**: Accuracy (with sensitivity and specificity)
- **Primary Outcome Reference arm**: NR
- **Primary Outcome group**: Baseline lung transplant patients with complete qCT data (n=41)
- **Primary Outcome Reporting**: Accuracy 85%, Sensitivity 73.3%, Specificity 92.3%
- **Primary Outcome Point Estimate**: 0.85
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: Approximately 8–9 patients (20% of 41) used as test set; total cohort n=41
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Proportion of correctly classified cases (accuracy) on held‑out test set
- **Primary Outcome Timepoints**: Baseline prediction (no follow‑up timepoint)
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: ML using three baseline qCT features predicts eventual BOS with high accuracy
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
