# Data Extraction Report: Ahady Dolatsara-2020-A two-stage machine learn
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult heart transplant recipients using non-linear machine learning models (e.g., random forests, XGBoost) to predict survival outcomes, includes relevant clinical comparators, and is a peer‑reviewed article published in 2020.

## Identification & Methods
- **Sponsorship source**: National Science Foundation
- **Country**: USA
- **Setting**: UNOS national heart transplant registry
- **Comments**: Retrospective analysis of UNOS heart transplant data using a two-stage machine learning framework with isotonic regression calibration.
- **Author_name**: Hamidreza Ahady Dolatsara
- **Institution**: Clark University, School of Management
- **Email**: hamid@clarku.edu
- **Address**: Worcester, MA 01610, USA
- **Country of Data Origin**: USA
- **Dataset Source**: UNOS registry
- **Organ Focus**: Heart
- **Study Period End**: 2016
- **Study Period Start**: 1987
- **Identification Notes**: Included all heart transplant events in the UNOS dataset up to September 30, 2016.
- **Design**: Two-stage machine learning framework: independent models per time period followed by isotonic regression calibration.
- **AI Model Architecture**: Logistic Regression, Linear Discriminant Analysis, Artificial Neural Networks, CART, SVM, Random Forest, XGBoost; final model logistic regression with LASSO feature selection.
- **Class Imbalance**: Addressed using sub‑sampling methods: up‑sampling, down‑sampling, SMOTE, and ROSE.
- **Comparator**: Standard machine learning models without isotonic regression calibration.
- **Input Variables**: Pre‑operative donor and recipient variables (originally 494, reduced after cleaning and feature engineering).
- **ML Primary Component**: Yes
- **Missing Data Handling**: Removed variables with >90% missing; numeric median imputation, categorical unknown imputation for remaining missing values.
- **Validation Method**: 5‑fold cross‑validation on training set and 20% hold‑out test set.
- **Methods Notes**: Used 5‑fold CV for model selection, isotonic regression to enforce monotonicity, code and analysis publicly available on GitHub.

## Population Characteristics
- **Inclusion criteria**: NR
- **Exclusion criteria**: NR
- **Sample Size Total**: 103,570
- **Target Population**: Heart transplant recipients (UNOS registry)
- **Population Notes**: National UNOS dataset of U.S. heart transplants from 1987 to 2016
- **Recipient Mean Age**: NR
- **Recipient Mean Age Overall**: NR
- **Recipient Female Sex Pct**: NR
- **Recipient Female Sex Pct Overall**: NR
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: NR
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
- **Specific Algorithm Name**: Logistic Regression
- **Intervention Input Data Modality**: Pre-operative tabular clinical variables from UNOS registry
- **Number of Predictors**: NR
- **Feature Selection Method**: LASSO
- **Temporal Handling**: Multi-period static baseline predictions for 1 month to 10 years post‑transplant
- **Interventions Notes**: Two-stage framework: Stage I independent ML models per time‑point, Stage II isotonic regression to enforce monotonic decreasing survival probabilities
- **Reported outcomes in study**: AUC, G‑Mean, accuracy, sensitivity, specificity for survival prediction at 1 month–10 years
- **Outcomes Notes**: Primary focus on discrimination (AUC) and calibration; isotonic regression improves metrics
- **Result data Notes**: Isotonic regression generally increased AUC and G‑Mean across time points
- **Primary Outcome Reported name**: 1-year survival probability
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: NR
- **Primary Outcome Reported as**: Area under the ROC curve (AUC)
- **Primary Outcome Reference arm**: NR
- **Primary Outcome group**: All heart transplant recipients in the hold‑out test set
- **Primary Outcome Reporting**: AUC 0.581 (pre‑calibration), improved to 0.598 after isotonic regression
- **Primary Outcome Point Estimate**: 0.581
- **Primary Outcome 95 CI Lower**: 0.645
- **Primary Outcome 95 CI Upper**: 0.664
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Area under the ROC curve on a held‑out test cohort
- **Primary Outcome Timepoints**: 1 year post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: AUC comparable to literature; isotonic regression yields modest improvement
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.598
- **Res_Primary 1Yr Accuracy**: 0.620
- **Res_Primary 1Yr Sens_Spec**: Sens 0.658, Spec 0.485
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
