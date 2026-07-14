---
concept: 1_Does_donor_identity_salience_predict_charitab
review: REVIEW-000093
claim_count: 9
claim_ids:
- DI-000009
- DI-000010
- DI-000011
- DI-000012
- OI-000005
- OI-000006
- OI-000007
- SI-000009
- PI-000004
status: accepted
review_status: reviewed
reviewed_at: '2026-07-12T17:30:46.272133+00:00'
reviewed_by: human
---

# Input Reviewed

The integration protocol is being applied to a set of nine candidate claims derived from `REVIEW-000093`. These claims concern the role of various identity constructs in nonprofit contexts.

-   **Donor Identity Salience:** Claims DI-000009, DI-000010, DI-000011, DI-000012.
-   **Organizational Identification:** Claims OI-000005, OI-000006, OI-000007.
-   **Social Identification:** Claim SI-000009.
-   **Peer Identification:** Claim PI-000004.

The claims collectively establish identity as a multi-faceted construct that serves as a key antecedent to prosocial intentions and behaviors, a mediator of past experiences, and a target for situational activation. They also introduce important qualifications and competing mechanisms.

# Core Theoretical Implication

The core implication is that **identity is not a monolithic construct within the BEBA framework**. To explain how brands enable behavior, BEBA must differentiate between the *target* of identification (organization, peers, social group) and the *nature* of the identity (general prosocial vs. specific role). These different facets of identity can have independent, and in some cases, opposing effects on behavior. This moves the theory beyond a simple "Identification -> Support" pathway and requires a more nuanced, multi-path model that aligns with the BEBA principle of "competing explanations."

# BEBA Layer Affected

All reviewed claims primarily affect the **Individual Layer** of the BEBA architecture. They describe psychological states and processes (identification, salience, intention) that occur within the individual stakeholder. However, claim DI-000011 ("Externally priming...") implies an interaction with the **Situational Layer**, where brand touchpoints can activate these individual-level constructs.

# Existing Claims Supported

These claims provide strong support for the general theoretical thrust of BEBA, particularly that brand-related psychological constructs are critical precursors to behavior.

-   **Identity as a key BEBA mechanism:** Claims DI-000009, DI-000012, OI-000005, and OI-000007 strongly support the idea that identity is a core component of the "architecture" that translates brand relationships into behavioral intent. It acts as a structure that stores relational capital and directs future action.
-   **Brand as a behavioral enabler:** Claim DI-000011 (priming identity) directly supports the "Brand-Enabled" aspect of BEBA. It provides a specific mechanism for how a brand artifact (e.g., a logo, a message) can activate a latent identity at a decision point, thereby enabling behavior.
-   **BEBA's scope beyond financial giving:** Claim OI-000006 (OI's effect on volunteering and WOM) supports the BEBA premise that brand equity influences a wide range of valuable stakeholder behaviors, not just donations.

# Existing Claims Challenged

-   **Challenge to a unified "Community Identification" effect:** Claim PI-000004 directly challenges any simplistic claim that "identification with the brand community is always positive." It suggests that if stakeholders perceive the NPO as a vehicle for social consumption, identifying with peers may substitute for, or detract from, organizational support.
-   **Challenge to the intention-behavior link:** Claim SI-000009 reinforces that the link between identity-driven *intention* and actual *behavior* is not perfect. This challenges any BEBA model that treats intention as a perfect proxy for behavior and supports the need to explicitly model the intention-behavior gap.

# New Candidate Claims

Based on this synthesis, the following higher-level claims should be considered for integration into the BEBA theory:

1.  **C-BEBA-ID-01:** The effect of brand-related identification on stakeholder support is contingent on the primary target of that identification (e.g., organization, peers, beneficiaries).
2.  **C-BEBA-ID-02:** The predictive power of role identity (e.g., "donor") on a specific behavior is a function of both its chronic accessibility and its situational salience.
3.  **C-BEBA-ID-03:** A key function of a nonprofit brand is to serve as a situational cue that increases the salience of specific, behavior-relevant role identities.
4.  **C-BEBA-ID-04:** Organizational Identification acts as a key mediating variable translating positive brand relationship history into future behavioral intentions across multiple support domains (financial, time, advocacy).

# Boundary Conditions

-   **Specificity Principle:** The predictive validity of identity constructs is bounded by their level of specificity. General prosocial identities are weaker predictors than specific role identities (DI-000010).
-   **NPO Mission Type:** The negative effect of peer identification on donations may be bounded to NPOs with a strong member-service or "social consumption" component (PI-000004). This suggests NPO mission type is a critical moderator.
-   **Outcome Measure Type:** The strength of the association between social identity and giving is bounded by the type of measurement, being significantly stronger for self-reported intentions than for objective behavior (SI-000009).

# Model Competition Implications

This review strongly reinforces the "competing explanations" principle of BEBA.

1.  **Organizational vs. Peer Identification Paths:** BEBA must feature competing models.
    -   *Model A (Mission-Focused Path):* Brand Cues -> Organizational Identification -> Prosocial Behavior (+)
    -   *Model B (Social-Consumption Path):* Brand Cues -> Peer Identification -> Prosocial Behavior (-)
    The choice between these models, or their relative weighting, is likely moderated by the NPO's value proposition and the stakeholder's motivation for affiliation.

2.  **Intention vs. Behavior Models:** BEBA should maintain a distinction between models that predict *intention* and those that predict *behavior*. The latter must include additional constructs that bridge the intention-behavior gap, such as situational cues (priming) and implementation intentions, which are directly related to the "Architecture" concept.

# Ontology Candidate Implications

The reviewed claims make it clear that a single `Concept:Identification` is insufficient. An ontology refinement is necessary.

A new ontology candidate should be created to structure identity-related concepts. A possible hierarchy:

-   `beba:Identification` (Abstract super-concept)
    -   `beba:SocialIdentification` (Identification with a social group)
        -   `beba:PeerIdentification` (Identification with fellow supporters)
        -   `beba:BeneficiaryIdentification` (Identification with service recipients)
    -   `beba:OrganizationalIdentification` (Identification with the NPO itself)
    -   `beba:RoleIdentity` (Identification with a specific behavioral role)
        -   `beba:DonorIdentity`
        -   `beba:VolunteerIdentity`

Furthermore, the concept of `beba:DonorIdentitySalience` needs to be formally defined as a *state* (the momentary activation of the identity), distinct from `beba:DonorIdentity` which is a *trait* or cognitive structure.

# Recommendation

1.  **Create an Ontology Candidate File:** Generate a new file, `02_Theory/Ontology_Candidates/OC-Identity_v1.md`, to formally propose the hierarchical structure of identity constructs outlined above. This will be critical for conceptual clarity and consistent operationalization.
2.  **Update Theoretical Map:** Add the "Organizational vs. Peer Identification" competing mechanism to `01_THEORETICAL_MAP.md` as a key theoretical tension that BEBA must address.
3.  **Create Concept Workspace:** Initiate a new workspace file, `02_Theory/Concept_Workspaces/CWS_Identity_Mechanisms.md`, to synthesize these claims, map their relationships, and develop the new candidate claims (C-BEBA-ID-01 to 04).
4.  **Update ConstructLedger:** Add `OrganizationalIdentification`, `PeerIdentification`, and `DonorIdentitySalience` as distinct entries in the `ConstructLedger.md` to ensure they are tracked separately for measurement and modeling purposes.

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

