---
title: "Chapter 7 — SEM, Model Comparison, and Robustness"
status: draft
object_type: Chapter
layer: Methodological
claim_anchors:
  - BR-000019
  - LP-000001
  - BE-000080
  - NB-000101
  - NB-000103
  - IB-000001
  - IB-000005
  - IB-000006
  - PI-000001
  - SR-000001
posteriors_used:
  BE_INT: {posterior: 0.846, n_evid: 63}
  BT_INT: {posterior: 0.892, n_evid: 31}
  BT_BEH: {posterior: 0.910, n_evid: 22}
  BI_ATT: {posterior: 0.921, n_evid: 16}
  BP_ATT: {posterior: 0.850, n_evid: 7}
  BA_INT: {posterior: 0.736, n_evid: 21}
  BD_BEH: {posterior: 0.611, n_evid: 6}
  ATT_INT: {posterior: 0.873, n_evid: 29}
  SNinj_INT: {posterior: 0.778, n_evid: 18}
  SNdes_INT: {posterior: 0.674, n_evid: 5}
  PBC_INT: {posterior: 0.802, n_evid: 16}
  INT_BEH: {posterior: 0.804, n_evid: 47}
  HAB_BEH: {posterior: 0.727, n_evid: 3}
  SAL_BEH: {posterior: 0.727, n_evid: 3}
reviews: [REVIEW-000006, REVIEW-000100, REVIEW-000112, REVIEW-000114, REVIEW-000115]
---

# Chapter 7 — SEM, Model Comparison, and Robustness

## Scientific Question

What methodological functions do CFA, SEM, model comparison, mediation analysis, moderation analysis, dominance analysis, NCA, and network analysis each fulfil within the BEBA research programme — and how do they fit together into a coherent analytical architecture?

---

## 7.1 The Two-Step Logic: From Measurement to Structure

Chapter 6 established the measurement model requirements for the BEBA constructs: valid, reliable, measurement-invariant indicators for each latent variable before any structural relationships are examined. Chapter 5 established the model competition framework: four competing structural architectures (Models A–D) evaluated through likelihood comparisons. This chapter operationalises both: it specifies the analytical tools, their function in the overall research programme, and their interconnections.

The governing logic is the **two-step approach** of Anderson and Gerbing (1988):

**Step 1 — Measurement model:** A Confirmatory Factor Analysis (CFA) of the full construct set is estimated and evaluated for fit. All validity criteria from Chapter 6 (AVE > 0.50, CR > 0.70, HTMT < 0.85, measurement invariance across groups) must be satisfied before Step 2.

**Step 2 — Structural model:** Path coefficients are added to the confirmed measurement model, and the resulting Structural Equation Model (SEM) is estimated. Structural fit is assessed and compared across the competing model architectures.

This sequence is not merely procedural. It enforces a principled separation between two distinct claims: "we have measured the constructs validly" and "we have found structural relationships between them." Conflating the two — estimating structural paths before verifying measurement quality — is a common error that produces inflated path coefficients and misleading model fit indices. The two-step approach makes the measurement claim explicit and testable before the structural claim is entertained.

---

## 7.2 CFA in the BEBA Programme: Fit, Inference, and Limits

**Confirmatory Factor Analysis** tests whether a hypothesised factor structure — a prespecified set of loadings and cross-loadings — is consistent with an observed covariance matrix. Unlike Exploratory Factor Analysis (EFA), CFA does not discover factor structures; it confirms or disconfirms a structure that theory has already specified.

### 7.2.1 Fit Evaluation

CFA fit is assessed through a standard battery of indices, each capturing a different aspect of model-data consistency:

| Index | Criterion | What it captures |
|---|---|---|
| **CFI** (Comparative Fit Index) | ≥ .95 (good); ≥ .90 (acceptable) | Proportional improvement over the independence model |
| **RMSEA** (Root Mean Square Error of Approximation) | ≤ .06 (good); ≤ .08 (acceptable) | Average discrepancy per degree of freedom |
| **SRMR** (Standardised Root Mean Square Residual) | ≤ .08 | Average standardised residual; sensitive to structural misfit |
| **χ²/df** | ≤ 3 | Chi-square normed by degrees of freedom |

