---
title: "Chapter 9 — Evidence-Based Charity Brand Dashboards"
status: draft
object_type: Chapter
layer: Empirical
chapter_number: 9
part: "III — Empirical Evidence"
claim_anchors:
  - NB-000110
  - NB-000111
  - NB-000112
  - CB-000030
  - CB-000031
pipeline_objects:
  - domir_FC_BO_freq.rds
  - domir_FC_BO_amount.rds
  - domir_FC_BO_bin.rds
  - kano_asymmetry_table.rds
  - segmented_BA_donation_intention.rds
  - EW_kmeans_clusters.rds
  - EW_cluster_moderation_BT.rds
estimator: MLR
missing_data: FIML
research_question: "How do nonprofit brands become behaviourally effective under conditions of uncertainty?"
chapter_function: >
  Derives actionable brand dashboard constructs from psychometric and structural evidence
  generated in Chapters 7 and 8. Applies dominance analysis, Kano-analog penalty-reward
  contrasts, segmented regression, and empathy cluster moderation to identify which brand
  equity dimensions are necessary conditions, which operate linearly, and which function as
  differentiation levers. Synthesises findings into an evidence-based three-tier brand
  dashboard framework for nonprofit brand management.
predecessors:
  - Chapter 8 — Triple Replication of Nonprofit Brand Equity Models
successors:
  - Chapter 10 — Empirical Evaluation of BEBA
---

# Chapter 9 — Evidence-Based Charity Brand Dashboards

---

## 9.1 Scientific Question and Chapter Function

The preceding chapters have established the psychometric foundations of nonprofit brand equity measurement and demonstrated which structural architectures survive transportability testing under Austrian donor conditions. Chapter 8 in particular generated a body of structural evidence — path coefficients, model fit indices, explained variance fractions — across the three donor-outcome dimensions (donation frequency, donation amount, donor status binary). That evidence is, however, inherently *symmetric*: a structural model tells us which latent constructs predict outcomes, but not whether their effects are linear, whether they carry threshold characteristics, or whether their relative importance differs across the donor population. Symmetric evidence is insufficient for brand management practice, which requires asymmetric and prioritised guidance.

The present chapter addresses a different and complementary scientific question: **Which brand equity dimensions are necessary, which are performance-linear, and which are excitement factors — and how should these properties be reflected in a nonprofit brand monitoring dashboard?** This question integrates four distinct analytical perspectives, each of which illuminates a different aspect of the brand–behaviour relationship:

1. **Dominance analysis** (Section 9.3) establishes the unique variance contributions of brand equity dimensions to donation outcomes, providing a theoretically grounded priority ranking that is not distorted by inter-predictor correlations.
2. **Kano-analog penalty-reward contrast** (Section 9.4) classifies dimensions by the functional form of their effect — whether donors notice deficits more than gains, gains more than deficits, or both symmetrically — a classification directly actionable for resource allocation.
3. **Segmented regression** (Section 9.5) tests whether the brand awareness–donation relationship contains a structural breakpoint above which marginal investment yields diminishing returns, informing threshold-based investment logic.
4. **Empathy cluster moderation** (Section 9.6) examines whether the effectiveness of individual brand equity dimensions varies systematically across donor empathy profiles, establishing conditions under which a single dashboard cannot serve the full donor population.

The chapter concludes with a **dashboard synthesis** (Section 9.7) that integrates all four analytical layers into a three-tier evidence-based framework, accompanied by concrete KPI recommendations for nonprofit brand monitoring practice.

A note on the relationship between Chapters 8 and 9: Chapter 8 establishes *what exists* in the data — structural relationships, explained variance, model discrimination. Chapter 9 establishes *what it implies for action* — priority weights, threshold effects, segmentation-contingent effectiveness. The two chapters together constitute the empirical core from which the BEBA architecture (Chapter 10) is derived.

The term "dashboard" is used here in a specific and restricted sense. It does not refer to a software tool, a data visualisation interface, or a real-time monitoring system. It refers to a **structured decision framework** — a categorised set of constructs, tier-assignments, KPI definitions, and benchmark logic that translates empirical evidence into management priorities. The framework is evidence-based in that every tier assignment and KPI threshold is derived from empirical analysis rather than borrowed from commercial brand management practice or imposed from theoretical convenience. This evidence-basis is the chapter's central methodological claim. Nonprofit brand management has historically relied on frameworks adapted from commercial brand equity literature (notably Aaker 1991; Keller 1993) without empirical validation of whether those frameworks' implicit priority orderings are appropriate to nonprofit contexts. The present chapter tests that assumption rather than accepting it.

The precedent for evidence-based brand dashboards in nonprofit contexts is thin. Sargeant and Jay (2004) and Hankinson (2001, 2004) have proposed qualitative brand framework for charities; Boenigk and colleagues have contributed psychometric foundations; but no prior work, to the author's knowledge, integrates dominance weighting, asymmetric functional classification, breakpoint analysis, and donor-segment moderation into a single empirically grounded dashboard architecture for the nonprofit sector.

---

## 9.2 Analytical Overview: How Four Methods Connect

The four analytical methods employed in this chapter are not independently motivated. They share a common theoretical premise: that the relationship between brand equity and donor behaviour is **neither uniform across dimensions nor linear across values**. This premise follows from several strands of theory developed in Chapters 2 through 4.

From dual-process theory (Evans 2008; Kahneman 2011): donors do not evaluate nonprofit brands through exhaustive attribute-by-attribute reasoning. Different brand dimensions activate different evaluative processes — some operate as heuristic enablers (awareness, familiarity as recognition triggers), others as deliberative criteria (trust, commitment as credence-quality proxies), and others as affective amplifiers (personality, associations as excitement signals). These process differences predict different functional response shapes.

From the charity choice architecture literature (Bekkers & Wiepking 2011; Sargeant & Lee 2004): charitable decisions are threshold-gated. An organisation that falls below a minimum trust or awareness threshold is simply not considered; above the threshold, differentiation factors begin to operate. This implies a non-linear, threshold-conditional structure that symmetric regression evidence cannot capture.

From the Kano model of customer satisfaction (Kano et al. 1984; Brandt 1987): product — and by extension, brand — attributes sort into three functional categories. Must-be attributes are hygiene factors whose absence produces dissatisfaction but whose presence produces no satisfaction gain; performance attributes produce symmetric satisfaction; excitement attributes produce asymmetric satisfaction gain. These categories map naturally onto the three tiers of the dashboard framework.

The four analyses are methodologically complementary in the following way. Dominance analysis provides the *priority ordering* of brand equity dimensions across donation outcomes. Kano-analog analysis provides the *functional classification* of each dimension. Segmented regression provides *investment threshold parameters* for the dimension most likely to exhibit saturation. Empathy cluster moderation provides *boundary conditions* — the population segments within which the preceding classifications hold or fail. Together they constitute a multi-lens evidence base for a management-relevant dashboard.

It is worth making explicit what the four methods share epistemologically. Each method belongs to the tradition of exploratory data analysis in the sense that it does not test a single pre-specified null hypothesis but instead characterises a pattern in the data — a priority ranking, a functional shape, a threshold location, a cluster structure. This is appropriate for the chapter's scientific purpose, which is pattern detection and characterisation, not hypothesis confirmation. The hypotheses articulated in Sections 9.3.2 and 9.4.2 function as structured priors that sharpen interpretation rather than as formal null hypotheses to be rejected. The risk of spurious pattern detection, however, is real; the chapter addresses this risk by requiring convergence across multiple methods before drawing dashboard-relevant conclusions. A finding that emerges from dominance analysis alone but is not corroborated by the Kano classification or the moderation analysis is flagged as exploratory and excluded from the primary dashboard tier assignments.

