---
title: "Chapter 6 — Measurement Theory, Psychometrics, and Latent Variables"
status: draft
object_type: Chapter
layer: Organisational / Individual
claim_anchors:
  - NB-000101
  - NB-000102
  - NB-000103
  - NB-000104
  - NB-000105
  - CB-000020
  - CB-000021
  - BA-000067
  - BL-000009
  - BI-000006
  - BP-000002
  - BA-000002
  - BT-000001
  - BT-000002
  - BC-000001
  - SC-000001
reviews: [REVIEW-000006, REVIEW-000058, REVIEW-000100]
---

# Chapter 6 — Measurement Theory, Psychometrics, and Latent Variables

## Scientific Question

Why must brand equity, trust, commitment, intention, and similar constructs be understood as latent variables and subjected to formal psychometric validation — and what does this require from the measurement architecture of the BEBA empirical programme?

---

## 6.1 The Measurement Problem in Brand Research

Brand equity, trust, donor commitment, and behavioural intention are not directly observable. They are hypothetical constructs — theoretical entities postulated to explain patterns in observable behaviour and self-report. A donor cannot be asked to point to their "brand trust" in the same way they can be asked to report their last donation amount. The construct must be inferred from a set of indicators — questionnaire items, behavioural records, or experimental responses — that are assumed to reflect the underlying theoretical entity.

This inference is the **measurement problem** in brand and behaviour research. It has two components:

1. **Ontological:** What kind of entity is "brand trust"? Is it a stable psychological property that causes observable responses? A formative aggregate of distinct components that together define the concept? Or a network of causally interrelated perceptions with no single underlying factor?

2. **Epistemic:** Given that the construct cannot be directly observed, how can we be confident that our indicators capture it — and not some other construct, some artefact of the measurement method, or some combination of both?

Failure to address these questions produces what Cronbach and Meehl (1955) called **construct invalidity**: the systematic error of believing we have measured a theoretically important construct when we have in fact measured something else. In brand equity research, construct invalidity is endemic — it is one of the primary reasons why effect size estimates differ dramatically across studies that nominally measure "the same" constructs.[^6-NB-000102]

---

## 6.2 What Is a Latent Variable?

A **latent variable** is an unobservable variable whose existence is inferred from its systematic effects on observable variables (the indicators or manifest variables). The key assumption is the **local independence assumption**: given the latent variable's value, the observed indicators are statistically independent of each other. All covariation among indicators is explained by their shared dependence on the latent factor.

This assumption has a strong theoretical implication: the latent variable is the *cause* of the indicator values, not the other way around. When a donor has high brand trust, they respond positively to items like "I trust this organisation to use my donation effectively" and "This organisation is honest and transparent" because the underlying trust state causes both responses. The indicators are effects of the construct, not its components.

