---
concept: BEBA_Evidence_Gaps_Literaturreview
review: REVIEW-000106
theory_source: Theory_Integration/BEBA_Evidence_Gaps_Literaturreview.md
status: accepted
review_status: reviewed
reviewed_at: '2026-07-13T21:26:28.768893+00:00'
reviewed_by: human
---

# Concept
`Injunctive Norm`

## Canonical Definition
An individual's perception of what constitutes commonly approved or disapproved conduct in a particular situation. It concerns what one is expected to do, or what one *ought* to do, based on the perceived preferences and potential sanctions of relevant others.

## Alternative Definitions
-   **Subjective Norm (TPB):** In Ajzen's (1991) Theory of Planned Behaviour, Subjective Norm is defined as "the perceived social pressure to perform or not to perform the behavior." While conceptually close, early operationalisations often conflated injunctive and descriptive elements. The BEBA model adopts the Cialdini, Reno, & Kallgren (1990) refinement, treating Injunctive Norm as a distinct component of social influence.

## BEBA Layer
`Individual Layer`

## Parent Concepts
-   `ont:SocialNorm`
-   `ont:PerceivedSocialPressure`

## Child Concepts
-   `ont:PrescriptiveNorm` (specifies what one *should* do)
-   `ont:ProscriptiveNorm` (specifies what one *should not* do)

## Related Concepts
-   `ont:DescriptiveNorm` (sibling concept; what is commonly done)
-   `ont:BehaviouralIntention` (Injunctive Norms are a primary antecedent)
-   `ont:Attitude` (parallel antecedent in the TPB framework)
-   `ont:PerceivedBehavioralControl` (parallel antecedent in the TPB framework)
-   `ont:AnticipatedAffect` (e.g., anticipated guilt or pride from conforming/deviating)

## Core Claims
-   Injunctive Norms are conceptually and empirically distinct from Descriptive Norms. (Source: `BEBA_Evidence_Gaps_Literaturreview`)
-   In the deliberative pathway of behaviour, Injunctive Norms are a stronger and more direct predictor of behavioural *intention* than Descriptive Norms are. (Source: `IN-000001`)
-   The influence of Injunctive Norms on behaviour is primarily mediated by `BehaviouralIntention`.

## Evidence Base
The review document `BEBA_Evidence_Gaps_Literaturreview` strongly supports the adoption of this differentiated construct, citing claim `IN-000001`. This finding aligns with the broader focus theory of normative conduct (Cialdini, Reno, & Kallgren, 1990) and subsequent meta-analyses in the TPB literature, which often find that carefully specified injunctive measures have robust predictive validity for intentions across various domains.

## Boundary Conditions
The influence of Injunctive Norms is likely moderated by:
-   **Salience of the normative source:** Effects are stronger when the referent group is psychologically important and salient in the decision context.
-   **Anonymity:** Effects may be weaker in situations where behaviour is private or anonymous, reducing the potential for social sanctions or rewards.
-   **Personal attitudes:** Effects may be attenuated when an individual holds a strong, conflicting personal attitude towards the behaviour.

(Note: These are theoretically derived; direct evidence from the provided literature review is not available for these specific moderators).

## Competing Explanations
-   **Unitary Social Norm Model:** A model that combines injunctive and descriptive elements into a single `SocialNorm` construct. The reviewed evidence (`IN-000001`) suggests this is a less precise and potentially misspecified model for predicting intention.
-   **Descriptive Norm Dominance Model:** In some contexts, particularly where a behaviour is ambiguous or novel, `DescriptiveNorms` (what others *do*) may be a more powerful driver of behaviour than `InjunctiveNorms` (what others *approve of*). BEBA must allow for testing the relative influence of both.

## Operationalisations
Typically measured via multi-item scales in surveys. Respondents are asked to rate their agreement with statements about the perceived expectations of specific or generalised others.

## Existing Scales
No single canonical scale, but items are typically adapted from the TPB measurement guidelines (e.g., Ajzen, 2006). Example items for a behaviour like "donating to Charity X":
-   "Most people who are important to me think I should donate to Charity X in the next month." (Strongly Disagree - Strongly Agree)
-   "My family and friends would approve of me donating to Charity X in the next month." (Strongly Disapprove - Strongly Approve)

## Recommended ConstructLedger Updates
-   **Create new entry:** `InjunctiveNorm`.
-   **Status:** Canonical.
-   **Measurement:** See 'Existing Scales' above.
-   **Flag for review:** Any existing `SocialNorm` or `SubjectiveNorm` constructs should be reviewed and potentially deprecated or redefined in light of this more specific concept.

