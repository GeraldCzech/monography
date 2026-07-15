---
title: "Chapter 10 — BEBA Empirical Evaluation: Model Competition and Structural Results"
status: draft
object_type: Chapter
layer: Empirical
chapter_number: 10
part: "III — Empirical Evidence"
claim_anchors:
  - C-BEBA-01
  - C-BEBA-02
  - C-BEBA-03
  - BT-000036
  - BT-000037
  - BE-000066
  - BD-BEH
  - BA-000080
  - BA-000081
  - BI-000001
  - BI-000002
pipeline_objects:
  - beba_cfa_full.rds
  - beba_invariance_configural.rds
  - beba_invariance_metric.rds
  - beba_invariance_scalar.rds
  - beba_sem_HA.rds
  - beba_sem_HB.rds
  - beba_sem_HC.rds
  - beba_sem_HD.rds
  - beba_mediation_boot5000.rds
  - beba_domir_INT.rds
  - beba_nca_INT.rds
  - beba_kano_asymmetry.rds
  - beba_segmented_SES.rds
  - beba_kmeans_EW.rds
  - beba_moderation_EW_cluster.rds
estimator: MLR
missing_data: FIML
theoretical_priors:
  BT_INT: {posterior: 0.892, n_evid: 31, source: "knowledge_graph_synthesis"}
  BI_ATT: {posterior: 0.921, n_evid: 16, source: "knowledge_graph_synthesis"}
  BD_BEH: {posterior: 0.611, n_evid: 6, source: "knowledge_graph_synthesis"}
  ATT_INT: {posterior: 0.873, n_evid: 29, source: "knowledge_graph_synthesis"}
  PBC_INT: {posterior: 0.802, n_evid: 16, source: "knowledge_graph_synthesis"}
predecessors:
  - Chapter 8 — Triple Replication of Nonprofit Brand Equity Models
  - Chapter 9 — Evidence-Based Charity Brand Dashboards
successors:
  - Chapter 11 — Discussion and Theoretical Integration
---

# Chapter 10 — BEBA Empirical Evaluation: Model Competition and Structural Results

---

## Scientific Question

Which of the four competing BEBA structural model architectures — H-A (full IBM/TPB mediation), H-B (partial mediation with direct brand equity effects), H-C (dimensional configural BEBA model), and H-D (Bourdieu-augmented field capital model) — best accounts for the relationships between nonprofit brand equity dimensions and donation behaviour in the Austrian donor sample, and what do the winning architecture's structural estimates imply for the theoretical propositions of the Brand-Enabled Behaviour Architecture?

---

## 10.1 Empirical Programme Overview

The empirical programme of this monograph moves in three stages. Chapters 8 and 9 constituted the first two stages: a systematic transportability test of existing nonprofit brand equity models under Austrian donor conditions, and a multi-lens analytical derivation of an evidence-based brand dashboard framework. The present chapter constitutes the third and culminating stage: the structural test of the Brand-Enabled Behaviour Architecture (BEBA) as a formally specified and empirically evaluated theoretical model. This stage is not merely additive to the preceding chapters. It is theoretically distinct from them. Whereas Chapters 8 and 9 asked what can be extracted from existing structural architectures — and what those architectures fail to explain — Chapter 10 asks whether the integrative BEBA architecture, constructed from first principles in Chapter 4, survives contact with Austrian donor data under the most demanding model-comparison conditions available within the SEM paradigm.

The scientific logic of this chapter is the **likelihood paradigm** (Edwards, 1972; Royall, 1997), as operationalised in the Bayesian model comparison framework introduced in Chapter 5.[^LP-000001] Rather than testing a null hypothesis against a single BEBA model, the chapter evaluates four formally specified competing architectures that represent distinct theoretical positions on how nonprofit brand equity translates into donation behaviour. These four models are not strawmen. Each embodies a theoretically defensible position that a reasoned advocate could hold on the basis of the existing literature:

**Model H-A — Full IBM/TPB Mediation:** All effects of brand equity dimensions on donation intention are fully mediated by the three Theory of Planned Behaviour / Integrated Behavioural Model constructs — Attitude toward the behaviour (ATT), Injunctive and Descriptive Subjective Norms (SN_inj, SN_des), and Perceived Behavioural Control (PBC). Brand equity operates as a distal cause; its effects on behaviour are entirely channelled through these proximal motivational constructs. This model instantiates the standard IBM/TPB architecture and represents the null hypothesis position that no structural novelty beyond the established behavioural models is required to explain donation behaviour.[^C-BEBA-01]

**Model H-B — Partial Mediation:** The IBM/TPB mediation pathways of H-A are retained, but direct paths from overall brand equity to Donation Intention are added. This represents the theoretically more permissive position that brand equity exerts both an indirect effect (via ATT/SN/PBC) and a direct residual effect on intention — a position supported by a substantial strand of the brand equity and charitable giving literature (Faircloth, Capella & Alford, 2001; Pope, Isely & Asamoa-Tutu, 2009; BI-000001).[^BI-000001] Model H-B constitutes the partial mediation baseline against which the dimensional specificity of H-C is evaluated.[^BI-000002]

**Model H-C — Dimensional Configural BEBA Model:** Each brand equity dimension is connected to a specific downstream target that its theoretical function predicts: Brand Awareness (BA) to Perceived Behavioural Control (via the recognition heuristic and salience pathway); Brand Image (BIM) to Attitude (via evaluative association transfer); Brand Trust (BT) to both PBC and Donation Intention directly (via uncertainty reduction and credence-quality certification); Brand Personality (BP) to Attitude contingent on donor empathy profile.[^BA-000080] This is the theoretically central model and the principal test of the BEBA framework. It represents C-BEBA-01 (brand equity as multi-channel behavioural architecture), C-BEBA-02 (trust as the primary mechanism under uncertainty), and C-BEBA-03 (dimensional specificity of brand equity pathways).[^C-BEBA-02]

**Model H-D — Bourdieu-Augmented:** An extension of H-C that adds a Symbolic Capital pathway and a field positioning moderator. Charitable giving, on this account, is not merely an expression of trust-based uncertainty reduction or evaluative preference — it also functions as a field-positioned act of social-image signalling within a donor's social network. Donors occupying positions in fields with high social visibility of giving (e.g., upper-middle-class professional networks with active charity culture) may donate in response to symbolic capital dynamics that operate independently of brand equity evaluations. Model H-D therefore adds: (a) a Social-Image Signalling construct (SIS) as a mediator between brand equity and intention; (b) a Field Uncertainty Index (FUI) as a moderator of the SIS→INT path; and (c) Symbolic Capital (SymCap) as an additional direct predictor of donation amount.[^C-BEBA-03]

### 10.1.1 Data Structure and Estimation Context

The Austrian donor survey (SoSci Survey 2026) employs a split design in which respondents in the FC_BO group evaluated nonprofit brands using Faircloth (2005) and Boenigk–Becker (2016) items, while respondents in the RO group evaluated the same brands using Romero et al. (2023) items. The BEBA structural model in Chapter 10 is estimated primarily on the FC_BO subsample, which contains the Brand Trust and Brand Commitment items central to the BEBA architecture. The RO subsample provides a replication check using Brand Reputation as the trust-adjacent construct.

Within-respondent paired observations (each participant evaluated two nonprofit organisations) introduce a nested data structure. Non-independence of observations within respondents is addressed through the MLR estimator's robust sandwich standard errors, which account for clustering without requiring explicit multilevel specification. Where organisation-level moderators are entered (e.g., FUI in H-D), a two-level random-intercept model is estimated as a robustness check.

The full working sample for the BEBA analyses consists of: FC_BO subsample n = [PIPELINE: beba_cfa_full → N_FCBO] organisation-level observations from [PIPELINE: beba_cfa_full → n_respondents_FCBO] respondents; RO subsample n = [PIPELINE: beba_cfa_full → N_RO] organisation-level observations from [PIPELINE: beba_cfa_full → n_respondents_RO] respondents. After FIML-based handling of item-level missingness, the effective analysis sample is [PIPELINE: beba_cfa_full → N_effective_FCBO] (FC_BO) and [PIPELINE: beba_cfa_full → N_effective_RO] (RO).

### 10.1.2 Model Comparison Strategy

The four models are compared using three complementary inferential strategies, as specified in Chapter 5:

**Bayesian model comparison via Bayes Factors** (Kass & Raftery, 1995): BF values are computed from marginal likelihood approximations (BIC-based conversion: BF ≈ exp((BIC_null − BIC_alt)/2)). Kass and Raftery's (1995) evidence classification is applied: BF < 3.2 constitutes weak evidence, 3.2–10 positive evidence, 10–100 strong evidence, and > 100 very strong evidence. The reference model is H-A in all pairwise comparisons; H-C is additionally compared directly to H-D.

**Fit index differences** (ΔCombined): ΔCFI ≥ −.010, ΔRMSEA ≤ +.015, and ΔSRMR ≤ +.030 constitute thresholds below which a more parsimonious model is not statistically preferred in fit-index terms (Cheung & Rensvold, 2002; Chen, 2007). Where nested model comparisons are applicable, a corrected likelihood ratio chi-square difference test (Satorra & Bentler, 2001) is conducted.

**AIC/BIC differences**: ΔAIC < 2 constitutes negligible evidence; 2–7 positive evidence; > 10 decisive evidence for the model with the lower information criterion (Burnham & Anderson, 2002). Because BIC penalises model complexity more severely than AIC, the two may produce different orderings when model complexity differences are substantial (as is the case between H-C and H-D).

All four models are estimated using Maximum Likelihood with Robust standard errors (MLR estimator in R lavaan; Rosseel, 2012) on the full Austrian donor dataset. Full Information Maximum Likelihood (FIML) is used for missing data. Estimation is conducted separately for the FC_BO and RO subsamples where construct availability differs, and results are compared for convergence.

A note on terminology: throughout this chapter, the terms "model H-A", "model H-B", "model H-C", and "model H-D" are used consistently to designate the four structural model architectures. These labels correspond to the hypothesis designations established in Chapter 4. The use of letter-coded hypothesis labels, rather than descriptive names, is intentional: it resists the rhetorical tendency to pre-identify one model as "the BEBA model" before the empirical comparison has been conducted. H-C happens to be the theoretically preferred architecture on the basis of the evidence synthesis in Chapters 2–4, but it earns that status empirically rather than by definitional fiat.

---

