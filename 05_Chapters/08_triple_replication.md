---
title: "Chapter 8 — Triple Replication of Nonprofit Brand Equity Models"
status: draft
object_type: Chapter
layer: Empirical
chapter_number: 8
part: "III — Empirical Evidence"
claim_anchors:
  - NB-000102
  - NB-000103
  - CB-000020
  - CB-000021
pipeline_objects:
  - cross_cfa_Faircloth.rds
  - cross_med_full_Faircloth.rds
  - cross_med_partial_Faircloth.rds
  - cross_cfa_Boenigk.rds
  - cross_med_full_Boenigk.rds
  - cross_med_partial_Boenigk.rds
  - cross_cfa_Romero.rds
  - ro_cfa_with_id.rds
  - ro_mediation_full.rds
  - ro_mediation_partial.rds
estimator: MLR
missing_data: FIML
fit_thresholds:
  CFI_TLI_good: "≥ .95"
  CFI_TLI_acceptable: "≥ .90"
  RMSEA_good: "≤ .06"
  RMSEA_acceptable: "≤ .08"
  SRMR_good: "≤ .08"
measurement_quality:
  omega_threshold: "≥ .70"
  AVE_threshold: "≥ .50"
  HTMT_strict: "< .85"
  HTMT_tolerant: "< .90"
research_question: "How do nonprofit brands become behaviourally effective under conditions of uncertainty?"
chapter_function: >
  Compares three existing nonprofit brand equity model architectures in an Austrian donor context,
  establishing which provides the best psychometric and structural foundation before the BEBA
  model is tested in Chapter 10.
predecessors:
  - Chapter 7 — SEM, Model Comparison, and Robustness
successors:
  - Chapter 9 — Evidence-Based Charity Brand Dashboards
  - Chapter 10 — Empirical Evaluation of BEBA
---

# Chapter 8 — Triple Replication of Nonprofit Brand Equity Models

---

## 8.1 Scientific Question and Chapter Function

The present chapter addresses a foundational question within the empirical portion of this research programme: Which of the existing structural architectures proposed for nonprofit brand equity replicates most adequately under Austrian donor conditions, and what does their comparative performance imply about the latent structure of brand equity in charitable contexts? This question is prior to the BEBA hypothesis tested in Chapter 10. Before proposing a novel integrative architecture, it is necessary to establish the empirical ceiling and the structural limits of the three most theoretically and methodologically developed nonprofit brand equity models in the existing literature.

Three models are evaluated: Faircloth (2005), whose third-order structure represents an early formalisation of nonprofit brand equity from commercial brand equity foundations; Boenigk and Becker (2016) / Boenigk and Helmig (2013), whose second-order Trust–Commitment model foregrounds the relational-institutional character of nonprofit brands; and Romero, Ríos, and colleagues (2023), whose nine-factor third-order structure represents the most comprehensive contemporary attempt to capture the multidimensionality of nonprofit brand equity.[^NB-000102] All three are evaluated on the same Austrian sample using identical estimation conditions, making the comparison meaningful rather than confounded by methodological inconsistency.

The chapter serves four functions within the broader research programme. First, it establishes measurement baselines: item-level psychometric quality, factor reliability, convergent and discriminant validity for each of the three operationalisations.[^NB-000103] Second, it tests whether the proposed higher-order factor structures hold under Austrian donor conditions — a context distinguished from the largely North American and Spanish source populations. Third, it delivers comparative structural evidence on which brand equity architecture predicts donation behaviour most consistently across three distinct behavioural outcomes: donor status (binary), donation frequency (log-transformed), and donation amount (log-transformed). Fourth, it identifies residual structural problems — unresolved discriminant validity failures, collapsed dimensions, or poor path predictability — that motivate the revised BEBA architecture introduced in Chapter 10.[^CB-000020]

The chapter is not a replication in the narrow sense of repeating a prior study. It is a **structural transportability test**: whether the latent structure proposed in a given model is preserved when applied to a different cultural, organisational, and demographic context using a more demanding estimation framework (MLR with FIML) than most source studies employed.[^CB-000021]

---

## 8.2 The Three Replication Models: Theoretical Justification and Construct Architectures

### 8.2.1 Faircloth (2005): Third-Order Brand Equity from Attitudinal Dimensions

Faircloth's (2005) operationalisation of nonprofit brand equity represents a deliberate adaptation of Aaker's (1991) consumer brand equity framework to the nonprofit domain. The underlying logic is that brand equity in nonprofit contexts is constituted by six interrelated perceptual dimensions: **Brand Image** (the set of associations held about the organisation), **Brand Personality** (symbolic and character-based differentiation), **Brand Salience/Awareness** (cognitive accessibility and top-of-mind recognition), **Brand Differentiation** (the degree to which the organisation is perceived as distinctive within its sector), **Brand Familiarity** (experiential knowledge and contact history), and **Brand Relevance** (perceived match between organisational mission and personal values or concerns). These six first-order factors are proposed to load onto a single second-order construct — Brand Attitude — which in turn constitutes the third-order construct of Brand Equity.[^NB-000102]

The structural model connects Brand Image (BI) and Brand Personality (BP) as primary attitudinal antecedents, each path-connected to Brand Attitude, which then predicts behavioural intentions. In the present replication, the downstream structural target is extended beyond Faircloth's original intention measure to encompass the three BEBA behavioural outcomes: donor status, donation frequency, and donation amount.

**Item structure.** The FC dataset includes items for each of the six first-order factors. Item counts per factor: Brand Image (FC_BI, [PIPELINE: cross_cfa_Faircloth → n_items FC_BI] items), Brand Personality (FC_BP, [PIPELINE: cross_cfa_Faircloth → n_items FC_BP] items), Brand Salience/Awareness (FC_BS, [PIPELINE: cross_cfa_Faircloth → n_items FC_BS] items), Brand Differentiation (FC_BD, [PIPELINE: cross_cfa_Faircloth → n_items FC_BD] items), Brand Familiarity (FC_BF, [PIPELINE: cross_cfa_Faircloth → n_items FC_BF] items), Brand Relevance (FC_BR, [PIPELINE: cross_cfa_Faircloth → n_items FC_BR] items).