---

## 9.3 Dominance Analysis: Unique Variance Attribution

### 9.3.1 Method and Design Rationale

Standard multiple regression — and by extension, standard SEM path analysis — cannot answer the question of which predictor contributes most uniquely to outcome variance. Path coefficients are partial effects conditional on all other predictors; they are sensitive to inter-predictor correlations and change when the predictor set changes. In a domain such as nonprofit brand equity, where theoretical constructs are substantially intercorrelated by design, partial coefficients systematically underestimate the contribution of constructs that are themselves correlated with other strong predictors.

Dominance analysis, developed by Budescu (1993) and extended by Azen and Budescu (2003), addresses this problem by computing a predictor's **general dominance weight**: the average increase in R² that accrues when that predictor is added to *all possible submodels* of the remaining predictors. General dominance weights sum to the total R² of the full model, enabling direct percentage-of-variance attribution without the interpretation problems of partial regression coefficients.[^NB-000110]

The analysis uses the `domir` package (Luchman 2022) in R. Three separate dominance analyses are conducted, one for each donation outcome:

- **Outcome 1:** `OF02_01_num_log` — log-transformed donation frequency
- **Outcome 2:** `OF02_02_num_log` — log-transformed donation amount
- **Outcome 3:** `OF_Spender_bin` — binary donor status (logistic dominance via pseudo-R²)

The predictor set for the FC_BO model includes: Brand Awareness (`FC_BS`), Brand Image/Associations (`FC_BI`), Brand Personality (`FC_BP`), Brand Differentiation (`FC_BD`), Brand Familiarity (`FC_BF`), Brand Relevance (`FC_BR`), Brand Trust (`BO_TR`), Brand Commitment (`BO_CO`), and the covariate SES_z. The covariate is included in all submodels to ensure dominance weights are estimated net of socioeconomic confounding.

For the Romero model, the predictor set covers the nine RO first-order factors (`RO_BA`, `RO_BAS`, `RO_BQ`, `RO_BL`, `RO_BAUT`, `RO_BREP`, `RO_BP`, `RO_BD`, `RO_BR`) plus SES_z.

### 9.3.2 Theoretical Expectations

Three directional hypotheses motivate the dominance analysis, derived from the BEBA knowledge graph and the structural evidence of Chapter 8.

**Hypothesis DA-1 (Trust Dominance):** Brand Trust (`BO_TR`) will show the highest or joint-highest general dominance weight across all three donation outcomes. Theoretical basis: the credence-good character of charitable organisations shifts relational weight onto trust as the primary behavioural lever (cf. Chapter 2, Section 2.4). The BEBA knowledge graph assigns Brand Trust a posterior behavioural integration weight of BT_INT = 0.892.[^NB-000111]

**Hypothesis DA-2 (Differentiation Subordination):** Brand Differentiation (`FC_BD`, or its Romero equivalent `RO_BD`) will show the lowest or near-lowest general dominance weight across all three outcomes. Theoretical basis: in the Austrian charity landscape, where major organisations are institutionally well-established, differentiation along brand personality lines adds marginal unique variance beyond the shared brand quality signal. BEBA knowledge graph posterior: BD_BEH = 0.611.

**Hypothesis DA-3 (Sectoral Heterogeneity):** Dominance weight orderings will differ non-trivially across NPO sectors (humanitarian, environmental, religious, animal welfare). Theoretical basis: empathy-domain specificity in donor motivation (cf. Section 9.6) implies that different brand equity dimensions function as dominant cues in different sectoral contexts.

### 9.3.3 Results

**Table 9.1 — General Dominance Weights: FC_BO Predictors × Three Donation Outcomes**

| Predictor | Outcome 1 (Freq.) | Outcome 2 (Amt.) | Outcome 3 (Binary) | Mean D. Weight |
|---|---|---|---|---|
| Brand Trust (BO_TR) | [PIPELINE: domir_FC_BO_freq → gd_BO_TR] | [PIPELINE: domir_FC_BO_amount → gd_BO_TR] | [PIPELINE: domir_FC_BO_bin → gd_BO_TR] | [PIPELINE: domir → mean_gd_BO_TR] |
| Brand Commitment (BO_CO) | [PIPELINE: domir_FC_BO_freq → gd_BO_CO] | [PIPELINE: domir_FC_BO_amount → gd_BO_CO] | [PIPELINE: domir_FC_BO_bin → gd_BO_CO] | [PIPELINE: domir → mean_gd_BO_CO] |
| Brand Awareness (FC_BS) | [PIPELINE: domir_FC_BO_freq → gd_FC_BS] | [PIPELINE: domir_FC_BO_amount → gd_FC_BS] | [PIPELINE: domir_FC_BO_bin → gd_FC_BS] | [PIPELINE: domir → mean_gd_FC_BS] |
| Brand Image/Assoc. (FC_BI) | [PIPELINE: domir_FC_BO_freq → gd_FC_BI] | [PIPELINE: domir_FC_BO_amount → gd_FC_BI] | [PIPELINE: domir_FC_BO_bin → gd_FC_BI] | [PIPELINE: domir → mean_gd_FC_BI] |
| Brand Personality (FC_BP) | [PIPELINE: domir_FC_BO_freq → gd_FC_BP] | [PIPELINE: domir_FC_BO_amount → gd_FC_BP] | [PIPELINE: domir_FC_BO_bin → gd_FC_BP] | [PIPELINE: domir → mean_gd_FC_BP] |
| Brand Relevance (FC_BR) | [PIPELINE: domir_FC_BO_freq → gd_FC_BR] | [PIPELINE: domir_FC_BO_amount → gd_FC_BR] | [PIPELINE: domir_FC_BO_bin → gd_FC_BR] | [PIPELINE: domir → mean_gd_FC_BR] |
| Brand Familiarity (FC_BF) | [PIPELINE: domir_FC_BO_freq → gd_FC_BF] | [PIPELINE: domir_FC_BO_amount → gd_FC_BF] | [PIPELINE: domir_FC_BO_bin → gd_FC_BF] | [PIPELINE: domir → mean_gd_FC_BF] |
| Brand Differentiation (FC_BD) | [PIPELINE: domir_FC_BO_freq → gd_FC_BD] | [PIPELINE: domir_FC_BO_amount → gd_FC_BD] | [PIPELINE: domir_FC_BO_bin → gd_FC_BD] | [PIPELINE: domir → mean_gd_FC_BD] |
| SES_z | [PIPELINE: domir_FC_BO_freq → gd_SES] | [PIPELINE: domir_FC_BO_amount → gd_SES] | [PIPELINE: domir_FC_BO_bin → gd_SES] | [PIPELINE: domir → mean_gd_SES] |
| **Total R²** | [PIPELINE: domir_FC_BO_freq → R2_full] | [PIPELINE: domir_FC_BO_amount → R2_full] | [PIPELINE: domir_FC_BO_bin → pseudo_R2_full] | — |

*Note.* General dominance weights are expressed as proportions of the total R² attributable to each predictor, summing to 1.00 within each outcome column. Estimates are computed using the `domir` package (Luchman 2022) with 2^k − 1 submodel averaging. Logistic pseudo-R² for the binary outcome follows the McFadden (1974) convention.

**Table 9.2 — Sectoral Dominance Heatmap: Brand Trust General Dominance Weight by NPO Sector**

