# Data Extraction Report: Kainuma et al. - 2022 - Predictors of 1-year outcome after cardiac re-transplantation Machine learning analysis
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult heart retransplant recipients using random survival forests (a non‑linear machine learning model) to predict 1‑year mortality, meeting all population, intervention, outcome, and study design criteria.

## Identification & Methods
- **Sponsorship source**: NR
- **Country**: USA
- **Setting**: NR
- **Comments**: Retrospective review of United Network for Organ Sharing (UNOS) registry data.
- **Author_name**: Atsushi Kainuma
- **Institution**: Columbia University Medical Center, Division of Cardiothoracic Surgery, Department of Surgery
- **Email**: kt2485@cumc.columbia.edu
- **Address**: 177 Fort Washington Avenue, New York, NY 10032, USA
- **Country of Data Origin**: USA
- **Dataset Source**: UNOS registry
- **Organ Focus**: Heart
- **Study Period End**: March 2020
- **Study Period Start**: January 2000
- **Identification Notes**: Included all adult (>17 years old) cardiac re‑transplant recipients identified in the UNOS registry.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Random survival forests (random forest algorithm applied to Cox modeling)
- **Class Imbalance**: NR
- **Comparator**: NR
- **Input Variables**: Recipient variables (age, gender, BMI, ethnicity, number of prior transplants, malignancy history, smoking, diabetes, creatinine, dialysis after listing, total bilirubin, transfusion need, ECMO, IABP, LVAD, TAH, ventilator dependence, inotrope use, PCWP, PVR, PRA, functional status, ICU stay) and donor variables (age, gender, BMI, donor risk index, BUN/creatinine, ethnicity, hepatitis C status, CDC high‑risk donor, drug use, ejection fraction, hypertension, diabetes, smoking history, ischemic time, race/size mismatch).
- **ML Primary Component**: Yes
- **Missing Data Handling**: Variables with >10% missing data were excluded from the machine‑learning analysis.
- **Validation Method**: NR
- **Methods Notes**: Analysis performed using the R package RandomForestSRC; variable importance (VIMP) calculated; complementary multivariable Cox regression performed for verification.

## Population Characteristics
- **Inclusion criteria**: Adult (>17 years) cardiac re-transplant recipients
- **Exclusion criteria**: NR
- **Sample Size Total**: 1294
- **Target Population**: Recipients of cardiac re-transplantation
- **Population Notes**: Cohort divided into early retransplant (≤1 year, n=137) and late retransplant (>1 year, n=1157)
- **Recipient Mean Age**: 45
- **Recipient Mean Age Overall**: 45
- **Recipient Female Sex Pct**: 35.5
- **Recipient Female Sex Pct Overall**: 35.5
- **Mean BMI**: 25.8
- **Mean BMI Overall**: 25.8
- **Diagnosis**: NR
- **Diagnosis Overall**: NR
- **Diabetes Pct**: 24.6
- **Diabetes Pct Overall**: 24.6
- **Pre-transplant Support**: LVAD 2.8%, ECMO 5.6%, IABP 9.7%, ventilator dependence 8.1%
- **Pre-transplant Support Overall**: LVAD 2.8%, ECMO 5.6%, IABP 9.7%, ventilator dependence 8.1%
- **Mean Creatinine**: 1.5
- **Mean Creatinine Overall**: 1.5
- **Donor Mean Age**: 30
- **Donor Mean Age Overall**: 30
- **Ischemic Time**: 3.3 h
- **Ischemic Time Overall**: 3.3 h

## Interventions & Outcomes
- **Specific Algorithm Name**: Random survival forests (RSF) with Cox modeling
- **Intervention Input Data Modality**: Clinical variables from UNOS registry (demographics, labs, device use, donor characteristics)
- **Number of Predictors**: NR
- **Feature Selection Method**: Variable importance (VIMP) ranking from random forests
- **Temporal Handling**: Static baseline data at time of retransplantation
- **Interventions Notes**: Random forest algorithm on Cox modeling used to calculate variable importance for 1-year mortality
- **Reported outcomes in study**: 1-year mortality, 30-day mortality, stroke, need for dialysis, length of stay
- **Outcomes Notes**: Primary focus on 1-year mortality after cardiac retransplantation
- **Result data Notes**: Machine learning identified total bilirubin, BMI, and ventilator dependence as key predictors
- **Primary Outcome Reported name**: 1-year mortality
- **Primary Outcome type**: Survival (time-to-event)
- **Primary Outcome Reported against**: NR
- **Primary Outcome Reported as**: Mortality proportion (percentage)
- **Primary Outcome Reference arm**: NR
- **Primary Outcome group**: All cardiac retransplant recipients (N=1294)
- **Primary Outcome Reporting**: Overall 1-year mortality 16.0% (55/137 early = 40.6%, 152/1157 late = 13.6%)
- **Primary Outcome Point Estimate**: 0.16
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: <0.001
- **Primary Outcome Test Set Size**: 1294
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Proportion of patients dying within one year post‑retransplant
- **Primary Outcome Timepoints**: 1 year post-transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Higher mortality in early retransplantation (≤1 year) vs late (>1 year); bilirubin >2 mg/dL, BMI >30 kg/m² and ventilator dependence identified as risk factors
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