These thresholds are benchmarks, not guarantees. A model that meets all fit thresholds is not necessarily the correct model — it is merely one that cannot be rejected on fit grounds alone. Competing models with similar fit must be distinguished through likelihood comparison (Chapter 5) and theoretical interpretability.[^7-fn-fit]

### 7.2.2 What CFA Can and Cannot Establish

CFA can establish:
- Whether the hypothesised factor structure is consistent with the data.
- Whether indicators load substantially and specifically on their intended factors.
- Whether factors are empirically distinguishable (discriminant validity).
- Whether the same factor structure holds across groups (measurement invariance).

CFA cannot establish:
- Causal direction (whether the factor causes the indicators or vice versa).
- Whether the specified model is the only model consistent with the data (equivalent models).
- Whether the constructs measured are the theoretically correct ones for the research question.

The third limitation is particularly important for BEBA: a CFA that confirms a four-factor brand equity structure does not establish that these four factors are the *right* theoretical architecture for understanding nonprofit donor behaviour. That question requires the structural model and the model competition framework.[^7-fn-equivalent]

---

## 7.3 Structural Equation Modelling: Paths, Fit, and the Latent Variable Advantage

**Structural Equation Modelling** extends CFA by adding directed paths between latent variables — the theoretical relationships predicted by the BEBA architecture. SEM simultaneously estimates the measurement model (Chapter 6) and the structural model, propagating measurement error appropriately rather than using observed variable proxies.

The latent variable advantage is directly relevant to BEBA. If brand trust were measured as a composite score (the average of five trust items) and used as an observed predictor, measurement error would attenuate the structural coefficient — the estimated relationship between brand trust and donation intention would be biased downward by the proportion of observed variance due to measurement error. SEM uses the true score variance (the latent variable) in all structural relationships, producing unattenuated estimates.

### 7.3.1 Estimation Method

The BEBA empirical programme uses **Maximum Likelihood (ML) estimation** as the primary method, with **MLR (robust ML)** as the default to correct for non-normality of Likert response distributions. MLR produces the Satorra-Bentler corrected chi-square statistic and robust standard errors without requiring distributional assumptions that ordinal data rarely satisfy.[^7-fn-estimation]

For models with non-normal residuals or categorical indicators (binary donation behaviour items), **WLSMV (Weighted Least Squares, Mean and Variance adjusted)** estimation is used. WLSMV is designed for ordinal and binary indicators and produces asymptotically distribution-free parameter estimates.

### 7.3.2 The BEBA Knowledge Graph Posteriors as Structural Priors

A distinctive feature of the BEBA empirical programme is the use of the **Bayesian posterior probabilities** from the knowledge graph (Chapters 2–4) as *informative priors* for the empirical analysis. The literature-derived posterior for each structural path represents the accumulated evidence prior to the Austrian empirical study. The empirical data then *updates* this prior through Jeffrey Conditionalization (Chapter M, Section M.4).

The current knowledge graph posteriors for key BEBA structural paths are:

| Path | Posterior | n_evid | Interpretation |
|---|---|---|---|
| Brand Image → Attitude (BI→ATT) | 0.921 | 16 | Very strong prior support |
| Brand Trust → Intention (BT→INT) | 0.892 | 31 | Very strong prior support |
| Brand Trust → Behaviour (BT→BEH) | 0.910 | 22 | Very strong prior support |
| Brand Personality → Attitude (BP→ATT) | 0.850 | 7 | Strong prior support |
| Attitude → Intention (ATT→INT) | 0.873 | 29 | Strong prior support |
| Brand Equity → Intention (BE→INT) | 0.846 | 63 | Strong prior support |
| PBC → Intention (PBC→INT) | 0.802 | 16 | Moderate-strong prior support |
| Intention → Behaviour (INT→BEH) | 0.804 | 47 | Moderate-strong prior; gap documented |
| Injunctive Norms → Intention (SNinj→INT) | 0.778 | 18 | Moderate prior support |
| Brand Awareness → Intention (BA→INT) | 0.736 | 21 | Moderate prior support |
| Habit → Behaviour (HAB→BEH) | 0.727 | 3 | Moderate prior; thin evidence base |
| Salience → Behaviour (SAL→BEH) | 0.727 | 3 | Moderate prior; thin evidence base |
| Descriptive Norms → Intention (SNdes→INT) | 0.674 | 5 | Weak-moderate prior support |
| Brand Differentiation → Behaviour (BD→BEH) | 0.611 | 6 | Weakly supported; high uncertainty |