| NPO Sector | Outcome 1 (Freq.) | Outcome 2 (Amt.) | Outcome 3 (Binary) |
|---|---|---|---|
| Humanitarian | [PIPELINE: domir → sector_humanitarian_gd_BT_freq] | [PIPELINE: domir → sector_humanitarian_gd_BT_amt] | [PIPELINE: domir → sector_humanitarian_gd_BT_bin] |
| Environmental | [PIPELINE: domir → sector_environmental_gd_BT_freq] | [PIPELINE: domir → sector_environmental_gd_BT_amt] | [PIPELINE: domir → sector_environmental_gd_BT_bin] |
| Animal Welfare | [PIPELINE: domir → sector_animal_gd_BT_freq] | [PIPELINE: domir → sector_animal_gd_BT_amt] | [PIPELINE: domir → sector_animal_gd_BT_bin] |
| Religious/Social | [PIPELINE: domir → sector_religious_gd_BT_freq] | [PIPELINE: domir → sector_religious_gd_BT_amt] | [PIPELINE: domir → sector_religious_gd_BT_bin] |
| Emergency Services | [PIPELINE: domir → sector_emergency_gd_BT_freq] | [PIPELINE: domir → sector_emergency_gd_BT_amt] | [PIPELINE: domir → sector_emergency_gd_BT_bin] |

*Note.* Cell values represent Brand Trust general dominance weights within each sector subsample. Sector classification follows the NPO categories operationalised in the survey instrument (EW01 empathy domain coding).

### 9.3.4 Interpretation Framework

The dominance weight ordering in Table 9.1 constitutes an empirically grounded *investment priority ranking* for nonprofit brand management. Dimensions with high general dominance weights yield greater unique returns across all subsets of the predictor space; they should be managed as primary performance levers. Dimensions with low general dominance weights contribute mainly via their collinearity with more dominant constructs; their contribution is real but not independent.

Three interpretive principles apply to the sectoral heatmap (Table 9.2). First, if Brand Trust dominance weights are substantially higher in humanitarian and emergency-services contexts than in environmental or animal welfare sectors, this implies that trust-based communication is sector-specifically effective rather than universally dominant. Second, heterogeneity across outcomes (frequency vs. amount vs. binary) within a sector indicates that the brand dimension predicts *whether* someone gives differently from *how much* and *how often* — a distinction with direct implications for donor segmentation and campaign design. Third, very low dominance weights (< 5% of total R²) across all outcomes and sectors should be read as evidence that the dimension belongs to the dashboard's threshold tier — it must clear a minimum bar but does not function as a differentiating lever.

A further interpretive consideration concerns the relationship between dominance weights and dominance *relations*. Azen and Budescu (2003) distinguish between general dominance (the average R² contribution across all submodels), conditional dominance (the average R² contribution at each level of subset size), and complete dominance (predictor A increases R² by more than predictor B in every possible submodel). General dominance weights, as reported in Table 9.1, summarise the priority ordering efficiently but may obscure cases where two predictors exchange rank depending on what other predictors are included — a pattern that general dominance averages over. The pipeline output `domir_FC_BO_freq.rds` contains the full conditional dominance matrices, which should be consulted when adjacent predictors have similar general dominance weights, as the rank uncertainty in those cases is meaningful for management interpretation.

---

## 9.4 Kano-Analog Analysis: Penalty-Reward Classification

### 9.4.1 Method: Penalty-Reward Contrast (Brandt 1987)

The original Kano model (Kano et al. 1984) classifies product attributes through paired questionnaires that elicit responses to both the presence and absence of each attribute. While this design is straightforward for product features, it is not directly transferable to psychometric survey data where constructs are measured on continuous scales rather than as binary presence/absence conditions. The penalty-reward contrast method, developed by Brandt (1987) and further elaborated by Matzler and Hinterhuber (1998) for customer satisfaction research, provides an operationally tractable analogue.

The method proceeds in four steps. First, each brand equity dimension is median-split into a *low* (below median) and *high* (above median) group. This dichotomisation is analytically motivated, not theoretically preferred: it creates the contrast necessary to observe asymmetric effects. Second, two regression coefficients are estimated for each dimension: the **penalty coefficient** (β_low), representing the marginal effect on the donation outcome when the dimension is in the low group relative to a baseline, and the **reward coefficient** (β_high), representing the marginal gain when the dimension is in the high group. Technically, this is implemented via a dummy-coded regression with Low and High dummies and a middle reference category around the median, though in practice the median-split typically produces only two usable groups.

Third, the **asymmetry ratio** is computed as:

$$\text{Asymmetry Ratio} = \frac{\beta_{\text{high}}}{|\beta_{\text{low}}|}$$

An asymmetry ratio substantially below 1.0 indicates that the penalty for low levels exceeds the reward for high levels — the Must-be / Floor / BBB pattern. A ratio near 1.0 indicates symmetric linear effects — the Performance / BUB pattern. A ratio substantially above 1.0 indicates that the reward for high levels exceeds the penalty for low levels — the Excitement / Ceiling / BRB pattern.[^CB-000030]

Fourth, constructs are classified as Must-be (BBB), Performance (BUB), or Excitement (BRB) based on the asymmetry ratio and a minimum threshold for both coefficients ensuring the construct has any detectable effect. Constructs with neither β_low nor β_high significantly different from zero are classified as **Indifferent** and are excluded from dashboard prioritisation.

It is important to acknowledge the epistemological status of the median-split operation. Dichotomisation of continuous scales reduces statistical power and introduces classification error at values close to the median. The method is adopted here not because it is the most powerful approach — spline regression would be preferable in that respect — but because it produces asymmetry ratios that are directly interpretable in the Kano framework and directly communicable to a management audience. The results should therefore be understood as directional classifications rather than precise effect size estimates. Bootstrapped confidence intervals for the asymmetry ratios (n_boot = 1000 iterations, bias-corrected) are reported from the pipeline to quantify classification uncertainty.

The analysis is conducted on the FC_BO dataset with donation frequency (`OF02_01_num_log`) as the primary outcome, replicating for donation amount (`OF02_02_num_log`) as a robustness check. Binary donor status is analysed via logistic regression with log-odds as the outcome metric.

### 9.4.2 Theoretical Expectations per Construct

**Brand Awareness (FC_BS) — Expected: Must-be (BBB).** Brand awareness functions as a cognitive prerequisite to charitable consideration. Organisations that fall below minimum recognition thresholds are simply absent from the donor's evoked set. However, high brand awareness cannot in itself produce donation behaviour — an organisation may be highly salient and still uninspiring. This asymmetry predicts a BBB classification: the cost of low awareness exceeds the reward of high awareness.[^NB-000112]

**Brand Image and Associations (FC_BI) — Expected: Performance (BUB).** Brand image captures the substantive evaluative content associated with a nonprofit — perceived mission clarity, impact effectiveness, and beneficiary relevance. These associations scale with donor intention in a relatively symmetric fashion: stronger associations produce stronger intentions, but the relationship is not fundamentally threshold-gated. A BUB classification is expected.

**Brand Personality (FC_BP) — Expected: Performance (BUB) or Excitement (BRB).** Brand personality — warmth, sincerity, competence dimensions — may produce modest excitement effects in empathy-active donor segments, but across the full sample the effect is likely to be moderate and approximately symmetric, given that personality perceptions are secondary to impact and trust evaluations in Austrian donor psychology.

**Brand Trust (BO_TR) — Expected: Excitement (BRB).** Trust in nonprofit organisations is, as Chapter 2 argues, the pre-eminent credence-quality substitute in a domain where output verification is structurally impossible. The reward for high trust is predicted to markedly exceed the penalty for low trust — not because low trust is unimportant, but because in the Austrian context many organisations clear the minimum trust threshold as a matter of institutional standing, making high trust a differentiating rather than a merely qualifying attribute.

