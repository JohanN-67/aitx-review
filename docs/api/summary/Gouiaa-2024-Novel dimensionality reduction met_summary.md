**Core Objective:** To predict acute cellular rejection (ACR) risk after lung transplantation using a topological autoencoder‑based dimensionality reduction (Taelcore) combined with machine learning classifiers.

**Patient Cohort & Study Scope:** 40 lung transplant recipients (median age 60 years, IQR 52–64; 70% male); ACR occurred in 7 patients (17.5%) within one year. Study period not explicitly reported.

**AI/ML Approach:** Topological autoencoder (Taelcore) integrating persistent homology (Rips filtration, persistence diagrams vectorised by entropy). Classifiers evaluated: Multilayer Perceptron (MLP), Random Forest, k‑Nearest Neighbours, Gaussian Naive Bayes. Input features: nine early postoperative biomarkers (sCD31 H24/48/72, PaO₂/FiO₂ H24/48/72, SOFA‑respiratory H24/48/72).

**Key Findings:**  
- Baseline (no topology) balanced accuracy: MLP 80%, GNB 90%, RF 50%, KNN 50%.  
- After topological improvement, MLP and GNB each achieved **90% accuracy** (balanced), while RF remained 50% and KNN 50%.  
- Overall model reported an **accuracy of 90%** for ACR prediction using the Taelcore‑enhanced pipeline.  
- Dimensionality reduced by ≈ 70% without loss of predictive performance.

**Main Limitations:** Retrospective single‑center study with a very small, imbalanced dataset and no external validation.