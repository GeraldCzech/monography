---
title: "Chapter M — Methodological Charter: Evidence-Based Theory Construction in the BEBA Project"
status: draft
object_type: Chapter
layer: Meta / Organisational
claim_anchors:
  - BE-000079
  - BE-000080
  - ET-000001
  - EW-000001
  - JC-000001
  - LP-000001
  - KG-000001
  - KG-000002
  - BM-000008
  - MR-000001
  - FO-000001
  - TS-000003
  - BR-000019
  - BR-000020
  - EP-000001
  - EP-000002
reviews: [REVIEW-000112, REVIEW-000121, REVIEW-000122]
---

# Chapter M — Methodological Charter: Evidence-Based Theory Construction in the BEBA Project

## Scientific Question

Why is the comparison and formal aggregation of competing theoretical explanations epistemologically superior to the isolated confirmation of a single model — and how does this principle operationalise into a research architecture?

---

## M.1 The Problem: Why Conventional Reviews Do Not Build Theory

The field of nonprofit branding has produced a substantial body of empirical work over the past three decades. Yet the accumulation of studies has not produced a correspondingly cumulative theoretical edifice. Review articles recapitulate findings, meta-analyses pool effect sizes across incompatible operationalisations, and narrative synthesis papers produce frameworks that are re-constructed anew with each review cycle rather than revised in light of prior evidence (Tranfield et al., 2003).[^M-TS-000003]

This is not a failure of individual researchers but a structural consequence of two dominant methodological conventions in social science. The first is **null-hypothesis significance testing (NHST)** as the primary epistemic arbiter. NHST reduces the complex evidential relationship between data and theory to a binary gate: statistically significant or not. It does not quantify how much evidence supports a claim, does not permit the formal combination of evidence across studies under different methodological conditions, and actively discourages the expression of degrees of belief (Cohen, 1994; Royall, 1997).[^M-LP-000001] The result is a literature composed of islands of isolated findings rather than a connected, revisable body of knowledge.

The second convention is the **narrative literature review** as the standard synthesis method. Narrative reviews depend on the reviewer's judgment at every stage of selection, interpretation, and integration. They are not formally replicable, they do not produce machine-readable outputs, and they do not provide a principled mechanism for weighting evidence by source quality or evidential strength (Higgins et al., 2019; Templier & Paré, 2015).[^M-TS-000003]

The BEBA project takes the position — grounded in philosophy of science — that cumulative theory building requires different tools: a formal epistemology of evidence, a structured synthesis workflow, and a computationally tractable representation of the resulting theory. These three elements form the methodological charter of the project.[^M-BR-000019]

---

## M.2 The Epistemological Foundation: The Likelihood Paradigm

The BEBA project adopts the **Likelihood Paradigm** as its core framework for understanding what it means for evidence to support a claim (Royall, 1997).[^M-LP-000001]

In this framework, the key question is not "Is this result statistically significant?" but rather: "How much more probable are the observed data under one hypothesis compared to a competing hypothesis?" Evidence is evaluated through the **likelihood ratio**: the probability of the data given the focal hypothesis divided by the probability of the data given the best alternative hypothesis.

A likelihood ratio greater than one favours the focal hypothesis; a ratio less than one favours the alternative. This formulation makes three things explicit that NHST conceals:

1. Evidence is always *relative* — it supports one hypothesis over another, never in isolation.
2. Evidence is *continuous* — stronger evidence produces larger likelihood ratios, not just a binary gate.
3. Evidence is *separable from prior belief* — what the data say (likelihood) can be distinguished from what one should believe after seeing them (posterior).

This distinction — between the **likelihood** (what data say) and the **posterior** (what one should believe) — is fundamental to the BEBA evidence-integration architecture.[^M-EVID-002176] It allows the project to handle the situation, common in social science, where different researchers hold different prior beliefs about a claim but need to agree on what the empirical evidence says.

---

## M.3 Bayesian Evidence Synthesis