**Brand Commitment (BO_CO) — Expected: Excitement (BRB).** Commitment captures the psychological depth of donor–organisation attachment and is theoretically linked to long-term giving behaviour, advocacy, and relationship maintenance. High commitment should produce disproportionate reward effects as it activates identity-consistent behaviour. Low commitment, while reducing donation likelihood, may be compensated by other dimensions for occasional donors.

**Brand Differentiation (FC_BD) — Expected: Indifferent or weak Performance.** In a market characterised by established, institutionally legitimate players, differentiation along personality or positioning lines contributes minimally to observed donation behaviour. The asymmetry ratio is expected to be close to 1.0 with small absolute coefficients.

### 9.4.3 Results

**Table 9.3 — Kano-Analog Classification of Brand Equity Dimensions (Outcome: Donation Frequency)**

| Brand Dimension | Median Score | β_low (Penalty) | β_high (Reward) | Asymmetry Ratio | Kano Type |
|---|---|---|---|---|---|
| Brand Awareness (FC_BS) | [PIPELINE: kano → median_FC_BS] | [PIPELINE: kano → beta_low_FC_BS] | [PIPELINE: kano → beta_high_FC_BS] | [PIPELINE: kano → asymmetry_ratio_BBB_FC_BS] | [PIPELINE: kano → type_FC_BS] |
| Brand Image/Assoc. (FC_BI) | [PIPELINE: kano → median_FC_BI] | [PIPELINE: kano → beta_low_FC_BI] | [PIPELINE: kano → beta_high_FC_BI] | [PIPELINE: kano → asymmetry_ratio_BUB_FC_BI] | [PIPELINE: kano → type_FC_BI] |
| Brand Personality (FC_BP) | [PIPELINE: kano → median_FC_BP] | [PIPELINE: kano → beta_low_FC_BP] | [PIPELINE: kano → beta_high_FC_BP] | [PIPELINE: kano → asymmetry_ratio_FC_BP] | [PIPELINE: kano → type_FC_BP] |
| Brand Relevance (FC_BR) | [PIPELINE: kano → median_FC_BR] | [PIPELINE: kano → beta_low_FC_BR] | [PIPELINE: kano → beta_high_FC_BR] | [PIPELINE: kano → asymmetry_ratio_FC_BR] | [PIPELINE: kano → type_FC_BR] |
| Brand Familiarity (FC_BF) | [PIPELINE: kano → median_FC_BF] | [PIPELINE: kano → beta_low_FC_BF] | [PIPELINE: kano → beta_high_FC_BF] | [PIPELINE: kano → asymmetry_ratio_FC_BF] | [PIPELINE: kano → type_FC_BF] |
| Brand Differentiation (FC_BD) | [PIPELINE: kano → median_FC_BD] | [PIPELINE: kano → beta_low_FC_BD] | [PIPELINE: kano → beta_high_FC_BD] | [PIPELINE: kano → asymmetry_ratio_FC_BD] | [PIPELINE: kano → type_FC_BD] |
| Brand Trust (BO_TR) | [PIPELINE: kano → median_BO_TR] | [PIPELINE: kano → beta_low_BO_TR] | [PIPELINE: kano → beta_high_BO_TR] | [PIPELINE: kano → asymmetry_ratio_BRB_BO_TR] | [PIPELINE: kano → type_BO_TR] |
| Brand Commitment (BO_CO) | [PIPELINE: kano → median_BO_CO] | [PIPELINE: kano → beta_low_BO_CO] | [PIPELINE: kano → beta_high_BO_CO] | [PIPELINE: kano → asymmetry_ratio_BRB_BO_CO] | [PIPELINE: kano → type_BO_CO] |

*Note.* Penalty and reward coefficients are OLS estimates from median-split dummy regressions controlling for SES_z. Asymmetry ratio = β_high / |β_low|. Classification thresholds: BBB < 0.75; BUB 0.75–1.33; BRB > 1.33. Bootstrapped 95% CIs for asymmetry ratios are available from pipeline output `kano_asymmetry_table.rds`.

### 9.4.4 Dashboard Implication of Kano Classification

The Kano classification carries direct implications for dashboard design and brand investment logic. **Must-be (BBB) constructs** define the nonprofit's threshold requirements: organisations that fall below their median must treat these dimensions as immediate remediation priorities, irrespective of their standing on other dimensions. Dashboard monitoring of BBB-type constructs should therefore employ *red-line* thresholds — alert conditions triggered at the lower quartile, not merely at below-average performance.

**Performance (BUB) constructs** support incremental efficiency tracking. These dimensions reward proportionate investment: each unit improvement produces a commensurate return. Dashboard indicators for BUB constructs should be tracked as continuous performance metrics with linear benchmarking against sector norms.

**Excitement (BRB) constructs** are the primary differentiation levers. Because their reward function outpaces the penalty function, they justify asymmetric investment: organisations that are already above median on BRB dimensions should invest further, while organisations below median on BRB dimensions may achieve greater return by first securing BBB threshold compliance before investing in excitement dimensions. Dashboard treatment of BRB constructs calls for *aspirational benchmarks* — sector-leading values rather than average performance targets.

---

## 9.5 Segmented Regression: Breakpoint Analysis for Brand Awareness

### 9.5.1 Purpose and Theoretical Motivation

The dominance analysis confirms the relative priority weight of Brand Awareness, and the Kano classification identifies its functional type. Neither analysis, however, resolves a third question with direct investment implications: **At what level of Brand Awareness does the marginal return on further awareness-building begin to diminish?** This question is a structural-break question, not answerable by linear or even polynomial regression, because it concerns whether the awareness–behaviour curve changes slope at a specific threshold value — the **breakpoint ψ**.

The theoretical motivation for expecting a breakpoint is well-grounded. Below a minimum awareness level, organisations are absent from the donor's consideration set entirely, so each unit increase in awareness produces substantial return as it moves the organisation across the consideration threshold. Above that threshold, awareness is no longer the binding constraint: other dimensions (trust, commitment, mission fit) determine donation likelihood. This implies a positive slope below ψ and a flatter or near-zero slope above ψ — a classic saturation curve.

### 9.5.2 Method: Segmented Regression

The analysis uses the `segmented` package in R (Muggeo 2003, 2008). Segmented regression estimates a piecewise linear model of the form:

$$Y = \alpha + \beta_1 \cdot X + \beta_2 \cdot (X - \psi)_+ + \epsilon$$

where $(X - \psi)_+$ denotes the positive part of $(X - \psi)$, $\psi$ is the estimated breakpoint, $\beta_1$ is the slope for $X < \psi$, and $\beta_1 + \beta_2$ is the slope for $X > \psi$. The breakpoint $\psi$ is estimated iteratively using the Muggeo (2003) algorithm, which linearises the problem around an initial starting value and converges to the maximum likelihood breakpoint.

Outcome: `OF02_01_num_log` (donation frequency, log-transformed). Predictor: Brand Awareness factor score (`FC_BS_score`). Covariates: SES_z included throughout. Starting value for $\psi$: the sample median of FC_BS_score.

The structural significance of the break is assessed via the **Davies test** (Davies 1987), a conservative test for the null hypothesis that no breakpoint exists ($\beta_2 = 0$). The Davies test p-value accounts for the floating-threshold problem inherent in break-point testing.

### 9.5.3 Results

**Estimated breakpoint:**

$$\hat{\psi} = [\text{PIPELINE: segmented\_BA\_donation\_intention} \rightarrow \text{psi\_breakpoint}]$$

**95% confidence interval for ψ:**

$$[\text{PIPELINE: segmented} \rightarrow \text{psi\_CI\_lower}], [\text{PIPELINE: segmented} \rightarrow \text{psi\_CI\_upper}]$$

**Slope below ψ (β₁):** [PIPELINE: segmented → slope_below_psi]

