---
concept: Consumer_based_brand_equity_measurement_lessons_learned_from_an_international_study
review: REVIEW-000057
claim_count: 5
claim_ids:
- CB-000017
- BK-000009
- CB-000018
- BK-000010
- CB-000019
status: accepted
review_status: reviewed
reviewed_at: '2026-07-12T12:43:47.604719+00:00'
reviewed_by: human
---

# Input Reviewed

The integration protocol is being applied to a set of five candidate claims (CB-000017, BK-000009, CB-000018, BK-000010, CB-000019) derived from `REVIEW-000057`. These claims collectively challenge the structural validity, measurement invariance, and universal applicability of Aaker's (1991) model of consumer-based brand equity (CBBE). Key findings include the lack of discriminant validity between brand awareness and associations, the exacerbation of this issue in service contexts, and the conceptual dependency of associations on awareness.

# Core Theoretical Implication

The core implication is a strong, evidence-based rejection of Aaker's (1991) four-factor CBBE model as a suitable theoretical or measurement foundation for BEBA. The evidence compels a fundamental reconceptualization of the Brand Knowledge Structure, moving away from a reflective, multi-factor model towards a process-based or causally dependent structure that is sensitive to the high intangibility and specific context of the nonprofit sector.

# BEBA Layer Affected

-   **Individual Layer:** Directly affected. The findings in `BK-000009` and `BK-000010` require a revision of how brand knowledge (awareness, associations) is structured and processed at the individual level.
-   **Market Layer:** Directly affected. The findings in `CB-000017`, `CB-000018`, and `CB-000019` challenge the idea of a universal, aggregate brand equity construct and support the need for a context-sensitive market-level theory.
-   **Methodological Layer (Implicit):** Deeply affected. These claims invalidate the common practice of applying Aaker's scales in a simple confirmatory factor analysis (CFA) model, especially in a nonprofit context. This has major implications for the empirical pipeline.

# Existing Claims Supported

-   Any existing BEBA claim positing the **inadequacy of commercial-sector brand equity models** for the nonprofit context is strongly supported.
-   The core BEBA rationale for developing a **new, context-specific theory** is validated (`CB-000019`).
-   The BEBA research principle of **"Theory before models"** is reinforced by demonstrating how a widely used model fails due to a flawed underlying theoretical assumption (i.e., treating dependent concepts as independent factors).

# Existing Claims Challenged

-   Any implicit or explicit assumption that Aaker's (1991) dimensions (awareness, associations, perceived quality, loyalty) could serve as a "good enough" starting point for the BEBA model is now untenable.
-   The notion of measuring brand equity via a simple, reflective, second-order construct based on Aaker's dimensions is empirically falsified by this evidence.

# New Candidate Claims

Based on this integration, the following new claims should be created and added to the knowledge base:

1.  **Claim (Theory):** The cognitive structure of nonprofit brand knowledge is a causal sequence, not a set of co-equal reflective dimensions. Specifically, brand awareness is a necessary precondition for the formation of brand associations. (Derived from `BK-000010`).
2.  **Claim (Boundary Condition):** The structural validity of brand equity models is moderated by the degree of brand intangibility; models developed for tangible goods are likely to fail when applied to highly intangible nonprofit brands. (Derived from `CB-000018`).
3.  **Claim (Boundary Condition):** Macro-level uncertainty (e.g., cultural, economic) acts as a boundary condition on the generalizability of any given brand equity structure. (Derived from `CB-000019`).

# Boundary Conditions

This review explicitly identifies three critical boundary conditions for brand equity theory:

1.  **Sector / Intangibility:** The goods vs. services/internet distinction is a key boundary. BEBA must treat the high intangibility of the nonprofit sector as a central design parameter.
2.  **National / Cultural Context:** Measurement and structural invariance cannot be assumed across countries.
3.  **Macro-Economic Environment:** The note in `CB-000019` suggests economic uncertainty may influence brand equity structures, which aligns directly with the core BEBA research question.

