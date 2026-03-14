**Core Objective:** To evaluate whether machine‑learning (ML) models improve prediction of 1‑year survival after adult heart transplantation compared with traditional statistical methods.

**Patient Cohort & Study Scope:** 50,453 adult heart transplant recipients (age ≥ 18 y) from the UNOS registry, transplanted between 1987 and 2014 (analysis focused on three periods: 1987‑1996, 1996‑2006, 2006‑2014).

**AI/ML Approach:** Traditional models – logistic regression, ridge regression, LASSO. ML models – neural network (multilayer perceptron), naïve Bayes, tree‑augmented naïve Bayes, support vector machine (SVM), random forest, stochastic gradient boosting. Input data: tabular pre‑transplant clinical variables (donor/recipient age, creatinine, BMI, liver tests, hemodynamics, etc.).

**Key Findings:** All models yielded modest discrimination (C‑statistic ≈ 0.65).  
- Neural network achieved the highest C‑statistic of **0.66** (range 0.66–0.67 across validation folds).  
- Logistic regression, ridge, and LASSO each had C‑statistic **0.65**.  
- Other ML models: random forest 0.63, tree‑augmented naïve Bayes 0.62, SVM 0.52.  
- Performance comparable to the established IMPACT score (C‑statistic 0.65). Calibration was good for traditional models and random forest/gradient boosting; inferior for several ML models.

**Main Limitations:** Retrospective single‑nation registry with limited variable granularity and no external validation.