**Slope above ψ (β₁ + β₂):** [PIPELINE: segmented → slope_above_psi]

**Davies test for structural break:** p = [PIPELINE: segmented → davies_test_p]

### 9.5.4 Managerial Interpretation

The segmented regression result quantifies what threshold logic predicts qualitatively. If the estimated breakpoint ψ falls at approximately the mid-range of the brand awareness scale, this indicates that the awareness-building investment curve saturates within observable variance — that a substantial proportion of surveyed donors perceive their target organisations above the threshold where further awareness investment yields diminishing returns on donation frequency. Organisations whose current awareness score lies below ψ should treat awareness investment as high-priority; those above ψ should redirect resources toward the higher-ranked differentiation levers identified in the dominance analysis (Trust, Commitment).

A narrow confidence interval for ψ strengthens the investment implication: it indicates a well-localised transition point rather than a diffuse saturation gradient. A wide confidence interval or a non-significant Davies test would, conversely, suggest that the monotonic linear model is not decisively worse than the piecewise model — that no strong threshold characterises the awareness–frequency relationship in the present sample. Either result is informative for the dashboard framework.

The breakpoint analysis is intentionally restricted to the Brand Awareness → Donation Frequency pathway rather than applied to all brand equity dimensions. This is both a practical and theoretical choice. Practically, the `segmented` package requires a continuous predictor with sufficient within-sample variance to detect a structural break; dimensions with restricted variance or high ceiling effects (common in charitable trust scales among highly engaged donors) produce unreliable breakpoint estimates. Theoretically, Brand Awareness is the dimension for which a threshold model is most strongly motivated by prior literature and for which the gatekeeping mechanism (consideration-set filtering) provides a clear causal account of the slope change. For Trust and Commitment — which are hypothesised as Excitement dimensions with asymmetric *reward* rather than *saturation* effects — the Kano penalty-reward contrast is the more appropriate analytic tool, and the segmented regression would not identify a comparable investment-relevant threshold.

---

## 9.6 Empathy Profiling: EW Cluster Moderation

### 9.6.0 Section Overview

The empathy profiling section has a dual function within the chapter. Its first function is descriptive: to characterise the latent empathy structure of the Austrian donor population, identifying how many meaningfully distinct empathy profiles exist and what their defining characteristics are. This descriptive output is independently valuable — it constitutes the first systematic empathy typology of Austrian nonprofit donors using a multidimensional domain-specific empathy scale rather than a general empathy measure. Its second function is explanatory: to test whether the empathy profiles constitute meaningful moderator groups for the brand trust–donation relationship identified as dominant in Section 9.3. If empathy profiles are merely descriptive categories with no moderating effect on brand equity pathways, their value for the BEBA framework is limited to donor segmentation. If they moderate brand equity effects, they become integral to the behavioural architecture — boundary conditions that determine when and for whom specific brand investments are effective.

### 9.6.1 Empathy Domain Structure (EW01/EW02)

Donor empathy in the BEBA framework is not treated as a unidimensional personality trait. The survey instrument includes an **Empathy-World scale** (EW01) covering five substantively distinct empathy domains, each operationalised with 3–5 items:

1. **Menschen** (Menschen-Empathie): affective responsiveness to human suffering and social vulnerability, particularly in poverty, displacement, and illness contexts.
2. **Kinder** (Kinder-Empathie): specific empathic activation toward child welfare situations — a distinct sub-domain in Austrian donor psychology given the prominence of child-focused organisations (SOS Kinderdorf, UNICEF Austria).
3. **Tiere** (Tier-Empathie): affective responsiveness to animal welfare situations, including domestic and wildlife contexts.
4. **Umwelt** (Umwelt-Empathie): concern activation toward environmental degradation, climate impact, and ecological systems — functionally distinct from interpersonal empathy.
5. **Einsatzkräfte** (Einsatzkräfte-Empathie): solidarity and support motivation specifically toward emergency responders, rescue workers, and disaster relief personnel.

The EW02 scale captures the donor's explicit **priority ordering** among these five domains, generating a ranked preference profile that may differ from the EW01 intensity scores. The combination of EW01 intensity and EW02 priority produces a multidimensional empathy profile per respondent.

### 9.6.2 Clustering Method

Donor empathy profiles are derived via **k-means clustering** on the five EW01 dimension scores, standardised prior to clustering. The optimal number of clusters k is determined by the `NbClust` package (Charrad et al. 2014), which evaluates 26 different cluster validity indices and selects k by majority vote across indices. This multi-index approach avoids over-reliance on any single criterion and has been shown to outperform single-index selection on simulated and empirical data (Milligan & Cooper 1985).

Clustering is conducted with 25 random restarts per candidate k value, retaining the solution with the lowest total within-cluster sum of squares. Cluster stability is assessed by bootstrap resampling (n_boot = 500 iterations), computing the Jaccard similarity coefficient between cluster solutions across bootstrap samples; values above 0.75 indicate stable clusters (Hennig 2007).

### 9.6.3 Cluster Solutions and Profiles

**Optimal number of clusters:** k = [PIPELINE: EW_clusters → n_clusters] (determined by NbClust majority vote: [PIPELINE: EW_clusters → NbClust_majority_vote] of 26 indices agree).

**Table 9.4 — Empathy Cluster Centroids (Standardised EW01 Scores)**

| Cluster | n | Menschen | Kinder | Tiere | Umwelt | Einsatzkräfte | Label |
|---|---|---|---|---|---|---|---|
| 1 | [PIPELINE: EW_clusters → n_C1] | [PIPELINE: EW_clusters → centroid_C1_Menschen] | [PIPELINE: EW_clusters → centroid_C1_Kinder] | [PIPELINE: EW_clusters → centroid_C1_Tiere] | [PIPELINE: EW_clusters → centroid_C1_Umwelt] | [PIPELINE: EW_clusters → centroid_C1_Einsatz] | [PIPELINE: EW_clusters → label_C1] |
| 2 | [PIPELINE: EW_clusters → n_C2] | [PIPELINE: EW_clusters → centroid_C2_Menschen] | [PIPELINE: EW_clusters → centroid_C2_Kinder] | [PIPELINE: EW_clusters → centroid_C2_Tiere] | [PIPELINE: EW_clusters → centroid_C2_Umwelt] | [PIPELINE: EW_clusters → centroid_C2_Einsatz] | [PIPELINE: EW_clusters → label_C2] |
| 3 | [PIPELINE: EW_clusters → n_C3] | [PIPELINE: EW_clusters → centroid_C3_Menschen] | [PIPELINE: EW_clusters → centroid_C3_Kinder] | [PIPELINE: EW_clusters → centroid_C3_Tiere] | [PIPELINE: EW_clusters → centroid_C3_Umwelt] | [PIPELINE: EW_clusters → centroid_C3_Einsatz] | [PIPELINE: EW_clusters → label_C3] |
| 4 | [PIPELINE: EW_clusters → n_C4] | [PIPELINE: EW_clusters → centroid_C4_Menschen] | [PIPELINE: EW_clusters → centroid_C4_Kinder] | [PIPELINE: EW_clusters → centroid_C4_Tiere] | [PIPELINE: EW_clusters → centroid_C4_Umwelt] | [PIPELINE: EW_clusters → centroid_C4_Einsatz] | [PIPELINE: EW_clusters → label_C4] |

*Note.* Centroids are reported in standardised units (z-scores). Cluster labels are descriptive interpretations pending validation. Bootstrap Jaccard stability coefficients: [PIPELINE: EW_clusters → jaccard_stability_all_clusters].

### 9.6.4 Cluster Moderation of Brand Trust Effects

