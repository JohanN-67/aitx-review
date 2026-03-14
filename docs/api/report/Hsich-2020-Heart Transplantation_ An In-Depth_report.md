# Data Extraction Report: Hsich-2020-Heart Transplantation_ An In-Depth
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult heart transplant recipients using random survival forests (a non‑linear machine learning model) to predict post‑transplant survival, meeting all population, intervention, outcome, and study design criteria.

## Identification & Methods
- **Sponsorship source**: NIH grants HL141892 and GM125072; Cystic Fibrosis Foundation
- **Country**: USA
- **Setting**: Retrospective analysis using the US Scientific Registry of Transplant Recipients (SRTR)
- **Comments**: Retrospective cohort study of adult heart transplant recipients analyzing survival phases with parametric temporal decomposition and random survival forests.
- **Author_name**: Eileen M. Hsich, MD
- **Institution**: Cleveland Clinic, Heart and Vascular Institute
- **Email**: Hsiche@ccf.org
- **Address**: J3-4, 9500 Euclid Avenue, Cleveland, Ohio 44195
- **Country of Data Origin**: USA
- **Dataset Source**: Scientific Registry of Transplant Recipients (SRTR)
- **Organ Focus**: Heart
- **Study Period End**: 2018-07-01
- **Study Period Start**: 2004-01-01
- **Identification Notes**: Included all adult (≥18 years) isolated heart transplant recipients in SRTR from Jan 1, 2004 to Jul 1, 2018; excluded multi‑organ transplants and pediatric cases.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Random Survival Forests (RSF) with 500 trees; also parametric temporal decomposition model
- **Class Imbalance**: NR
- **Comparator**: NR
- **Input Variables**: Recipient and donor demographics, clinical characteristics, laboratory values, mechanical circulatory support status, transplant era, insurance type, and other pre‑transplant variables.
- **ML Primary Component**: Yes
- **Missing Data Handling**: Multiple imputation by chained equations for parametric models; missForest imputation for random forest analysis.
- **Validation Method**: NR
- **Methods Notes**: Temporal decomposition identified early, constant, and late hazard phases; RSF used to assess variable importance and interactions across time points (90 days, 1 yr, 5 yr, 10 yr).

## Population Characteristics
- **Inclusion criteria**: All adults in the SRTR who underwent isolated heart transplantation from January 1, 2004 to July 1, 2018
- **Exclusion criteria**: Recipients of multi-organ transplants and recipients <18 years of age
- **Sample Size Total**: 30606
- **Target Population**: Adult heart transplant recipients
- **Population Notes**: Final cohort of 30,606 adult transplants after exclusions; median follow‑up 3.9 years
- **Recipient Mean Age**: 56
- **Recipient Mean Age Overall**: 56
- **Recipient Female Sex Pct**: 25.4
- **Recipient Female Sex Pct Overall**: 25.4
- **Mean BMI**: 27
- **Mean BMI Overall**: 27
- **Diagnosis**: Dilated cardiomyopathy (50% of cohort)
- **Diagnosis Overall**: Dilated cardiomyopathy most common overall
- **Diabetes Pct**: 27.2
- **Diabetes Pct Overall**: 27.2
- **Pre-transplant Support**: LVAD in 34% of recipients
- **Pre-transplant Support Overall**: LVAD in 34% overall
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: 30
- **Donor Mean Age Overall**: 30
- **Ischemic Time**: 3.2 hours
- **Ischemic Time Overall**: 3.2 hours

## Interventions & Outcomes
- **Specific Algorithm Name**: Random Survival Forests (RSF) and parametric non-proportional hazards temporal decomposition
- **Intervention Input Data Modality**: National registry data (Scientific Registry of Transplant Recipients) with clinical variables
- **Number of Predictors**: 92 variables used in RSF model
- **Feature Selection Method**: Machine‑learning variable selection within RSF and parsimonious modeling for sex interaction
- **Temporal Handling**: Temporal decomposition into early, constant, and late hazard phases; RSF evaluated at 90 days, 1 year, 5 years, and 10 years
- **Interventions Notes**: Both conventional parametric time‑varying hazard modeling and non‑parametric RSF were applied to identify risk factors and interactions
- **Reported outcomes in study**: All‑cause mortality, survival rates at 90 days, 1 year, 5 years, and 10 years
- **Outcomes Notes**: Primary endpoint was time from transplant to death; survival curves generated for each temporal phase
- **Result data Notes**: Identified three mortality phases; sex was not a significant risk factor; numerous interactions affecting early, constant, and late mortality were discovered
- **Primary Outcome Reported name**: All‑cause mortality
- **Primary Outcome type**: Time‑to‑event (survival)
- **Primary Outcome Reported against**: NR
- **Primary Outcome Reported as**: Mortality incidence and survival percentages
- **Primary Outcome Reference arm**: NR
- **Primary Outcome group**: All adult heart transplant recipients (N=30,606)
- **Primary Outcome Reporting**: 8,278 deaths observed; 1‑month survival 96%, 1‑year survival 89%, 12‑year survival 50%
- **Primary Outcome Point Estimate**: NR
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 30,606 transplant recipients
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Time from heart transplantation to death or end of follow‑up
- **Primary Outcome Timepoints**: 90 days, 1 year, 5 years, 10 years (as evaluated by RSF)
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: 10 years
- **Primary Outcome Notes**: Sex not a significant predictor; risk factors varied by temporal phase
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
