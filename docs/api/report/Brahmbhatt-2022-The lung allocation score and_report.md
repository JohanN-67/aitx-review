# Data Extraction Report: Brahmbhatt-2022-The lung allocation score and
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult lung transplant recipients using non‑linear machine learning models (Random Forests) to predict post‑transplant survival, meeting all population, intervention, outcome, and study design criteria.

## Identification & Methods
- **Sponsorship source**: NR
- **Country**: USA
- **Setting**: Retrospective cohort using national UNOS registry data
- **Comments**: Study evaluated predictive accuracy of LAS and novel models for 1‑year and 3‑year post‑lung transplant mortality using UNOS data.
- **Author_name**: Jay M. Brahmbhatt
- **Institution**: University of Washington, Seattle; Johns Hopkins University School of Medicine, Baltimore
- **Email**: ramoskj@uw.edu
- **Address**: 1959 NE Pacific Street, Box 356522, Seattle, WA 98107
- **Country of Data Origin**: USA
- **Dataset Source**: UNOS (United Network for Organ Sharing) database via OPTN
- **Organ Focus**: Lung
- **Study Period End**: 2017
- **Study Period Start**: 2005
- **Identification Notes**: Included adult patients (≥18 years) receiving first lung transplant between May 1, 2005 and May 1, 2017; excluded lost to follow‑up.
- **Design**: Retrospective cohort
- **AI Model Architecture**: LASSO (Least Absolute Shrinkage and Selection Operator), Random Forests
- **Class Imbalance**: NR
- **Comparator**: Lung Allocation Score (LAS) and Chan et al. model
- **Input Variables**: Pre‑transplant recipient covariates from UNOS (e.g., demographics, pulmonary function, labs, diagnosis) and donor covariates in secondary analyses.
- **ML Primary Component**: Yes
- **Missing Data Handling**: Categorical missing values grouped into a separate category; continuous variables imputed with mean.
- **Validation Method**: Random split: 85% development set, 15% validation set; performance assessed on validation cohort.
- **Methods Notes**: Calibration evaluated by decile plots and calibration slope; models compared using AUC, sensitivity, specificity, PPV, NPV.

## Population Characteristics
- **Inclusion criteria**: Adult patients (≥18 years) who had their first lung transplant between May 1, 2005 and May 1, 2017
- **Exclusion criteria**: NR
- **Sample Size Total**: 19,900
- **Target Population**: Lung transplant recipients
- **Population Notes**: Retrospective cohort from UNOS; data split into 85% development set and 15% validation set
- **Recipient Mean Age**: 55.1 (alive) / 56.5 (died or re‑transplanted)
- **Recipient Mean Age Overall**: NR
- **Recipient Female Sex Pct**: 41% (alive) / 37% (died or re‑transplanted)
- **Recipient Female Sex Pct Overall**: NR
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Idiopathic pulmonary fibrosis (most common, 38% of cohort)
- **Diagnosis Overall**: NR
- **Diabetes Pct**: Approximately 20% (type I 3%, type II 11%, other 4%)
- **Diabetes Pct Overall**: NR
- **Pre-transplant Support**: Mechanical ventilation (5% alive, 11% died), dialysis prior to transplant (<1% each)
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: 0.85 (alive) / 0.90 (died or re‑transplanted)
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: NR
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: NR
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: LAS, Chan et al model, clinician model (27 a priori predictors), LASSO, Random Forests
- **Intervention Input Data Modality**: UNOS registry pre‑transplant recipient covariates (and donor covariates in secondary analyses)
- **Number of Predictors**: LAS uses many registry variables; clinician model uses 27 pre‑selected predictors; LASSO selected a subset of available UNOS variables (≈15–20 listed)
- **Feature Selection Method**: A priori expert selection for clinician model; LASSO shrinkage for LASSO model; variable importance (Gini) for Random Forests
- **Temporal Handling**: Static baseline data at time of transplant
- **Interventions Notes**: Random 85% development set, 15% validation set; logistic regression fitted on selected covariates; calibration assessed by decile plots
- **Reported outcomes in study**: 1‑year mortality (death or re‑transplant), 3‑year mortality, calibration metrics, AUC, sensitivity, specificity, PPV, NPV
- **Outcomes Notes**: Primary outcome was death or re‑transplant within the specified timeframe
- **Result data Notes**: AUC low for all models (0.55–0.62); NPV high (0.87‑0.90); PPV low (<0.25); LAS overestimated risk
- **Primary Outcome Reported name**: 1‑year mortality (death or re‑transplant)
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: LAS, Chan et al model, clinician model, LASSO, Random Forests
- **Primary Outcome Reported as**: Area under the receiver‑operator characteristic curve (AUC)
- **Primary Outcome Reference arm**: LAS AUC ≈0.55
- **Primary Outcome group**: All lung transplant recipients in the validation cohort
- **Primary Outcome Reporting**: AUC range 0.55–0.62 across models
- **Primary Outcome Point Estimate**: NR
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: Cut‑point maximizing combined sensitivity and specificity (Youden index)
- **Primary Outcome Metric Definition**: AUC calculated on a completely held‑out validation set
- **Primary Outcome Timepoints**: 1 year (primary), also evaluated at 3 years
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year post‑transplant
- **Primary Outcome Late Reported time**: 3 years post‑transplant
- **Primary Outcome Notes**: LAS overestimated risk, novel models did not improve prediction; calibration poor for high‑risk patients
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.55–0.62 (range across models)
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