Once the Likelihood Paradigm establishes how individual pieces of evidence are evaluated, **Bayesian Evidence Synthesis** provides the formal mechanism for integrating evidence across multiple studies and updating beliefs over time.[^M-BE-000079]

The core machinery is Bayes' theorem in its odds form:

$$\frac{P(H_1 \mid D)}{P(H_2 \mid D)} = \frac{P(D \mid H_1)}{P(D \mid H_2)} \times \frac{P(H_1)}{P(H_2)}$$

The posterior odds ratio is the product of the likelihood ratio and the prior odds ratio. Every new piece of evidence updates the relative credibility of competing hypotheses.[^M-fn-bayes]

In a research programme with many evidence items — as in BEBA, where reviewed evidence currently spans more than 2,100 EVID objects — this updating is not done manually claim by claim. Instead, evidence items are assigned to claims, weighted by source quality (see Section M.5), and the cumulative evidence base shifts posterior probabilities across the claim set. Claims with a large, consistent, high-quality evidence base gain high posterior credibility; claims supported by few, methodologically weak, or contradictory studies remain at lower credibility until further evidence arrives.

This approach has several properties that conventional synthesis methods lack (Gelman et al., 2013; Howson & Urbach, 2006):

- **Transparency:** The weight of each piece of evidence is explicit and revisable.
- **Cumulativity:** New evidence updates beliefs rather than replacing prior synthesis.
- **Uncertainty quantification:** Posterior probability distributions express degrees of belief, not binary verdicts.
- **Model competition:** Multiple competing hypotheses can be simultaneously evaluated against the same evidence base.

The treatment of prior probabilities requires care. The BEBA project follows Jaynes (2003) in adopting *weakly informative* priors calibrated to the existing literature.[^M-fn-priors] Where strong prior consensus exists in the field, this is reflected in relatively high starting priors; where the literature is contested or sparse, priors are set near 0.5 to let the evidence speak.

---

## M.4 Jeffrey Conditionalization: Updating on Uncertain Evidence

A standard challenge in social science synthesis is that evidence rarely arrives in the form of logically certain observations. A study does not *prove* that brand trust reduces donation uncertainty; it provides partial, design-conditioned, construct-validly limited evidence for this claim. The BEBA project handles this through **Jeffrey Conditionalization** (Jeffrey, 1983).[^M-JC-000001]

Classical conditionalization updates beliefs only when new evidence is treated as certain. Jeffrey Conditionalization extends this to the case where the new information is itself uncertain — where the evidence shifts one's confidence in a proposition without making it certain.[^M-fn-jeffrey]

The updating rule is:

$$P'(H) = P(H \mid E) \cdot P'(E) + P(H \mid \neg E) \cdot P'(\neg E)$$

Here, $P'(E)$ is the posterior probability assigned to the evidence proposition after reviewing the study — a value less than 1.0 if the study has methodological limitations, construct validity concerns, or cross-cultural generalisability issues. This allows the BEBA pipeline to formally represent what reviewers express informally as "this study suggests, but does not confirm, that..."[^M-BE-000080]

In the BEBA Trust and Potency System, methodological quality is quantified through four auditable subscores — source trust, author trust, article trust, and study potency — that together determine how much credibility weight an evidence item receives when updating claim posteriors (see Section M.5).

---

## M.5 The Trust and Potency System: Source Quality as Formal Evidence Weight

One of the most important contributions of BEBA's methodological architecture is the replacement of informal judgements about source quality with a **formal, auditable scoring system**.[^M-BM-000008]

Every source object (SRC-XXXXXX) in the BEBA knowledge base receives a **Trust composite score** computed from four independently verifiable subscores:

| Subscore | Weight | Operationalisation |
|---|---|---|
| `source_trust` | 0.30 | Journal tier via Scimago/OpenAlex |
| `author_trust` | 0.20 | h-Index via OpenAlex |
| `article_trust` | 0.20 | Citation count via Semantic Scholar |
| `potency` | 0.30 | Study design via LLM-assisted extraction |

