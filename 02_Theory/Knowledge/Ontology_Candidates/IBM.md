---
concept: IBM
review: REVIEW-000010
theory_source: Theory_Integration/IBM.md
status: accepted
review_status: reviewed
reviewed_at: '2026-07-13T18:45:00.852010+00:00'
reviewed_by: human
---

# Concept

**IBM — Intention-Based Model**

## Canonical Definition

An **Intention-Based Model** is a behavioural explanation model in which donation behaviour is primarily explained through donation intention, with intention formed by antecedents such as attitude toward donating, perceived norms, perceived behavioural control, moral norms, trust, and prior behaviour.

In BEBA, IBM should be treated as a **baseline behavioural architecture**, not as a complete explanation of nonprofit brand-enabled behaviour.

## Alternative Definitions

- **Theory of Planned Behaviour-based donation model:** A model explaining donation intention through attitude, subjective norm, and perceived behavioural control.
- **Donation intention model:** A model focused on the formation of intention to donate, sometimes without modelling actual donation behaviour.
- **Extended intention model:** A model that adds moral norms, trust, past behaviour, cultural context, or digital platform trust to standard intention-based predictors.

## BEBA Layer

**Primary layer:** Individual  
**Secondary layers:**  
- Societal, where cultural context moderates intention pathways.  
- Technological / Infrastructure context, where platform trust affects digital donation intention.

## Parent Concepts

- Behavioural Explanation Model
- Donation Behaviour Architecture
- Individual-Level Behavioural Mechanism

## Child Concepts

- Donation Intention
- Donation Behaviour
- Attitude toward Donating
- Subjective Norm / Social Norm
- Moral Norm
- Perceived Behavioural Control
- Nonprofit Trust
- Platform Trust
- Past Donation Behaviour
- Intention-Behaviour Gap

## Related Concepts

- Nonprofit Brand Trust
- Brand-Enabled Behaviour
- Uncertainty Reduction
- Behavioural Continuity
- Digital Giving
- Cultural Context
- Moral Obligation
- Donor Experience

## Core Claims

1. Donation intention is positively predicted by attitude toward donating, perceived norms, and perceived behavioural control.  
   **Supported by:** DI-000002

2. Moral norms may improve explanation beyond subjective social norms.  
   **Supported by:** MN-000001

3. Donation intention predicts donation behaviour but does not fully explain actual donation behaviour.  
   **Supported by:** IB-000003

4. Trust in a charitable organization is a distinct positive antecedent of donation intention.  
   **Supported by:** NT-000001

5. Past donation behaviour improves explanation of future donation intention and behaviour.  
   **Supported by:** PD-000001

6. Cultural context may moderate the predictive validity of intention-based donation models.  
   **Supported by:** CC-000002

7. In digital donation contexts, platform trust predicts donation intention in addition to organizational trust.  
   **Supported by:** PT-000001

## Evidence Base

The evidence base consists of the reviewed claim set:

- DI-000002
- MN-000001
- IB-000003
- NT-000001
- PD-000001
- CC-000002
- PT-000001

The claim set supports IBM as a useful behavioural baseline for BEBA, especially for modelling donation intention. However, it also shows that intention-based explanation is incomplete unless the model distinguishes intention from enacted donation behaviour and includes uncertainty, trust, behavioural history, cultural context, and digital infrastructure conditions where relevant.

## Boundary Conditions

1. **Intention-behaviour gap**  
   Donation intention does not automatically become donation behaviour.

2. **Digital giving context**  
   Platform trust becomes relevant when donations are mediated by online platforms, crowdfunding systems, or digital payment infrastructures.

3. **Cultural context**  
   The strength of intention-based pathways may vary across cultural settings. Current confidence should remain cautious.

4. **Prior donor experience**  
   First-time, occasional, repeat, and habitual donors may differ in how intention is formed and enacted.

5. **Moral salience of the cause**  
   Moral norms may be more relevant when the donation context is perceived as ethically urgent or personally meaningful. This requires further evidence.

## Competing Explanations

1. **Brand-centric explanation**  
   Donation behaviour may be attributed primarily to nonprofit brand equity. The reviewed claims challenge this by showing that intention, norms, control, trust, and past behaviour also matter.

2. **Standard TPB-style explanation**  
   Attitude, subjective norm, and perceived behavioural control explain donation intention. This is useful as a baseline but may omit moral norms, trust, past behaviour, and digital trust.

3. **Moral norm extension**  
   Internalised obligation explains additional variance beyond perceived social expectations.

4. **Trust-augmented BEBA model**  
   Nonprofit trust and brand trust operate as uncertainty-reduction mechanisms that support donation intention.

5. **Past-behaviour continuity model**  
   Future giving is partly explained by previous donation behaviour, familiarity, learned trust, or habit-like repetition.

6. **Digital infrastructure model**  
   In online donation contexts, platform trust may constrain or enable the effect of nonprofit trust.

7. **Culturally moderated model**  
   Cultural context may alter the relative importance of attitude, norms, control, trust, and moral obligation.

## Operationalisations

Possible operationalisations include:

- Self-reported donation intention.
- Self-reported past donation behaviour.
- Observed or verified donation behaviour where available.
- Attitude toward donating.
- Subjective norm / perceived social expectation.
- Moral norm / personal obligation.
- Perceived behavioural control.
- Trust in the nonprofit organization.
- Trust in the digital donation platform.
- Cultural context as moderator.
- Donor status: first-time, occasional, repeat, habitual.

Empirical coefficients, sample sizes, fit indices, and model comparisons must be taken from verified pipeline outputs and are not specified here.

## Existing Scales

Not sufficiently covered in the reviewed literature.

Relevant scale candidates should be checked against the ConstructLedger, Citavi/BibTeX records, and verified measurement sources before canonical adoption.

