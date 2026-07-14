---
concept: Was_ist_der_intention_behavior_gap_Welche_modelle
review: REVIEW-000107
claim_count: 14
claim_ids:
- IB-000033
- IB-000034
- I-000004
- TO-000010
- PI-000005
- P-000001
- P-000002
- H-000002
- I-000005
- A-000015
- IB-000035
- I-000006
- C-000003
- RM-000002
status: candidate
---

# Input Reviewed

The integration protocol has been executed on a set of 14 candidate claims derived from a literature review (`REVIEW-000107`) on the Intention-Behavior Gap (IBG). These claims cover the existence of the gap, its primary drivers, the limitations of established models like TPB/TRA, and the role of post-intentional factors such as planning, habit, identity, and automaticity.

# Core Theoretical Implication

The core implication is that the Intention-Behavior Gap is the foundational problem that BEBA is designed to solve. The reviewed claims collectively establish that generating behavioral *intention* is a solved problem to a large extent (e.g., via TPB), but converting that intention into *action* is not. This validates the central premise of BEBA: that a brand's function must extend beyond persuasion and preference-shaping into the post-intentional, volitional phase of behavior enactment. BEBA is framed not as an alternative to intention-based models, but as a necessary architectural supplement that addresses their primary weakness.

# BEBA Layer Affected

-   **Individual Layer:** This is the primary layer affected. The claims deal with individual psychological constructs like intention (`I-000004`), planning (`P-000001`, `P-000002`), habit (`H-000002`), identity (`I-000005`), and automaticity (`A-000015`).
-   **Societal Layer:** This layer is secondarily affected through the concept of context (`C-000003`), which posits that environmental factors (resource availability, time) moderate the intention-action link. This requires BEBA to be a context-sensitive theory.

# Existing Claims Supported

The reviewed claims provide strong foundational support for BEBA's core tenets:

-   **Problem Relevance:** Claims `IB-000033` ("A substantial discrepancy exists...") and `I-000004` ("Intention is a necessary but insufficient predictor...") directly support BEBA's reason for existence.
-   **Theoretical Niche:** Claim `TO-000010` ("Models like TPB...are weak at explaining the conversion of intention into behavior") confirms the theoretical gap that BEBA aims to fill.
-   **Architectural Focus:** Claim `PI-000005` ("Explaining the...gap requires incorporating post-intentional psychological constructs...") is a direct validation of BEBA's focus on the volitional phase.
-   **Specific Mechanisms:** Claims on planning (`P-000001`, `P-000002`), habit (`H-000002`), identity (`I-000005`), and automaticity (`A-000015`) all support the inclusion of these specific mechanisms within the BEBA framework, where the brand acts as a facilitator or trigger for these processes.

# Existing Claims Challenged

No existing BEBA claims are directly challenged or contradicted by this input. The reviewed claims serve to ground and justify the theory, rather than to challenge it. They do, however, implicitly challenge any simplistic version of BEBA that might ignore the initial strength of intention or contextual factors.

# New Candidate Claims

Based on this integration, the following claims could be formalized for BEBA:

1.  **BEBA-C-001 (Target Population):** The primary function of a Brand-Enabled Behaviour Architecture is to convert 'inclined abstainers'—individuals with positive behavioral intentions but a failure to act—into consistent actors. (Derived from `IB-000034`)
2.  **BEBA-C-002 (Planning Support):** A BEBA reduces the volitional burden of enacting intentions by providing cognitive and environmental scaffolds for action planning and coping planning. (Derived from `P-000001`, `P-000002`)
3.  **BEBA-C-003 (Cueing Function):** A core BEBA mechanism involves engineering brand touchpoints as situational cues that trigger desired automatic responses, thereby bypassing or supporting deliberative control. (Derived from `A-000015`, `H-000002`)
4.  **BEBA-C-004 (Identity Alignment):** A BEBA strengthens the intention-behavior link by increasing the perceived centrality of the desired behavior to the individual's self-concept through brand identity alignment. (Derived from `I-000005`)

# Boundary Conditions

The reviewed claims introduce two critical boundary conditions for BEBA's effectiveness:

1.  **Intention Strength (`I-000006`):** BEBA is not designed to create intention from scratch. Its effectiveness is likely moderated by the pre-existing strength of an individual's intention. The architecture is most relevant for those with medium-to-strong intentions who still fail to act.
2.  **Contextual reality (`C-000003`):** BEBA is not a purely psychological system. Its ability to facilitate behavior is constrained by real-world contextual factors like resource availability, time, and social opportunity. A brand's architecture can fail if it is not designed to operate within the user's actual environment.

# Model Competition Implications

-   **Complement to TPB/TRA:** This integration solidifies BEBA's position as a *complement* to, not a *competitor* of, models like the Theory of Planned Behavior. BEBA's mechanisms operate *after* TPB has explained intention. This clarifies BEBA's contribution.
-   **Integrative Framework:** Claim `IB-000035` ("No single, universally accepted model adequately explains the gap") justifies the need for BEBA as an *integrative framework* that orchestrates multiple post-intentional mechanisms (planning, habit, identity) rather than championing a single one. BEBA's competitive claim is its ability to show how a *brand* serves as the unifying architecture for these disparate mechanisms.
-   **Methodological Edge:** Claim `RM-000002` suggests a direction for empirical model competition: demonstrating that a BEBA-informed model performs better in predicting *within-person* behavioral dynamics over time, moving beyond the static, between-person designs common in the field.

# Ontology Candidate Implications

1.  **New Concept: `Inclined Abstainer`**. This term from `IB-000034` perfectly describes the target persona for BEBA interventions. It should be added to the ontology as a key `Stakeholder` or `Persona` type.
2.  **Refinement of `Planning`**. The distinction between `Action Planning` (`P-000001`) and `Coping Planning` (`P-000002`) is crucial. The `Planning` concept in the ontology should be refined to include these two sub-types, as a brand might support them in different ways.
3.  **Solidification of Core Concepts:** The claims cement the importance of formally defining `Post-Intentional Phase`, `Volitional Control`, and `Situational Cue` as first-class citizens in the BEBA information model.

# Recommendation

1.  **Update Core Problem Definition:** Create or update a core theory document (e.g., `02_Theory/01_Core_Problem/The_Intention_Behavior_Gap.md`) to formally position the IBG as the central puzzle BEBA solves, using these 14 claims as the evidentiary basis.
2.  **Propose New Claims:** Submit the four "New Candidate Claims" listed above for formal review and inclusion in the BEBA claims registry.
3.  **Update Ontology:** Create an `Ontology Candidate` file proposing the addition of `Inclined Abstainer` and the sub-typing of `Planning` into `Action Planning` and `Coping Planning`.
4.  **Add Methodological Note:** Add a note to the `Research Compass` or create a `DecisionLog` entry highlighting the methodological implication from `RM-000002`—that empirical validation of BEBA should prioritize dynamic, within-person research designs (e.g., ecological momentary assessment, longitudinal studies).
