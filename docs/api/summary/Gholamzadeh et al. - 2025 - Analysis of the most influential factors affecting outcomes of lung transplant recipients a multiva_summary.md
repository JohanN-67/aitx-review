**Core Objective:** To develop a machine‑learning model that predicts the allocation priority score for lung transplant candidates and to identify the most influential pre‑transplant variables affecting that priority.

**Patient Cohort & Study Scope:** 32,966 adult lung transplant recipients (≥18 y) from the UNOS database, median age 54.3 ± 14.2 y, 66.9% male; transplants performed between 2005 and 2022 (data extracted up to 2023).

**AI/ML Approach:** Six regression models were trained on tabular EMR data (15 selected features after feature engineering): Multiple Linear Regression, Random Forest Regressor, Support Vector Machine Regressor, XGBoost Regressor, Multilayer Perceptron, and a Deep Learning model. The Random Forest (n_estimators = 90, max_depth = 10, max_features = sqrt) achieved the best performance.

**Key Findings:**  
- Random Forest yielded an R² of **95.168 %** (Adjusted R² = 95.163 %).  
- Lowest error metrics: MAE **2.056**, RMSE **3.542**, MSE **12.548**.  
- SHAP analysis identified the top 11 predictors (e.g., INIT_O2, diagnosis group, waiting time).  
- XGBoost performed second best (R² = 82.88 %). All other models had R² < 66 %.

**Main Limitations:** Single‑center, retrospective design with no external validation beyond the UNOS dataset.