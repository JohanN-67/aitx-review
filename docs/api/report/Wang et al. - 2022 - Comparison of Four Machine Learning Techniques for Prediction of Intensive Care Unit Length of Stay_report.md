# Data Extraction Report: Wang et al. - 2022 - Comparison of Four Machine Learning Techniques for Prediction of Intensive Care Unit Length of Stay
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Requires Human Review (Rejected by LLM)

## Eligibility
- **Eligibility Status**: Not Accepted
- **Eligibility Rationale**: Although the study involves adult heart transplant recipients and uses non‑linear machine learning models, its primary outcome is ICU length of stay, which is not among the specified eligible outcomes (survival, waitlist mortality, post‑transplant complications, quality of life, or economic measures).

## Identification & Methods
- **Sponsorship source**: NR
- **Country**: NR
- **Setting**: Single tertiary hospital (Union Hospital, Wuhan)
- **Comments**: Retrospective study of 365 heart transplantation patients to predict ICU length of stay using machine learning.
- **Author_name**: Kan Wang
- **Institution**: Department of Cardiovascular Surgery, Union Hospital, Tongji Medical College, Huazhong University of Science and Technology, Wuhan, China
- **Email**: shijiawei@21cn.com
- **Address**: Wuhan, China
- **Country of Data Origin**: China
- **Dataset Source**: Clinical data from Wuhan Union Hospital electronic medical records
- **Organ Focus**: Heart
- **Study Period End**: 2020
- **Study Period Start**: 2017
- **Identification Notes**: Included consecutive adult heart transplantation patients (365) from April 2017 to August 2020.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: XGBoost, Random Forest, Naive Bayes, Support Vector Machine, Logistic Regression
- **Class Imbalance**: Up-sampling of minority class
- **Comparator**: Logistic regression (LR) model
- **Input Variables**: 84 clinical features initially; six key variables selected (ECMO, donor age, IABP, surgery length, creatinine, CRRT)
- **ML Primary Component**: Yes
- **Missing Data Handling**: Median imputation of missing values
- **Validation Method**: Fivefold cross‑validation and 7:3 train‑test split
- **Methods Notes**: LASSO regression for feature selection, SHAP values for model interpretation, online web‑server for prediction.

## Population Characteristics
- **Inclusion criteria**: Heart transplantation surgery for moderate (NYHA grade 3) or severe (NYHA grade 4) heart failure
- **Exclusion criteria**: NR
- **Sample Size Total**: 365
- **Target Population**: Heart transplant recipients
- **Population Notes**: Patients randomly divided into training (N=256) and test (N=109) sets; 84 clinical features collected
- **Recipient Mean Age**: 47.20
- **Recipient Mean Age Overall**: 47.20
- **Recipient Female Sex Pct**: NR
- **Recipient Female Sex Pct Overall**: NR
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Moderate (NYHA 3) or severe (NYHA 4) heart failure
- **Diagnosis Overall**: Moderate (NYHA 3) or severe (NYHA 4) heart failure
- **Diabetes Pct**: 16.4
- **Diabetes Pct Overall**: 16.4
- **Pre-transplant Support**: ECMO 5.2%, IABP 44.4%, CRRT 12.6%
- **Pre-transplant Support Overall**: ECMO 5.2%, IABP 44.4%, CRRT 12.6%
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: 35.58
- **Donor Mean Age Overall**: 35.58
- **Ischemic Time**: NR
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: XGBoost, Random Forest, Naive Bayes, Support Vector Machine, Logistic Regression
- **Intervention Input Data Modality**: Tabular clinical variables (84 pre‑operative features)
- **Number of Predictors**: 84 clinical features collected; 6 selected by LASSO for final model
- **Feature Selection Method**: LASSO regression with five‑fold cross‑validation
- **Temporal Handling**: Static baseline (pre‑operative) data
- **Interventions Notes**: Five‑fold cross‑validation, up‑sampling for class imbalance, SHAP values for model interpretation, online web‑server tool
- **Reported outcomes in study**: Prediction of intensive care unit length of stay (ICU‑LOS) with metrics AUC‑ROC, accuracy, sensitivity, specificity, PPV, NPV
- **Outcomes Notes**: Primary outcome is binary classification of prolonged vs short ICU stay
- **Result data Notes**: XGBoost achieved the highest performance (AUC‑ROC = 0.8828) compared with other models
- **Primary Outcome Reported name**: ICU length of stay (prolonged vs short)
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Logistic regression and other machine‑learning models (RF, NB, SVM)
- **Primary Outcome Reported as**: Area under the ROC curve (AUC‑ROC)
- **Primary Outcome Reference arm**: Logistic regression AUC = 0.8159
- **Primary Outcome group**: All heart transplantation patients (n = 365)
- **Primary Outcome Reporting**: AUC = 0.8828 (Accuracy = 0.8780; Sensitivity = 0.9883; Specificity = 0.5190; PPV = 0.8699; NPV = 0.9318)
- **Primary Outcome Point Estimate**: 0.8828
- **Primary Outcome 95 CI Lower**: 0.8572
- **Primary Outcome 95 CI Upper**: 0.9284
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 109
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: AUC‑ROC calculated on a completely held‑out test cohort
- **Primary Outcome Timepoints**: NR
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: XGBoost significantly outperformed logistic regression and other ML models for ICU‑LOS prediction
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