# Model Competition Implications

-   **Disadvantaged Models:** Any model in the BEBA research program that specifies a direct replication of Aaker's (1991) four-factor reflective model is now strongly disfavored and should be deprioritized or used only as a failed benchmark.
-   **Advantaged Models:** This evidence favors competing models that:
    -   Model brand knowledge as a **causal chain** (e.g., Awareness -> Associations -> ...) or a process.
    -   Explicitly incorporate **intangibility** as a moderator.
    -   Are designed for **context-sensitivity** (e.g., via multi-group SEM testing for contextual moderators).
-   This significantly strengthens the mandate for the BEBA project to proceed with developing its unique, behaviour-first architecture rather than adapting existing commercial models.

# Ontology Candidate Implications

1.  **Reject Aaker's Structure:** The concept `ConsumerBasedBrandEquity` should not be defined in the BEBA ontology as a composition of `BrandAwareness`, `BrandAssociations`, `PerceivedQuality`, and `BrandLoyalty` as co-equal parts.
2.  **Introduce Causal Relationship:** A new relationship should be introduced between `BrandAwareness` and `BrandAssociations`. A candidate for the BEBA Relationship Model would be `isPrerequisiteFor`. The resulting triple would be: (`BrandAwareness`, `isPrerequisiteFor`, `BrandAssociations`).
3.  **Elevate Intangibility:** The concept of `Intangibility` needs to be defined as a core property of `NonprofitBrand` and formally linked as a moderator to relationships within the `BrandKnowledgeStructure`.

# Recommendation

1.  **Action:** Formally reject the Aaker (1991) four-factor model as a candidate for the BEBA core theory. Create a `DecisionLog` entry to document this.
2.  **Action:** Update the `ConstructLedger` to mark the Aaker (1991) CBBE scale set as "Not Recommended for BEBA" and link to this integration analysis as the rationale.
3.  **Action:** Initiate a new concept workspace file: `02_Theory/Concept_Workspaces/Brand_Knowledge_Structure_v2.md`. This file should begin by drafting a process-based model of brand knowledge, using claim `BK-000010` as its foundation.
4.  **Action:** Draft the new candidate claims identified above and add them to the claims database for further review.
5.  **Action:** Propose an update to the `BEBA_RELATIONSHIP_MODEL_v1.md` to include the `isPrerequisiteFor` relationship type.

## Integration from REVIEW-000057

**Integrated:** 2026-07-13T19:02:54.597069+00:00

**Accepted claims (5):**
- CB-000017: Aaker's (1991) four-dimensional model of consumer-based brand equity (awareness, associations, perce
- BK-000009: The constructs of brand awareness and brand associations, as measured by standard survey items based
- CB-000018: The lack of discriminant validity among the dimensions of Aaker's (1991) CBBE model is more severe f
- BK-000010: The empirical lack of discriminant validity between brand awareness and brand associations stems fro
- CB-000019: The universal applicability of a single, invariant structure for consumer-based brand equity is not 

**Accepted evidence (6):**
- EVID-001495: Aaker's (1991) four-dimensional model of consumer-based brand equity (CBBE) does not demonstrate mea
- EVID-001496: The constructs of brand awareness and brand associations, as conceptualized by Aaker (1991), lack di
- EVID-001497: The lack of discriminant validity among the dimensions of Aaker's (1991) CBBE model is more severe f
- EVID-001498: The empirical lack of discriminant validity between brand awareness and brand associations likely st
- EVID-001499: The direct application of Aaker's (1991) model is problematic in cross-national and multi-sector con
- EVID-001500: Previous studies concluded that Aaker's CBBE model was invariant across different countries.

**Accepted sources (3):**
- SRC-000271: Aaker, David A. (1991)
- SRC-000272: Yoo, Boonghee; Donthu, Naveen (2001)
- SRC-000273: Buil, Isabel; de Chernatony, Leslie; Martínez, Eva (2008)

