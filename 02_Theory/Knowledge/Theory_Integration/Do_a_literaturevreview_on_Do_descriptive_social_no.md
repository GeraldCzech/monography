---
concept: Do_a_literaturevreview_on_Do_descriptive_social_no
review: REVIEW-000105
claim_count: 6
claim_ids:
- DS-000009
- DS-000010
- DS-000011
- DS-000012
- DS-000013
- DS-000014
status: accepted
review_status: reviewed
reviewed_at: '2026-07-13T20:40:04.166655+00:00'
reviewed_by: human
---

# Input Reviewed

-   **Claim Set:** `DS-000009` to `DS-000014`
-   **Primary Concept:** Descriptive Social Norm

# Core Theoretical Implication

The reviewed claims collectively argue for a nuanced and cautious integration of social norms into the BEBA architecture. The core implication is that social norms are a necessary but insufficient component of pro-social behavioural models. They are not a "silver bullet" but a contributing factor with a modest, context-dependent, and potentially overestimated effect size. BEBA must model social influence with high granularity, specifically separating the distinct mechanisms of descriptive (social proof) and injunctive (social approval) norms, and account for critical boundary conditions like referent group proximity.

# BEBA Layer Affected

-   **Individual Layer:** The primary locus of effect is on individual-level perceptions and intentions (Claims `DS-000009` through `DS-000013`). This affects how BEBA models the cognitive and social inputs to an individual's decision-making process.
-   **Societal Layer:** Claim `DS-000014` affects this layer by highlighting a systemic issue in the scientific evidence base (publication bias), which informs how BEBA's knowledge engine should weigh and trust different sources of evidence.

# Existing Claims Supported

-   Any existing BEBA claim that posits a multi-factorial model of pro-social behaviour over a single-factor model. The modest effect size (`DS-000009`) supports the idea that norms are just one piece of the puzzle.
-   Any claim supporting a more granular model of social influence than that found in classic theories like the Theory of Planned Behaviour (TPB). The finding that adding descriptive norms improves TPB models (`DS-000012`) validates BEBA's presumed deeper architecture.
-   Any claim that BEBA must be grounded in empirically distinct constructs. The clear distinction between descriptive and injunctive norms (`DS-000011`) provides foundational support for this principle.

# Existing Claims Challenged

-   Any potential (explicit or implicit) claim that social norms are a primary or dominant driver of pro-social behaviour. The "modest" effect size (`DS-000009`) and the risk of effect size inflation (`DS-000014`) challenge this view.
-   Any claim that assumes the mechanisms of social influence are uniform across different behavioural domains. The finding that injunctive norms are stronger than descriptive norms in the donation context (`DS-000010`) challenges a "one-size-fits-all" model of social norms.

# New Candidate Claims

Based on this review, the following claims should be considered for formal inclusion in the BEBA knowledge base:

1.  **C-NEW-SN-01:** The BEBA architecture must model descriptive and injunctive social norms as separate constructs with distinct causal pathways to behavioural intention. (Source: `DS-000011`)
2.  **C-NEW-SN-02:** Within the charitable donation context, the causal path from injunctive norms to intention is stronger than the path from descriptive norms to intention. (Source: `DS-000010`)
3.  **C-NEW-SN-03:** The influence of perceived descriptive norms on pro-social intention is moderated by referent group proximity, with the effect strengthening as proximity increases. (Source: `DS-000013`)
4.  **C-NEW-SN-04:** The evidential weight assigned to social norm effect sizes within BEBA must be adjusted for study pre-registration status to mitigate known publication bias. (Source: `DS-000014`)

# Boundary Conditions

This review introduces two critical boundary conditions for the effect of social norms within BEBA:

1.  **Context Specificity:** The relative importance of descriptive vs. injunctive norms is specific to the behavioural context (e.g., charitable giving). This implies BEBA models may need context-specific parameterization.
2.  **Referent Group Proximity:** The influence of descriptive norms is not universal but is conditional on the psychological closeness of the group demonstrating the behaviour.

# Model Competition Implications

-   **Superiority over TPB:** BEBA's separation of descriptive and injunctive norms provides a clear point of theoretical and empirical superiority over the classic TPB, which confounds them in a single "subjective norm" construct. This should be a core argument in BEBA's positioning.
-   **Against Norm-Centric Models:** The findings challenge the validity of models that place social norms as the central or sole driver of behaviour. This strengthens BEBA's case for a more comprehensive, brand-centric architecture where norms are an important input but not the entire mechanism.

# Ontology Candidate Implications

