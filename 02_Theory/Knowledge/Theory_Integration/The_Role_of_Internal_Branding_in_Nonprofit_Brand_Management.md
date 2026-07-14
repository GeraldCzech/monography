---
concept: The_Role_of_Internal_Branding_in_Nonprofit_Brand_Management
review: REVIEW-000085
claim_count: 6
claim_ids:
- IB-000022
- SD-000001
- EB-000009
- L-000005
- CL-000001
- CL-000002
status: accepted
review_status: reviewed
reviewed_at: '2026-07-12T09:56:18.823803+00:00'
reviewed_by: human
---

# Input Reviewed

-   **IB-000022**: The effect of NPO brand orientation on performance is fully mediated serially by staff emotional brand attachment and then staff service involvement.
-   **SD-000001**: NPO brand orientation acts as an extrinsic motivator, initiating motivation internalization in staff per Self-Determination Theory (SDT).
-   **EB-000009**: Staff emotional brand attachment is a direct antecedent of staff service involvement.
-   **L-000005**: The effectiveness of internal branding is contingent on leadership style.
-   **CL-000001**: Charismatic leadership strengthens the link between brand orientation and staff emotional brand attachment.
-   **CL-000002**: Charismatic leadership strengthens the link between staff emotional brand attachment and service involvement.

# Core Theoretical Implication

These claims collectively propose a detailed, empirically-grounded mechanism for the **internal dimension of BEBA**. They specify a moderated serial mediation pathway, explaining *how* an organization's strategic brand orientation is translated into performance-relevant staff behaviour. The core insight is that the pathway is not direct, but psychological, flowing from strategic intent to staff emotion, then to staff behaviour, with leadership acting as a critical catalyst. Self-Determination Theory (SDT) is introduced as the underlying psychological engine driving this process of motivation internalization.

# BEBA Layer Affected

The claims bridge the **Organisational Layer** and the **Individual Layer**.

-   **Organisational Layer:** `Brand Orientation Behaviour`, `Charismatic Leadership`, `Organizational Performance`.
-   **Individual Layer:** `Staff Emotional Brand Attachment`, `Staff Service Involvement`, and the psychological process of `Motivation Internalization` (SDT).

The set of claims explicitly models the causal influence from the Organisational Layer to the Individual Layer, and the subsequent impact of the Individual Layer back onto the Organisational Layer (via performance).

# Existing Claims Supported

-   Supports the core BEBA tenet that brand is a behavioural architecture, by detailing a specific internal pathway from strategy to behaviour.
-   Supports the idea that BEBA's mechanisms are not purely cognitive, but heavily involve affective components (`Emotional Brand Attachment`).
-   Supports the principle that BEBA is a system whose effectiveness is contingent on contextual factors, not a deterministic machine.
-   Supports the linkage between micro-level psychological states and macro-level organisational outcomes.

# Existing Claims Challenged

-   These claims challenge any simplified model of BEBA that posits a direct link from `Brand Orientation` to `Organizational Performance` or `Staff Behaviour`. The finding of **full serial mediation** (IB-000022) suggests that the psychological pathway through emotional attachment and service involvement is necessary, not optional.

# New Candidate Claims

1.  **C-BEBA-Internal-01 (Mechanism):** The internal BEBA pathway operates through a sequence of staff motivation internalization, progressing from affective connection (emotional attachment) to behavioural enactment (service involvement).
2.  **C-BEBA-Internal-02 (Theory):** Self-Determination Theory explains the psychological process by which organisational brand orientation is transformed into self-determined staff behaviour.
3.  **C-BEBA-Internal-03 (Moderation):** The efficiency of the internal BEBA pathway (from brand orientation to staff behaviour) is positively moderated by leadership behaviours, specifically charismatic leadership.

# Boundary Conditions

-   **Leadership Style:** The claims explicitly introduce leadership as a key boundary condition. The effectiveness of the brand-to-behaviour link is contingent on the presence of a supportive leadership style (charismatic leadership is the tested example). The absence of such leadership would presumably weaken or break the causal chain.

# Model Competition Implications

This introduces a specific, testable model for the internal BEBA architecture: a **Moderated Serial Mediation Model**. This model should compete against:

-   **A Direct Effects Model:** Brand Orientation -> Performance.
-   **A Simple Mediation Model:** Brand Orientation -> Emotional Attachment -> Performance.
-   **An Alternative Mediator Model:** Testing cognitive mediators (e.g., `Brand Understanding`) instead of or alongside affective ones (`Emotional Attachment`).
-   **An Alternative Theory Model:** Framing the mechanism using Social Identity Theory instead of Self-Determination Theory.