The central moderation question is whether the path coefficient Brand Trust → Donation Frequency differs significantly across empathy clusters. A significant cluster × brand-trust interaction would imply that the dominance weight of Brand Trust (Section 9.3) and its Kano classification (Section 9.4) are not uniformly valid across the donor population — that empathy profile constitutes a boundary condition for the effectiveness of trust-based brand communication.

**Table 9.5 — Brand Trust Path Coefficients by Empathy Cluster (Outcome: Donation Frequency)**

| Empathy Cluster | β_BT_cluster | SE | 95% CI | Dominant EW Domain |
|---|---|---|---|---|
| Cluster 1 | [PIPELINE: EW_cluster_moderation_BT → beta_C1] | [PIPELINE: EW_cluster_moderation_BT → se_C1] | [PIPELINE: EW_cluster_moderation_BT → CI_C1] | [PIPELINE: EW_clusters → dominant_domain_C1] |
| Cluster 2 | [PIPELINE: EW_cluster_moderation_BT → beta_C2] | [PIPELINE: EW_cluster_moderation_BT → se_C2] | [PIPELINE: EW_cluster_moderation_BT → CI_C2] | [PIPELINE: EW_clusters → dominant_domain_C2] |
| Cluster 3 | [PIPELINE: EW_cluster_moderation_BT → beta_C3] | [PIPELINE: EW_cluster_moderation_BT → se_C3] | [PIPELINE: EW_cluster_moderation_BT → CI_C3] | [PIPELINE: EW_clusters → dominant_domain_C3] |
| Cluster 4 | [PIPELINE: EW_cluster_moderation_BT → beta_C4] | [PIPELINE: EW_cluster_moderation_BT → se_C4] | [PIPELINE: EW_cluster_moderation_BT → CI_C4] | [PIPELINE: EW_clusters → dominant_domain_C4] |
| Omnibus cluster × BT interaction | — | — | — | p = [PIPELINE: EW_cluster_moderation_BT → interaction_p] |

*Note.* Path coefficients estimated via multi-group SEM with cluster membership as grouping variable. Omnibus test uses the Satorra–Bentler scaled difference χ² test comparing the constrained (equal BT paths across clusters) and unconstrained models.

### 9.6.5 Interpretation

A significant omnibus interaction (Table 9.5, final row) would establish empathy-profile heterogeneity in brand trust effectiveness, with three concrete implications. First, it validates the theoretical claim that donor identity — expressed here as empathy domain profile — moderates the cognitive route by which brand signals translate into donation behaviour (cf. Chapter 2, Section 2.6 on identity-based giving). Second, it qualifies the dominance analysis finding: if Brand Trust is the highest-weight predictor on average but its effect is near-zero in one or more empathy clusters, the average dominance weight overstates its universality. Third, and most practically, it implies that trust-building communication should be targeted to high-trust-responsive empathy profiles rather than broadcast homogeneously.

If the interaction is not significant — if Brand Trust path coefficients are statistically equivalent across clusters — this constitutes a positive finding of a different kind: it implies that trust is a genuinely cross-segment dimension whose effectiveness does not depend on empathy-domain alignment, strengthening its identification as the primary management lever regardless of donor segmentation strategy.

---

## 9.7 Dashboard Synthesis: The Three-Tier Evidence-Based Brand Framework

### 9.7.1 Design Logic

The four preceding analyses converge on a **three-tier evidence-based brand dashboard framework** for nonprofit brand management. The tier structure is not imposed a priori from the Kano model; it emerges from the convergent evidence of dominance weights, asymmetry ratios, breakpoint analysis, and cluster moderation results. A dimension's tier assignment is determined by the preponderance of evidence across all four lenses, making the framework more robust than any single method would allow.

The three tiers are:

- **Threshold Tier (Must-be / BBB):** Dimensions whose absence generates the greatest penalisation relative to their reward potential. These are non-negotiable minimum standards. Dashboard function: compliance monitoring with sector-specific floor thresholds.
- **Performance Tier (Linear / BUB):** Dimensions whose effect is symmetric and proportionate. These reward sustained, incremental investment. Dashboard function: continuous benchmarking against sector-norm trajectories.
- **Differentiation Tier (Excitement / BRB):** Dimensions with asymmetric reward potential and high dominance weights. These are the primary levers for organisational distinction and competitive positioning. Dashboard function: aspirational benchmarking with cluster-specific targeting.

### 9.7.2 Construct Assignment and Evidence Summary

**Table 9.6 — Three-Tier Dashboard Framework: Construct Assignment and Evidence Basis**

| Tier | Construct | Kano Type | Dom. Weight Rank | Breakpoint? | Cluster-Moderated? | Management Implication |
|---|---|---|---|---|---|---|
| Threshold | Brand Awareness (FC_BS) | BBB (expected) | [PIPELINE: domir → rank_FC_BS] | ψ = [PIPELINE: segmented → psi_breakpoint] | [PIPELINE: EW_cluster_moderation_BT → moderated_BA] | Monitor minimum recognition; redirect above ψ |
| Threshold | Brand Familiarity (FC_BF) | [PIPELINE: kano → type_FC_BF] | [PIPELINE: domir → rank_FC_BF] | Not tested | [PIPELINE: EW_cluster_moderation_BT → moderated_BF] | Ensure regular communication touchpoints |
| Performance | Brand Image/Assoc. (FC_BI) | BUB (expected) | [PIPELINE: domir → rank_FC_BI] | Not tested | [PIPELINE: EW_cluster_moderation_BT → moderated_BI] | Content-quality investment scales linearly |
| Performance | Brand Relevance (FC_BR) | [PIPELINE: kano → type_FC_BR] | [PIPELINE: domir → rank_FC_BR] | Not tested | [PIPELINE: EW_cluster_moderation_BT → moderated_BR] | Mission-value alignment messaging |
| Performance | Brand Personality (FC_BP) | [PIPELINE: kano → type_FC_BP] | [PIPELINE: domir → rank_FC_BP] | Not tested | [PIPELINE: EW_cluster_moderation_BT → moderated_BP] | Character-consistent communication |
| Differentiation | Brand Trust (BO_TR) | BRB (expected) | [PIPELINE: domir → rank_BO_TR] | Not primary | [PIPELINE: EW_cluster_moderation_BT → moderated_BT] | Transparency investment; highest ROI above threshold |
| Differentiation | Brand Commitment (BO_CO) | BRB (expected) | [PIPELINE: domir → rank_BO_CO] | Not tested | [PIPELINE: EW_cluster_moderation_BT → moderated_CO] | Relationship programmes; loyalty architecture |
| — | Brand Differentiation (FC_BD) | Indifferent (expected) | [PIPELINE: domir → rank_FC_BD] | Not tested | Not tested | Low standalone return; support other tiers |

*Note.* Tier assignments marked "(expected)" are theoretical priors; actual assignments follow from pipeline results. Discrepancies between expected and observed assignments are reported in Section 9.8.

### 9.7.2a Tier Coherence Check

Before specifying KPIs, a methodological coherence check is required: the three-tier assignment in Table 9.6 should be consistent across the four analytical lenses. A construct genuinely belonging to the Threshold tier should show (a) a BBB Kano classification, (b) a comparatively lower dominance weight than Differentiation-tier constructs (since its variance contribution is more diffusely distributed across low-to-moderate values rather than concentrated at high values), (c) a significant breakpoint if threshold-gating is a strong feature, and (d) relatively consistent cluster-moderated path coefficients (because threshold effects are less identity-contingent than relational effects). Conversely, a Differentiation-tier construct should show (a) a BRB Kano classification, (b) the highest dominance weights, (c) no breakpoint (or a breakpoint at the high end of its scale), and (d) significant cluster moderation indicating population-segment sensitivity.

