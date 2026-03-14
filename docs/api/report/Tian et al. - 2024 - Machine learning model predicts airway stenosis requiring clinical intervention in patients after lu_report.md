# Data Extraction Report: Tian et al. - 2024 - Machine learning model predicts airway stenosis requiring clinical intervention in patients after lu
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study involves adult lung transplant recipients and uses a non‑linear machine learning model (random forest) to predict post‑transplant airway stenosis, an accepted complication outcome, and is a peer‑reviewed article published after 2018.

## Identification & Methods
- **Sponsorship source**: National Natural Science Foundation of China (No. 82070059)
- **Country**: China
- **Setting**: Single-center retrospective case-controlled study at Wuxi People’s Hospital affiliated with Nanjing Medical University
- **Comments**: Retrospective case-controlled study of lung transplant recipients
- **Author_name**: Dong Tian
- **Institution**: Wuxi People’s Hospital affiliated with Nanjing Medical University
- **Email**: 22tiandong@163.com
- **Address**: Wuxi People’s Hospital, Nanjing Medical University, Wuxi 214023, China
- **Country of Data Origin**: China
- **Dataset Source**: Hospital clinical database / electronic medical records
- **Organ Focus**: Lung
- **Study Period End**: December 2019
- **Study Period Start**: January 2017
- **Identification Notes**: Included adult lung transplant patients; excluded retransplant, pediatric cases, lost to follow‑up, and incomplete records
- **Design**: Retrospective case-controlled study
- **AI Model Architecture**: Random Forest (optimal), also evaluated Logistic Regression, Decision Tree, K‑Nearest Neighbors, Naïve Bayes, Support Vector Machine, Generalized Boosted Regression Modeling, Extreme Gradient Boosting
- **Class Imbalance**: Yes (approximately 10% of patients developed airway stenosis)
- **Comparator**: Conventional logistic regression model
- **Input Variables**: Age, BMI, sex, diagnosis (ILD, COPD, PAH, others), surgical type (SLTx/DLTx), ECMO type (none/VA/VV), ECMO support, preoperative hormone use, 72‑h PGD grade 3, operation time, postoperative ventilator time, ICU stay, postoperative 6‑minute walk test, cold‑ischemia time, PaO2/FiO2
- **ML Primary Component**: Yes
- **Missing Data Handling**: NR
- **Validation Method**: Internal bootstrap validation with 1000 resamples
- **Methods Notes**: Seven feature‑selection methods (filtering, wrapping, embedding) and eight ML algorithms were combined to create 56 models; optimal model selected based on highest AUC; class imbalance acknowledged; no external validation performed

## Population Characteristics
- **Inclusion criteria**: Patients who underwent lung transplantation between January 2017 and December 2019 at Wuxi People’s Hospital
- **Exclusion criteria**: Retransplant patients, pediatric lung transplant patients, lost to follow‑up, incomplete clinical records
- **Sample Size Total**: 381
- **Target Population**: Lung transplant recipients
- **Population Notes**: Single‑center retrospective study; dataset imbalanced with ~10% developing airway stenosis
- **Recipient Mean Age**: 55.13
- **Recipient Mean Age Overall**: 55.13
- **Recipient Female Sex Pct**: 36
- **Recipient Female Sex Pct Overall**: 36
- **Mean BMI**: 20.59
- **Mean BMI Overall**: 20.59
- **Diagnosis**: Interstitial lung disease (ILD)
- **Diagnosis Overall**: Interstitial lung disease (ILD)
- **Diabetes Pct**: NR
- **Diabetes Pct Overall**: NR
- **Pre-transplant Support**: NR
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: NR
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: 7.31 hours
- **Ischemic Time Overall**: 7.31 hours

## Interventions & Outcomes
- **Specific Algorithm Name**: Random Forest
- **Intervention Input Data Modality**: Clinical characteristics (tabular data)
- **Number of Predictors**: 5 selected features (postoperative 6MWT, diagnosis, sex, ECMO type, preoperative hormone use)
- **Feature Selection Method**: Determination coefficient (DC)
- **Temporal Handling**: Retrospective static baseline data
- **Interventions Notes**: 56 ML models evaluated; optimal model identified as Random Forest with DC feature selection; internally validated by bootstrap (1000 resamples)
- **Reported outcomes in study**: Airway stenosis requiring clinical intervention, AUC, brier score, sensitivity, specificity, PPV, NPV
- **Outcomes Notes**: Primary outcome is prediction of airway stenosis requiring clinical intervention after lung transplantation
- **Result data Notes**: Optimal ML model achieved AUC 0.760 (95% CI 0.666–0.864) and brier score 0.085, outperforming conventional logistic regression (AUC 0.689)
- **Primary Outcome Reported name**: Airway stenosis requiring clinical intervention
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Conventional logistic regression model
- **Primary Outcome Reported as**: Area under the ROC curve (AUC)
- **Primary Outcome Reference arm**: Logistic regression AUC 0.689 (95% CI 0.545–0.803)
- **Primary Outcome group**: All lung transplant recipients (n=381)
- **Primary Outcome Reporting**: AUC 0.760 (95% CI 0.666–0.864)
- **Primary Outcome Point Estimate**: 0.760
- **Primary Outcome 95 CI Lower**: 0.666
- **Primary Outcome 95 CI Upper**: 0.864
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 381
- **Primary Outcome Threshold**: 0.163 (optimal cut‑off for risk stratification)
- **Primary Outcome Metric Definition**: Area under the ROC curve on bootstrapped internal validation
- **Primary Outcome Timepoints**: NR
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Optimal Random Forest model showed superior discrimination and calibration compared with logistic regression
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
