# Data Extraction Report: Gholamzadeh et al. - 2025 - Analysis of the most influential factors affecting outcomes of lung transplant recipients a multiva
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Requires Human Review (Rejected by LLM)

## Eligibility
- **Eligibility Status**: Not Accepted
- **Eligibility Rationale**: Although the study uses non‑linear AI models on adult lung transplant data, it predicts waiting‑list priority rather than the required outcomes such as post‑transplant survival or complications, thus failing the outcome criterion.

## Identification & Methods
- **Sponsorship source**: Thoracic Research Center (Tehran University of Medical Sciences)
- **Country**: Iran
- **Setting**: Retrospective analysis of UNOS open‑source transplant database
- **Comments**: Retrospective study using UNOS data to develop and validate machine‑learning models for predicting lung transplant priority scores.
- **Author_name**: Marsa Gholamzadeh
- **Institution**: Tehran University of Medical Sciences
- **Email**: hrabtahi@tums.ac.ir
- **Address**: Tehran, Iran
- **Country of Data Origin**: USA
- **Dataset Source**: United Network for Organ Sharing (UNOS) database
- **Organ Focus**: Lung
- **Study Period End**: 2023
- **Study Period Start**: 2005
- **Identification Notes**: Included adult lung transplant recipients (>18 years) from UNOS between 2005 and 2023; excluded heart transplants, patients with survival <2 years, records before 2005, and pediatric cases.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Multiple linear regression, Random Forest regressor, Support Vector Machine regressor, XGBoost regressor, Multilayer Perceptron, Deep Learning model
- **Class Imbalance**: NR
- **Comparator**: Six regression‑based ML models compared (MLR, RF, SVM, XGBoost, MLP, DL)
- **Input Variables**: Demographic, clinical and donor variables; after feature selection 15 most relevant features (e.g., oxygen requirement, diagnosis group, waiting time, lung condition, hemodynamics).
- **ML Primary Component**: Yes
- **Missing Data Handling**: Columns with >80 % missing removed; remaining numeric features imputed with mean values; categorical encoding via LabelEncoder.
- **Validation Method**: 80/20 train‑test split plus 10‑fold cross‑validation
- **Methods Notes**: Comprehensive preprocessing (duplicate removal, de‑identification, outlier detection via IQR), feature engineering and selection (correlation analysis, variance threshold, XGBoost importance, expert review), hyperparameter tuning with random search, SHAP for model interpretability.

## Population Characteristics
- **Inclusion criteria**: Patients over 18 years old with end-stage lung disease who underwent lung transplants between 2005 and 2022
- **Exclusion criteria**: Patients under 18, records before 2005, heart transplantation records, missing priority scores, survival <2 years
- **Sample Size Total**: 45966
- **Target Population**: Lung transplant recipients
- **Population Notes**: Raw dataset of 196,270 records reduced to 45,966 after preprocessing; data split 80% training and 20% testing
- **Recipient Mean Age**: 54.27
- **Recipient Mean Age Overall**: 54.27
- **Recipient Female Sex Pct**: 33.20
- **Recipient Female Sex Pct Overall**: 33.20
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: End-stage lung disease (various diagnoses)
- **Diagnosis Overall**: NR
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
- **Specific Algorithm Name**: Multiple linear regression, Random forest regressor, Support vector machine regressor, XGBoost regressor, Multilayer perceptron, Deep learning
- **Intervention Input Data Modality**: Tabular clinical and demographic variables from UNOS database
- **Number of Predictors**: 15 selected features after feature engineering
- **Feature Selection Method**: Correlation analysis, variance threshold filtering, embedded XGBoost feature importance, expert review
- **Temporal Handling**: Static baseline data (single time point per patient)
- **Interventions Notes**: Data preprocessing, duplicate removal, de-identification, missing data imputation, outlier removal, feature engineering, hyperparameter tuning via random search, 80:20 train‑test split and 10‑fold cross‑validation
- **Reported outcomes in study**: R-squared (R2), Mean Absolute Error (MAE), Root Mean Square Error (RMSE) for each regression model
- **Outcomes Notes**: Primary outcome was prediction of lung transplant priority score; performance compared across six models
- **Result data Notes**: Random forest regressor achieved highest R2 (95.168%) with lowest MAE (2.056) and RMSE (3.542)
- **Primary Outcome Reported name**: Lung transplant priority allocation score
- **Primary Outcome type**: Regression (continuous)
- **Primary Outcome Reported against**: NR
- **Primary Outcome Reported as**: R-squared (R2)
- **Primary Outcome Reference arm**: NR
- **Primary Outcome group**: All lung transplant recipients in the UNOS dataset used for model development
- **Primary Outcome Reporting**: R2 = 95.168% (adjusted R2 = 95.163%)
- **Primary Outcome Point Estimate**: 0.95168
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Coefficient of determination (R2) calculated on the held‑out test set
- **Primary Outcome Timepoints**: NR
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Random forest model demonstrated superior predictive performance for priority score
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
