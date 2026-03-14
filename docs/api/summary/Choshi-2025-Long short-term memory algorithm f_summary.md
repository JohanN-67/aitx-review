**Core Objective:** To develop and validate a time‑series deep learning model that predicts tacrolimus trough levels (TTL) after lung transplantation using only prior dosing and concentration data, enabling personalized dose adjustments.

**Patient Cohort & Study Scope:** 117 lung transplant recipients (training/validation/testing) plus 6 additional cases for simulation validation; age not explicitly reported. All patients underwent lung transplantation at Okayama University Hospital between April 2011 and May 2023.

**AI/ML Approach:** Multivariate Long Short‑Term Memory (LSTM) neural network (3‑layer architecture) using three prior time points as input. Input modalities limited to tacrolimus dose, route (IV/oral), and previous TTLs (no genetic or extensive laboratory variables).

**Key Findings:** The final LSTM model achieved an R² of 0.67 on the test set. Predicted TTLs were within ±20% of observed values for 74.3% of time points and within ±30% for 88.5% of time points. Mean absolute error decreased across validation cases (4.78 ng/mL at first point to 1.51 ng/mL by third). The tool correctly suggested dose modifications in all six simulation cases, aligning predicted TTLs with target ranges.

**Main Limitations:** Single‑center retrospective design with limited sample size, restricting generalizability.