**Key theoretical expectation.** The third-order structure should yield a single dominant higher-order factor whose variance is sufficient to account for first-order covariances, leaving only small residual correlations. If the structure collapses — if first-order factors fail to discriminate adequately from one another — this indicates that Austrian donors do not hold sufficiently differentiated perceptions of these six brand dimensions, and that a more parsimonious structure may be empirically preferable.

### 8.2.2 Boenigk and Becker (2016) / Boenigk and Helmig (2013): Trust–Commitment Brand Equity

The Boenigk and Becker (2016) model, developed on the theoretical foundations of Boenigk and Helmig (2013), represents a distinctly relational approach to nonprofit brand equity. Rather than decomposing brand equity into attitudinal facets, this framework identifies two core relational constructs — **Brand Trust** (BO_TR) and **Brand Commitment** (BO_CO) — as first-order indicators of a second-order Brand Equity construct. Brand Trust captures the donor's willingness to rely on the nonprofit under conditions of incomplete information about organisational impact and integrity. Brand Commitment captures the depth of psychological attachment and the donor's disposition toward long-term relationship maintenance.

The second-order structure is theoretically motivated by the credence-good nature of nonprofit services: since donors cannot directly verify organisational output quality, reliance shifts to relational signals. Trust and commitment, in this account, are not merely antecedents of brand equity — they are its constitutive dimensions in a context where transactional evaluation is impossible.[^NB-000103] The structural model then connects Brand Equity (second-order) to Donation Intention as the primary downstream criterion; in the present replication, this pathway is extended to the three behavioural outcomes.

**Item structure.** BO_TR ([PIPELINE: cross_cfa_Boenigk → n_items BO_TR] items); BO_CO ([PIPELINE: cross_cfa_Boenigk → n_items BO_CO] items). Total model scale coverage: [PIPELINE: cross_cfa_Boenigk → total items] items across two first-order factors.

**Key theoretical expectation.** Given the theoretical centrality of trust in the charitable decision literature (cf. Chapter 2), the Boenigk–Becker model should show superior predictive validity for actual behavioural outcomes relative to attitudinal-only operationalisations. A critical test is whether Brand Equity (BO_BE, second-order) fully mediates the Trust–Commitment → behaviour pathway, or whether Trust and Commitment have residual direct effects on behavioural outcomes once their shared Brand Equity variance is removed.

### 8.2.3 Romero et al. (2023): Nine-Factor Third-Order Brand Equity

The Romero et al. (2023) model is the most recent and structurally ambitious of the three frameworks. Drawing on extensive qualitative and quantitative research in the Spanish nonprofit sector, it proposes nine first-order factors — including dimensions of brand awareness, brand associations, brand quality, brand loyalty, brand authenticity, brand reputation, brand personality, brand differentiation, and brand relevance — loading onto a single third-order Brand Equity construct (RO_BE). The precise factor labels and item groupings follow the Romero et al. (2023) operationalisation.

This architecture reflects an attempt to integrate Aakerian, Kellerian, and relationship-marketing perspectives within a single measurement model. Its complexity is both its theoretical strength and its empirical vulnerability: nine correlated first-order factors create substantial discriminant validity pressure, and the higher-order structure requires that each first-order factor's covariance with others is adequately explained by shared Brand Equity variance.

**Item structure.** RO_BE is constituted by nine first-order factors: [PIPELINE: cross_cfa_Romero → factor names and item counts per factor]. Total items: [PIPELINE: cross_cfa_Romero → total items].

**Key theoretical expectation.** The complexity of the Romero model makes it sensitive to cultural context. Austrian donors, operating in a high-trust, institutionalised charity landscape with strong regulatory visibility, may not differentiate between some of the nine dimensions as sharply as donors in the original Spanish context. Collapsed or near-identical first-order factors would signal inadequate discriminant validity and motivate dimension reduction in subsequent models.

---

## 8.3 Sample and Data

### 8.3.1 The Austrian Donor Context: Why Replication Here Matters

Austria constitutes a theoretically interesting and practically underexplored replication context for nonprofit brand equity research. Charitable giving in Austria is characterised by a comparatively high level of sectoral institutionalisation: dominant national charity brands (Caritas, Rotes Kreuz, WWF Austria, SOS Kinderdorf, and others) operate under sustained public visibility and regulatory oversight (Österreichisches Spendengütesiegel), creating a donor environment in which brand familiarity and institutional trust are high on average but potentially less discriminating than in contexts where nonprofit brands are less established. This structural characteristic has two implications for the replication exercise.

First, Austrian donors' brand perceptions may be compressed toward positive evaluations for established organisations, producing restricted variance and attenuated correlations — a condition unfavourable to the recovery of fine-grained higher-order factor structures. Second, the emphasis on institutional trust and credibility in Austrian civil-society culture aligns theoretically with the Boenigk–Becker framework's prioritisation of Trust and Commitment over attitudinal facets. The comparative replication allows these theoretical expectations to be evaluated against the data rather than assumed.

No prior Austrian-sample replication of any of the three models exists in published form. The present study therefore constitutes, to the author's knowledge, the first systematic comparative psychometric evaluation of all three nonprofit brand equity frameworks using Austrian donor data.

### 8.3.2 Survey Design and Data Collection

Data were collected via SoSci Survey in 2026 using an online survey administered to Austrian adults with a documented history of charitable giving. The survey employed a **split-design** with within-respondent duplication: each participant evaluated two nonprofit organisations, generating two organisation-level observations per respondent. This within-respondent paired design increases statistical efficiency and allows the detection of respondent-level variance components, but also requires that estimation accounts for the resulting non-independence of observations.

**Dataset structure.** The sample is divided into two subsets corresponding to the two model groups:

- **FC_BO dataset** (Faircloth + Boenigk items): n ≈ 900 organisation-level observations, used for the Faircloth and Boenigk–Becker replications.
- **RO dataset** (Romero items): n ≈ 900 organisation-level observations, used for the Romero replication.

Exact achieved sample sizes and response rates are reported from pipeline outputs: FC_BO n = [PIPELINE: cross_cfa_Faircloth → N]; RO n = [PIPELINE: cross_cfa_Romero → N].

**Outcome variables.** Three behavioural outcome variables are used across all structural models:

| Variable | Label | Coding |
|---|---|---|
| `OF_Spender_bin` | Donor status | Binary: 1 = donated to org in past 12 months, 0 = did not |
| `OF02_01_num_log` | Donation frequency | Log-transformed count of donations to org in past 12 months |
| `OF02_02_num_log` | Donation amount | Log-transformed total amount donated (€) to org in past 12 months |

**Covariate.** Socioeconomic status (`SES_z`) is included as a covariate in all structural models. SES_z is a composite z-standardised index constructed from household income, educational attainment, and occupational prestige. Its inclusion controls for the well-documented positive association between socioeconomic resources and donation propensity, ensuring that brand equity effects are estimated net of economic capacity to give.

### 8.3.3 Missingness and Estimation

Missing data were handled via Full Information Maximum Likelihood (FIML), which recovers unbiased estimates under the assumption of Missing At Random (MAR). All models were estimated using the MLR (Yuan–Bentler robust maximum likelihood) estimator in lavaan 0.6+, which provides standard errors and test statistics robust to non-normality and non-independence. The Satorra–Bentler scaled χ² statistic and robust fit indices (CFI, TLI, RMSEA with confidence intervals, SRMR) are reported throughout. Model comparisons use the Satorra–Bentler scaled difference χ² test where applicable.

---

## 8.4 Analysis Plan

The analysis follows a six-stage protocol, identical across all three models, to ensure comparability:

**Stage 1 — Confirmatory Factor Analysis (CFA).** The full item-level measurement model for each brand equity framework is estimated. Fit indices (CFI, TLI, RMSEA [90% CI], SRMR) are evaluated against the thresholds specified in Chapter 6. Standardised factor loadings, residual variances, and modification indices are inspected.

**Stage 2 — Measurement Quality.** For each first-order factor: McDonald's ω (reliability), Average Variance Extracted (AVE, convergent validity), and HTMT ratios for all factor pairs (discriminant validity). The convergent validity threshold is AVE ≥ .50; the discriminant validity thresholds are HTMT < .85 (strict) or HTMT < .90 (tolerant, where theoretical overlap is expected).

**Stage 3 — Measurement Invariance.** Multi-group measurement invariance is tested across organisation type (`org_type`) using `semTools::measurementInvariance()`. The sequence tests configural → metric → scalar invariance. Invariance is evaluated via ΔCFI (threshold: ≤ .010) and ΔRMSEA (threshold: ≤ .015) following Cheung and Rensvold (2002). Partial invariance is retained where freeing specific intercepts restores acceptable fit.

**Stage 4 — Full Mediation SEM.** The structural model is estimated with all three outcomes as dependent variables, brand equity (at the appropriate order) as the structural predictor, and SES_z as covariate. A **full mediation specification** routes all brand equity effects on outcomes through the mediation layer (IBM/TPB constructs in the BEBA framework; intention in the source models). Path coefficients and total effects are reported.

**Stage 5 — Partial Mediation SEM.** The structural model is re-estimated with direct paths from brand equity to outcomes added alongside mediated paths. The partial mediation specification tests whether brand equity has behavioural effects beyond those channelled through the mediation layer. Comparison of full vs. partial mediation models uses the Satorra–Bentler scaled χ² difference test and change in CFI.

**Stage 6 — Cross-Model Comparison.** Fit indices and key structural coefficients from all three replications are assembled in a comparative table. Model adequacy is evaluated jointly on measurement quality (ω, AVE, HTMT) and structural predictive validity (R² for outcomes, path coefficients to behavioural outcomes).

---

## 8.5 Measurement Results

### 8.5.1 Faircloth (2005) — CFA Results

**CFA global fit.** The six-factor Faircloth measurement model was estimated on the FC_BO dataset (N = [PIPELINE: cross_cfa_Faircloth → N]). Global fit indices:

| Index | Value | Threshold | Evaluation |
|---|---|---|---|
| CFI | [PIPELINE: cross_cfa_Faircloth → CFI] | ≥ .95 | [PIPELINE: cross_cfa_Faircloth → CFI_eval] |
| TLI | [PIPELINE: cross_cfa_Faircloth → TLI] | ≥ .95 | [PIPELINE: cross_cfa_Faircloth → TLI_eval] |
| RMSEA | [PIPELINE: cross_cfa_Faircloth → RMSEA] | ≤ .06 | [PIPELINE: cross_cfa_Faircloth → RMSEA_eval] |
| RMSEA 90% CI | [PIPELINE: cross_cfa_Faircloth → RMSEA_CI] | — | — |
| SRMR | [PIPELINE: cross_cfa_Faircloth → SRMR] | ≤ .08 | [PIPELINE: cross_cfa_Faircloth → SRMR_eval] |
| χ²(df) | [PIPELINE: cross_cfa_Faircloth → chi2_df] | — | — |

**Factor loadings.** All standardised loadings are reported in Table 8.1. Loadings below .50 are flagged for possible exclusion in subsequent models.

*Table 8.1. Faircloth CFA: Standardised factor loadings.*

| Factor | Item | λ (std) | SE | p |
|---|---|---|---|---|
| FC_BI | BI_1 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BI | BI_2 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BI | BI_3 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BP | BP_1 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BP | BP_2 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BP | BP_3 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BS | BS_1 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BS | BS_2 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BD | BD_1 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BD | BD_2 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BF | BF_1 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BF | BF_2 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BR | BR_1 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BR | BR_2 | [PIPELINE] | [PIPELINE] | [PIPELINE] |

**Measurement quality.** Reliability and validity statistics per factor:

*Table 8.2. Faircloth CFA: Measurement quality indices.*

