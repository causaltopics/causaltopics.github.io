---
week: 2
lecture: "L02"
date: "2026-09-09"
title: "Basic Estimators and Experimental Pitfalls"
session_type: "lecture"
duration_minutes: 115
source: "../../../syllabus.md"
---

# Lecture scope

- Present the difference-in-means estimator as an estimator of the finite-sample average treatment effect under complete randomization. Derive its design unbiasedness.
- Introduce the randomization variance of the estimator and distinguish it from an estimator of that variance and from the realized variance estimate.
<!-- - Introduce randomization-based inference and explain how its probability statements arise from the assignment mechanism.
--> 
- Use one small, hand-workable finite-population example that can be reconstructed at the blackboard. 
- Introduce Inverse probability weighting (IPW).
- introduce the Horvitz-Thompson (HT) estimator.
- Above, we present the difference in means as an estimator of the finite-sample average treatment effect under complete randomization and derive its design unbiasedness. Now consider an iid Bernoulli design. Explain that the usual difference-in-means estimator is undefined on all-treated and all-control assignments, but is design-unbiased conditional on any nondegenerate realized treatment count. Explain that the Horvitz–Thompson estimator is unconditionally design-unbiased under both iid Bernoulli and complete randomization, and that under complete randomization it coincides with difference in means.
- Introduce Hajek estimator. Explain self-normalization idea, and how it almost always reduces variance and MSE (Sarndal's textbook has an analysis of the variance (or MSE?) based on taylor expansion. Reproduce it tersely. 
- Embed an interactive simulation where the HT estiamtor wins or the Hajek estimator wins, in terms of MSE, depending on the settings of the simulation. For the PDF version, create a static plot with two panels showing one winning vs. the other winning. 
- Trotter-Tukey estimators, per Khan and Ugander. Summarize this paper rather completely, at least the ideas of TT, and the iteration, and the fixed point, and the fixed point being a regression control estimator. I like it a lot, it teaches a lot I think, and I want to present it pretty fully.  
- Regression adjustment, including for treatment probabilities (build forward from Khan and Ugander).
- Variance reduction using covariates (other than treatment probabilities).
- Generalized regression estimators (GREG)
- CUPED
- Calibration estimators. See the long-form notes in scattered_notes/calibration_estimators_notes_latex_bundle/ and distill content that is suitable for the lecture, leaving longer exposition for Advanced material.


Advanced material (each bullet should be a stand alone section):
- Summarize Ron Kohavi's work on "common pitfalls" in experimentation and related work. See "Seven pitfalls to avoid when running controlled experiments on the web" from KDD 2009. See the recent paper from KDD 2026, "Trustworthy A/B Patterns and the Winner’s Curse: Lessons from Eight Large-Scale Replications". Review Kohavi's other practical/empirical papers and produce a concise summary of this line of work, through the 2026 paper, with pointers to read more.

- Outline the arguments of Hirano, Imbens, and Ridder (2003, *Econometrica*), sometimes called the propensity paradox. Note how this has implications specifically for (non-observational) experiments where assignment probabilities are known.

- Give a history of th different IPW estimator ideas (HT, Hajek, Trotter-Tukey) including relation to ideas in Monte Carlo (Art Owen's lecture notes), and relation to papers like Swaminathan & Joachims's paper on self-normalized estimators. 

- Give a short summary of Parikh et al. (2026), [arXiv:2607.23254](https://arxiv.org/abs/2607.23254), as it relates to the language of this lecture. 


# Literature

Hajek and self-normalization:
- Hale F. Trotter and John W. Tukey. Conditional monte carlo for normal samples. In Symposium on Monte Carlo Methods, 1954.
- D Basu. An essay on the logical foundations of survey sampling, part i. In VP Godambe and
DA Sprott, editors, Foundations of Statistical Inferences. Holt, Rinehart and Winston, Toronto, Canada, 1971.
- Adith Swaminathan and Thorsten Joachims. The self-normalized estimator for counterfactual
learning. In Advances in Neural Information Processing Systems, pages 3231–3239, 2015.
- Samir Khan, Johan Ugander (2023) "Adaptive normalization for IPW estimation," Journal of Causal Inference. 

Regression control:
- Lin, Winston. 2013. “Agnostic Notes on Regression Adjustments to Experimental Data: Reexamining Freedman’s Critique.” The Annals of Applied Statistics 7 (1): 295–318. https://doi.org/10.1214/12-AOAS583.


Calibration:
- Deville and Sarndal (1992), calibration estimators; full citation pending verification

Pitfalls
- Kohavi et al., common pitfalls in experimentation; exact source pending verification

Estimating propensities:
- Hirano, Imbens, and Ridder 2003, Econometrica.
