# Data Extraction Report: Ozcan et al. - 2022 - Artificial intelligence-derived cardiac ageing is associated with cardiac events post-heart transpla
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study involves adult heart transplant recipients, uses a convolutional neural network (non‑linear AI) to predict ECG‑derived age, and evaluates post‑transplant survival/MACE outcomes; it is a peer‑reviewed observational cohort published after 2018.

## Identification & Methods
- **Sponsorship source**: None
- **Country**: USA
- **Setting**: Single-center retrospective cohort at Mayo Clinic, Rochester, MN
- **Comments**: Retrospective single-centre cohort using Mayo HTx database with prospective data collection
- **Author_name**: Amir Lerman
- **Institution**: Mayo Clinic
- **Email**: lerman.amir@mayo.edu
- **Address**: 200 First Street SW, Rochester, MN 55902, USA
- **Country of Data Origin**: USA
- **Dataset Source**: Mayo Clinic heart transplantation database (prospective HTx registry)
- **Organ Focus**: Heart
- **Study Period End**: 2018
- **Study Period Start**: 1990
- **Identification Notes**: Consecutive heart transplant patients with available pre- and post‑transplant ECGs; 540 analyzed
- **Design**: Retrospective cohort
- **AI Model Architecture**: Convolutional neural network (CNN) built in Keras/TensorFlow
- **Class Imbalance**: NR
- **Comparator**: NR
- **Input Variables**: Raw 12‑lead ECG signals (averaged pre‑ and post‑transplant), recipient and donor ages, clinical covariates for multivariable models
- **ML Primary Component**: Yes
- **Missing Data Handling**: NR
- **Validation Method**: NR
- **Methods Notes**: Average ECG age calculated from ECGs within 1 year before and after transplant; Cox proportional hazards models used for outcome analysis

## Population Characteristics
- **Inclusion criteria**: Consecutive cardiac transplant patients who underwent heart transplantation at Mayo Clinic between 1990 and 2018
- **Exclusion criteria**: NR
- **Sample Size Total**: 540
- **Target Population**: Heart transplant recipients
- **Population Notes**: Retrospective single‑centre cohort study using a prospective HTx database; analyses performed on patients with available pre‑ and post‑transplant ECG data
- **Recipient Mean Age**: 49
- **Recipient Mean Age Overall**: 49
- **Recipient Female Sex Pct**: 32
- **Recipient Female Sex Pct Overall**: 32
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Non‑ischemic cardiomyopathy (75% of transplants)
- **Diagnosis Overall**: Non‑ischemic cardiomyopathy (most common etiology)
- **Diabetes Pct**: 22
- **Diabetes Pct Overall**: 22
- **Pre-transplant Support**: NR
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: 32
- **Donor Mean Age Overall**: 32
- **Ischemic Time**: 173 min
- **Ischemic Time Overall**: 173 min

## Interventions & Outcomes
- **Specific Algorithm Name**: Convolutional neural network AI-ECG age algorithm
- **Intervention Input Data Modality**: 12-lead electrocardiogram (ECG)
- **Number of Predictors**: NR
- **Feature Selection Method**: NR
- **Temporal Handling**: Average ECG ages within 1 year before and after transplantation used as pre- and post-transplant values
- **Interventions Notes**: Algorithm applied without additional training; originally trained on >770,000 ECGs using raw 12-lead signals and chronological age as label
- **Reported outcomes in study**: Major adverse cardiovascular events (MACE) – composite of coronary revascularization, heart failure hospitalization, re‑transplantation, and all‑cause mortality
- **Outcomes Notes**: MACE defined as any incident of the listed events; also reported individual components separately
- **Result data Notes**: Increase in ECG age post‑transplant associated with higher risk of MACE (adjusted HR 1.58, 95% CI 1.18–2.10, p=0.002)
- **Primary Outcome Reported name**: Composite major adverse cardiovascular events (MACE)
- **Primary Outcome type**: Time‑to‑event (survival) analysis
- **Primary Outcome Reported against**: Patients with decrease in ECG age post‑transplant (ΔECG age < 0)
- **Primary Outcome Reported as**: Hazard ratio (HR) from Cox proportional hazards model
- **Primary Outcome Reference arm**: ΔECG age < 0 group
- **Primary Outcome group**: All heart transplant recipients with available ECG data (n=540)
- **Primary Outcome Reporting**: Adjusted HR 1.58 (95% CI 1.18–2.10)
- **Primary Outcome Point Estimate**: 1.58
- **Primary Outcome 95 CI Lower**: 1.18
- **Primary Outcome 95 CI Upper**: 2.10
- **Primary Outcome p-value**: 0.002
- **Primary Outcome Test Set Size**: 540
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Hazard ratio derived from multivariable Cox proportional hazards model adjusting for recipient age, donor age, sex, hypertension, diabetes, ischemic cardiomyopathy, CAV grade, HDL‑C, triglycerides, and sirolimus conversion
- **Primary Outcome Timepoints**: Median follow‑up 8.8 years (range 4.9–14.3)
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Patients with increased ECG age after transplant had significantly higher risk of MACE even after adjustment for confounders
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
