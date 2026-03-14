# Data Extraction Report: Dueñas-Jurado et al. - 2021 - New models for donor-recipient matching in lung transplantations
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult lung transplant recipients using a neural network (non‑linear AI) to predict six‑month survival, published in a peer‑reviewed journal in 2021, thus meeting all inclusion criteria.

## Identification & Methods
- **Sponsorship source**: Spanish Ministry of Economy and Competitiveness (MINECO) and FEDER
- **Country**: Spain
- **Setting**: Reina Sofia University Hospital, Cordoba, Spain (Intensive Care Unit and Lung Transplant Service)
- **Comments**: Retrospective analysis of 404 lung transplants performed over 23 years.
- **Author_name**: J. M. Dueñas-Jurado
- **Institution**: Reina Sofia University Hospital, Cordoba, Spain
- **Email**: angeti@hotmail.com
- **Address**: Reina Sofia University Hospital, Cordoba, Spain
- **Country of Data Origin**: Spain
- **Dataset Source**: Hospital records from the Lung Transplant Program at Reina Sofia University Hospital
- **Organ Focus**: Lung
- **Study Period End**: January 2016
- **Study Period Start**: October 1993
- **Identification Notes**: Included adult lung transplant recipients; excluded pediatric (<15 years) and combined/multi-organ transplants (>2 organs).
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Logistic Regression combined with Evolutionary Product‑Unit Neural Network (EPUNN)
- **Class Imbalance**: NR
- **Comparator**: Classical statistical methods (standard logistic regression)
- **Input Variables**: Demographic, clinical and procedural variables of donors and recipients (e.g., age, sex, disease type, ventilation status, cause of donor death, ischemia time, transplant type, etc.)
- **ML Primary Component**: Yes
- **Missing Data Handling**: NR
- **Validation Method**: NR
- **Methods Notes**: Used evolutionary algorithms and product‑unit neural networks; hybrid LR‑EPUNN model optimized for binary survival outcome at six months.

## Population Characteristics
- **Inclusion criteria**: Retrospective analysis of lung transplant recipients performed at Reina Sofía University Hospital between October 1993 and January 2016
- **Exclusion criteria**: Pediatric recipients (<15 years) and combined or multi-organ transplants (more than two vital organs)
- **Sample Size Total**: 404
- **Target Population**: Lung transplant recipients
- **Population Notes**: Single‑center cohort spanning 23 years; all transplants performed at the same hospital
- **Recipient Mean Age**: NR
- **Recipient Mean Age Overall**: NR
- **Recipient Female Sex Pct**: NR
- **Recipient Female Sex Pct Overall**: NR
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Recipient underlying disease categories included COPD, cystic fibrosis, pulmonary fibrosis, bronchiectasis and other respiratory diseases
- **Diagnosis Overall**: Same as Diagnosis
- **Diabetes Pct**: NR
- **Diabetes Pct Overall**: NR
- **Pre-transplant Support**: Pre‑transplant status recorded (ambulatory, hospitalized, ICU) but percentages not reported
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: NR
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: Cold ischemia time categorized (short, medium, long, very long) but no mean value reported
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: LRIPU (logistic regression using initial covariates and product units)
- **Intervention Input Data Modality**: Tabular clinical variables (donor and recipient characteristics)
- **Number of Predictors**: 36 donor-recipient pairing variables (plus bias term)
- **Feature Selection Method**: NR
- **Temporal Handling**: Static baseline data (variables collected at transplant)
- **Interventions Notes**: Hybrid model combining logistic regression with evolutionary product‑unit neural network (EPUNN) to optimize architecture and weights
- **Reported outcomes in study**: Graft survival at six months (binary)
- **Outcomes Notes**: Primary outcome is binary survival/non‑survival of the graft at six months post‑transplant
- **Result data Notes**: Model provides probability equation; no performance metrics (e.g., AUC, accuracy) reported
- **Primary Outcome Reported name**: Graft survival at six months
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: NR
- **Primary Outcome Reported as**: Probability of survival (logistic probability)
- **Primary Outcome Reference arm**: NR
- **Primary Outcome group**: All 404 lung transplant recipients in the retrospective cohort
- **Primary Outcome Reporting**: Model coefficients and probability equation; no quantitative performance reported
- **Primary Outcome Point Estimate**: NR
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Probability of graft survival derived from logistic regression‑product unit model
- **Primary Outcome Timepoints**: Six months post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Outcome focused on six‑month graft survival; no separate in‑hospital, 1‑year or late timepoint results provided
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
