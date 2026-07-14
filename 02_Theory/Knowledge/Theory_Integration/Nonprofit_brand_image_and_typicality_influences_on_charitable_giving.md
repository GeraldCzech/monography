---
concept: Nonprofit_brand_image_and_typicality_influences_on_charitable_giving
review: REVIEW-000074
claim_count: 7
claim_ids:
- NB-000077
- NB-000078
- NB-000079
- NB-000080
- NB-000081
- NB-000082
- NB-000083
status: accepted
review_status: reviewed
reviewed_at: '2026-07-12T06:17:15.743801+00:00'
reviewed_by: human
---

# Input Reviewed

-   **NB-000077:** Definition of Nonprofit Brand Image as a multidimensional construct (Usefulness, Efficiency, Affect, Dynamism).
-   **NB-000078:** Positive effect of Nonprofit Brand Image on the intention to donate money.
-   **NB-000079:** Positive effect of Nonprofit Brand Image on the intention to donate time.
-   **NB-000080:** Stronger effect of the 'Efficiency' dimension on monetary donation intention.
-   **NB-000081:** Stronger effect of the 'Affect' dimension on time donation intention.
-   **NB-000082:** Positive effect of Nonprofit Brand Typicality on the intention to donate money.
-   **NB-000083:** Positive effect of Nonprofit Brand Typicality on the intention to donate time.

# Core Theoretical Implication

The primary implication is the validation of **behaviour-specific pathways** within the BEBA framework. The evidence demonstrates that the brand is not a monolithic driver of behaviour. Instead, different components of the brand's cognitive and affective architecture (e.g., 'Efficiency' vs. 'Affect') differentially enable distinct classes of supportive behaviour (financial vs. time-based). This moves the theory from a general "Brand -> Behaviour" model to a more nuanced "Specific Brand Component -> Specific Behaviour" architecture.

Furthermore, the strong, independent effect of **Brand Typicality** introduces a powerful cognitive heuristic into the BEBA model. This suggests that under uncertainty, behaviour can be enabled not just by a detailed, positive brand image but also by the brand's perceived prototypicality within its cause category, which simplifies choice and confers legitimacy.

# BEBA Layer Affected

**Individual Layer**. All claims relate to an individual's mental representations of the nonprofit brand (image, typicality) and how these representations influence their behavioural intentions.

# Existing Claims Supported

-   Supports the foundational BEBA proposition that a brand's architecture directly enables supportive behaviours.
-   Supports the idea that brand knowledge structures (i.e., brand image as a network of associations) are key antecedents to behavioural outcomes.
-   Strongly supports any existing claims that different forms of pro-social behaviour (e.g., donating money vs. time) are psychologically distinct and have different drivers.

# Existing Claims Challenged

-   Challenges a monolithic or unidimensional view of Nonprofit Brand Equity. If BEBA previously treated Brand Equity as a single score, this evidence forces a deconstruction into a multidimensional architecture with heterogeneous effects.
-   Challenges purely affect-driven models of nonprofit support. The superior predictive power of 'Efficiency' for financial donations suggests a more calculative, rational component is critical for certain behaviours.

# New Candidate Claims

Based on this review, the following claims should be considered for addition to the BEBA knowledge base:

1.  **C-BEBA-NEW-01:** The BEBA contains behaviour-specific pathways, where functional brand perceptions (e.g., Efficiency) more strongly enable financial support intentions, while affective brand perceptions (e.g., Affect) more strongly enable intentions for personal involvement (e.g., volunteering).
2.  **C-BEBA-NEW-02:** Brand Typicality functions as a distinct cognitive heuristic within the BEBA, enabling supportive behavioural intentions independently of detailed brand image by reducing cognitive load and conferring category-based legitimacy.
3.  **C-BEBA-NEW-03:** A comprehensive model of brand-enabled behaviour must account for the independent and complementary effects of both detailed brand image and general brand typicality.

# Boundary Conditions

-   **Context:** The findings originate from a study of large, well-known humanitarian aid charities in a French context. Their generalizability to small, niche, or non-humanitarian NPOs (e.g., arts, local advocacy) or to other cultural contexts is not established.
-   **Measurement:** The dependent variables are *behavioural intentions*, not observed behaviours. The well-known intention-behaviour gap is a significant boundary condition.

# Model Competition Implications

This evidence provides a strong basis for specifying a more complex, and likely more accurate, model of brand-enabled behaviour to compete with simpler alternatives.