Any construct whose profile does not cohere across all four lenses is flagged as a **cross-method ambiguity**. Ambiguous constructs are not excluded from the dashboard but are annotated with uncertainty markers, and their tier assignments are treated as provisional pending longitudinal or experimental evidence. The pipeline output `kano_asymmetry_table.rds` includes a cross-method coherence column generated during analysis. Coherence failures are reported in Section 9.8 as part of the limitations discussion.

### 9.7.3 KPI Recommendations for Nonprofit Brand Monitoring

The dashboard framework translates into a concrete set of Key Performance Indicators (KPIs) organised by tier. The following recommendations apply to nonprofit organisations with established sector positions (annual donation revenue > €1M); smaller or newer organisations may require modified thresholds pending sector-specific calibration.

**Tier 1 — Threshold KPIs:**

- *Brand Awareness Index*: Percentage of target-segment respondents who can spontaneously name or recognise the organisation. Recommended floor: sector-median score on FC_BS item set. Red-line alert: below lower quartile. Above-ψ organisations should not increase awareness spending without first identifying whether trust or commitment is the binding constraint.
- *Recency of Contact*: Average number of months since last organisational communication received by donor panel member. Recommended maximum gap: [sector-specific; requires calibration from the EW cluster segmentation].

**Tier 2 — Performance KPIs:**

- *Mission Clarity Score*: Mean FC_BI item score tracking the clarity and credibility of organisational mission communication. Benchmark: sector-mean trajectory over four reporting periods.
- *Value-Alignment Score*: Mean FC_BR item score tracking perceived match between organisational mandate and donor values. Benchmark: segment-adjusted norm per empathy cluster.
- *Brand Personality Consistency Index*: Deviation between intended brand personality dimensions (FC_BP items) and actual donor perceptions. Lower deviation = better consistency.

**Tier 3 — Differentiation KPIs:**

- *Trust Capital Index*: Composite BO_TR scale score, monitored quarterly. Recommended aspirational target: 90th percentile within sector. Investment priority: high above ψ_awareness. Evidence of trust depreciation (negative quarter-on-quarter trend) should trigger immediate crisis communication review.
- *Commitment Depth Score*: Mean BO_CO scale score, supplemented by behavioural proxies (repeat donation rate, multi-year retention, referral behaviour). Recommended programme: annual donor relationship programme targeting commitment deepening in the two most trust-responsive empathy clusters.
- *Cluster-Specific Trust-Effectiveness Score*: For organisations with access to donor segmentation data, compute Brand Trust path coefficient within each empathy cluster. This operationalises the moderation evidence of Section 9.6 as a live diagnostic.

**Cross-tier integration note.** The three-tier structure implies a **priority sequencing rule** for resource-constrained organisations: invest first in Tier 1 (threshold compliance), then in Tier 2 (performance scaling), and only then in Tier 3 (differentiation amplification). An organisation that invests heavily in trust-deepening campaigns while its brand awareness remains below ψ is investing in a high-reward dimension for a donor population that has not yet formed a stable consideration set — the excitement effect cannot fire where the threshold condition is not met. This sequencing rule is the principal practical output of combining the Kano classification with the dominance analysis and the breakpoint result. It is not derivable from any single method in isolation.

The sequencing rule should not be interpreted as unconditional. In crisis situations — where trust is actively under threat — organisations above ψ_awareness may need to redirect resources from performance-tier activities to trust-tier crisis management even if their Tier 1 compliance is intact. The dashboard framework is a planning tool for stable operating conditions; it is not designed to replace crisis communication judgement.

---

## 9.8 Discussion: Contribution, Limitations, and Implications for BEBA

### 9.8.0 Preliminary: Findings Relative to Theoretical Priors

Before evaluating the broader contribution of the chapter's findings, it is useful to assess the degree to which the results confirm or revise the theoretical priors encoded in the design of the analysis (Section 9.4.2) and in the BEBA knowledge graph (Section 9.3.2). Three outcomes are possible for each prior: confirmation (evidence aligns with theoretical expectation), revision (evidence diverges systematically from expectation in a theoretically interpretable direction), or inconclusive (evidence is non-significant or ambiguous across outcomes).

The dominance analysis hypotheses (DA-1 through DA-3) are evaluated against the general dominance weights in Table 9.1. The Kano classification expectations for each construct (Section 9.4.2) are evaluated against the asymmetry ratios in Table 9.3. Where a construct's observed Kano type departs from its expected type, this signals a finding of theoretical interest — for instance, if Brand Commitment emerges as a Performance (BUB) rather than Excitement (BRB) construct, this would challenge the relational-depth account of commitment in the BEBA theoretical framework and would require re-examination of the BO_CO measurement model.

These prior-to-result comparisons are not reported here with empirical values — those await pipeline execution — but the analytical scaffolding for their evaluation is documented in the BEBA knowledge graph and in the relevant claim anchors (CB-000030, CB-000031). The theoretical architecture of this chapter is therefore fully falsifiable: all priors are stated directionally prior to analysis, and deviations from expected patterns constitute genuine disconfirmatory evidence.

### 9.8.1 What This Chapter Contributes Beyond Chapter 8

Chapter 8 established the structural evidence base: which brand equity architecture survives Austrian replication, which paths from brand dimensions to donation outcomes are significant and in what direction. That evidence, while foundational, operates within the logic of symmetric linear models. Chapter 9 introduces four methodological lenses — dominance weighting, penalty-reward asymmetry, breakpoint detection, and cluster moderation — that collectively transform the symmetric structural evidence into an asymmetric, prioritised, and segmentation-qualified account of how brand dimensions actually function in the donor–organisation relationship.

The primary scientific contribution of this chapter is therefore methodological as well as substantive. Methodologically, it demonstrates that nonprofit brand management science requires tools beyond standard structural equation modelling: the priority ordering, functional classification, threshold identification, and population heterogeneity that are the practical prerequisites of any management-relevant dashboard cannot be read from SEM path coefficients alone. Substantively, it produces the first empirically grounded, multi-method brand dashboard framework in the Austrian nonprofit context and — to the extent that the methodological combination is novel — in nonprofit brand management literature more broadly.

The Kano-analog application to brand equity is specifically under-developed in the existing literature. While Kano classifications have been applied to product features and to service quality in commercial contexts (Matzler & Hinterhuber 1998; Mikulic & Prebežac 2011), systematic penalty-reward contrasts for nonprofit brand dimensions appear to be absent from published empirical work. The present analysis provides a methodological template replicable in other nonprofit brand equity research programmes.

### 9.8.2 Limitations of the Dashboard Approach

Several limitations qualify the dashboard framework's scope and generalisability.

**Median-split attenuation.** The Kano-analog method requires median-splitting continuous scales, which discards within-group variance and reduces statistical power. Asymmetry ratios are therefore less precisely estimated than path coefficients from the corresponding continuous-scale models. Future work should consider spline regression as a more powerful continuous alternative to the penalty-reward contrast.

**Single-wave cross-sectional data.** The dominance weights, asymmetry ratios, and breakpoint estimates are derived from cross-sectional data. Whether the tier assignments are stable over time — whether Brand Trust reliably remains a BRB dimension across donation cycles and economic conditions — cannot be established without longitudinal or repeated-cross-section data. The dashboard should therefore be understood as a time-stamped evidence framework requiring periodic empirical recalibration.

**Cluster solution dependency.** The empathy cluster moderation findings depend on the specific cluster solution produced by the NbClust-guided k-means analysis. K-means solutions are sensitive to the random-seed initialisation (mitigated here by 25 restarts), the choice of distance metric (Euclidean assumed), and the set of validity indices used for k selection. Alternative clustering algorithms (hierarchical agglomerative, model-based Gaussian mixture models) may produce different segment structures and therefore different moderation patterns.

