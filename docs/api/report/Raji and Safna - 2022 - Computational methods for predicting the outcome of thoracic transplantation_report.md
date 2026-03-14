# Data Extraction Report: Raji and Safna - 2022 - Computational methods for predicting the outcome of thoracic transplantation
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Requires Human Review (Rejected by LLM)

## Eligibility
- **Eligibility Status**: Not Accepted
- **Eligibility Rationale**: Although the study uses non‑linear AI models on adult thoracic transplant recipients and is a peer‑reviewed article from 2022, it does not compare the AI predictions to current clinical practice or a gold‑standard comparator.

## Identification & Methods
- **Sponsorship source**: Health Resources and Services Administration contract 234-2005-370011C
- **Country**: India
- **Setting**: NR
- **Comments**: Retrospective study using UNOS data for thoracic transplantation survival prediction with ANN models.
- **Author_name**: C. G. Raji
- **Institution**: MEA Engineering College, Department of Computer Science and Engineering, Perinthalmanna, Kerala, India
- **Email**: rajicg80@gmail.com
- **Address**: MEA Engineering College, Perinthalmanna, Kerala, India
- **Country of Data Origin**: USA
- **Dataset Source**: UNOS database
- **Organ Focus**: Thoracic transplantation (heart)
- **Study Period End**: NR
- **Study Period Start**: NR
- **Identification Notes**: Included adult patients only; pediatric records (9373) removed.
- **Design**: Retrospective
- **AI Model Architecture**: Multi-layer perceptron ANN and Radial Basis Function ANN
- **Class Imbalance**: NR
- **Comparator**: Existing MLP model from prior study (85.9% accuracy)
- **Input Variables**: 24 selected attributes including GENDER, ABO, TOT_SERUM_ALBUM, RESIST_INF, INIT_AGE, ECMO_TRR, CREAT_TRR, HEMO_PA_MN_TRR, IABP_TRR, ACUTE_REJ_EPI, GTIME, TRTREJ1Y, HLAMIS, PRAMR_CL2, AGE_DON, ABO_DON, GENDER_DON, DOPAMINE_DON_OLD, ABO_MAT, AGE, ISCHITIME, GRF_FAIL_CAUSE, AGE_GROUP, INOTROP_AGENTS
- **ML Primary Component**: Yes
- **Missing Data Handling**: NR
- **Validation Method**: Tenfold cross-validation
- **Methods Notes**: Feature selection using InfoGain Attribute Eval with ranker; tenfold CV; performance evaluated with accuracy, sensitivity, specificity, ROC AUC.

## Population Characteristics
- **Inclusion criteria**: Adult thoracic transplantation patients from UNOS database
- **Exclusion criteria**: Pediatric records (9373 pediatric records removed)
- **Sample Size Total**: 485
- **Target Population**: Thoracic transplantation recipients
- **Population Notes**: Dataset originally contained 1,48,509 records; after removing pediatric cases only 485 adult records remained
- **Recipient Mean Age**: 51.192
- **Recipient Mean Age Overall**: NR
- **Recipient Female Sex Pct**: 47.6
- **Recipient Female Sex Pct Overall**: NR
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: NR
- **Diagnosis Overall**: NR
- **Diabetes Pct**: NR
- **Diabetes Pct Overall**: NR
- **Pre-transplant Support**: NR
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: 0.9
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: NR
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: 4.651 hours
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: Multi-layer perceptron, Radial basis function
- **Intervention Input Data Modality**: Tabular clinical variables from UNOS database
- **Number of Predictors**: 24
- **Feature Selection Method**: InfoGain Attribute Eval with ranker search
- **Temporal Handling**: Static baseline data
- **Interventions Notes**: Tenfold cross‑validation, back‑propagation training of ANN models
- **Reported outcomes in study**: Accuracy, sensitivity, specificity, precision, recall, F‑measure, ROC AUC
- **Outcomes Notes**: Short‑term survival prediction (1–3 years) after thoracic transplantation
- **Result data Notes**: MLP accuracy 97.1%, RBF accuracy 92.37%; MLP ROC AUC 0.918, RBF ROC AUC 0.95
- **Primary Outcome Reported name**: Survival prediction accuracy (short‑term)
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Existing MLP model (85.9% accuracy)
- **Primary Outcome Reported as**: Accuracy (%)
- **Primary Outcome Reference arm**: Existing system accuracy 85.9%
- **Primary Outcome group**: All adult thoracic transplantation records (n=485)
- **Primary Outcome Reporting**: Accuracy 97.1%
- **Primary Outcome Point Estimate**: 0.971
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 485
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Accuracy on held‑out test set using tenfold cross‑validation
- **Primary Outcome Timepoints**: 1 year (short‑term)
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: MLP outperforms RBF and existing models in accuracy and AUC
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.918
- **Res_Primary 1Yr Accuracy**: 97.1%
- **Res_Primary 1Yr Sens_Spec**: Sensitivity 0.966, Specificity 0.984
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
