---
concept: In_Nonprofits_We_Trust_A_Large_Scale_Study_on_the_Public_s_Trust_in_Nonprofit_Organizations
review: REVIEW-000069
claim_count: 10
claim_ids:
- TR-000014
- TR-000015
- TR-000016
- TR-000017
- TR-000018
- TR-000019
- TR-000020
- TR-000021
- TR-000022
- TR-000023
status: accepted
review_status: reviewed
reviewed_at: '2026-07-11T17:09:17.284167+00:00'
reviewed_by: human
---

# Input Reviewed

The set of candidate claims TR-000014 through TR-000023, derived from a multi-level analysis of public trust in nonprofit organizations (NPOs). These claims collectively describe the relative importance of individual-level versus organizational-level factors in explaining trust.

# Core Theoretical Implication

The central and most significant implication is the overwhelming dominance of individual-level factors in the formation of public trust. The findings suggest that the majority of variance in who trusts which NPO is located *within the individual* (their stable dispositions and their specific evaluation) rather than *between organizations* (their objective characteristics and signals).

This fundamentally reframes the role of the brand. Instead of being the primary driver of trust, the brand and its signals appear to be weak forces acting upon a strong, pre-existing architecture of individual-level predispositions. BEBA must therefore shift from a brand-centric view of trust formation to a stakeholder-centric one, where the brand's role is heavily mediated and constrained by the individual's context.

# BEBA Layer Affected

1.  **Individual Layer**: This layer is most significantly affected. It is elevated from being one component among others to being the primary locus of explanation for trust. The claims mandate a more sophisticated modeling of the individual, distinguishing between stable, pre-existing context and the specific, in-the-moment evaluation of an NPO.
2.  **Organisational Layer**: This layer is qualified. The direct causal power of organizational attributes and brand signals on trust is significantly down-weighted. While specific signals (certifications, mission type) are validated as effective (`TR-000017`, `TR-000018`), their overall contribution to the variance in trust is small (`TR-000016`). Their role becomes more about influencing the margins of the specific evaluation rather than being a foundational determinant.
3.  **Societal Layer**: This layer is reinforced as a crucial moderator. The finding that a religious mission is negatively associated with trust in a secular context (`TR-000019`) highlights that the effectiveness of any brand signal is conditional upon the surrounding socio-cultural environment.

# Existing Claims Supported

-   **Brands as Uncertainty-Reduction Signals**: `TR-000017` (third-party certification) and `TR-000018` (mission focus on children) directly support the core BEBA premise that brands deploy signals to reduce stakeholder uncertainty and build trust.
-   **Importance of Individual Factors**: BEBA's inclusion of an Individual Layer is strongly validated. Claims `TR-000020` (age), `TR-000021` (gender), and `TR-000022` (income) confirm that demographic characteristics are significant antecedents of trust.

# Existing Claims Challenged

-   Any implicit or explicit BEBA claim that posits organizational brand strategy as the *primary driver* of public trust is severely challenged. The evidence (`TR-000014`, `TR-000016`) suggests its direct effect is minor compared to individual-level factors.
-   Simple, linear models of "Brand Signal -> Trust" are challenged. The findings imply a more complex interaction where the individual's "Stable Context" (`TR-000015`) acts as a massive filter, moderator, or even a co-equal antecedent of the final trust judgment.

# New Candidate Claims

Based on this synthesis, the following higher-level claims should be considered for formal inclusion in the BEBA theory:

1.  **Primacy of the Individual in Trust Formation**: The majority of explainable variance in public trust in NPOs is attributable to individual-level factors (stable context and specific evaluation), not the objective characteristics of the organization.
2.  **Dual-Component Individual Trust**: An individual's trust evaluation is a function of two distinct, and roughly equally important, components: (1) their stable, pre-existing dispositional and demographic context, and (2) their specific evaluation of the target organization.
3.  **Conditional and Weak Effect of Brand Signals**: The influence of organizational brand signals on public trust is weak in magnitude and conditional upon the individual's pre-existing context and the broader socio-cultural environment.

# Boundary Conditions

-   **Cultural Context**: The findings, particularly regarding a religious mission (`TR-000019`), are from a largely secular German context. The relative weight of individual vs. organizational factors may differ in more religious or collectivistic societies.
-   **Stakeholder Type**: The claims are based on the "general public". The variance decomposition might be different for expert stakeholders (e.g., foundation program officers, major donors) who may engage in more systematic, organization-focused due diligence, potentially increasing the explanatory power of organizational factors for their specific group.

# Model Competition Implications

