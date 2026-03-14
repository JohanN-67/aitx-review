# Data Extraction Report: Rodriguez et al. - 2022 - A Framework for Using Real-World Data and Health Outcomes Modeling to Evaluate Machine Learning-Base
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult lung transplant candidates using a machine‑learning risk model versus usual care, reports survival and transplant outcomes, and is a peer‑reviewed observational analysis published after 2018.

## Identification & Methods
- **Sponsorship source**: NIH
- **Country**: USA
- **Setting**: NR
- **Comments**: Framework using real-world longitudinal data to evaluate a machine‑learning lung‑transplant referral risk model in cystic fibrosis.
- **Author_name**: Patricia J. Rodriguez
- **Institution**: The Comparative Health Outcomes, Policy & Economics (CHOICE) Institute, University of Washington
- **Email**: prodrig@uw.edu
- **Address**: 1959 NE Pacific St, HSB H-375, Box 357630, Seattle, WA 98195-7630, USA
- **Country of Data Origin**: USA
- **Dataset Source**: Cystic Fibrosis Foundation Patient Registry linked with UNOS data
- **Organ Focus**: Lung
- **Study Period End**: 2016
- **Study Period Start**: 2012
- **Identification Notes**: Adults ≥18 years, not transplanted by Jan 1 2012, with at least one encounter in 2011 and 2012; validation cohort n=4247.
- **Design**: Patient‑level microsimulation model using retrospective registry data
- **AI Model Architecture**: Super learner ensemble (lasso, elastic net, ridge, XGBoost, random forest, support vector machine)
- **Class Imbalance**: NR
- **Comparator**: FEV1‑based referral policy and usual care (heterogeneous clinical practice)
- **Input Variables**: Demographics, lung function (FEV1), ML‑predicted 2‑year mortality risk, visit history, covariates from CFFPR (e.g., BMI, diabetes), organ allocation scores
- **ML Primary Component**: Yes
- **Missing Data Handling**: Imputation using linear mixed‑effects models and multiple imputation for longitudinal biomarkers and LAS values
- **Validation Method**: 60/40 training‑validation split; 40% validation set (n=4247) used in 1000 simulation runs
- **Methods Notes**: Plasmode simulation to resample observed data, dynamic decision making at each encounter, organ allocation modeled with UNOS flow and LAS imputation, survival modeled with exponential time‑varying covariate model.

## Population Characteristics
- **Inclusion criteria**: Adults (≥18 years) with cystic fibrosis not undergone lung transplant by Jan 1, 2012 and at least one encounter in both 2011 and 2012
- **Exclusion criteria**: NR
- **Sample Size Total**: 4247
- **Target Population**: Adults with cystic fibrosis (CF) in the CFFPR cohort
- **Population Notes**: Validation set of 4247 patients used for patient-level simulation; linked to UNOS data
- **Recipient Mean Age**: 33 (mean age at referral, range 32.1‑34.4)
- **Recipient Mean Age Overall**: NR
- **Recipient Female Sex Pct**: NR
- **Recipient Female Sex Pct Overall**: NR
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Cystic fibrosis
- **Diagnosis Overall**: Cystic fibrosis
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
- **Specific Algorithm Name**: Super learner ensemble (lasso, elastic net, ridge, XGBoost, random forest, support vector machine)
- **Intervention Input Data Modality**: Longitudinal real-world clinical registry data (demographics, lung function, encounters, biomarkers)
- **Number of Predictors**: NR
- **Feature Selection Method**: NR
- **Temporal Handling**: Dynamic decision making with risk predictions updated at each clinic visit
- **Interventions Notes**: Referral policies compared: ML-based risk threshold (95% specificity), FEV1 <30% criterion, and usual care derived from observed referral patterns
- **Reported outcomes in study**: 5-year overall survival, number of pretransplant deaths, number of post-transplant deaths, referral rates
- **Outcomes Notes**: No significant differences in overall 5-year survival across policies despite different referral rates
- **Result data Notes**: Simulation results presented as mean years survived with 95% confidence intervals
- **Primary Outcome Reported name**: 5-year overall survival
- **Primary Outcome type**: Survival (time-to-event)
- **Primary Outcome Reported against**: Usual care and FEV1-based reference policies
- **Primary Outcome Reported as**: Mean years survived over 5-year horizon
- **Primary Outcome Reference arm**: Usual care (4.73 years, 95% CI 4.70-4.76)
- **Primary Outcome group**: All patients in the validation cohort (n=4247) simulated over 5 years
- **Primary Outcome Reporting**: 4.75 (4.72-4.77) years
- **Primary Outcome Point Estimate**: 4.75
- **Primary Outcome 95 CI Lower**: 4.72
- **Primary Outcome 95 CI Upper**: 4.77
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 4247
- **Primary Outcome Threshold**: Risk threshold corresponding to 95% specificity of the ML model
- **Primary Outcome Metric Definition**: Mean years survived during the 5-year simulation horizon
- **Primary Outcome Timepoints**: 5 years post‑referral
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Differences in referral timing did not translate into survival benefit due to fixed organ supply
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
