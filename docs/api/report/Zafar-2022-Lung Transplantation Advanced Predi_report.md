# Data Extraction Report: Zafar-2022-Lung Transplantation Advanced Predi
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Requires Human Review (Rejected by LLM)

## Eligibility
- **Eligibility Status**: Not Accepted
- **Eligibility Rationale**: The study employs Cox‑Lasso, a penalized linear regression model rather than a non‑linear AI method, which does not meet the inclusion criterion for an AI component.

## Identification & Methods
- **Sponsorship source**: NIH
- **Country**: USA
- **Setting**: NR
- **Comments**: Retrospective cohort study using UNOS registry data to develop and validate a lung transplantation risk scoring tool.
- **Author_name**: Farhan Zafar, MD
- **Institution**: Cincinnati Children’s Hospital Medical Center
- **Email**: farhan.zafar@cchmc.org
- **Address**: 3333 Burnet Ave, Cincinnati, OH 45229
- **Country of Data Origin**: USA
- **Dataset Source**: UNOS (United Network for Organ Sharing) registry
- **Organ Focus**: Lung
- **Study Period End**: 2020
- **Study Period Start**: 2005
- **Identification Notes**: Included double lung transplant recipients aged ≥12 years from UNOS (2005–2020); excluded retransplantations, simultaneous solid organ transplants, and cases with missing post‑transplant survival status.
- **Design**: Retrospective Cohort (derivation and validation cohorts)
- **AI Model Architecture**: Cox‑Lasso regression; compared with random forest Cox and backward elimination Cox models
- **Class Imbalance**: NR
- **Comparator**: Cox regression with backward elimination and random forest Cox models
- **Input Variables**: 42 recipient, donor, and transplant variables (e.g., age, race, BMI, LAS, diagnosis, KPS, eGFR, albumin, tobacco use, steroid use, ECMO, ventilation, donor age/race/tobacco/diabetes, CMV mismatch, ischemia time)
- **ML Primary Component**: Yes
- **Missing Data Handling**: Single missing data points imputed separately for recipient and donor variables; records with multiple missing values excluded
- **Validation Method**: 70/30 split into derivation (n=10,660) and validation (n=4,464) cohorts; external validation of risk clusters using EM clustering and Kaplan‑Meier survival analysis
- **Methods Notes**: Lasso used for variable selection; Cox proportional hazards modeling; expectation‑maximization clustering to define risk groups; web‑based tool developed for clinical use

## Population Characteristics
- **Inclusion criteria**: Double lung transplant recipients aged ≥12 years from UNOS registry 2005–2020
- **Exclusion criteria**: Retransplantations, simultaneous other solid organ transplants, missing post‑transplant survival status
- **Sample Size Total**: 15124
- **Target Population**: Lung transplant recipients (double lung)
- **Population Notes**: Derivation cohort n=10660 (70%); Validation cohort n=4464 (30%)
- **Recipient Mean Age**: 57
- **Recipient Mean Age Overall**: NR
- **Recipient Female Sex Pct**: 41.4% (validation) / 42.7% (derivation)
- **Recipient Female Sex Pct Overall**: NR
- **Mean BMI**: 25.3 (validation) / 25.0 (derivation)
- **Mean BMI Overall**: NR
- **Diagnosis**: Obstructive 28.2%, Pulmonary vascular 4.9%, Cystic fibrosis 16.3%, Restrictive 50.6% (validation)
- **Diagnosis Overall**: NR
- **Diabetes Pct**: 6.9% (validation) / 7.4% (derivation) donor diabetes
- **Diabetes Pct Overall**: NR
- **Pre-transplant Support**: ECMO 5.4% (validation) / 5.1% (derivation); Ventilation ~6% (both cohorts)
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: 32
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: 5.48 h median
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: Cox-Lasso regression
- **Intervention Input Data Modality**: UNOS registry clinical variables (recipient, donor, transplant factors)
- **Number of Predictors**: 19 selected predictors (13 recipient, 4 donor, 2 transplant variables)
- **Feature Selection Method**: Lasso (penalized regression) for variable selection
- **Temporal Handling**: Static baseline data at time of transplant
- **Interventions Notes**: Web‑based tool; expectation‑maximization clustering into low, medium, high risk groups
- **Reported outcomes in study**: 1‑year, 5‑year and 10‑year survival probabilities / mortality rates
- **Outcomes Notes**: Includes short‑, medium‑ and long‑term survival; model provides estimated vs observed rates
- **Result data Notes**: C statistics (AUC) for mortality prediction: 0.67 (1‑yr), 0.64 (5‑yr), 0.72 (10‑yr); model‑estimated survival closely matches observed in validation cohort
- **Primary Outcome Reported name**: 1‑year mortality
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Low‑risk group (reference)
- **Primary Outcome Reported as**: C statistic (AUC)
- **Primary Outcome Reference arm**: Low‑risk group
- **Primary Outcome group**: All double lung transplant recipients in validation cohort
- **Primary Outcome Reporting**: C statistic = 0.67
- **Primary Outcome Point Estimate**: 0.67
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 4464
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Area under the ROC curve for predicting 1‑year mortality using adjusted total risk score
- **Primary Outcome Timepoints**: 1 year post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Model also provides 5‑yr and 10‑yr survival estimates with C statistics 0.64 and 0.72
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.67
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
