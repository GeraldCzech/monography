---
title: "Chapter 5 — Philosophy of Science and Model Competition"
status: draft
object_type: Chapter
layer: Meta / Societal
claim_anchors:
  - BE-000079
  - BE-000080
  - LP-000001
  - JC-000001
  - TS-000003
  - BR-000019
  - BR-000020
  - EP-000001
  - EP-000002
  - NB-000101
  - RQ-000002
  - RQ-000003
  - R-000012
reviews: [REVIEW-000112, REVIEW-000121, REVIEW-000122, REVIEW-000100, REVIEW-000118]
---

# Chapter 5 — Philosophy of Science and Model Competition

## Scientific Question

Why is the systematic comparison of competing theoretical model architectures epistemologically superior to the isolated confirmation of a single model — and what practical consequences does this position have for empirical research design?

---

## 5.1 Two Philosophies of Science and Their Consequences

Scientific inquiry in the social sciences has been shaped by two broad epistemological traditions that produce different research practices, different standards of evidence, and ultimately different theories.

The first tradition, rooted in the **verification-oriented positivism** of the Vienna Circle and its successors, treats science as the progressive accumulation of confirmed facts. A theory is accepted when it passes empirical tests; it is rejected when it fails them. The practical consequence in psychology and marketing research is the confirmatory hypothesis test: the researcher derives a prediction from theory, collects data, and interprets statistical significance as confirmation.

The second tradition, associated most prominently with Popper (1959) and elaborated by Lakatos (1978), Kuhn (1970), and the semantic view of theories (Suppe, 1977), holds that theories cannot be confirmed — only provisionally corroborated or refuted. Scientific progress occurs not through accumulation but through **competition between rival theoretical programmes**. A theory is not simply accepted or rejected but maintained until a superior competitor displaces it by explaining more, predicting novel phenomena, or generating more productive research.

The BEBA project adopts the second tradition. The choice is not merely philosophical — it has concrete methodological consequences for every aspect of the research design.[^5-BR-000020]

---

## 5.2 The Failure Mode of Single-Model Confirmation in Social Science

The dominant research practice in marketing, psychology, and nonprofit studies is built around **null hypothesis significance testing (NHST)**: a researcher posits a null hypothesis (typically: no relationship), collects data, and treats $p < .05$ as evidence for the alternative (there is a relationship). This practice has been the subject of sustained methodological critique since at least the 1960s.

The critique has several distinct strands:

**1. NHST does not quantify evidence.** A p-value tells you the probability of observing data at least as extreme as obtained *if the null hypothesis is true*. It does not tell you the probability that the null hypothesis is true, nor the probability that the alternative hypothesis is true. A p-value of 0.049 and a p-value of 0.001 are treated as equivalent (both "significant") despite representing very different evidential situations (Cohen, 1994).[^5-TS-000003]

**2. NHST encourages theoretical laziness.** Because significance testing is binary and the null hypothesis is invariably false in social science (any two variables have some nonzero relationship in any sufficiently large sample), almost any study can produce "significant" results with a large enough sample. Meehl (1978) termed the endemic correlation structure of social science phenomena the "crud factor" — the general tendency of psychological variables to be weakly but positively correlated, which means the null hypothesis is never literally true. In this context, rejecting the null hypothesis provides almost no theoretical information.

**3. Single-model confirmation is not model selection.** When a researcher tests whether "brand equity predicts donation intention" and finds a significant coefficient, they have not established that a brand equity model is superior to a competing model — they have only established that the relationship exists at some nonzero magnitude. The comparison with alternatives (What if perceived social norms are the real driver? What if trust alone accounts for all the variance?) is simply not conducted.[^5-LP-000001]

**4. The replication crisis has reached philanthropy research.** Bekkers's (2026) preprint systematically assessed the replicability of charitable giving findings. Approximately 60% of attempted replications confirmed prior results — a replication rate that, while not catastrophic, indicates that a substantial proportion of published findings in the philanthropy literature are false positives, underpowered, or context-specific findings that do not generalise (Bekkers, 2026).[^5-RQ-000002] Several mechanisms previously treated as foundational — the identifiable victim effect in field settings, situational reputation cues ("watching eyes"), public recognition — replicate poorly or not at all under pre-registered conditions.[^5-R-000012]

This situation constitutes the background against which BEBA's model competition framework is designed: not as a response to a stable, well-replicated literature but to a fragmented, partly non-replicable body of evidence in which single-model confirmation is particularly misleading.

---

## 5.3 The Likelihood Paradigm at the Model Level

Chapter M introduced the Likelihood Paradigm as a framework for evaluating individual evidence items. The same framework extends to the evaluation of **theoretical models** — and this extension is the epistemological core of the model competition approach (Royall, 1997).[^5-LP-000001]