| Factor | Items (n) | McDonald's ω | AVE | Meets ω ≥ .70 | Meets AVE ≥ .50 |
|---|---|---|---|---|---|
| FC_BI | [PIPELINE] | [PIPELINE: cross_cfa_Faircloth → omega_BI] | [PIPELINE: cross_cfa_Faircloth → AVE_BI] | [PIPELINE] | [PIPELINE] |
| FC_BP | [PIPELINE] | [PIPELINE: cross_cfa_Faircloth → omega_BP] | [PIPELINE: cross_cfa_Faircloth → AVE_BP] | [PIPELINE] | [PIPELINE] |
| FC_BS | [PIPELINE] | [PIPELINE: cross_cfa_Faircloth → omega_BS] | [PIPELINE: cross_cfa_Faircloth → AVE_BS] | [PIPELINE] | [PIPELINE] |
| FC_BD | [PIPELINE] | [PIPELINE: cross_cfa_Faircloth → omega_BD] | [PIPELINE: cross_cfa_Faircloth → AVE_BD] | [PIPELINE] | [PIPELINE] |
| FC_BF | [PIPELINE] | [PIPELINE: cross_cfa_Faircloth → omega_BF] | [PIPELINE: cross_cfa_Faircloth → AVE_BF] | [PIPELINE] | [PIPELINE] |
| FC_BR | [PIPELINE] | [PIPELINE: cross_cfa_Faircloth → omega_BR] | [PIPELINE: cross_cfa_Faircloth → AVE_BR] | [PIPELINE] | [PIPELINE] |

**Discriminant validity.** HTMT ratios for all factor pairs:

*Table 8.3. Faircloth CFA: HTMT discriminant validity matrix.*

| | FC_BI | FC_BP | FC_BS | FC_BD | FC_BF | FC_BR |
|---|---|---|---|---|---|---|
| FC_BI | — | | | | | |
| FC_BP | [PIPELINE] | — | | | | |
| FC_BS | [PIPELINE] | [PIPELINE] | — | | | |
| FC_BD | [PIPELINE] | [PIPELINE] | [PIPELINE] | — | | |
| FC_BF | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | — | |
| FC_BR | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | — |

*Note.* HTMT values ≥ .85 are underlined; values ≥ .90 are flagged as indicating inadequate discriminant validity.

**Higher-order structure.** The second-order Brand Attitude and third-order Brand Equity factor loadings are reported as: Brand Attitude ← FC_BI: λ = [PIPELINE: cross_cfa_Faircloth → lambda_BA_BI]; Brand Attitude ← FC_BP: λ = [PIPELINE: cross_cfa_Faircloth → lambda_BA_BP]. Brand Equity ← Brand Attitude: λ = [PIPELINE: cross_cfa_Faircloth → lambda_BE_BA].

### 8.5.2 Boenigk and Becker (2016) — CFA Results

**CFA global fit.** The two-factor Boenigk–Becker measurement model was estimated on the FC_BO dataset (N = [PIPELINE: cross_cfa_Boenigk → N]).

*Table 8.4. Boenigk–Becker CFA: Global fit indices.*

| Index | Value | Threshold | Evaluation |
|---|---|---|---|
| CFI | [PIPELINE: cross_cfa_Boenigk → CFI] | ≥ .95 | [PIPELINE: cross_cfa_Boenigk → CFI_eval] |
| TLI | [PIPELINE: cross_cfa_Boenigk → TLI] | ≥ .95 | [PIPELINE: cross_cfa_Boenigk → TLI_eval] |
| RMSEA | [PIPELINE: cross_cfa_Boenigk → RMSEA] | ≤ .06 | [PIPELINE: cross_cfa_Boenigk → RMSEA_eval] |
| RMSEA 90% CI | [PIPELINE: cross_cfa_Boenigk → RMSEA_CI] | — | — |
| SRMR | [PIPELINE: cross_cfa_Boenigk → SRMR] | ≤ .08 | [PIPELINE: cross_cfa_Boenigk → SRMR_eval] |
| χ²(df) | [PIPELINE: cross_cfa_Boenigk → chi2_df] | — | — |

**Factor loadings.** Standardised loadings for BO_TR and BO_CO items, and higher-order loadings of each factor on the second-order Brand Equity construct:

*Table 8.5. Boenigk–Becker CFA: Standardised factor loadings.*

| Factor | Item | λ (std) | SE | p |
|---|---|---|---|---|
| BO_TR | TR_1 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_TR | TR_2 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_TR | TR_3 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_TR | TR_4 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_CO | CO_1 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_CO | CO_2 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_CO | CO_3 | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_CO | CO_4 | [PIPELINE] | [PIPELINE] | [PIPELINE] |

**Second-order loadings.** BO_BE ← BO_TR: λ = [PIPELINE: cross_cfa_Boenigk → lambda_BE_TR]; BO_BE ← BO_CO: λ = [PIPELINE: cross_cfa_Boenigk → lambda_BE_CO].

**Measurement quality.**

*Table 8.6. Boenigk–Becker CFA: Measurement quality indices.*

| Factor | Items (n) | McDonald's ω | AVE | Meets ω ≥ .70 | Meets AVE ≥ .50 |
|---|---|---|---|---|---|
| BO_TR | [PIPELINE] | [PIPELINE: cross_cfa_Boenigk → omega_TR] | [PIPELINE: cross_cfa_Boenigk → AVE_TR] | [PIPELINE] | [PIPELINE] |
| BO_CO | [PIPELINE] | [PIPELINE: cross_cfa_Boenigk → omega_CO] | [PIPELINE: cross_cfa_Boenigk → AVE_CO] | [PIPELINE] | [PIPELINE] |

**HTMT.** BO_TR ↔ BO_CO: HTMT = [PIPELINE: cross_cfa_Boenigk → HTMT_TR_CO]. Given the theoretically expected overlap between trust and commitment in relational contexts, the tolerant HTMT threshold (< .90) is applied; values approaching or exceeding .90 would indicate that the two constructs share more variance than the second-order structure formally requires.

### 8.5.3 Romero et al. (2023) — CFA Results

**CFA global fit.** The nine-factor Romero measurement model was estimated on the RO dataset (N = [PIPELINE: cross_cfa_Romero → N]).

*Table 8.7. Romero CFA: Global fit indices.*

| Index | Value | Threshold | Evaluation |
|---|---|---|---|
| CFI | [PIPELINE: cross_cfa_Romero → CFI] | ≥ .95 | [PIPELINE: cross_cfa_Romero → CFI_eval] |
| TLI | [PIPELINE: cross_cfa_Romero → TLI] | ≥ .95 | [PIPELINE: cross_cfa_Romero → TLI_eval] |
| RMSEA | [PIPELINE: cross_cfa_Romero → RMSEA] | ≤ .06 | [PIPELINE: cross_cfa_Romero → RMSEA_eval] |
| RMSEA 90% CI | [PIPELINE: cross_cfa_Romero → RMSEA_CI] | — | — |
| SRMR | [PIPELINE: cross_cfa_Romero → SRMR] | ≤ .08 | [PIPELINE: cross_cfa_Romero → SRMR_eval] |
| χ²(df) | [PIPELINE: cross_cfa_Romero → chi2_df] | — | — |

