**Core Objective:** To develop and validate a machine‑learning model for predicting 1‑year mortality after orthotopic heart transplantation (HTx) in a Chinese cohort.

**Patient Cohort & Study Scope:** 381 HTx recipients (mean age 43.8 ± 16.5 years; 76.2% male) transplanted between 1 Jan 2015 and 31 Dec 2018; only heart transplants were included.

**AI/ML Approach:** Seven algorithms evaluated (Random Forest, Gradient Boosting Machine, XGBoost, Adaptive Boosting, Logistic Regression, Support Vector Machine, Artificial Neural Network) using 13 pre‑operative variables selected by LASSO; input data were tabular electronic medical record features (laboratory, imaging, clinical history).

**Key Findings:**  
- Random Forest achieved the highest discrimination: **AUC 0.801 (95% CI 0.697–0.891)**, **accuracy 0.828**, **sensitivity 0.268**, **specificity 0.927**.  
- Gradient Boosting Machine showed AUC 0.786 and the best sensitivity among models (**0.271**).  
- Top predictive features (SHAP) were albumin, recipient age, left atrial diameter, red blood cell count, and hemoglobin.  
- All models exhibited low sensitivity for positive (mortality) cases.

**Main Limitations:** Retrospective single‑center design with a relatively small sample and limited number of mortality events, leading to modest sensitivity.