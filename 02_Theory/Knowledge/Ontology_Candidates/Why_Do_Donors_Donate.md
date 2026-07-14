---
concept: Why_Do_Donors_Donate
review: REVIEW-000092
theory_source: Theory_Integration/Why_Do_Donors_Donate.md
status: accepted
review_status: reviewed
reviewed_at: '2026-07-11T11:04:20.757954+00:00'
reviewed_by: human
---

# Concept

Donor Loyalty

## Canonical Definition

Donor Loyalty is a psychological construct representing an individual's deep-seated attitudinal commitment and behavioural intention to continue supporting a specific nonprofit organisation over time. It is an antecedent to, but distinct from, actual donation behaviour. Within the BEBA model, it is conceptualised as the primary proximal outcome of both transactional (satisfaction-based) and relational (identity-based) psychological pathways.

## Alternative Definitions

-   **Behavioural Loyalty:** Often defined purely by repeat behaviour (e.g., frequency or recency of donations). BEBA explicitly rejects this as a sufficient definition because it conflates intention with action and ignores the underlying psychological drivers. Claim DB-000009 provides evidence for the distinction.
-   **Composite Loyalty:** A multi-dimensional view combining attitudinal and behavioural components. While more nuanced, BEBA prioritises modelling the causal link from the attitudinal component (loyalty as intention) to the behavioural component (action) to better investigate the intention-action gap.

## BEBA Layer

Individual Layer. It is a psychological state of the individual donor.

## Parent Concepts

-   `Behavioural Intention`
-   `Brand Loyalty`
--   `Pro-Organisational Attitudes`

## Child Concepts

-   `Attitudinal Loyalty` (Primary BEBA focus)
-   `Intentional Loyalty`

## Related Concepts

-   `Donor Satisfaction`: A direct antecedent via the transactional pathway.
-   `Organizational Identification`: An indirect antecedent. Satisfaction influences Organizational Identification, which then initiates the identity-based pathway to loyalty.
-   `Donor Identity Salience`: The most proximal identity-based antecedent. It mediates the effect of Organizational Identification on Loyalty.
-   `Donation Behaviour`: The key behavioural outcome that Loyalty is intended to predict, but often does so weakly.

## Core Claims

-   Donor Loyalty is the outcome of at least two parallel psychological pathways: a transactional path driven by `Donor Satisfaction` and a relational path driven by identity constructs. (DL-000005)
-   The identity-based path to Loyalty follows a specific causal sequence: `Organizational Identification` -> `Donor Identity Salience` -> `Donor Loyalty`. (IS-000001)
-   `Donor Identity Salience` has a direct effect on Donor Loyalty and does not merely moderate the effect of `Organizational Identification`. (IS-000002)
-   Attitudinal Donor Loyalty is a necessary but insufficient condition for actual `Donation Behaviour`, with a notable gap between stated intention and performed action. (DB-000009)

## Evidence Base

The primary evidence is the synthesis of claims from `REVIEW-000092`, specifically claims: DS-000008, DL-000004, OI-000003, IS-000001, OI-000004, DL-000005, IS-000002, DL-000006, DB-000009. These claims provide empirical support for a dual-pathway model, the causal ordering of its components, and the distinction between loyalty and behaviour.

## Boundary Conditions

The relative influence of the pathways leading to Donor Loyalty is moderated by the **Behavioural Context**. The identity pathway is stronger for high-involvement, identity-relevant behaviours (e.g., monetary donations), while the satisfaction pathway may be more salient for lower-involvement behaviours (e.g., blood donations). (DL-000006)

## Competing Explanations

-   **Satisfaction-Only Models:** Models that posit satisfaction as the sole or primary driver of loyalty are incomplete, as they neglect the powerful, parallel identity-based pathway.
-   **Conflated Identity Models:** Models that fail to distinguish between `Organizational Identification` (social identity) and `Donor Identity Salience` (role identity) are misspecified. (OI-000004)
-   **Loyalty-as-Behaviour Models:** Models that use repeat donations as a direct proxy for the psychological construct of loyalty obscure the critical intention-action gap. (DB-000009)

## Operationalisations

Donor Loyalty is operationalised as a latent construct measured through multi-item scales assessing behavioural intentions. Typical items include:
-   Likelihood of donating to the organisation in the future.
-   Willingness to recommend the organisation to others.
-   Commitment to supporting the organisation over others.

## Existing Scales

Not specified in the provided synthesis. The source literature from `REVIEW-000092` must be consulted. Scales are likely adapted from the for-profit marketing literature (e.g., Zeithaml et al., 1996) and nonprofit-specific studies (e.g., Sargeant, 2001).

## Recommended ConstructLedger Updates

-   **`Construct: DonorLoyalty`**:
    -   **Status**: Core Mediator
    -   **Definition**: A behavioural intention reflecting a psychological commitment to an NPO.
    -   **Canonical Scale**: To be determined based on `REVIEW-000092`.
    -   **Notes**: Crucially distinguish from `DonationBehaviour`. Document its position as the terminal node of the satisfaction and identity pathways *before* the intention-action gap.

## Recommended Glossary Entry

**Donor Loyalty:** A behavioural intention rooted in a deep psychological commitment to continue supporting a nonprofit organisation. It is a key attitudinal outcome in the BEBA model, resulting from both satisfaction- and identity-based pathways, and serves as a direct antecedent to, but is empirically distinct from, actual donation behaviour.

## Confidence

High. The candidate is based on a synthesis of multiple empirical claims from a formal review (`REVIEW-000092`) that includes model comparisons and tests of discriminant validity.

## Review Recommendation

Strongly recommend adoption. The synthesis from `REVIEW-000092` provides a clear, evidence-based, and theoretically rich specification for how Donor Loyalty is formed. The key actions for the reviewer are to:
1.  Integrate the dual-pathway (Satisfaction, Identity) model into `01_THEORETICAL_MAP.md`.
2.  Formalise the specific causal chain (`Org. Identification` -> `Identity Salience` -> `Loyalty`).
3.  Use claim DB-000009 to justify the BEBA focus on the intention-action gap in core monograph chapters.
4.  Update the ontology and glossary to reflect the strict distinction between `Organizational Identification` and `Donor Identity Salience`.

## Integration from REVIEW-000092

**Integrated:** 2026-07-13T19:05:37.835712+00:00

**Accepted claims (3):**
- DS-000008: An organization's donor-oriented strategy positively influences donor satisfaction.
- DL-000004: Donor satisfaction is a significant positive driver of donor loyalty.
- OI-000003: Donor satisfaction is a causal antecedent to donor-nonprofit organizational identification.

**Accepted evidence (10):**
- EVID-001805: Organizational Identification and Identity Salience are empirically distinct constructs in the nonpr
- EVID-001806: Donor satisfaction is a causal antecedent to donor-nonprofit organizational identification.
- EVID-001807: Donor-nonprofit organizational identification is a causal antecedent to a donor's identity salience.
- EVID-001808: Both organizational identification and identity salience have direct, positive effects on donor loya
- EVID-001809: Donor identity salience functions as a direct predictor of donor loyalty, not as a moderator of the 
- EVID-001810: The relative influence of satisfaction versus identification constructs on donor loyalty is continge
- EVID-001811: The link from donor loyalty intentions to actual donation behavior is weak.
- EVID-001812: A donor-oriented strategy by a nonprofit organization positively influences donor satisfaction.
- EVID-001813: Donor satisfaction is a significant positive driver of donor loyalty.
- EVID-001814: Standard loyalty scale items, such as "willingness to donate more," may not be appropriate for donat