**Factor loadings.** Standardised loadings across all nine first-order factors:

*Table 8.8. Romero CFA: Standardised factor loadings (selected).*

| Factor | Item | λ (std) | SE | p |
|---|---|---|---|---|
| RO_F1 | [PIPELINE: cross_cfa_Romero → item labels F1] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F2 | [PIPELINE: cross_cfa_Romero → item labels F2] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F3 | [PIPELINE: cross_cfa_Romero → item labels F3] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F4 | [PIPELINE: cross_cfa_Romero → item labels F4] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F5 | [PIPELINE: cross_cfa_Romero → item labels F5] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F6 | [PIPELINE: cross_cfa_Romero → item labels F6] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F7 | [PIPELINE: cross_cfa_Romero → item labels F7] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F8 | [PIPELINE: cross_cfa_Romero → item labels F8] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F9 | [PIPELINE: cross_cfa_Romero → item labels F9] | [PIPELINE] | [PIPELINE] | [PIPELINE] |

**Measurement quality.**

*Table 8.9. Romero CFA: Measurement quality indices.*

| Factor | Items (n) | McDonald's ω | AVE | Meets ω ≥ .70 | Meets AVE ≥ .50 |
|---|---|---|---|---|---|
| RO_F1 | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F2 | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F3 | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F4 | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F5 | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F6 | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F7 | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F8 | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_F9 | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |

**Discriminant validity (HTMT matrix, abbreviated).** Given the nine-factor structure, the full 36-entry HTMT matrix is reported in the supplementary pipeline output (`ro_cfa_with_id.rds`). Critical pairs — those theoretically expected to overlap most — are reported here:

*Table 8.10. Romero CFA: HTMT critical pairs.*

| Factor Pair | HTMT | Threshold | Verdict |
|---|---|---|---|
| RO_F[a] ↔ RO_F[b] | [PIPELINE: cross_cfa_Romero → HTMT_critical_1] | .85 | [PIPELINE] |
| RO_F[c] ↔ RO_F[d] | [PIPELINE: cross_cfa_Romero → HTMT_critical_2] | .85 | [PIPELINE] |
| RO_F[e] ↔ RO_F[f] | [PIPELINE: cross_cfa_Romero → HTMT_critical_3] | .85 | [PIPELINE] |

*Note.* Full HTMT matrix available from pipeline object `ro_cfa_with_id.rds`. Pairs identified in the ConstructLedger as theoretically overlapping apply the tolerant threshold of .90.

---

## 8.6 Structural Results

### 8.6.1 Faircloth (2005) — Structural Paths and Mediation

**Full mediation model.** The full mediation specification routes all brand equity effects on behavioural outcomes through a single Brand Attitude pathway. Results from `cross_med_full_Faircloth.rds`:

*Table 8.11. Faircloth full mediation: Standardised path coefficients.*

| Path | β (std) | SE | p | 95% CI |
|---|---|---|---|---|
| FC_BE → Donation status | [PIPELINE: Faircloth full mediation → β_BE_donstat] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BE → Donation frequency | [PIPELINE: Faircloth full mediation → β_BE_donfreq] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BE → Donation amount | [PIPELINE: Faircloth full mediation → β_BE_donamnt] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| SES_z → Donation status | [PIPELINE: Faircloth full mediation → β_SES_donstat] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| SES_z → Donation frequency | [PIPELINE: Faircloth full mediation → β_SES_donfreq] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| SES_z → Donation amount | [PIPELINE: Faircloth full mediation → β_SES_donamnt] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Model R² (donation status) | [PIPELINE] | — | — | — |
| Model R² (donation freq) | [PIPELINE] | — | — | — |
| Model R² (donation amount) | [PIPELINE] | — | — | — |

**Partial mediation model.** Adding direct paths from FC_BE to each outcome. Results from `cross_med_partial_Faircloth.rds`:

*Table 8.12. Faircloth partial mediation: Direct and indirect effects.*

| Path | Effect type | β (std) | SE | p |
|---|---|---|---|---|
| FC_BE → Donation status (direct) | Direct | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BE → Donation status (indirect) | Indirect | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BE → Donation frequency (direct) | Direct | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BE → Donation frequency (indirect) | Indirect | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BE → Donation amount (direct) | Direct | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| FC_BE → Donation amount (indirect) | Indirect | [PIPELINE] | [PIPELINE] | [PIPELINE] |

**Full vs. partial mediation model comparison (Faircloth):**

| Criterion | Full mediation | Partial mediation | ΔCFI | Δχ²(Δdf) | p(Δχ²) |
|---|---|---|---|---|---|
| CFI | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RMSEA | [PIPELINE] | [PIPELINE] | — | — | — |
| Preferred model | [PIPELINE: Faircloth → preferred_mediation_model] | | | | |

### 8.6.2 Boenigk and Becker (2016) — Structural Paths and Mediation

**Full mediation model.** Results from `cross_med_full_Boenigk.rds`:

*Table 8.13. Boenigk–Becker full mediation: Standardised path coefficients.*

| Path | β (std) | SE | p | 95% CI |
|---|---|---|---|---|
| BO_BE → Donation status | [PIPELINE: Boenigk full mediation → β_BE_donstat] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_BE → Donation frequency | [PIPELINE: Boenigk full mediation → β_BE_donfreq] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_BE → Donation amount | [PIPELINE: Boenigk full mediation → β_BE_donamnt] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| SES_z → Donation status | [PIPELINE: Boenigk full mediation → β_SES_donstat] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| SES_z → Donation frequency | [PIPELINE: Boenigk full mediation → β_SES_donfreq] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| SES_z → Donation amount | [PIPELINE: Boenigk full mediation → β_SES_donamnt] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Model R² (donation status) | [PIPELINE] | — | — | — |
| Model R² (donation freq) | [PIPELINE] | — | — | — |
| Model R² (donation amount) | [PIPELINE] | — | — | — |

