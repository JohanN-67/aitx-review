**Core Objective:** Evaluate whether the traditional 6‑status heart allocation system accurately ranks urgency of adult heart transplant candidates and compare its performance to multivariable predictive models for death before transplantation.

**Patient Cohort & Study Scope:** 32,294 adult heart transplant candidates (mean age 53 y; 73.7% male) listed between 2010‑2017 (training) and November 2018–March 2020 (post‑policy test). Only heart transplants (no heart‑lung) were included.

**AI/ML Approach:** Developed Cox proportional hazards (CPH) and Random Survival Forest (RSF) models using pre‑policy registry data. Input variables: demographics, diagnosis, laboratory values (e.g., GFR), hemodynamics (PCWP, PAP, cardiac index), and support therapies (IABP, ECMO, LVAD, etc.).

**Key Findings:**  
- 6‑status system C‑index = 0.67 (95% CI 0.63–0.71).  
- CPH with treatment variables: C‑index = 0.76 (95% CI 0.72–0.79), p < 0.001 vs 6‑status.  
- RSF with treatment variables: C‑index = 0.74 (95% CI 0.70–0.78), p = 0.011 vs 6‑status.  
- Models without treatment variables still outperformed 6‑status (CPH 0.69, RSF 0.70).  
- Variable importance: GFR highest (RSF‑T = 0.093), followed by ECMO (0.089).  
- 90‑day Brier scores: CPH‑T = 0.0340, RSF‑T = 0.0345 (both better calibrated than 6‑status).

**Main Limitations:** Retrospective single‑center registry analysis lacking external validation.