These posteriors have two operational uses. First, they inform the **specification of Bayesian SEM priors**: paths with high posterior support receive tighter (less diffuse) prior distributions centred on a positive effect, while paths with low posterior support or high uncertainty receive wider or less directional priors.[^7-fn-bsem] Second, they provide the **theoretical baseline** for interpreting empirical results: if the Austrian data produce path estimates substantially inconsistent with the literature posteriors, this constitutes a theoretically significant finding about the Austrian context rather than simply a null result.

---

## 7.4 The BEBA Structural Hypotheses: Prior Specification

In line with the model competition framework (Chapter 5), the BEBA structural hypotheses are stated as a set of competing architectures rather than as isolated directional predictions. The hypotheses below correspond to Models A–D from Chapter 4 (Section 4.5), now translated into testable structural specifications.[^7-fn-hypotheses]

**H-A (Standard IBM/TPB Baseline):**  
Attitude (ATT), Injunctive Norms (SNinj), Descriptive Norms (SNdes), and Perceived Behavioural Control (PBC) are the only direct predictors of Donation Intention (INT). Brand equity constructs are not included.

**H-B (Brand Equity-Augmented, Full Mediation):**  
Brand equity dimensions (Brand Image, Brand Trust, Brand Awareness, Brand Personality) predict ATT and PBC, which fully mediate their effects on INT. No direct path from brand equity to INT.

**H-C1 (Configural BEBA, Partial Mediation):**  
Brand equity dimensions predict INT both through IBM/TPB mediators and directly. Specific dimension-mechanism pairings are specified: Brand Image → ATT; Brand Trust → PBC; Brand Awareness → PBC; Brand Personality → ATT; Overall Brand Equity → INT direct.

**H-C2 (Configural BEBA, Mechanism-Differentiated):**  
As H-C1, but brand trust additionally predicts behaviour directly (bypass of intention pathway), consistent with the high BT→BEH posterior (0.910). This tests whether trust operates as both an intention antecedent and a direct behavioural governance mechanism.

