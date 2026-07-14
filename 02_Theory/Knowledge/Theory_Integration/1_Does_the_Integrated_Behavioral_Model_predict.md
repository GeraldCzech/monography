---
concept: 1_Does_the_Integrated_Behavioral_Model_predict
review: REVIEW-000097
claim_count: 5
claim_ids:
- TO-000007
- MN-000008
- PB-000028
- IB-000025
- SN-000007
status: accepted
review_status: reviewed
reviewed_at: '2026-07-12T06:10:28.405707+00:00'
reviewed_by: human
---

# Input Reviewed

The set of five claims (TO-000007, MN-000008, PB-000028, IB-000025, SN-000007) derived from a review of the Theory of Planned Behavior (TPB) in the context of charitable giving. These claims collectively argue for an extended TPB model that incorporates moral norms and past behavior, highlights the weakness of the intention-behavior link, and differentiates between types of social norms.

# Core Theoretical Implication

The standard, rational-calculative model of intention formation (TPB) is insufficient to explain nonprofit support. BEBA must operate as a dual-process framework that accounts for:
1.  A **deliberative pathway** (intention-based), which is strongly influenced by non-calculative **moral norms**.
2.  An **automatic pathway**, where **past behavior (habit)** directly drives future action.
3.  A significant **execution gap** (`Intention-Behavior Gap`) that the brand architecture must explicitly address.

# BEBA Layer Affected

**Layer: Individual**

All claims pertain directly to the psychological antecedents of individual donation behavior and intention.

# Existing Claims Supported

-   Claims that frame BEBA as a *behavior-centric* theory rather than an attitude-centric one are strongly supported by the `Intention-Behavior Gap` (IB-000025). The brand's job is not done when intention is formed.
-   Claims that position the brand as a mechanism for reducing friction and facilitating action are supported by the need to bridge the `Intention-Behavior Gap` (IB-000025).
-   Claims that emphasize the role of habit and loyalty are strongly supported by the finding that `Past Behavior` (PB-000028) is a powerful direct predictor of future intention and behavior.

# Existing Claims Challenged

-   Any existing claim that proposes a simple, linear progression from brand attitude -> intention -> behavior is challenged. The evidence suggests this model is underspecified.
-   Claims that treat "social influence" or "social norms" as a monolithic construct are challenged. The superior predictive power of `Injunctive Social Norms` (SN-000007) and `Moral Norms` (MN-000008) requires a more nuanced approach.
-   Claims that position brand equity's primary function as enhancing deliberative cognitions (e.g., brand attitude) are challenged. The strength of `Moral Norms` and `Past Behavior` suggests brand equity must also activate identity/values and trigger habits.

# New Candidate Claims

1.  **C-BEBA-011: Dual-Process Influence.** A nonprofit brand's effect on supportive behavior operates through two distinct pathways: a) an intention-formation pathway moderated by moral norms, and b) a habit-activation pathway.
2.  **C-BEBA-012: Moral Resonance as Equity Driver.** A key component of nonprofit brand equity is its ability to resonate with and activate an individual's pre-existing moral norms, making support feel like an obligation rather than a choice.
3.  **C-BEBA-013: Habit Formation as Brand Function.** A primary function of a BEBA is to convert initial, intention-driven behaviors into stable habits, thereby reducing the brand's long-term reliance on activating deliberative processing for repeat support.
4.  **C-BEBA-014: Gap-Bridging Mechanisms.** The behavioral effectiveness of a nonprofit brand is contingent on its inclusion of specific mechanisms that bridge the intention-behavior gap (e.g., implementation intentions, reminders, simplified action pathways).

# Boundary Conditions

-   The relative importance of the deliberative vs. automatic pathway may depend on the donor's history. For **new donors**, the extended TPB model (deliberative path) is likely dominant. For **repeat donors**, the `Past Behavior` (habitual path) may be the primary driver.
-   The effect of social norms may be highly context-dependent. `Injunctive Norms` may be more powerful in collectivist cultures or tight-knit communities.

# Model Competition Implications

This integration establishes a clear opportunity for model competition to test the core of BEBA:

-   **Model 1 (Baseline):** Standard TPB (Attitude + Subjective Norm + PBC -> Intention -> Behavior).
-   **Model 2 (Extended Rational Choice):** Extended TPB (Model 1 predictors + Moral Norms + Past Behavior -> Intention -> Behavior).
-   **Model 3 (BEBA-informed Dual-Process Model):** A model where Brand Equity influences the Extended TPB predictors, but also includes a direct path from Past Behavior to Future Behavior, and mechanisms designed to moderate the Intention -> Behavior link.

This directly addresses the "Competing explanations over single models" research principle.

