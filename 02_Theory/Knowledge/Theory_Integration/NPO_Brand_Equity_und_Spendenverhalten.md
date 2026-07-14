---
concept: NPO_Brand_Equity_und_Spendenverhalten
review: REVIEW-000123
claim_count: 5
claim_ids:
- BA-000084
- BI-000054
- BD-000013
- BD-000014
- BE-000081
status: accepted
review_status: reviewed
reviewed_at: '2026-07-14T15:59:57.328641+00:00'
reviewed_by: human
---

# Input Reviewed

The input consists of a set of five candidate claims from `REVIEW-000123`. These claims concern the relationship between nonprofit brand constructs (Awareness, Image, Differentiation) and their influence on social norms, behavioural intentions, and the notable gap between intention and actual behaviour in the existing research.

# Core Theoretical Implication

The core implication is twofold and central to the BEBA project's justification:

1.  **Mechanism Specification:** The claims provide a specific social-cognitive mechanism for the BEBA architecture: key brand perceptions (awareness, image) can shape behaviour by influencing an individual's perception of descriptive social norms. This fleshes out how a brand acts as a social, not just an individual, enabler.
2.  **Strategic Justification:** The claims (`BD-000014`, `BE-000081`) powerfully validate BEBA’s core research principle of "Behaviour before brands." By identifying the intention-behaviour gap as a significant, under-addressed weakness in the field, the input confirms that BEBA's focus on actual, enacted behaviour is a necessary and high-value contribution.

# BEBA Layer Affected

-   **Primary: Individual:** Claims `BA-000084`, `BI-000054`, `BD-000013`, and `BD-000014` operate at the level of the individual stakeholder, describing how their perceptions of a brand influence their social cognitions (perceived norms) and conative states (intentions).
-   **Secondary: Market/Field:** Claim `BE-000081` is a meta-claim about the state of the nonprofit branding research field. It affects BEBA at a strategic level, justifying its positioning and methodological priorities within the broader academic discourse.

# Existing Claims Supported

The reviewed claims provide strong support for several foundational BEBA principles and assumptions:

-   **"Behaviour before brands":** Claim `BE-000081` provides direct, field-level evidence justifying this core research principle, framing BEBA's focus on actual behaviour as a critical corrective to a known gap in the literature.
-   **Brand as a social-cognitive architecture:** Claims `BA-000084` and `BI-000054` support the "architecture" concept by demonstrating that brand perceptions do more than influence individual attitudes; they structure how individuals perceive the social context of a behaviour (i.e., its normative status).
-   **Brand-enabled behavioural precursors:** Claim `BD-000013` supports the general BEBA logic that brand constructs like differentiation are upstream antecedents of behavioural precursors, such as intention and commitment.

# Existing Claims Challenged

The input does not directly contradict any core BEBA claims, but it crucially qualifies and challenges oversimplified interpretations of the brand-to-behaviour link:

-   **Challenge to simplistic "Brand -> Behaviour" models:** Claim `BD-000014` directly challenges any assumption that strong brand differentiation automatically leads to stakeholder action. It forces BEBA to explicitly theorize and model the intention-behaviour gap as a critical point of friction or failure within the architecture.
-   **Challenge to assumption of direct effects:** The set of claims collectively suggests that the path from brand perception to behaviour is indirect, mediated by social norms and intentions, and fraught with potential breakdowns. This challenges any BEBA model that relies too heavily on unmediated, direct effects of brand on behaviour.

# New Candidate Claims

Based on the synthesis of the reviewed claims, the following higher-level candidate claims are proposed for BEBA:

-   **Candidate Claim (Mechanism): BEBA-SN-01**  
    **Statement:** Nonprofit brand equity influences stakeholder behaviour in part by shaping perceptions of descriptive social norms, thereby altering the social-cognitive context of the decision to act.

-   **Candidate Claim (Friction): BEBA-GAP-01**  
    **Statement:** The translation of brand-enabled intention into actual stakeholder behaviour is a distinct, non-guaranteed stage within the BEBA, representing a primary locus of behavioural friction and a key point for empirical investigation.

-   **Candidate Claim (Differentiation Role): BEBA-DIF-01**  
    **Statement:** The primary behavioural function of nonprofit brand differentiation is to strengthen cognitive and conative precursors (e.g., intention, commitment), while its translation into actual behaviour is contingent upon other factors that bridge the intention-behaviour gap.

# Boundary Conditions

The reviewed claims imply a crucial boundary condition for the BEBA architecture:

-   The effectiveness of brand-building efforts (like increasing differentiation) in producing *actual behaviour* is conditional on the presence of mechanisms or contextual factors that successfully bridge the intention-behaviour gap. In the absence of such factors (e.g., low-friction action pathways, strong situational cues), the behavioural return on brand investment will be limited to intentional outcomes.

# Model Competition Implications

These claims have significant implications for BEBA's empirical strategy:

1.  **Justifies BEBA vs. Intention Models:** The claims validate the competition between a full BEBA model (predicting `Actual Behaviour`) and standard models that terminate at `Behavioural Intention`. Claim `BE-000081` provides the rationale that intention-only models are insufficient for the nonprofit field.
2.  **Specifies a Social Norms Mediation Model:** Claims `BA-000084` and `BI-000054` suggest a clear mediational model for testing:  
    `Brand Perceptions (Awareness, Image) -> Perceived Social Norms -> Behavioural Intention -> Actual Behaviour`.  
    This should be tested against competing models (e.g., one where brand only affects attitude).