## Recommended Glossary Entry
**Injunctive Norm:** An individual's perception of what valued others think they ought to do (or not do) in a given situation. It reflects perceived social pressure based on social approval or disapproval for a behaviour.

## Confidence
High. The distinction is theoretically robust and supported by empirical evidence cited in the BEBA research system (`IN-000001`, `BEBA_Evidence_Gaps_Literaturreview`). Adopting this concept improves the precision of the BEBA theoretical model.

## Review Recommendation
Adopt into canonical ontology. The introduction of this concept, alongside `DescriptiveNorm`, is a primary recommendation of the `BEBA_Evidence_Gaps_Literaturreview` (Review ID `REVIEW-000106`) and is critical for advancing model competition.

## Integration from REVIEW-000106

**Integrated:** 2026-07-13T21:04:46.959733+00:00

**Accepted claims (7):**
- IE-000002: The Austrian nonprofit sector is defined by a corporatist welfare partnership with the state, creati
- SS-000004: Social and health services form the economic core of the Austrian nonprofit sector in terms of value
- PF-000001: Service-providing nonprofits in Austria, particularly within the welfare sub-sector, are characteriz
- CR-000007: The 2008 financial crisis was associated with an increase in market concentration within the Austria
- CR-000008: The corporatist state-nonprofit partnership acts as a stabilizing financial and institutional force 
- A-000014: The adoption of performance-based contracting in Austrian social services has increased the power of
- BS-000021: In the Austrian context, the effectiveness of third-party charity labels is greater for lesser-known

**Accepted evidence (13):**
- EVID-001958: The Austrian nonprofit sector is consistently characterized as a corporatist or neo-corporatist welf
- EVID-001959: Social and health services form the economic core of the Austrian nonprofit sector in terms of value
- EVID-001960: Austrian service-providing nonprofits, especially in welfare, are heavily dependent on government fu
- EVID-001961: The current structure of the Austrian nonprofit sector is an outcome of deep historical and legal fo
- EVID-001962: After the 2008 financial crisis, Austria's nonprofit social-services sector experienced persistently
- EVID-001963: The claim that performance-based contracting has shifted power towards funders is well-supported in 
- EVID-001964: Coping mechanisms during the COVID-19 crisis centered on digitalization, new task forces, leadership
- EVID-001965: The effects of Austrian charity labels are real but modest, and their positive effect is strongest f
- EVID-001966: Environmental integration in large Austrian social-service and healthcare nonprofits remains in an e
- EVID-001967: There is a significant lack of research on nonprofit sub-sectors outside of social and health servic
- EVID-001968: The experiences, governance, and crisis adaptation of smaller, volunteer-run organizations are poorl
- EVID-001969: The consequences of state dependence for nonprofit autonomy, innovation capacity, and mission drift 
- EVID-001970: A persistent methodological gap in the research is the absence of a single legal-statistical system 

**Accepted sources (22):**
- SRC-000635: Wymer, W., & Gross, H. P. (2021)
- SRC-000096: Heitzmann and Simsa (2004)
- SRC-000636: Caviola, L., Schubert, S., & Greene, J. (2021)
- SRC-000637: Chapman et al. (2025)
- SRC-000638: Rivis & Sheeran (2003)
- SRC-000639: McEachan et al. (2016)
- SRC-000102: Neumayr (2015)
- SRC-000640: Helferich et al. (2023)
- SRC-000641: Melnyk et al. (2019)
- SRC-000642: Morren & Grinstein (2021)
- SRC-000643: Manning (2009)
- SRC-000644: Miller & Prentice (2016)
- SRC-000645: Albarracín et al. (2024)
- SRC-000646: Brewer et al. (2017)
- SRC-000647: Fischer & Karl (2021)
- SRC-000648: Melnyk et al. (2021)
- SRC-000649: Agerström, J., Carlsson, R., Nicklasson, L., & Guntell, L. (2016)
- SRC-000650: Alpizar, F., Carlsson, F., & Johansson-Stenman, O. (2008)
- SRC-000651: Chapman, C. M., Spence, J., Dixon, L., Smith, A. E., & Hornsey, M. J. (2025)
- SRC-000652: Ekström, M. (2012)
- SRC-000653: Knowles, S. R., Hyde, M. K., & White, K. M. (2012)
- SRC-000654: Krupka, E. L., & Croson, R. T. A. (2016)

