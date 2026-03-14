**Core Objective:** Develop a hybrid deep‑learning model (MCNN‑HELM) to predict the most suitable donor for transplant candidates and minimize recipient waiting time, with priority given to high‑risk patients.

**Patient Cohort & Study Scope:** Combined real‑time datasets comprising 96,508 donor–recipient records (6,898 liver pairs from the PLTSD registry; 29,210 lung recipients and 60,400 heart recipients from UNOS) covering the period 2012‑2022. Age distribution not reported. Organs included: liver, lung, and heart.

**AI/ML Approach:** Modified Convolutional Neural Network combined with a Hybrid Extreme Learning Machine (MCNN‑HELM); feature optimization via Prairie Dog Optimization algorithm. Input modalities: tabular donor and recipient clinical variables (≈55–57 features per record).

**Key Findings:**  
- Training accuracy = 97.5% (Table 5).  
- Computational time = 2.2 s per run.  
- Precision of estimated factual outcomes (PEFO) = 16.3582.  
- Precision of estimated potential outcomes (PEPO) = 16.1401.  
- Accuracy of best donor type (ABDT) = 0.6784.  
- Outperformed comparative methods (MINLP, IGBFS‑NB, SVM, FO) on all listed metrics.

**Main Limitations:** Retrospective simulation using existing registries with no external prospective validation.