## 10.2 Measurement Model Confirmation

The structural tests in this chapter presuppose that the BEBA constructs have been measured validly and reliably. This section briefly confirms that presupposition by summarising the CFA results from Chapter 8 and the additional measurement invariance tests conducted specifically for the BEBA item set.

### 10.2.1 CFA Results: Triple Replication Foundation

Chapter 8 established, through triple replication across the Faircloth (2005), Boenigk and Becker (2016), and Romero et al. (2023) model architectures, that nonprofit brand equity constructs can be recovered with adequate psychometric quality in the Austrian donor sample. The CFA results relevant to Chapter 10 are those from the Faircloth and Boenigk-Becker subsets, which together constitute the FC_BO dataset from which the BEBA structural models are estimated.

Key CFA results from Chapter 8 (all as pipeline confirmations, not re-estimated here):

- **Faircloth CFA global fit**: CFI = [PIPELINE: cross_cfa_Faircloth → CFI]; RMSEA = [PIPELINE: cross_cfa_Faircloth → RMSEA]; SRMR = [PIPELINE: cross_cfa_Faircloth → SRMR]
- **Boenigk–Becker CFA global fit**: CFI = [PIPELINE: cross_cfa_Boenigk → CFI]; RMSEA = [PIPELINE: cross_cfa_Boenigk → RMSEA]; SRMR = [PIPELINE: cross_cfa_Boenigk → SRMR]
- **Composite reliability** (ω): all factors ω ≥ [PIPELINE: cross_cfa_Faircloth → omega_min]
- **Average Variance Extracted**: all factors AVE ≥ [PIPELINE: cross_cfa_Faircloth → AVE_min]
- **HTMT discriminant validity**: all pairwise HTMT < [PIPELINE: cross_cfa_Faircloth → HTMT_max] (strict threshold .85 applied)

The BEBA model requires in addition that the IBM/TPB constructs — ATT, SN_inj, SN_des, PBC, and Donation Intention (INT) — meet the same measurement standards. These constructs were assessed with items adapted from validated German-language TPB scales (Ajzen, 2002; Francis et al., 2004; Hagger et al., 2022 meta-analytic item pool) and administered in both the FC_BO and RO subsets.

BEBA-specific CFA global fit: CFI = [PIPELINE: beba_cfa_full → CFI]; RMSEA = [PIPELINE: beba_cfa_full → RMSEA]; SRMR = [PIPELINE: beba_cfa_full → SRMR]. Item-level standardised loadings for ATT, SN_inj, SN_des, PBC, and INT: all ≥ [PIPELINE: beba_cfa_full → min_loading], n.s. cross-loadings. The formative outer model for overall Brand Equity (BE_overall), specified as a weighted composite of the four dimensional scores (BA, BIM, BT, BP) with weights derived from the dominance analysis in Chapter 9, is confirmed to produce a valid reflective-formative second-order specification.[^BE-000066]

### 10.2.2 Measurement Invariance Across Subsamples

Comparison of structural results across the FC_BO and RO subsamples, and across donor segments in Section 10.11, requires established measurement invariance. The standard invariance testing sequence (Vandenberg & Lance, 2000; Putnick & Bornstein, 2016) was applied:

| Invariance level | ΔCFI | ΔRMSEA | Verdict |
|---|---|---|---|
| Configural | — | — | [PIPELINE: beba_invariance_configural → verdict] |
| Metric (equal loadings) | [PIPELINE: beba_invariance_metric → ΔCFI] | [PIPELINE: beba_invariance_metric → ΔRMSEA] | [PIPELINE: beba_invariance_metric → verdict] |
| Scalar (equal intercepts) | [PIPELINE: beba_invariance_scalar → ΔCFI] | [PIPELINE: beba_invariance_scalar → ΔRMSEA] | [PIPELINE: beba_invariance_scalar → verdict] |

Where scalar invariance is not achieved for all items, partial scalar invariance is evaluated using the Byrne, Shavelson and Muthén (1989) procedure: at least two invariant items per factor are required for latent mean comparisons to proceed. Items with non-invariant intercepts are identified and their substantive interpretation is noted.[^NB-000103]

### 10.2.3 Convergent and Discriminant Validity Summary

The pattern of AVE, CR, and HTMT estimates across the BEBA constructs is summarised in the following table. All entries are pipeline placeholders to be populated from `beba_cfa_full.rds`:

| Construct | CR | AVE | Max HTMT (with) |
|---|---|---|---|
| Brand Awareness (BA) | [PIPELINE: beba_cfa_full → CR_BA] | [PIPELINE: beba_cfa_full → AVE_BA] | [PIPELINE: beba_cfa_full → HTMT_BA_max] (with [PIPELINE: beba_cfa_full → HTMT_BA_partner]) |
| Brand Image (BIM) | [PIPELINE: beba_cfa_full → CR_BIM] | [PIPELINE: beba_cfa_full → AVE_BIM] | [PIPELINE: beba_cfa_full → HTMT_BIM_max] |
| Brand Trust (BT) | [PIPELINE: beba_cfa_full → CR_BT] | [PIPELINE: beba_cfa_full → AVE_BT] | [PIPELINE: beba_cfa_full → HTMT_BT_max] |
| Brand Personality (BP) | [PIPELINE: beba_cfa_full → CR_BP] | [PIPELINE: beba_cfa_full → AVE_BP] | [PIPELINE: beba_cfa_full → HTMT_BP_max] |
| Attitude (ATT) | [PIPELINE: beba_cfa_full → CR_ATT] | [PIPELINE: beba_cfa_full → AVE_ATT] | [PIPELINE: beba_cfa_full → HTMT_ATT_max] |
| Subj. Norms-inj (SN_inj) | [PIPELINE: beba_cfa_full → CR_SNinj] | [PIPELINE: beba_cfa_full → AVE_SNinj] | [PIPELINE: beba_cfa_full → HTMT_SNinj_max] |
| Subj. Norms-des (SN_des) | [PIPELINE: beba_cfa_full → CR_SNdes] | [PIPELINE: beba_cfa_full → AVE_SNdes] | [PIPELINE: beba_cfa_full → HTMT_SNdes_max] |
| Perc. Behav. Control (PBC) | [PIPELINE: beba_cfa_full → CR_PBC] | [PIPELINE: beba_cfa_full → AVE_PBC] | [PIPELINE: beba_cfa_full → HTMT_PBC_max] |
| Donation Intention (INT) | [PIPELINE: beba_cfa_full → CR_INT] | [PIPELINE: beba_cfa_full → AVE_INT] | [PIPELINE: beba_cfa_full → HTMT_INT_max] |

---

## 10.3 Structural Model H-A: Full IBM/TPB Mediation

### 10.3.1 Specification

Model H-A implements the theoretical position that all brand equity effects on donation intention are fully channelled through the three proximal motivational constructs of the Theory of Planned Behaviour / Integrated Behavioural Model. The structural specification is:

1. **Brand equity → ATT/SN/PBC layer**: Overall Brand Equity (BE_overall, formative composite) predicts ATT, SN_inj, SN_des, and PBC. Brand equity is conceived as an undifferentiated global construct at this stage; dimensional decomposition is reserved for H-C.
2. **ATT/SN/PBC → INT**: The three proximal constructs predict Donation Intention.
3. **INT → BEH**: Donation Intention predicts behavioural outcomes (donor status binary, donation frequency log-transformed, donation amount log-transformed), consistent with the IBM's distinction between intention and behavioural enactment.
4. **No direct path BE_overall → INT**: The full mediation constraint is the defining restriction that distinguishes H-A from H-B.

The model additionally includes covariates: Socioeconomic Status (SES_z, standardised composite) as a covariate on INT and BEH; Habit (HAB) and Salience (SAL) as additional IBM enactment predictors of BEH where items are available.

### 10.3.2 Estimated Path Coefficients

All structural path estimates below are `[PIPELINE: ...]` placeholders to be populated from `beba_sem_HA.rds`:

| Path | β (standardised) | SE | p |
|---|---|---|---|
| BE_overall → ATT | [PIPELINE: beba_sem_HA → path_BE_ATT] | [PIPELINE: beba_sem_HA → se_BE_ATT] | [PIPELINE: beba_sem_HA → p_BE_ATT] |
| BE_overall → SN_inj | [PIPELINE: beba_sem_HA → path_BE_SNinj] | [PIPELINE: beba_sem_HA → se_BE_SNinj] | [PIPELINE: beba_sem_HA → p_BE_SNinj] |
| BE_overall → SN_des | [PIPELINE: beba_sem_HA → path_BE_SNdes] | [PIPELINE: beba_sem_HA → se_BE_SNdes] | [PIPELINE: beba_sem_HA → p_BE_SNdes] |
| BE_overall → PBC | [PIPELINE: beba_sem_HA → path_BE_PBC] | [PIPELINE: beba_sem_HA → se_BE_PBC] | [PIPELINE: beba_sem_HA → p_BE_PBC] |
| ATT → INT | [PIPELINE: beba_sem_HA → path_ATT_INT] | [PIPELINE: beba_sem_HA → se_ATT_INT] | [PIPELINE: beba_sem_HA → p_ATT_INT] |
| SN_inj → INT | [PIPELINE: beba_sem_HA → path_SNinj_INT] | [PIPELINE: beba_sem_HA → se_SNinj_INT] | [PIPELINE: beba_sem_HA → p_SNinj_INT] |
| SN_des → INT | [PIPELINE: beba_sem_HA → path_SNdes_INT] | [PIPELINE: beba_sem_HA → se_SNdes_INT] | [PIPELINE: beba_sem_HA → p_SNdes_INT] |
| PBC → INT | [PIPELINE: beba_sem_HA → path_PBC_INT] | [PIPELINE: beba_sem_HA → se_PBC_INT] | [PIPELINE: beba_sem_HA → p_PBC_INT] |
| INT → BEH (binary) | [PIPELINE: beba_sem_HA → path_INT_BEH_bin] | [PIPELINE: beba_sem_HA → se_INT_BEH_bin] | [PIPELINE: beba_sem_HA → p_INT_BEH_bin] |
| INT → BEH (freq) | [PIPELINE: beba_sem_HA → path_INT_BEH_freq] | [PIPELINE: beba_sem_HA → se_INT_BEH_freq] | [PIPELINE: beba_sem_HA → p_INT_BEH_freq] |
| HAB → BEH | [PIPELINE: beba_sem_HA → path_HAB_BEH] | [PIPELINE: beba_sem_HA → se_HAB_BEH] | [PIPELINE: beba_sem_HA → p_HAB_BEH] |

