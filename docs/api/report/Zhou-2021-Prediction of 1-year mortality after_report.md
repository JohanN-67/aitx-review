# Data Extraction Report: Zhou-2021-Prediction of 1-year mortality after
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study involves adult heart transplant recipients, uses non‑linear machine‑learning models (e.g., random forest, gradient boosting) to predict 1‑year mortality, and is a peer‑reviewed article published in 2021.

## Identification & Methods
- **Sponsorship source**: National Natural Science Foundation of China
- **Country**: China
- **Setting**: Single-center study at Union Hospital, Wuhan, China
- **Comments**: Retrospective cohort using electronic medical records of heart transplant recipients from a single Chinese center.
- **Author_name**: Fei Li
- **Institution**: Department of Cardiovascular Surgery, Union Hospital, Tongji Medical College, Huazhong University of Science and Technology
- **Email**: lifei_union@sina.com
- **Address**: 1277 Jiefang Avenue, Wuhan 430022, China
- **Country of Data Origin**: China
- **Dataset Source**: Electronic medical records from Union Hospital
- **Organ Focus**: Heart
- **Study Period End**: 2018-12-31
- **Study Period Start**: 2015-01-01
- **Identification Notes**: Consecutive orthotopic heart transplant recipients from Jan 1 2015 to Dec 31 2018; excluded re‑transplant, multi‑organ transplant and patients with survival <1 year.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: LASSO for feature selection; seven machine‑learning models: logistic regression, support vector machine, random forest, XGBoost, AdaBoost, gradient boosting machine, artificial neural network
- **Class Imbalance**: NR
- **Comparator**: NR
- **Input Variables**: 70 variables after imputation; key ones include albumin, recipient age, left atrium diameter, red blood cell count, hemoglobin, lymphocyte %, smoking history, lyophilized rhBNP, Levosimendan, hypertension, cardiac surgery history, malignancy, endotracheal intubation history
- **ML Primary Component**: Yes
- **Missing Data Handling**: Variables with >10% missing discarded; remaining continuous variables imputed with column mean, categorical with most frequent value
- **Validation Method**: Bootstrap validation (1000 resamples) and five‑fold cross‑validation for hyperparameter tuning; 70/30 train‑test split
- **Methods Notes**: SHAP used for model interpretation; grid search for tuning; bootstrap approach to evaluate performance; primary outcome 1‑year mortality

## Population Characteristics
- **Inclusion criteria**: Consecutive recipients of orthotopic heart transplantation at the institute between January 1, 2015 and December 31, 2018
- **Exclusion criteria**: Patients with survival time less than one year and those undergoing re‑transplant or multiple organ transplant
- **Sample Size Total**: 381
- **Target Population**: Heart transplantation recipients
- **Population Notes**: Data randomly split into 70% training set and 30% testing set
- **Recipient Mean Age**: 43.783
- **Recipient Mean Age Overall**: 43.783
- **Recipient Female Sex Pct**: 23.8
- **Recipient Female Sex Pct Overall**: 23.8
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Dilated cardiomyopathy (65.2% of recipients)
- **Diagnosis Overall**: Dilated cardiomyopathy (65.2%)
- **Diabetes Pct**: 12.5
- **Diabetes Pct Overall**: 12.5
- **Pre-transplant Support**: NR
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: 32.527
- **Donor Mean Age Overall**: 32.527
- **Ischemic Time**: 336.32 min
- **Ischemic Time Overall**: 336.32 min

## Interventions & Outcomes
- **Specific Algorithm Name**: Random Forest, Gradient Boosting Machine, XGBoost, AdaBoost, Support Vector Machine, Logistic Regression, Artificial Neural Network
- **Intervention Input Data Modality**: Electronic medical records with clinical variables (70 preprocessed features)
- **Number of Predictors**: 13 selected variables after LASSO
- **Feature Selection Method**: Least absolute shrinkage and selection operator (LASSO) with five‑fold cross‑validation
- **Temporal Handling**: Static baseline pre‑operative data (single time point)
- **Interventions Notes**: Bootstrap validation (1000 resamples), grid search for hyper‑parameter tuning, 5‑fold cross‑validation, training/testing split 70/30
- **Reported outcomes in study**: 1-year mortality (including in‑hospital and post‑discharge mortality)
- **Outcomes Notes**: Primary outcome combines in‑hospital death and death within one year after transplantation
- **Result data Notes**: Random Forest achieved highest discrimination (AUC 0.801); GBM had highest sensitivity (0.271); overall low sensitivities across models
- **Primary Outcome Reported name**: 1-year mortality
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: NR
- **Primary Outcome Reported as**: Area under the receiver operating characteristic curve (AUC)
- **Primary Outcome Reference arm**: NR
- **Primary Outcome group**: All heart transplant recipients in the cohort
- **Primary Outcome Reporting**: AUC 0.801 (95% CI 0.697–0.891)
- **Primary Outcome Point Estimate**: 0.801
- **Primary Outcome 95 CI Lower**: 0.697
- **Primary Outcome 95 CI Upper**: 0.891
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: AUC calculated on bootstrap‑validated test set for predicting 1‑year mortality
- **Primary Outcome Timepoints**: 1 year post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Random Forest showed highest discrimination; sensitivities were low for all models
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.801
- **Res_Primary 1Yr Accuracy**: 0.828
- **Res_Primary 1Yr Sens_Spec**: Sens 0.268, Spec 0.927
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
