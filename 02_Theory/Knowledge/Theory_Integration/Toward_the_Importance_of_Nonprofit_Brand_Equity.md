---
concept: Toward_the_Importance_of_Nonprofit_Brand_Equity
review: REVIEW-000089
claim_count: 6
claim_ids:
- NB-000096
- NB-000097
- BT-000025
- BT-000026
- NB-000098
- NB-000099
status: accepted
review_status: reviewed
reviewed_at: '2026-07-11T10:24:08.488988+00:00'
reviewed_by: human
---

# Input Reviewed

-   **NB-000096**: Justification for a sector-specific brand equity model.
-   **NB-000097**: Proposes a three-dimensional structure (Awareness, Trust, Commitment) for the general public.
-   **BT-000025**: Elevates Brand Trust as a distinct, powerful dimension over 'brand image'.
-   **BT-000026**: Defines Brand Trust's function as reducing perceived risk about mission fidelity and resource use.
-   **NB-000098**: Suggests a sequential formation process: Awareness -> Trust -> Commitment.
-   **NB-000099**: Suggests a second-order formative construct for the "relational component" (Trust + Commitment).

# Core Theoretical Implication

The reviewed claims collectively propose a specific, parsimonious, and testable psychological process model for how nonprofit brand equity is formed in the minds of the general public. The core mechanism is **Brand Trust**, which acts as a risk-reduction device, translating cognitive accessibility (**Brand Awareness**) into relational intent (**Brand Commitment**). This provides a foundational alternative to directly transferred for-profit models and directly addresses BEBA's core question about brand effectiveness under uncertainty.

# BEBA Layer Affected

-   **Individual Layer**: Primarily affected. Claims BT-000025, BT-000026, NB-000097, and NB-000098 describe the perceptual and psychological structure of brand equity from the stakeholder's perspective (risk perception, sequential processing, belief formation).
-   **Organisational Layer**: Secondarily affected. Claim NB-000096 provides a foundational argument for the BEBA project at the organizational strategy level. Claim NB-000099 offers a specific approach for modeling organizational-level brand equity by aggregating individual-level perceptions.

# Existing Claims Supported

-   Supports the foundational premise of BEBA that a sector-specific theory is necessary (NB-000096).
-   Supports the elevation of `Brand Trust` to a primary, first-class construct within the BEBA framework (BT-000025).
-   Directly supports BEBA's focus on uncertainty, providing a mechanism (risk reduction) through which brands operate (BT-000026).

# Existing Claims Challenged

-   Challenges any claim positing the direct and unmodified transferability of commercial brand equity models (e.g., Aaker's or Keller's dimensions) to the nonprofit sector.
-   Challenges conceptualizations where `Brand Trust` is merely a sub-dimension of a broader construct like `Brand Image` or `Brand Associations`. It argues for Trust's distinct and superior explanatory power.

# New Candidate Claims

Based on this integration, the following claims should be considered for formal inclusion in the BEBA claim set:

1.  **C-BEBA-2024-03-21-001**: The primary function of nonprofit Brand Trust is the reduction of stakeholder perceived risk concerning mission fidelity and resource allocation. (Derived from BT-000026)
2.  **C-BEBA-2024-03-21-002**: For the general public, the formation of brand-related behavioural intent follows a psychological sequence from Brand Awareness to Brand Trust to Brand Commitment. (Derived from NB-000098)
3.  **C-BEBA-2024-03-21-003**: The relational core of nonprofit brand equity is a composite of Brand Trust and Brand Commitment. (Derived from NB-000097 & NB-000099)

# Boundary Conditions

-   The three-dimensional structure (Awareness, Trust, Commitment) is explicitly validated for the **'general public' stakeholder group**. Its applicability to other groups with higher information access and different motivations (e.g., major donors, institutional funders, expert volunteers) is not established and requires separate investigation.
-   The sequential nature of the model (Awareness -> Trust -> Commitment) is a theoretical proposition derived from a cross-sectional study. It establishes a plausible "relationship cycle" but does not provide longitudinal proof of the temporal order.

# Model Competition Implications

This integration provides a strong, theory-driven competitor model for the BEBA project. It creates several clear points of model competition:

1.  **Dimensionality Competition**: A parsimonious `Awareness-Trust-Commitment` model versus more complex models including dimensions like `Perceived Quality`, `Brand Personality`, or `Brand Loyalty` (split into attitudinal/behavioural).
2.  **Process Competition**: The proposed `Sequential Model` (Awareness -> Trust -> Commitment) can be tested against:
    -   A `Parallel Model` where Awareness influences Trust and Commitment simultaneously.
    -   A `Mediated Model` where Trust fully mediates the effect of other perceptions (e.g., Image) on Commitment and behaviour.
3.  **Measurement Model Competition**: Claim NB-000099's proposal of a `formative` second-order "relational" construct can be directly tested against a more common `reflective` measurement model. This has significant implications for the empirical pipeline.

# Ontology Candidate Implications

1.  **Concept: `Brand Commitment`**: This integration necessitates the creation of a canonical concept file for `Brand Commitment` as a core component of stakeholder-based nonprofit brand equity. It should be defined as a psychological attachment and intent to support the NPO.
2.  **Concept: `Relational Component of Brand Equity`**: A new candidate concept could be created to represent the higher-order construct formed by Trust and Commitment, capturing the relational (as opposed to cognitive) aspect of brand equity.
3.  **Relationship: `is_precondition_for`**: The sequential model (NB-000098) implies a specific relationship between concepts in the ontology: `Brand Awareness` `is_precondition_for` `Brand Trust`, and `Brand Trust` `is_precondition_for` `Brand Commitment`. This should be added to the relationship model.

# Recommendation

1.  **Adopt Core Mechanism**: Formally integrate the risk-reduction function of Brand Trust (BT-000026) into the core BEBA theory documents and the canonical definition of the `Brand Trust` concept.
2.  **Create Model Candidate**: Create a new `Model` file in `02_Theory/Models/` named `M-CANDIDATE-AWARENESS_TRUST_COMMITMENT_SEQUENTIAL_v1.md`. This file should formally specify the model derived from these claims for empirical testing.
3.  **Update Ontology**:
    -   Create a new concept candidate file: `02_Theory/Ontology_Candidates/Concept_BrandCommitment.md`.
    -   Update the `BEBA_RELATIONSHIP_MODEL_v1.md` to include the `is_precondition_for` relationship as specified above.
4.  **Log Boundary Condition**: Ensure the 'general public' stakeholder group boundary condition is explicitly attached to the new model candidate and any claims derived from NB-000097.
5.  **Create ADR**: The question of a formative vs. reflective measurement model for the "Relational Component" (NB-000099) is a significant architectural decision for the empirical pipeline. Propose an **ADR** to decide on the default measurement model strategy for higher-order BEBA constructs.

## Integration from REVIEW-000089

**Integrated:** 2026-07-13T19:05:23.514784+00:00

**Accepted claims (5):**
- NB-000096: A stakeholder-based brand equity model incorporating context-specific dimensions like Brand Trust pr
- NB-000097: From the perspective of the general public, nonprofit brand equity is a multidimensional construct c
- BT-000025: For nonprofit brands, Brand Trust is a distinct and more powerful explanatory dimension for stakehol
- BT-000026: The primary function of Brand Trust within the nonprofit brand equity framework is to reduce stakeho
- NB-000098: The dimensions of nonprofit brand equity are formed sequentially, with Brand Awareness acting as a n

**Accepted evidence (10):**
- EVID-001780: Direct applications of for-profit brand equity models are inadequate for the nonprofit sector.
- EVID-001781: A valid stakeholder-based nonprofit brand equity framework consists of three core dimensions: Nonpro
- EVID-001782: Brand Trust is a more precise and contextually relevant primary dimension for nonprofit brand equity
- EVID-001783: Brand awareness is a necessary precondition for the development of brand trust and commitment.
- EVID-001784: The primary function of brand trust for nonprofits is to reduce perceived risk for stakeholders, sig
- EVID-001785: Brand commitment converts a transactional relationship into a durable, emotional one, characterized 
- EVID-001786: The proposed nonprofit brand equity model is validated only from the perspective of the "general pub
- EVID-001787: The model measures perceptual and attitudinal dimensions of brand equity but does not link them to a
- EVID-001788: The empirical results of the study are specific to the German national and cultural context.
- EVID-001789: The study is cross-sectional, providing a static snapshot of brand equity at a single point in time.

**Accepted sources (2):**
- SRC-000276: Aaker, D. A. (1991)
- SRC-000263: Keller, K.L. (1993)