### 10.3.3 Fit Indices

Global fit for H-A: χ²(df) = [PIPELINE: beba_sem_HA → chi2(df)]; CFI = [PIPELINE: beba_sem_HA → CFI]; TLI = [PIPELINE: beba_sem_HA → TLI]; RMSEA = [PIPELINE: beba_sem_HA → RMSEA] (90% CI: [PIPELINE: beba_sem_HA → RMSEA_CI]); SRMR = [PIPELINE: beba_sem_HA → SRMR]; AIC = [PIPELINE: beba_sem_HA → AIC]; BIC = [PIPELINE: beba_sem_HA → BIC].

### 10.3.4 Interpretation

Model H-A represents the most theoretically conservative position: nonprofit brand equity matters, but it matters exclusively through the standard TPB/IBM pathway. The critical diagnostic for H-A is the magnitude and significance of the BE_overall → ATT and BE_overall → PBC paths. If these paths are strong and the overall model fit is adequate, the full mediation hypothesis cannot be rejected on statistical grounds alone. However, the model makes a strong theoretical claim — that brand equity has zero direct effect on intention once ATT, SN, and PBC are entered — that is theoretically implausible in the credence-good setting described in Chapters 2 and 4. Under conditions of high uncertainty, brand equity may operate as a direct cognitive shortcut to intention formation that bypasses deliberative evaluation (cf. Kahneman, 2011; Gigerenzer & Brighton, 2009). This expectation motivates the H-B comparison.

The theoretical priors from the knowledge graph synthesis — ATT_INT posterior = 0.873 (n = 29 studies), PBC_INT posterior = 0.802 (n = 16 studies) — function as informative Bayesian priors on the plausibility of the H-A path structure. These are not results from the Austrian survey; they are the meta-analytic synthesis values that informed model construction. Whether the Austrian sample replicates or departs from these priors is an empirical question answered by the pipeline estimates above.[^LP-000001]

---

## 10.4 Structural Model H-B: Partial Mediation

### 10.4.1 Specification

Model H-B relaxes the full mediation constraint of H-A by adding a direct path from overall Brand Equity (BE_overall) to Donation Intention (INT). All other paths are identical to H-A. The single structural addition — one free parameter — makes H-B nested within the same model family, enabling a formal chi-square difference test.

The theoretical motivation is clear from the prior literature: a consistent finding across multiple donor behaviour studies is that brand equity or brand attitude exerts a direct effect on behavioural intention beyond what is explained by ATT, SN, and PBC — suggesting that global brand evaluations operate as heuristic intention determinants that are not fully decomposed into deliberative attitude and normative representations (Faircloth et al., 2001; Pope et al., 2009; Sargeant & Lee, 2004).[^BI-000001] The partial mediation model thus embodies the hypothesis that brand equity functions both as a signal that feeds into deliberative constructs (indirect path) and as a fast, System 1 heuristic that bypasses them (direct path).[^BI-000002]

### 10.4.2 Estimated Paths and Chi-Square Difference Test

| Path | β | SE | p |
|---|---|---|---|
| BE_overall → INT (direct) | [PIPELINE: beba_sem_HB → path_BE_INT] | [PIPELINE: beba_sem_HB → se_BE_INT] | [PIPELINE: beba_sem_HB → p_BE_INT] |
| (All H-A paths retained — see above) | | | |

Chi-square difference test (Satorra–Bentler corrected) H-A vs. H-B: Δχ²(1) = [PIPELINE: beba_sem_HB → delta_chi2_vs_HA]; p = [PIPELINE: beba_sem_HB → p_delta_chi2]. ΔCFI = [PIPELINE: beba_sem_HB → ΔCFI_vs_HA]; ΔRMSEA = [PIPELINE: beba_sem_HB → ΔRMSEA_vs_HA].

Global fit for H-B: CFI = [PIPELINE: beba_sem_HB → CFI]; RMSEA = [PIPELINE: beba_sem_HB → RMSEA]; AIC = [PIPELINE: beba_sem_HB → AIC]; BIC = [PIPELINE: beba_sem_HB → BIC].

### 10.4.3 Interpretation

Based on the substantial evidence base for partial mediation in the prior literature — thirty or more studies reviewed in Chapter 7 find residual direct effects of brand evaluations on intention once TPB constructs are controlled — the prior theoretical expectation is that H-B will show statistically significantly better fit than H-A. The BE_overall → INT direct path is expected to be positive, moderate in size, and statistically significant. Should the pipeline estimates confirm this, H-A is rejected in favour of H-B as the partial mediation baseline.

The key question then becomes whether the *undifferentiated* partial mediation of H-B is further improved by the *dimensionally specific* architecture of H-C, which makes theoretically motivated rather than generic direct-path claims. The BE_overall → INT path in H-B is a theoretically agnostic specification: it asserts that *something* about overall brand equity reaches intention directly, without specifying the causal mechanism or the dimensional locus of that effect. This agnosticism is empirically inefficient: if the direct effect of Brand Equity on Intention is driven primarily by Brand Trust — which, as a credence-quality signal, operates through a fast-heuristic mechanism — then the H-B specification conflates the Trust-specific direct path with smaller and theoretically distinct contributions from Image, Personality, and Awareness. H-C recovers the dimensional structure of this direct effect and thereby provides both a more precise parameter estimate and a more interpretable theoretical account.

The comparison of H-B and H-C is therefore not merely a fit-index contest. It is a test of whether theory-driven dimensional routing adds structural information to the data. If it does, the dimensionally informed model is to be preferred on both explanatory and predictive grounds — even if the absolute fit improvement is moderate — because the theoretical interpretation is richer and the management implications are clearer.

---

## 10.5 Structural Model H-C: Configural BEBA Model (Dimensional)

### 10.5.1 Theoretical Architecture

Model H-C is the theoretically central specification of the Brand-Enabled Behaviour Architecture. It abandons the aggregated Brand Equity composite (BE_overall) used in H-A and H-B and instead connects each brand equity dimension to the specific downstream construct that its theoretical function predicts. This dimensional specificity is the defining structural claim of BEBA: that nonprofit brand equity is not a unitary influence on behaviour but a multi-channel architecture in which different brand dimensions activate different cognitive and motivational pathways.[^C-BEBA-01]

The dimensional routing logic is derived from the theoretical synthesis in Chapter 4 and the knowledge graph posterior estimates from the literature pipeline. These posterior values — BT_INT = 0.892 (31 studies), BI_ATT = 0.921 (16 studies), BD_BEH = 0.611 (6 studies) — are *theoretical priors* that informed the model specification: they represent the meta-analytic weight of prior evidence for each path and anchor the direction and approximate magnitude expected in the Austrian sample. They are not the results of the present Austrian survey and must not be read as such. The Austrian survey estimates are reported as pipeline placeholders below.

The four dimensional pathways are:

**Brand Awareness (BA) → PBC**: The recognition heuristic (Goldstein & Gigerenzer, 2002) predicts that awareness of a charity functions primarily as a signal of organisational legitimacy and epistemic accessibility, reducing the cognitive cost of the decision and thereby elevating Perceived Behavioural Control — the donor's sense that they know how and where to donate to a credible organisation.[^BA-000080] The BA → PBC pathway represents uncertainty reduction through familiarity, not through evaluative processing.

**Brand Image (BIM) → ATT**: Brand Image, conceived as the stored set of evaluative associations (positive mission alignment, organisational competence, benefit distinctiveness), predicts Attitude toward donating directly. This pathway aligns with the classical conditioning account of attitude formation from brand associations (Keller, 1993; De Pelsmacker, Geuens & Van den Bergh, 2013) and with the meta-analytic evidence for BI_ATT = 0.921 in the knowledge graph synthesis.[^BA-000081]

**Brand Trust (BT) → PBC and INT (direct)**: Brand Trust is theoretically the central mechanism of BEBA.[^BT-000036] Under conditions of credence-good uncertainty — where donors cannot observe organisational impact before, during, or after the gift — trust functions as a governance substitute (Williamson, 1993; Nooteboom, 2002). It reduces perceived risk, elevates the donor's sense that the gift will be used as intended (thus raising PBC), and directly elevates the motivational readiness to donate (INT) through a fast-trust heuristic that operates prior to full deliberative evaluation. The dual BT pathway — BT → PBC and BT → INT (direct) — is the architectural core of BEBA and represents the integration of the trust-as-uncertainty-reduction mechanism with the IBM framework.[^BT-000037]

**Brand Personality (BP) → ATT (contingent)**: Brand Personality, understood as the attribution of human character traits to a nonprofit (Aaker, 1997), elevates Attitude primarily through a self-congruity mechanism: donors whose self-concept aligns with the personality attributed to the charity form more positive attitudes toward donating. This path is expected to be moderated by donor empathy profile (Section 10.11): donors with high empathy for the charity's beneficiary group show stronger BP → ATT effects. The path is therefore included as a main-effect parameter in H-C with the expectation that its magnitude is smaller and more variable than the BIM → ATT and BT → PBC paths.[^BE-000066]

The theoretically expected pattern of path strengths in H-C can be stated in advance, again as a theoretical prior rather than as a result. The knowledge graph posteriors provide an approximate ordering: BIM → ATT is expected to carry the highest standardised coefficient among the brand-equity-to-mediator paths (posterior BI_ATT = 0.921 from 16 studies); BT → INT (direct) is expected to be the strongest brand-equity-to-intention path (posterior BT_INT = 0.892 from 31 studies); BT → PBC is expected to be substantial but smaller than BT → INT (reflecting the two-step uncertainty reduction mechanism where trust first elevates control perceptions, which then feed intention); BA → PBC is expected to be moderate (posterior BA_INT = 0.736, 21 studies, partly decomposed through the PBC step); and BP → ATT is expected to be the weakest dimensional path given the smallest evidence base (7 studies) and the contingency of personality effects on donor-organisation congruence.[^BT-000037]

These prior expectations do not bind the analysis. They are stated explicitly so that departures from the prior — a weaker-than-expected BT → INT path, an unexpectedly strong BA → ATT path, a suppressed BP effect — can be identified as theoretically informative rather than merely reported as unexplained empirical variation.

### 10.5.2 Full Structural Specification and Path Estimates