**H-D (Bourdieu-Augmented):**  
H-C2 extended with a field-level symbolic capital variable (operationalised as perceived organisational prestige and legitimacy in the donor's social environment). Cross-level interaction between symbolic capital and individual-level brand trust.

The empirical evaluation sequence is: H-A first (baseline fit), then likelihood comparison against H-B, then H-C1 vs. H-B, then H-C2 vs. H-C1, then H-D against H-C2. At each step, the model with the best BIC score and theoretically interpretable parameters is retained as the reference for the next comparison.

---

## 7.5 Mediation Analysis: Identifying Mechanisms

Model competition alone cannot fully answer the BEBA theoretical question. Even if H-C1 (configural BEBA) is preferred over H-A (standard IBM/TPB) on likelihood grounds, this preference establishes only that brand equity dimensions improve fit — not *through which mechanisms* they operate. Mediation analysis provides the mechanism evidence.

### 7.5.1 The Indirect Effect and Its Estimation

A **mediated effect** (indirect effect) is the product of two path coefficients: $a \cdot b$, where $a$ is the path from the predictor X to the mediator M, and $b$ is the path from M to the outcome Y. The mediated effect represents the component of X's total effect on Y that operates through M.

The BEBA mediation hypotheses are:

- **Trust-PBC mediation:** Brand Trust → PBC → Donation Intention (testing the uncertainty-reduction mechanism)
- **Image-Attitude mediation:** Brand Image → Attitude → Donation Intention (testing the meaning pathway)
- **Awareness-PBC mediation:** Brand Awareness → PBC → Donation Intention (testing the cognitive availability mechanism)
- **Satisfaction mediation:** Overall Brand Equity → Satisfaction → Donation Intention (testing the confirmatory loop)

### 7.5.2 Estimation and Inference for Indirect Effects

The classical Baron-Kenny causal steps approach to mediation (Baron & Kenny, 1986) is not used in the BEBA programme. It has well-documented limitations: it is underpowered, it does not directly test the indirect effect, and it produces false negatives when the mediated effect is present without a significant total effect (as is possible when direct and indirect effects have opposite signs).[^7-fn-BK]

Instead, indirect effects are estimated and tested through **bias-corrected bootstrapped confidence intervals** (Preacher & Hayes, 2008). The bootstrap generates an empirical sampling distribution of the indirect effect by resampling the data (5,000 resamples); the 95% confidence interval that excludes zero constitutes evidence for mediation. This approach makes no distributional assumptions about the indirect effect — critical because the product of two non-normal distributions is rarely normally distributed.

For the Bayesian SEM specification, indirect effects are estimated from the joint posterior distribution of the two component paths, which naturally produces a posterior distribution of the indirect effect and a credible interval that can be interpreted probabilistically rather than in frequentist terms.

### 7.5.3 Full, Partial, and No Mediation

The BEBA programme does not treat full mediation as theoretically preferred over partial mediation. The knowledge graph posteriors already suggest partial mediation is more consistent with the literature: the high direct posterior for Brand Trust → Intention (0.892) and the high BT→BEH posterior (0.910) both suggest that trust effects are not fully mediated by IBM/TPB constructs. The empirical analysis therefore does not test *whether* mediation occurs but rather *how much* of the total brand equity effect on behaviour is mediated through each mechanism pathway — a continuous question better answered by effect decomposition than by binary mediation classification.[^7-fn-decomp]

---

## 7.6 Moderation Analysis: Identifying Boundary Conditions

The BEBA boundary conditions (Chapter 4, Section 4.6) generate empirically testable moderation hypotheses: conditions under which the relationships between brand equity dimensions and behavioural outcomes are stronger or weaker.

### 7.6.1 Observed Variable Moderation

For moderators measured as observed variables (demographic characteristics: age, income, religious affiliation; contextual characteristics: prior donation history, cause category), interaction terms are introduced into the structural model: the product of the predictor and the moderator is added as an additional predictor of the outcome.

**Moderation hypotheses for the BEBA programme:**

| Moderator | Focal path | Expected direction | Theoretical basis |
|---|---|---|---|
| Donor age | Brand Trust → Intention | Stronger for older donors | Accumulated trust experience; risk aversion |
| Prior donation experience | Brand Trust → Behaviour | Weaker (direct trust; less signal needed) | Habitual pathway replaces signal pathway |
| Income | Brand Awareness → Intention | Stronger for lower income | Higher cognitive effort costs; heuristics more valuable |
| Religious identity | Moral norms → Intention | Stronger | Duty motive supplements warm glow |
| Cultural collectivism | Injunctive Norms → Intention | Stronger | Social conformity norm activated |

### 7.6.2 Latent Variable Interaction: LMS and QML

When the moderator is a latent variable (e.g., the strength of the donor's social-image motivation as a moderator of the social norms → intention path), observed variable interaction terms are biased because they conflate construct variance with measurement error.

**Latent Moderated Structural Equations (LMS)** (Klein & Moosbrugger, 2000) and **Quasi-Maximum Likelihood (QML)** estimation (Klein & Muthén, 2007) are the appropriate methods for latent variable interactions in SEM. Both estimate the interaction effect directly from the latent variable scores rather than from product terms of fallible observed variables, avoiding the attenuation bias inherent in observed-variable interactions.[^7-fn-LMS]

### 7.6.3 Johnson-Neyman Regions of Significance

When a moderation effect is found, the question is not merely whether the effect is moderated but *at what levels of the moderator* the focal relationship is significant. The **Johnson-Neyman technique** (Johnson & Neyman, 1936; Hayes & Matthes, 2009) identifies the range of moderator values for which the conditional effect of the predictor on the outcome is statistically significant — providing a substantively interpretable picture of the boundary condition rather than a simple "significant interaction" claim.

---

## 7.7 Dominance Analysis: Which Predictors Matter Most?

The standard SEM output — standardised path coefficients — does not answer the question of **relative importance**: among the multiple brand equity dimensions that predict donation intention, which contributes the most unique explanatory variance? Standardised coefficients cannot answer this question because they are affected by the intercorrelations among predictors — in a model where brand trust and brand image are substantially correlated, the coefficient for each is a conditional effect holding the other constant, which understates the unique contribution of each.

**Dominance Analysis** (Budescu, 1993; Azen & Budescu, 2003) addresses this by comparing all possible subset regression models and computing each predictor's average contribution to $R^2$ across all models in which it appears. A predictor *dominates* another if it contributes more to $R^2$ in every possible subset — a strict criterion. *Conditional dominance* (dominance in all subsets of a given size) and *general dominance* (dominance on average) are the more practical criteria for applied research.

In the BEBA context, dominance analysis will be applied to the question: among Brand Trust, Brand Image, Brand Awareness, Brand Personality, and Overall Brand Equity, which dimensions dominate in predicting:
1. Donation Intention (the intention outcome)
2. Actual Donation Behaviour (the behavioural outcome)

The knowledge graph posteriors provide a strong prediction: Brand Trust (posterior BT→INT = 0.892) and Brand Image (posterior BI→ATT = 0.921 for the attitude-mediated path) should dominate, while Brand Differentiation should be weakest (posterior BD→BEH = 0.611). The dominance analysis tests whether this prediction is borne out in the Austrian data, and where the prediction fails, this constitutes evidence for context-specific modification of the BEBA mechanism architecture.[^7-fn-dominance]

---

## 7.8 Necessary Condition Analysis: Floors, Bottlenecks, and INUS Causation

Standard regression and SEM estimate **average effects** — the expected change in an outcome for a unit change in a predictor, averaged over the full sample distribution. But some theoretical relationships are not average effects; they are **necessary conditions**: conditions whose absence makes the outcome impossible, regardless of the levels of other predictors.

**Necessary Condition Analysis (NCA)** (Dul, 2016, 2020) identifies necessary conditions by examining the upper-left corner of the scatterplot between predictor and outcome. If there are no high-outcome cases with low values of the predictor — if high donation behaviour never occurs without at least some minimum level of brand trust — this boundary pattern indicates that brand trust is a necessary condition for high donation behaviour.

NCA operationalises **INUS causation** (Insufficient but Non-redundant parts of an Unnecessary but Sufficient condition) — the philosophical notion that a cause may be necessary without being sufficient. Brand trust alone may not produce donations, but donations above some threshold may be impossible without sufficient brand trust.

### 7.8.1 NCA Applied to the BEBA Mechanism Architecture

The BEBA mechanism architecture (Chapter 4, Section 4.4) implies specific necessary condition hypotheses:

| Necessary condition | Outcome | Theoretical justification |
|---|---|---|
| Minimum brand trust | Donation Behaviour ≥ threshold | Uncertainty reduction prerequisite; no donation without basic trust |
| Minimum brand awareness | Donation Behaviour ≥ threshold | Cannot donate to an organisation you do not know exists |
| Minimum perceived quality | Donation Intention ≥ threshold | No intention without some belief in impact effectiveness |

These are distinct from the *sufficient* condition hypotheses tested in SEM: SEM tests whether higher brand trust *on average* produces higher donation intention; NCA tests whether there is a *floor* of brand trust below which high donation behaviour is never observed regardless of other factors.

### 7.8.2 Effect Size and Bottleneck Analysis

NCA produces a **necessity effect size** $d$, ranging from 0 to 1, where $d = 0$ indicates no necessary condition and $d = 1$ indicates a perfect necessary condition (the outcome is impossible without the condition). Dul (2020) suggests $d > 0.10$ as a small necessary effect and $d > 0.30$ as a large necessary effect.

The **bottleneck table** identifies the minimum level of each necessary condition required to achieve each level of the outcome. For the BEBA programme, this translates to: "What minimum level of brand trust (and other brand equity dimensions) must an Austrian nonprofit achieve for its donors to reach a given donation frequency or amount?" — a direct practical implication for brand management that average-effect SEM cannot provide.[^7-fn-NCA]

---

## 7.9 Network Analysis: Capturing Construct Interdependence

The SEM framework assumes that the relationships among BEBA constructs can be represented as a directed acyclic graph (DAG) — a set of one-way causal paths without feedback loops. For the core BEBA structural model (brand equity → IBM/TPB constructs → intention → behaviour), this assumption is defensible.

However, some parts of the BEBA construct system do not fit neatly into a DAG. Brand trust and brand commitment are bidirectionally related: trust builds commitment, and commitment reinforces trust over time. Attitude toward donating and subjective norms may mutually influence each other in social learning contexts. For these constructs, the directed SEM architecture may be misspecified.

**Partial Correlation Networks** (Epskamp & Fried, 2018) represent the construct system as an undirected or mixed graph where edges represent partial correlations — the association between two constructs after removing the influence of all other constructs in the network. Network analysis serves three functions in the BEBA programme:

1. **Construct centrality:** Which constructs are most central to the brand equity-donation network? Centrality measures (strength, closeness, betweenness) identify the constructs whose removal would most disrupt the network — likely candidates: brand trust and brand image, consistent with the knowledge graph posteriors.

2. **Community detection:** Do the BEBA constructs form coherent clusters (brand perceptions, IBM/TPB constructs, behavioural outcomes) or does the network cut across these theoretical boundaries? Community structure provides evidence for or against the three-layer BEBA architecture.

3. **Cross-lagged network stability:** If longitudinal data are available, cross-lagged partial correlation networks capture which constructs causally precede which across time — providing causal evidence that cross-sectional networks cannot.[^7-fn-network]

Network analysis is used as a **supplementary analytic layer** rather than as a replacement for SEM. The two approaches are complementary: SEM tests theoretically specified causal structures; network analysis explores the overall association structure without prespecification. Discrepancies between the two — constructs that are highly central in the network but weakly loaded in SEM, or vice versa — generate theoretical questions about the adequacy of the prespecified structure.

---

## 7.10 Robustness: Sensitivity Analysis and Specification Checks

A single preferred model from the SEM comparison is not the final empirical word. The BEBA programme conducts a systematic **robustness programme** to establish that the preferred model is not an artefact of specific analytic choices, sample characteristics, or outlier patterns.

### 7.10.1 Alternative Specification Checks

For each preferred structural model, alternative specifications are tested:
- **Alternative indicator sets:** Re-running the model with different item subsets to verify that findings are not driven by specific items.
- **Alternative mediation structures:** Swapping the hypothesised mediator-outcome ordering (e.g., testing whether Attitude mediates the brand trust → PBC relationship rather than the other way around).
- **Alternative scaling:** Using parcelled items instead of individual items for constructs with more than four indicators.
- **Alternative estimator:** Repeating the main analysis with WLSMV to verify robustness across estimation methods.

### 7.10.2 Outlier and Influence Analysis

Influential cases — observations whose removal substantially changes parameter estimates — are identified through Cook's distance and the DFbeta statistic. Cases with high leverage and high discrepancy are investigated individually before being removed or retained. In a charitable giving sample, high-frequency donors (e.g., donors giving monthly to five or more organisations) may have distinctive structural patterns that inflate or deflate specific path coefficients.

### 7.10.3 Sample Split Validation

The Austrian dataset is randomly split into development (70%) and holdout (30%) samples. The full model comparison sequence is conducted on the development sample; the preferred model structure is then estimated on the holdout sample to verify cross-sample stability. Path coefficient stability across the two samples is assessed through a chi-square test of the difference between the two models' solutions.[^7-fn-holdout]

### 7.10.4 Bayesian Sensitivity Analysis

For the Bayesian SEM specifications, the sensitivity of the posterior results to prior specification is assessed by varying the prior distributions within a principled range: wide uniform priors, moderately informative priors centred on the knowledge graph posteriors, and strongly informative priors. If posterior estimates are insensitive to this variation, the empirical data dominate prior beliefs — a sign of informative data. If posteriors shift substantially with prior changes, the data are weak and prior sensitivity must be reported alongside the empirical conclusions.

---

## 7.11 Summary: The BEBA Analytical Architecture

The seven analytical methods described in this chapter serve distinct but interlocking functions in the BEBA empirical programme:

| Method | Primary Function | Where Applied |
|---|---|---|
| CFA | Confirm valid measurement | Before all structural analyses |
| SEM | Test structural hypotheses | Chapters 8, 9, 10 |
| Model comparison (likelihood) | Select between competing architectures | Chapter 10 |
| Mediation analysis (bootstrap) | Identify mechanisms | Chapter 10 |
| Moderation analysis (LMS) | Identify boundary conditions | Chapter 10 |
| Dominance analysis | Rank predictor importance | Chapter 9 |
| NCA | Identify necessary conditions | Chapter 10 |
| Network analysis | Explore construct interdependence | Chapter 9 |
| Robustness checks | Assess analytic specificity | All empirical chapters |

The BEBA knowledge graph posteriors serve as the bridge between the theoretical programme (Chapters 1–4) and the empirical programme (Chapters 8–10). They translate the literature's accumulated evidence into formal prior distributions that the Austrian data then update — making BEBA a genuinely cumulative research project in which each empirical study leaves the knowledge base in an improved state for the next researcher who encounters the same theoretical questions.

---

## Footnotes

[^7-fn-fit]: The fit thresholds cited follow Hu & Bentler (1999) and are widely adopted as conventional benchmarks. However, Marsh et al. (2004) have shown that these thresholds are model- and sample-size dependent; the BEBA programme therefore interprets fit indices in conjunction with likelihood comparisons rather than applying them as pass/fail criteria.

[^7-fn-equivalent]: The problem of equivalent models — models with identical fit but different structural specifications — is addressed by the Bayesian model comparison framework (Chapter 5). BIC penalises model complexity in a way that breaks ties among statistically equivalent models that differ in parsimony.

[^7-fn-estimation]: MLR (Maximum Likelihood with Robust standard errors) is implemented in Mplus 8.x and lavaan (R) as the default estimator for continuous indicators. For ordinal indicators with five or fewer response categories, WLSMV is preferred. The choice of estimator is documented in the empirical pipeline and applied consistently across all BEBA analyses.

[^7-fn-bsem]: Bayesian SEM is implemented through the BSEM module in Mplus (Muthén & Asparouhov, 2012) or through brms (Bürkner, 2017) in R. The prior specification uses the knowledge graph posteriors as follows: for a path with posterior $p$, the prior distribution is specified as $\mathcal{N}(\text{logit}(p), \sigma^2)$ where $\sigma^2$ reflects the uncertainty in the literature (narrower for paths with many evidence items, wider for paths with few). The exact prior specification procedure is documented in the empirical pipeline.

[^7-fn-hypotheses]: The structural hypotheses are stated at the model level (sets of paths) rather than as individual path-level directional hypotheses. This prevents the fragmentation of the research programme into many isolated significance tests. The model comparison framework evaluates architectures holistically.

[^7-fn-BK]: The Baron-Kenny causal steps approach requires four conditions: X significantly predicts Y, X significantly predicts M, M significantly predicts Y controlling for X, and the X→Y coefficient is reduced when M is included. This procedure does not test the indirect effect directly, has low power for small indirect effects, and is conceptually limited. Preacher and Hayes (2008) and Hayes (2013) provide the methodological standard for indirect effect estimation in psychology and marketing research.

[^7-fn-decomp]: Effect decomposition reports: total effect of X on Y, direct effect (path X→Y not through M), and specific indirect effects through each mediator separately. When multiple mediators are modelled simultaneously, specific indirect effects are estimated with bootstrap CIs; the comparison of specific indirect effect CIs answers which mechanism pathway is more important than which, not merely whether mediation occurs.

[^7-fn-LMS]: LMS (Klein & Moosbrugger, 2000) is implemented in Mplus. It is computationally intensive and requires numerical integration; for models with more than two latent interaction terms, QML (Klein & Muthén, 2007) is a computationally efficient approximation. Both produce unbiased estimates of the interaction effect when the distributional assumptions are met; LMS is preferred when sample sizes are sufficient.

[^7-fn-dominance]: Dominance analysis for latent variables requires an adaptation: the analysis is conducted on factor scores (Bartlett or regression-weighted) extracted from the CFA rather than on observed composites, to preserve the latent variable properties established in Step 1.

[^7-fn-NCA]: NCA is implemented in R using the `NCA` package (Dul, 2021). Effect sizes are computed using the Ceiling Envelopment with Free Disposal Hull (CE-FDH) and the Ceiling Regression with Free Disposal Hull (CR-FDH) methods. CE-FDH is the more conservative estimator and is used as the primary effect size; CR-FDH is reported as a sensitivity check.

[^7-fn-network]: Cross-sectional partial correlation networks cannot establish causal priority — a central brand trust construct in a cross-sectional network may be central because it causes other constructs, because it is caused by them, or because of unmeasured common causes. Longitudinal or experimental designs are required for causal network inference (Hamaker et al., 2015; Fried et al., 2022). The BEBA network analysis is interpreted in association terms and serves exploratory rather than confirmatory functions.

[^7-fn-holdout]: The 70/30 development-holdout split follows Cudeck and Browne (1983). If the holdout sample produces substantially different path estimates (defined as a difference in standardised coefficients exceeding 0.10 for key paths), this is reported as a robustness failure and the preferred model is downgraded from "confirmed" to "candidate." Sample split procedures are pre-registered to prevent opportunistic selection of favourable split results.
