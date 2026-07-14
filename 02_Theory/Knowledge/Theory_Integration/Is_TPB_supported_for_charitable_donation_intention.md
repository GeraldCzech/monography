---
concept: Is_TPB_supported_for_charitable_donation_intention
review: REVIEW-000105
claim_count: 6
claim_ids:
- DI-000014
- DI-000015
- DI-000016
- SN-000009
- IB-000032
- BT-000035
status: accepted
review_status: reviewed
reviewed_at: '2026-07-13T20:43:48.013118+00:00'
reviewed_by: human
---

# Input Reviewed

The reviewed input consists of six claims (DI-000014 to BT-000035) derived from a literature synthesis on the Theory of Planned Behaviour (TPB) as it applies to charitable donation. The claims establish the standard TPB predictors, introduce extensions (Moral Norm, Past Behaviour), qualify the relative importance and cultural dependence of predictors, highlight the Intention-Behaviour Gap, and propose a specific mechanism for how Brand Trust links to the TPB framework.

# Core Theoretical Implication

The core implication is that the TPB and its extensions provide a necessary but insufficient psychological foundation for BEBA. While it robustly identifies the cognitive antecedents of *intention* (Attitude, PBC, Moral Norm), it simultaneously validates the central problem BEBA seeks to solve: the significant gap between intention and actual behaviour. This positions BEBA not as a replacement for TPB, but as a framework that (1) explains how brand equity (an organisational asset) systematically influences the key TPB antecedents, and (2) provides the "Architecture" to bridge the Intention-Behaviour Gap.

# BEBA Layer Affected

-   **Individual Layer:** Primarily affected. The claims define the core psychological mechanics of intention formation (`Attitude`, `Subjective Norm`, `Perceived Behavioural Control`, `Moral Norm`, `Donation Intention`).
-   **Organisational Layer:** Affected by claim BT-000035, which posits that an organisational asset (`Brand Trust`) is a key antecedent to the individual-level psychological variables.
-   **Societal Layer:** Affected by claim SN-000009, which introduces `Cultural Context` as a moderator, establishing a macro-level boundary condition.

# Existing Claims Supported

-   The claims strongly support the core BEBA premise that a theory of brand effectiveness must be grounded in a theory of human behaviour.
-   Claim **IB-000032 (Intention-Behaviour Gap)** provides direct empirical and theoretical justification for the "Architecture" component of BEBA. It validates the research problem that BEBA is designed to address.
-   Claim **DI-000014** validates the choice of `Attitude` and `Perceived Behavioural Control` as key mediating variables for brand effects, as proposed in claim **BT-000035**.

# Existing Claims Challenged

The reviewed claims do not directly challenge existing BEBA claims; rather, they provide the foundation upon which BEBA is built. However, they indirectly challenge any simplistic BEBA model that might propose a direct, unmediated path from brand equity to behaviour, by highlighting the critical mediating role of intention and the significant hurdle of the Intention-Behaviour Gap. They also caution against over-reliance on social norm-based brand strategies, revealing them to be less robust and more context-dependent than strategies focused on self-efficacy (PBC) and moral conviction.

# New Candidate Claims

Based on this integration, the following claims should be considered for formal inclusion in the BEBA theory:

1.  **C-BEBA-TPB-01:** The BEBA framework incorporates the extended Theory of Planned Behaviour as the core model of individual-level intention formation for pro-social behaviours.
2.  **C-BEBA-TPB-02:** A primary function of nonprofit brand equity is to positively influence the antecedents of donation intention, specifically Attitude (towards the act), Perceived Behavioural Control, and Moral Norms.
3.  **C-BEBA-TPB-03:** The "Architecture" component of BEBA is specifically designed to bridge the empirically established gap between Donation Intention and Donation Behaviour.
4.  **C-BEBA-TPB-04:** The effectiveness of brand strategies leveraging social influence (`Subjective Norm`) is bounded by `Cultural Context` and should be considered less universally applicable than strategies targeting `Perceived Behavioural Control` or `Moral Norms`.

# Boundary Conditions

A significant boundary condition is identified:
-   **Cultural Context:** The influence of Subjective Norms on donation intention is moderated by culture (stronger in collectivist, weaker in individualist societies). This implies that the social-signalling function of a brand is not universally effective and must be adapted to the cultural environment.

# Model Competition Implications

This review sets up a clear path for model competition:

1.  **Baseline Model (Extended TPB):** A model where Attitude, SN, PBC, Moral Norm, and Past Behaviour predict Intention, which in turn predicts Behaviour. This model has no role for the brand.
2.  **Mediated BEBA Model:** A model where Brand Equity dimensions (e.g., Trust, Awareness, Loyalty) predict the Extended TPB variables, which in turn predict Intention. This model tests the hypothesis that the brand's effect is fully mediated by donor psychology.
3.  **Architectural BEBA Model:** This model adds the "Architecture" construct as a moderator of the Intention -> Behaviour relationship. This directly tests BEBA's core value proposition in solving the Intention-Behaviour Gap.

The claims suggest that a simple model linking brand equity directly to behaviour is likely to be misspecified and inferior to models that account for the psychological mediation and the intention-behaviour gap.

# Ontology Candidate Implications

This integration necessitates the formal inclusion and definition of the following constructs within the BEBA ontology, primarily at the Individual Layer:

-   `Concept: Attitude (towards donation)`
-   `Concept: Subjective Norm (re: donation)`
-   `Concept: Perceived Behavioural Control (re: donation)`
-   `Concept: Moral Norm (re: donation)`
-   `Concept: Donation Intention`
-   `Concept: Past Behaviour`
-   `Concept: Intention-Behaviour Gap` (as a key phenomenon/problem)

The relationships between these (e.g., `predicts`, `is_antecedent_to`) should be formally mapped. The proposed link from `Brand Trust` to `Attitude` and `PBC` should be captured as a core hypothetical relationship to be tested.

# Recommendation

1.  **Formalise Foundation:** Adopt the Extended Theory of Planned Behaviour (including Attitude, SN, PBC, Moral Norm, Past Behaviour) as the canonical psychological micro-foundation for the Individual Layer of the BEBA model.
2.  **Create Concept Files:** Create canonical concept files for the core TPB constructs (`Attitude`, `Subjective Norm`, `Perceived Behavioural Control`, `Moral Norm`, `Donation Intention`) and add them to the `02_Theory/Concepts/` directory.
3.  **Update Theoretical Map:** Update `01_THEORETICAL_MAP.md` to explicitly show Brand Equity dimensions influencing these core TPB constructs, which in turn influence Intention.
4.  **Prioritise Architecture:** Frame future theoretical and empirical work on the "Architecture" component around its role as a moderator of the intention-behaviour link, directly addressing the gap identified in claim **IB-000032**. This becomes a central, testable hypothesis for the BEBA framework.
