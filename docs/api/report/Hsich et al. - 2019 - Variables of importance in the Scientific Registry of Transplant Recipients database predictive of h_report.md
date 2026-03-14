# Data Extraction Report: Hsich et al. - 2019 - Variables of importance in the Scientific Registry of Transplant Recipients database predictive of h
---
## Metadata
- **Form**: Data Extraction
- **Reviewer**: Extractor Script V2
- **Status**: Complete

## Eligibility
- **Eligibility Status**: Accepted
- **Eligibility Rationale**: The study analyzes adult heart transplant candidates using a Random Survival Forest (non‑linear AI) to predict waitlist mortality, meeting population, intervention, outcome, and study design criteria.

## Identification & Methods
- **Sponsorship source**: National Heart, Lung, and Blood Institute (NIH)
- **Country**: USA
- **Setting**: NR
- **Comments**: Retrospective analysis of SRTR data to identify variables predictive of heart transplant waitlist mortality.
- **Author_name**: Eileen M. Hsich
- **Institution**: Cleveland Clinic, Heart and Vascular Institute
- **Email**: Hsiche@ccf.org
- **Address**: Cleveland, Ohio, USA
- **Country of Data Origin**: USA
- **Dataset Source**: Scientific Registry of Transplant Recipients (SRTR)
- **Organ Focus**: Heart
- **Study Period End**: August 31, 2015
- **Study Period Start**: January 1, 2004
- **Identification Notes**: Included adult candidates >18 years on active heart transplant waiting list; excluded inactive (UNOS Status 7) and pediatric candidates.
- **Design**: Retrospective cohort
- **AI Model Architecture**: Random Survival Forest (RSF)
- **Class Imbalance**: NR
- **Comparator**: NR
- **Input Variables**: Demographics (age, sex, race, BMI), clinical labs (eGFR, serum albumin), device support (ECMO, VAD, IABP, LVAD, RVAD, TAH), hemodynamics (PCWP, PAP, cardiac index), functional capacity (peak VO2), comorbidities (diabetes, hypertension, tobacco use, malignancy, stroke, vascular disease), insurance, blood type, diagnosis.
- **ML Primary Component**: Yes
- **Missing Data Handling**: Imputed using missForest algorithm.
- **Validation Method**: Out-of-bag (OOB) internal validation with bootstrap sampling; variable importance assessed via OOB error.
- **Methods Notes**: Used RSF to rank variable importance, handle missing data, and explore complex interactions; partial plots generated for selected variables.

## Population Characteristics
- **Inclusion criteria**: Adult candidates on the active heart transplant waiting list in the SRTR database between Jan 1, 2004 and Aug 31, 2015
- **Exclusion criteria**: Inactive candidates (UNOS Status 7) and candidates <18 years of age
- **Sample Size Total**: 33069
- **Target Population**: Heart transplant waitlist candidates (adults)
- **Population Notes**: 33,069 adult candidates; UNOS Status distribution: 7,681 status 1A, 13,027 status 1B, 12,361 status 2; median follow‑up 4.3 months; 5,514 deaths during follow‑up
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
- **Specific Algorithm Name**: Random Survival Forests
- **Intervention Input Data Modality**: SRTR registry clinical variables at time of listing
- **Number of Predictors**: NR
- **Feature Selection Method**: Variable importance (VIMP) using out-of-bag data and Harrell's concordance index
- **Temporal Handling**: Static baseline variables at initial wait‑list listing
- **Interventions Notes**: Machine learning RSF applied to pre‑listing variables; missing data imputed with missForest
- **Reported outcomes in study**: All‑cause waitlist mortality (time from listing to death)
- **Outcomes Notes**: Primary endpoint was all‑cause mortality censored at transplant or end of follow‑up
- **Result data Notes**: Identified eGFR, serum albumin, ECMO, VADs, ventilation, etc. as most important predictors of waitlist mortality
- **Primary Outcome Reported name**: All‑cause waitlist mortality
- **Primary Outcome type**: Survival (time‑to‑event)
- **Primary Outcome Reported against**: NR
- **Primary Outcome Reported as**: NR
- **Primary Outcome Reference arm**: NR
- **Primary Outcome group**: All adult heart transplant candidates on the active waitlist (N=33,069)
- **Primary Outcome Reporting**: NR
- **Primary Outcome Point Estimate**: NR
- **Primary Outcome 95 CI Lower**: NR
- **Primary Outcome 95 CI Upper**: NR
- **Primary Outcome p-value**: NR
- **Primary Outcome Test Set Size**: 33,069
- **Primary Outcome Threshold**: NR
- **Primary Outcome Metric Definition**: Variable importance (VIMP) based on change in Harrell's C‑index
- **Primary Outcome Timepoints**: Overall follow‑up (median 4.3 months); survival curves presented up to 5 years
- **Primary Outcome In-Hospital Reported time**: NR
- **Primary Outcome 1-Year Reported time**: NR
- **Primary Outcome Late Reported time**: NR
- **Primary Outcome Notes**: eGFR and serum albumin were strong predictors not currently included in allocation system
- **Res_Primary InHosp AUC**: NR
- **Res_Primary InHosp Accuracy**: NR
- **Res_Primary InHosp Sens_Spec**: NR
- **Res_Primary 1Yr AUC**: NR
- **Res_Primary 1Yr Accuracy**: NR
- **Res_Primary 1Yr Sens_Spec**: NR
- **Res_Primary Late AUC**: NR
- **Res_Primary Late Accuracy**: NR
- **Res_Primary Late Sens_Spec**: NR
