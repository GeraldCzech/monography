---
concept: Is_TPB_supported_for_charitable_donation_intention
review: REVIEW-000105
theory_source: Theory_Integration/Is_TPB_supported_for_charitable_donation_intention.md
status: accepted
review_status: reviewed
reviewed_at: '2026-07-13T20:43:48.014328+00:00'
reviewed_by: human
---

# Concept

Intention-Behaviour Gap

## Canonical Definition

The observable discrepancy between an individual's stated intention to perform a specific behaviour (e.g., charitable donation) and their subsequent execution of that behaviour. It is a well-documented phenomenon where positive intentions do not reliably translate into corresponding actions.

## Alternative Definitions

- Value-Action Gap
- Attitude-Behaviour Gap (a related, but broader and historically distinct concept)

## BEBA Layer

**Individual Layer.** The gap is a psychological and behavioural phenomenon that manifests at the level of the individual. The proposed BEBA solution to bridge this gap (the "Architecture") is an Organisational Layer concept that acts upon the Individual Layer.

## Parent Concepts

- `Implementation Failure`
- `Prediction Error` (within psychological models of behaviour)

## Child Concepts

- `Donation Intention-Behaviour Gap`
- `Volunteering Intention-Behaviour Gap`

## Related Concepts

- `Donation Intention` (The antecedent that fails to fully predict the outcome)
- `Donation Behaviour` (The outcome that is not fully explained by intention)
- `BEBA (Behaviour Architecture)` (The core theoretical construct in BEBA designed to bridge this gap)
- `Implementation Intentions` (A related self-regulatory strategy for closing the gap)
- `Perceived Behavioural Control` (A partial explanation for the gap; low PBC can inhibit the translation of intention into action)

## Core Claims

1.  **IB-000032:** There is a significant, well-documented gap between the intention to donate and actual donation behaviour.
2.  **C-BEBA-TPB-03 (Candidate):** The "Architecture" component of BEBA is specifically designed to bridge the empirically established gap between Donation Intention and Donation Behaviour.

## Evidence Base

The existence of the gap is strongly supported by meta-analytic evidence in social psychology and is explicitly referenced in the synthesis document under claim **IB-000032**. The input review document positions this gap as a core justification for the BEBA framework.

## Boundary Conditions

The reviewed literature does not specify boundary conditions for the gap itself, but it implies that the gap may be larger when antecedents of intention (like Perceived Behavioural Control) are weak. The BEBA framework hypothesises that the gap is smaller in the presence of an effective Behaviour Architecture provided by a nonprofit brand.

## Competing Explanations

- **BEBA Explanation:** The gap exists due to a lack of an effective "architecture" that facilitates the translation of intention into behaviour.
- **Alternative Psychological Explanations:** The gap can be attributed to factors such as forgetting, procrastination, unstable intentions, competing goals, or a failure to form concrete implementation plans.

## Operationalisations

The gap is operationalised as the statistical residual in models predicting behaviour from intention. It can be observed by:

1.  The correlation coefficient `r(Intention, Behaviour)` being substantially less than 1.0.
2.  The proportion of variance in Behaviour explained by Intention (R²) in a regression model.
3.  Directly tracking the percentage of individuals with a positive intention at Time 1 who fail to perform the behaviour by Time 2.

## Existing Scales

Not applicable. The Intention-Behaviour Gap is a derived phenomenon representing the difference between two separate measurements (intention and behaviour); it is not a latent construct measured by a psychometric scale.

## Recommended ConstructLedger Updates

- Ensure that `Donation Intention` and `Donation Behaviour` have canonical entries in the `ConstructLedger`, as they are the two components required to measure the gap.
- No entry is required for the "Gap" itself, as it is a derived outcome.

## Recommended Glossary Entry

**Intention-Behaviour Gap:** A common phenomenon where an individual's stated intention to act does not reliably or fully translate into the performance of that action. In the context of BEBA, it refers specifically to the discrepancy between the intention to donate and actual donation behaviour, which the 'Behaviour Architecture' component of the framework aims to bridge.

## Confidence

High. The existence of the Intention-Behaviour Gap is a robust and widely replicated finding in behavioural science. It serves as a central pillar for the justification of the BEBA framework.

## Review Recommendation

Accept and formalise. This concept is a cornerstone of the BEBA research problem. It justifies the "Architecture" component of the theory and is essential for framing model competition. It should be promoted from a candidate to a canonical concept file located at `02_Theory/Concepts/Intention-Behaviour_Gap.md`.
