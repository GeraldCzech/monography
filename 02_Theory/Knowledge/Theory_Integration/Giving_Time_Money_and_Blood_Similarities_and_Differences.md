---
concept: Giving_Time_Money_and_Blood_Similarities_and_Differences
review: REVIEW-000068
claim_count: 11
claim_ids:
- RI-000001
- PB-000018
- PB-000019
- RI-000002
- RI-000003
- RI-000004
- RI-000005
- SE-000004
- PM-000001
- PN-000001
- BT-000024
status: accepted
review_status: reviewed
reviewed_at: '2026-07-12T12:35:59.982767+00:00'
reviewed_by: human
---

# Input Reviewed

The set of eleven claims from `REVIEW-000068` introduces a model of institutionalized pro-social behavior centered on the concepts of **Role-Identity** and **Past Behaviour**. The core argument is that pro-social role-identity (e.g., "I am a volunteer") is formed by antecedents like past behavior, social expectations, parental modeling, and personal norms. This role-identity, in turn, predicts future behavioral intention. Critically, past behavior is identified as both a key driver of identity and the single strongest direct predictor of future intention. The review also highlights that the strength of these relationships differs significantly across behavioral types (donating time, money, or blood).

# Core Theoretical Implication

The primary implication is that sustained pro-social behavior is driven by a **self-reinforcing feedback loop where behavior builds identity, and identity in turn motivates future behavior**. This positions behavioral activation and habit formation not as outcomes of brand equity, but as foundational inputs to the very identity structures that ensure long-term engagement. The brand's role shifts from merely persuading to actively facilitating initial behaviors and providing the symbolic meaning to integrate those behaviors into a stable role-identity.

# BEBA Layer Affected

*   **Individual Layer:** All claims operate at the individual psychological level, dealing with identity, norms, intentions, and behavior.

# Existing Claims Supported

*   **Behaviour-first principle:** The finding that past behavior is the strongest predictor of intention (PB-000019) strongly validates BEBA's core principle of "Behaviour before brands." It confirms that a successful architecture must focus on enabling and reinforcing action.
*   **Identity mechanisms:** Claims RI-000001 through RI-000005 provide a specific, evidence-based mechanism (`Role-Identity`) for how a brand can connect to an individual's self-concept to drive commitment. This supports any existing BEBA claims related to self-congruence or brand identification.
*   **Social influence:** The role of social expectations (RI-000003, SE-000004) supports the idea that a BEBA must operate within and shape the social context of the individual.

# Existing Claims Challenged

*   **Primacy of Brand Equity:** These claims challenge any BEBA model where brand equity (or its attitudinal components) is the primary, direct antecedent of behavioral intention. They posit `Past Behaviour` as a more powerful, direct predictor (PB-000019), suggesting brand equity might play a different role—perhaps as an initiator of novel behavior or a moderator of the behavior-to-identity link.
*   **Homogeneity of Pro-Social Behaviour:** The claims strongly challenge a "one-size-fits-all" BEBA. The findings that different antecedents matter more for different behaviors (SE-000004, PM-000001, PN-000001, BT-000024) imply that a generic BEBA is likely misspecified.

# New Candidate Claims

1.  **BEBA-C-01 (Dual Pathways):** Sustained pro-social behavior is driven by two interconnected pathways: a direct, habit-based pathway (`Past Behaviour -> Intention`) and a reflective, identity-based pathway (`Past Behaviour -> Role-Identity -> Intention`).
2.  **BEBA-C-02 (Brand as Identity Catalyst):** The primary function of a nonprofit brand within a BEBA is to (a) lower the barriers to initial behavior and (b) provide the symbolic framework for individuals to interpret their behavior as diagnostic of a valued pro-social role-identity.
3.  **BEBA-C-03 (Behavioural Contingency):** The optimal configuration of a BEBA is contingent on the psychological profile of the target behavior. Architectures for behaviors driven by moral obligation (e.g., blood donation) must differ from those driven by social expectations (e.g., volunteering).

# Boundary Conditions

*   The findings apply specifically to **institutionalized pro-social behaviors**. The model's relevance to spontaneous, informal, or one-off helping behaviors is not established.
*   The dominance of past behavior as a predictor is likely strongest for **repeated behaviors**. For entirely novel actions where no "past behavior" exists, the relative importance of identity and other cognitive antecedents would be higher.

# Model Competition Implications

*   This introduces a **Role-Identity/Habit Model** as a strong competitor to simpler attitudinal models like the Theory of Planned Behavior (TPB). It suggests that any BEBA model based on TPB must be extended to include `Past Behaviour` and `Role-Identity` as central, non-background variables.
*   It forces a theoretical choice between a single, complex BEBA model with many interaction terms for behavioral type, versus a portfolio of more parsimonious, **behavior-specific BEBA models** (e.g., BEBA-Volunteer, BEBA-BloodDonor). The evidence supports the latter approach.

