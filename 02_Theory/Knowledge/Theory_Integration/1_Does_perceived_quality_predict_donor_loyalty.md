---
concept: 1_Does_perceived_quality_predict_donor_loyalty
review: REVIEW-000095
claim_count: 8
claim_ids:
- PQ-000010
- PV-000002
- S-000011
- S-000012
- PV-000003
- RQ-000001
- BE-000063
- BC-000042
status: candidate
---

# Input Reviewed

This analysis integrates a set of eight related claims derived from literature review `REVIEW-000095`. These claims collectively outline a standard service-logic model for nonprofit stakeholder behaviour and explore the role of brand-related constructs within it.

The core causal chain proposed is:
`Perceived Quality -> Perceived Value -> Satisfaction -> Behavioural Outcomes (Repeat Support, WOM)`

Key additional claims are:
-   A direct path from `Relationship Quality` to loyalty and WOM.
-   A lack of evidence for `Brand Equity` as a direct antecedent of `Perceived Quality`.
-   Evidence for `Brand Credibility` as a *moderator* of the `Service Quality -> Behavioural Outcomes` link.

# Core Theoretical Implication

The primary implication is that a standard, non-brand-centric service-logic model (`Quality -> Value -> Satisfaction -> Behaviour`) is a robust baseline for explaining stakeholder behaviour in nonprofits. The reviewed literature challenges a simplistic view of Brand Equity as a mere signal of quality. Instead, it positions brand constructs (like Brand Credibility) in a more sophisticated role: as **amplifiers or moderators** of the behavioural consequences of service experiences.

This creates the central theoretical puzzle for BEBA: not to replace this service-logic chain, but to explain how a brand architecture *interacts with, strengthens, and systematizes* it. The brand's role shifts from being a simple input (cause of quality perception) to being a catalyst (enhancer of behavioural conversion).

# BEBA Layer Affected

-   **Individual Layer:** This is the primary layer affected. The claims describe the cognitive, affective, and behavioural sequence of an individual stakeholder (e.g., donor, member, volunteer).
-   **Organisational Layer:** This layer is indirectly but critically affected. The claim `BE-000063` questions the direct impact of organisational-level Brand Equity on individual perceptions of quality, forcing a re-evaluation of how organisational assets translate into individual-level effects. BEBA, as an architecture, must explain this link.

# Existing Claims Supported

-   Any existing BEBA claims that posit a link between psychological states (e.g., satisfaction, perceived value) and behavioural outcomes are strongly supported by claims `S-000011` and `S-000012`.
-   The foundational BEBA principle that behaviour is the outcome of a complex process is supported by the sequential, multi-stage model (`PQ -> PV -> S`).

# Existing Claims Challenged

-   **Claim `BE-000063` directly challenges any simplistic, pre-existing BEBA claim that "Nonprofit Brand Equity is a direct, positive antecedent of Perceived Quality."** This forces BEBA to move beyond a signaling theory explanation for the brand's function.
-   **Claim `RQ-000001` (Relationship Quality -> Loyalty) challenges a brand-centric view of BEBA.** It suggests that loyalty can be generated through interpersonal relationships, potentially independent of the organizational brand. BEBA must either incorporate this relational path or define its scope as separate from it.

# New Candidate Claims

Based on this integration, the following candidate claims should be added to the BEBA theory:

1.  **C-BEBA-011:** The primary mechanism through which nonprofit brands enable supportive behaviour is by amplifying the conversion of positive service experiences (quality, value, satisfaction) into behavioural intentions and actions.
2.  **C-BEBA-012:** Brand Credibility acts as a positive moderator on the relationship between stakeholder satisfaction and subsequent supportive behaviours (e.g., repeat support, positive WOM).
3.  **C-BEBA-013:** The effectiveness of the core `Quality -> Value -> Satisfaction` chain as a driver of behaviour is contingent on the stakeholder type, with the strongest effect observed in stakeholders who are also direct service consumers.

# Boundary Conditions

-   **Stakeholder Role:** The reviewed literature (note on `PV-000003`) suggests the Q->V->S model is most applicable to stakeholders who are also service consumers (e.g., members of a sports club). This may be a crucial boundary condition. The model might function differently for pure donors, volunteers, or institutional funders.
-   **Sector/Context:** The contradictory evidence from the banking sector (note on `S-000011`, `S-000012`) suggests that the link between satisfaction and behaviour is not universal. BEBA must consider context-specific factors that may weaken or strengthen this relationship.

# Model Competition Implications

This review is highly valuable as it establishes a clear set of competing models for BEBA to test:

1.  **The Signaling Model:** `Brand Equity -> Perceived Quality -> ... -> Behaviour`. Claim `BE-000063` suggests this model lacks empirical support in this context.
2.  **The Service-Logic Model (Baseline):** `Perceived Quality -> Perceived Value -> Satisfaction -> Behaviour`. This is the non-brand baseline model.
3.  **The Relational Bypass Model:** A parallel process where `Relationship Quality -> Behaviour` operates independently of the main service-logic chain.
4.  **The BEBA Amplification Model (Proposed):** The baseline Service-Logic Model holds, but brand constructs (e.g., Brand Credibility, Trust) *moderate* the links within the chain, particularly the `Satisfaction -> Behaviour` link.

BEBA's theoretical contribution lies in proposing and testing the Amplification Model (4) against the simpler alternatives (1, 2, 3).

