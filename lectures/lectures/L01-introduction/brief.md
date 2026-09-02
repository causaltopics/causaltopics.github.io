---
week: 1
lecture: "L01"
date: "2026-09-02"
title: "Introduction"
session_type: "lecture"
duration_minutes: 60
source: "../../../syllabus.md"
---
 
# Lecture scope

- For this lecture, the meeting duration is set to only 60 minutes (instead of the usual 115), since a solid hour will be spent going over the meta/admin/structure of the course.

- Begin with a concise course overview and explain the course's design-based emphasis.
- Also emphasize how we will be making parallel use of "design", meaning choices/optimizations of the experimental design, and "analysis", meaning choice/optimization of estimators and adjustments, etc. Note that the estimand/target will generally be fixed, except for when it isn't (Lecture 4's discussion of sample trimming). 

- Define potential outcomes in the Neyman-Rubin framework. Present this framework as a natural outgrowth of survey-sampling ideas applied to causal effects, and briefly contrast it with Pearl-style structural causal inference. Keep the historical lineage concise in the lecture spine and give primary-source pointers in Further reading at the end of this lecture's lecture notes.
- Give an example of a ``science table'', giving a view of individual outcomes and individual treatment effects (ITEs), and encourage critical thinking about when we should care about the average treatment effect or other perspectives on the table. 
- Develop Neyman's perspective from his argricultural work, setting up design-based inference. Contrast with the idea of modelling the outcomes, e.g., through linear models or some other method of imputation. 
- Having defined outcomes, define a randomized experimental design as a probability distribution over assignment vectors. Contrast complete randomization, which fixes the treated count, with Bernoulli i.i.d. randomization, which assigns units independently and leaves the treated count random. Note that under complete randomization, the treatmenet vector elements are weakly dependent.
- Introduce positivity (only after defining the design), as a property of the assignment mechanism relative to the causal comparisons of interest.
- Explain why randomization identifies causal effects, while keeping clear which conclusions come from the design and which would require a model or superpopulation argument (explain what a superpopulation estimand is).
- Emphasize the importance of specifying the target population and estimand. Distinguish an estimand, an estimator, and an estimate.
- Define SUTVA and preview (very briefly) how its components will be relaxed later in the course.
- Define the finite-sample average treatment effect as the main estimand of causal inference. Briefly map it to population ATEs, CATEs, GATEs (Global Average Treatment Effects, when SUTVA is not assumed), without developing the specialized identification arguments for any of those estimands.
- Do not include an interactive demonstration in this lecture.

# Advanced material

- Give a compact missing-data interpretation of potential outcomes and distinguish MCAR, MAR, and MNAR, including enough history to locate the terminology without making missing-data theory part of the central lecture path.
- Elaborate on subtleties of Bernoulli randomization, including random treatment-arm sizes and the possibility of an empty arm in a small experiment.
- Clarify the distinction among finite-population, sample, and superpopulation estimands, and explain why the target population will matter later when the course studies overlap and trimming.
- Give the exact Neyman randomization variance under complete randomization and explain why its treatment-effect-heterogeneity term is not generally identified from observed outcomes.

# Deferred or sidelined material

- Defer indefinitely: structural causal models, causal graphs, and do-calculus; the Pearl comparison here is high-level only and not a focus of the course.
- Defer indefinitely: derivation and identification of LATE to a later treatment of noncompliance or instrumental variables; use LATE here only (if at all) to show that causal questions can target different populations and contrasts.
- Defer substantive treatments of positivity failures, overlap, trimming, and partial identification to L04.
- Defer a full development of variance estimators, confidence intervals, and alternative estimators to L02.
- Defer interference and departures from SUTVA to L05.

# Literature

- Neyman (1934), "On the Two Different Aspects of the Representative Method" ([DOI](https://doi.org/10.1111/j.2397-2335.1934.tb04184.x)).
- Neyman (1923; English translation 1990), "On the Application of Probability Theory to Agricultural Experiments" ([DOI](https://doi.org/10.1214/ss/1177012031)).
- Rubin (1974), "Estimating Causal Effects of Treatments in Randomized and Nonrandomized Studies" ([DOI](https://doi.org/10.1037/h0037350)).
- Rubin (1976), "Inference and Missing Data" ([DOI](https://doi.org/10.1093/biomet/63.3.581)).
- Holland (1986), "Statistics and Causal Inference" ([DOI](https://doi.org/10.1080/01621459.1986.10478354)).
- Pearl (1995), "Causal Diagrams for Empirical Research" ([DOI](https://doi.org/10.1093/biomet/82.4.669)).
- Seaman et al. (2013), "What Is Meant by 'Missing at Random'?" ([DOI](https://doi.org/10.1214/13-STS415)).
- Angrist, Imbens, and Rubin (1996), "Identification of Causal Effects Using Instrumental Variables" ([DOI](https://doi.org/10.1080/01621459.1996.10476902)).
- Crump et al. (2009), "Dealing with Limited Overlap in Estimation of Average Treatment Effects" ([DOI](https://doi.org/10.1093/biomet/asn055)).