At the model level, the question is: given the observed data, which of the competing structural models is better supported? The likelihood function for a model $M_i$ with parameters $\theta_i$ given data $D$ is:

$$\mathcal{L}(M_i \mid D) = P(D \mid M_i, \hat{\theta}_i)$$

where $\hat{\theta}_i$ are the maximum likelihood estimates of the model parameters. The **likelihood ratio** between two models:

$$\Lambda = \frac{\mathcal{L}(M_1 \mid D)}{\mathcal{L}(M_2 \mid D)}$$

quantifies the relative evidential support that the data provide for $M_1$ versus $M_2$. Values substantially greater than one favour $M_1$; values near one indicate insufficient discriminative evidence; values substantially less than one favour $M_2$.[^5-fn-lr]

In structural equation modelling — the primary analytic tool of the empirical chapters — the model likelihood function is evaluated through fit indices and model comparison tests. The key distinction from NHST is that model comparison is *comparative* rather than absolute: a model is not evaluated against the null hypothesis ("does brand equity have any effect?") but against a specific competing model ("does the BEBA architecture explain donation behaviour better than a standard IBM/TPB model, and by how much?").

---

## 5.4 Bayesian Model Comparison

Bayesian inference provides the formal framework for model comparison that fully inherits the likelihood approach while additionally expressing prior model probabilities (Gelman et al., 2013).[^5-BE-000079]

The **Bayes Factor** $BF_{12}$ compares models $M_1$ and $M_2$:

$$BF_{12} = \frac{P(D \mid M_1)}{P(D \mid M_2)} = \frac{\int P(D \mid \theta_1, M_1) P(\theta_1 \mid M_1) \, d\theta_1}{\int P(D \mid \theta_2, M_2) P(\theta_2 \mid M_2) \, d\theta_2}$$

The Bayes Factor integrates over the prior distributions on each model's parameters, which means it automatically penalises overfitted models — a model that fits the current data well by using many free parameters but has a diffuse prior on those parameters will receive a lower Bayes Factor than a parsimonious model that is well-calibrated to the data.[^5-fn-bf]

Jeffreys (1961) provided interpretive guidelines: $BF_{12} > 10$ provides strong evidence for $M_1$; $BF_{12} > 100$ provides decisive evidence. In SEM contexts, approximations to the Bayes Factor are available through information criteria: the Bayesian Information Criterion (BIC) approximates $-2 \log BF$, and differences in BIC between models provide a practical model comparison tool without full Bayesian estimation.[^5-fn-bic]

The Bayesian model comparison framework has one property that is particularly important for the BEBA project: it handles **model uncertainty** rather than forcing a binary choice between models. The posterior probability of each model in a comparison set can be computed, and in empirical applications where no single model is decisively superior, this probability distribution over models accurately represents the evidential state rather than forcing an artificial winner.

---

## 5.5 Research Programmes and Theoretical Progress

Lakatos's (1978) concept of **scientific research programmes** provides a higher-level framework for understanding how the model competition approach positions the BEBA project in the broader theoretical landscape.

A research programme in Lakatos's sense consists of a **hard core** — the central theoretical commitments that are protected from direct refutation — and a **protective belt** of auxiliary hypotheses that are tested and revised. Theoretical progress occurs when the programme generates novel predictions that are empirically confirmed; theoretical degeneration occurs when the programme can only explain past data through post-hoc adjustments.

The BEBA project constitutes a research programme in this sense:

| Component | Content |
|---|---|
| **Hard core** | Nonprofit brand equity is a multi-dimensional architecture that reduces uncertainty and enables behaviour through identifiable mechanisms |
| **Protective belt** | Specific mechanism weights, contextual moderators, measurement model choices |
| **Novel predictions** | Model C (configural BEBA) will outperform Models A and B; trust pathway is the strongest single mechanism; Bourdieu-augmented Model D will add unique variance |

The programme's progress is measured not by whether individual studies are statistically significant but by whether the family of models it generates progressively explains more about donation behaviour than the competing programmes (IBM/TPB alone, commercial brand equity models, purely altruistic models).

---

## 5.6 Competing Models in the BEBA Empirical Programme

The four-model competition introduced in Chapter 4 (Section 4.5) is now formalised as an empirical programme. The models are nested in a partial order: each more complex model contains the previous as a special case, which permits formal likelihood ratio testing.[^5-fn-nested]

**Model A: Standard IBM/TPB.**  
Attitude, Subjective Norms, and Perceived Behavioural Control as direct antecedents of Donation Intention. No brand equity constructs.

**Model B: Brand Equity-Augmented IBM/TPB (Full Mediation).**  
Brand equity dimensions as exogenous variables, fully mediated by Attitude, Subjective Norms, and PBC. Brand equity adds no direct path to Intention.

