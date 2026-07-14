---
concept: 1_What_factors_predict_donation_intention_in_ch
review: REVIEW-000101
claim_count: 6
claim_ids:
- DI-000013
- TR-000029
- R-000006
- BI-000051
- WG-000008
- DT-000002
status: accepted
review_status: reviewed
reviewed_at: '2026-07-12T06:08:01.987569+00:00'
reviewed_by: human
---

# Input Reviewed

This theory integration protocol reviews the following set of six candidate claims derived from `REVIEW-000101`:
- `DI-000013`: The Theory of Planned Behavior (TPB) as a foundational cognitive model for donation intention.
- `TR-000029`: The role of Trust in reducing uncertainty.
- `R-000006`: The direct and indirect (via Trust) effects of Reputation.
- `BI-000051`: The direct effect of Brand Identification, independent of TPB.
- `WG-000008`: The effectiveness of donor-centric (Warm Glow) appeals.
- `DT-000002`: The distinction between antecedents for donating time versus money.

# Core Theoretical Implication

The combined claims strongly suggest that BEBA should not be conceptualized as a single, monolithic pathway from brand equity to behaviour. Instead, these claims mandate a **dual-pathway architecture**. The brand enables behaviour through at least two distinct routes:

1.  A **Deliberative-Cognitive Pathway**: This is the rational, belief-based route described by the Theory of Planned Behavior, where brand assets like Reputation and Trust function to improve attitudes, strengthen norms, and increase perceived behavioural control.
2.  An **Affective-Identity Pathway**: This is a more direct, heuristic route where concepts like Brand Identification and the potential for "warm glow" drive behaviour by fulfilling self-concept needs, bypassing or operating in parallel with extensive cognitive deliberation.

The brand, therefore, does not just provide information for a decision; it provides the cognitive, relational, and identity resources for multiple types of decision-making processes.

# BEBA Layer Affected

-   **Individual Layer**: This layer is most significantly affected. The claims specify the core psychological mechanisms (TPB, Trust, Identification, Warm Glow) that BEBA must incorporate to explain individual behaviour.
-   **Organisational Layer**: This layer is affected through the concepts of Reputation (an organisational asset) and brand communications (the vehicle for "warm glow" appeals), which act as antecedents and activators of the individual-level mechanisms.
-   **Relational Layer**: This layer, which mediates between the Organisational and Individual, is reinforced by the concepts of Trust and Brand Identification, which are inherently relational.

# Existing Claims Supported

-   The core premise of BEBA—that brands are architectures for enabling behaviour—is strongly supported.
-   The claim that brands function to reduce uncertainty and overcome the credence good problem in the nonprofit sector is directly validated by `TR-000029` (Trust).
-   The notion that brand equity components like Reputation are key drivers of stakeholder support is supported by `R-000006`.

# Existing Claims Challenged

-   These claims challenge any simplistic or singular model of BEBA that posits a direct, unmediated path from "Brand Equity" to "Behaviour."
-   They challenge the assumption that the BEBA model is uniform across all supportive behaviours. `DT-000002` explicitly refutes this by distinguishing between the architectures for donating time versus money.
-   `BI-000051` challenges the supremacy of purely cognitive models by demonstrating an independent, identity-based pathway to intention. BEBA cannot be solely based on TPB or other deliberative frameworks.

# New Candidate Claims

Based on the synthesis of the input claims, the following new higher-order claims for the BEBA theory are proposed:

1.  **C-BEBA-01 (Dual Pathway)**: The BEBA framework enables pro-social behaviour through at least two distinct psychological pathways: a deliberative-cognitive path (mediated by attitudes, norms, and perceived control) and an affective-identity path (mediated by brand identification).
2.  **C-BEBA-02 (Contingent Architecture)**: The specific structure and relative influence of BEBA's pathways are contingent on the target behaviour (e.g., donating money vs. time).
3.  **C-BEBA-03 (Mechanism Activation)**: Organisational brand communications are a primary mechanism for activating specific motivational states (e.g., warm glow) within the BEBA framework, thereby influencing the choice and outcome of the behavioural pathway.

# Boundary Conditions

-   **Target Behaviour Type**: The findings from `DT-000002` establish the type of supportive behaviour (time vs. money) as a critical boundary condition. The BEBA model must be specified and tested separately for different behaviours.
-   **Communication Framing**: The findings from `WG-000008` suggest that the framing of brand communication (donor-centric vs. recipient-centric) acts as a boundary condition for the effectiveness of the architecture.

# Model Competition Implications

This set of claims provides a clear mandate for a model competition approach to validating BEBA. The empirical strategy must not test a single, final BEBA model but rather compare competing theoretical explanations:

1.  **Model A (Pure Deliberation)**: A model where brand assets (Reputation) influence Trust, which in turn feeds into the components of an extended Theory of Planned Behavior to predict intention.
2.  **Model B (Pure Identity)**: A model where Brand Identification directly predicts intention, positioned as a powerful heuristic that bypasses deliberation.
3.  **Model C (Integrated Dual-Pathway BEBA)**: A model that includes both pathways from Model A and Model B, allowing them to operate in parallel and potentially interact.

The evidence from `BI-000051` explicitly suggests that Model C will provide a superior explanation to Model A or B alone. Furthermore, these competitions must be run separately for different target behaviours (donating time vs. money).

# Ontology Candidate Implications

