# Data Extraction Report: Pelzer-2023-The Accuracy of Initial U.S. Heart
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult heart transplant candidates using a random survival forest (non‑linear AI) to predict waitlist mortality, compares it to the current allocation system, and meets all population, intervention, comparator, outcome, and publication criteria.

## Identification & Methods
- **Sponsorship source**: Hennepin Healthcare Research Institute (contractor for SRTR) and NIH grant K08HL150291
- **Country**: USA
- **Setting**: Observational registry-based retrospective cohort study using national transplant data
- **Comments**: Retrospective analysis of SRTR data to compare the standard 6‑status heart allocation system with Cox proportional hazards and random survival forest models
- **Author_name**: Kenley M. Pelzer
- **Institution**: University of Chicago, Department of Medicine
- **Email**: wparker@uchicago.edu
- **Address**: University of Chicago, 5841 South Maryland Avenue, MC 6076, Chicago, Illinois 60637, USA
- **Country of Data Origin**: USA
- **Dataset Source**: Scientific Registry of Transplant Recipients (SRTR)
- **Organ Focus**: Heart
- **Study Period End**: March 2020
- **Study Period Start**: 2010
- **Identification Notes**: Included adult candidates ≥18 years listed for heart transplantation; excluded heart‑lung candidates, data entry errors, inactive listings, and implausible values
- **Design**: Retrospective cohort (registry) study
- **AI Model Architecture**: Cox proportional hazards model and Random survival forest (RSF)
- **Class Imbalance**: NR
- **Comparator**: Standard 6‑status heart allocation ranking system
- **Input Variables**: Age, diagnosis categories, laboratory measurements (e.g., GFR), hemodynamic parameters (PCWP, mean PAP, cardiac index), supportive treatments (IABP, IV inotropes, ECMO, LVAD, other VAD), blood type, medical history (malignancy, cerebrovascular disease, tobacco use), BMI, diabetes
- **ML Primary Component**: Yes
- **Missing Data Handling**: Multiple imputation by chained equations (mice) for missing values; indicator variables assumed absent for binary conditions
- **Validation Method**: Model development on pre‑policy cohort (Jan 2010–Dec 2017) and external validation on post‑policy cohort (Nov 2018–Mar 2020)
- **Methods Notes**: Harrell's C‑index and log‑rank tests used for performance; variable importance assessed via RSF anti‑method; calibration with Kaplan‑Meier curves and Brier scores; joint variable importance by predictor categories reported

## Population Characteristics
- **Inclusion criteria**: NR
- **Exclusion criteria**: Heart-lung candidates, data entry errors (height <30 cm, BMI >100 kg/m2, creatinine <0.1 mg/dL), inactive listed candidates, missing 6 status, death date preceding listing
- **Sample Size Total**: 32294
- **Target Population**: Adult heart transplant candidates (≥18 years) listed in the US SRTR registry
- **Population Notes**: Training set prepolicy (27,200) and test set postpolicy (5,094); final dataset after exclusions 32,294
- **Recipient Mean Age**: 53.0
- **Recipient Mean Age Overall**: 53.0
- **Recipient Female Sex Pct**: 26.3
- **Recipient Female Sex Pct Overall**: 26.3
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Nonischemic dilated cardiomyopathy most common
- **Diagnosis Overall**: Nonischemic dilated cardiomyopathy most common
- **Diabetes Pct**: 29.9
- **Diabetes Pct Overall**: 29.9
- **Pre-transplant Support**: NR
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: NR
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: NR
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: Cox proportional hazards, Random survival forest
- **Intervention Input Data Modality**: Registry clinical variables from SRTR (demographics, physiologic measurements, treatments, diagnosis, history)
- **Number of Predictors**: NR
- **Feature Selection Method**: NR
- **Temporal Handling**: Static baseline data at listing
- **Interventions Notes**: Developed Cox and RSF models with and without treatment variables; four total models evaluated
- **Reported outcomes in study**: Death before receipt of a heart transplant (waitlist mortality)
- **Outcomes Notes**: Primary outcome defined as death without receiving a transplant, censoring transplantation
- **Result data Notes**: 6-status C-index 0.67 (95% CI 0.63-0.71); CPH with treatment C-index 0.76 (95% CI 0.72-0.79, p<0.001); RSF with treatment C-index 0.74 (95% CI 0.70-0.78, p=0.011)
- **Primary Outcome Reported name**: Death before receipt of heart transplant
- **Primary Outcome type**: Survival (time-to-event)
- **Primary Outcome Reported against**: 6-status ranking system
- **Primary Outcome Reported as**: Harrell’s C-index
- **Primary Outcome Reference arm**: 6-status C-index 0.67 (95% CI 0.63-0.71)
- **Primary Outcome group**: All adult heart transplant candidates in the postpolicy test set
- **Primary Outcome Reporting**: C-index 0.76 (95% CI 0.72-0.79)
- **Primary Outcome Point Estimate**: 0.76
- **Primary Outcome 95 CI Lower**: 0.72
- **Primary Outcome 95 CI Upper**: 0.79
- **Primary Outcome p-value**: <0.001
- **Primary Outcome Test Set Size**: 5,094
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Harrell’s C-index measuring concordance of predicted risk with observed death in the test cohort
- **Primary Outcome Timepoints**: All follow‑up time until death or censoring
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: 6-status ranking showed moderate discrimination; multivariable CPH and RSF models showed higher discrimination
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
