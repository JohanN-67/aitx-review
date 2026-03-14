# Data Extraction Report: Gnanasambandhan-2023-HEL-MCNN_ Hybrid extreme
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The 2023 peer‑reviewed observational study uses a non‑linear deep learning model (MCNN‑HELM) on adult heart, lung and liver transplant datasets to predict donor–recipient matching and survival outcomes, meeting population, intervention, outcome, and study design criteria.

## Identification & Methods
- **Sponsorship source**: NR
- **Country**: India
- **Setting**: NR
- **Comments**: Proposes MCNN-HELM model using three real-time organ datasets to minimize waiting time.
- **Author_name**: G. Sangeetha; Vanathi Balasubramanian
- **Institution**: Department of Computer Science and Engineering, SRM Valliammai Engineering College
- **Email**: sangeethag.cse@srmvalliammai.ac.in; vanathib.cse@srmvalliammai.ac.in
- **Address**: Kattankulathur, Chennai, Tamil Nadu, India
- **Country of Data Origin**: UK and USA
- **Dataset Source**: Paired Liver Transplant Standard Dataset (PLTSD), UNOS Lung (UNOS-LU) and UNOS Heart (UNOS-HR) datasets
- **Organ Focus**: Liver, Heart, Lung
- **Study Period End**: NR
- **Study Period Start**: NR
- **Identification Notes**: Includes real-time datasets of donor-recipient pairs for liver, heart, and lung transplantation.
- **Design**: NR
- **AI Model Architecture**: Hybrid extreme learning modified convolutional neural network (MCNN-HELM) with prairie dog optimizer
- **Class Imbalance**: NR
- **Comparator**: Compared against MINLP, IGBFS-NB, SVM, and fuzzy optimization models
- **Input Variables**: Donor and recipient features (e.g., 28 donor features, 55 recipient features) from the datasets
- **ML Primary Component**: Yes
- **Missing Data Handling**: Pre-processing removed missing and inaccurate values
- **Validation Method**: Train-test split with 80% training and 20% testing
- **Methods Notes**: Prairie dog optimization fine-tunes MCNN parameters; ELM replaces softmax classifier for output layer.

## Population Characteristics
- **Inclusion criteria**: NR
- **Exclusion criteria**: NR
- **Sample Size Total**: NR
- **Target Population**: NR
- **Population Notes**: NR
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
- **Specific Algorithm Name**: Modified CNN-HELM with Prairie Dog Optimization
- **Intervention Input Data Modality**: Tabular records from three real-time organ transplantation datasets (liver, heart, lung)
- **Number of Predictors**: NR
- **Feature Selection Method**: NR
- **Temporal Handling**: NR
- **Interventions Notes**: Preprocessing to remove missing/incorrect values, MCNN-HELM model training with PDO for hyperparameter tuning, ELM classifier replaces softmax
- **Reported outcomes in study**: Training accuracy, computational time, precision of estimated factual outcomes (PEFO), precision of estimated potential outcomes (PEPO), accuracy of best donor type (ABDT)
- **Outcomes Notes**: Metrics used to evaluate model performance compared to state-of-the-art methods
- **Result data Notes**: Comparative analysis shows MCNN-HELM outperforms MINLP, IGBFS-NB, SVM, FO on all reported metrics
- **Primary Outcome Reported name**: Training accuracy
- **Primary Outcome type**: Classification performance metric
- **Primary Outcome Reported against**: MINLP, IGBFS-NB, SVM, FO models
- **Primary Outcome Reported as**: Percentage
- **Primary Outcome Reference arm**: MINLP training accuracy 79%
- **Primary Outcome group**: All transplant recipient pairs in test set
- **Primary Outcome Reporting**: 97.5%
- **Primary Outcome Point Estimate**: 97.5
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: NR
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Proportion of correctly predicted donor-recipient matches on held-out test data
- **Primary Outcome Timepoints**: NR
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: High training accuracy indicates effective model learning
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
