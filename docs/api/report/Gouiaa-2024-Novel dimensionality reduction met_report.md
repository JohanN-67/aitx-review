# Data Extraction Report: Gouiaa-2024-Novel dimensionality reduction met
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Requires Human Review (Rejected by LLM)

## Eligibility
- **Eligibility Status**: Not Accepted
- **Eligibility Rationale**: The study uses non‑linear AI models on adult lung transplant recipients, but it does not compare the predictions to current clinical practice (gold standard), lacking a required comparator.

## Identification & Methods
- **Sponsorship source**: National Research Association (ANR) (Inflamex renewal 10-LABX-0017), Consejería de Universidades, fondos FEDER de la Junta de Andalucía (ProyExec_0499), DHU FIRE Emergence 4, l’Agence de la Biomedecine
- **Country**: France
- **Setting**: Hospital-based clinical cohort of lung transplant patients
- **Comments**: Open access article; uses recycled dataset from a previous study on soluble CD31 risk prediction
- **Author_name**: Fatma Gouiaa
- **Institution**: Université Sorbonne Paris Nord, LAGA, CNRS, UMR 7539, Laboratoire d’excellence Inflamex, Villetaneuse, France
- **Email**: morilla@math.univ-paris13.fr
- **Address**: University of Malaga, Department of Genetics, MLiMO, 29010, Málaga, Spain
- **Country of Data Origin**: France
- **Dataset Source**: Personalised Risk Predictor for Acute Cellular Rejection in Lung Transplant Using Soluble CD31 (previous study)
- **Organ Focus**: Lung
- **Study Period End**: NR
- **Study Period Start**: NR
- **Identification Notes**: Included 40 lung transplant patients; 7 (17.5%) experienced acute cellular rejection within one year
- **Design**: Retrospective cohort
- **AI Model Architecture**: Multilayer Perceptron, Autoencoder, Random Forest, k-Nearest Neighbours, Gaussian Naive Bayes
- **Class Imbalance**: Handled by stratified k‑fold cross‑validation and balanced mini‑batches (≈5% of each class per batch)
- **Comparator**: Standard machine learning models without topological improvement
- **Input Variables**: CD31 H24, CD31 H48, CD31 H72, PaO2/FiO2 H24, PaO2/FiO2 H48, PaO2/FiO2 H72, SOFA respiratory H24, SOFA respiratory H48, SOFA respiratory H72
- **ML Primary Component**: Yes
- **Missing Data Handling**: NR
- **Validation Method**: Stratified k‑fold cross‑validation (75% train, 25% test)
- **Methods Notes**: Proposed topological autoencoder (Taelcore) with topological loss based on persistence diagram entropy; class balancing in mini‑batches; evaluation using KL divergence, RMSE, TRUST, MSE

## Population Characteristics
- **Inclusion criteria**: NR
- **Exclusion criteria**: NR
- **Sample Size Total**: 40
- **Target Population**: Lung transplant recipients
- **Population Notes**: Clinical dataset of 40 patients; 7 (17.5%) experienced acute cellular rejection within one year.
- **Recipient Mean Age**: NR
- **Recipient Mean Age Overall**: NR
- **Recipient Female Sex Pct**: NR
- **Recipient Female Sex Pct Overall**: NR
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Emphysema (33%), interstitial lung disease (50%), other etiologies (17.5%)
- **Diagnosis Overall**: Emphysema (33%), interstitial lung disease (50%), other etiologies (17.5%)
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
- **Specific Algorithm Name**: Taelcore (topological autoencoder with best linear combination), also using Multilayer Perceptron (MLP) and Autoencoder (AE)
- **Intervention Input Data Modality**: Clinical numeric variables (CD31 levels, PaO2/FiO2 ratios, SOFA respiratory scores) measured during first 3 days post‑transplant
- **Number of Predictors**: 9 clinical characteristics
- **Feature Selection Method**: NR
- **Temporal Handling**: Static baseline data (measurements within first 3 days)
- **Interventions Notes**: Topological autoencoder (Taelcore) combines TDA (Rips filtration, persistence diagrams, entropy vectorisation) with machine learning classifiers; grid search for hyper‑parameters; stratified k‑fold cross‑validation; 75/25 train‑test split
- **Reported outcomes in study**: Prediction of acute cellular rejection (ACR) risk after lung transplantation
- **Outcomes Notes**: Primary outcome is binary classification of ACR vs non‑ACR within one year
- **Result data Notes**: Applying topological improvement increased MLP accuracy from 80% to 90%; overall model achieved 90% accuracy for ACR prediction
- **Primary Outcome Reported name**: Acute cellular rejection (ACR) risk prediction
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: Model without topological improvement (baseline MLP)
- **Primary Outcome Reported as**: Accuracy
- **Primary Outcome Reference arm**: Baseline MLP accuracy 80%
- **Primary Outcome group**: Lung transplant recipients (n=40)
- **Primary Outcome Reporting**: Accuracy 90%
- **Primary Outcome Point Estimate**: 0.90
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Classification accuracy on held‑out test set after applying Taelcore dimensionality reduction
- **Primary Outcome Timepoints**: Within one year post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Significant improvement over baseline model without topological features
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: 0.90
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