-   **Model A (Simple):** `Overall Brand Equity -> Supportive Behaviour`
-   **Model B (Refined, based on this input):** A structural model where `[Efficiency, Affect, Typicality]` are distinct latent variables that differentially predict two distinct outcome variables, `[Intention to Donate Money, Intention to Donate Time]`.

The findings strongly suggest Model B will have superior explanatory power, providing a clear avenue for empirical testing within the BEBA project.

# Ontology Candidate Implications

This review necessitates the creation or refinement of several concepts within the BEBA ontology:

-   **New Concept Candidate:** `Nonprofit Brand Image`.
    -   **Properties/Sub-Concepts:** Must be defined as a multidimensional construct composed of `Usefulness`, `Efficiency`, `Affect`, and `Dynamism`.
-   **New Concept Candidate:** `Nonprofit Brand Typicality`.
    -   **Definition:** To be defined as the degree to which a brand is perceived as a prototypical example of its cause category.
-   **New Relationship Types:** The ontology should be able to capture not just `positivelyPredicts` but also a comparative relationship like `hasStrongerPredictiveEffectOn`.
    -   Example: `(NonprofitBrandImage.Efficiency) -[hasStrongerPredictiveEffectOn]-> (IntentionToDonateMoney)` compared to `(IntentionToDonateTime)`.

# Recommendation

1.  **Create Candidate Concept Files:** Generate new markdown files in the ontology candidates directory for `Nonprofit Brand Image` (specifying its dimensions) and `Nonprofit Brand Typicality`.
2.  **Draft New Claims:** Formally write up the "New Candidate Claims" (C-BEBA-NEW-01 to 03) and add them to the claims repository for tracking and future testing.
3.  **Update Theoretical Map:** Revise `01_THEORETICAL_MAP.md` to include these new constructs and visually represent the behaviour-specific pathways from brand image dimensions to different support intentions.
4.  **Propose ADR:** An Architectural Decision Record (ADR) should be proposed to formally adopt the "behaviour-specific pathways" principle as a core tenet of the BEBA theory. This refines the theory from a general brand equity model to a more precise behavioural architecture.
5.  **Log in ConstructLedger:** Note `Nonprofit Brand Image` and `Nonprofit Brand Typicality` as constructs with available, validated scales (from the source literature), noting the context of their validation (French, large NPOs).

## Integration from REVIEW-000074

**Integrated:** 2026-07-13T19:04:12.254328+00:00

**Accepted claims (7):**
- NB-000077: The brand image of a nonprofit organization is a multidimensional construct composed of Usefulness, 
- NB-000078: A positive nonprofit brand image is a significant positive predictor of an individual's intention to
- NB-000079: A positive nonprofit brand image is a significant positive predictor of an individual's intention to
- NB-000080: The 'Efficiency' dimension of nonprofit brand image has a stronger positive effect on the intention 
- NB-000081: The 'Affect' dimension of nonprofit brand image has a stronger positive effect on the intention to d
- NB-000082: The perceived typicality of a nonprofit within its cause category is a significant positive predicto
- NB-000083: The perceived typicality of a nonprofit within its cause category is a significant positive predicto

**Accepted evidence (9):**
- EVID-001635: Nonprofit brand image is a multidimensional construct comprising four core dimensions: Usefulness, E
- EVID-001636: A four-dimensional brand image model explains 31% of the variance in intentions to give money and 24
- EVID-001637: Brand typicality independently explains 29% of the variance in intentions to donate money and 23% of
- EVID-001638: The 'Efficiency' dimension of brand image is a stronger predictor of intentions to donate money comp
- EVID-001639: The 'Affect' dimension of brand image is a stronger predictor of intentions to donate time compared 
- EVID-001640: Donating time is theorised as a more emotionally involving decision, whereas donating money is frame
- EVID-001641: Previous nonprofit brand scales are argued to be overly derived from corporate brand reputation lite
- EVID-001642: The explanatory power of brand image for giving intentions (R² = .31) appears substantially higher t
- EVID-001643: Higher perceived typicality of a nonprofit relative to its cause category leads to it being a more r

**Accepted sources (8):**
- SRC-000359: Michel, G., & Rieunier, S. (2012)
- SRC-000360: Rosch, E. (1978)
- SRC-000263: Keller, K.L. (1993)
- SRC-000361: Liu, W., & Aaker, J. (2008)
- SRC-000362: Bennett, R., & Gabriel, H. (2003)
- SRC-000363: Venable, B. T., Rose, G. M., Bush, V. D., & Gilbert, F. W. (2005)
- SRC-000364: Sargeant, A., West, D. C., & Ford, J. B. (2008)
- SRC-000276: Aaker, D. A. (1991)