The claim of *full* mediation (IB-000022) is a strong assertion that makes this model highly falsifiable and a prime candidate for competitive testing.

# Ontology Candidate Implications

This integration requires formalizing several concepts and relationships within the BEBA ontology:

-   **New Concept Candidates:**
    -   `Staff Emotional Brand Attachment`: Requires a canonical definition distinguishing it from general consumer brand attachment.
    -   `Staff Service Involvement`: Requires definition and differentiation from related concepts like Brand Citizenship Behaviour or job engagement.
    -   `Charismatic Leadership`: Requires a specific definition within the NPO branding context.
-   **New Relationship Candidates:**
    -   A `seriallyMediates` relationship type to capture the `Brand Orientation -> Attachment -> Involvement -> Performance` chain.
    -   A `strengthens` relationship type (a form of positive moderation) to capture the effect of `Charismatic Leadership` on two specific paths in the model.

# Recommendation

1.  **Formalize Concepts:** Create new candidate files in `02_Theory/Concepts/Candidates/` for `StaffEmotionalBrandAttachment.md`, `StaffServiceInvolvement.md`, and `CharismaticLeadership.md`. These files should capture the definitions implied by the source literature.
2.  **Model the Mechanism:** Create a new model file, `M-BEBA-Internal_SDT_v1_candidate.md`, in `02_Theory/Models/Candidates/`. This file should formally specify the moderated serial mediation model, citing these claims. It should include a visual diagram and list the paths for empirical testing.
3.  **Update Relationship Model:** The `BEBA_RELATIONSHIP_MODEL_v1.md` should be reviewed to see if `seriallyMediates` and `strengthens` (moderation) relationships are adequately defined. If not, an ADR should be considered to update the knowledge engineering guide.
4.  **Integrate into Master Outline:** The `00_MASTER_OUTLINE.md` should be updated to include a specific subsection on the "Internal BEBA: From Brand Orientation to Staff Behaviour," referencing this new candidate model. This provides a clear mechanism for the "living the brand" concept.

## Integration from REVIEW-000085

**Integrated:** 2026-07-13T19:05:04.348170+00:00

**Accepted claims (6):**
- IB-000022: The effect of an NPO's brand orientation behaviour on its organizational performance is fully mediat
- SD-000001: An NPO's brand orientation behaviour functions as an extrinsic motivator that initiates a psychologi
- EB-000009: The development of staff emotional brand attachment is a direct antecedent of staff service involvem
- L-000005: The effectiveness of an NPO's internal branding process is contingent on leadership style.
- CL-000001: Charismatic leadership strengthens the positive relationship between an NPO's brand orientation beha
- CL-000002: Charismatic leadership strengthens the positive relationship between staff's emotional brand attachm

**Accepted evidence (8):**
- EVID-001742: The relationship between an NPO's brand orientation behaviour and its organizational performance is 
- EVID-001743: Charismatic leadership positively moderates the relationship between an NPO's brand orientation beha
- EVID-001744: Charismatic leadership positively moderates the relationship between staff's emotional brand attachm
- EVID-001745: The process of internal branding can be explained by Self-Determination Theory as a mechanism of mot
- EVID-001746: Models proposing a simple, direct link between brand orientation and organizational performance are 
- EVID-001747: Leadership plays a critical role in facilitating internal brand management processes.
- EVID-001748: Future research should focus on developing context-specific performance scales for NPOs rather than 
- EVID-001749: The cultural aspects of brand orientation were not included in the model, representing a potential a

**Accepted sources (9):**
- SRC-000460: Liu, G., Chapleo, C., Ko, W. W., & Ngugi, I. K. (2015)
- SRC-000461: Deci, E. L., & Ryan, R. M. (2004)
- SRC-000428: Ewing, M. & Napoli, J. (2005)
- SRC-000432: Hankinson, P. (2001)
- SRC-000462: Napoli, J. (2006)
- SRC-000463: Hankinson, P. (2002)
- SRC-000464: Punjaisri, K., & Wilson, A. (2011)
- SRC-000465: Morhart, F., Herzog, W., & Tomczak, T. (2009)
- SRC-000466: Wieseke, J., Ahearne, M., Lam, S. K., & van Dick, R. (2009)

