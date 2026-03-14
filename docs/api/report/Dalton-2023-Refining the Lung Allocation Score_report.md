# Data Extraction Report: Dalton-2023-Refining the Lung Allocation Score
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult lung transplant candidates and recipients using non‑linear AI models (random survival forests, gradient‑boosted trees) versus the current LAS/CAS standard and reports survival outcomes, meeting all inclusion criteria.

## Identification & Methods
- **Sponsorship source**: National Heart, Lung, and Blood Institute (NHLBI) of the NIH
- **Country**: USA
- **Setting**: Tertiary academic center (Cleveland Clinic)
- **Comments**: Retrospective cohort study using SRTR data to evaluate current LAS/CAS models and alternative statistical/ML approaches for lung transplant waitlist and post‑transplant survival.
- **Author_name**: Maryam Valapour
- **Institution**: Cleveland Clinic
- **Email**: valapom@ccf.org
- **Address**: Cleveland, OH, USA
- **Country of Data Origin**: USA
- **Dataset Source**: Scientific Registry for Transplant Recipients (SRTR)
- **Organ Focus**: Lung
- **Study Period End**: May 18, 2020
- **Study Period Start**: 2010
- **Identification Notes**: Adults ≥18 years, retrospective SRTR data; excluded candidates with missing age, sex, supplemental oxygen or mechanical respiratory support.
- **Design**: Retrospective cohort
- **AI Model Architecture**: Cox proportional hazards (baseline LAS/CAS), re‑estimated Cox, Cox with cubic splines, random survival forests, logistic regression (stacked), linear discriminant analysis, gradient‑boosted trees
- **Class Imbalance**: NR
- **Comparator**: Current lung allocation score (LAS)/Composite Allocation Score (CAS) model
- **Input Variables**: Demographics, clinical variables, laboratory values, and other predictors used in the LAS/CAS models (e.g., age, sex, diagnosis group, ADI, insurance, respiratory support, labs).
- **ML Primary Component**: Yes
- **Missing Data Handling**: Multiple imputation for missing predictors; inverse probability‑of‑censoring weighting used for informative censoring.
- **Validation Method**: 10‑fold cross‑validation (internal validation per TRIPOD guidelines).
- **Methods Notes**: Survival stacking to convert time‑to‑event data for binary ML models; AUC evaluated at multiple time points and across socioeconomic subgroups; TRIPOD‑aligned internal validation.

## Population Characteristics
- **Inclusion criteria**: US lung transplant candidates aged ≥18 years
- **Exclusion criteria**: Missing data on age, sex, supplemental oxygen, or mechanical respiratory support
- **Sample Size Total**: 13,204 waitlist candidates (baseline cohort)
- **Target Population**: Lung transplant candidates and recipients in the United States
- **Population Notes**: Retrospective SRTR data from 2015-2020 for waitlist and 2010-2020 for post‑transplant; candidates listed once, censored at retransplant; includes variables used in LAS/CAS models
- **Recipient Mean Age**: NR
- **Recipient Mean Age Overall**: NR
- **Recipient Female Sex Pct**: 41% (5,442 of 13,204) at baseline
- **Recipient Female Sex Pct Overall**: 41% (5,442 of 13,204) at baseline
- **Mean BMI**: 26.1 (IQR 22.3‑29.3)
- **Mean BMI Overall**: 26.1 (IQR 22.3‑29.3)
- **Diagnosis**: Group A 24%, Group B 5.5%, Group C 8.9%, Group D 61% at baseline waitlist
- **Diagnosis Overall**: Group A 24%, Group B 5.5%, Group C 8.9%, Group D 61% at baseline waitlist
- **Diabetes Pct**: NR
- **Diabetes Pct Overall**: NR
- **Pre-transplant Support**: Mechanical ventilation 5.4%, BiPAP 7.3%, CPAP 6.1%, No support 81% at baseline
- **Pre-transplant Support Overall**: Mechanical ventilation 5.4%, BiPAP 7.3%, CPAP 6.1%, No support 81% at baseline
- **Mean Creatinine**: 0.80 (IQR 0.69‑0.97)
- **Mean Creatinine Overall**: 0.80 (IQR 0.69‑0.97)
- **Donor Mean Age**: NR
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: NR
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: Cox proportional hazards (LAS/CAS), re-estimated Cox, Cox with cubic splines, Random survival forests, Logistic model (stacked survival), Linear discriminant analysis, Gradient boosted tree
- **Intervention Input Data Modality**: SRTR registry clinical variables (demographics, diagnosis, physiologic measures)
- **Number of Predictors**: NR
- **Feature Selection Method**: NR
- **Temporal Handling**: Baseline cohort predictions at 1, 3, and 6 months on waitlist; post‑transplant predictions at 1, 3, and 5 years; survival stacking used to create binary outcomes for machine‑learning models
- **Interventions Notes**: 10‑fold cross‑validation; models trained on contemporary SRTR data (2015‑2020 WL, 2010‑2020 PT); inverse probability of censoring weighting and multiple imputation applied
- **Reported outcomes in study**: Area under the ROC curve (AUC) for waitlist and post‑transplant survival models at multiple time points
- **Outcomes Notes**: Discrimination performance (AUC) was similar across models; no model outperformed the current LAS/CAS; WL AUC ranged 0.84‑0.93, PT AUC ranged 0.58‑0.61
- **Result data Notes**: Alternative statistical and machine‑learning approaches did not improve model discrimination compared with the standard LAS/CAS models
- **Primary Outcome Reported name**: Discrimination (AUC) of waitlist mortality model
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Current LAS/CAS model (Model I)
- **Primary Outcome Reported as**: Area under the ROC curve (AUC)
- **Primary Outcome Reference arm**: Model I – WL‑LAS/CAS baseline model
- **Primary Outcome group**: All lung transplant candidates on the waitlist (baseline cohort)
- **Primary Outcome Reporting**: AUC 0.92 (95% CI 0.88‑0.97) for 1‑month forecasted time
- **Primary Outcome Point Estimate**: 0.92
- **Primary Outcome 95 CI Lower**: 0.88
- **Primary Outcome 95 CI Upper**: 0.97
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Area under the receiver operating characteristic curve for predicting waitlist mortality at specified forecasted times
- **Primary Outcome Timepoints**: 1 month, 3 months, 6 months (waitlist); 1 year, 3 years, 5 years (post‑transplant)
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year (post‑transplant)
- **Primary Outcome Late Reported time**: 5 years (post‑transplant)
- **Primary Outcome Notes**: AUC declined with longer waitlist time; PT models showed poor discrimination (AUC ~0.60) and were not improved by alternative modeling
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.61 (baseline PT model)
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: 0.60 (baseline PT model at 5 years)
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