**Retraction protection:** If a source's article has been retracted, `article_trust` is set to 0 and the composite Trust score collapses to 0.0, removing the source from the evidence-weighting calculation entirely. This prevents the well-documented problem of post-retraction citation contamination.

The `potency` subscore deserves particular attention. Where source trust and article trust are bibliometric proxies for community esteem, potency is a direct assessment of **internal evidential strength**: whether the study used an appropriate design for the claim it supports, whether effect sizes were reported, whether samples were adequate, whether key confounders were addressed. This operationalises the Royallian insight that *what the data say* is a function of study design, not just of how the scientific community received the study.

The composite score is a pure function of the four subscores; it is never stored, only computed at evaluation time. This means that recalibrating the weighting scheme (e.g., based on domain-specific validation work) automatically propagates to all composite scores without requiring re-annotation of individual sources.

---

## M.6 The Evidence-Theory-Ontology Pipeline

The three epistemological components — the Likelihood Paradigm, Bayesian Evidence Synthesis, and Jeffrey Conditionalization — are embedded within a structured **Evidence-Theory-Ontology (ETO) workflow** that governs how raw literature is transformed into formal theory (Eisenhardt, 1989; Tranfield et al., 2003).[^M-EW-000001]

The pipeline operates in seven stages:

```
1  Synthesis        Literature → structured evidence synthesis (synthesized/<stem>.md)
2  Evidence + SRC   Synthesis → evidence objects (EVID-XXXXXX) + source stubs (SRC-XXXXXX)
3  Claims           Evidence → claim objects with IDs and confidence levels
4  Theory           Claims → Theory_Integration/<concept>.md
5  Ontology         Theory → Ontology_Candidates/<concept>.md
6  Review           Human-in-the-loop validation (REVIEW-XXXXXX.md)
7  Finalise         INDEX.yaml + master.bib + manifest update
```

Each transition is explicit, traceable, and stored as a named object in the knowledge base. The pipeline never permits a jump from raw literature to theoretical conclusion — each step must be completed and reviewed before the next begins. This operationalises the BEBA principle: *evidence before preference*.[^M-ET-000001]

The human review stage (Step 6) is structurally non-negotiable. AI-assisted processing handles the extraction and structuring of evidence; human review handles the theoretical interpretation, the assessment of competing explanations, and the final decision to accept, reject, or hold objects. This prevents the conflation of AI-generated text with scientific authority — a risk that purely AI-driven literature synthesis systems do not adequately address.

---

## M.7 Formal Ontology: Making Theory Computable

The output of the ETO pipeline is not a narrative chapter but a **formal ontology** — an explicit, machine-readable specification of the concepts, relationships, and constraints that constitute the developing theory (Gruber, 1993; Noy & McGuinness, 2001).[^M-FO-000001]

An ontology in this sense is not a glossary or a conceptual diagram. It is a structured representation with the following properties:

- **Unambiguity:** Each concept has exactly one canonical definition; there are no synonyms or context-dependent meanings at the ontological level.
- **Relationship typing:** Relationships between concepts are formally typed (e.g., `causes`, `moderates`, `mediates`, `is-a`, `part-of`) rather than expressed through prose.
- **Computability:** The ontology can be queried, reasoned over, and extended without loss of consistency.
- **Extensibility:** New evidence can add nodes and edges to the ontology without invalidating existing structure.

The BEBA information model distinguishes a **substantive namespace** (`beba-theory:`) covering nonprofit brand equity, donor behaviour, and organisational mechanisms from a **methodological namespace** (`beba-meta:`) covering the epistemic and procedural concepts described in this chapter (Suppe, 1977).[^M-BR-000020]

This self-documentation property — the ontology representing not only the theory being studied but also the method of studying it — is a specific design choice. It makes the BEBA project's epistemological commitments part of its machine-readable output, enabling future researchers to critique, revise, or extend the methodology through the same formal apparatus.

---

## M.8 Middle-Range Theory as the Appropriate Target