| Path | Theory | β | SE | p |
|---|---|---|---|---|
| BA → PBC | Recognition heuristic → perceived ease of giving | [PIPELINE: beba_sem_HC → path_BA_PBC] | [PIPELINE: beba_sem_HC → se_BA_PBC] | [PIPELINE: beba_sem_HC → p_BA_PBC] |
| BIM → ATT | Evaluative association transfer | [PIPELINE: beba_sem_HC → path_BIM_ATT] | [PIPELINE: beba_sem_HC → se_BIM_ATT] | [PIPELINE: beba_sem_HC → p_BIM_ATT] |
| BT → PBC | Trust reduces perceived risk | [PIPELINE: beba_sem_HC → path_BT_PBC] | [PIPELINE: beba_sem_HC → se_BT_PBC] | [PIPELINE: beba_sem_HC → p_BT_PBC] |
| BT → INT | Fast-trust heuristic, direct | [PIPELINE: beba_sem_HC → path_BT_INT] | [PIPELINE: beba_sem_HC → se_BT_INT] | [PIPELINE: beba_sem_HC → p_BT_INT] |
| BP → ATT | Self-congruity, affective alignment | [PIPELINE: beba_sem_HC → path_BP_ATT] | [PIPELINE: beba_sem_HC → se_BP_ATT] | [PIPELINE: beba_sem_HC → p_BP_ATT] |
| ATT → INT | TPB core path | [PIPELINE: beba_sem_HC → path_ATT_INT] | [PIPELINE: beba_sem_HC → se_ATT_INT] | [PIPELINE: beba_sem_HC → p_ATT_INT] |
| SN_inj → INT | Injunctive social norm | [PIPELINE: beba_sem_HC → path_SNinj_INT] | [PIPELINE: beba_sem_HC → se_SNinj_INT] | [PIPELINE: beba_sem_HC → p_SNinj_INT] |
| SN_des → INT | Descriptive social norm | [PIPELINE: beba_sem_HC → path_SNdes_INT] | [PIPELINE: beba_sem_HC → se_SNdes_INT] | [PIPELINE: beba_sem_HC → p_SNdes_INT] |
| PBC → INT | Control facilitates intention | [PIPELINE: beba_sem_HC → path_PBC_INT] | [PIPELINE: beba_sem_HC → se_PBC_INT] | [PIPELINE: beba_sem_HC → p_PBC_INT] |
| INT → BEH (binary) | Intention-enactment | [PIPELINE: beba_sem_HC → path_INT_BEH_bin] | [PIPELINE: beba_sem_HC → se_INT_BEH_bin] | [PIPELINE: beba_sem_HC → p_INT_BEH_bin] |
| INT → BEH (freq) | Intention-enactment | [PIPELINE: beba_sem_HC → path_INT_BEH_freq] | [PIPELINE: beba_sem_HC → se_INT_BEH_freq] | [PIPELINE: beba_sem_HC → p_INT_BEH_freq] |
| HAB → BEH | Habit, routinised giving | [PIPELINE: beba_sem_HC → path_HAB_BEH] | [PIPELINE: beba_sem_HC → se_HAB_BEH] | [PIPELINE: beba_sem_HC → p_HAB_BEH] |

**Explained variance estimates** (R² for endogenous constructs):

| Endogenous construct | R² |
|---|---|
| Attitude (ATT) | [PIPELINE: beba_sem_HC → R2_ATT] |
| Subj. Norms-inj (SN_inj) | [PIPELINE: beba_sem_HC → R2_SNinj] |
| Subj. Norms-des (SN_des) | [PIPELINE: beba_sem_HC → R2_SNdes] |
| Perc. Behav. Control (PBC) | [PIPELINE: beba_sem_HC → R2_PBC] |
| Donation Intention (INT) | [PIPELINE: beba_sem_HC → R2_INT] |
| BEH (binary, donor status) | [PIPELINE: beba_sem_HC → R2_BEH_bin] |
| BEH (frequency log) | [PIPELINE: beba_sem_HC → R2_BEH_freq] |

### 10.5.3 Fit Indices

Global fit for H-C: χ²(df) = [PIPELINE: beba_sem_HC → chi2(df)]; CFI = [PIPELINE: beba_sem_HC → CFI]; TLI = [PIPELINE: beba_sem_HC → TLI]; RMSEA = [PIPELINE: beba_sem_HC → RMSEA] (90% CI: [PIPELINE: beba_sem_HC → RMSEA_CI]); SRMR = [PIPELINE: beba_sem_HC → SRMR]; AIC = [PIPELINE: beba_sem_HC → AIC]; BIC = [PIPELINE: beba_sem_HC → BIC].

### 10.5.4 Interpretation

Model H-C is theoretically the most informative of the four competing architectures. Its dimensional routing makes the theoretical mechanism explicit and testable: if H-C fits better than H-B, it means that *specifying which brand dimension activates which motivational channel* carries empirical information — that the Austrian donor data contain structural signal that the aggregated model obscures. The pattern of estimated dimensional path strengths, when available from the pipeline, will also carry substantive theoretical implications: a strong BT → INT direct path, relative to the BT → PBC pathway, would confirm the fast-trust mechanism over a purely deliberative trust channel; a weaker BP → ATT path relative to BIM → ATT would confirm that symbolic-affective personalisation is less behaviourally potent than evaluative image associations in the Austrian nonprofit context.

---

## 10.6 Structural Model H-D: Bourdieu-Augmented

### 10.6.1 Theoretical Extension

Model H-D extends H-C with a sociological mechanism derived from Bourdieu's (1984, 1986) theory of capital and field positioning. The theoretical claim is that charitable giving in socially visible contexts is not merely a product of trust-based uncertainty reduction and evaluative preference — it is also an act of symbolic capital accumulation and social distinction. Donors embedded in social fields where charitable giving carries high symbolic value (professional networks, high-SES peer environments, institutional community contexts) may make giving decisions that are partly governed by the anticipated social-image signal of the gift, independent of their brand equity evaluations.

This theoretical extension is not a rejection of H-C but an augmentation that adds a sociological layer of explanation. Two additional constructs are introduced:

**Social-Image Signalling (SIS)**: The donor's perception that donating to a specific nonprofit will enhance their social standing or signal desirable values to relevant others. SIS is measured by items adapted from the conspicuous charity literature (Glazer & Konrad, 1996; Harbaugh, 1998; Ariely, Bracha & Meier, 2009). SIS is positioned as a partial mediator of the BT → INT and BIM → ATT pathways.

**Field Uncertainty Index (FUI)**: An organisational- and community-level operationalisation of the degree to which the donor's social field places charitable giving under normative scrutiny. FUI is constructed from items measuring perceived giving norms among the donor's social reference group, the visibility of giving behaviour in the donor's social network, and the degree to which giving is perceived as socially evaluated. FUI moderates the SIS → INT path: donors in high-FUI contexts should show stronger SIS effects.

**Symbolic Capital pathway**: A direct path from a Symbolic Capital composite (SymCap) to donation amount, testing whether field-positioned symbolic capital accumulation predicts giving magnitude beyond what brand equity and intention explain.

### 10.6.2 Estimated Paths

| Path | β | SE | p |
|---|---|---|---|
| BT → SIS | [PIPELINE: beba_sem_HD → path_BT_SIS] | [PIPELINE: beba_sem_HD → se_BT_SIS] | [PIPELINE: beba_sem_HD → p_BT_SIS] |
| BIM → SIS | [PIPELINE: beba_sem_HD → path_BIM_SIS] | [PIPELINE: beba_sem_HD → se_BIM_SIS] | [PIPELINE: beba_sem_HD → p_BIM_SIS] |
| SIS → INT | [PIPELINE: beba_sem_HD → path_SIS_INT] | [PIPELINE: beba_sem_HD → se_SIS_INT] | [PIPELINE: beba_sem_HD → p_SIS_INT] |
| SIS × FUI → INT | [PIPELINE: beba_sem_HD → path_SISxFUI_INT] | [PIPELINE: beba_sem_HD → se_SISxFUI_INT] | [PIPELINE: beba_sem_HD → p_SISxFUI_INT] |
| SymCap → BEH (amount) | [PIPELINE: beba_sem_HD → path_SymCap_BEH_amt] | [PIPELINE: beba_sem_HD → se_SymCap_BEH_amt] | [PIPELINE: beba_sem_HD → p_SymCap_BEH_amt] |
| (All H-C paths retained) | | | |

Global fit for H-D: CFI = [PIPELINE: beba_sem_HD → CFI]; RMSEA = [PIPELINE: beba_sem_HD → RMSEA]; AIC = [PIPELINE: beba_sem_HD → AIC]; BIC = [PIPELINE: beba_sem_HD → BIC].

### 10.6.3 Interpretation

The Bourdieu-augmented model introduces both theoretical richness and empirical cost: additional latent variables, additional paths, and additional measurement complexity. The critical question for the model competition is not whether H-D explains *some* additional variance — with more free parameters, it almost certainly will — but whether it explains *meaningfully more* variance given its additional complexity, as quantified through BIC and Bayes Factors that penalise over-parameterisation. The prior theoretical expectation, based on the Austrian donation context, is that symbolic capital dynamics are present but secondary: Austrian charitable giving is characterised by relatively private, institutionally regularised giving behaviour rather than the highly visible conspicuous philanthropy documented in Harbaugh (1998) and Ariely et al. (2009) for North American contexts. H-D is therefore retained as a theoretical competitor rather than predicted to outperform H-C.[^C-BEBA-03]

---

## 10.7 Model Competition Results

### 10.7.1 Fit Index Comparison

The following table presents the comparative fit of all four models. All values are pipeline placeholders:

