# Data Extraction Report: Adedinsewo et al. - 2023 - Non-invasive detection of cardiac allograft rejection among heart transplant recipients using an ele
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study involves adult heart transplant recipients and uses a deep‑learning (non‑linear) AI model to detect acute cellular rejection, reporting diagnostic performance outcomes; it is a peer‑reviewed observational study published after 2018.

## Identification & Methods
- **Sponsorship source**: Mayo Clinic clinical practice committee innovation funds
- **Country**: USA
- **Setting**: Tertiary academic center (Mayo Clinic)
- **Comments**: Retrospective cohort study with a prospective proof-of-concept validation; used ECG and biopsy data from three Mayo Clinic sites.
- **Author_name**: Demilade Adedinsewo
- **Institution**: Mayo Clinic
- **Email**: adedinsewo.demilade@mayo.edu
- **Address**: 4500 San Pablo Rd, Jacksonville, FL 32224, USA
- **Country of Data Origin**: USA
- **Dataset Source**: Electronic health record (Mayo Clinic) – digital 12‑lead ECGs and endomyocardial biopsy results
- **Organ Focus**: Heart
- **Study Period End**: 2021
- **Study Period Start**: 1998
- **Identification Notes**: Included adult heart transplant recipients (≥18 years) with digital 12‑lead ECGs within 30 days prior to biopsy; excluded patients without digital ECGs, <18 years, or inconclusive pathology.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Convolutional neural network (39 layers) implemented in Keras/TensorFlow; input 12 × 5000 array (12 leads, 10 s at 500 Hz).
- **Class Imbalance**: Addressed using class weights during training and hyperparameter search.
- **Comparator**: NR
- **Input Variables**: 12‑lead ECG waveform data (raw signal).
- **ML Primary Component**: Yes
- **Missing Data Handling**: Patients lacking digital ECGs or with missing biopsy data were excluded; no imputation performed.
- **Validation Method**: 80/10/10 train‑validation‑test split with patient-level partitioning; prospective proof‑of‑concept cohort for external validation.
- **Methods Notes**: Data augmentation with random noise and translation; binary cross‑entropy loss; hyperparameter search over optimizer, learning rate, class weights, batch size, regularization; threshold 0.4 selected to maximize sensitivity.

## Population Characteristics
- **Inclusion criteria**: Age ≥18 years, heart transplant recipient, scheduled for endomyocardial biopsy (EMB)
- **Exclusion criteria**: Age <18 years, without digital ECG, inconclusive EMB pathology results
- **Sample Size Total**: 1427
- **Target Population**: Heart transplant recipients
- **Population Notes**: Data split into training (80%), validation (10%), and test (10%) sets; each patient included in only one partition. Prospective proof-of-concept cohort of 56 patients also reported.
- **Recipient Mean Age**: 55.6 years (median age at transplant)
- **Recipient Mean Age Overall**: 55.6 years
- **Recipient Female Sex Pct**: 28.9%
- **Recipient Female Sex Pct Overall**: 28.9%
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: NR
- **Diagnosis Overall**: NR
- **Diabetes Pct**: 56.3%
- **Diabetes Pct Overall**: 56.3%
- **Pre-transplant Support**: NR
- **Pre-transplant Support Overall**: NR
- **Mean Creatinine**: NR
- **Mean Creatinine Overall**: NR
- **Donor Mean Age**: NR
- **Donor Mean Age Overall**: NR
- **Ischemic Time**: NR
- **Ischemic Time Overall**: NR

## Interventions & Outcomes
- **Specific Algorithm Name**: Convolutional neural network deep-learning model (AI-ECG)
- **Intervention Input Data Modality**: 12-lead digital ECG signals (500 Hz, 10 s recordings)
- **Number of Predictors**: NR
- **Feature Selection Method**: NR
- **Temporal Handling**: Static single ECG obtained within 30 days prior to endomyocardial biopsy
- **Interventions Notes**: Model comprised 39 layers with ~80 million trainable parameters; trained using binary cross‑entropy loss and hyperparameter search over optimizer, learning rate, class weights, batch size and regularisation; input array 12 × 5000.
- **Reported outcomes in study**: Detection of moderate‑to‑severe acute cellular rejection (ACR) using AI-ECG; performance metrics AUC, sensitivity, specificity, PPV, NPV.
- **Outcomes Notes**: Primary outcome was non‑invasive identification of moderate/severe ACR compared with biopsy reference.
- **Result data Notes**: Test‑set AUC 0.84 (95% CI 0.78–0.90), sensitivity 95%, specificity 52.6%; prospective proof‑of‑concept AUC 0.78 (95% CI 0.61–0.96).
- **Primary Outcome Reported name**: Detection of moderate‑to‑severe acute cellular rejection (ACR)
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Endomyocardial biopsy (gold‑standard)
- **Primary Outcome Reported as**: Area under the receiver operating characteristic curve (AUC)
- **Primary Outcome Reference arm**: Biopsy‑confirmed ACR status
- **Primary Outcome group**: Heart transplant recipients in the held‑out test set (n = 140 patients; 758 ECG‑biopsy pairs)
- **Primary Outcome Reporting**: AUC 0.84 (95% CI 0.78–0.90)
- **Primary Outcome Point Estimate**: 0.84
- **Primary Outcome 95 CI Lower**: 0.78
- **Primary Outcome 95 CI Upper**: 0.90
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 140 patients
- **Primary Outcome Threshold**: Predicted probability ≥ 0.4 (optimal for sensitivity)
- **Primary Outcome Metric Definition**: AUC calculated on completely held‑out test cohort of ECG‑biopsy pairs
- **Primary Outcome Timepoints**: ECG obtained up to 30 days before biopsy (baseline screening)
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: AI‑ECG showed high sensitivity (95%) and moderate specificity; prospective study confirmed detection with AUC 0.78.
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.84
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: Sens 0.95, Spec 0.526
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
