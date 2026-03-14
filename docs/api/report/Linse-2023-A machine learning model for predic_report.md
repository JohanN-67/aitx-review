# Data Extraction Report: Linse-2023-A machine learning model for predic
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study uses a non‑linear artificial neural network to predict 30‑day graft failure in adult heart transplant recipients, meeting population, AI intervention, outcome, and publication criteria.

## Identification & Methods
- **Sponsorship source**: Swedish Research Council, Vinnova, Swedish Heart-Lung Foundation, region Skane research funds, donation funds from Skane University Hospital, Anna-Lisa and Sven Eric Lundgrens Foundation
- **Country**: Sweden
- **Setting**: NR
- **Comments**: Retrospective analysis of the ISHLT Heart Transplant Registry with internal validation using nested cross‑validation.
- **Author_name**: Johan Nilsson
- **Institution**: Lund University, Sweden
- **Email**: johan.nilsson@med.lu.se
- **Address**: NR
- **Country of Data Origin**: NR
- **Dataset Source**: International Society for Heart and Lung Transplantation (ISHLT) Heart Transplant Registry
- **Organ Focus**: Heart
- **Study Period End**: 2013
- **Study Period Start**: 1994
- **Identification Notes**: Included adult heart transplant recipients (age ≥18) from the ISHLT registry between 1994‑2013; excluded pediatric cases and records with incomplete mandatory data.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Fully connected artificial neural network (multilayer perceptron) with up to three hidden layers, ReLU or tanh activation, sigmoid output.
- **Class Imbalance**: Dataset highly imbalanced (~3% events); weighted error function applied during training.
- **Comparator**: Logistic regression (0 hidden layer MLP) and RADIAL risk score model.
- **Input Variables**: 77 candidate recipient‑donor variables (33 selected as relevant); after dichotomization total of 83 variables used in modeling.
- **ML Primary Component**: Yes
- **Missing Data Handling**: Multiple probability imputation (MPI) during training and mean imputation (MI) during validation; also simple mean imputation with extra category for categorical variables.
- **Validation Method**: Internal validation using nested stratified 5‑fold cross‑validation (outer test loop and inner model‑selection loop) plus an independent internal validation cohort.
- **Methods Notes**: Weighted loss to address class imbalance, stratified 5‑fold CV, random search for hyperparameter tuning, normalization of continuous variables, one‑hot encoding of categorical variables, and evaluation with AUROC.

## Population Characteristics
- **Inclusion criteria**: Adult heart transplant recipients transplanted between January 1, 1994 and December 31, 2013 from the ISHLT registry
- **Exclusion criteria**: Pediatric recipients (<18 years), donor age <15 years, and cases with incomplete mandatory data (diagnosis, blood group, age, gender, follow‑up duration, cause of death)
- **Sample Size Total**: 64,964
- **Target Population**: Heart transplant recipients
- **Population Notes**: Patients were randomly divided into derivation and independent internal validation cohorts
- **Recipient Mean Age**: 51.4
- **Recipient Mean Age Overall**: 51.4
- **Recipient Female Sex Pct**: 22
- **Recipient Female Sex Pct Overall**: 22
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Non‑ischemic cardiomyopathy most common (48.8% of recipients)
- **Diagnosis Overall**: Non‑ischemic cardiomyopathy most common (48.8%)
- **Diabetes Pct**: 1.7
- **Diabetes Pct Overall**: 1.7
- **Pre-transplant Support**: Inotropic support pre‑transplant 46.4%
- **Pre-transplant Support Overall**: Inotropic support pre‑transplant 46.4%
- **Mean Creatinine**: 1.4
- **Mean Creatinine Overall**: 1.4
- **Donor Mean Age**: 34.1
- **Donor Mean Age Overall**: 34.1
- **Ischemic Time**: 189 minutes
- **Ischemic Time Overall**: 189 minutes

## Interventions & Outcomes
- **Specific Algorithm Name**: Artificial Neural Network (ANN)
- **Intervention Input Data Modality**: Tabular clinical donor‑recipient variables from ISHLT registry
- **Number of Predictors**: 33 selected risk variables (out of 77 available)
- **Feature Selection Method**: NR
- **Temporal Handling**: Static baseline data at time of transplantation
- **Interventions Notes**: Fully connected MLP with up to three hidden layers, random search hyper‑parameter optimization, stratified 5‑fold nested cross‑validation, weighted loss for class imbalance, multiple imputation and mean imputation strategies evaluated
- **Reported outcomes in study**: 30‑day primary graft failure (PGF)
- **Outcomes Notes**: Primary endpoint defined as death within 30 days due to graft failure, cardiovascular causes or retransplantation for non‑rejection reasons
- **Result data Notes**: ANN model achieved AUROC ≈0.69 (95 % CI 0.67–0.71) on independent test sets, outperforming logistic regression and RADIAL score
- **Primary Outcome Reported name**: 30‑day primary graft failure
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Logistic regression (baseline) and RADIAL score
- **Primary Outcome Reported as**: Area under the receiver operating characteristic curve (AUROC)
- **Primary Outcome Reference arm**: Logistic regression AUROC ≈0.66 (validation) / 0.67 (test)
- **Primary Outcome group**: All adult heart transplant recipients in the ISHLT registry cohort
- **Primary Outcome Reporting**: AUROC 0.69 (95 % CI 0.67–0.71)
- **Primary Outcome Point Estimate**: 0.69
- **Primary Outcome 95 CI Lower**: 0.67
- **Primary Outcome 95 CI Upper**: 0.71
- **Primary Outcome p-value**: <0.001
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: AUROC calculated on a completely held‑out test cohort using nested cross‑validation
- **Primary Outcome Timepoints**: 30 days post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Good discrimination (AUROC ≈0.69) superior to RADIAL model; performance limited by missing data and registry nature
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.69
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