# Ontology Candidate Implications

1.  **New Concept:** No fundamentally new concepts are introduced, as they are common in marketing and nonprofit literature.
2.  **New Relationships:** The review necessitates formalizing a **moderates** relationship type in the BEBA ontology.
    -   *Candidate Relationship:* `BrandCredibility --moderates--> (Satisfaction -> SupportiveBehaviour)`
3.  **New Model Object:** A new candidate model file should be created to formally specify the "Service-Logic Baseline Model" and the proposed "BEBA Amplification Model". This would visually and textually represent the model competition.

# Recommendation

1.  **Adopt the Baseline:** Formally adopt the `Quality -> Value -> Satisfaction -> Behaviour` chain as the **Baseline Behavioural Model** within the BEBA framework. This is the phenomenon BEBA must explain the brand's role in.
2.  **Prioritize the "Brand as Amplifier" Hypothesis:** Shift BEBA's core theoretical focus from the brand as a *creator* of quality perceptions to the brand as an *amplifier* of behavioural outcomes. This should become a central thesis.
3.  **Address the "Relational Bypass":** The theory must explicitly address the role of interpersonal Relationship Quality. Is it part of the BEBA, a competitor to it, or something the architecture seeks to systematize? This needs to be resolved.
4.  **Create New Object:** Create a new candidate model file: `02_Theory/Models/Candidates/M-CAND-ServiceLogicAmplification-v1.md`. This file should detail the competing models identified above and position the "Amplification Model" as the primary BEBA-driven hypothesis.
5.  **Update Ontology Guide:** Propose an update to `BEBA_RELATIONSHIP_MODEL_v1.md` to formally include the `moderates` relationship type, providing its definition and graphical representation.

## Integration from REVIEW-000095

**Integrated:** 2026-07-13T19:05:51.336879+00:00

**Accepted claims (8):**
- PQ-000010: In nonprofit settings, higher stakeholder-perceived quality is a positive antecedent of perceived va
- PV-000002: Higher perceived value from a nonprofit is a positive antecedent of stakeholder satisfaction.
- S-000011: Stakeholder satisfaction with a nonprofit is a positive predictor of repeat support behaviours.
- S-000012: Stakeholder satisfaction with a nonprofit is a positive predictor of positive word-of-mouth.
- PV-000003: Perceived value mediates the relationship between perceived quality and stakeholder satisfaction in 
- RQ-000001: The perceived quality of the relationship between a stakeholder and a nonprofit directly predicts lo
- BE-000063: There is no consistent evidence in the reviewed literature for a direct, causal effect of nonprofit 
- BC-000042: Brand credibility moderates the relationship between service quality and stakeholder behavioural out

**Accepted evidence (12):**
- EVID-001836: In German nonprofit sport clubs, service quality had a major effect on perceived value, satisfaction
- EVID-001837: Perceived value mediates the relationship between service quality and satisfaction in nonprofit spor
- EVID-001838: Satisfaction mediates the relationship between service quality and loyalty in nonprofit sport clubs.
- EVID-001839: Donor-perceived relationship quality is a central antecedent to donor loyalty and positive word-of-m
- EVID-001840: Satisfaction is a positive predictor of loyalty intentions and behaviours, such as repeat support an
- EVID-001841: In a banking study, satisfaction did not affect word-of-mouth or repurchase intention, despite servi
- EVID-001842: Existing literature does not provide consistent evidence for a direct, causal effect of nonprofit br
- EVID-001843: Charity brand credibility moderates the links between perceived quality, brand equity, and loyalty.
- EVID-001844: Some nonprofit brand equity models define equity through awareness, trust, and commitment, rather th
- EVID-001845: Donors weight different dimensions of service quality differently, with reliability and tangibles ra
- EVID-001846: The quality of staff-donor relationships can have a greater impact on donation intention than celebr
- EVID-001847: Perceived beneficiary benefits and communication of impact build trust, which indirectly fosters com

**Accepted sources (17):**
- SRC-000542: Min, D. (2022)
- SRC-000543: Shabbir, H., Palihawadana, D., & Thwaites, D. (2007)
- SRC-000544: Jones, J. L., & Shandiz, M. (2015)
- SRC-000545: Kim, M., Yoon, Y., & Zhang, J. J. (2023)
- SRC-000546: Sargeant, A., Ford, J. B., & West, D. (2006)
- SRC-000547: Marcos, A., & Coelho, A. (2021)
- SRC-000548: Oktaviani, N., & Nisa, P. C. (2024)
- SRC-000549: Kashif, M., Fernando, P., Samad, S., & Thurasamy, R. (2018)
- SRC-000339: Boenigk, S., & Becker, A. (2016)
- SRC-000550: Graça, S. S. (2022)
- SRC-000551: Hommerová, D., Alaimo, S., & Sojková, O. M. (2025)
- SRC-000552: Crawford, E. C., & Jackson, J. (2025)
- SRC-000553: Lee, Z., Spry, A., Ekinci, Y., & Vredenburg, J. (2023)
- SRC-000554: Anwar, S., & Gulzar, A. (2011)
- SRC-000555: Jibran, R., Rasul, M., Hussain, M., Shahid, R., & Yasin, M. (2025)
- SRC-000556: Hume, M., & Mort, G. S. (2010)
- SRC-000557: Kusuma, I. E. T., Yasmari, N. N. W., Agung, A., & Landra, N. (2021)

