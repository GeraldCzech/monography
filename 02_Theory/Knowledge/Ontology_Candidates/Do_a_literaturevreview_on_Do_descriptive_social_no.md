---
concept: Do_a_literaturevreview_on_Do_descriptive_social_no
review: REVIEW-000105
theory_source: Theory_Integration/Do_a_literaturevreview_on_Do_descriptive_social_no.md
status: accepted
review_status: reviewed
reviewed_at: '2026-07-13T20:40:10.222074+00:00'
reviewed_by: human
---

# Concept

Descriptive Social Norm

## Canonical Definition

The perception of which behaviours are typically performed by others in a particular situation. It refers to an individual's belief about "what is" commonly done, deriving its influence from the principle of social proof.

## Alternative Definitions

-   **Focus Theory of Normative Conduct (Cialdini et al., 1990):** Defines descriptive norms as what is typical or normal, contrasting them with injunctive norms (what is approved or disapproved of).
-   **Theory of Planned Behaviour (Ajzen, 1991):** This theory does not explicitly distinguish between descriptive and injunctive norms, often confounding them within the broader "Subjective Norm" construct, which is defined as perceived social pressure to perform or not perform a behaviour. BEBA explicitly rejects this confounded definition.

## BEBA Layer

Individual Layer. Descriptive norms are a cognitive input (a perception) that influences an individual's decision-making calculus.

## Parent Concepts

-   Social Influence

## Child Concepts

-   None identified in the current review.

## Related Concepts

-   **Injunctive Social Norm:** A sibling concept. Represents perceptions of what others approve or disapprove of (social approval). The review stresses their conceptual and empirical distinctness.
-   **Referent Group Proximity:** A key moderator. The perceived closeness of the group whose behaviour constitutes the norm.
-   **Donation Intention:** A primary outcome variable influenced by descriptive social norms.
-   **Subjective Norm (TPB):** A precursor concept from the Theory of Planned Behaviour that BEBA aims to deconstruct and improve upon by separating it into descriptive and injunctive components.

## Core Claims

Based on `REVIEW-000105`:

1.  **Modest Effect Size:** The influence of descriptive norms on pro-social behaviour is statistically significant but generally modest in size (Source: `DS-000009`).
2.  **Conceptual & Empirical Distinction:** Descriptive and injunctive social norms are distinct constructs with separate causal pathways to behavioural intention (Source: `DS-000011`).
3.  **Superiority to TPB:** Explicitly modelling descriptive norms adds explanatory power to models of intention over and above the classic Theory of Planned Behaviour's confounded "Subjective Norm" construct (Source: `DS-000012`).
4.  **Context-Dependent Strength:** In the context of charitable giving, the effect of descriptive norms on intention is typically weaker than the effect of injunctive norms (Source: `DS-000010`).

## Evidence Base

The primary evidence is derived from the synthesis of claims `DS-000009` through `DS-000014`. This includes meta-analytic findings and experimental studies in the pro-social and donation domains. A critical caveat from claim `DS-000014` is that the evidence base for social norms suffers from significant publication bias, likely leading to an overestimation of published effect sizes.

## Boundary Conditions

1.  **Referent Group Proximity:** The effect of descriptive norms is not universal; it is strengthened as the perceived psychological, social, or physical closeness of the referent group increases (Source: `DS-000013`).
2.  **Context Specificity:** The relative influence of descriptive versus injunctive norms is dependent on the behavioural domain.

## Competing Explanations

-   **Confounded Subjective Norm (TPB):** The classic TPB model offers a less granular explanation by combining descriptive and injunctive influences into a single predictor, which this evidence suggests is suboptimal.
-   **Norm-Centric Models:** Models that posit social norms as the primary or sole driver of behaviour are challenged by the evidence of modest effect sizes and the importance of other factors. BEBA positions norms as one component within a larger behavioural architecture.

## Operationalisations

Typically operationalised as a self-reported perception. Respondents are asked to estimate the frequency or prevalence of a specific behaviour among a specified referent group (e.g., "Out of 100 people like you, how many do you think donated to [Nonprofit X] last year?").

## Existing Scales

While many study-specific items exist, common scale formats include:
-   Frequency estimation questions (e.g., "How many of your close friends volunteer regularly?").
-   Percentage estimation questions (e.g., "What percentage of students at your university do you think participate in the annual food drive?").
-   Likert-type agreement scales (e.g., "Most people who are important to me would donate to this cause." - *Note: This wording can blur the line with injunctive norms and requires careful phrasing*).

## Recommended ConstructLedger Updates

-   **Action:** Create a new entry for `DescriptiveSocialNorm`.
-   **Definition:** Use the canonical definition provided above.
-   **Type:** Latent Variable (Perception).
-   **Relationships:**
    -   `is_distinct_from` InjunctiveSocialNorm.
    -   `influences` DonationIntention.
    -   `is_moderated_by` ReferentGroupProximity.
-   **Source:** `REVIEW-000105`.

## Recommended Glossary Entry

**Descriptive Social Norm:** An individual's perception of how commonly a behaviour is performed by others. It reflects the belief about "what is" popular or typical, and influences behaviour through the mechanism of social proof. It is distinct from an injunctive norm, which concerns beliefs about what behaviour is socially approved of.

## Confidence

**Medium-High.** The conceptual distinction from injunctive norms and the role of referent group proximity are well-supported. However, confidence in the precise effect size is lowered to "Medium" due to the strong evidence of publication bias in the wider literature (`DS-000014`), suggesting published effects are likely inflated.

## Review Recommendation

**Accept and Ingest.** This ontology candidate is well-supported by the provided review (`REVIEW-000105`). Recommend formalising this concept and proceeding with the recommendations from the review:
1.  Create the sibling ontology candidate for `InjunctiveSocialNorm` and the moderator candidate for `ReferentGroupProximity`.
2.  Add the new candidate claims (`C-NEW-SN-01` to `04`) to the claims repository.
3.  Update the `01_THEORETICAL_MAP.md` to reflect the distinct pathways.

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