The BEBA project does not aim to produce a grand unified theory of charitable behaviour. The appropriate theoretical target is **middle-range theory** in the sense of Merton (1968): bounded, empirically testable propositions that are specific enough to make falsifiable predictions and general enough to extend across contexts.[^M-MR-000001]

Merton's concept responds to the tension between grand theories (which are too abstract to generate empirical predictions) and merely empirical generalisations (which are too specific to constitute theory). Middle-range theories occupy the productive intermediate: they explain why and how a defined phenomenon occurs, under specified boundary conditions, and generate predictions that can be tested against data.

For the BEBA project, this means the theoretical target is not "a theory of everything about nonprofit marketing" but rather:

> *How do nonprofit brands become behaviourally effective under conditions of uncertainty?* — and specifically, which mechanisms (signalling, trust formation, uncertainty reduction, identity alignment, social norming) account for the observed relationships between brand equity dimensions and stakeholder behaviour, and under which boundary conditions do these mechanisms operate?

This formulation is bounded (nonprofit brands), empirically tractable (observable brand dimensions, measurable behaviour), and generative (it implies competing causal models that can be tested against each other). Weick's (1989) framing of theory construction as "disciplined imagination" is apposite: the goal is to generate a model set that is both imaginative enough to go beyond what the data directly show and disciplined enough to remain falsifiable.[^M-EVID-002182]

---

## M.9 The BEBA Project as Methodological Exemplar

The ETO pipeline, the Bayesian evidence architecture, the Trust and Potency scoring system, and the formal ontology are not only the methods of the BEBA project; they constitute an **exemplar** of a specific paradigm for social science theory building (Suppe, 1977).[^M-BR-000020]

The paradigm can be stated concisely:

| Traditional paradigm | BEBA paradigm |
|---|---|
| Narrative synthesis | Structured ETO workflow |
| NHST significance | Bayesian evidence synthesis |
| Implicit source quality | Formal Trust/Potency scoring |
| Prose chapters | Formal ontology + human chapters |
| Isolated studies | Cumulative belief revision |
| Single confirming model | Model competition with likelihoods |

This is a claim of *methodological superiority in a specific domain* — not a universal claim. As the evidence itself indicates (EVID-002190), the ETO methodology is most effective in research domains characterised by a fragmented body of empirical literature with contested constructs and heterogeneous methods.[^M-EP-000002] The nonprofit branding literature satisfies this condition: construct definitions differ across studies, operationalisations are rarely standardised, effect sizes vary widely, and no single dominant theoretical model has emerged (Rios Romero et al., 2023).

The methodological contribution of the BEBA project is therefore twofold: it produces substantive theory about nonprofit brands as behaviour architectures *and* it demonstrates a methodology for producing such theory in complex, fragmented social science domains.

---

## Footnotes

[^M-TS-000003]: **Claim TS-000003** (REVIEW-000112): NHST-based meta-analyses and purely narrative reviews are insufficient for building cumulative, computationally tractable theory. Sources: SRC-001174 (Cohen, 1994), SRC-001026 (Tranfield et al., 2003). Evidence: EVID-002188, EVID-002202.

[^M-LP-000001]: **Claim LP-000001** (REVIEW-000112): The Likelihood Paradigm frames scientific inference as a comparison of competing hypotheses through their relative likelihoods of producing observed data, avoiding the epistemic conflation embedded in NHST. Source: SRC-001171 (Royall, 1997).

[^M-BE-000079]: **Claim BE-000079** (REVIEW-000121): Bayesian evidence synthesis provides a more rigorous, transparent, and epistemologically sound method for theory building than NHST-based approaches. Sources: SRC-001168 (Howson & Urbach, 2006), SRC-001032 (Gelman et al., 2013), SRC-001172 (Jaynes, 2003). Evidence: EVID-002173, EVID-002174, EVID-002175, EVID-002177.

[^M-BE-000080]: **Claim BE-000080** (REVIEW-000122): Bayesian updating via Jeffrey Conditionalization offers a coherent epistemological framework for aggregating uncertain evidence. Source: SRC-001178 (Jeffrey, 1983). Evidence: EVID-002196, EVID-002197.

