**Core Objective:** To develop and evaluate machine‑learning models that predict the occurrence of de novo malignancies in lung transplant recipients without prior cancer history.

**Patient Cohort & Study Scope:** 30,917 lung transplant patients (25 % developed malignancy) from the UNOS STAR registry; age range not specified, mean/median not reported. Transplants performed between 1984 and 2021 in the United States.

**AI/ML Approach:** Tested multiple algorithms on tabular EMR‑derived features (544 variables reduced to 371 after preprocessing). Models included Gradient Boosting, Random Forest, Decision Tree, Least Angle Regression, Neural Network (MLP), Logistic Regression, Rule Induction, and Support Vector Machine. Input modalities were solely structured clinical/demographic/laboratory data.

**Key Findings:** Gradient Boosting achieved the best discrimination (AUROC = 0.746). Its performance metrics: Accuracy = 0.690, Sensitivity = 0.731, Specificity = 0.649, Precision = 0.676. Important predictors (ranked by importance) were DR52 antigen, BMI, CMV IgG status, total serum albumin, and ECMO use. Random Forest showed highest sensitivity (0.726) but lower AUROC (0.731). All other models yielded AUROCs between 0.694 and 0.712.

**Main Limitations:** Retrospective single‑center analysis with no external validation cohort.