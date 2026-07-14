---
concept: 1_How_does_nonprofit_brand_equity_change_over_t
review: REVIEW-000099
claim_count: 5
claim_ids:
- NB-000100
- BF-000015
- ST-000001
- BA-000075
- BA-000076
status: accepted
review_status: reviewed
reviewed_at: '2026-07-11T21:32:56.149375+00:00'
reviewed_by: human
---

# Input Reviewed

The following five candidate claims have been reviewed for integration into the BEBA theory:

1.  **NB-000100 (Nonprofit Brand Equity Dynamics):** The influence of brand equity drivers on donor behaviour changes over multi-year periods.
2.  **BF-000015 (Behavioural Feedback Loop):** Donating positively reinforces brand equity perceptions, mediated by commitment and brand-self congruence.
3.  **ST-000001 (Signalling Theory):** Brand equity evaluation is a nonlinear function of signals, with asymmetric and substitution effects.
4.  **BA-000075 (Brand Associations):** Higher-order associations (e.g., values, mission congruence) are stronger predictors of sustained support than lower-order ones (e.g., awareness).
5.  **BA-000076 (Brand Activism):** The effect of sociopolitical advocacy on brand equity is moderated by stakeholders' perception of its authenticity.

# Core Theoretical Implication

Collectively, these claims mandate that BEBA must be conceptualized as a **dynamic, adaptive, and non-linear system**, rather than a static, linear, or unidirectional model. The core implication is that the "architecture" in BEBA is not fixed; it is a system whose component weights, relationships, and even structure evolve over time in response to stakeholder behaviour and perceptions of the nonprofit's actions. Simple, additive models of brand equity are insufficient to capture the phenomena described.

# BEBA Layer Affected

These claims affect multiple layers of the BEBA model:

-   **Individual Layer:** The cognitive and psychological mechanisms are heavily implicated. This includes the non-linear integration of signals (`ST-000001`), the hierarchical structure of brand associations (`BA-000075`), and the behavioural feedback loop that reinforces perceptions (`BF-000015`).
-   **Market Layer:** The long-term evolution of driver importance (`NB-000100`) and the contextual moderation of brand actions like advocacy (`BA-000076`) are market-level phenomena that shape the environment in which individual-level processes occur.

# Existing Claims Supported

These claims provide substantial support for the core tenets of BEBA:

-   They affirm the central premise that BEBA is a *Behaviour Architecture*, requiring a more complex specification than a simple list of antecedents.
-   `BF-000015` directly specifies the bidirectional feedback mechanism that is a cornerstone of the BEBA concept, moving beyond a simple "brand -> behaviour" pathway.
-   `BA-000075` supports the idea that the *structure* of brand knowledge matters, justifying the need for an "architecture" view.
-   `ST-000001` and `BA-000076` reinforce the idea that the link between nonprofit actions (signals) and stakeholder perception is not direct but is filtered, interpreted, and integrated in complex ways.

# Existing Claims Challenged

These claims do not fundamentally challenge the BEBA theory itself. Instead, they challenge and guard against **oversimplified operationalizations** of BEBA. Specifically, they challenge any model that is:

-   **Static:** `NB-000100` requires that any BEBA model must account for parameter variance over time. A cross-sectional model is insufficient as a complete representation.
-   **Unidirectional:** `BF-000015` makes a simple recursive path model (Brand Equity -> Behaviour) untenable.
-   **Additive/Linear:** `ST-000001` and `BA-000075` challenge the use of simple composite scores or first-order factor models where all indicators or lower-order constructs are weighted equally.
-   **Acontextual:** `BA-000076` challenges any model that ignores key moderators, such as stakeholder perceptions of organizational actions.

# New Candidate Claims

The five input documents are themselves the primary new candidate claims. A synthesized, higher-order claim emerging from this review is proposed:

-   **SYS-000001 (BEBA System Dynamics):** *The behavioural effectiveness of a nonprofit brand is an emergent property of a dynamic system characterized by (a) feedback loops between stakeholder behaviour and brand perceptions, (b) a hierarchical and non-linear integration of brand signals, and (c) parameters that are contingent on both time and the perceived authenticity of brand actions.*

# Boundary Conditions

Several new boundary conditions and moderators are introduced:

1.  **Temporal Frame:** The relevance of specific BEBA components is time-dependent. Short-term and long-term models may require different weightings (`NB-000100`).
2.  **Perceived Authenticity:** The relationship between a brand's advocacy actions and its equity is bounded by stakeholder perception of authenticity. Inauthentic actions may degrade equity (`BA-000076`).
3.  **Giving Context:** The non-linear signalling effects have been primarily observed in online crowdfunding contexts, which may not fully generalize to all forms of nonprofit support (`ST-000001` Note).

# Model Competition Implications

This integration significantly strengthens BEBA's position relative to competing theoretical models:

-   **vs. Simple CBBE Models:** BEBA is differentiated by its explicit inclusion of feedback loops (`BF-000015`) and hierarchical structure (`BA-000075`), moving beyond a simple "brand knowledge -> response" sequence.
-   **vs. Static SEM Models:** BEBA, by incorporating temporal dynamics (`NB-000100`) and feedback, positions itself as a more realistic, longitudinal framework, creating a clear case for research designs like panel studies or dynamic panel models over one-shot cross-sectional surveys.
-   **vs. Composite Index Models:** BEBA's emphasis on non-linear, asymmetric, and substitution effects (`ST-000001`) argues for more sophisticated measurement and modelling approaches (e.g., choice experiments, fuzzy-set QCA, or non-linear SEM) over simple summated scales.