-   **A New Baseline Model**: These findings establish a powerful "null hypothesis" competitor for any BEBA model. A baseline model using only individual-level variables (demographics, disposition to trust) must be established. The BEBA model's value will be measured by its ability to explain variance *over and above* this baseline.
-   **Favours Heterogeneity Models**: The massive individual-level variance suggests that single, universal structural equation models may be inadequate. Models that account for heterogeneity, such as Latent Class Analysis or mixture models, should be prioritized in the empirical strategy to identify different "truster segments".
-   **Mediated/Moderated Brand Effects**: The evidence pushes BEBA towards models where brand equity's effect on behavioural outcomes is mediated by the "specific evaluation" component and/or moderated by the "stable individual context". A direct path from Brand Signals to Trust is likely misspecified or, at best, a minor pathway.

# Ontology Candidate Implications

1.  **New Concept Required**: A new, formal concept is necessary: **`Stable Individual Context`**. This concept should be created as an ontology candidate. It would be defined as "The set of stable, pre-existing individual characteristics, including demographics and general dispositions (e.g., generalized trust), that shape an individual's perception and evaluation of organizations." It would act as a parent concept for constructs like age, gender, income, etc., in the context of trust formation.
2.  **Relationship Refinement**: The relationship between `Brand Signal` and `Trust` must be refined in the BEBA ontology. It should be qualified as `weakly influences` and explicitly modeled as being mediated by `Stakeholder Evaluation` and moderated by `Stable Individual Context`.

# Recommendation

1.  **Architectural Shift**: Formally elevate the **Individual Layer** to a position of primary importance in the BEBA theoretical architecture for explaining trust. The causal story of trust must *start* with the individual.
2.  **Create New Concept Candidate**: Initiate a new concept file for `Stable Individual Context` to be integrated into the ontology. This concept is critical for capturing the main finding.
3.  **Update Theoretical Map**: Revise `01_THEORETICAL_MAP.md` to reflect the weak direct path from `Organisational Signals` to `Trust` and the strong, primary path from `Stable Individual Context` to `Trust`.
4.  **Adopt Baseline Model Strategy**: Formally adopt the "individual-level baseline model" as a required competitor model in the BEBA empirical testing plan. This makes the theory more robust and falsifiable.
5.  **Log Synthesized Claims**: Add the three "New Candidate Claims" listed above into the project's central claims registry as synthesized, higher-order theoretical propositions.

## Integration from REVIEW-000069

**Integrated:** 2026-07-13T19:03:49.171092+00:00

**Accepted claims (10):**
- TR-000014: The variance in public trust in a nonprofit organization is predominantly explained by individual-le
- TR-000015: The stable context of a trustor accounts for a portion of variance in their trust evaluations that i
- TR-000016: The objective characteristics of a nonprofit organization explain less than 10% of the total varianc
- TR-000017: The public display of a recognized, third-party accountability certification is positively associate
- TR-000018: A nonprofit mission focused on children is positively associated with public trust.
- TR-000019: In a largely secular societal context, an explicit religious mission is negatively associated with t
- TR-000020: Trust in nonprofit organizations is positively correlated with an individual's age.
- TR-000021: Women report higher levels of trust in nonprofit organizations than men.
- TR-000022: Trust in nonprofit organizations is negatively correlated with an individual's income level.
- TR-000023: Organizational age is a weak but positive predictor of public trust in a nonprofit organization.

**Accepted evidence (12):**
- EVID-001590: The variance in public trust in a nonprofit organization is predominantly explained by individual-le
- EVID-001591: The stable context of a trustor accounts for a portion of variance in trust evaluations (50.91%) tha
- EVID-001592: Objective organizational characteristics explain a small fraction (6.38%) of the total variance in p
- EVID-001593: The public display of a recognized, third-party accountability certification is positively associate
- EVID-001594: A nonprofit mission focused on children is positively associated with public trust.
- EVID-001595: In a largely secular societal context like Germany, an explicit religious mission is negatively asso
- EVID-001596: Trust in nonprofit organizations is positively correlated with an individual's age.
- EVID-001597: Women report higher levels of trust in nonprofit organizations than men.
- EVID-001598: Trust in nonprofit organizations is negatively correlated with an individual's income level.
- EVID-001599: Organizational age is a weak but positive predictor of public trust in a nonprofit organization.
- EVID-001600: Public trust is a foundational asset for NPOs, essential for securing legitimacy and support.
- EVID-001601: Sociodemographic factors are established correlates of pro-social behaviour.

**Accepted sources (2):**
- SRC-000326: Becker, A., Boenigk, S., & Willems, J. (2020)
- SRC-000253: Morgan, R. M., & Hunt, S. D. (1994)