This is the **reflective model** assumption — and it is the appropriate measurement model for constructs that represent psychological states or dispositions: trust, attitude, intention, commitment. In reflective models, all indicators should be:
- Positively and substantially correlated with each other.
- Approximately interchangeable (removing one indicator should not change the construct's meaning).
- Caused by the latent factor (the direction of causality runs from construct to indicator).

---

## 6.3 Reflective vs. Formative Models: A Critical Distinction

Not all brand equity constructs are appropriately modelled as reflective latent variables. The distinction between **reflective** and **formative** measurement models is consequential for the entire measurement architecture.[^6-fn-rfmodel]

**Reflective models** (discussed above) assume that the construct causes the indicators. Appropriate for psychological states and dispositions: attitude, trust, commitment, intention.

**Formative models** assume that the indicators *cause* or *constitute* the construct. The indicators are defining components, not effects. Removing one indicator changes the construct's meaning because that component is now absent. Appropriate for composite indices where the components are definitionally enumerated: socioeconomic status (education + income + occupational prestige), or a nonprofit's "fundraising portfolio" (number of channels + frequency + reach).

The error of treating a formative construct as reflective (or vice versa) produces systematic parameter bias, distorted reliability estimates, and misleading factor structures (Jarvis et al., 2003). In nonprofit brand equity research, this error is common: brand equity is sometimes treated as a reflective higher-order construct (a latent variable that causes its dimensions) and sometimes as a formative composite (the weighted aggregate of its dimensions). The two specifications are not equivalent — they test different theoretical claims and require different analytic approaches.[^6-NB-000102]

The BEBA project adopts the following default specification, subject to revision via ADR:

| Construct | Measurement Model | Justification |
|---|---|---|
| Brand Awareness | Reflective | Recall and recognition items caused by awareness state |
| Brand Image | Reflective | Evaluative associations caused by image representation |
| Brand Trust | Reflective | Trust belief items caused by underlying trust disposition |
| Brand Commitment | Reflective | Commitment items caused by relational attachment |
| Brand Personality | Reflective | Personality attributions caused by brand personality perception |
| Overall Brand Equity | Formative (second-order) | Defined by its dimensional components; removing a dimension changes what is meant |
| Donation Intention | Reflective | Intention items caused by motivational state |
| Donation Behaviour | Formative (index) | Frequency × amount index; definitional |

The second-order specification for Brand Equity is particularly important: a second-order reflective model (all first-order dimensions caused by a general brand equity factor) tests a different theoretical claim than a second-order formative model (the general brand equity construct is constituted by its dimensions). Yoo and Donthu's (2001) widely used CBBE scale implicitly assumes a first-order reflective structure; Keller's (1993) Brand Knowledge Model and Chatzipanagiotou et al.'s (2019) configural model are more compatible with second-order formative or network representations.[^6-CB-000020]

---

## 6.4 Validity and Its Components

A measurement instrument has **validity** to the degree that it measures what it claims to measure. Classical measurement theory decomposes validity into multiple components, each assessed by different empirical procedures (Messick, 1995).

### 6.4.1 Content Validity

The item pool covers the full conceptual domain of the construct without including items from adjacent constructs. Content validity is assessed through expert review and systematic comparison with existing definitions — in the BEBA project, against the **ConstructLedger** definitions and the formal ontology. Every item proposed for the BEBA survey instrument must be traceable to a specific construct definition in the ConstructLedger.[^6-fn-constructledger]

### 6.4.2 Convergent Validity

Indicators of the same construct should share substantial common variance. Operationally, convergent validity is assessed through:

- **Average Variance Extracted (AVE):** The proportion of variance in the indicators captured by the latent factor. AVE > 0.50 indicates that the factor captures more variance than measurement error (Fornell & Larcker, 1981).
- **Factor loadings:** Standardised loadings should generally exceed 0.70, indicating that items are better explained by the factor than by measurement error.
- **Composite Reliability (CR):** A more appropriate reliability coefficient than Cronbach's alpha for confirmatory models (see Section 6.5). CR > 0.70 is the conventional threshold.

### 6.4.3 Discriminant Validity

Different constructs should be empirically distinguishable. The classical criterion (Fornell & Larcker, 1981) requires that the AVE for each construct exceeds the squared correlation between that construct and any other construct in the model. The more conservative **HTMT criterion** (Heterotrait-Monotrait ratio) requires that the average inter-construct item correlation is substantially below the average within-construct item correlation (Henseler et al., 2015).

Discriminant validity is a particular concern for the BEBA measurement model because several constructs are theoretically adjacent: brand trust and brand commitment share relational content; brand image and brand personality both concern symbolic meaning; attitude toward donating and donation intention are psychologically proximal. The measurement model must demonstrate that these constructs remain empirically separable despite their conceptual proximity.[^6-NB-000103]

### 6.4.4 Nomological Validity

Constructs behave in theoretically expected ways in their network of relationships. In the BEBA measurement validation, nomological validity is assessed by checking that:
- Brand trust predicts donation intention more strongly than brand awareness.
- Brand image predicts attitude more strongly than perceived behavioural control.
- These patterns hold across subsamples (see Section 6.6 on measurement invariance).

Nomological validity is assessed within the structural model (Chapter 7) rather than the measurement model, but the measurement model must be sound before nomological validity can be meaningfully evaluated.

---

## 6.5 Reliability: Cronbach's Alpha and Its Limitations

**Cronbach's alpha** (α) is the most widely reported reliability coefficient in social science research. It estimates the proportion of observed score variance attributable to the true score by computing the ratio of inter-item covariances to total item variance. The conventional threshold of α > 0.70 is applied mechanically across most research contexts.

Alpha has several important limitations that motivate the use of alternative reliability estimates in the BEBA measurement model:

**1. Alpha assumes essentially tau-equivalent measurement** — that all items have equal factor loadings. In practice, items differ in their loading strength, and alpha underestimates reliability when items have unequal loadings and overestimates it when the scale has many items (regardless of their individual quality). For the BEBA scales, which are adapted from existing instruments and likely to have heterogeneous item quality, this assumption is implausible.

**2. Alpha is sensitive to the number of items.** Adding more items to a scale always increases alpha, even if the additional items add no construct-relevant information. This creates an incentive to use longer scales than theoretically necessary.

**3. Alpha is not a measure of unidimensionality.** A high alpha value is consistent with a multidimensional scale — the common misconception that high alpha implies a single underlying factor is false (Sijtsma, 2009).

The BEBA measurement model uses **Composite Reliability (CR)** and **omega coefficients** ($\omega$) as primary reliability estimates, supplemented by alpha for comparability with the existing literature. CR appropriately accommodates unequal factor loadings; omega additionally accounts for the distinction between the general factor and specific factors in hierarchical models.[^6-fn-omega]

---

## 6.6 Measurement Invariance: The Hidden Assumption in Group Comparisons

A foundational but frequently overlooked requirement for valid cross-group comparisons is **measurement invariance**: the assurance that measurement instruments function identically across the groups being compared (Horn & McArdle, 1992; Vandenberg & Lance, 2000).

If Brand Trust items carry different meanings for male versus female donors, or if a Trust scale has different factor loadings for high-income versus low-income respondents, then observed differences between groups on the latent Trust variable may reflect differences in how the construct is measured rather than differences in actual trust levels. Comparing group means without testing measurement invariance is analogous to comparing temperatures measured on Celsius and Fahrenheit scales without converting units.

**The BEBA evidence base explicitly documents this problem.** Claim NB-000103 states: "A single brand equity measurement model is not invariant across stakeholder groups (donors, volunteers, etc.)" — a finding that directly challenges the common practice in nonprofit brand equity research of using a single scale across heterogeneous populations.[^6-NB-000103]

The **measurement invariance testing sequence** in BEBA follows the established hierarchy:

| Step | Model | What is constrained | If rejected |
|---|---|---|---|
| 1 | Configural | Factor structure only (same items per factor) | Cannot proceed to CFA |
| 2 | Metric | Factor loadings equal across groups | Only partial metric invariance; no latent mean comparison |
| 3 | Scalar | Loadings + intercepts equal across groups | Only partial scalar invariance; latent mean comparison may still be possible |
| 4 | Strict | Loadings + intercepts + residuals equal | Rarely required; useful for longitudinal comparisons |

**Partial invariance** — where some but not all loadings or intercepts are group-invariant — permits limited comparisons and is theoretically informative: non-invariant items indicate that specific aspects of the construct are understood differently across groups. This information feeds directly into the BEBA theoretical architecture, potentially supporting stakeholder-group-specific model specifications.[^6-fn-MI]

---

## 6.7 Common Method Bias and Design Remedies

**Common method bias** (CMB) refers to the artificial covariance induced when the same method is used to measure both predictor and outcome constructs. In survey-based research — the primary data collection method for the BEBA empirical programme — both brand equity perceptions and donation intentions are measured via self-report, creating a methodological confound: shared questionnaire variance, social desirability pressure, and implicit theories about the expected relationships can all artificially inflate observed correlations (Podsakoff et al., 2003).

Claim NB-000101 explicitly identifies this problem: "Causal claims from cross-sectional survey data are likely inflated by common method bias."[^6-NB-000101] This is not a minor qualification — in the charitable giving literature, inflated cross-sectional correlations have contributed to the non-replication problem documented in Chapter 5: effect sizes estimated in single-survey studies are systematically larger than effect sizes recovered in multi-wave or experimental designs.

The BEBA empirical programme addresses CMB through a combination of design and analytic remedies:

**Design remedies:**
- **Temporal separation:** Predictor constructs (brand perceptions) measured at time 1; outcome constructs (donation intention, behaviour) measured at time 2 (minimum two weeks later).
- **Item ordering:** Brand perception items placed after donation history items to reduce priming effects.
- **Scale variation:** Multiple response formats used (Likert, semantic differential, frequency) to break method-induced covariance patterns.

**Analytic remedies:**
- **Harman's single-factor test:** Performed as a baseline check (not as the primary CMB assessment).
- **Marker variable technique:** An unmeasured latent marker variable is added to the CFA to absorb shared method variance (Richardson et al., 2009).
- **CFA-CMV model comparison:** A model with a common latent method factor is compared to the substantive model using the likelihood comparison framework from Chapter 5.

---

## 6.8 Scale Adaptation: Existing Instruments in the BEBA Context

The BEBA empirical programme does not develop new measurement scales from scratch. Instead, it **adapts existing validated scales** to the nonprofit donation context, following the established procedure: select scale, adapt item wording to the target context, pilot-test with the target population, conduct CFA to verify factor structure, assess measurement invariance before cross-group comparison.

The existing scales for the BEBA construct set derive from the following sources:

| Construct | Primary Source Scale | Adaptation Notes |
|---|---|---|
| Brand Awareness | Yoo & Donthu (2001); Pappu et al. (2005) | Adapt to nonprofit: "I am aware of what this organisation does" |
| Brand Image | Faircloth (2005) nonprofit adaptation | Direct application; context-specific images may require additional items |
| Brand Trust | Boenigk & Becker (2016); Sargeant & Lee (2004) | Nonprofit-specific trust scale; integrity, benevolence, competence subscales |
| Brand Commitment | Boenigk & Becker (2016) | Attitudinal commitment in nonprofit context |
| Brand Personality | Aaker (1997) adapted for nonprofits | Sincerity and Competence dimensions primarily relevant |
| Donation Intention | Romero et al. (2023) DBBE scale | Willingness to donate, intent to continue, intent to recommend |
| Attitude | Ajzen (2002) TPB attitude scale | Evaluate donating on a series of evaluative bipolar adjectives |
| Subjective Norms | Ajzen (2002) | "Most people important to me think I should donate to this organisation" |
| PBC | Ajzen (2002) | Perceived ability, ease, and control over donation decision |

**Claim CB-000020** establishes that Consumer-Based Brand Equity is a higher-order construct with four dimensions (Brand Awareness, Brand Associations, Perceived Quality, Brand Loyalty).[^6-CB-000020] The BEBA adaptation retains the higher-order structure but replaces "Perceived Quality" with "Perceived Impact Quality" (reflecting the nonprofit's inability to price-signal service quality) and integrates Brand Trust and Brand Commitment as distinct constructs rather than collapsing them under Brand Loyalty.[^6-CB-000021]

The empirical consequence of this adaptation decision is directly testable: if the commercial CBBE four-factor structure (Model A) provides equivalent fit to the nonprofit-adapted structure (Model B) in an Austrian donor sample, the commercial translation is justified. If the nonprofit-specific constructs improve fit and discriminant validity, the adaptation is warranted. This comparison is a specific instance of the model competition programme from Chapter 5.

---

## 6.9 The ConstructLedger as Measurement Governance

The **ConstructLedger** (`ConstructLedger.md`) serves as the formal measurement governance document for the BEBA project. Its function is to maintain a single, canonical map of constructs across theory development, measurement, and empirical analysis — preventing the proliferation of synonymous or conflicting construct definitions that has historically fragmented the nonprofit brand equity literature.[^6-fn-constructledger]

Each construct entry specifies:
- The construct name and its BEBA layer (Individual, Organisational, Societal).
- Its theoretical role in the BEBA architecture.
- The source model or theory from which it derives.
- The pipeline variable name in the empirical dataset.
- The chapters and articles in which it appears.
- Its current status (active, planned, conceptual, deprecated).

Changes to construct definitions, item sets, scale formation rules, or theoretical roles require a formal entry in the ADR or DecisionLog — the same governance mechanism used for architectural decisions. This prevents undocumented measurement drift, where the operational definition of a construct silently diverges from its theoretical definition over the course of a research programme.

The ConstructLedger currently contains 21 entries spanning the full range from foundational epistemological constructs (Epistemic Uncertainty, Information Asymmetry, Credence Goods) to active measurement constructs (Brand Trust, Brand Commitment, Donation Behaviour) to planned constructs awaiting scale development (Attitude, Subjective Norms, Perceived Behavioural Control).[^6-fn-status]

---

## 6.10 From Measurement to Structure: The Interface with Chapter 7

The measurement theory established in this chapter is a prerequisite for the structural analysis conducted in Chapter 7. The division of labour is conceptually clear:

- **Chapter 6 (Measurement):** Assesses whether each construct is validly and reliably measured in isolation. All CFA analyses are conducted on individual constructs before they are included in a structural model.
- **Chapter 7 (Structure):** Assesses the structural relationships between constructs — the causal paths, mediation effects, moderation effects, and model competition results that constitute the BEBA theory's empirical test.

This sequential logic (measurement before structure) is implemented through the **two-step approach** (Anderson & Gerbing, 1988): the measurement model is confirmed first, and only then are structural paths added. This prevents the common error of compensating for poor measurement with unrealistic structural parameters.

The practical consequence for the BEBA programme is that measurement fit of the full 21-construct model must be established before any substantive structural conclusions are drawn. If measurement fit is poor — if brand trust items do not load on a distinct factor, or if measurement invariance is violated across age groups — these are theoretical findings in their own right, not merely technical problems to be solved before the "real" analysis can proceed. They tell us something about whether the theoretical constructs are genuinely distinct entities in the target population.

---

## Footnotes

[^6-NB-000101]: **Claim NB-000101** (REVIEW-000100): Causal claims from cross-sectional survey data are likely inflated by common method bias. Evidence: BEBA Knowledge Base, REVIEW-000100.

[^6-NB-000102]: **Claim NB-000102** (REVIEW-000100): Commercial brand equity models are misspecified for nonprofits, omitting constructs like trust, authenticity, and mission alignment that are central to nonprofit stakeholder behaviour. Evidence: BEBA Knowledge Base, REVIEW-000100.

[^6-NB-000103]: **Claim NB-000103** (REVIEW-000100): A single brand equity measurement model is not invariant across stakeholder groups (donors, volunteers, etc.). Evidence: BEBA Knowledge Base, REVIEW-000100.

[^6-NB-000104]: **Claim NB-000104** (REVIEW-000100): The brand equity-behaviour relationship is likely negatively moderated by brand hypocrisy — perceived inconsistency between brand claims and organisational behaviour. Evidence: BEBA Knowledge Base, REVIEW-000100.

[^6-NB-000105]: **Claim NB-000105** (REVIEW-000100): The structure of brand equity is contingent on cultural context; no single measurement model can be assumed to hold across national populations. Evidence: BEBA Knowledge Base, REVIEW-000100.

[^6-CB-000020]: **Claim CB-000020** (REVIEW-000058): Consumer-Based Brand Equity is a higher-order construct with four dimensions: Brand Awareness, Brand Associations, Perceived Quality, and Brand Loyalty. Evidence: BEBA Knowledge Base, REVIEW-000058.

[^6-CB-000021]: **Claim CB-000021** (REVIEW-000058): Brand Awareness and Brand Associations are empirically distinct dimensions of brand equity and should not be collapsed into a single factor. Evidence: BEBA Knowledge Base, REVIEW-000058.

[^6-fn-rfmodel]: The reflective-formative distinction follows Bollen & Lennox (1991) and Jarvis et al. (2003). The decision rule for each BEBA construct is documented in the ConstructLedger and requires an ADR entry to change. The formative specification for overall brand equity follows from the theoretical claim that brand equity is constituted by its dimensions rather than being a common cause of them — but this is itself a theoretical choice that can be tested empirically through CFA model comparison.

[^6-fn-constructledger]: The ConstructLedger (`ConstructLedger.md` in the monography root) is the authoritative source for all construct definitions. It is the formal operationalisation of the BEBA principle "one canonical definition per construct." Any measurement decision that conflicts with a ConstructLedger entry requires a formal ADR to update the ledger before implementation.

[^6-fn-omega]: McDonald's omega ($\omega$) is computed as $\omega = \frac{(\sum \lambda_i)^2}{(\sum \lambda_i)^2 + \sum \delta_i}$ where $\lambda_i$ are the factor loadings and $\delta_i$ are the residual variances. Omega is a lower bound on reliability that does not require tau-equivalence. Omega hierarchical ($\omega_h$) specifically estimates the proportion of variance attributable to the general factor in a bifactor model — useful for evaluating whether overall brand equity retains explanatory value above and beyond its specific dimensions.

[^6-fn-MI]: Partial measurement invariance — where factor loadings but not item intercepts are invariant — still permits the comparison of structural relationships (regression coefficients, correlations) but not of latent variable means. The practical threshold for adequate partial invariance is typically that at least two items per factor are fully invariant (Byrne et al., 1989). Items that fail scalar invariance are investigated for content-based explanations (e.g., an item about "publicly recognising donors" may function differently for donors who value anonymity versus social recognition).

[^6-fn-omega2]: Full implementation details for the CMB test protocol (Harman test, marker variable, CFA-CMV comparison) follow Richardson et al. (2009). The marker variable is selected as a construct plausibly unrelated to the BEBA theoretical architecture — currently proposed: "interest in fantasy sports" or equivalent implausible correlate — following Lindell & Whitney (2001). This selection should be confirmed via pilot study.

[^6-fn-status]: ConstructLedger status categories: **Active** — construct is measured in the current empirical pipeline; **Planned** — construct is theoretically specified but not yet measured; **Conceptual** — construct is part of the theoretical architecture but no scale development is planned; **Deprecated** — construct has been removed from the active measurement model (requires ADR entry).