**Partial mediation model.** Results from `cross_med_partial_Boenigk.rds`:

*Table 8.14. Boenigk–Becker partial mediation: Direct and indirect effects.*

| Path | Effect type | β (std) | SE | p |
|---|---|---|---|---|
| BO_BE → Donation status (direct) | Direct | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_BE → Donation status (indirect) | Indirect | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_BE → Donation frequency (direct) | Direct | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_BE → Donation frequency (indirect) | Indirect | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_BE → Donation amount (direct) | Direct | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| BO_BE → Donation amount (indirect) | Indirect | [PIPELINE] | [PIPELINE] | [PIPELINE] |

**Full vs. partial mediation model comparison (Boenigk–Becker):**

| Criterion | Full mediation | Partial mediation | ΔCFI | Δχ²(Δdf) | p(Δχ²) |
|---|---|---|---|---|---|
| CFI | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RMSEA | [PIPELINE] | [PIPELINE] | — | — | — |
| Preferred model | [PIPELINE: Boenigk → preferred_mediation_model] | | | | |

### 8.6.3 Romero et al. (2023) — Structural Paths and Mediation

**Full mediation model.** Results from `ro_mediation_full.rds`:

*Table 8.15. Romero full mediation: Standardised path coefficients.*

| Path | β (std) | SE | p | 95% CI |
|---|---|---|---|---|
| RO_BE → Donation status | [PIPELINE: Romero full mediation → β_BE_donstat] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_BE → Donation frequency | [PIPELINE: Romero full mediation → β_BE_donfreq] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_BE → Donation amount | [PIPELINE: Romero full mediation → β_BE_donamnt] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| SES_z → Donation status | [PIPELINE: Romero full mediation → β_SES_donstat] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| SES_z → Donation frequency | [PIPELINE: Romero full mediation → β_SES_donfreq] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| SES_z → Donation amount | [PIPELINE: Romero full mediation → β_SES_donamnt] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Model R² (donation status) | [PIPELINE] | — | — | — |
| Model R² (donation freq) | [PIPELINE] | — | — | — |
| Model R² (donation amount) | [PIPELINE] | — | — | — |

**Partial mediation model.** Results from `ro_mediation_partial.rds`:

*Table 8.16. Romero partial mediation: Direct and indirect effects.*

| Path | Effect type | β (std) | SE | p |
|---|---|---|---|---|
| RO_BE → Donation status (direct) | Direct | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_BE → Donation status (indirect) | Indirect | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_BE → Donation frequency (direct) | Direct | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_BE → Donation frequency (indirect) | Indirect | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_BE → Donation amount (direct) | Direct | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RO_BE → Donation amount (indirect) | Indirect | [PIPELINE] | [PIPELINE] | [PIPELINE] |

**Full vs. partial mediation model comparison (Romero):**

| Criterion | Full mediation | Partial mediation | ΔCFI | Δχ²(Δdf) | p(Δχ²) |
|---|---|---|---|---|---|
| CFI | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| RMSEA | [PIPELINE] | [PIPELINE] | — | — | — |
| Preferred model | [PIPELINE: Romero → preferred_mediation_model] | | | | |

---

## 8.7 Measurement Invariance Results

Measurement invariance was tested across organisation type (`org_type`) for all three models using `semTools::measurementInvariance()`. The sequence configural → metric → scalar is reported for each. Invariance conclusions use ΔCFI ≤ .010 and ΔRMSEA ≤ .015 as primary criteria, with likelihood ratio tests as secondary criteria.

*Table 8.17. Measurement invariance results across organisation type.*

| Model | Invariance Level | CFI | ΔCFI | RMSEA | ΔRMSEA | χ²(df) | Δχ²(Δdf) | p | Verdict |
|---|---|---|---|---|---|---|---|---|---|
| Faircloth | Configural | [PIPELINE: Faircloth MI → CFI_config] | — | [PIPELINE] | — | [PIPELINE] | — | — | — |
| Faircloth | Metric | [PIPELINE: Faircloth MI → CFI_metric] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Faircloth | Scalar | [PIPELINE: Faircloth MI → CFI_scalar] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Boenigk–Becker | Configural | [PIPELINE: Boenigk MI → CFI_config] | — | [PIPELINE] | — | [PIPELINE] | — | — | — |
| Boenigk–Becker | Metric | [PIPELINE: Boenigk MI → CFI_metric] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Boenigk–Becker | Scalar | [PIPELINE: Boenigk MI → CFI_scalar] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Romero | Configural | [PIPELINE: Romero MI → CFI_config] | — | [PIPELINE] | — | [PIPELINE] | — | — | — |
| Romero | Metric | [PIPELINE: Romero MI → CFI_metric] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Romero | Scalar | [PIPELINE: Romero MI → CFI_scalar] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] | [PIPELINE] |

*Note.* Where scalar invariance fails (ΔCFI > .010), partial scalar invariance is evaluated by freeing non-invariant intercepts. Items with non-invariant intercepts are identified and theoretically interpreted: systematic intercept differences across organisation types indicate that donors apply systematically different absolute response scales to a brand equity dimension depending on the type of organisation evaluated, which would constrain cross-group mean comparisons but not cross-group path coefficient comparisons.

**Implications.** The level of invariance achieved for each model determines which cross-group comparisons are permissible. Models achieving at minimum metric invariance permit comparison of latent covariances and path coefficients across organisation types. Models achieving full scalar invariance additionally permit comparison of latent means.

---

## 8.8 Cross-Model Comparison

The three models are now compared on the full set of psychometric and structural criteria. This comparison is the direct empirical basis for the model selection decision that informs the BEBA architecture in Chapter 10.

*Table 8.18. Cross-model comparison: Global CFA fit indices.*

