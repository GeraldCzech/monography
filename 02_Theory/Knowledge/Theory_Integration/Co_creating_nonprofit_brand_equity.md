---
concept: Co_creating_nonprofit_brand_equity
review: REVIEW-000056
claim_count: 5
claim_ids:
- NB-000069
- BC-000033
- BA-000066
- BI-000041
- NB-000070
status: accepted
review_status: reviewed
reviewed_at: '2026-07-11T12:39:54.326856+00:00'
reviewed_by: human
---

# Input Reviewed

-   **NB-000069:** Functional similarity of NBE structure for internal/external stakeholders.
-   **BC-000033:** Co-creation via internal-to-external stakeholder transition.
-   **BA-000066:** Greater influence of brand awareness for internal stakeholders.
-   **BI-000041:** Greater influence of brand image for external stakeholders.
-   **NB-000070:** Need for modification of B2B models in nonprofit contexts.

# Core Theoretical Implication

The core implication is that while the cognitive *structure* of nonprofit brand equity (Awareness, Image) may be shared across stakeholder groups, its functional *dynamics* are contingent on the stakeholder's position and type of experience. The brand acts as a shared interface, but stakeholders interact with it differently. Specifically, the influence of brand equity components (awareness vs. image) on behaviour is moderated by whether the stakeholder is internal (direct experience) or external (indirect experience). This provides a mechanism for brand co-creation through stakeholder transitions and reinforces the need for a dedicated nonprofit brand theory.

# BEBA Layer Affected

This set of claims affects three BEBA layers:

1.  **Individual Layer:** By specifying how individual-level constructs (Brand Awareness, Brand Image) have differential effects on perceptions of Brand Equity depending on the individual's role.
2.  **Market Layer:** By identifying a specific mechanism (`StakeholderTransition`) that facilitates brand co-creation and creates a behavioural feedback loop between different stakeholder groups.
3.  **Organisational Layer:** By highlighting the methodological inadequacy of directly transferring commercial B2B measurement models, thus justifying the BEBA framework's existence and the need for context-specific operationalisation.

# Existing Claims Supported

-   Claims related to the brand's function as a **shared cognitive architecture** for coordinating behaviour are supported by NB-000069, which finds a common factor structure for brand equity across groups.
-   Claims framing BEBA as a **self-sustaining behavioural system** are supported by BC-000033, which provides an example of a reinforcing stakeholder loop.
-   The foundational claim that **nonprofit branding requires a distinct theoretical framework** is strongly supported by NB-000070, which shows the poor fit of standard commercial models.

# Existing Claims Challenged

No core BEBA claims are directly challenged. However, these findings *qualify* any overly simplistic claims that assume a uniform effect of brand equity components across all stakeholders. They suggest that models of BEBA must account for stakeholder-specific variations.

# New Candidate Claims

Based on this integration, the following new candidate claims for the BEBA theory are proposed:

1.  **BEBA-C-NEW-01:** The structural components of a BEBA (e.g., Awareness, Image) can form a common cognitive interface shared by diverse stakeholder groups. (From NB-000069)
2.  **BEBA-C-NEW-02:** The behavioural influence of BEBA components is contingent on the stakeholder's relationship to the organization and their primary mode of experience (direct vs. indirect). (Synthesis of BA-000066, BI-000041)
3.  **BEBA-C-NEW-02a (Sub-claim):** For internal stakeholders with direct, experiential knowledge, brand awareness has a greater relative influence on their brand-related cognitions and behaviour. (From BA-000066)
4.  **BEBA-C-NEW-02b (Sub-claim):** For external stakeholders with indirect, observational knowledge, brand image serves as a primary quality heuristic and has a greater relative influence on their brand-related cognitions and behaviour. (From BI-000041)
5.  **BEBA-C-NEW-03:** The transition of stakeholders from one role to another (e.g., internal to external) is a key mechanism for brand co-creation, strengthening the BEBA's feedback loops. (From BC-000033)

# Boundary Conditions

The findings introduce important boundary conditions:

-   **Organisational Context:** The claims originate from a highly structured, mandatory-participation nonprofit (military training). Their applicability to voluntary, low-structure nonprofits is not established.
-   **Stakeholder Definition:** The specific definitions of "internal" (conscripts) and "external" (potential employers) are narrow and may not generalize to other stakeholder types (e.g., donors, volunteers).
-   **Measurement Model:** The claims are conditional on a specific, modified B2B measurement model. The differential effects might be an artifact of this operationalisation.

# Model Competition Implications

This evidence provides a clear path for refining BEBA model testing:

1.  **Against a Null Model:** It provides a strong rationale for proposing a multi-group structural equation model (testing for differences between internal vs. external stakeholders) as a competing explanation against a simpler, pooled model that assumes invariant path coefficients. The evidence suggests the multi-group model will provide a better fit.
2.  **Against External Models:** It reinforces the argument against the direct application of commercial B2B/B2C brand equity models (like the one by Davis et al., 2008) in the nonprofit context, positioning BEBA as a theoretically and empirically superior alternative.

# Ontology Candidate Implications

This review suggests the need for several additions or refinements to the BEBA ontology:

1.  **Concept: `Stakeholder`:** Requires sub-typing to distinguish `InternalStakeholder` from `ExternalStakeholder`.
2.  **Property: `ExperienceType`:** A new property for the `Stakeholder` concept, with values such as `Direct` or `Indirect`, to capture the mechanism moderating the effects of awareness and image.
3.  **Process: `StakeholderTransition`:** A new concept representing the process of a stakeholder changing roles, which can be modeled as a relationship that facilitates `BrandCoCreation`.

# Recommendation

1.  **Create Candidate Claims:** Formally draft the five "New Candidate Claims" listed above and add them to the repository for further review and testing.
2.  **Update Ontology Candidates:** Propose an `OntologyCandidate` file that includes the concepts `InternalStakeholder`, `ExternalStakeholder`, the property `ExperienceType`, and the process `StakeholderTransition`.
3.  **Inform Empirical Pipeline:** Add a note to the research compass to design a multi-group SEM analysis in the empirical pipeline. The goal is to explicitly test for the differential effects of Brand Awareness and Brand Image on Brand Equity for internal vs. external stakeholder groups (e.g., employees vs. donors).
4.  **Acknowledge Limitations:** Ensure the "Notes" and "Confidence" levels of the new claims reflect the single-case, modified-measurement basis of this evidence, flagging them for priority replication in a different nonprofit context.

## Integration from REVIEW-000056

**Integrated:** 2026-07-13T19:02:50.149591+00:00

**Accepted claims (5):**
- NB-000069: The perceived structure of nonprofit brand equity, defined by brand awareness and brand image, can b
- BC-000033: The co-creation of nonprofit brand equity is facilitated when internal stakeholders transition to be
- BA-000066: In co-created nonprofit brand equity models, brand awareness has a greater relative influence on bra
- BI-000041: In co-created nonprofit brand equity models, brand image has a greater relative influence on brand e
- NB-000070: Standard B2B brand equity measurement models may require modification to achieve construct validity 

**Accepted evidence (7):**
- EVID-001488: A statistically workable and similar structure for brand equity, with Brand Awareness and Brand Imag
- EVID-001489: Brand Awareness is a stronger driver of Brand Equity for internal stakeholders (recruits) than for e
- EVID-001490: Brand Image is a stronger driver of Brand Equity for external stakeholders (LSPs) than for internal 
- EVID-001491: Standard B2B brand equity models may not be directly applicable to nonprofit contexts without modifi
- EVID-001492: Brand Image is a statistically significant determinant of Brand Equity for internal stakeholders in 
- EVID-001493: The mechanism of brand co-creation is facilitated by a continuous flow of individuals from an intern
- EVID-001494: The constructs of Brand Awareness and Brand Image are significant antecedents of overall Brand Equit

**Accepted sources (5):**
- SRC-000258: Juntunen, M., Juntunen, J., and Autere, J. (2013)
- SRC-000261: Vargo, S.L. and Lusch, R.F. (2004)
- SRC-000263: Keller, K.L. (1993)
- SRC-000264: Aaker, D.A. (1996)
- SRC-000269: Faircloth, J.B. (2005)