To accommodate these findings, the BEBA information model and ontology should be extended with the following candidate concepts:

-   **Concept: `Behavioral Pathway`**: A new high-level concept to classify the route through which the brand enables behaviour.
    -   **Sub-Concept: `Deliberative-Cognitive Pathway`**: The TPB-based route.
    -   **Sub-Concept: `Affective-Identity Pathway`**: The identification-based route.
-   **Concept: `Target Behavior`**: Formalize this as a class with distinct instances (`DonateMoney`, `DonateTime`, `Advocacy`, etc.) to reflect that they are governed by different architectures.
-   **Relationship: `activates`**: A new relationship type to model how an `Organisational Action` (like a `Communication Appeal`) `activates` a `Psychological State` (like `Warm Glow`).

# Recommendation

1.  **Integrate the Dual-Pathway Architecture**: Formally adopt the dual-pathway structure (Deliberative-Cognitive and Affective-Identity) as the core explanatory framework for the BEBA theory. This should be reflected in `01_THEORETICAL_MAP.md`.
2.  **Propose New Canonical Claims**: Formulate the three `C-BEBA` claims listed above and add them to the claims repository as candidate claims for formal adoption.
3.  **Update Ontology Candidates**: Create candidate files for the new concepts (`Behavioral Pathway`, `Target Behavior`) and the `activates` relationship to be reviewed for inclusion in the canonical ontology.
4.  **Refine Empirical Strategy**: The research plan must be updated to prioritize model competition as described above. The goal is not to "prove" one BEBA model but to demonstrate the superior explanatory power of the dual-pathway model over simpler, single-pathway alternatives.
5.  **Segregate Behavioral Models**: All theoretical and empirical modeling must now explicitly state the `Target Behavior` it aims to explain, avoiding generalizations that treat all pro-social behaviours as homogenous.

## Integration from REVIEW-000101

**Integrated:** 2026-07-13T19:06:17.421318+00:00

**Accepted claims (6):**
- DI-000013: The Theory of Planned Behavior, extended with moral norms, is a highly predictive cognitive framewor
- TR-000029: Trust in a nonprofit organization positively influences donation intention by reducing perceived unc
- R-000006: Organizational reputation has both a direct positive effect on donation intention and an indirect po
- BI-000051: Donor identification with a nonprofit brand has a direct, positive effect on donation intention.
- WG-000008: Fundraising appeals emphasizing donor-centric benefits (e.g., warm glow) are more effective in incre
- DT-000002: The psychological antecedents for donating time differ systematically from the antecedents for donat

**Accepted evidence (15):**
- EVID-001902: The Theory of Planned Behavior (TPB) is a foundational and highly predictive model for charitable do
- EVID-001903: Perceived Behavioral Control (PBC) is the strongest predictor within the Theory of Planned Behavior 
- EVID-001904: Adding moral norms to the Theory of Planned Behavior (TPB) significantly increases its explanatory p
- EVID-001905: Donors use organizational trust and reputation as proxy signals to reduce the uncertainty inherent i
- EVID-001906: Trust in a nonprofit organization is a significant positive predictor of charitable giving intention
- EVID-001907: Organizational reputation influences donation intention through both a direct path and an indirect p
- EVID-001908: A donor's identification with a nonprofit's brand is a direct predictor of their intention to donate
- EVID-001909: Past donation behaviour is a strong predictor of future donation intention.
- EVID-001910: Fundraising appeals framed around donor-centric benefits like warm glow are more effective at increa
- EVID-001911: The direct effect of dispositional traits such as altruism and self-esteem on donation intention is 
- EVID-001912: Warm-glow motivation is an important driver of donations but is not a sufficient explanation on its 
- EVID-001913: The psychological drivers for donating time are systematically different from the drivers for donati
- EVID-001914: A CEO's reputation can moderate which predictors within the Theory of Planned Behavior are most sali
- EVID-001915: The dimensions of perceived organizational trustworthiness (ability, integrity, and benevolence) pos
- EVID-001916: Donor satisfaction as a predictor of donor loyalty and repeat giving behaviour is not sufficiently c

**Accepted sources (15):**
- SRC-000567: White, K., Sutton, L. S. C., & Zhao, X. (2023)
- SRC-000600: Chapman, C., Hornsey, M., & Gillespie, N. (2021)
- SRC-000601: Ghoorah, U., Talukder, M. H., & Khan, A. (2021)
- SRC-000520: Millán, Á., Retamosa, M., & Carranza, R. (2023)
- SRC-000602: List, J., Murphy, J., Price, M. K., & James, A. G. (2021)
- SRC-000603: Amonhaemanon, D., Khongkaew, P., Akartwipart, A., & Thamthanakoon, N. (2024)
- SRC-000604: Lee, J. Y., & Kim, S. S. (2023)
- SRC-000524: Kim, H. H., & Han, E. (2020)
- SRC-000605: Chen, Y., Dai, R., Yao, J., & Li, Y. (2019)
- SRC-000606: Carpenter, J. (2021)
- SRC-000575: Li, W., Mao, Y., & Liu, C. (2022)
- SRC-000607: Li, W., Yang, D.-H., & Sun, Y. (2022)
- SRC-000608: Benli, B., & Kocaman, R. (2025)
- SRC-000609: Robson, A., & Hart, D. (2020)
- SRC-000570: Mittelman, R., & Rojas Méndez, J. I. (2018)

