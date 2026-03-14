# Data Extraction Report: Lisboa et al. - 2022 - Enhanced survival prediction using explainable artificial intelligence in heart transplantation
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult heart transplant recipients using a neural network (non‑linear AI) to predict 1‑year mortality, includes relevant outcomes and comparator, and is a peer‑reviewed article published after 2018.

## Identification & Methods
- **Sponsorship source**: Swedish Research Council, Vinnova, Swedish Heart-Lung Foundation, region Skane research funds, donation funds from Skane University Hospital, Anna-Lisa and Sven Eric Lundgrens Foundation
- **Country**: Sweden
- **Setting**: NR
- **Comments**: Retrospective cohort study of heart transplantation using UNOS and Scandinavian registries to develop and externally validate an interpretable self‑explaining neural network (Partial Response Network) against deep learning, IHTSA and IMPACT models.
- **Author_name**: Paulo J. G. Lisboa
- **Institution**: Liverpool John Moores University; Lund University
- **Email**: johan.nilsson@med.lu.se
- **Address**: Lund, Sweden
- **Country of Data Origin**: USA
- **Dataset Source**: UNOS SRTR registry and Scandia Thoracic Transplantation Database
- **Organ Focus**: Heart
- **Study Period End**: 2020
- **Study Period Start**: 1987
- **Identification Notes**: Included adult heart transplant recipients (≥18 y); excluded pediatric cases, donor age <15 y and records with missing mandatory data.
- **Design**: Retrospective Cohort with temporal derivation (1997‑2013), test (2014‑2016) and external blinded validation cohorts (2017‑2018).
- **AI Model Architecture**: Self‑explaining neural network (Partial Response Network) with ANOVA decomposition, Lasso‑regularised GAM; benchmarked against deep learning model and IHTSA/IMPACT.
- **Class Imbalance**: Handled by PRN probabilistic threshold adjustment for class assignment.
- **Comparator**: International Heart Transplant Survival Algorithm (IHTSA), IMPACT score, Explainable Boosting Machines (EBM).
- **Input Variables**: Recipient age, donor age, creatinine, ischemic time, ventilator at OHT, diagnosis (non‑ischemic cardiomyopathy), recipient female gender, infection within 2 weeks, transplant year, plus a two‑way interaction (recipient age × ICM).
- **ML Primary Component**: Yes
- **Missing Data Handling**: Multiple imputation (probability imputation with stratified era) for UNOS data; median imputation for Scandinavian dataset.
- **Validation Method**: Temporal split (derivation, test, external validation); five‑fold cross‑validation for recalibrated IHTSA; external cohorts from UNOS (2017‑2018) and Scandia database.
- **Methods Notes**: Data extracted from UNOS SRTR (1987‑onward) and Scandia registry; ANOVA decomposition to obtain partial responses; Lasso for variable selection; GAM for interpretability; statistical analysis with Stata 16.1, Mann‑Whitney U, chi‑square, Hosmer–Lemeshow, AUROC with DeLong test.

## Population Characteristics
- **Inclusion criteria**: Heart transplant recipients from UNOS registry between Jan 1 1987 and Jun 30 2020 meeting mandatory data completeness; adult recipients (≥18 years)
- **Exclusion criteria**: Pediatric recipients (<18 years), donor age <15 years, missing mandatory data (age, sex, follow‑up duration, vital status)
- **Sample Size Total**: 42185
- **Target Population**: Recipients
- **Population Notes**: Three cohorts: derivation (n=31,315), test (n=6,120) and external blinded validation (n=4,750); cohorts differ in age, BMI, comorbidities
- **Recipient Mean Age**: 54
- **Recipient Mean Age Overall**: 54
- **Recipient Female Sex Pct**: 26%
- **Recipient Female Sex Pct Overall**: 24%
- **Mean BMI**: NR
- **Mean BMI Overall**: NR
- **Diagnosis**: Non‑ischemic cardiomyopathy (NICM) most common (60% in validation cohort)
- **Diagnosis Overall**: Non‑ischemic cardiomyopathy most common overall (46.7%)
- **Diabetes Pct**: 29%
- **Diabetes Pct Overall**: 24%
- **Pre-transplant Support**: Ventilator at OHT 0.9% (validation cohort)
- **Pre-transplant Support Overall**: Ventilator at OHT 2.6% (overall)
- **Mean Creatinine**: 120 µmol/L
- **Mean Creatinine Overall**: 119 µmol/L
- **Donor Mean Age**: 33 years
- **Donor Mean Age Overall**: 32 years
- **Ischemic Time**: 183 min
- **Ischemic Time Overall**: 187 min

## Interventions & Outcomes
- **Specific Algorithm Name**: Partial Response Network (PRN) with Lasso (PRN-Lasso)
- **Intervention Input Data Modality**: Tabular clinical variables (recipient and donor characteristics, demographics, physiological measurements)
- **Number of Predictors**: 10 (nine univariate effects plus one two‑way interaction)
- **Feature Selection Method**: LASSO (L1 regularisation) applied to partial responses
- **Temporal Handling**: Derivation cohort 1997–2013, test cohort 2014–2016, external blinded validation cohort 2017–2018 (temporal validation)
- **Interventions Notes**: Self‑explaining neural network (PRN) benchmarked against deep learning IHTSA and traditional IMPACT models; external validation on UNOS (n=4750) and Scandinavian (n=2293) datasets.
- **Reported outcomes in study**: 1‑year mortality (AUROC)
- **Outcomes Notes**: Primary outcome is classification of death within one year after heart transplantation.
- **Result data Notes**: AUROC for PRN-Lasso in external validation cohort: 0.628 (95% CI 0.602–0.654); comparable to IHTSA (0.635) and superior to IMPACT (0.602).
- **Primary Outcome Reported name**: 1‑year mortality
- **Primary Outcome type**: Classification
- **Primary Outcome Reported against**: IHTSA, IHTSA recalibrated, IMPACT, EBM
- **Primary Outcome Reported as**: AUROC (area under the ROC curve)
- **Primary Outcome Reference arm**: IHTSA AUROC 0.635 (95% CI 0.609–0.662)
- **Primary Outcome group**: Heart transplant recipients in the external blinded validation cohort (UNOS 2017–2018, n = 4750)
- **Primary Outcome Reporting**: AUROC 0.628 (95% CI 0.602–0.654)
- **Primary Outcome Point Estimate**: 0.628
- **Primary Outcome 95 CI Lower**: 0.602
- **Primary Outcome 95 CI Upper**: 0.654
- **Primary Outcome p-value**: 0.488 (comparison with IHTSA)
- **Primary Outcome Test Set Size**: 4750
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Area under the ROC curve calculated on a completely held‑out external validation cohort
- **Primary Outcome Timepoints**: 1 year post‑transplant
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: 1 year
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: PRN‑Lasso achieved similar discrimination to deep learning models while being interpretable and well calibrated.
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: 0.628
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