| Criterion | Faircloth (2005) | Boenigk–Becker (2016) | Romero et al. (2023) |
|---|---|---|---|
| Dataset | FC_BO | FC_BO | RO |
| N | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| First-order factors | 6 | 2 | 9 |
| Higher-order level | 3rd order | 2nd order | 3rd order |
| CFI | [PIPELINE: cross_cfa_Faircloth → CFI] | [PIPELINE: cross_cfa_Boenigk → CFI] | [PIPELINE: cross_cfa_Romero → CFI] |
| TLI | [PIPELINE: cross_cfa_Faircloth → TLI] | [PIPELINE: cross_cfa_Boenigk → TLI] | [PIPELINE: cross_cfa_Romero → TLI] |
| RMSEA | [PIPELINE: cross_cfa_Faircloth → RMSEA] | [PIPELINE: cross_cfa_Boenigk → RMSEA] | [PIPELINE: cross_cfa_Romero → RMSEA] |
| SRMR | [PIPELINE: cross_cfa_Faircloth → SRMR] | [PIPELINE: cross_cfa_Boenigk → SRMR] | [PIPELINE: cross_cfa_Romero → SRMR] |
| Min. ω across factors | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Min. AVE across factors | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Max. HTMT across pairs | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| HTMT violations (> .85) | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Measurement invariance | [PIPELINE: Faircloth → MI_level] | [PIPELINE: Boenigk → MI_level] | [PIPELINE: Romero → MI_level] |

*Table 8.19. Cross-model comparison: Structural predictive validity.*

| Criterion | Faircloth | Boenigk–Becker | Romero |
|---|---|---|---|
| β*(BE → donation status) | [PIPELINE: Faircloth → β_donstat] | [PIPELINE: Boenigk → β_donstat] | [PIPELINE: Romero → β_donstat] |
| β*(BE → donation freq) | [PIPELINE: Faircloth → β_donfreq] | [PIPELINE: Boenigk → β_donfreq] | [PIPELINE: Romero → β_donfreq] |
| β*(BE → donation amount) | [PIPELINE: Faircloth → β_donamnt] | [PIPELINE: Boenigk → β_donamnt] | [PIPELINE: Romero → β_donamnt] |
| R² (donation status) | [PIPELINE: Faircloth → R2_donstat] | [PIPELINE: Boenigk → R2_donstat] | [PIPELINE: Romero → R2_donstat] |
| R² (donation freq) | [PIPELINE: Faircloth → R2_donfreq] | [PIPELINE: Boenigk → R2_donfreq] | [PIPELINE: Romero → R2_donfreq] |
| R² (donation amount) | [PIPELINE: Faircloth → R2_donamnt] | [PIPELINE: Boenigk → R2_donamnt] | [PIPELINE: Romero → R2_donamnt] |
| Preferred mediation spec. | [PIPELINE: Faircloth → pref_med] | [PIPELINE: Boenigk → pref_med] | [PIPELINE: Romero → pref_med] |

*Table 8.20. Summary evaluation matrix: Overall verdict per model.*

| Evaluation dimension | Faircloth (2005) | Boenigk–Becker (2016) | Romero et al. (2023) |
|---|---|---|---|
| CFA global fit | [PIPELINE: overall rating] | [PIPELINE: overall rating] | [PIPELINE: overall rating] |
| Factor reliability (ω) | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Convergent validity (AVE) | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Discriminant validity (HTMT) | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Higher-order structure feasibility | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Measurement invariance level | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Structural predictive validity | [PIPELINE] | [PIPELINE] | [PIPELINE] |
| Parsimony | Moderate | High | Low |
| **Overall recommendation** | [PIPELINE: Faircloth → overall] | [PIPELINE: Boenigk → overall] | [PIPELINE: Romero → overall] |

---

## 8.9 Discussion

### 8.9.1 Which Model Architecture Is Most Tenable in the Austrian Context?

The comparative evidence assembled in Section 8.8 addresses a question that is prior to the BEBA hypothesis: which of the three existing model architectures provides the most defensible psychometric and structural foundation for nonprofit brand equity research in the Austrian donor context?

The answer must be read on two dimensions simultaneously: measurement quality (which model produces a valid and reliable measurement structure) and structural predictive validity (which brand equity operationalisation is most predictive of actual donation behaviour). A model that fits the data well at the measurement level but fails to predict behaviour is theoretically incomplete; a model that predicts behaviour but rests on a psychometrically inadequate measurement structure is epistemically problematic, since observed predictions may be an artefact of over-extracted common variance.

**Faircloth (2005).** The six-factor third-order structure tests whether Austrian donors differentiate among the attitudinal facets of brand equity that Faircloth's framework requires. The theoretical expectation, stated in Section 8.2.1, was that the structure might partially collapse under Austrian conditions: high baseline trust in established charity brands and compressed positive evaluations across organisations could reduce the variance in dimensionally specific ratings necessary for the six-factor structure to discriminate cleanly. Whether this expectation is borne out depends on the HTMT values in Table 8.3 and the global fit in Table 8.1. The attitudinal pathway — Brand Image and Brand Personality → Brand Attitude → Equity → Behaviour — is theoretically coherent but represents a relatively indirect mechanism: the model hypothesises that symbolic and evaluative dimensions of brand perception aggregate upward through attitude to generate behavioural effects. If the predictive validity in Table 8.19 is weak relative to the Boenigk–Becker model, this suggests that the attitudinal-facet architecture fails to capture the primary behavioural mechanism in the Austrian charitable context.[^NB-000102]

**Boenigk and Becker (2016).** The Trust–Commitment framework is theoretically aligned with the Austrian charitable giving context: it foregrounds exactly the dimensions — reliance and attachment under informational uncertainty — that Chapter 2 identified as critical for credence-good decisions. If the measurement structure performs well (Table 8.4, 8.5, 8.6) and the structural coefficients in Table 8.13 and 8.14 are consistent and interpretable, the Boenigk–Becker model would represent the most parsimonious tenable architecture. Its two-factor, second-order structure also minimises discriminant validity pressure relative to the six- and nine-factor alternatives, which reduces the risk of measurement artefacts inflating apparent structural effects.[^NB-000103] A critical interpretive question for this model is whether the Trust and Commitment dimensions carry differential predictive weight for the three outcome types: trust may be more strongly associated with donor status (the initial decision to engage) and commitment with donation frequency and amount (ongoing relational behaviour).