[^M-JC-000001]: **Claim JC-000001** (REVIEW-000112): Jeffrey Conditionalization is a formal mechanism for revising the strength of beliefs based on new uncertain evidence. Source: SRC-001178 (Jeffrey, 1983).

[^M-EW-000001]: **Claim EW-000001** (REVIEW-000122): The ETO workflow is a valid and rigorous methodology for moving from heterogeneous empirical inputs to formal theory. Sources: SRC-001026 (Tranfield et al., 2003), SRC-001033 (Eisenhardt, 1989). Evidence: EVID-002194.

[^M-ET-000001]: **Claim ET-000001** (REVIEW-000112): The Evidence-Theory-Ontology workflow provides a structured, replicable alternative to narrative literature reviews. Evidence: EVID-002178, EVID-002179.

[^M-FO-000001]: **Claim FO-000001** (REVIEW-000121): Formal ontology is a necessary and sufficient step to translate social science theory into a computationally tractable, unambiguous, and scalable knowledge representation. Sources: SRC-001019 (Gruber, 1993), SRC-001029 (Noy & McGuinness, 2001). Evidence: EVID-002183, EVID-002184, EVID-002185.

[^M-MR-000001]: **Claim MR-000001** (REVIEW-000121): Middle-range theory provides the appropriate level of abstraction for building testable and practically applicable social science theory. Source: SRC-001034 (Merton, 1968). Evidence: EVID-002181.

[^M-KG-000002]: **Claim KG-000002** (REVIEW-000122): Representing a developing social science theory as a knowledge graph provides a more precise, communicable, and extensible structure than prose or path diagrams. Evidence: EVID-002195, EVID-002199, EVID-002200.

[^M-BM-000008]: **Claim BM-000008** (REVIEW-000112): The synthesis of Bayesian Evidence Aggregation, ETO Workflow, Jeffrey Conditionalization, Likelihood Paradigm, and Knowledge Graph constitutes the BEBA Methodological Framework as a novel contribution in its own right.

[^M-BR-000019]: **Claim BR-000019** (REVIEW-000122): A research design integrating Bayesian evidence aggregation, a structured ETO workflow, and a knowledge graph is superior for cumulative theory development compared to disconnected significance-tested studies. Evidence: EVID-002193, EVID-002201.

[^M-BR-000020]: **Claim BR-000020** (REVIEW-000122): The BEBA research design operationalises the semantic view of scientific theories. Source: SRC-001181 (Suppe, 1977). Evidence: EVID-002203.

[^M-EP-000002]: **Claim EP-000002** (REVIEW-000121): The effectiveness of the ETO methodology is conditional on the existence of a fragmented body of empirical literature in the research domain. Evidence: EVID-002190.

[^M-EVID-002176]: EVID-002176: A strict distinction should be made between what data say (likelihood), what one should believe (posterior), and what one should do (decision). Source: SRC-001171 (Royall, 1997).

[^M-EVID-002182]: EVID-002182: Theory construction can be viewed as a process of disciplined imagination where quality is determined by plausibility and testability. Source: SRC-001020 (Weick, 1989).

[^M-fn-bayes]: The odds form of Bayes' theorem is used here because it makes the multiplicative updating structure explicit and permits clear separation of prior beliefs from evidential weight. For the full derivation and computational treatment, see Gelman et al. (2013, ch. 1) and Jaynes (2003, ch. 2).

[^M-fn-priors]: The specification of weakly informative priors is itself a theoretical choice requiring justification. The BEBA project draws on the prior-elicitation literature (Higgins & Spiegelhalter, 2002; SRC-001169) and uses the existing empirical literature's central tendency as a reference point for prior calibration.

[^M-fn-jeffrey]: Classical Bayesian conditioning assumes the evidence proposition $E$ becomes certain: $P'(E) = 1$. Jeffrey Conditionalization relaxes this to allow $0 < P'(E) < 1$, which is the epistemologically appropriate form for scientific evidence. See Jeffrey (1983) for the full formal treatment.