This integration requires updates to the BEBA ontology:

1.  **Distinct Norm Concepts:** `DescriptiveSocialNorm` and `InjunctiveSocialNorm` must be formalized as distinct, non-interchangeable concepts in the ontology. They should not be children of a generic `SocialNorm` but rather sibling concepts under a broader `SocialInfluence` category.
2.  **New Moderator Concept:** A new concept, `ReferentGroupProximity`, should be created as an ontology candidate. It should be defined as "The perceived psychological, social, or physical closeness of a group used by an individual as a standard for comparison."
3.  **Relationship Specification:** The relationship between `ReferentGroupProximity` and `DescriptiveSocialNorm` should be typed as `moderates`, specifically strengthening the `influences` relationship between `DescriptiveSocialNorm` and `DonationIntention`.

# Recommendation

1.  **Formalize Ontology Candidates:** Create/update the candidate files for `DescriptiveSocialNorm`, `InjunctiveSocialNorm`, and `ReferentGroupProximity` to reflect their distinct roles and relationships as identified above.
2.  **Ingest New Claims:** Add the four "New Candidate Claims" (`C-NEW-SN-01` to `04`) to the official claims repository for tracking and testing.
3.  **Update Theoretical Map:** Revise `01_THEORETICAL_MAP.md` to explicitly show two separate pathways for social influence, one for descriptive and one for injunctive norms, flowing into the individual decision-making layer.
4.  **Create Methodological Note:** Add an entry to the `ResearchCompass.md` or a relevant ADR regarding the "Pre-registration Principle": "When synthesizing evidence on social norm effects, prioritize or assign higher weight to findings from pre-registered studies to control for publication bias."
5.  **Tag for Model Specification:** The finding that injunctive > descriptive norms in the donation context (`DS-000010`) should be tagged as a key prior for Bayesian model specifications in future empirical work.

## Integration from REVIEW-000105

**Integrated:** 2026-07-13T20:44:44.944230+00:00

**Accepted claims (6):**
- DI-000014: Attitude, subjective norm, and perceived behavioural control are significant positive predictors of 
- DI-000015: Adding moral norm and past behaviour to the standard Theory of Planned Behaviour model significantly
- DI-000016: The effects of Perceived Behavioural Control and Moral Norm on charitable donation intention are mor
- SN-000009: The positive effect of Subjective Norm on donation intention is moderated by cultural context.
- IB-000032: The relationship between donation intention and actual donation behaviour is significantly weaker th
- BT-000035: The perceived trustworthiness of a nonprofit brand positively influences donation intention by incre

**Accepted evidence (10):**
- EVID-001948: The Theory of Planned Behaviour (TPB) is a robust and widely supported framework for predicting the 
- EVID-001949: Models of donation intention extended with moral norm and past behaviour consistently explain more v
- EVID-001950: A significant "intention-behaviour gap" exists, where the TPB is substantially more successful at pr
- EVID-001951: Perceived Behavioural Control (PBC) is the most consistent and often the strongest predictor of dona
- EVID-001952: The effect of Subjective Norm on donation intention is highly variable, being significant in some cu
- EVID-001953: Moral Norm, defined as a personal feeling of moral obligation, is a powerful and direct predictor of
- EVID-001954: Past donation behaviour is a strong predictor of future donation intention, capturing effects not fu
- EVID-001955: The TPB framework is not universally supported, with some studies finding its core predictors non-si
- EVID-001956: A research gap exists in systematically integrating organisational factors like trust in the charity
- EVID-001957: There is a research gap in understanding the contextual barriers and facilitators that moderate the 

**Accepted sources (10):**
- SRC-000567: White, K., Sutton, L. S. C., & Zhao, X. (2023)
- SRC-000617: Ajzen, I. (2002)
- SRC-000568: Smith, J. R., & McSweeney, A. (2007)
- SRC-000569: Veludo-De-Oliveira, T., Alhaidari, I. S., Yani-De-Soriano, M., & Yousafzai, S. Y. (2016)
- SRC-000631: Bhati, A., & Hansen, R. K. (2020)
- SRC-000632: Wedel, M., Kannan, P., & Tyser, R. J. (2016)
- SRC-000575: Li, W., Mao, Y., & Liu, C. (2022)
- SRC-000570: Mittelman, R., & Rojas Méndez, J. I. (2018)
- SRC-000633: Swaminathan, V., Sorescu, A., Steenkamp, J., O’Guinn, T. C., & Schmitt, B. H. (2020)
- SRC-000634: Södergren, J. (2021)

