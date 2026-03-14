# Data Extraction Report: Lehr-2020-Extremes of Age Decrease Survival in
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult lung transplant recipients using a random survival forest (non‑linear AI) to predict post‑transplant survival, compares against standard clinical outcomes, and is a peer‑reviewed article published in 2020.

## Identification & Methods
- **Sponsorship source**: None
- **Country**: USA
- **Setting**: NR
- **Comments**: Retrospective cohort study using the Scientific Registry of Transplant Recipients (SRTR) to assess age effects on lung transplant survival.
- **Author_name**: Carli J. Lehr
- **Institution**: Cleveland Clinic
- **Email**: valapom@ccf.org
- **Address**: 9500 Euclid Ave, A90, Cleveland, OH 44195
- **Country of Data Origin**: USA
- **Dataset Source**: Scientific Registry of Transplant Recipients (SRTR)
- **Organ Focus**: Lung
- **Study Period End**: 2015-02-19
- **Study Period Start**: 2006-01-01
- **Identification Notes**: Included adult (≥18 years) lung transplant recipients in the US between Jan 1, 2006 and Feb 19, 2015; multiorgan transplants excluded.
- **Design**: Retrospective cohort
- **AI Model Architecture**: Random survival forest (RSF) and nonproportional hazard modeling
- **Class Imbalance**: NR
- **Comparator**: NR
- **Input Variables**: Recipient and donor demographics, clinical characteristics, laboratory values, Lung Allocation Score (LAS), diagnosis groups, transplant type, hospitalization status, etc.
- **ML Primary Component**: Yes
- **Missing Data Handling**: Described in supplemental appendix; details not specified in main text.
- **Validation Method**: Bootstrap aggregation (1,000 samples) for variable selection; RSF with 500 trees using randomForestSRC package.
- **Methods Notes**: Used SAS and R for analysis; variable importance measured by VIMP; interactions with age assessed; internal validation via bootstrap and RSF.

## Population Characteristics
- **Inclusion criteria**: Adult (age ≥18) lung transplant recipients in the US between January 1, 2006 and February 19, 2015
- **Exclusion criteria**: Multiorgan transplants
- **Sample Size Total**: 14253
- **Target Population**: Lung transplant recipients
- **Population Notes**: Retrospective cohort using the Scientific Registry of Transplant Recipients (SRTR) covering the LAS era in the United States
- **Recipient Mean Age**: NR
- **Recipient Mean Age Overall**: NR
- **Recipient Female Sex Pct**: NR
- **Recipient Female Sex Pct Overall**: NR
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Idiopathic pulmonary fibrosis (51.2% of recipients)
- **Diagnosis Overall**: Idiopathic pulmonary fibrosis (most common overall)
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
- **Specific Algorithm Name**: NR
- **Intervention Input Data Modality**: Registry data (SRTR) clinical variables
- **Number of Predictors**: 96 variables used in random survival forest model
- **Feature Selection Method**: Bootstrap aggregation (bagging) for variable importance
- **Temporal Handling**: Static baseline data; survival analyzed over follow‑up time
- **Interventions Notes**: Random survival forest and nonproportional hazard modeling applied to identify risk factors for death
- **Reported outcomes in study**: Post‑transplant survival (overall survival), mortality risk
- **Outcomes Notes**: Survival reported at multiple time points (1‑yr, 5‑yr, median follow‑up)
- **Result data Notes**: Age identified as the most important risk factor; extremes of age associated with lower survival
- **Primary Outcome Reported name**: Post‑transplant survival
- **Primary Outcome type**: Time-to-event (survival)
- **Primary Outcome Reported against**: NR
- **Primary Outcome Reported as**: Survival probability (%)
- **Primary Outcome Reference arm**: NR
- **Primary Outcome group**: All lung transplant recipients (n=14,253)
- **Primary Outcome Reporting**: 5‑year survival ≈54% (Kaplan‑Meier), median post‑transplant survival 5.6 years
- **Primary Outcome Point Estimate**: 54
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Kaplan‑Meier estimated survival probability at specified time points
- **Primary Outcome Timepoints**: 1 year, 5 years
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: Beyond 5 years
- **Primary Outcome Notes**: Survival declines for recipients <30 y and >55 y compared with 30‑55 y group
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
