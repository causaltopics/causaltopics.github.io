---
week: 3
lecture: "L03"
date: "2026-09-16"
title: "Experimental Design, Blocking, Balancing"
session_type: "lecture"
duration_minutes: 115
source: "../../../syllabus.md"
---

# Lecture scope
- Develop blocking and stratified randomization, connecting to the contast between complete randomization and Bernoulli randomization, in a world with covariates. Matched pairs design. Discuss pros and cons. Give an introduction to approaches based on discrepancy minimization. 
- Contrast the use of blocking or stratified randomization (a design choice), with using an i.i.d. Bernoulli design but employing covariate adjustment (an analysis choice). Use this contrast a basic example of choices that happen "during design vs. during analysis".
- Motivate and develop Augmented inverse probability weighting (AIPW).
- Review Imai, King, Nall (2009) on "pair matching" for cluster randomized experiments. Discuss work analyzing such designs since, including Candogan, Chen, Niazadeh (2023) in Management Science. Condogan et al. does not use covariate information, which is notable. Describe their assumptions. If too much material, have the main lecture just discuss Imai et al. (2009), with a pointer to Condogan et al. as Advanced Material. 

- As a possible initial motivation for studying blocking, to explore the consequences of experimental design choices, consider what happens if you have N=1000 units, Bernoulli randomization with a p=0.5 coin flip probability, but their treatment assignemnts are perfectly correlated in 10 groups of 100. Study the variance of the HT estimator of the ATE for this population. Contrast it with the variance of the HT estimator under a Bernoulli(0.5) iid design with N=10 units, and a Bernoulli(0.5) iid design with N=1000 units. 

- Present re-randomization, develop it as a form of randomized design. Give the classic pros and cons, and how to analyze experiments under re-randomization. Summarize the work of Li, Ding, Rubin (2018). Draw on Peng Ding's lecture notes, specifically Section 6.1.

Advanced Material:
- As a key example of an exotic design, briefly introduce Gram-Schmidt random walk designs, connecting experimental design to discrepancy theory.
- Connect Harshaw et al.'s work to the very recent pre-print by Max Cytrynbaum (https://arxiv.org/abs/2608.18057), and briefly discuss kernalization of GSW.
- Harshaw discusses "optimization-based designs" and cites many papers by Kallus as well as others (e.g., D Bertsimas, M Johnson, N Kallus, Operations Research, 2015;
 Kallus 2018 "Optimal a priori balance in the design of controlled experiments", JRSSB; Kallus 2021, "On the optimality of randomization in experimental design: How to randomize for minimax variance and design-based inference", JRSSB). These predate the GSW work. Discuss the aspects of the Harshaw et al. paper that emphasis the robustness-balance tradeoff, how the best assignment from optimization-based designs are usually deterministic and thus may lack robustness.
- As another example of an exotic experimental deisgn, present Efron's biased-coin designs
- As part of the dicsussion of optimization-based deisgns, briefly summarize the contents of Section 7.5 of Boyd and Vandenberghe's Convex optimization book, on optimized experimental designs, including D-optimal, A-optimal, and E-optimal designs. Give pointers to that book chapter (available online). Are there connections to the Harshaw et al. paper on GSW?  
- Briefly mention staggered rollout experiments, and consider their value for no-SUTVA experiments.

<!-- - Introduce double robustness.  -->


# Literature

- Morgan and Rubin, rerandomization; exact source pending verification
- Efron, biased-coin designs; exact source pending verification
- Gram-Schmidt random-walk designs; exact source pending verification
