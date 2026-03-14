# Data Extraction Report: Yoon et al. - 2018 - Personalized survival predictions via Trees of Predictors An application to cardiac transplantation
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult heart transplant candidates and recipients using a non‑linear machine learning method (Trees of Predictors) to predict post‑ and pre‑transplant survival, meeting all population, intervention, outcome, and study design criteria.

## Identification & Methods
- **Sponsorship source**: Office of Naval Research (ONR) and National Science Foundation (NSF)
- **Country**: United States
- **Setting**: Retrospective cohort using UNOS registry data
- **Comments**: Open access article; uses United Network for Organ Sharing (UNOS) database of heart transplant patients from 1985-2015
- **Author_name**: Jinsung Yoon
- **Institution**: University of California Los Angeles
- **Email**: mihaela.vanderschaar@oxford-man.ox.ac.uk
- **Address**: Los Angeles, CA, USA
- **Country of Data Origin**: United States
- **Dataset Source**: UNOS database
- **Organ Focus**: Heart
- **Study Period End**: 2015
- **Study Period Start**: 1985
- **Identification Notes**: Included adults >18 years; excluded patients <18; final cohorts 51,971 transplanted and 30,911 wait-listed patients
- **Design**: Retrospective cohort
- **AI Model Architecture**: Trees of Predictors (ToPs) with base learners Cox Regression, Linear Perceptron, Logistic Regression
- **Class Imbalance**: NR
- **Comparator**: Clinical risk scores (DRI, IMPACT, RSS) and state-of-the-art machine learning methods
- **Input Variables**: 53 selected features (33 recipient, 14 donor, 6 donor-recipient compatibility) after discarding high-missing features
- **ML Primary Component**: Yes
- **Missing Data Handling**: Multiple imputation by chained equations (MICE) with 10 imputations; discarded features with >10% missing
- **Validation Method**: 5-fold cross-validation
- **Methods Notes**: Tree of predictors creates clusters and assigns specific predictive models; predictions aggregated via weighted average using linear perceptron; addresses heterogeneity across patients and time horizons

## Population Characteristics
- **Inclusion criteria**: Patients registered for heart transplantation in the UNOS database (1985-2015) who are adults (age ≥18)
- **Exclusion criteria**: Patients age <18; features with >10% missing data; post-transplantation only features
- **Sample Size Total**: 82882
- **Target Population**: Heart transplant recipients and wait-listed patients
- **Population Notes**: Data split into 5-fold cross-validation with 80% training and 20% testing; cohorts: 51,971 transplanted and 30,911 wait-listed after exclusions
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
- **Specific Algorithm Name**: Trees of Predictors (ToPs/R)
- **Intervention Input Data Modality**: Tabular clinical features from UNOS database
- **Number of Predictors**: 53 features (33 recipient, 14 donor, 6 compatibility)
- **Feature Selection Method**: Relevance scores based on correlation coefficient; discarding features with >10% missing
- **Temporal Handling**: Static baseline data with separate models for each time horizon (3‑month, 1‑year, 3‑year, 10‑year)
- **Interventions Notes**: Tree of predictors that clusters patients and assigns specific base learners (Cox Regression, Linear Perceptron, Logistic Regression) to each cluster; 5‑fold cross‑validation
- **Reported outcomes in study**: Survival prediction AUC and C‑index at multiple horizons (3‑month, 1‑year, 3‑year, 10‑year) post‑ and pre‑transplantation
- **Outcomes Notes**: Focus on AUC improvements over clinical risk scores and other ML methods
- **Result data Notes**: Tables report AUC values (e.g., 0.660 for 3‑month post‑transplantation) and C‑index; statistically significant improvements (p < 0.01)
- **Primary Outcome Reported name**: 3‑month post‑transplantation survival
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Risk‑Stratification Score (RSS) clinical risk score
- **Primary Outcome Reported as**: Area Under the ROC Curve (AUC)
- **Primary Outcome Reference arm**: RSS AUC 0.587 (95% CI 0.579‑0.598)
- **Primary Outcome group**: All transplanted patients in the test set
- **Primary Outcome Reporting**: AUC 0.660 (95% CI 0.650‑0.671)
- **Primary Outcome Point Estimate**: 0.660
- **Primary Outcome 95 CI Lower**: 0.650
- **Primary Outcome 95 CI Upper**: 0.671
- **Primary Outcome p-value**: <0.01
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Area under ROC curve for predicting survival at 3 months post‑transplantation
- **Primary Outcome Timepoints**: 3 months post‑transplantation
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Significant improvement over RSS; AUC increase from 0.587 to 0.660
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
