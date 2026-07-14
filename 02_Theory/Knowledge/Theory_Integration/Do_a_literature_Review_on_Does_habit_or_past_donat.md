---
concept: Do_a_literature_Review_on_Does_habit_or_past_donat
review: REVIEW-000103
claim_count: 5
claim_ids:
- PB-000029
- IB-000026
- DP-000002
- HF-000001
- BE-000064
status: candidate
---

# Input Reviewed

-   `PB-000029`: Past donation behavior is a significant predictor of future donation behavior.
-   `IB-000026`: A significant gap exists between donation intention and actual donation behavior.
-   `DP-000002`: The effect of past donation on future donation is mediated by cognitive automaticity and relational commitment.
-   `HF-000001`: Context stability moderates the relationship between past behavior and cognitive automaticity.
-   `BE-000064`: A strong nonprofit brand fosters donation by increasing commitment and serving as a stable cue for automaticity.

# Core Theoretical Implication

The integration of these five claims forms the central causal engine of the BEBA theory. It posits that the well-documented intention-behavior gap in prosocial behavior (`IB-000026`) can be explained and addressed by a dual-process model. This model moves beyond purely deliberative/intentional explanations.

Specifically, it argues that the strong predictive power of past behavior (`PB-000029`) is not just an artifact but a substantive effect channeled through two parallel pathways: a deliberative, relational pathway (`Relational Commitment`) and a non-deliberative, automatic pathway (`Cognitive Automaticity`) (`DP-000002`).

The brand is the critical component that activates and sustains this dual-process architecture. It simultaneously builds the `Relational Commitment` necessary for the deliberative path and provides the `Context Stability` (`HF-000001`) required for the automatic path, acting as a recurring cue that facilitates habit formation (`BE-000064`).

Therefore, BEBA is not merely Brand Equity *leading to* behavior; it is a **Brand-Enabled Behaviour Architecture** that explains *how* a brand structures the psychological process to make desired behaviors (like donating) more reliable and repeatable.

# BEBA Layer Affected

-   **Individual Layer**: The entire synthesized mechanism operates at the individual psychological level, explaining donor decision-making and behavior formation.

# Existing Claims Supported

-   This synthesis strongly supports the foundational claim that **Brand Equity is a behavioral asset, not just a perceptual one.** It provides the specific micro-foundations for *how* brand perceptions translate into reliable behavior.
-   It supports the claim that **BEBA is a process-oriented theory**, focusing on the dynamics of behavior over time (past -> future) rather than a static prediction at a single point in time.
-   It directly validates the framing of the **intention-behavior gap as the central research problem** for the monograph.

# Existing Claims Challenged

This synthesis does not challenge existing *internal* BEBA claims; rather, it forms their core. However, it mounts a significant challenge to external theoretical approaches applied to nonprofit marketing:

-   It challenges the **sufficiency of purely deliberative models** like the Theory of Planned Behavior (TPB) or Theory of Reasoned Action (TRA) in explaining recurring donation. It argues they are incomplete because they neglect the role of habit and automaticity.
-   It challenges brand models that treat Brand Equity as a simple direct antecedent to a global 'behavioral intention' construct, arguing for a more nuanced, dual-pathway mediation.

# New Candidate Claims

This synthesis suggests the formulation of a higher-order, integrative claim that could serve as the master hypothesis for the entire monograph:

-   **Claim Candidate `BEBA-CORE-01`**: "Nonprofit brand equity closes the intention-behavior gap by functioning as a dual-process architecture that converts past supportive behavior into future supportive behavior through parallel, reinforcing pathways of (a) deliberative, relational commitment and (b) non-deliberative, context-cued cognitive automaticity."

# Boundary Conditions

-   The claim `HF-000001` explicitly introduces **Context Stability** as a key boundary condition. The habit-formation (automaticity) pathway of the BEBA model is theorized to be strongest in stable contexts where the brand can act as a reliable cue (e.g., regular giving programs, annual appeals).
-   Conversely, in highly volatile or one-off contexts (e.g., novel disaster appeals, new fundraising event formats), the model predicts the automaticity pathway will be weaker, and the deliberative/relational pathway will be the dominant driver of behavior.

# Model Competition Implications

This synthesis sets up a clear agenda for empirical model competition:

1.  **BEBA vs. Deliberative Models**: The BEBA model can be tested against a restricted model that only includes the intentional pathway (e.g., a standard TPB model). The BEBA model would predict a significant direct or habit-mediated path from past behavior to future behavior, which the TPB model omits.
2.  **BEBA vs. Habit-Only Models**: The BEBA model can be tested against a model that only includes the automaticity/habit pathway. The BEBA model would predict that the relational commitment pathway adds significant explanatory power, especially in contexts of changing goals or high involvement.
3.  **Testing the Brand's Role**: The moderating role of the brand (as a stable cue) can be tested. The model predicts that the path `Past Behavior -> Automaticity -> Future Behavior` will be significantly stronger for individuals with high brand awareness/salience compared to those with low awareness.

# Ontology Candidate Implications

This synthesis solidifies the centrality of several key concepts and their relationships, requiring explicit definition in the BEBA ontology:

-   **Concepts**: `Cognitive Automaticity`, `Relational Commitment`, `Context Stability`, `Brand as Cue`.
-   **Relationships**:
    -   `Past Behavior` -> (mediates) `Cognitive Automaticity` -> `Future Behavior`
    -   `Past Behavior` -> (mediates) `Relational Commitment` -> `Future Behavior`
    -   `Brand Salience` -> (moderates) `Context Stability`
    -   `Context Stability` -> (moderates) `Past Behavior` -> `Cognitive Automaticity` link.
-   The term **BEBA** itself is ontologically defined as the integrated system comprising these two parallel pathways, enabled by the brand.

# Recommendation

1.  **Formalize the Core Theory**: This synthesized argument should be documented in a new or existing core theory file, likely `02_Theory/BEBA_CORE_THEORY.md`. This document should serve as the canonical explanation of the monograph's central mechanism.
2.  **Create a Canonical Figure**: A directed acyclic graph (DAG) visually representing this dual-pathway model should be created and stored as a canonical figure (`04_Figures/FIG_BEBA_DUAL_PROCESS_MODEL.md`). This figure will be the central organizing visual for the theory chapters and empirical work.
3.  **Update Ontology Candidates**: Create or update ontology candidate files for `Cognitive Automaticity` and `Relational Commitment`, specifying their proposed role as parallel mediators between past and future behavior within the BEBA framework.
4.  **Prioritize for Empirical Testing**: The model competition implications outlined above should be used to structure the empirical validation plan. The test of the full dual-pathway model against restricted (deliberative-only, habit-only) models should be a primary empirical objective.
