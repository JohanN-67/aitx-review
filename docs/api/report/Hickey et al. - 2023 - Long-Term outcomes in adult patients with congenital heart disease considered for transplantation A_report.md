# Data Extraction Report: Hickey et al. - 2023 - Long-Term outcomes in adult patients with congenital heart disease considered for transplantation A
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study involves adult heart transplant candidates/recipients, uses a machine learning decision‑tree model (non‑linear AI), reports survival outcomes, and is a peer‑reviewed observational study published after 2018.

## Identification & Methods
- **Sponsorship source**: National Institutes of Health; American Heart Association; HeartFest
- **Country**: USA
- **Setting**: Single-center tertiary academic hospital (University of Pittsburgh Medical Center)
- **Comments**: Retrospective chart review of adult congenital heart disease patients evaluated for heart or heart+ transplantation.
- **Author_name**: Gavin Hickey
- **Institution**: University of Pittsburgh Medical Center, Heart and Vascular Institute
- **Email**: saraf@pitt.edu
- **Address**: John G. Rangos Sr. Research Center, #8122, 4401 Penn Ave, Pittsburgh, PA 15224, USA
- **Country of Data Origin**: USA
- **Dataset Source**: Electronic medical records from University of Pittsburgh Medical Center
- **Organ Focus**: Heart (including heart+ additional organ transplants)
- **Study Period Start**: 2004
- **Study Period End**: 2014
- **Identification Notes**: Adults ≥18 years evaluated for heart or heart+ transplantation; 58 patients with complete clinical, hemodynamic, functional and laboratory data included.
- **Design**: Retrospective cohort study
- **AI Model Architecture**: Decision tree machine learning model
- **Class Imbalance**: NR
- **Comparator**: NR
- **Input Variables**: Demographics, CHD diagnosis, prior surgeries (sternotomies), NYHA class, cardiopulmonary exercise testing parameters, invasive hemodynamic measurements (PCWP, SVP, EDP), laboratory values.
- **ML Primary Component**: Yes
- **Missing Data Handling**: Patients lacking any of the required data were excluded; no imputation performed.
- **Validation Method**: K‑fold cross‑validation
- **Methods Notes**: Univariate logistic regression and non‑parametric tests performed; significant variables entered into multivariate decision‑tree analysis using JMP software.

## Population Characteristics
- **Inclusion criteria**: Adults ≥18 years considered for heart or heart+ transplantation
- **Exclusion criteria**: NR
- **Sample Size Total**: 58
- **Target Population**: Adult congenital heart disease patients considered for transplantation
- **Population Notes**: Single-center retrospective chart review of patients evaluated between 2004 and 2014 with follow-up through June 2021
- **Recipient Mean Age**: 35.8 years
- **Recipient Mean Age Overall**: 35.8 years
- **Recipient Female Sex Pct**: 34.5
- **Recipient Female Sex Pct Overall**: 34.5
- **Mean BMI**: 24 (IQR 21–27) kg/m2
- **Mean BMI Overall**: 24 (IQR 21–27) kg/m2
- **Diagnosis**: D-transposition of the great arteries with atrial switch (20.7%) most common
- **Diagnosis Overall**: D-transposition of the great arteries with atrial switch (20.7%) most common
- **Diabetes Pct**: 10.3
- **Diabetes Pct Overall**: 10.3
- **Pre-transplant Support**: LVAD in 5 patients (8.6%)
- **Pre-transplant Support Overall**: LVAD in 5 patients (8.6%)
- **Mean Creatinine**: 0.9 mg/dL
- **Mean Creatinine Overall**: 0.9 mg/dL
- **Donor Mean Age**: NR
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: NR
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: Machine learning decision tree model
- **Intervention Input Data Modality**: Clinical variables including hemodynamic measurements, cardiopulmonary exercise testing, laboratory values, imaging data
- **Number of Predictors**: NR
- **Feature Selection Method**: Univariate analysis followed by multivariate decision‑tree selection
- **Temporal Handling**: Static baseline data at time of transplant evaluation
- **Interventions Notes**: Retrospective chart review of 58 adult congenital heart disease patients evaluated for heart or multi‑organ transplantation; decision‑tree analysis used to identify predictors of survival
- **Reported outcomes in study**: 1‑year survival, 10‑year survival (mortality)
- **Outcomes Notes**: Survival outcomes reported for transplanted, waitlisted, deferred and declined groups
- **Result data Notes**: Focus on invasive hemodynamic parameters (SVP, PCWP) identified by decision‑tree as correlating with 1‑ and 10‑year survival
- **Primary Outcome Reported name**: 1‑year survival
- **Primary Outcome type**: Binary survival outcome
- **Primary Outcome Reported against**: Non‑transplanted (waitlisted/declined) patients
- **Primary Outcome Reported as**: Survival rate (percentage)
- **Primary Outcome Reference arm**: Non‑transplanted patients
- **Primary Outcome group**: All adult congenital heart disease patients considered for transplantation (n=58)
- **Primary Outcome Reporting**: Transplanted patients with SVP < 14 mmHg had 100% survival at 1 year
- **Primary Outcome Point Estimate**: 1.00
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 58
- **Primary Outcome Threshold**: SVP < 14 mmHg
- **Primary Outcome Metric Definition**: Proportion surviving to 1 year post‑transplant decision
- **Primary Outcome Timepoints**: 1 year, 10 years
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: 10 years
- **Primary Outcome Notes**: Invasive hemodynamic parameters (SVP, PCWP) were the strongest correlates of survival
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
