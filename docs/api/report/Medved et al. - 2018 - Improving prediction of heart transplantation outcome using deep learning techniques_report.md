# Data Extraction Report: Medved et al. - 2018 - Improving prediction of heart transplantation outcome using deep learning techniques
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult heart transplant recipients using a deep learning neural network to predict post‑transplant survival, published in 2018 as an observational registry analysis, meeting all inclusion criteria.

## Identification & Methods
- **Sponsorship source**: Health Resources and Services Administration contract 234-2005-370011C; Swedish National Infrastructure for Computing; Swedish Heart-Lung Foundation; Swedish Society of Medicine; Region Skåne Research Funds; Donation Funds of Skane University Hospital; Anna-Lisa and Sven Eric Lundgrens Foundation; Crafoord Foundation; Swedish Research Council; eSSENCE program
- **Country**: Sweden
- **Setting**: NR
- **Comments**: Retrospective analysis of the UNOS registry to compare deep learning (IHTSA) and logistic regression (IMPACT) models for heart transplantation outcome prediction.
- **Author_name**: Dennis Medved
- **Institution**: Lund University, Sweden
- **Email**: johan.nilsson@med.lu.se
- **Address**: Lund, Sweden
- **Country of Data Origin**: USA
- **Dataset Source**: UNOS registry
- **Organ Focus**: Heart
- **Study Period End**: December 2011
- **Study Period Start**: January 1997
- **Identification Notes**: Included adult heart transplant patients >17 years from the UNOS registry between Jan 1997 and Dec 2011.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Artificial Neural Network ensemble (deep learning) for IHTSA; logistic regression for IMPACT.
- **Class Imbalance**: NR
- **Comparator**: IMPACT model (logistic regression) versus IHTSA model (deep learning).
- **Input Variables**: 56 variables extracted; IHTSA uses 43 (recipient and donor), IMPACT uses 18 recipient variables.
- **ML Primary Component**: Yes
- **Missing Data Handling**: Probability imputation using uniform distribution from non‑missing values.
- **Validation Method**: 5‑fold cross‑validation on derivation cohort (1997–2008) and independent test cohort (2009–2011).
- **Methods Notes**: Performance assessed with AUROC, C‑index, DeLong test; recalibrated IHTSA model; Hosmer–Lemeshow goodness‑of‑fit test applied.

## Population Characteristics
- **Inclusion criteria**: Adult heart transplant patients >17 years from January 1997 to December 2011
- **Exclusion criteria**: NR
- **Sample Size Total**: 27,860
- **Target Population**: Recipients
- **Population Notes**: Cohort divided into derivation (1997–2008, n=22,263) and test (2009–2011, n=5,597) cohorts
- **Recipient Mean Age**: 52 ± 13 years
- **Recipient Mean Age Overall**: 52 ± 13 years
- **Recipient Female Sex Pct**: 24%
- **Recipient Female Sex Pct Overall**: 24%
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Ischemic cardiomyopathy (45% of recipients)
- **Diagnosis Overall**: Ischemic cardiomyopathy most common overall
- **Diabetes Pct**: 22%
- **Diabetes Pct Overall**: 22%
- **Pre-transplant Support**: Ventricular assist device in 25% of recipients
- **Pre-transplant Support Overall**: Ventricular assist device in 25% overall
- **Mean Creatinine**: 1.4 ± 0.8 mg/dl
- **Mean Creatinine Overall**: 1.4 ± 0.8 mg/dl
- **Donor Mean Age**: NR
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: 189 ± 63 minutes
- **Ischemic Time Overall**: 189 ± 63 minutes

## Interventions & Outcomes
- **Specific Algorithm Name**: International Heart Transplantation Survival Algorithm (IHTSA) – deep learning; Index for Mortality Prediction After Cardiac Transplantation (IMPACT) – logistic regression
- **Intervention Input Data Modality**: UNOS registry tabular clinical variables (recipient and donor data)
- **Number of Predictors**: IHTSA uses 43 variables; IMPACT uses 18 variables
- **Feature Selection Method**: NR
- **Temporal Handling**: Derivation cohort 1997‑2008, test (validation) cohort 2009‑2011
- **Interventions Notes**: IHTSA employs an ensemble of artificial neural networks (deep learning) and was recalibrated on UNOS data; IMPACT is a logistic‑regression based risk index using only recipient variables
- **Reported outcomes in study**: One‑year mortality (primary), long‑term survival (C‑index) as secondary
- **Outcomes Notes**: Primary endpoint: one‑year mortality; secondary endpoint: all‑cause cumulative mortality over study period
- **Result data Notes**: Comparison of AUROC and C‑index between IHTSA and IMPACT on the test cohort
- **Primary Outcome Reported name**: One‑year mortality
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: IMPACT model
- **Primary Outcome Reported as**: Area under the receiver operating characteristic curve (AUROC)
- **Primary Outcome Reference arm**: IMPACT AUROC 0.608 (95% CI 0.583–0.634)
- **Primary Outcome group**: Heart transplant recipients in the test cohort (2009‑2011)
- **Primary Outcome Reporting**: AUROC 0.643 (95% CI 0.619–0.667) for IHTSA
- **Primary Outcome Point Estimate**: 0.643
- **Primary Outcome 95 CI Lower**: 0.619
- **Primary Outcome 95 CI Upper**: 0.667
- **Primary Outcome p-value**: 0.004
- **Primary Outcome Test Set Size**: 5,597 transplants
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Area under ROC for predicting one‑year mortality on a completely held‑out test cohort
- **Primary Outcome Timepoints**: 1 year post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: IHTSA showed superior discrimination to IMPACT with an error reduction of ~11.7% in AUROC
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.643
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
