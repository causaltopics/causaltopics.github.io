# Course notation

This file records notation intended to remain stable across lectures. Before
introducing notation in a lecture, check the conventions here. Add notation
when it becomes course-wide; leave symbols used only in a local derivation or
example in that lecture.

## Units, samples, and populations

- $N$ is the number of units in the finite experimental population, indexed by
  $i=1,\ldots,N$.
- $n$ is the sample size in explicitly stated i.i.d. superpopulation or
  observational-sampling arguments. Do not silently replace the finite
  experimental population indexed by $N$ with an i.i.d. sample indexed by
  $n$.
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
- In a stated superpopulation, $\tau_P=\mathbb E\{Y(1)-Y(0)\}$ denotes the
  population ATE. For a measurable covariate subset $A$,
  $\tau_A=\mathbb E\{Y(1)-Y(0)\mid X\in A\}$ is the ATE in the restricted
  target population. For a nonnegative tilting function $h$,
  $\tau_h=\mathbb E[h(X)\{Y(1)-Y(0)\}]/\mathbb E\{h(X)\}$ is the ATE in the
  corresponding tilted target population.
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
- In superpopulation arguments, $m_z(x)=\mathbb E\{Y(z)\mid X=x\}$ denotes
  the conditional potential-outcome mean for arm $z$. In design-based
  arguments, the same symbol may denote a working outcome prediction;
  distinguish the population conditional mean, a function fixed before
  assignment, and a function fitted using realized outcomes.
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
- In observational or superpopulation arguments,
  $e(x)=\mathbb P(Z=1\mid X=x)$ is the propensity score. Introduce the change
  of framework explicitly; do not use $e(x)$ as though it were the known
  finite-population design probability $\pi_i$.

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

- Under interference, $Y_i(\mathbf z)$ is unit $i$'s potential outcome under
  the full assignment vector $\mathbf z\in\{0,1\}^N$, and
  $Y_i^{\mathrm{obs}}=Y_i(\mathbf Z)$. The two-outcome notation $Y_i(z)$
  applies when other units' assignments do not affect unit $i$.
- $\mathcal N_i$ is the known interference neighborhood of unit $i$,
  including $i$ unless explicitly stated otherwise; $d_i=|\mathcal N_i|$.
  For a directed interference network, $j\in\mathcal N_i$ means that
  treatment of $j$ may affect the outcome of $i$.
- $\tau_{\mathrm G}=N^{-1}\sum_i\{Y_i(\mathbf 1_N)-Y_i(\mathbf 0_N)\}$
  is the global average treatment effect (GATE), also called the total
  treatment effect (TTE) in the interference literature. It is an average
  over units even when called a total effect.
- $E_i=f_i(\mathbf Z)$ is the exposure induced by a prespecified mapping.
  When the mapping is sufficient, $y_i(e)$ denotes the common potential
  outcome under assignments with exposure label $e$.
  When used for exposure probabilities, $\pi_i(e)=\mathbb P_Z(E_i=e)$ and
  $\pi_{ij}(e,e')=\mathbb P_Z(E_i=e,E_j=e')$; the argument denotes an
  exposure label rather than a unit's own treatment state.
- $\mathcal C=\{C_1,\ldots,C_K\}$ is a partition into clusters, $c(i)$ is
  the index of unit $i$'s cluster, and $W_k$ is cluster $k$'s treatment.
  Cluster-constant assignment means $Z_i=W_{c(i)}$.
  $k_i(\mathcal C)$ counts the clusters intersecting $\mathcal N_i$.
- A low-order outcome model has maximum interaction order $\beta$ and
  subset collection $\mathcal S_i^\beta
  =\{S\subseteq\mathcal N_i:|S|\le\beta\}$, including the empty set.
  The feature vector $\mathbf v_i(\mathbf z)$ contains the monomials
  $\prod_{j\in S}z_j$ for these subsets, with the empty product equal to one.
- $\mathbf c_i$ collects the coefficients in
  $Y_i(\mathbf z)=\mathbf v_i(\mathbf z)^\top\mathbf c_i$.
  $\mathbf a_i=\mathbf v_i(\mathbf 1_N)-\mathbf v_i(\mathbf 0_N)$
  selects unit $i$'s contribution to the global contrast.
- $\mathbf M_i=\mathbb E_Z[
  \mathbf v_i(\mathbf Z)\mathbf v_i(\mathbf Z)^\top]$ is the design
  second-moment matrix, and $\mathbf M_i^\dagger$ is its Moore--Penrose
  pseudoinverse. Define any fitted or empirical matrix separately.

## Stochastic policy evaluation

- In network seeding examples, $M$ is the number of villages or independent
  networks, indexed by $g$. $S_g$ is the selected seed set, and $Y_g(s)$ is
  the village-level potential outcome under seed set $s$.
- $p_g^a(s)$ is the seed-set probability under target policy $a$;
  $q_g(s)$ is its probability under the actual experimental design.
  $\mathbb E_q$ and $\operatorname{Var}_q$ hold the villages, graphs, and
  potential outcomes fixed and average over this design.
- $V_M(p)=M^{-1}\sum_g\sum_s p_g(s)Y_g(s)$ is a policy's value averaged
  over the fixed villages. $\Delta_M(A,B)=V_M(p^A)-V_M(p^B)$ is the
  policy-value contrast. State any alternative village or resident weights.

## Panel data and matrices

- Panel units are indexed by $i=1,\ldots,N$ and periods by $t=1,\ldots,T$.
  $Z_{it}$ denotes treatment. The notation $Y_{it}(z)$ presumes that a
  contemporaneous treatment indicator adequately describes the intervention;
  introduce treatment-history notation when anticipation or carryover matters.
- $\mathcal O=\{(i,t):Z_{it}=0\}$ is the set of observed untreated cells,
  and $\mathcal T=\{(i,t):Z_{it}=1\}$ is the treated set. The complete
  matrix of observed outcomes is not the matrix of untreated potential
  outcomes: entries of the latter are missing on $\mathcal T$.
- $\tau_{\mathcal T}=|\mathcal T|^{-1}\sum_{(i,t)\in\mathcal T}
  \{Y_{it}(1)-Y_{it}(0)\}$ averages effects over the specified treated cells.
- $M_{it}^0$ is the systematic untreated outcome in
  $Y_{it}(0)=M_{it}^0+\varepsilon_{it}$. In a factor model,
  $M_{it}^0=\alpha_i+\delta_t+L_{it}$ with
  $\mathbf L=\mathbf U\mathbf F^\top$ and
  $L_{it}=\mathbf u_i^\top\mathbf f_t$.
  $r$ denotes the rank bound on $\mathbf L$, not necessarily on the full
  mean matrix after adding fixed effects.
- $\|\mathbf L\|_*=\sum_j\sigma_j(\mathbf L)$ is the nuclear norm,
  the sum of the singular values. Distinguish this penalty from a hard
  constraint on the number of nonzero singular values.

## Probability, convergence, and norms

- $\mathbf 1\{A\}$ is the indicator of event $A$. When a vector of ones is
  needed, write $\mathbf 1_N$ for the length-$N$ vector so it is not confused
  with the indicator notation.
- Always subscript probability, expectation, and variance when more than one
  source of randomness is in play.