**Romero et al. (2023).** The nine-factor third-order structure provides the richest theoretical vocabulary for nonprofit brand equity, but also the most demanding empirical requirements. If significant HTMT violations are detected (Table 8.10) — that is, if Austrian donors do not differentiate among multiple of the nine proposed dimensions — the model is not merely a poor fit; it is theoretically inappropriate as a measurement structure for this population. Dimension collapse would imply that the conceptual distinctions drawn in the Romero framework, however theoretically defensible in the Spanish context, do not map onto distinct psychological constructs as perceived by Austrian donors. This is a substantive finding, not merely a psychometric limitation: it speaks to the cultural and contextual transportability of nonprofit brand equity constructs.[^CB-000020]

### 8.9.2 Implications for the Mediation Architecture

The mediation comparison (Tables 8.11–8.16) addresses a question that is theoretically central to the BEBA programme: does brand equity produce behavioural effects directly, or does it operate through an intermediate psychological layer? The full mediation specification is theoretically preferred by the BEBA framework, which proposes that brand equity functions as a distal antecedent whose effects on donation behaviour are channelled through intentional processes (attitude formation, norm internalisation, perceived control, knowledge activation — the IBM/TPB layer). If partial mediation is uniformly preferred across all three source models, this would suggest that brand equity has behavioural effects that are not explained by its effects on the intentional layer, which would either imply that the mediation layer in the source models is misspecified or that there exist additional causal pathways not captured by a pure intention-mediated account.

The pattern of direct vs. indirect effects across the three outcomes is particularly informative. Donation status (binary, reflecting any giving at all) may be most sensitive to attitude and intention; donation frequency (reflecting habitual engagement) may be more sensitive to commitment and relational constructs; donation amount (reflecting resource allocation) may depend on SES_z more heavily than on brand equity. Cross-model consistency of these patterns would strengthen the substantive interpretation; inconsistency would suggest model-specific mediation architectures.[^CB-000021]

### 8.9.3 What This Implies for Chapter 10

The triple replication establishes three inputs for the BEBA model in Chapter 10. First, it identifies the **most psychometrically adequate brand equity operationalisation** for use in the Austrian context: whichever model performs best on the criteria in Table 8.20 provides the measurement template that the BEBA empirical model should incorporate or build upon. Second, it identifies the **structural limitations** of existing frameworks — particularly, any consistent failure to predict donation frequency and amount — that the BEBA architecture attempts to address by explicitly incorporating IBM/TPB intentional mechanisms as a mediating layer between brand signals and behavioural enactment. Third, it establishes the **measurement invariance baseline**: if existing models already achieve metric or scalar invariance across organisation types, the BEBA model must do at least as well; if they do not, partial invariance findings serve as contextual benchmarks for the more complex BEBA structure.

Critically, the triple replication does not select a "winner" in the sense of a model to be adopted in Chapter 10. None of the three frameworks was designed to integrate brand equity with IBM/TPB intention processes. The BEBA model in Chapter 10 is not a selection among these three — it is a theoretical extension that draws on the relational constructs most supported by the replication evidence (likely Trust and Commitment, given the Austrian context) while adding the motivational and enactment mechanisms that none of the three source models contains. The present chapter's function is therefore to establish the brand equity floor: the psychometric minimum and the structural baseline against which the BEBA model's added explanatory value will be benchmarked in Chapter 10.

---

## 8.10 Chapter Summary

Chapter 8 executed a triple replication of the three leading nonprofit brand equity model architectures — Faircloth (2005), Boenigk and Becker (2016), and Romero et al. (2023) — on Austrian donor data collected via split-design online survey in 2026. All models were estimated using the MLR estimator with FIML missing data handling in lavaan 0.6+, with identical fit thresholds and validity criteria applied across replications.

The psychometric evaluation assessed CFA global fit, factor reliability (McDonald's ω), convergent validity (AVE), and discriminant validity (HTMT) for each model. The structural evaluation tested full and partial mediation specifications across three behavioural outcomes — donor status, donation frequency, and donation amount — with SES_z as a socioeconomic covariate. Measurement invariance was tested across organisation type using semTools::measurementInvariance().

The comparative analysis in Section 8.8 identified [PIPELINE: cross-model summary → preferred model] as providing the most defensible psychometric foundation under Austrian donor conditions, while [PIPELINE: cross-model summary → structural finding for preferred model] with respect to structural predictive validity. Key limitations identified in the replication — including [PIPELINE: summary of discriminant validity failures or collapsed dimensions] — motivate the revised construct architecture developed in the BEBA model (Chapter 10), which integrates the most psychometrically robust brand equity constructs with the IBM/TPB intentional pathway not present in any of the three source frameworks.

---

## Footnotes

[^NB-000102]: The theoretical justification for treating Faircloth (2005), Boenigk and Becker (2016)/Boenigk and Helmig (2013), and Romero et al. (2023) as the canonical replication targets follows from BEBA knowledge object NB-000102, which registers the evidence weight for each framework in the nonprofit brand equity literature and their relative representativeness of distinct theoretical traditions (attitudinal-facet, relational-institutional, and comprehensive-multidimensional, respectively).

[^NB-000103]: The decision to apply MLR/FIML estimation uniformly across all three replications is grounded in BEBA knowledge object NB-000103, which specifies the estimation standards for the BEBA empirical programme. MLR is preferred over ordinary ML because the item distributions in nonprofit brand equity surveys systematically depart from multivariate normality (positive skew, ceiling effects for established brands), and FIML is preferred over listwise or pairwise deletion because the missing-at-random assumption is more defensible than the missing-completely-at-random assumption required for listwise deletion.

[^CB-000020]: The theoretical claim that cultural and contextual transportability of brand equity constructs cannot be assumed without empirical testing is anchored in BEBA knowledge object CB-000020, which synthesises the cross-national and cross-sector evidence on nonprofit brand equity measurement. CB-000020 specifically flags the Spanish → Austrian transport as a theoretically non-trivial test case, given differences in civil-society structure, donation culture, and regulatory environment.

[^CB-000021]: The mediation architecture — specifically, the theoretical argument for full vs. partial mediation of brand equity effects on donation behaviour — is developed in BEBA knowledge object CB-000021, which maps the evidence from IBM and TPB studies on charitable giving that support an intentional mediation layer between brand-level cognitions and behavioural enactment. CB-000021 distinguishes between the predictive mediation logic of source-model intention constructs and the mechanistic mediation logic of the IBM/TPB architecture adopted in the BEBA framework.
