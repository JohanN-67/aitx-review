# Data Extraction Report: Tian et al. - 2023 - Machine Learning-Based Prognostic Model for Patients After Lung Transplantation
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study involves adult lung transplant recipients and uses a random survival forests machine learning model to predict post‑transplant survival, meeting all population, intervention, outcome, and study design criteria.

## Identification & Methods
- **Sponsorship source**: National Natural Science Foundation of China
- **Country**: China
- **Setting**: Single-center retrospective prognostic study at Wuxi People’s Hospital affiliated to Nanjing Medical University
- **Comments**: Retrospective prognostic study using random survival forests to predict overall survival after lung transplantation
- **Author_name**: Dong Tian
- **Institution**: Wuxi People’s Hospital affiliated to Nanjing Medical University
- **Email**: chenjy@wuxiph.com
- **Address**: Wuxi Lung Transplant Center, Wuxi People’s Hospital affiliated to Nanjing Medical University, 214000 Wuxi, China
- **Country of Data Origin**: China
- **Dataset Source**: Clinical records from Wuxi People’s Hospital (single-center)
- **Organ Focus**: Lung
- **Study Period End**: December 2020
- **Study Period Start**: January 2017
- **Identification Notes**: Included adult patients >18 years who underwent lung transplantation; excluded retransplant, pediatric cases, and those with severe missing data
- **Design**: Retrospective cohort (prognostic) study
- **AI Model Architecture**: Random Survival Forests (RSF)
- **Class Imbalance**: NR
- **Comparator**: Cox regression model (benchmark)
- **Input Variables**: 22 clinical characteristics (4 recipient, 1 donor, 4 procedural, 13 post‑transplant); 16 variables selected for final RSF model
- **ML Primary Component**: Yes
- **Missing Data Handling**: Multiple imputation by chained equations using the ‘mice’ R package
- **Validation Method**: Hold‑out validation with 7:3 train‑test split; internal test set and subgroup analyses
- **Methods Notes**: Feature selection via variable importance with bootstrapping (1000 repetitions); hyperparameter tuning by grid search; performance assessed using integrated AUC, integrated Brier score, and calibration; internal validation on test set and subgroup validation

## Population Characteristics
- **Inclusion criteria**: Adult patients (>18 years) who underwent lung transplantation between January 2017 and December 2020 with complete follow-up records
- **Exclusion criteria**: Retransplantation (6 patients), pediatric lung transplant (7 patients), severe missing data (6 patients)
- **Sample Size Total**: 504
- **Target Population**: Lung transplant recipients
- **Population Notes**: Patients randomly assigned to training (353) and test (151) sets in a 7:3 ratio; both single and double lung transplants included
- **Recipient Mean Age**: 55.6
- **Recipient Mean Age Overall**: 55.6
- **Recipient Female Sex Pct**: 33.7
- **Recipient Female Sex Pct Overall**: 33.7
- **Mean BMI**: 20.54
- **Mean BMI Overall**: 20.54
- **Diagnosis**: Interstitial pulmonary fibrosis (most common)
- **Diagnosis Overall**: Interstitial pulmonary fibrosis (most common)
- **Diabetes Pct**: NR
- **Diabetes Pct Overall**: NR
- **Pre-transplant Support**: NR
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: NR
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: 7.58 hours (cold‑ischemia time)
- **Ischemic Time Overall**: 7.58 hours (cold‑ischemia time)

## Interventions & Outcomes
- **Specific Algorithm Name**: Random Survival Forests (RSF)
- **Intervention Input Data Modality**: Tabular clinical variables (22 pre- and post-transplant characteristics)
- **Number of Predictors**: 16 selected predictors
- **Feature Selection Method**: Variable importance (VIMP) with bootstrapping resampling
- **Temporal Handling**: Static baseline data used for time-to-event prediction
- **Interventions Notes**: Grid search hyperparameter tuning; bootstrapping for VIMP; internal validation with hold‑out test set
- **Reported outcomes in study**: Overall survival, 1‑month survival, 1‑year survival
- **Outcomes Notes**: Primary outcome was overall survival; secondary time‑point predictions at 1 month and 1 year
- **Result data Notes**: Focus on RSF performance versus Cox regression benchmark
- **Primary Outcome Reported name**: Overall survival
- **Primary Outcome type**: Survival (time‑to‑event)
- **Primary Outcome Reported against**: Cox regression model
- **Primary Outcome Reported as**: Integrated area under the curve (iAUC) and integrated Brier score (iBS)
- **Primary Outcome Reference arm**: Cox regression iAUC 0.658 (95% CI 0.572‑0.747)
- **Primary Outcome group**: All lung transplant recipients in the test set
- **Primary Outcome Reporting**: iAUC 0.879 (95% CI 0.832‑0.921)
- **Primary Outcome Point Estimate**: 0.879
- **Primary Outcome 95 CI Lower**: 0.832
- **Primary Outcome 95 CI Upper**: 0.921
- **Primary Outcome p-value**: <0.001
- **Primary Outcome Test Set Size**: 151
- **Primary Outcome Threshold**: 30.74 (optimal risk‑stratification threshold)
- **Primary Outcome Metric Definition**: Integrated AUC over 1–48 months on held‑out test cohort
- **Primary Outcome Timepoints**: Overall survival up to 48 months
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: RSF outperformed Cox; stratified patients into low‑ and high‑risk groups with mean OS 52.91 months vs 14.83 months
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.921
- **Res_Primary 1Yr Accuracy**: 0.828
- **Res_Primary 1Yr Sens_Spec**: Sensitivity 88.7%, Specificity 79.6%
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