## Recommended ConstructLedger Updates

Consider adding or reviewing entries for:

1. **Donation Intention**  
   Status: candidate / existing candidate  
   Note: Should remain distinct from donation behaviour.

2. **Donation Behaviour**  
   Status: candidate  
   Note: Should be modelled as enacted giving, not as equivalent to intention.

3. **Moral Norm**  
   Status: candidate  
   Note: Should be distinguished from subjective norm.

4. **Subjective Norm / Social Norm**  
   Status: candidate or existing construct requiring distinction  
   Note: Represents perceived external social expectations.

5. **Perceived Behavioural Control**  
   Status: candidate  
   Note: Individual-level control-related antecedent of intention and possibly behaviour.

6. **Nonprofit Trust / Nonprofit Brand Trust**  
   Status: candidate  
   Note: Should be modelled as uncertainty-reduction mechanism.

7. **Platform Trust**  
   Status: candidate for digital contexts  
   Note: Should not be collapsed into nonprofit trust.

8. **Past Donation Behaviour**  
   Status: candidate  
   Note: Represents behavioural continuity or prior behavioural trace.

9. **Cultural Context**  
   Status: boundary condition candidate  
   Note: Keep low-confidence until further evidence is reviewed.

## Recommended Glossary Entry

**Intention-Based Model (IBM):**  
A behavioural explanation model that explains donation behaviour primarily through donation intention and its antecedents, such as attitude, perceived norms, perceived behavioural control, moral norms, trust, and past behaviour. In BEBA, intention-based models are treated as useful baseline models but not as complete explanations of enacted donation behaviour.

## Confidence

**Medium.**

The claim set provides coherent support for treating IBM as a baseline individual-level behavioural architecture in BEBA. Confidence is lower for cultural moderation and context-specific pathway stability because the reviewed evidence appears less developed.

## Review Recommendation

Proceed as a **candidate ontology entry** for manual review.

Recommended next action:

- Create a theory integration note rather than updating canonical ontology files directly.
- Suggested filename: `Donation_Intention_BEBA_Integration_Candidate.md`
- Suggested target directory: `02_Theory/Concept_Workspace/`
- Do not update the canonical ontology, ConstructLedger, or glossary until the candidate has been reviewed.

## Integration from REVIEW-000010

**Integrated:** 2026-07-13T18:59:21.160335+00:00

**Accepted claims (7):**
- DI-000002: An individual's intention to donate is positively predicted by attitude toward donating, perceived n
- MN-000001: Donation intention models that include moral norms explain more variance than models limited to subj
- IB-000003: Donation intention positively predicts donation behaviour but does not fully explain actual donation
- NT-000001: Trust in a charitable organization is a distinct positive antecedent of donation intention alongside
- PD-000001: Past donation behaviour improves the explanation of future donation intention and future donation be
- CC-000002: The predictive validity of standard intention-based donation models is moderated by cultural context
- PT-000001: In digital donation contexts, trust in the technological platform positively predicts donation inten

**Accepted evidence (23):**
- EVID-000253: The Integrated Model of Behaviour, Theory of Planned Behaviour, and Theory of Reasoned Action are re
- EVID-000254: Attitude, perceived norms, and perceived behavioural control are consistent and significant predicto
- EVID-000255: Intention is consistently reported as the strongest single predictor of actual donation behaviour.
- EVID-000256: The relationship between donation intention and actual donation behaviour is positive and significan
- EVID-000257: Moral norms can be a stronger predictor of charitable donation intention than social or subjective n
- EVID-000258: Adding moral norms to the standard intention model significantly improves its explanatory power for 
- EVID-000259: Past donation behaviour improves the explanation of future donation intention and future donation be
- EVID-000260: Multidimensional trust in the nonprofit organization improves the predictive power of donation inten
- EVID-000261: Trust in a charitable organization is reported as a distinct antecedent of donation intention alongs
- EVID-000262: A persistent intention-behaviour gap exists because many people who intend to donate do not follow t
- EVID-000263: Standard IBM or TPB predictors may be less powerful in non-Western contexts where macro-level factor
- EVID-000264: The predictive validity of standard intention-based models is moderated by cultural context.
- EVID-000265: In collectivist cultures or developing nations, religious norms, community obligations, or economic 
- EVID-000266: For online giving and crowdfunding, additional factors such as trust in technology, platform credibi
- EVID-000267: In digital donation contexts, trust in the technological platform is necessary in addition to trust 
- EVID-000268: The IBM or TPB framework is well suited for predicting a single discrete act of donation.
- EVID-000269: The IBM or TPB framework is less equipped to explain sustained donor loyalty or repeat giving than s
- EVID-000270: Relationship quality and feedback loops may be more influential for long-term donor retention than a
- EVID-000271: There is no consensus on a single definitive extended IBM or TPB model for charitable giving.
- EVID-000272: There is a lack of research on theoretically grounded interventions that reliably convert positive d
- EVID-000273: There is a deficit of studies applying and testing intention-based donation models in diverse non-We
- EVID-000274: The mechanisms through which digital platforms alter established drivers of donation intention are n
- EVID-000275: Longitudinal research tracking the evolution of attitudes, norms, and perceived behavioural control 

**Accepted sources (10):**
- SRC-000065: White and others (2023)
- SRC-000070: Linden (2011)
- SRC-000071: Smith and McSweeney (2007)
- SRC-000072: Lee and Kim (2023)
- SRC-000073: Musamuxamedov and others (2025)
- SRC-000074: Li and others (2022)
- SRC-000033: Kim and Han (2020)
- SRC-000075: Talie and others (2020)
- SRC-000076: Nguyen and others (2022)
- SRC-000077: Chetioui and others (2022)

