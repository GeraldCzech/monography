---
concept: 1_Does_donor_identity_salience_predict_charitab
review: REVIEW-000093
theory_source: Theory_Integration/1_Does_donor_identity_salience_predict_charitab.md
status: accepted
review_status: reviewed
reviewed_at: '2026-07-12T17:30:48.893300+00:00'
reviewed_by: human
---

# Concept

Donor Identity Salience

## Canonical Definition

Donor Identity Salience is a temporary psychological state reflecting the degree to which an individual's role identity as a "donor" is activated and prominent in their consciousness at a specific point in time. It is distinct from Donor Identity as a chronic trait, representing the situational accessibility of that identity.

## Alternative Definitions

In some literature, "salience" is used interchangeably with identity "importance" or "centrality". Within the BEBA framework, these are treated as distinct. Importance and centrality are properties of the chronic `DonorIdentity` trait, whereas salience is a momentary state variable, subject to situational influence.

## BEBA Layer

-   **Primary:** Individual Layer. It is a cognitive-affective state within the individual.
-   **Interacts with:** Situational Layer. It is often triggered or enhanced by external cues (e.g., brand communications, fundraising appeals) present in the decision environment.

## Parent Concepts

-   `beba:RoleIdentitySalience` (The momentary activation of any specific behavioral role identity).

## Child Concepts

-   None identified at this stage.

## Related Concepts

-   `beba:DonorIdentity` (The chronic, trait-level self-concept of being a donor, which is a prerequisite for salience).
-   `beba:OrganizationalIdentification` (Can be activated concurrently; salience of donor identity might be NPO-specific).
-   `beba:BrandCues` (A primary antecedent; brand artifacts often serve to prime and increase donor identity salience).
-   `beba:ProsocialIntention` (A primary consequence of heightened donor identity salience).

## Core Claims

-   **DI-000009:** Donor identity salience is a significant positive predictor of charitable giving intentions.
-   **DI-000011:** Externally priming a donor identity can increase its salience and subsequent prosocial behavior.
-   **C-BEBA-ID-03 (Candidate):** A key function of a nonprofit brand is to serve as a situational cue that increases the salience of specific, behavior-relevant role identities.

## Evidence Base

The primary evidence is derived from the synthesis in `REVIEW-000093`, which established the above claims. The concept is well-supported in identity theory and has been demonstrated empirically in prosocial behavior literature.

## Boundary Conditions

-   **Pre-existing Identity:** The effect of priming on salience is bounded by the existence and strength of the underlying chronic `DonorIdentity`. An identity that does not exist cannot be made salient.
-   **Situational Conflict:** The effect of donor identity salience may be attenuated if other, competing identities (e.g., "frugal saver," "parent providing for family") are made more salient by the immediate context.
-   **Time Decay:** The increase in salience from an external prime is transient and will likely decay over time.

## Competing Explanations

-   **Emotional Arousal:** Prosocial behavior may be driven primarily by an immediate, affective response (e.g., empathy, pity) to a stimulus, rather than the cognitive activation of a self-concept.
-   **Rational Calculation:** Behavior may result from a deliberative cost-benefit analysis (e.g., perceived impact, tax incentives) that does not require identity activation.
-   **Social Norms:** Behavior could be a response to perceived social pressure or descriptive norms in the situation, independent of an individual's internal identity structure.

## Operationalisations

This concept is most frequently operationalised as a manipulated independent variable in experimental designs.
-   **Experimental Manipulation:** Participants are exposed to priming stimuli intended to activate the donor identity (e.g., writing about a time they helped, seeing words related to giving) versus a neutral control condition. The behavioral outcome is then compared between groups.
-   **Situational Measurement:** Can be measured post-manipulation or in surveys using items that capture the momentary state, such as "To what extent do you think of yourself as a donor right now?".

## Existing Scales

As a state, this is not typically measured with multi-item psychometric scales, which are designed for traits. Measurement relies on single-item, ad-hoc questions adapted to the specific context (e.g., using a Likert or slider scale for "How much do you feel like a donor at this moment?").

## Recommended ConstructLedger Updates