3.  **Requires Moderated-Mediation Models:** Claim `BD-000014` suggests that the final `Intention -> Behaviour` link is not constant. This calls for testing models where this path is moderated by factors that either facilitate or inhibit action (e.g., perceived behavioural control, opportunity, situational salience).

# Ontology Candidate Implications

The input necessitates refinement and elevation of several concepts within the BEBA ontology:

-   **`Intention-Behaviour Gap`**: This concept must be formalized as a core theoretical component of BEBA, not just a methodological note. It should be treated as a key point of **behavioural friction** in the architecture. A dedicated concept or relationship file is warranted.
-   **`Perceived Descriptive Social Norm`**: This concept is confirmed as a critical intermediary. The BEBA information model must formally represent its relationship as an outcome of brand perceptions (e.g., Awareness, Image).
-   **`Brand Differentiation`**: The ontology entry for this construct should be refined to specify its primary impact is on **precursors to behaviour** (intention, commitment), with its effect on actual behaviour being indirect and conditional.
-   **`Actual Behaviour` vs. `Behavioural Intention`**: The claims reinforce the absolute necessity of maintaining a strict distinction between these two constructs throughout the BEBA ontology and empirical work.

# Recommendation

1.  **Adopt Candidate Claims:** Fully integrate the five candidate claims from `REVIEW-000123` into the BEBA knowledge base.
2.  **Elevate the Intention-Behaviour Gap:** Make the "Intention-Behaviour Gap" a formal, high-priority theoretical problem within BEBA. Create a candidate concept file for `Behavioural Friction` that explicitly incorporates the gap as a primary manifestation.
3.  **Update Theoretical Map:** Revise `01_THEORETICAL_MAP.md` to include a candidate pathway from `Brand Awareness` and `Brand Image` to `Perceived Social Norms`.
4.  **Prioritize Behavioural Measures:** Issue a formal recommendation (e.g., via a DecisionLog entry) that all future empirical studies under the BEBA framework must prioritize the measurement of `Actual Behaviour` over `Behavioural Intention`.
5.  **Create Integration Memo:** Create a new Theory Integration Memo in `02_Theory/Integration_Memos/` named `BEBA_Theory_Integration_Social_Norms_Intention-Gap_REVIEW-000123.md` to serve as the canonical record of this analysis.

## Integration from REVIEW-000123

**Integrated:** 2026-07-14T16:00:21.789810+00:00

**Accepted claims (5):**
- BA-000084: Increased stakeholder awareness of a nonprofit brand enhances the perceived descriptive social norm 
- BI-000054: A nonprofit brand image characterized by high social standing and perceived popularity is positively
- BD-000013: Perceived brand differentiation of a nonprofit has a positive effect on stakeholders' intention to d
- BD-000014: The direct effect of perceived brand differentiation on actual stakeholder donation behaviour is not
- BE-000081: A significant intention-behaviour gap exists in nonprofit brand research, with most studies measurin

**Accepted evidence (14):**
- EVID-002207: High brand awareness can lead individuals to misinterpret cognitive fluency as a signal of an NPO's 
- EVID-002208: Brand image dimensions such as 'established', 'market leader', or 'mainstream' function as direct he
- EVID-002209: The effect of brand differentiation on actual donation behaviour is likely mediated by the stakehold
- EVID-002210: The 'Popularity/Social Standing' dimension of a nonprofit's brand image significantly predicts stake
- EVID-002211: A strong, dynamic nonprofit brand image increases the perception that the organization is important 
- EVID-002212: Nonprofit brand personality dimensions of 'Integrity' and 'Stateliness' (prestige/establishment) are
- EVID-002213: Integrating explicit popularity cues like "#1 Charity" or "Over 1 Mio. Supporters" into an organizat
- EVID-002214: A nonprofit's perceived brand distinctiveness is positively associated with stakeholder commitment a
- EVID-002215: Nonprofit organizations with strongly differentiated brand positioning, such as through a unique imp
- EVID-002216: In commercial markets, perceived brand uniqueness is strongly and positively related to actual repea
- EVID-002217: The probability of actual giving increases significantly when donors understand what makes a nonprof
- EVID-002218: A direct, unmediated causal link from perceived brand differentiation to actual donation behaviour i
- EVID-002219: There is a lack of NPO-specific studies directly testing the causal link from brand awareness to a f
- EVID-002220: There is an unresolved methodological challenge in distinguishing whether an established brand image

**Accepted sources (8):**
- SRC-000362: Bennett, R., & Gabriel, H. (2003)
- SRC-000359: Michel, G., & Rieunier, S. (2012)
- SRC-000363: Venable, B. T., Rose, G. M., Bush, V. D., & Gilbert, F. W. (2005)
- SRC-001182: Sundar, S. S., Tamul, D. J., & Wu, M. (2014)
- SRC-000374: Stride, H.; Lee, S. (2007)
- SRC-001183: Kylander, N., & Stone, C. (2012)
- SRC-001184: Netemeyer, R. G., Krishnan, B., Pullig, C., Wang, G., Yagci, M., Dean, D., Ricks, J., & Wirth, F. (2004)
- SRC-000330: Bekkers, R., & Wiepking, P. (2011)

