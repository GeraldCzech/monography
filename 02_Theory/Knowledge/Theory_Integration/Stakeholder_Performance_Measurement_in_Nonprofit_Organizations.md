---
concept: Stakeholder_Performance_Measurement_in_Nonprofit_Organizations
review: REVIEW-000079
claim_count: 7
claim_ids:
- SQ-000001
- DL-000003
- OI-000002
- DS-000007
- NP-000007
- NP-000008
- SQ-000002
status: accepted
review_status: reviewed
reviewed_at: '2026-07-11T20:37:16.981599+00:00'
reviewed_by: human
---

# Input Reviewed

The set of claims under review (SQ-000001, DL-000003, OI-000002, DS-000007, NP-000007, NP-000008, SQ-000002) are derived from `REVIEW-000079`. Collectively, they describe and validate a causal model for donor loyalty in a nonprofit service context (German blood donation). The model is an adaptation of the American Customer Satisfaction Index (ACSI), augmented with the construct of Organisational Identification.

The core causal structure proposed is:
*Perceived Service Quality* -> *Donor Satisfaction*
*Donor Satisfaction* -> *Donor Loyalty* (Direct Path)
*Donor Satisfaction* -> *Organisational Identification* -> *Donor Loyalty* (Mediated, Relational Path)

# Core Theoretical Implication

The primary implication is that stakeholder loyalty in nonprofits is driven by a dual-pathway mechanism. It is not sufficient to model only a direct, transactional path from satisfaction to loyalty. A parallel, relational path, where positive service experiences are converted into deeper organisational identification which in turn drives loyalty, is of comparable importance. This firmly positions tangible stakeholder experience (service quality) as the foundation for building both transactional satisfaction and relational commitment, which are the core psychological assets of a behaviour-enabling brand.

# BEBA Layer Affected

1.  **Individual Layer:** This is the primary layer affected. The claims specify a micro-level causal model of individual stakeholder psychology, detailing how perceptions (service quality) are converted into attitudes (satisfaction, identification) and then into behavioural intentions (loyalty).
2.  **Organisational Layer:** This layer is also significantly affected. The claims translate the individual-level model into actionable organisational strategy (improving service quality) and a concrete performance measurement framework (a "donor satisfaction barometer" incorporating both satisfaction and identification). This directly addresses how an NPO can architect its behaviour-enabling systems.

# Existing Claims Supported

These findings provide strong support for several core BEBA principles:
*   **Behaviour before brands:** The model's ultimate dependent variable is a behaviour (loyalty), reinforcing BEBA's focus on behavioural outcomes.
*   **Tangible experiences as primary drivers:** The model is rooted in `Perceived Service Quality`, supporting the BEBA principle that brand equity is built primarily through lived experiences with the organisation, not just through communication (as stated in `SQ-000001` and `SQ-000002`).
*   **Multiple pathways to behaviour:** The validation of both direct (satisfaction-based) and indirect (identification-based) paths supports the architectural view of BEBA, where the brand provides multiple, sometimes redundant, routes to desired behaviours (`DL-000003`).
*   **Importance of relational constructs:** The finding that identification's effect on loyalty is comparable to that of satisfaction reinforces the necessity of including relational constructs as first-class citizens in the BEBA framework (`OI-000002`).

# Existing Claims Challenged

The reviewed claims do not directly contradict the stated BEBA principles. However, they would challenge any simplified or competing model that:
*   Posits a single, linear path from brand perception to behaviour.
*   Subsumes relational constructs like identification under a broader, undifferentiated "brand equity" or "satisfaction" construct. This evidence argues for their distinct roles as mediators.
*   Overemphasizes the role of marketing communications at the expense of service delivery and operational excellence in building a strong nonprofit brand.

# New Candidate Claims

Based on this integration, the following higher-order claims should be considered for inclusion in the BEBA theory:

1.  **C-BEBA-NEW-01:** A nonprofit's brand-enabled behaviour architecture must account for both transactional (e.g., satisfaction-driven) and relational (e.g., identification-driven) pathways to stakeholder loyalty.
2.  **C-BEBA-NEW-02:** In service-oriented nonprofits, stakeholder satisfaction acts as a critical conversion point, directly influencing loyalty while simultaneously building deeper relational assets like organisational identification.
3.  **C-BEBA-NEW-03:** The effectiveness of a nonprofit's brand architecture can be measured by a system that tracks both satisfaction and identification as leading indicators of behavioural loyalty.

# Boundary Conditions

