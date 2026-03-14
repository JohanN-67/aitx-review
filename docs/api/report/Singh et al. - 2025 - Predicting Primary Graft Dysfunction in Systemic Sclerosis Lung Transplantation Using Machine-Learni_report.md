# Data Extraction Report: Singh et al. - 2025 - Predicting Primary Graft Dysfunction in Systemic Sclerosis Lung Transplantation Using Machine-Learni
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study involves adult lung transplant recipients with systemic sclerosis, uses non‑linear machine‑learning models (random forest, SVM, MLP) to predict primary graft dysfunction, and reports relevant post‑transplant outcomes; it is a peer‑reviewed article published after 2018.

## Identification & Methods
- **Sponsorship source**: National Institutes of Health (NIH) and UPMC Hillman Developmental Pilot Program
- **Country**: USA
- **Setting**: University of Pittsburgh Medical Center, single tertiary academic center
- **Comments**: Retrospective cohort study using pre‑operative clinical data and CT‑derived imaging features to develop machine‑learning models predicting primary graft dysfunction in systemic sclerosis lung transplant recipients.
- **Author_name**: Jiantao Pu
- **Institution**: University of Pittsburgh School of Medicine
- **Email**: puj@upmc.edu
- **Address**: Pittsburgh, Pennsylvania, USA
- **Country of Data Origin**: USA
- **Dataset Source**: Electronic health records and chest CT scans from University of Pittsburgh Medical Center (2007‑2020)
- **Organ Focus**: Lung
- **Study Period End**: 2020
- **Study Period Start**: 2007
- **Identification Notes**: Included 92 adult systemic sclerosis recipients who underwent bilateral lung transplantation at a single center.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Multivariate Logistic Regression, Support Vector Machine (SVM), Random Forest Classifier (RFC), Multilayer Perceptron (MLP)
- **Class Imbalance**: NR
- **Comparator**: Multivariate logistic regression model used as comparator for other ML algorithms
- **Input Variables**: Pre‑operative clinical variables (e.g., BMI, race, FEV1, FVC, LAS, waitlist time) and CT‑derived quantitative features (lung volume, chest cavity volume, heart‑chest cavity ratio, epicardial adipose tissue density, vascular volumes, donor‑recipient size matching ratios).
- **ML Primary Component**: Yes
- **Missing Data Handling**: Variables with >5% missing excluded; remaining missing values imputed using mean for continuous variables and mode for categorical variables.
- **Validation Method**: Repeated stratified 5‑fold cross‑validation with five runs; hyperparameter tuning via randomized grid search within each fold.
- **Methods Notes**: Feature reduction using variance inflation factor and Lasso regression; models limited to four most predictive features to avoid overfitting; class weights balanced/unbalanced explored; no external validation performed.

## Population Characteristics
- **Inclusion criteria**: Systemic sclerosis patients undergoing bilateral lung transplantation at University of Pittsburgh between 2007 and 2020
- **Exclusion criteria**: NR
- **Sample Size Total**: 92
- **Target Population**: SSc lung transplant recipients
- **Population Notes**: Single-center retrospective cohort; all recipients had pre‑transplant chest CT scans
- **Recipient Mean Age**: 51
- **Recipient Mean Age Overall**: 51
- **Recipient Female Sex Pct**: 61
- **Recipient Female Sex Pct Overall**: 61
- **Mean BMI**: 25.1
- **Mean BMI Overall**: 25.1
- **Diagnosis**: Systemic sclerosis (SSc)
- **Diagnosis Overall**: Systemic sclerosis (SSc)
- **Diabetes Pct**: NR
- **Diabetes Pct Overall**: NR
- **Pre-transplant Support**: NR
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: 36
- **Donor Mean Age Overall**: 36
- **Ischemic Time**: NR
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: multivariate logistic regression, support vector machine (SVM), random forest classifier (RFC), multilayer perceptron (MLP)
- **Intervention Input Data Modality**: Pre‑operative clinical variables and CT‑derived imaging features (volumetric measurements, tissue densities)
- **Number of Predictors**: 173 variables initially tested; final model used 4 selected features
- **Feature Selection Method**: Variables with p<0.10 filtered, VIF removal, Lasso regression to eliminate zero‑weight features
- **Temporal Handling**: Static baseline data (pre‑transplant)
- **Interventions Notes**: Repeated stratified 5‑fold cross‑validation with five runs; randomized grid search for hyperparameter tuning
- **Reported outcomes in study**: Primary graft dysfunction (grade 3 PGD at 72 h)
- **Outcomes Notes**: Only occurrence of grade 3 PGD reported as outcome
- **Result data Notes**: Model performance evaluated using AUROC and AUPRC on cross‑validated predictions
- **Primary Outcome Reported name**: Grade 3 primary graft dysfunction
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Multivariate logistic regression (reference model)
- **Primary Outcome Reported as**: AUROC
- **Primary Outcome Reference arm**: Logistic regression AUROC 0.84 (95% CI 0.81–0.88)
- **Primary Outcome group**: All 92 systemic sclerosis lung transplant recipients
- **Primary Outcome Reporting**: AUROC 0.85 (95% CI 0.81–0.88)
- **Primary Outcome Point Estimate**: 0.85
- **Primary Outcome 95 CI Lower**: 0.81
- **Primary Outcome 95 CI Upper**: 0.88
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 92
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Area under the receiver operating characteristic curve on cross‑validated predictions
- **Primary Outcome Timepoints**: 72 h post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: MLP model achieved highest AUROC using four pre‑transplant features
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.85
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
