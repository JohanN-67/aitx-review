# Data Extraction Report: Seraphin-2023-Prediction of heart transplant r
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult heart transplant recipients using a deep learning (non‑linear) model to predict cellular rejection, includes relevant post‑transplant outcomes, and is a peer‑reviewed observational study published after 2018.

## Identification & Methods
- **Sponsorship source**: German Federal Ministry of Health (DEEP LIVER), German Cancer Aid, European Research Council, German Research Foundation (DFG)
- **Country**: Germany
- **Setting**: Multicenter study at German university hospitals
- **Comments**: Retrospective analysis of digital pathology images from three transplant centres in Germany.
- **Author_name**: Jakob Nikolas Kather
- **Institution**: Else Kroener Fresenius Center for Digital Health, Technical University Dresden
- **Email**: jakob-nikolas.kather@alumni.dkfz.de
- **Address**: Fetscherstrasse 74, 01307 Dresden, Germany
- **Country of Data Origin**: Germany
- **Dataset Source**: Routine endomyocardial biopsy slides from three German transplant centres (Regensburg, Hamburg-Eppendorf, Aachen)
- **Organ Focus**: Heart
- **Study Period End**: 2021
- **Study Period Start**: 1999
- **Identification Notes**: Included heart transplant biopsy slides with ISHLT grading; excluded slides without grading information.
- **Design**: Retrospective cohort (case series) with cross‑validation and external validation.
- **AI Model Architecture**: Attention‑based multiple instance learning using a self‑supervised pre‑trained RetCCL encoder.
- **Class Imbalance**: NR
- **Comparator**: CRANE deep learning pipeline
- **Input Variables**: Whole slide H&E‑stained histopathology images (tiles of 512×512 px).
- **ML Primary Component**: Yes
- **Missing Data Handling**: NR
- **Validation Method**: Three‑fold cross‑validation repeated five times with external validation on three independent cohorts; also 10‑fold Monte Carlo CV for CRANE comparator.
- **Methods Notes**: Images digitized at ×40, tessellated into patches; features extracted with RetCCL; attention scores computed per tile; Adam optimizer, early stopping after 16 epochs without loss reduction; training on up to 512 tiles per slide.

## Population Characteristics
- **Inclusion criteria**: NR
- **Exclusion criteria**: NR
- **Sample Size Total**: 325
- **Target Population**: Heart transplant recipients
- **Population Notes**: Four retrospective case series cohorts from three German centres (Regensburg, Hamburg, Aachen) comprising 1079 histopathology slides from 325 patients.
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
- **Specific Algorithm Name**: SSL-attention-MIL (self-supervised learning with attention-based multiple instance learning)
- **Intervention Input Data Modality**: Routine H&E-stained whole slide pathology images
- **Number of Predictors**: 2048-dimensional feature vectors per image tile
- **Feature Selection Method**: NR
- **Temporal Handling**: Static (no temporal component)
- **Interventions Notes**: Trained on Cohort 1 using three‑fold cross‑validation (repeated five times), evaluated on three external cohorts; used self‑supervised pre‑trained RetCCL encoder and attention MIL; compared against CRANE pipeline.
- **Reported outcomes in study**: Area under the receiver operating curve (AUROC) for binary rejection prediction and for ISHLT grade prediction
- **Outcomes Notes**: Primary outcome is AUROC for binary (yes/no) rejection; secondary outcomes are AUROCs for ISHLT grades 0R, 1R, 2/3R
- **Result data Notes**: Mean cross‑validated AUROC 0.849 (95 % CI 0.822–0.877) for binary prediction; external validation AUROCs 0.734, 0.729, 0.716 across cohorts; grade AUROCs also reported.
- **Primary Outcome Reported name**: Binary heart transplant rejection (yes/no) AUROC
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: CRANE method
- **Primary Outcome Reported as**: Area under the receiver operating curve (AUROC)
- **Primary Outcome Reference arm**: CRANE cross‑validated AUROC 0.776 (95 % CI 0.717–0.835)
- **Primary Outcome group**: All slides in Cohort 1 (training cohort) during cross‑validation
- **Primary Outcome Reporting**: Mean AUROC 0.849 (95 % CI 0.822–0.877)
- **Primary Outcome Point Estimate**: 0.849
- **Primary Outcome 95 CI Lower**: 0.822
- **Primary Outcome 95 CI Upper**: 0.877
- **Primary Outcome p-value**: <0.001
- **Primary Outcome Test Set Size**: 393 slides (Cohort 1)
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: AUROC calculated on held‑out test folds of three‑fold cross‑validation
- **Primary Outcome Timepoints**: NR
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: High discrimination in internal cross‑validation; performance decreased modestly in external cohorts.
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