**Model C: Configural BEBA (Partial Mediation).**  
Brand equity dimensions retain direct paths to Intention alongside mediated paths. Different dimensions are permitted to load primarily on different IBM/TPB constructs (brand image → Attitude; brand trust → PBC; overall brand equity → direct Intention).

**Model D: Bourdieu-Augmented BEBA.**  
Model C extended with field-level symbolic capital dynamics. Includes cross-level interactions between organisational brand position and individual-level mechanisms.

The empirical programme tests these models in sequence: first establishing Model A as a baseline, then comparing the incremental fit and likelihood of each more complex model. The comparison is evaluated through likelihood ratio tests, BIC differences, and theoretically interpreted fit indices (CFI, RMSEA, SRMR). A model is preferred when it offers substantially better fit *and* the additional parameters are theoretically interpretable rather than merely statistically extractable.[^5-fn-fit]

This approach reflects a core BEBA principle: **parsimony is not the only virtue**. A model that is parsimonious but wrong about the mechanisms — that finds a global "brand equity effect" but cannot distinguish the trust pathway from the awareness pathway — is less useful for theoretical development than a more complex model that correctly identifies the mechanism structure, even at the cost of additional parameters.

---

## 5.7 The Replication Problem and Evidential Conservatism

The replication crisis in philanthropy research (Bekkers, 2026) and in psychology more broadly (Open Science Collaboration, 2015) has a specific implication for the BEBA project: **the prior probability that any particular published finding will replicate is meaningfully less than one**. This is not a counsel of despair but an evidential reality that should be formally incorporated into the research design.[^5-RQ-000003]

The BEBA Trust and Potency system (described in Chapter M) operationalises this insight at the source level: sources are weighted by the quality of the study design that produced them, not merely by their presence in the literature. A highly-cited but methodologically weak study receives lower potency weight than a less-cited but methodologically rigorous one.

At the model level, the same conservatism applies. The model competition framework avoids the replication problem's worst consequence — the cascade of non-replicating effects built into theory by uncritical narrative synthesis — by requiring that model preferences be grounded in likelihood comparisons rather than in the significance of individual coefficients.

Claim RQ-000002 from the Bekkers (2026) preprint provides a specific empirical anchor: approximately 60% of philanthropy research findings replicate, and the non-replication rate is substantially higher for mechanisms that rely on subtle psychological framing effects.[^5-RQ-000002] The BEBA model competition framework responds to this by focusing on structural relationships (brand equity mechanisms) rather than framing effects, and by treating the empirical results from Part III not as confirmatory tests but as likelihood updates on prior theoretical positions.

---

## 5.8 Model Competition and the Intention-Behaviour Gap

A specific empirical challenge for the BEBA programme is the **intention-behaviour gap** — the well-documented finding that behavioural intentions are substantially stronger predictors of self-reported intention than of actual behaviour (Sheeran, 2002; Webb & Sheeran, 2006).

In the BEBA evidence base, this gap is visible in the posterior probabilities computed for different claim types: intention-related claims have substantially higher posterior credibility than behaviour-related claims for the same brand equity predictors.[^5-fn-ibgap] The brand equity–intention relationship is relatively well-supported; the brand equity–behaviour relationship is more ambiguous.

This creates a model competition question at the outcome level: does a model targeting **donation intention** represent the same theoretical construct as a model targeting **actual donation behaviour**? If the intention-behaviour pathway is imperfect (as the literature suggests), then a model that predicts intention well may predict behaviour poorly — not because brand equity is ineffective but because the intention-to-behaviour translation depends on additional factors (habituation, situational constraints, salience at moment of choice) that brand equity does not govern.

The BEBA empirical programme addresses this by measuring both intention and behaviour as separate outcomes, permitting direct comparison of brand equity effects across the intention-behaviour boundary. The model competition framework then evaluates whether the structural architecture that best explains intention is the same architecture that best explains behaviour, or whether the two require different theoretical specifications.

---

## 5.9 Implications for the Empirical Programme

The model competition framework established in this chapter generates five design requirements for the empirical chapters (8–10):

1. **Multiple models must be specified in advance.** The four competing BEBA models must be preregistered before data collection to prevent post-hoc model selection.

2. **Fit evaluation must be comparative, not absolute.** Model A (standard IBM/TPB) is the reference against which BEBA models are evaluated. Fit indices are interpreted as comparisons between models, not as absolute thresholds.

3. **Both intention and behaviour must be measured.** The intention-behaviour gap is a theoretical issue, not a measurement convenience. Both must be included as outcomes.