| Model | χ² (df) | CFI | RMSEA | SRMR | AIC | BIC |
|---|---|---|---|---|---|---|
| H-A: Full mediation | [PIPELINE: beba_sem_HA → chi2(df)] | [PIPELINE: beba_sem_HA → CFI] | [PIPELINE: beba_sem_HA → RMSEA] | [PIPELINE: beba_sem_HA → SRMR] | [PIPELINE: beba_sem_HA → AIC] | [PIPELINE: beba_sem_HA → BIC] |
| H-B: Partial mediation | [PIPELINE: beba_sem_HB → chi2(df)] | [PIPELINE: beba_sem_HB → CFI] | [PIPELINE: beba_sem_HB → RMSEA] | [PIPELINE: beba_sem_HB → SRMR] | [PIPELINE: beba_sem_HB → AIC] | [PIPELINE: beba_sem_HB → BIC] |
| H-C: Configural BEBA | [PIPELINE: beba_sem_HC → chi2(df)] | [PIPELINE: beba_sem_HC → CFI] | [PIPELINE: beba_sem_HC → RMSEA] | [PIPELINE: beba_sem_HC → SRMR] | [PIPELINE: beba_sem_HC → AIC] | [PIPELINE: beba_sem_HC → BIC] |
| H-D: Bourdieu-augmented | [PIPELINE: beba_sem_HD → chi2(df)] | [PIPELINE: beba_sem_HD → CFI] | [PIPELINE: beba_sem_HD → RMSEA] | [PIPELINE: beba_sem_HD → SRMR] | [PIPELINE: beba_sem_HD → AIC] | [PIPELINE: beba_sem_HD → BIC] |

### 10.7.2 Bayes Factor Evidence Classification

Pairwise Bayes Factors are computed from the BIC values using the approximation BF ≈ exp((BIC_H0 − BIC_H1)/2), where H1 is the model being evaluated and H0 is the reference (H-A). The Kass and Raftery (1995) evidence scale is applied.

| Comparison | ΔBIC | BF (approx.) | Evidence classification |
|---|---|---|---|
| H-B vs. H-A | [PIPELINE: beba_sem_HB → ΔBIC_vs_HA] | [PIPELINE: beba_sem_HB → BF_vs_HA] | [PIPELINE: beba_sem_HB → BF_class_vs_HA] |
| H-C vs. H-A | [PIPELINE: beba_sem_HC → ΔBIC_vs_HA] | [PIPELINE: beba_sem_HC → BF_vs_HA] | [PIPELINE: beba_sem_HC → BF_class_vs_HA] |
| H-D vs. H-A | [PIPELINE: beba_sem_HD → ΔBIC_vs_HA] | [PIPELINE: beba_sem_HD → BF_vs_HA] | [PIPELINE: beba_sem_HD → BF_class_vs_HA] |
| H-C vs. H-B | [PIPELINE: beba_sem_HC → ΔBIC_vs_HB] | [PIPELINE: beba_sem_HC → BF_vs_HB] | [PIPELINE: beba_sem_HC → BF_class_vs_HB] |
| H-C vs. H-D | [PIPELINE: beba_sem_HC → ΔBIC_vs_HD] | [PIPELINE: beba_sem_HC → BF_vs_HD] | [PIPELINE: beba_sem_HC → BF_class_vs_HD] |

### 10.7.3 AIC Comparison

AIC differences across the four models are summarised for comparison. Note that AIC and BIC may disagree in ordering where H-D is concerned: H-D contains substantially more free parameters, and BIC's stronger penalty for complexity may therefore rank H-D below H-C even if AIC ranks them closely.

| Model pair | ΔAIC | Evidence strength (Burnham & Anderson) |
|---|---|---|
| H-B vs. H-A | [PIPELINE: beba_sem_HB → ΔAIC_vs_HA] | [PIPELINE: beba_sem_HB → AIC_evidence_vs_HA] |
| H-C vs. H-A | [PIPELINE: beba_sem_HC → ΔAIC_vs_HA] | [PIPELINE: beba_sem_HC → AIC_evidence_vs_HA] |
| H-C vs. H-B | [PIPELINE: beba_sem_HC → ΔAIC_vs_HB] | [PIPELINE: beba_sem_HC → AIC_evidence_vs_HB] |
| H-C vs. H-D | [PIPELINE: beba_sem_HC → ΔAIC_vs_HD] | [PIPELINE: beba_sem_HC → AIC_evidence_vs_HD] |

Where AIC and BIC disagree in their ordering of H-C and H-D, the BIC is taken as the primary criterion, in line with the model comparison protocol specified in Chapter 5. BIC's stronger complexity penalty is appropriate given that H-D introduces conceptually novel latent constructs (SIS, FUI, SymCap) whose theoretical justification in the Austrian donor context is exploratory rather than confirmatory.

### 10.7.4 Winner Model Identification

Based on the theoretical priors from the knowledge graph, the prior expectation is that H-C — the dimensional configural BEBA model — will emerge as the best-supported architecture. The theoretical reasoning for this expectation is threefold:

First, the dimensional routing of H-C makes theoretically principled claims about which brand equity dimension activates which motivational channel. If the Austrian data carry signal for these dimensionally specific pathways — as the meta-analytic evidence for BI_ATT, BT_INT, and BA_PBC suggests — then H-C should account for structural variance that the aggregated models (H-A, H-B) cannot recover.

Second, H-C offers a parsimony advantage over H-D: it achieves dimensional specificity without the additional complexity of the Bourdieu-augmented constructs. In Austrian donor data, where private giving patterns dominate and symbolic public display of philanthropy is culturally less pronounced than in Anglo-American contexts, the symbolic capital pathways of H-D are expected to carry relatively weak empirical weight — insufficient to compensate for their model complexity cost under BIC.

Third, H-C directly instantiates C-BEBA-01 (dimensional architecture), C-BEBA-02 (trust as primary mechanism under uncertainty), and C-BEBA-03 (brand equity as behavioural architecture integrating signalling and motivational psychology) — the three core propositions of the BEBA framework. A result in which H-C wins the model competition would constitute the strongest available empirical support for all three core propositions simultaneously.

The empirical verdict, however, rests entirely with the pipeline output. The above represents the theoretical prior, not the finding. If the pipeline results contradict this expectation — for instance, if H-D substantially outperforms H-C, or if H-B is not improved upon by H-C — the theoretical interpretation must be revised accordingly in Chapter 11.

---

## 10.8 Mediation Analysis

### 10.8.1 Bootstrap Mediation Procedure

Indirect effects are estimated using a bias-corrected and accelerated bootstrap procedure (BCa bootstrap) with 5,000 resamples (Preacher & Hayes, 2008; Hayes, 2013). Point estimates are maximum likelihood estimates; confidence intervals are BCa bootstrap intervals. All mediation estimates are conducted within the winning model structure (expected H-C); if the model competition produces a different winner, mediation estimates are reported from that model. The analysis quantifies specific indirect effects for the theoretically central pathways identified in Chapter 4.

### 10.8.2 Specific Indirect Effects

| Indirect path | Point estimate | BCa 95% CI | Proportion mediated |
|---|---|---|---|
| BT → PBC → INT | [PIPELINE: beba_mediation_boot5000 → IE_BT_PBC_INT] | [[PIPELINE: beba_mediation_boot5000 → CI_lo_BT_PBC_INT], [PIPELINE: beba_mediation_boot5000 → CI_hi_BT_PBC_INT]] | [PIPELINE: beba_mediation_boot5000 → PM_BT_PBC_INT] |
| BIM → ATT → INT | [PIPELINE: beba_mediation_boot5000 → IE_BIM_ATT_INT] | [[PIPELINE: beba_mediation_boot5000 → CI_lo_BIM_ATT_INT], [PIPELINE: beba_mediation_boot5000 → CI_hi_BIM_ATT_INT]] | [PIPELINE: beba_mediation_boot5000 → PM_BIM_ATT_INT] |
| BA → PBC → INT | [PIPELINE: beba_mediation_boot5000 → IE_BA_PBC_INT] | [[PIPELINE: beba_mediation_boot5000 → CI_lo_BA_PBC_INT], [PIPELINE: beba_mediation_boot5000 → CI_hi_BA_PBC_INT]] | [PIPELINE: beba_mediation_boot5000 → PM_BA_PBC_INT] |
| BP → ATT → INT | [PIPELINE: beba_mediation_boot5000 → IE_BP_ATT_INT] | [[PIPELINE: beba_mediation_boot5000 → CI_lo_BP_ATT_INT], [PIPELINE: beba_mediation_boot5000 → CI_hi_BP_ATT_INT]] | [PIPELINE: beba_mediation_boot5000 → PM_BP_ATT_INT] |
| BT → INT (direct) | [PIPELINE: beba_mediation_boot5000 → DE_BT_INT] | [[PIPELINE: beba_mediation_boot5000 → CI_lo_DE_BT_INT], [PIPELINE: beba_mediation_boot5000 → CI_hi_DE_BT_INT]] | — |
| BT → INT (total) | [PIPELINE: beba_mediation_boot5000 → TE_BT_INT] | [[PIPELINE: beba_mediation_boot5000 → CI_lo_TE_BT_INT], [PIPELINE: beba_mediation_boot5000 → CI_hi_TE_BT_INT]] | — |

### 10.8.2b Total and Direct Effects

For completeness, direct and total effects of all brand equity dimensions on Donation Intention are reported alongside the indirect effects above. This decomposition allows a clean assessment of the degree to which brand equity effects are mediated versus direct:

| Effect | BT → INT | BIM → INT | BA → INT | BP → INT |
|---|---|---|---|---|
| Direct | [PIPELINE: beba_mediation_boot5000 → DE_BT_INT] | [PIPELINE: beba_mediation_boot5000 → DE_BIM_INT] | [PIPELINE: beba_mediation_boot5000 → DE_BA_INT] | [PIPELINE: beba_mediation_boot5000 → DE_BP_INT] |
| Indirect (via PBC or ATT) | [PIPELINE: beba_mediation_boot5000 → IE_BT_INT] | [PIPELINE: beba_mediation_boot5000 → IE_BIM_INT] | [PIPELINE: beba_mediation_boot5000 → IE_BA_INT] | [PIPELINE: beba_mediation_boot5000 → IE_BP_INT] |
| Total | [PIPELINE: beba_mediation_boot5000 → TE_BT_INT] | [PIPELINE: beba_mediation_boot5000 → TE_BIM_INT] | [PIPELINE: beba_mediation_boot5000 → TE_BA_INT] | [PIPELINE: beba_mediation_boot5000 → TE_BP_INT] |

The ratio of indirect to total effect — the proportion mediated — provides the key evidence for the theoretical claim that ATT and PBC function as proper mediating mechanisms (not mere covariates). If the proportion mediated for BIM → INT via ATT exceeds 0.50, this confirms that Attitude is the primary channel through which Brand Image reaches Donation Intention. If the proportion mediated for BT → INT via PBC is substantially lower than the BT → INT direct effect, this confirms the dual-pathway structure: trust operates through both a deliberative (PBC-mediated) and a heuristic (direct) channel simultaneously.[^BT-000037]