**Construct-level aggregation.** The dashboard framework assigns constructs to tiers at the construct level, obscuring potential item-level heterogeneity. Individual items within a scale may exhibit different functional characteristics than the scale aggregate. More granular item-level Kano analysis is possible but falls outside the scope of the present chapter.

**Dominance analysis assumption of additive effects.** The domir implementation of dominance analysis relies on the submodel-averaging approach, which assumes that the relationship between predictors and outcome is additive in the R² metric. Interaction effects — including the cluster moderation detected in Section 9.6 — are not captured in the general dominance weights, which are therefore marginal average weights rather than interaction-conditional weights. A dominance analysis that incorporates interaction terms within each submodel would provide a more nuanced priority ordering but requires an exponentially larger submodel space (2^k where k includes interaction terms), making it computationally intractable for predictor sets of the present size.

**Temporal stability of Kano classifications.** There is theoretical reason to expect that Kano classifications are not stable over a product's or brand's lifecycle. What functions as an Excitement attribute in a brand's growth phase may become a Must-be attribute as it becomes institutionally normalised and competitor brands match its level. For nonprofit brands, this temporal dynamic implies that Trust — currently hypothesised as an Excitement attribute in the Austrian context — may migrate toward the Performance tier as transparency-signalling practices (audits, impact reporting, donation-tracking technology) become sector-standard. The present analysis provides a cross-sectional snapshot that should be interpreted within this dynamic possibility.

**Austrian-market specificity.** The breakpoint ψ estimated in Section 9.5, the empathy cluster structure in Section 9.6, and the asymmetry ratios in Section 9.4 are specific to the Austrian donor population surveyed in this study. Austria's combination of high institutional charity trust, Spendengütesiegel regulatory visibility, and concentrated market structure (a small number of dominant national brands capturing the majority of individual donations) creates a brand-equity landscape that may not generalise to more fragmented markets (Germany, Switzerland, UK) or to markets with lower baseline institutional trust (Eastern European contexts, Global South). Portability of the dashboard framework should not be assumed without replication.

**Generalisability to the sector.** The sample was recruited with reference to established Austrian charity brands. Organisations that are sector-new, internationally unfamiliar, or operating in thematically niche domains may face different functional landscapes than the three-tier framework predicts. Threshold values and asymmetry ratios should be recalibrated before application beyond the sampled organisational range.

### 9.8.3 Implications for Chapter 10 and BEBA

The dashboard framework produced in this chapter serves as the *practical referent* for the BEBA architecture developed and tested in Chapter 10. The BEBA model is not a dashboard per se; it is a theoretical account of how brand equity dimensions jointly produce behavioural outcomes under uncertainty. But the BEBA architecture must be evaluable against the management implications derived here: a model that cannot account for the Trust dominance, the awareness breakpoint, or the Excitement character of commitment dimensions would be theoretically deficient relative to the evidence base.

Specifically, the tier structure anticipates the pathway structure of BEBA. The threshold tier implies that BEBA must include a **gatekeeping function** — brand dimensions that operate as necessary (but not sufficient) conditions for behavioural activation. The differentiation tier implies that BEBA must include an **amplification mechanism** — dimensions whose effects are non-linearly increasing in the brand–behaviour translation. The performance tier implies a **scaling mechanism** — dimensions whose contribution grows proportionately with investment without acceleration or deceleration. Chapter 10 develops and tests the structural model that integrates all three mechanisms within a single coherent behavioural architecture.[^CB-000031]

The empathy cluster moderation evidence carries a further implication for BEBA's theoretical scope conditions. If the Brand Trust path coefficient is significantly larger in high-empathy-human clusters than in high-empathy-animal or high-empathy-environment clusters, BEBA's general architecture may need to incorporate an **identity-alignment amplifier** — a mechanism by which empathy-domain congruence between donor and organisational mission moderates the brand-equity-to-behaviour pathway. This would extend the BEBA model beyond its currently proposed cross-sector invariance assumption and require that the Chapter 10 multi-group analysis test not only factor loadings and intercepts but also structural path invariance across empathy cluster groups. Whether such an extension is theoretically motivated and empirically necessary is a question the Chapter 9 moderation evidence directly bears upon.

Finally, the segmented regression breakpoint ψ serves a specific function within the BEBA knowledge graph: it is the empirical operationalisation of the concept of a **behavioural threshold** — the scale value below which brand awareness functions as a gatekeeping variable and above which it becomes a background condition. The location of ψ relative to the observed distribution of FC_BS scores in the sample determines what proportion of the surveyed nonprofit organisations operate below versus above the threshold, and therefore for what proportion of the sector the awareness-investment argument applies. This population-level interpretation of ψ transforms a statistical breakpoint into a sector-diagnostic — a tool for identifying where within the Austrian charity landscape the three tiers of the dashboard are binding versus already satisfied.

---

## Footnotes

[^NB-000110]: The dominance analysis methodology is grounded in Budescu (1993), who first formalised the concept of general, conditional, and complete dominance within the regression framework. Azen and Budescu (2003) extended the framework and developed procedures for significance testing of dominance relationships. The `domir` package (Luchman 2022) provides the computational implementation used here and supports both OLS and generalised linear models, enabling consistent dominance estimation across continuous and binary outcomes. In BEBA terminology, general dominance weights operationalise the concept of a construct's **behavioural integration score** — the empirical analogue of the theoretically derived BT_INT posterior weights in the knowledge graph.

[^NB-000111]: The BEBA knowledge graph assigns Brand Trust a posterior behavioural integration weight (BT_INT) of 0.892, derived from theory-integration across the TPB pathway literature, the charitable-decision literature, and the relational-marketing trust literature. This prior is not itself an empirical finding — it is a knowledge-engineering summary of accumulated theoretical evidence that should be updated by empirical dominance weights. If the general dominance analysis yields Brand Trust dominance weights substantially below 0.89 of total R², this constitutes evidence that the knowledge graph prior overestimates Trust's behavioural centrality in the Austrian context and should trigger a theoretical revision documented as an ADR.

[^NB-000112]: The threshold function of Brand Awareness in charitable choice contexts is discussed in Bekkers and Wiepking (2011), who identify *awareness of need* and *solicitation* as sequential gatekeeping conditions prior to any donation decision. Brand Awareness in the BEBA framework extends this logic from cause-level awareness to organisation-level cognitive accessibility: even where cause-awareness is present, an organisation that falls below recognition threshold is filtered from the choice set without further deliberative evaluation. The BBB classification expected for Brand Awareness formalises this gatekeeping role in Kano-functional terms.

[^CB-000030]: The penalty-reward contrast method, as developed by Brandt (1987), was originally applied to customer satisfaction data in commercial product contexts. Its transfer to nonprofit brand equity scales requires two methodological adaptations. First, the Likert-scaled continuous scores must be dichotomised, which necessarily discards fine-grained within-group variance — a limitation noted in Section 9.8.2. Second, the benchmark criterion is not satisfaction but donation behaviour, which has a substantially skewed distribution (many zero observations, right-skewed amounts). Log transformation of donation outcomes prior to the regression step addresses this second issue and is standard practice in the donation economics literature (Andreoni & Payne 2013).

[^CB-000031]: Chapter 10 will evaluate whether the BEBA structural model — incorporating Trust as a high-weight amplifier, Awareness as a threshold gatekeeper, and Commitment as a relational deepener — achieves superior fit and predictive validity relative to the three replication models assessed in Chapter 8. The three-tier dashboard provides the management-interpretive frame within which that empirical comparison acquires practical significance: the goal is not merely a better-fitting latent model, but a model whose structure maps onto actionable management categories.
