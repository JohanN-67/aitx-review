# Data Extraction Report: Johnston et al. - 2025 - Estimating Calibrated Risks Using Focal Loss and Gradient-Boosted Trees for Clinical Risk Prediction
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study uses gradient‑boosted decision trees (a non‑linear AI model) to predict post‑lung transplant cancer risk in adult recipients, includes relevant outcomes, and is a peer‑reviewed article published after 2018.

## Identification & Methods
- **Sponsorship source**: NR
- **Country**: USA
- **Setting**: NR
- **Comments**: Retrospective analysis of SRTR lung transplant and BRFSS diabetes datasets using calibrated focal-loss GBDT models.
- **Author_name**: Henry Johnston; Nandini Nair; Dongping Du
- **Institution**: Department of Industrial, Manufacturing, and Systems Engineering, Texas Tech University; Heart and Vascular Institute, Pennsylvania State University College of Medicine
- **Email**: henry.johnston@ttu.edu; nnair@pennstatehealth.psu.edu; dongping.du@ttu.edu
- **Address**: Lubbock, TX 79409, USA; Hershey, PA 17033, USA
- **Country of Data Origin**: USA
- **Dataset Source**: Scientific Registry of Transplant Recipients (SRTR); Behavioral Risk Factor Surveillance System (BRFSS)
- **Organ Focus**: Lung
- **Study Period End**: 2020
- **Study Period Start**: 1988
- **Identification Notes**: Included lung transplant recipients ≥18 years, excluded retransplantation, missing follow‑up, and unknown cancer status; diabetes cohort from 2015 BRFSS survey.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Gradient‑Boosted Decision Trees (XGBoost, LightGBM) with focal loss and Ψγ calibration
- **Class Imbalance**: NR
- **Comparator**: Standard XGBoost with cross‑entropy loss; logistic regression (unregularized, LASSO, ridge); Platt scaling and isotonic regression calibrations
- **Input Variables**: 54 features including demographics, immunosuppression, viral infections, HLA types for lung transplant; 21 survey variables for diabetes
- **ML Primary Component**: Yes
- **Missing Data Handling**: Median imputation for numeric features and mode imputation for categorical features
- **Validation Method**: 10‑fold cross‑validation with Bayesian hyperparameter optimization (SMBO)
- **Methods Notes**: Bayesian hyperparameter tuning of GBDT; Ψγ closed‑form transformation for calibration; decision‑threshold optimization to maximize balanced accuracy

## Population Characteristics
- **Inclusion criteria**: Lung transplant recipients from SRTR, age ≥18 years
- **Exclusion criteria**: Retransplantation, patients under 18 years, without follow-up records, unknown cancer status
- **Sample Size Total**: 33244
- **Target Population**: Lung transplant recipients
- **Population Notes**: Dataset split into 70% training and 30% testing sets
- **Recipient Mean Age**: 54.81
- **Recipient Mean Age Overall**: 54.81
- **Recipient Female Sex Pct**: 43.3
- **Recipient Female Sex Pct Overall**: 43.3
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Post‑transplant lymphoproliferative disorder (PTLD)
- **Diagnosis Overall**: NR
- **Diabetes Pct**: 2.96
- **Diabetes Pct Overall**: 2.96
- **Pre-transplant Support**: NR
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: 33.73
- **Donor Mean Age Overall**: 33.73
- **Ischemic Time**: NR
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: XGBoost, LightGBM
- **Intervention Input Data Modality**: Tabular clinical variables (demographics, medical history, transplant data, survey responses)
- **Number of Predictors**: 54 features for PTLD prediction; 21 features for diabetes prediction
- **Feature Selection Method**: NR
- **Temporal Handling**: Static baseline data (risk prediction at fixed time horizons)
- **Interventions Notes**: Bayesian hyperparameter optimization to select focal loss parameter; Ψγ transformation applied to calibrate confidence scores of GBDT trained with focal loss
- **Reported outcomes in study**: Post‑transplant cancer risk (PTLD) at 1, 3, 5, 8 and 10 years; diabetes status prediction
- **Outcomes Notes**: Metrics include AUROC, H‑measure, average precision, Brier score, calibration slope and intercept; balanced accuracy evaluated with prevalence‑based threshold
- **Result data Notes**: Calibrated focal‑aware XGBoost achieved AUROC 0.700, Brier score 0.128 and calibration slope 0.968 for 10‑year cancer risk, improving calibration while preserving discrimination
- **Primary Outcome Reported name**: 10‑year post‑transplant cancer risk (PTLD)
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Standard XGBoost trained with cross‑entropy loss
- **Primary Outcome Reported as**: AUROC, Brier score and calibration slope
- **Primary Outcome Reference arm**: Standard XGBoost AUROC 0.736 for 10‑year cancer risk
- **Primary Outcome group**: Lung transplant recipients in the SRTR dataset
- **Primary Outcome Reporting**: AUROC 0.700, Brier score 0.128, calibration slope 0.968
- **Primary Outcome Point Estimate**: 0.700
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: AUROC on a completely held‑out test cohort; Brier score as overall accuracy metric
- **Primary Outcome Timepoints**: 10 years post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: 10 years
- **Primary Outcome Notes**: Calibration improved markedly after Ψγ transformation while AUROC remained unchanged
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: 0.700
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
