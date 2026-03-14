**Core Objective:**  
To develop and compare machine‑learning models for early prediction of intensive care unit length of stay (ICU‑LOS) in patients after heart transplantation.

**Patient Cohort & Study Scope:**  
365 consecutive heart transplant recipients (median age 47.2 y; donor median age 35.6 y) treated at Union Hospital, Wuhan, China from April 2017 to August 2020. All patients underwent heart transplantation (NYHA III–IV).

**AI/ML Approach:**  
Four classifiers—XGBoost, Random Forest, Naive Bayes, Support Vector Machine—and logistic regression were trained on 84 pre‑operative/ intra‑operative variables. Feature reduction used LASSO (5‑fold CV) to select six key predictors; model interpretation employed SHAP values. Data split: training N=256, testing N=109 (7:3).

**Key Findings:**  
- XGBoost achieved the highest performance: AUC‑ROC 0.88 (95% CI 0.857–0.928), Accuracy 0.878, Sensitivity 0.988, Specificity 0.519, PPV 0.870, NPV 0.932.  
- Logistic regression: AUC‑ROC 0.816, Accuracy 0.844.  
- Other models: NB AUC 0.821, RF AUC 0.783, SVM AUC 0.784.  
- Six most important features (ranked by SHAP): ECMO use, donor age, IABP use, surgery duration, high creatinine, CRRT use.

**Main Limitations:**  
Single‑center retrospective design with a modest sample size and no external validation.