---
concept: Profiling_Donors_of_Blood_Money_and_Time
review: REVIEW-000076
claim_count: 5
claim_ids:
- DS-000004
- DS-000005
- DS-000006
- DP-000001
- BA-000070
status: candidate
---

# Input Reviewed

-   **DS-000004**: The supporter population is segmented by single vs. multiple resource donation types.
-   **DS-000005**: Multi-behaviour donors have systematically different profiles from single-behaviour donors.
-   **DS-000006**: Modelling pro-social behaviours in isolation is methodologically flawed and risks misleading conclusions.
-   **DP-000001**: "Blood only" vs. "money only" donors have significantly different profiles, requiring different activation strategies.
-   **BA-000070**: An effective NPO architecture must be based on a segmentation of a supporter's complete behavioural portfolio.

# Core Theoretical Implication

The reviewed claims provide strong empirical and normative support for the "Behaviour Architecture" component of BEBA. The core implication is that pro-social behaviour is not a monolithic construct. Instead, the *pattern* of an individual's engagement across different behavioural types (e.g., donating money, time, blood) is a fundamental segmentation variable. This "behavioural portfolio" distinguishes supporter types with different profiles, who likely require different brand-enabled activation pathways. Ignoring this heterogeneity is a methodological flaw that leads to invalid inferences about supporter motivations and characteristics.

# BEBA Layer Affected

-   **Market Layer**: Directly affected by introducing a behaviour-based segmentation model (DS-000004, DS-000006). This refines the understanding of market structure.
-   **Individual Layer**: Directly affected by identifying distinct socio-demographic and psychographic profiles for different behavioural segments (DS-000005, DP-000001). This informs the concept of the "supporter" or "actor".
-   **Organisational Layer**: Directly affected by the normative principle that an NPO's strategy must account for this behavioural portfolio segmentation (BA-000070).

# Existing Claims Supported

These claims strongly support the foundational premise of BEBA: that pro-social behaviours form an interconnected system (an "architecture") rather than being isolated events. They validate any existing BEBA claims that:
-   Treat pro-sociality as a multi-dimensional construct.
-   Argue against single-behaviour research models.
-   Posit that different behaviours may be driven by different antecedents.
-   Justify the need for a holistic framework like BEBA to understand supporter value.

# Existing Claims Challenged

The claims do not challenge the core BEBA theory. Instead, they challenge the broader research status quo. Within the BEBA project, they would challenge any model, assumption, or existing claim that:
-   Uses a single, generic "support behaviour" as the primary dependent variable.
-   Is based on literature that models donation types (e.g., money vs. time) in isolation without accounting for the overlap.
-   Assumes a homogenous response to brand stimuli across all supporter types.

# New Candidate Claims

1.  **Claim**: The distinction between single-behaviour and multi-behaviour supporters is a primary axis for market segmentation, preceding segmentation based on demographics or psychographics alone.
2.  **Claim**: The effectiveness of brand equity in activating a specific pro-social behaviour is conditional upon the supporter's existing behavioural portfolio.
3.  **Claim (Methodological)**: To be considered valid within the BEBA framework, empirical models must account for the covariance between different pro-social behaviours, preferably by modelling them as simultaneous outcomes.

# Boundary Conditions

-   **Cultural Context**: The findings are based on a representative German sample (DS-000004, Note). The specific profiles and prevalence of segments may not generalize to other countries with different civic or philanthropic norms.
-   **Explanatory Power**: The identified profiles are statistical tendencies, not deterministic rules (DP-000001, Note: pseudo-R²=.06). This implies that while the segmentation is valid, demographic and psychographic variables alone are weak predictors, leaving significant variance to be explained by other factors, such as brand perceptions and relationships.

# Model Competition Implications

This set of claims provides a powerful criterion for model evaluation and competition. A BEBA model that jointly predicts a portfolio of behaviours (e.g., via a multivariate latent variable model) is theoretically and methodologically superior to a set of competing models that predict each behaviour in isolation. Any model predicting a single behaviour must now be seen as a special, simplified case whose limitations must be explicitly acknowledged.

# Ontology Candidate Implications

This integration suggests the need for new or refined concepts in the BEBA ontology:

1.  **New Concept Candidate**: `Behavioural Portfolio`.
    -   *Definition*: The set of distinct pro-social behaviours an individual has performed within a given timeframe.
    -   *Purpose*: To move beyond single-behaviour analysis and provide a basis for segmentation.

2.  **Refined Concept Candidate**: `Supporter Segment`.
    -   *Refinement*: Must include subtypes based on the structure of the Behavioural Portfolio, such as:
        -   `Single-Behaviour Supporter` (e.g., Money-Only, Time-Only)
        -   `Multi-Behaviour Supporter` (e.g., Money-and-Time)

3.  **Refined Relationship**: The relationship between `Brand Equity` and `Pro-Social Behaviour` should be moderated by the `Supporter Segment` (specifically, their `Behavioural Portfolio` type).

# Recommendation

1.  **Adopt**: Fully adopt the principle of behaviour-portfolio-based segmentation as a core tenet of the BEBA framework.
2.  **Update Ontology**: Create candidate files for the concept `Behavioural Portfolio` and refine the `Supporter Segment` concept to include `Single-Behaviour` and `Multi-Behaviour` types.
3.  **Update Methodology**: Formally document the methodological imperative (see New Candidate Claim 3) in the BEBA Knowledge Engineering Guide. All future empirical work under BEBA should strive to model multiple behavioural outcomes simultaneously.
4.  **Review Existing Claims**: Audit existing BEBA claims to identify any that rely on evidence from single-behaviour models and flag them for re-evaluation or qualification.

## Integration from REVIEW-000076

**Integrated:** 2026-07-13T19:04:21.710524+00:00

**Accepted claims (5):**
- DS-000004: The population of nonprofit supporters is not a single group but is composed of distinct behavioural
- DS-000005: Individuals who engage in multiple forms of donation (e.g., money and time) possess a socio-demograp
- DS-000006: Analysing different pro-social behaviours (e.g., donating money vs. donating time) in separate model
- DP-000001: The profile of a "blood only" donor (younger, higher risk-propensity, unmarried) is significantly di
- BA-000070: An effective Behaviour Architecture for an NPO must be based on a segmentation model that accounts f

**Accepted evidence (8):**
- EVID-001657: The population of nonprofit donors can be segmented into distinct profiles based on their past behav
- EVID-001658: Individuals who engage in multiple forms of donation possess sociodemographic and psychographic prof
- EVID-001659: Analysing different pro-social behaviours in separate models risks generating misleading donor profi
- EVID-001660: The profile of a "blood only" donor is characterized by being younger, having a higher risk-propensi
- EVID-001661: The "time only" donor segment is predominantly male.
- EVID-001662: The profile of monetary donors as being older, female, with higher incomes, and having children is c
- EVID-001663: Sociodemographic, psychographic, and health-related variables explain only a small portion of the va
- EVID-001664: Past pro-social behaviour is a powerful differentiator of donors' underlying characteristics.

**Accepted sources (1):**
- SRC-000380: Shehu et al. (2015)