# Ontology Candidate Implications

*   **New Concept:** `Pro-Social Role-Identity` must be added to the ontology as a key concept. It should be defined as "a self-conception tied to the performance of a specific, institutionalized pro-social role (e.g., 'blood donor', 'volunteer', 'supporter')." It is more specific than `Self-Concept`.
*   **New Relationships:** The causal loop requires formal relationship definitions, such as `Past Behaviour` -> `strengthens` -> `Role-Identity` and `Role-Identity` -> `predicts` -> `Behavioural Intention`.
*   **Concept Qualification:** The concept of `Behaviour` in BEBA must be refined. The attribute `Behavioural Type` (with values like Time, Money, Blood, etc.) is not just descriptive but a critical qualifier that alters causal relationships throughout the model.

# Recommendation

1.  **Create Candidate Concept File:** Draft a new file `02_Theory/Concepts/Candidates/pro_social_role_identity.md` to formalize the definition and its relationships based on these claims.
2.  **Update Theoretical Map:** Revise `01_THEORETICAL_MAP.md` to explicitly include the `Past Behaviour <-> Role-Identity -> Intention` loop as a core psychological mechanism within the Individual Layer.
3.  **Propose ADR for Model Specificity:** Draft an ADR proposing that the BEBA framework mandates behavior-specific models. The default assumption should be that relationships differ by behavioral type (Time, Money, Blood, Advocacy, etc.) unless there is strong evidence for their equivalence.
4.  **Review Brand Equity's Role:** Initiate a review of existing claims about Brand Equity's direct influence on behavior. Re-evaluate Brand Equity's position as a potential moderator or an antecedent to *initial* behavior rather than a direct driver of *sustained* behavior.

## Integration from REVIEW-000068

**Integrated:** 2026-07-13T19:03:44.620384+00:00

**Accepted claims (11):**
- RI-000001: The intention to perform an institutionalized pro-social behavior is positively predicted by the str
- PB-000018: The intention to perform an institutionalized pro-social behavior is positively predicted by past be
- PB-000019: Past behavior is the strongest predictor of future intentions for institutionalized pro-social behav
- RI-000002: The strength of a pro-social role-identity is positively predicted by an individual's past behavior 
- RI-000003: The strength of a pro-social role-identity is positively predicted by perceived social expectations.
- RI-000004: The strength of a pro-social role-identity is positively predicted by parental modeling of the behav
- RI-000005: The strength of a pro-social role-identity is positively predicted by personal norms of moral obliga
- SE-000004: Perceived social expectations have a stronger effect on past volunteering of time compared to past d
- PM-000001: Parental modeling has a stronger effect on past blood donation compared to past volunteering of time
- PN-000001: Personal norms of moral obligation are a stronger predictor of a blood donor role-identity compared 
- BT-000024: The antecedent model for donating time is more similar to the model for donating money than either i

**Accepted evidence (11):**
- EVID-001579: An identity theory model, originally developed to explain blood donation, generalizes well to explai
- EVID-001580: Behavioral intentions for giving blood, time, and money are significantly predicted by both past beh
- EVID-001581: A pro-social role-identity is predicted by past behavior, perceived expectations of others, parental
- EVID-001582: Volunteering time is more strongly influenced by others' expectations compared to donating blood or 
- EVID-001583: Blood donation is more strongly affected by parental modeling compared to donating time or money.
- EVID-001584: The development of a blood donor role-identity is more dependent on feelings of moral obligation (pe
- EVID-001585: The patterns of antecedents for donating time and money are more similar to each other than either i
- EVID-001586: Behavioral intentions are the most direct and reliable predictor of actual behavior.
- EVID-001587: Parental modeling influences the development of prosocial behavior in children and adults.
- EVID-001588: Perceived expectations from significant others (social norms) impact behavior.
- EVID-001589: Internalized feelings of moral obligation (personal norms) serve as a motivator for helping behavior

**Accepted sources (10):**
- SRC-000316: Lee, L., Piliavin, J. A., and Call, V. R. A. (1999)
- SRC-000317: Stryker, S. (1980)
- SRC-000318: Mead, G. H. (1934)
- SRC-000319: Fishbein, M., & Ajzen, I. (1975)
- SRC-000320: Randall, D. M., & Wolff, J. A. (1994)
- SRC-000321: Sheppard, B. H., Hartwick, J., & Warshaw, P. R. (1988)
- SRC-000322: Grusec, J. E. (1982)
- SRC-000323: Rosenhan, D. L. (1970)
- SRC-000324: Oliner, S. P., & Oliner, P. M. (1988)
- SRC-000325: Schwartz, S. H., & Howard, J. A. (1981)