4. **Mechanism evidence must be reported.** Indirect effects (mediation paths) must be estimated and reported alongside direct effects to provide evidence for specific mechanisms, not only for "brand equity predicts donation."

5. **Bayesian and frequentist results must be reconciled.** Likelihood-based model comparison (BIC, Bayes Factors) and conventional fit indices must both be reported to permit readers to evaluate the evidence under both frameworks.

---

## Footnotes

[^5-BR-000020]: **Claim BR-000020** (REVIEW-000122): The BEBA research design provides a practical application of the semantic view of scientific theories. Source: SRC-001181 (Suppe, 1977). Evidence: EVID-002203.

[^5-TS-000003]: **Claim TS-000003** (REVIEW-000112): NHST-based meta-analyses and narrative reviews are insufficient for building cumulative, computationally tractable theory. Sources: SRC-001174 (Cohen, 1994), SRC-001026 (Tranfield et al., 2003). Evidence: EVID-002188, EVID-002202.

[^5-LP-000001]: **Claim LP-000001** (REVIEW-000112): The Likelihood Paradigm frames scientific inference as a comparison of competing hypotheses through their relative likelihoods of producing observed data. Source: SRC-001171 (Royall, 1997). Evidence: EVID-002176.

[^5-BE-000079]: **Claim BE-000079** (REVIEW-000121): Bayesian evidence synthesis provides a more rigorous, transparent, and epistemologically sound method for theory building than NHST-based approaches. Sources: SRC-001032 (Gelman et al., 2013), SRC-001168 (Howson & Urbach, 2006). Evidence: EVID-002173 to EVID-002177.

[^5-RQ-000002]: **Claim RQ-000002** (REVIEW-000118): Approximately 60% of philanthropy research replications confirm prior results, indicating a meaningful false-positive rate in the published literature. Source: Bekkers (2026). Evidence: BEBA Knowledge Base, REVIEW-000118.

[^5-RQ-000003]: **Claim RQ-000003** (REVIEW-000118): The prior probability of a published philanthropy finding replicating is substantially less than 1.0, requiring formal evidential conservatism in theory building. Source: Bekkers (2026).

[^5-R-000012]: **Claim R-000012** (REVIEW-000118): Several widely cited charitable giving mechanisms — the identifiable victim effect in field settings, situational reputation cues, public recognition — replicate poorly under pre-registered conditions. Source: Bekkers (2026).

[^5-NB-000101]: **Claim NB-000101** (REVIEW-000100): Causal claims from cross-sectional survey data are likely inflated by common method bias, requiring caution in interpreting single-study coefficient magnitudes. Evidence: BEBA Knowledge Base, REVIEW-000100.

[^5-fn-lr]: The interpretive benchmarks for likelihood ratios follow Royall (1997): $\Lambda > 8$ provides strong evidence for $M_1$; $8 \geq \Lambda > 3$ provides moderate evidence; $\Lambda \approx 1$ indicates weak evidence. These benchmarks are not universal conventions but Royall's suggested thresholds — they should be applied with judgment rather than mechanically.

[^5-fn-bf]: The full computation of Bayes Factors requires specification of parameter priors, which is itself a theoretical choice. For the BEBA empirical programme, weakly informative priors calibrated to the meta-analytic effect size distribution in the nonprofit brand equity literature will be used. BIC-based approximations are used where full Bayesian estimation is computationally impractical.

[^5-fn-bic]: BIC difference interpretation follows Raftery (1995): $|\Delta BIC| > 10$ provides strong evidence; $6 < |\Delta BIC| \leq 10$ provides positive evidence; $2 < |\Delta BIC| \leq 6$ provides weak evidence; $|\Delta BIC| \leq 2$ is not worth more than a bare mention. These thresholds apply to comparisons between non-nested models; nested model comparisons use the likelihood ratio test.

[^5-fn-nested]: Models A through C are strictly nested (each contains the previous as a restricted case). Model D is not fully nested in Models A–C because it introduces cross-level effects. Model comparison for D uses BIC and Bayes Factor approximations rather than the likelihood ratio test.

[^5-fn-fit]: Standard fit thresholds (CFI > .95, RMSEA < .06, SRMR < .08) are used as descriptive benchmarks rather than as hard pass/fail criteria. The model comparison interpretation takes precedence: a model with slightly lower absolute fit that represents a theoretically meaningful architecture is preferred over a numerically well-fitting model with uninterpretable parameter structure.

[^5-fn-ibgap]: The intention-behaviour gap is visible in the BEBA evidence base through the posterior probability differences between brand equity–intention claims (posterior ≈ 0.85–0.92 across multiple claims) and brand equity–behaviour claims (posterior ≈ 0.61 for some specific pathways). See `04_brand_equity_layer_draft.md` for the full posterior summary.