### 10.8.3 Comparison Across FC/BO and RO Subsamples

Mediation estimates are compared across the two measurement subsamples (FC_BO and RO) where the relevant constructs are available in both. The FC_BO subsample carries Brand Trust (BO_TR) and Brand Image (FC_BI) items; the RO subsample carries Brand Reputation (RO_BR) as the trust-adjacent construct. Cross-sample comparison is conducted as a constrained vs. unconstrained model comparison: if equality constraints on specific indirect effects across subsamples do not significantly worsen fit, cross-sample stability is inferred.

| Indirect path | FC_BO estimate | RO estimate | Δ (FC_BO − RO) | Equality test p |
|---|---|---|---|---|
| BT → PBC → INT | [PIPELINE: beba_mediation_boot5000 → IE_FCBO_BT_PBC_INT] | [PIPELINE: beba_mediation_boot5000 → IE_RO_BT_PBC_INT] | [PIPELINE: beba_mediation_boot5000 → Δ_BT_PBC_INT] | [PIPELINE: beba_mediation_boot5000 → p_eq_BT_PBC_INT] |
| BIM → ATT → INT | [PIPELINE: beba_mediation_boot5000 → IE_FCBO_BIM_ATT_INT] | [PIPELINE: beba_mediation_boot5000 → IE_RO_BIM_ATT_INT] | [PIPELINE: beba_mediation_boot5000 → Δ_BIM_ATT_INT] | [PIPELINE: beba_mediation_boot5000 → p_eq_BIM_ATT_INT] |

---

## 10.9 Dominance and Necessity Analysis

### 10.9.1 Dominance Analysis: Relative Importance of Brand Equity Dimensions

Dominance analysis (Budescu, 1993; Azen & Budescu, 2003; implemented in R as `domir`; Luchman, 2021) identifies the unique and shared variance contribution of each brand equity dimension to Donation Intention, controlling for all inter-predictor correlations. Unlike standardised path coefficients, which are distorted by inter-predictor collinearity and indirect paths, dominance weights partition the total R² into non-overlapping additive contributions that sum to the total explained variance. This property makes dominance analysis the preferred method for determining the relative empirical importance of brand equity dimensions as actionable management priorities.[^BD-BEH]

The theoretical prior ordering — based on the posterior evidence weights in the knowledge graph — is: Brand Trust > Brand Image > Brand Awareness > Brand Personality. This ordering reflects: the highest knowledge-graph posterior for BT (BT_INT = 0.892, 31 studies); a strong but somewhat lower posterior for BIM (BI_ATT = 0.921, feeding into INT via ATT); a moderate posterior for BA (BA_INT = 0.736, 21 studies); and the most restricted evidence base for BP (7 studies, posterior = 0.850 for BP_ATT, but a weaker chain to INT). The empirical ordering from the Austrian sample is reported as pipeline output.

| Predictor | General dominance weight | % of total R² | Empirical rank |
|---|---|---|---|
| Brand Trust (BT) | [PIPELINE: beba_domir_INT → dom_BT] | [PIPELINE: beba_domir_INT → pct_BT] | [PIPELINE: beba_domir_INT → rank_BT] |
| Brand Image (BIM) | [PIPELINE: beba_domir_INT → dom_BIM] | [PIPELINE: beba_domir_INT → pct_BIM] | [PIPELINE: beba_domir_INT → rank_BIM] |
| Brand Awareness (BA) | [PIPELINE: beba_domir_INT → dom_BA] | [PIPELINE: beba_domir_INT → pct_BA] | [PIPELINE: beba_domir_INT → rank_BA] |
| Brand Personality (BP) | [PIPELINE: beba_domir_INT → dom_BP] | [PIPELINE: beba_domir_INT → pct_BP] | [PIPELINE: beba_domir_INT → rank_BP] |
| Total R² (INT) | — | 100% | [PIPELINE: beba_domir_INT → R2_total] |

Complete dominance between pairs of predictors (i.e., whether predictor A dominates predictor B in all possible subsets of the remaining predictors) is assessed using the complete dominance matrix from `domir`. Pairwise complete dominance is declared only where the directional advantage holds across all subset sizes.

### 10.9.2 Necessary Condition Analysis

Necessary Condition Analysis (NCA; Dul, 2016, 2020) identifies whether a given brand equity dimension functions as a *necessary condition* for donation intention — that is, whether above-threshold levels of the dimension are required for intention to be high, regardless of other conditions. NCA operates on the upper-left ceiling of the bivariate scatter plot (ceiling line regression, CR-FDH: Free Disposal Hull; and CE-FDH: ceiling envelopment) and calculates an effect size d as the area above the ceiling line divided by the total scatter area. The NCA effect size interpretation follows Dul (2020): d < 0.1 negligible, 0.1–0.3 small, 0.3–0.5 medium, d > 0.5 large.

| Predictor → INT | d (CR-FDH) | d (CE-FDH) | Bottleneck threshold | Necessity verdict |
|---|---|---|---|---|
| Brand Trust (BT) | [PIPELINE: beba_nca_INT → d_CR_BT] | [PIPELINE: beba_nca_INT → d_CE_BT] | [PIPELINE: beba_nca_INT → bottleneck_BT] | [PIPELINE: beba_nca_INT → necessity_BT] |
| Brand Image (BIM) | [PIPELINE: beba_nca_INT → d_CR_BIM] | [PIPELINE: beba_nca_INT → d_CE_BIM] | [PIPELINE: beba_nca_INT → bottleneck_BIM] | [PIPELINE: beba_nca_INT → necessity_BIM] |
| Brand Awareness (BA) | [PIPELINE: beba_nca_INT → d_CR_BA] | [PIPELINE: beba_nca_INT → d_CE_BA] | [PIPELINE: beba_nca_INT → bottleneck_BA] | [PIPELINE: beba_nca_INT → necessity_BA] |
| Brand Personality (BP) | [PIPELINE: beba_nca_INT → d_CR_BP] | [PIPELINE: beba_nca_INT → d_CE_BP] | [PIPELINE: beba_nca_INT → bottleneck_BP] | [PIPELINE: beba_nca_INT → necessity_BP] |

The theoretical expectation, derived from the credence-good framework in Chapter 2, is that Brand Trust and Brand Awareness will qualify as necessary conditions for donation intention — trust because donors who have no confidence in the organisation's integrity do not donate regardless of image or personality, and awareness because a brand that does not exceed the awareness threshold is not in the donor's consideration set at all. Brand Image and Brand Personality, by contrast, are expected to function as sufficiency-enhancing factors rather than necessity conditions: their absence constrains ceiling levels of intention but does not uniformly block low-to-medium intention formation.[^BA-000081]

---

## 10.10 Kano-Analog Analysis

### 10.10.1 Penalty-Reward Contrast Method

The Kano-analog analysis applies the penalty-reward contrast method (Brandt, 1987; Matzler, Fuchs & Schubert, 2004) to classify brand equity dimensions by the asymmetric functional form of their effect on Donation Intention. The method runs two separate regressions:

1. **Reward regression**: Regresses high satisfaction on brand equity dimensions (satisfaction dummy coded: 5 = 1, others = 0).
2. **Penalty regression**: Regresses low satisfaction on reverse-coded brand equity dimensions (dissatisfaction dummy coded: 1 = 1, others = 0).

The Brandt (1987) quadrant classification is then applied:
- **Basic (Must-Be / BBB)**: High penalty, low reward — deficit hurts, surplus does not help.
- **Performance (Linear / BLB)**: Penalty ≈ Reward — symmetric functional form.
- **Bonus (Excitement / BUB)**: Low penalty, high reward — deficit not noticed, surplus appreciated.
- **Indifferent (Neutral / NNB)**: Low penalty, low reward — dimension does not drive satisfaction.

### 10.10.2 Classification Results

| Dimension | Penalty coefficient | Reward coefficient | Quadrant | Management interpretation |
|---|---|---|---|---|
| Brand Trust (BT) | [PIPELINE: beba_kano_asymmetry → penalty_BT] | [PIPELINE: beba_kano_asymmetry → reward_BT] | [PIPELINE: beba_kano_asymmetry → quadrant_BT] | [PIPELINE: beba_kano_asymmetry → interpretation_BT] |
| Brand Image (BIM) | [PIPELINE: beba_kano_asymmetry → penalty_BIM] | [PIPELINE: beba_kano_asymmetry → reward_BIM] | [PIPELINE: beba_kano_asymmetry → quadrant_BIM] | [PIPELINE: beba_kano_asymmetry → interpretation_BIM] |
| Brand Awareness (BA) | [PIPELINE: beba_kano_asymmetry → penalty_BA] | [PIPELINE: beba_kano_asymmetry → reward_BA] | [PIPELINE: beba_kano_asymmetry → quadrant_BA] | [PIPELINE: beba_kano_asymmetry → interpretation_BA] |
| Brand Personality (BP) | [PIPELINE: beba_kano_asymmetry → penalty_BP] | [PIPELINE: beba_kano_asymmetry → reward_BP] | [PIPELINE: beba_kano_asymmetry → quadrant_BP] | [PIPELINE: beba_kano_asymmetry → interpretation_BP] |

### 10.10.3 Theoretical Expectations and Management Implications

The theoretical synthesis in Chapter 4 generates two specific classification expectations for the Kano analysis:

**Brand Trust — expected Basic (BBB)**: Trust in a nonprofit is a credence-good certification signal. Under conditions of high uncertainty, donors who perceive low trust will not donate, regardless of image or personality evaluations. The threshold effect of trust — its necessity function established in Section 10.9 — predicts an asymmetric penalty: deficits in trust produce strong intention penalties (donors exit the consideration set), but surpluses produce diminishing marginal returns because trust already exceeds the functional threshold for most donors once a basic legitimacy level is established. This expectation aligns with the Basic quadrant: trust is a hygiene factor in donation decisions.[^BT-000036]

**Brand Image — expected Bonus (BUB)**: Brand Image, as a set of positive evaluative associations about mission distinctiveness and organisational competence, functions differently from trust. Donors who perceive low image quality do not necessarily exit the consideration set — they may still donate if trust and awareness are adequate. But donors who perceive high image quality may become meaningfully more engaged: strong brand associations amplify the reward value of giving beyond the baseline motivation level. This pattern predicts a Bonus classification: low image does not produce strong intention penalties, but high image produces incremental intention gains.[^BI-000001]

