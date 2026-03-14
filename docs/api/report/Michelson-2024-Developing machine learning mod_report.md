# Data Extraction Report: Michelson-2024-Developing machine learning mod
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study uses non‑linear machine learning models on adult lung transplant recipients to predict primary graft dysfunction, an important post‑transplant complication, and is a peer‑reviewed article published after 2018.

## Identification & Methods
- **Sponsorship source**: Mid-America Transplant Foundation
- **Country**: USA
- **Setting**: Single-center retrospective cohort study at Washington University School of Medicine, St. Louis
- **Comments**: Retrospective cohort study developing and evaluating machine learning pipelines to predict primary graft dysfunction grade 3 after lung transplantation using donor and recipient variables known at the time of donor offer acceptance.
- **Author_name**: Andrew P. Michelson
- **Institution**: Washington University School of Medicine
- **Email**: rhachem@wustl.edu
- **Address**: 4523 Clayton Ave., Mailstop 8052-0043-14, St. Louis, MO 63110
- **Country of Data Origin**: USA
- **Dataset Source**: UNOS registry, UNet donor portal, and local electronic health record (Epic)
- **Organ Focus**: Lung
- **Study Period Start**: 2010-01-01
- **Study Period End**: 2019-12-31
- **Identification Notes**: All adult (≥18 years) bilateral lung transplant recipients at the center between Jan 1, 2010 and Dec 31, 2019; excluded combined organ transplants and single lung transplants.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Logistic Regression, K-Nearest Neighbors, Extreme Gradient Boosting (XGB), Support Vector Classifier (SVC) with lasso regression for feature selection
- **Class Imbalance**: NR
- **Comparator**: Standard logistic regression model used as baseline comparator
- **Input Variables**: Pre‑transplant donor and recipient variables from UNOS/UNet and local EHR including demographics, laboratory values, vital signs, ventilator parameters, donor chest trauma, LAS, ICU admission, etc.
- **ML Primary Component**: Yes
- **Missing Data Handling**: Median imputation for continuous variables and mode imputation for binary variables
- **Validation Method**: 75%/25% train‑test split, 5‑fold cross‑validation for hyperparameter tuning, random grid search optimizing log loss, and 50‑iteration bootstrap analysis
- **Methods Notes**: Lasso regression used for feature reduction (AIC selection); hyperparameters optimized via random grid search; model calibration performed with sigmoid calibration; compliance with TRIPOD statement; performance evaluated using AUROC, AUPRC, F1 score.

## Population Characteristics
- **Inclusion criteria**: Adult (≥18 years) bilateral lung transplant recipients between Jan 1, 2010 and Dec 31, 2019 who consented to the Lung Transplant Registry
- **Exclusion criteria**: Combined organ transplants (e.g., lung‑liver, heart‑lung) and single lung transplants
- **Sample Size Total**: 576
- **Target Population**: Recipients of bilateral lung transplantation
- **Population Notes**: Single‑center retrospective cohort; data split 75% train / 25% test for machine‑learning model development
- **Recipient Mean Age**: 59
- **Recipient Mean Age Overall**: 59
- **Recipient Female Sex Pct**: 41.15
- **Recipient Female Sex Pct Overall**: 41.15
- **Mean BMI**: 24.5
- **Mean BMI Overall**: 24.5
- **Diagnosis**: Interstitial lung disease (46.9% of recipients)
- **Diagnosis Overall**: Interstitial lung disease (46.9% of recipients)
- **Diabetes Pct**: NR
- **Diabetes Pct Overall**: NR
- **Pre-transplant Support**: ICU admission pre‑transplant (6.25% of recipients)
- **Pre-transplant Support Overall**: ICU admission pre‑transplant (6.25% of recipients)
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: 33
- **Donor Mean Age Overall**: 33
- **Ischemic Time**: NR
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: K-nearest neighbors (KNN)
- **Intervention Input Data Modality**: Tabular clinical variables from donor and recipient (UNOS, UNet, local EHR)
- **Number of Predictors**: 11 selected features
- **Feature Selection Method**: Lasso regression
- **Temporal Handling**: Static baseline data (pre‑transplant variables)
- **Interventions Notes**: Hyperparameter optimization with 5‑fold cross‑validation and random grid search; model calibrated using sigmoid calibration; final KNN model selected for deployment
- **Reported outcomes in study**: Primary graft dysfunction (PGD) grade 3 within first 72 hours post‑transplant
- **Outcomes Notes**: Binary classification outcome
- **Result data Notes**: KNN calibrated model achieved AUROC 0.65 with relatively small confidence intervals; selected as final predictive tool
- **Primary Outcome Reported name**: PGD grade 3 within 72 hours
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: NR
- **Primary Outcome Reported as**: Area under the receiver operating characteristic curve (AUROC)
- **Primary Outcome Reference arm**: NR
- **Primary Outcome group**: All bilateral lung transplant recipients (n=576)
- **Primary Outcome Reporting**: AUROC 0.65
- **Primary Outcome Point Estimate**: 0.65
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: AUROC calculated on held‑out test set
- **Primary Outcome Timepoints**: Within 72 hours post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: KNN calibrated model chosen for website implementation; performance modest with AUROC ~0.65
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