The integration highlights several important boundary conditions:
*   **Context:** The findings are validated in a high-contact nonprofit service context (blood donation). Their applicability to other contexts, such as advocacy, fundraising-only, or international aid organisations, is not established.
*   **Stakeholder Group:** The model applies specifically to donors who are also service users. It may function differently for non-user donors, volunteers, or other stakeholder groups.
*   **Model Parsimony:** The model explained only 15% of the variance in identification, indicating that satisfaction is a significant but not exhaustive antecedent. Other factors (e.g., value congruence, perceived impact) are likely also at play.

# Model Competition Implications

This review solidifies a specific model, the "Augmented ACSI for Nonprofits," as a strong candidate and benchmark within the BEBA framework. It implies that any competing model for explaining loyalty must demonstrate superior explanatory power to this dual-pathway model. It sets up a direct competition between:
*   A satisfaction-centric model.
*   An identification-centric model.
*   The integrated dual-pathway model (which this evidence supports).
*   More complex models that might include other mediators like trust or perceived value.

# Ontology Candidate Implications

*   **Concepts:** The core concepts (`Service Quality`, `Satisfaction`, `Organisational Identification`, `Loyalty`) are reinforced as essential components of the BEBA ontology.
*   **Relationships:** The following relationships should be formally captured as high-confidence candidates in the BEBA Relationship Model:
    *   `Perceived Service Quality` -> `hasPositiveCausalEffectOn` -> `Stakeholder Satisfaction`
    *   `Stakeholder Satisfaction` -> `hasPositiveCausalEffectOn` -> `Stakeholder Loyalty`
    *   `Stakeholder Satisfaction` -> `hasPositiveCausalEffectOn` -> `Organisational Identification`
    *   `Organisational Identification` -> `hasPositiveCausalEffectOn` -> `Stakeholder Loyalty`
*   **Models:** A new candidate file for a `Model` object should be created: `M-ACSI-NPO-v1.md`, describing the "Augmented ACSI model for Nonprofits".

# Recommendation

1.  **Adopt the Dual-Pathway Mechanism:** Formally integrate the `satisfaction -> loyalty` (transactional) and `satisfaction -> identification -> loyalty` (relational) mechanism as a core, evidence-supported causal pattern within the BEBA Individual Layer.
2.  **Create New Model Candidate:** Create a new file, `02_Theory/Models/Candidates/M_ACSI_NPO_v1.md`, to document the "Augmented ACSI model for Nonprofits" based on these claims. This file should detail the constructs, paths, and supporting evidence from `REVIEW-000079`.
3.  **Update Relationship Model:** Add the specific causal relationships identified above to the BEBA Relationship Model candidate file, citing these claims as evidence.
4.  **Acknowledge Boundaries:** Explicitly document the boundary conditions (service NPO context, donor-user stakeholder) associated with this mechanism in the relevant theory files to guide future research and generalization.
5.  **Refine Performance Measurement Principles:** Use claim `NP-000007` to inform the section on the practical application of BEBA, emphasizing that any BEBA-derived measurement framework must capture both transactional and relational indicators.

## Integration from REVIEW-000079

**Integrated:** 2026-07-13T19:04:35.922498+00:00

**Accepted claims (7):**
- SQ-000001: Perceived service quality is a strong, positive antecedent of stakeholder satisfaction in nonprofit 
- DL-000003: Donor loyalty in nonprofits is positively influenced by both a direct effect from donor satisfaction
- OI-000002: The positive effect of organisational identification on donor loyalty is comparable in magnitude to 
- DS-000007: Donor satisfaction has a positive causal effect on organisational identification in nonprofit servic
- NP-000007: A performance measurement system for nonprofit donor behaviour should incorporate measures of both t
- NP-000008: An augmented American Customer Satisfaction Index (ACSI) model, incorporating organisational identif
- SQ-000002: Improving the perceived quality of service delivery is an effective strategy for a nonprofit to incr

**Accepted evidence (7):**
- EVID-001688: In the nonprofit blood donation context, perceived service quality is a very strong positive driver 
- EVID-001689: Donor satisfaction has a direct, positive influence on donor loyalty.
- EVID-001690: Donor satisfaction is a positive antecedent of organizational identification.
- EVID-001691: Organizational identification exerts a strong, direct, and positive effect on donor loyalty.
- EVID-001692: A dual-path model, where loyalty is driven by both satisfaction and organizational identification, p
- EVID-001693: A stakeholder satisfaction barometer, adapted from the for-profit ACSI model and augmented with orga
- EVID-001694: Financial metrics are insufficient as primary indicators of NPO performance, necessitating a focus o

**Accepted sources (4):**
- SRC-000419: Leipnitz, S. (2014)
- SRC-000423: Parasuraman, A., Zeithaml, V. A., & Berry, L. L. (1988)
- SRC-000425: Arnett, D. B., German, S. D., & Hunt, S. D. (2003)
- SRC-000426: Mael, F., & Ashforth, B. E. (1992)