If the pipeline results confirm these classifications, they have direct implications for nonprofit brand management resource allocation: trust-building must be treated as a non-negotiable baseline investment (threshold maintenance), while image investment yields returns primarily in the upper segment of the donor engagement spectrum and should be targeted rather than universally deployed.

---

## 10.11 Segmented Results and Moderation

### 10.11.1 Socioeconomic Status as Covariate

Socioeconomic Status (SES_z, standardised composite from self-reported education, income band, and occupational prestige) was included as a covariate in all structural models. Its structural role is twofold: (a) as a control variable that prevents brand equity path estimates from absorbing SES-confounded variance (higher-SES donors may both have higher brand equity perceptions and donate more, for reasons unrelated to brand equity's causal effect); and (b) as a potential moderator of the brand equity → intention relationship, if the BEBA architecture operates differently across the SES distribution.

The estimated SES_z coefficient on Donation Intention: β = [PIPELINE: beba_segmented_SES → path_SES_INT]; on Donation Amount: β = [PIPELINE: beba_segmented_SES → path_SES_BEH_amt]. The interaction term SES_z × BT for the BT → INT path: β = [PIPELINE: beba_segmented_SES → path_SESxBT_INT], p = [PIPELINE: beba_segmented_SES → p_SESxBT_INT]. A significant positive interaction would indicate that Brand Trust is a more potent predictor of donation intention among higher-SES donors — consistent with theoretical arguments that trust becomes especially decision-relevant when the stakes of giving are higher (higher gift amounts, higher engagement commitment).

### 10.11.2 Empathy Profiling: k-Means Cluster Results

Donor empathy is measured through five EW01 dimensions operationalising the donor's affective and cognitive engagement with the nonprofit's beneficiary group: Empathic Concern (EC), Perspective Taking (PT), Personal Distress (PD), Empathic Resonance (ER), and Narrative Transportation (NT). The k-Means cluster analysis (k = [PIPELINE: beba_kmeans_EW → k_optimal], determined by silhouette criterion) identifies internally homogeneous donor empathy profiles:

| Cluster | n | EC (M) | PT (M) | PD (M) | ER (M) | NT (M) | Profile label |
|---|---|---|---|---|---|---|---|
| [PIPELINE: beba_kmeans_EW → cluster_1_label] | [PIPELINE: beba_kmeans_EW → n_cluster_1] | [PIPELINE: beba_kmeans_EW → EC_c1] | [PIPELINE: beba_kmeans_EW → PT_c1] | [PIPELINE: beba_kmeans_EW → PD_c1] | [PIPELINE: beba_kmeans_EW → ER_c1] | [PIPELINE: beba_kmeans_EW → NT_c1] | [PIPELINE: beba_kmeans_EW → label_c1] |
| [PIPELINE: beba_kmeans_EW → cluster_2_label] | [PIPELINE: beba_kmeans_EW → n_cluster_2] | [PIPELINE: beba_kmeans_EW → EC_c2] | [PIPELINE: beba_kmeans_EW → PT_c2] | [PIPELINE: beba_kmeans_EW → PD_c2] | [PIPELINE: beba_kmeans_EW → ER_c2] | [PIPELINE: beba_kmeans_EW → NT_c2] | [PIPELINE: beba_kmeans_EW → label_c2] |
| [PIPELINE: beba_kmeans_EW → cluster_3_label] | [PIPELINE: beba_kmeans_EW → n_cluster_3] | [PIPELINE: beba_kmeans_EW → EC_c3] | [PIPELINE: beba_kmeans_EW → PT_c3] | [PIPELINE: beba_kmeans_EW → PD_c3] | [PIPELINE: beba_kmeans_EW → ER_c3] | [PIPELINE: beba_kmeans_EW → NT_c3] | [PIPELINE: beba_kmeans_EW → label_c3] |

### 10.11.3 Moderation: Does the BEBA Architecture Differ by Donor Segment?

To test whether the dimensional routing of the BEBA model is invariant across empathy clusters, a multigroup SEM is estimated with cluster membership as the grouping variable. Two constrained models are compared: one in which all structural paths are equal across clusters (full structural invariance) and one in which all paths are freely estimated per cluster (unconstrained multigroup model). The chi-square difference test quantifies whether allowing path heterogeneity across empathy clusters yields a statistically significant improvement.

The theoretically predicted interaction is between the BP → ATT path and empathy cluster membership: donors with high Empathic Concern and Narrative Transportation profiles are expected to show a stronger Brand Personality → Attitude path, because personality cues that communicate affinity and congruity with the beneficiary group are more personally relevant to high-empathy donors. By contrast, for low-empathy, instrumentally oriented donors, Brand Trust and Perceived Behavioural Control are expected to carry relatively more weight in the intention-formation process.

| Path | Full sample β | High-empathy cluster β | Low-empathy cluster β | Interaction p |
|---|---|---|---|---|
| BP → ATT | [PIPELINE: beba_sem_HC → path_BP_ATT] | [PIPELINE: beba_moderation_EW_cluster → path_BP_ATT_highEW] | [PIPELINE: beba_moderation_EW_cluster → path_BP_ATT_lowEW] | [PIPELINE: beba_moderation_EW_cluster → p_interaction_BP_ATT] |
| BT → INT | [PIPELINE: beba_sem_HC → path_BT_INT] | [PIPELINE: beba_moderation_EW_cluster → path_BT_INT_highEW] | [PIPELINE: beba_moderation_EW_cluster → path_BT_INT_lowEW] | [PIPELINE: beba_moderation_EW_cluster → p_interaction_BT_INT] |
| BA → PBC | [PIPELINE: beba_sem_HC → path_BA_PBC] | [PIPELINE: beba_moderation_EW_cluster → path_BA_PBC_highEW] | [PIPELINE: beba_moderation_EW_cluster → path_BA_PBC_lowEW] | [PIPELINE: beba_moderation_EW_cluster → p_interaction_BA_PBC] |

If the moderation analysis reveals significant path heterogeneity — particularly for the BP → ATT path — this has implications for the generalisability of the BEBA architecture: the configural routing is correct at the aggregate level, but the weights of individual pathways are donor-segment-contingent. Such a finding would motivate a segmented BEBA dashboard framework in Chapter 11, where different brand management priorities apply to different empathy-defined donor groups.

---

## 10.12 Synthesis: What the Results Mean for BEBA Theory

### 10.12.1 Mechanisms That Received Strongest Empirical Support

The empirical evaluation in this chapter is designed to provide differentiated rather than binary support for the BEBA framework. Even if H-C emerges as the best-supported model in the formal model competition, not all of its dimensional pathways carry equal empirical support, and the synthesis in Chapter 11 must reflect this heterogeneity. The present section maps the anticipated pattern of evidence onto the three core BEBA propositions:

**C-BEBA-01 — Brand equity operates as a multi-channel behavioural architecture**: Supported if H-C fits better than H-B — i.e., if dimensional specificity carries structural information beyond the undifferentiated partial mediation baseline. The strength of this support is a function of the ΔBIC between H-C and H-B and the pattern of dimensionally specific path estimates.[^C-BEBA-01]

**C-BEBA-02 — Brand Trust is the primary mechanism under conditions of credence-good uncertainty**: Supported if BT → PBC and BT → INT paths are among the strongest in H-C, if Brand Trust achieves the highest dominance weight in the dominance analysis, if NCA identifies Brand Trust as a necessary condition for intention, and if the Kano analysis classifies it as a Basic (BBB) factor. Convergence across all four analyses constitutes the strongest possible support for C-BEBA-02.[^BT-000036][^BT-000037]

**C-BEBA-03 — The BEBA architecture integrates signal theory, brand equity theory, and IBM into a unified behavioural explanation**: Supported if H-C outperforms H-D — i.e., if the sociological augmentation of the Bourdieu model does not explain meaningfully more variance than the theoretically leaner BEBA configural architecture. A finding that H-C is preferred over H-D under BIC would indicate that signalling, brand equity, and TPB/IBM mechanisms already capture the variance that a social capital mechanism would explain — and that the Bourdieu extension is theoretically interesting but empirically redundant in the Austrian charitable giving context.[^C-BEBA-03]

### 10.12.2 Implications for the Uncertainty Reduction Framework

The BEBA framework's foundation is the conceptualisation of nonprofit brand equity as an uncertainty reduction mechanism rather than as a simple value indicator (Chapter 2). The empirical results speak to this foundational claim primarily through two channels: (a) the relative strength of Brand Trust pathways compared to Brand Image and Brand Personality pathways, and (b) the necessity analysis results for trust.

If Brand Trust is both the strongest predictor of donation intention in the dominance analysis and a necessary condition in the NCA — i.e., if it functions as both the most important sufficient driver and as a gateway condition — this provides triangulated support for the credence-good mechanism: donors who have not achieved a minimum trust threshold simply do not donate, and among donors who have crossed that threshold, higher trust continues to elevate intention more than any other brand dimension. This dual pattern of necessity and sufficiency cannot be explained by a simple linear brand equity model; it requires the threshold-and-gradient architecture that BEBA supplies.[^BE-000066]

The uncertainty reduction framework also implies that the brand equity → behaviour relationship should be stronger for donors facing higher epistemic uncertainty about the nonprofit — donors with lower prior knowledge of the organisation, donors evaluating organisations in sectors where output quality is harder to verify, donors with less experience of charitable giving. The SES moderation and empathy cluster moderation results in Section 10.11 provide partial tests of this boundary condition: if trust effects are stronger among low-experience, low-awareness segments, the uncertainty reduction mechanism is further supported.

### 10.12.3 Limitations

Four limitations qualify the empirical findings and must be foregrounded in the discussion:

**Cross-sectional design**: The Austrian donor survey is a single time-point measurement. Path coefficients in the structural models represent covariance relationships, not experimentally established causal effects. While the theoretical causal ordering from brand equity to intention to behaviour is well-grounded in prior research and in the IBM/TPB framework, the data themselves are correlational. The intention measures (INT) were assessed in the same survey wave as the brand equity measures; the behavioural outcomes (BEH) are retrospective self-reports of past giving behaviour rather than prospectively observed actual donations. This creates a shared-method-variance risk for INT-based analyses and a recall-validity risk for BEH-based analyses.

**Single-country sample**: The Austrian donor context — characterised by high institutional trust, a concentrated charity landscape, and specific regulatory visibility (Spendengütesiegel) — may not generalise to other national or cultural settings. Specifically, the expected weakness of the Bourdieu-augmented H-D in Austrian data may not replicate in contexts where public charitable giving is more visibility-driven (e.g., North American major giving cultures, or emerging market contexts where social signalling of prosocial behaviour is more prominent). The theoretical and structural parameters of BEBA must be treated as Austrian-context estimates; cross-national generalisability requires additional replication.

**Self-report intention as a behavioural proxy**: Donation Intention is not donation behaviour. The intention–behaviour gap documented across numerous applied health and social behaviour studies (Sheeran, 2002; Webb & Sheeran, 2006) cautions against treating high intention scores as reliable predictors of actual future giving. The IBM's enactment layer constructs (Habit, Salience, Knowledge, Constraints) partially address this gap, but they do not eliminate it. A longitudinal design with follow-up actual giving data would be required to validate the INT → BEH pathway empirically.

**Formative outer model for overall Brand Equity**: The formative specification of BE_overall as a weighted composite of BA, BIM, BT, and BP introduces a measurement assumption — that the four dimensions are conceptually distinct and collectively sufficient — that is maintained rather than empirically tested within the SEM. The weights assigned from the dominance analysis carry uncertainty that is not propagated into the structural path estimates. A future study using a fully reflective second-order model or a Bayesian hierarchical specification would allow this uncertainty to be represented in the credible intervals of the structural parameters.

### 10.12.3b Convergent Evidence from Complementary Analyses

A key methodological characteristic of this chapter is the use of multiple analytical lenses applied to the same dataset. The model competition (Section 10.7), mediation analysis (Section 10.8), dominance and necessity analysis (Section 10.9), Kano-analog classification (Section 10.10), and segmented moderation (Section 10.11) each address a distinct facet of the brand equity → behaviour relationship. Their value derives precisely from their independence: a finding that emerges from only one analysis must be treated as exploratory; a finding that appears convergently across multiple analyses carries substantially stronger evidentiary weight.

The convergence strategy applies directly to the core BEBA propositions:

- If Brand Trust is the strongest predictor in dominance analysis AND achieves necessity status in NCA AND shows a Basic classification in Kano AND the BT → INT path is significant in H-C AND the BT-related Bayes Factor for H-C over H-A is large, the convergent evidence for C-BEBA-02 is of the highest grade attainable in a single-study cross-sectional design.
- If the model competition confirms H-C over H-B AND the dimensional path estimates are individually significant AND the dominance ordering follows the theoretical prior (Trust > Image > Awareness > Personality), this constitutes convergent multi-method support for C-BEBA-01.
- If H-C outperforms H-D under BIC AND the Bourdieu-specific paths (SIS, FUI, SymCap) show weak or non-significant estimates, this constitutes evidence against the sociological extension and in favour of the parsimonious psychological-signalling architecture of C-BEBA-03.

Divergences across methods — findings where one analysis supports and another qualifies a BEBA proposition — are reported transparently in Chapter 11 and treated as boundary conditions rather than refutations. The goal is not to confirm the BEBA framework but to characterise the conditions under which its propositions hold, the magnitude of the supporting evidence, and the domains in which further research is required.

### 10.12.4 Future Research Directions

The limitations above define a clear agenda for future research within the BEBA programme:

**Longitudinal tracking**: A two-wave or multi-wave design that separates brand equity measurement from subsequent actual giving behaviour would allow the INT → BEH pathway to be validated with observational behavioural data. Panel designs with linked CRM records (donor database linkage) would eliminate retrospective recall bias in the BEH measures.

**Actual behaviour via field experiments**: Experimental or quasi-experimental designs that manipulate brand equity perceptions — e.g., by varying the trust signals or brand associations presented to prospective donors in online fundraising contexts — would establish causal evidence for the brand equity → behaviour pathways that correlational SEM cannot provide. Digital fundraising platforms offer a natural experimental infrastructure for such designs.

**Cross-national replication**: Replication of the BEBA model competition in at least two additional national contexts — one with a more public, visibility-driven giving culture and one with lower institutional trust levels — would allow the cultural boundary conditions of the Austrian findings to be assessed. The theoretical prediction is that the Bourdieu-augmented H-D should show stronger relative performance in high-visibility, low-institutional-trust contexts.

**Necessary condition threshold tracking**: The NCA bottleneck thresholds identified in Section 10.9 represent the minimum levels of each brand equity dimension required for high donation intention. These thresholds can serve as KPI targets in brand monitoring systems. Longitudinal tracking of threshold positions — whether they remain stable or shift as the charitable landscape becomes more crowded or as donor uncertainty patterns change — would convert a static analytical result into a dynamic management instrument.

**Multi-organisation and sector heterogeneity**: The present study evaluates multiple nonprofit brands within a single survey, but the analytical unit is the organisation-level observation rather than the organisation itself. A future design that recruits separate large samples per organisation — enabling proper organisational-level SEM with between-organisation variance modelled explicitly — would allow the BEBA architecture to be tested as an organisational-level theory: which organisations with higher brand trust attract more donations, net of individual donor characteristics and organisational size? This is a meaningfully different causal question from the individual-level question answered here.

**Empathy dimensionality and brand personality routing**: The empathy cluster moderation in Section 10.11 is exploratory. A confirmatory test of the BP → ATT × empathy moderation would require a preregistered design with a priori cluster definitions and a larger within-cluster sample size to achieve sufficient statistical power for interaction detection. The theoretical prediction — that narrative transportation and empathic concern specifically amplify brand personality effects — warrants direct experimental testing through vignette designs that manipulate brand personality cues and empathy activation independently.

---

## Footnotes

[^LP-000001]: The likelihood paradigm as the governing inferential framework of the BEBA model competition is specified in Chapter 5 (Edwards, 1972; Royall, 1997). Bayes Factors are computed from BIC approximations following Kass and Raftery (1995); all BF thresholds applied in Section 10.7 follow their published classification scale.

[^C-BEBA-01]: C-BEBA-01 states that nonprofit brand equity operates not as a unitary antecedent but as a dimensional architecture in which each brand equity component activates a specific motivational pathway. The architectural specificity claim is the primary hypothesis distinguishing H-C from H-A and H-B.

[^C-BEBA-02]: C-BEBA-02 states that Brand Trust is the primary uncertainty-reduction mechanism in nonprofit brand equity, functioning as both a necessary and a sufficient-amplifying condition for donation intention under conditions of credence-good uncertainty. This proposition is tested empirically through the dominance analysis (Section 10.9.1), the NCA (Section 10.9.2), and the Kano-analog analysis (Section 10.10).

[^C-BEBA-03]: C-BEBA-03 states that the BEBA architecture provides a theoretically parsimonious integration of signalling theory (Chapter 2), brand equity theory (Chapter 3), and the IBM/TPB (Chapter 4), and that this integration is sufficient to account for donation behaviour variation without recourse to sociological field-capital mechanisms. C-BEBA-03 is tested through the H-C vs. H-D comparison in Section 10.7.

[^BT-000036]: BT-000036 identifies Brand Trust as the central theoretical mechanism of nonprofit brand equity in credence-good donation contexts. The canonical definition used throughout: Brand Trust is the donor's willingness to rely on the nonprofit to fulfil its stated mission without direct verification of organisational conduct or impact, grounded in accumulated reputational signals and prior relationship experiences.

[^BT-000037]: BT-000037 specifies the dual-pathway mechanism of Brand Trust in the BEBA model: a deliberative pathway (BT → PBC → INT, trust elevates perceived behavioural control through risk reduction) and a fast-heuristic pathway (BT → INT direct, trust functions as a cognitive shortcut to intention formation bypassing full deliberative processing). The dual specification reflects the dual-process theoretical foundation developed in Chapter 2.

[^BE-000066]: BE-000066 anchors the claim that nonprofit brand equity is a multidimensional construct whose dimensions are non-interchangeable in their downstream behavioural functions. The formative outer model specification adopted in H-C directly instantiates this multidimensionality claim. Evidence: the comparative fit of H-C over H-A and H-B, to be populated from pipeline outputs.

[^BD-BEH]: BD-BEH encodes the knowledge-graph posterior for the Brand Differentiation → Behaviour pathway: posterior = 0.611, based on n = 6 studies in the evidence synthesis. This is a *theoretical prior* from the meta-analytic literature review pipeline, not a result from the Austrian survey. Austrian-sample estimates are represented as `[PIPELINE: ...]` placeholders throughout this chapter.

[^BA-000080]: BA-000080 anchors the recognition heuristic pathway: Brand Awareness functions as a cognitive accessibility signal that elevates Perceived Behavioural Control by reducing the epistemic cost of the donation decision. The theoretical source is Goldstein and Gigerenzer (2002); the nonprofit application is developed in Chapter 4.

[^BA-000081]: BA-000081 identifies the boundary condition of Brand Awareness as a heuristic pathway: awareness effects on PBC are expected to be threshold-conditional. Below a minimum awareness level, a charity does not enter the donor's consideration set; above the threshold, marginal awareness increments yield diminishing returns to PBC. This is consistent with the NCA necessity framework applied in Section 10.9.

[^BI-000001]: BI-000001 encodes the partial mediation evidence base: a review of existing nonprofit brand equity studies finds consistent evidence that brand evaluations retain a direct effect on donation intention even after ATT, SN, and PBC are controlled (Faircloth et al., 2001; Pope et al., 2009; Sargeant & Lee, 2004). The posterior for this claim informs the H-B specification.

[^BI-000002]: BI-000002 encodes the complementary claim: while partial mediation is evidenced in the existing literature, the *dimensional specificity* of partial mediation pathways — which brand equity dimension directly reaches intention, and which is fully channelled through ATT or PBC — is underspecified in prior models. H-C addresses this underspecification by routing each dimension to its theoretically predicted mediating construct.

[^NB-000102]: Faircloth, R. L., Capella, L. M., & Alford, B. L. (2001). The effect of brand attitude and brand image on brand equity. *Journal of Marketing Theory and Practice*, 9(3), 61–75. See Chapter 8 for full model specification.

[^NB-000103]: The measurement invariance assessment framework follows Vandenberg and Lance (2000) and Putnick and Bornstein (2016). All invariance tests are conducted in lavaan (Rosseel, 2012) using the MLR estimator with Satorra–Bentler scaled test statistics.
