# Data Extraction Report: Kozinski et al. - 2025 - Harnessing deep learning to detect bronchiolitis obliterans syndrome from chest CT
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study involves adult lung transplant recipients and uses a deep neural network (a non‑linear AI model) to detect bronchiolitis obliterans syndrome, comparing its performance to current clinical practice, and reports clinically relevant outcomes related to post‑transplant complications. It meets all inclusion criteria for population, intervention, comparator, outcomes, and study characteristics.

## Identification & Methods
- **Sponsorship source**: FWF Austrian Science Fund, Swiss Cancer League, SNSF grants
- **Country**: Switzerland
- **Setting**: Retrospective single-center study at University Hospital of Lausanne
- **Comments**: Retrospective review of CT scans from lung transplant recipients (75 patients, 228 scans) with BOS and non‑BOS groups.
- **Author_name**: Mateusz Koziński
- **Institution**: Institute of Computer Graphics and Vision, Technische Universität Graz; NeuraVision Research Lab, Bilkent University; EPFL; Lausanne University Hospital (CHUV)
- **Email**: nahal.mansouri@chuv.ch
- **Address**: Lausanne, Switzerland
- **Country of Data Origin**: Switzerland
- **Dataset Source**: Hospital picture archiving and communication system (PACS) CT scans
- **Organ Focus**: Lung
- **Study Period End**: 2020
- **Study Period Start**: 1990
- **Identification Notes**: Included lung transplant recipients with CT scans; excluded scans with pixel size >0.75 mm or <50 transverse slices; removed scans with extensive infiltrates.
- **Design**: Retrospective Cohort
- **AI Model Architecture**: Late‑fusion deep neural network processing 2D CT slices with auxiliary temporal order task
- **Class Imbalance**: NR
- **Comparator**: NR
- **Input Variables**: Raw thoracic CT scans (standard, thin‑slice, high‑resolution); auxiliary task uses paired scans for temporal ordering
- **ML Primary Component**: Yes
- **Missing Data Handling**: NR
- **Validation Method**: Five‑fold cross‑validation (five splits of BOS and non‑BOS patients)
- **Methods Notes**: Co‑training with auxiliary temporal order task, random slice dropout during training, late‑fusion architecture to reduce overfitting; hierarchical bootstrapping for confidence intervals.

## Population Characteristics
- **Inclusion criteria**: NR
- **Exclusion criteria**: Scans with pixel size >0.75 mm, <50 transverse slices, and scans with extensive lung infiltrates were excluded
- **Sample Size Total**: 75
- **Target Population**: Lung transplant recipients
- **Population Notes**: Retrospective single‑center study; initially 130 lung transplant recipients identified, of which 75 patients (26 with BOS, 49 without) had usable CT scans for analysis
- **Recipient Mean Age**: 46.77 (BOS) / 47.75 (non‑BOS)
- **Recipient Mean Age Overall**: NR
- **Recipient Female Sex Pct**: 65.4% (BOS) / 55.1% (non‑BOS)
- **Recipient Female Sex Pct Overall**: 58.7%
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Bronchiolitis obliterans syndrome (BOS) after lung transplantation
- **Diagnosis Overall**: Bronchiolitis obliterans syndrome (BOS) after lung transplantation
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
- **Specific Algorithm Name**: Deep Neural Network with co‑training (late‑fusion architecture, random slice dropout, auxiliary temporal order task)
- **Intervention Input Data Modality**: Thoracic chest CT scans (standard, thin‑slice, or high‑resolution)
- **Number of Predictors**: NR
- **Feature Selection Method**: NR
- **Temporal Handling**: Auxiliary task predicts temporal order of scan pairs; inference on single CT scan
- **Interventions Notes**: Co‑training to enhance low‑data performance, late‑fusion DNN, random slice dropout during training, auxiliary temporal precedence prediction
- **Reported outcomes in study**: BOS detection (ROC‑AUC), stage‑specific AUC, risk prediction AUC
- **Outcomes Notes**: Primary outcome is classification of BOS vs non‑BOS using ROC‑AUC
- **Result data Notes**: Aggregated ROC‑AUC 0.90 (95% CI 0.840–0.953) across five‑fold cross‑validation
- **Primary Outcome Reported name**: BOS detection (presence vs absence)
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: NR
- **Primary Outcome Reported as**: ROC‑AUC
- **Primary Outcome Reference arm**: NR
- **Primary Outcome group**: All lung transplant patients in study (26 BOS, 49 non‑BOS)
- **Primary Outcome Reporting**: AUC 0.90 (95% CI 0.840–0.953)
- **Primary Outcome Point Estimate**: 0.90
- **Primary Outcome 95 CI Lower**: 0.840
- **Primary Outcome 95 CI Upper**: 0.953
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 228 scans (aggregated across five folds)
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Receiver operating characteristic area under curve on aggregated test predictions across five independently trained DNNs
- **Primary Outcome Timepoints**: NR
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: Performance consistent across scan resolutions; comparable to radiologist reports
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