# Ontology Candidate Implications

This review necessitates the creation or refinement of several concepts in the BEBA ontology:

1.  **New Concept Candidate: `Moral Norm`**. Must be created as a first-class concept, distinct from `Social Norm`. Definition should focus on an individual's personal sense of right and wrong or moral obligation.
2.  **New Concept Candidate: `Habit`**. `Past Behavior` is its operationalization. The concept of `Habit` itself, implying automaticity and reduced conscious guidance, needs to be formally defined.
3.  **Refinement of `Social Norm`**. This concept must be decomposed into `Injunctive Social Norm` (perceptions of what others approve/disapprove of) and `Descriptive Social Norm` (perceptions of what others actually do).
4.  **New Concept Candidate: `Intention-Behavior Gap`**. This should be formally included as a key phenomenon that the BEBA framework is designed to explain and solve.

# Recommendation

1.  **Update Theoretical Map:** Formally integrate a dual-process (deliberative vs. automatic) architecture into `01_THEORETICAL_MAP.md`.
2.  **Create Ontology Candidates:** Draft candidate files for the new concepts (`Moral Norm`, `Habit`, `Intention-Behavior Gap`) and the refined `Social Norm` components in the `03_Ontology/candidates/` directory.
3.  **Formulate New Claims:** Draft the `New Candidate Claims` listed above as formal claim objects and place them in the `04_Claims/` directory for further review.
4.  **Update Model Competition Plan:** Document the three-model competition structure (Baseline vs. Extended TPB vs. BEBA-Dual-Process) in the relevant research design or model competition file. This will be a central part of the empirical validation strategy.

## Integration from REVIEW-000097

**Integrated:** 2026-07-13T19:06:00.050666+00:00

**Accepted claims (5):**
- TO-000007: An extended Theory of Planned Behavior model incorporating moral norms and past behavior explains si
- MN-000008: The direct effect of moral norms on charitable giving intention is consistently stronger than the di
- PB-000028: Past donation behavior is a direct predictor of future donation intention, with an effect size compa
- IB-000025: Intention-based models explain a systematically and substantially lower proportion of variance in ac
- SN-000007: Injunctive social norms are a more reliable and significant predictor of donation intention than des

**Accepted evidence (12):**
- EVID-001857: The standard Theory of Planned Behavior explains 44% of the variance in charitable donation intentio
- EVID-001858: Extending the standard Theory of Planned Behavior with moral norms and past behavior significantly i
- EVID-001859: Adding moral norms to the standard TPB model increased the explained variance in donation intention 
- EVID-001860: Personal moral norms are a powerful and significant predictor of charitable giving intention, often 
- EVID-001861: Past donation behavior is a strong and consistent predictor of future donation intention.
- EVID-001862: A significant intention-behavior gap exists in charitable giving, where models explain intention sub
- EVID-001863: Injunctive social norms, reflecting perceived social approval, are a more consistent and significant
- EVID-001864: The effect of descriptive social norms, reflecting the perceived behavior of others, on donation int
- EVID-001865: Social norms can moderate the link between donation intention and subsequent donation behavior.
- EVID-001866: The predictive strength of different Theory of Planned Behavior components varies depending on the t
- EVID-001867: The reviewed literature lacks a direct, formal comparison of a distinct Integrated Behavioral Model 
- EVID-001868: The specific role of donor or role identity as a moderator of the intention-behavior relationship is

**Accepted sources (11):**
- SRC-000567: White, K., Sutton, L. S. C., & Zhao, X. (2023)
- SRC-000568: Smith, J. R., & McSweeney, A. (2007)
- SRC-000569: Veludo-De-Oliveira, T., Alhaidari, I. S., Yani-De-Soriano, M., & Yousafzai, S. Y. (2016)
- SRC-000570: Mittelman, R., & Rojas Méndez, J. I. (2018)
- SRC-000571: Fehresti, S., Takian, A., Jaafaripooyan, E., Parsaeian, M., & Jalilian, H. (2021)
- SRC-000572: Gugenishvili, I., & Colliander, J. (2022)
- SRC-000572: Gugenishvili, I., & Colliander, J. (2022)
- SRC-000573: Lakew, G., Gebretsadkan, B. T., Alemu, G. G., Bazezew, A. M., Yirsaw, A. N., Wondie, W., Mengistie, B. A., Dagnaw, T. E., Aweke, M. N., & Baykemagn, N. D. (2026)
- SRC-000574: Van Steenburg, E., & Spears, N. (2021)
- SRC-000575: Li, W., Mao, Y., & Liu, C. (2022)
- SRC-000576: Kusuma, H., & Anafisati, V. (2020)