Add `DonorIdentitySalience` as a new entry.
-   **Type:** Construct (State)
-   **Definition:** The momentary, situational activation of an individual's self-concept as a donor.
-   **Canonical Measurement:** Experimental Manipulation (Priming vs. Control).
-   **Notes:** Distinguish clearly from `DonorIdentity` (Trait). Key mechanism for the "Brand-Enabled" component of BEBA.

## Recommended Glossary Entry

**Donor Identity Salience:** A temporary psychological state where a person's identity as a "donor" is consciously accessible and prominent. This state can be triggered by external cues, such as brand messages, and is a key predictor of immediate prosocial intentions and behavior.

## Confidence

High. The concept of identity salience is well-established in social psychology, and the reviewed claims (DI-000009, DI-000011) provide direct evidence for its applicability and importance in the nonprofit context.

## Review Recommendation

Accept for inclusion in the canonical ontology. It is crucial for operationalizing the "Brand-Enabled" aspect of the BEBA theory, providing a specific mechanism by which brand touchpoints in the **Situational Layer** activate psychological predispositions in the **Individual Layer** to produce behavior. This candidate should be reviewed in conjunction with the broader `OC-Identity_v1.md` proposal to ensure a coherent identity framework.

## Integration from REVIEW-000093

**Integrated:** 2026-07-13T19:05:42.632968+00:00

**Accepted claims (9):**
- DI-000009: An increase in the salience of a specific "donor" identity is positively associated with an individu
- DI-000010: Behavior-specific identity salience is a stronger predictor of corresponding prosocial behavior than
- DI-000011: Externally priming a relevant donor identity at the point of decision increases giving behavior.
- DI-000012: Donor identity salience mediates the relationship between past relationship satisfaction and future 
- OI-000005: Higher organizational identification with a nonprofit is positively associated with higher donation 
- OI-000006: Higher organizational identification with a nonprofit is positively associated with non-monetary pro
- OI-000007: Organizational identification mediates the positive relationship between a stakeholder's perception 
- SI-000009: The positive association between social identification and charitable giving is stronger for self-re
- PI-000004: In nonprofit contexts with a strong member-service component, organizational identification is posit

**Accepted evidence (10):**
- EVID-001815: A meta-analysis found a medium-sized positive association between social identification and charitab
- EVID-001816: The predictive power of identity constructs is consistently stronger for self-reported giving intent
- EVID-001817: Higher organizational identification with a nonprofit is positively associated with higher donation 
- EVID-001818: Behavior-specific donor identities (e.g., "blood donor") are better predictors of related charitable
- EVID-001819: In nonprofit service contexts with a strong member community, organizational identification is posit
- EVID-001820: Externally activating a relevant identity through primes (e.g., reminding someone of their prior don
- EVID-001821: Perceived relationship investment from a nonprofit increases organizational identification, which in
- EVID-001822: Organizational identification is positively associated with a range of non-monetary prosocial behavi
- EVID-001823: Social Identity Theory posits that individuals act in ways that confirm and are congruent with their
- EVID-001824: Identity salience can mediate the relationship between past relationship satisfaction and future don

**Accepted sources (12):**
- SRC-000516: Chapman, C., Spence, J. L., Hornsey, M., & Dixon, L. J. (2025)
- SRC-000517: White, K., Poulsen, B. E., & Hyde, M. K. (2017)
- SRC-000518: Tidwell, M. (2005)
- SRC-000519: Taylor, J. A., & Miller Stevens, K. (2018)
- SRC-000520: Millán, Á., Retamosa, M., & Carranza, R. (2023)
- SRC-000521: Lai, C.-S., & Nguyen, D. T. (2024)
- SRC-000522: Kessler, J. B., & Milkman, K. L. (2016)
- SRC-000523: Fang, D., Fombelle, P. W., & Bolton, R. N. (2020)
- SRC-000524: Kim, H. H., & Han, E. (2020)
- SRC-000422: Boenigk, S., & Helmig, B. (2013)
- SRC-000526: Chell, K., Mortimer, G., Masser, B., & Russell–Bennett, R. (2021)
- SRC-000527: Gold, J. (2023)