# Ontology Candidate Implications

This review necessitates the creation or refinement of several concepts in the BEBA ontology:

-   **New Concept Candidates:**
    -   `Perceived Authenticity` (as a moderating construct).
    -   `Behavioural Feedback Loop` (as a core mechanism/process).
    -   `Brand Activism` (as a specific type of `Brand Action` or `Brand Signal`).
-   **Refinement of Existing Concepts:**
    -   `Brand Associations` must be structured hierarchically into `Lower-Order Brand Associations` (e.g., Awareness, Recognition) and `Higher-Order Brand Associations` (e.g., Brand-Self Congruence, Perceived Mission Authenticity).
    -   `Brand Signal` must have properties to account for `Signal Asymmetry` and `Signal Substitution`.
-   **New Relationships:**
    -   A `moderates` relationship is needed between `Perceived Authenticity` and the `Brand Action -> Brand Equity` path.
    -   A `reinforces` relationship type is needed to model the `Behaviour -> Brand Equity` feedback loop.
    -   Relationships within the BEBA model must be capable of having a `time-varying` property.

# Recommendation

1.  **Accept Claims:** Formally add the five candidate claims (`NB-000100`, `BF-000015`, `ST-000001`, `BA-000075`, `BA-000076`) to the project's `Claim` registry.
2.  **Create Ontology Candidates:** Initiate new concept workspace files for `Perceived Authenticity` and `Behavioural Feedback Loop`. Begin work on a revised, hierarchical concept file for `Brand Associations`.
3.  **Draft Architectural Decision Record (ADR):** Propose an ADR titled "Adoption of a Dynamic, Non-Linear System Framework for BEBA". This ADR will formally state that any operationalization of BEBA must account for feedback loops, parameter instability over time, and non-additive signal integration. This has significant implications for the empirical pipeline.
4.  **Update Theoretical Map:** Revise `01_THEORETICAL_MAP.md` to visually and textually represent the feedback loop from behaviour back to brand equity, and to explicitly mark the `Brand Action -> Equity` link as being moderated by contextual perceptions.

## Integration from REVIEW-000099

**Integrated:** 2026-07-13T19:06:08.732180+00:00

**Accepted claims (5):**
- NB-000100: The relative influence of core brand equity drivers on donor behaviour changes systematically over m
- BF-000015: The act of donating to a nonprofit organization positively reinforces the donor's perception of bran
- ST-000001: Stakeholder evaluation of nonprofit brand equity is a nonlinear function of its constituent signals,
- BA-000075: Higher-order brand associations are stronger predictors of sustained donor support than lower-order 
- BA-000076: The impact of a nonprofit's sociopolitical advocacy on its brand equity is contingent on stakeholder

**Accepted evidence (11):**
- EVID-001880: There is a significant lack of direct empirical evidence from true panel data studies on the longitu
- EVID-001881: Donor behavior is theorized to create a positive feedback loop that reinforces brand equity through 
- EVID-001882: Brand equity is built through the cumulative perception of various brand signals, and their effects 
- EVID-001883: In commercial brands, a longitudinal panel study found that the relevance of brand personality trait
- EVID-001884: Higher-order brand associations like reputation, differentiation, and identification are more signif
- EVID-001885: The impact of nonprofit brand activism on brand equity is complex and moderated by stakeholder perce
- EVID-001886: On charitable crowdfunding platforms, the disclosure of donor badges improves performance, but the e
- EVID-001887: The reviewed literature does not contain direct evidence on how the temporal distance of a charitabl
- EVID-001888: Existing nonprofit brand equity indices and models have limited cross-cultural robustness, often bei
- EVID-001889: In charitable crowdfunding, signals like images and updates exhibit nonlinear and substitution effec
- EVID-001890: In cause-campaign research, consumer engagement can persist after a brand's affiliation with the cau

**Accepted sources (11):**
- SRC-000339: Boenigk, S., & Becker, A. (2016)
- SRC-000552: Crawford, E. C., & Jackson, J. (2025)
- SRC-000583: Gardberg, N. A., Zyglidopoulos, S. C., Symeou, P., & Schepers, D. H. (2019)
- SRC-000578: Ghoorah, U., Mariyani-Squire, E., & Amin, S. Z. (2025)
- SRC-000584: Gleasure, R., & Feller, J. (2016)
- SRC-000585: Holiday, S., Hayes, J. L., Britt, B. C., & Lyu, Y. (2020)
- SRC-000533: Huang, S.-L., & Ku, H.-H. (2016)
- SRC-000586: Luffarelli, J., Delre, S., & Landgraf, P. (2022)
- SRC-000587: Parris, D., & Guzmán, F. (2022)
- SRC-000588: Rama, A., Ali, H., & Syafruddin, S. (2026)
- SRC-000589: Wu, X., Wu, T., Guo, X., & Yang, H. (2025)

