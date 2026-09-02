# Course notation

This file records notation intended to remain stable across lectures. Before
introducing notation in a lecture, check the conventions here. Add notation
when it becomes course-wide; leave symbols used only in a local derivation or
example in that lecture.

## Units, samples, and populations

- $N$ is the number of units in the finite experimental population, indexed by
  $i=1,\ldots,N$.
- $X_i$ is the vector of pretreatment covariates for unit $i$; $\mathbf X$
  collects these vectors.
- A target population beyond the experimental units is described explicitly.
  Do not use "ATE" without making its target population clear.

## Treatments, assignments, and exposures

- $Z_i\in\{0,1\}$ is unit $i$'s treatment assignment, with $1$ denoting
  treatment and $0$ control. The assignment vector is
  $\mathbf Z=(Z_1,\ldots,Z_N)$.
- $N_1=\sum_{i=1}^N Z_i$ and $N_0=N-N_1$ are the realized treatment-arm sizes.
- $\mathcal Z$ is the support of the experimental design, the set of assignment
  vectors with positive probability.
- When units are partitioned into $H$ design strata or blocks, $h=1,\ldots,H$
  indexes the strata, $N_h$ is the stratum size, and $N_{1h}$ and $N_{0h}$ are
  its treatment-arm sizes.

## Potential outcomes and observed outcomes

- $Y_i(z)$ is the potential outcome for unit $i$ under treatment level
  $z\in\{0,1\}$.
- $Y_i^{\mathrm{obs}}=Y_i(Z_i)=Z_iY_i(1)+(1-Z_i)Y_i(0)$ is the observed
  outcome when SUTVA and consistency hold.
- $\tau_i=Y_i(1)-Y_i(0)$ is unit $i$'s treatment effect.

## Estimands and estimators

- $\overline Y(z)=N^{-1}\sum_{i=1}^N Y_i(z)$ is the finite-population mean
  potential outcome under treatment level $z$.
- $\tau=N^{-1}\sum_{i=1}^N\tau_i=\overline Y(1)-\overline Y(0)$ is the
  finite-population average treatment effect. Qualify population and
  conditional versions with a subscript or argument, such as $\tau_P$,
  $\tau(x)$, or $\tau_g$.
- A hat denotes an estimator, a random function of the assignment and observed
  outcomes. Its value at the realized data is an estimate.
- $\widehat\tau_{\mathrm{DM}}$ denotes the treated-minus-control difference in
  observed means.
- $\widehat\mu_{z,\mathrm{HT}}$ and $\widehat\mu_{z,\mathrm{H}}$ denote,
  respectively, the Horvitz--Thompson and Hájek estimators of
  $\overline Y(z)$. The corresponding treatment-effect estimators are
  $\widehat\tau_{\mathrm{HT}}=\widehat\mu_{1,\mathrm{HT}}-
  \widehat\mu_{0,\mathrm{HT}}$ and
  $\widehat\tau_{\mathrm{H}}=\widehat\mu_{1,\mathrm{H}}-
  \widehat\mu_{0,\mathrm{H}}$.
- $\widehat\mu_\lambda$ denotes a member of the Trotter--Tukey affine
  normalization family, with Horvitz--Thompson at $\lambda=0$ and Hájek at
  $\lambda=1$. $\widehat\mu_{\mathrm{AN}}$ denotes the adaptively normalized
  fixed-point estimator.
- $\overline X=N^{-1}\sum_{i=1}^N X_i$ is the finite-population covariate
  mean. Center covariates at $\overline X$ when writing regression-adjusted
  treatment effects.
- $\widehat\tau_X=\overline X_1^{\mathrm{obs}}-
  \overline X_0^{\mathrm{obs}}$ denotes realized covariate mean imbalance.
- $m_z(x)$ denotes an outcome prediction for treatment arm $z$; distinguish a
  function fixed before assignment from one fitted using realized outcomes.
- $\widehat\mu_{z,\mathrm{AIPW}}$ denotes the prediction-plus-IPW-correction
  estimator of $\overline Y(z)$, and
  $\widehat\tau_{\mathrm{AIPW}}=\widehat\mu_{1,\mathrm{AIPW}}-
  \widehat\mu_{0,\mathrm{AIPW}}$.

## Assignment and sampling probabilities

- $\mathbb P_Z$, $\mathbb E_Z$, $\operatorname{Var}_Z$, and
  $\operatorname{Cov}_Z$ refer to probability under the assignment design,
  holding the finite population and all potential outcomes fixed.
- $\pi_i=\mathbb P_Z(Z_i=1)$ is unit $i$'s marginal treatment probability.
- When both treatment states appear symmetrically, use
  $\pi_i(z)=\mathbb P_Z(Z_i=z)$, so that $\pi_i(1)=\pi_i$ and
  $\pi_i(0)=1-\pi_i$.
- Use $p$ for a common Bernoulli assignment probability.

## Finite-population and superpopulation operators

- For $z\in\{0,1\}$,
  $S_z^2=(N-1)^{-1}\sum_{i=1}^N\{Y_i(z)-\overline Y(z)\}^2$ is the
  finite-population variance of potential outcomes.
- $S_\tau^2=(N-1)^{-1}\sum_{i=1}^N(\tau_i-\tau)^2$ is the finite-population
  variance of unit-level treatment effects.
- Within stratum $h$, use $\tau_h$, $S_{zh}^2$, and $S_{\tau h}^2$ for the
  stratum ATE and the corresponding finite-population variances.
- $s_z^2$ is the usual sample variance of observed outcomes within realized
  arm $z$.
- Unsubscripted probabilistic expectations such as $\mathbb E$ refer to a
  stated superpopulation or statistical model, not to the assignment design.

## Networks and interference

<!-- Placeholder. -->

## Panel data and matrices

<!-- Placeholder. -->

## Probability, convergence, and norms

- $\mathbf 1\{A\}$ is the indicator of event $A$. When a vector of ones is
  needed, write $\mathbf 1_N$ for the length-$N$ vector so it is not confused
  with the indicator notation.
- Always subscript probability, expectation, and variance when more than one
  source of randomness is in play.
