# BEBA Evidence Synthesis for Preregistration Revision


_Generated from BEBA-ROS verification pipeline. Only sources and findings grounded in machine-verified PDF passages are included._


---


## 1. Methodology

### 1.1 Overview

This document synthesises the empirical evidence base underlying the
Brand-Enabled Behaviour Architecture (BEBA) framework and serves as the
theoretical foundation for the preregistration revision of the associated
survey study. The evidence was assembled through a systematic multi-phase
verification pipeline described below.

### 1.2 Literature Retrieval and Source Qualification

A total of **969 source records** were identified across multiple
database searches (Scopus, Web of Science, Google Scholar, Crossref) and
snowballing from key review articles. Sources were classified as *accepted*
(peer-reviewed primary studies or systematic reviews), *candidate*, or *stub*
(records with insufficient metadata). **581 sources** passed
the *accepted* quality threshold.

### 1.3 PDF Acquisition and Text Extraction

Full-text PDFs were retrieved via DOI resolution (Unpaywall), institutional
access, and manual upload. Text extraction was performed using PDFMiner.
**585 source records** had machine-readable full text
available for verification.

### 1.4 Evidence Extraction

Evidence items (EVIDs) were extracted from accepted sources through an
AI-assisted pipeline. Each EVID captures a discrete empirical finding
(*finding*), its directional relationship to a theoretical construct
(*direction*: supports / mixed / contradicts / neutral), and an extraction
confidence rating (*high / medium / low*). A total of **2148 EVIDs**
were extracted.

### 1.5 Automated Verification (Key Funnel Step)

Each EVID was subjected to automated PDF-grounded verification. The verifier
retrieved passages from the source PDF that semantically match the EVID
finding and compared them against the extracted claim. The outcome was one of:

| Status | Meaning | Count |
|---|---|---|
| **supported** | Verbatim or near-verbatim passage found confirming the finding | 772 (35.9%) |
| unsupported | No corroborating passage found; finding may be an over-extraction | 600 |
| uncertain | Passage found but insufficient to confirm or reject | 40 |
| unverifiable | No machine-readable PDF available for this source | 731 (34.0%) |
| failed | Verification attempt failed (LLM parse error) | 5 |

**Only EVIDs with `verification_status: supported` are used in subsequent
analyses.** This constitutes a strict fidelity criterion: every empirical
claim incorporated below is backed by a verbatim or near-verbatim passage
from the original source document.

Sources contribute to the evidence base only if they appear in at least one
verified EVID. This yields a **verified source set of 517
sources** out of 969 retrieved.

### 1.6 Bayesian Claim Scoring

Each theoretical claim (extracted from the systematic literature reviews as
explicit propositions) is scored using a Beta-Binomial Bayesian update. The
prior is set from the claim's extraction confidence level
(high: α=4, β=1; medium: α=2, β=2; low: α=1, β=3).
Each linked verified EVID updates the posterior:
- **supports**: α += strength_weight × extraction_weight × source_quality × 2
- **contradicts**: β += same
- **mixed**: α += 0.5 × weight, β += 0.3 × weight
- **neutral**: α += 0.2 × weight

Only EVIDs with `verification_status ∈ {supported, unsupported, uncertain}`
contribute to the Bayesian update; unverifiable and failed EVIDs are excluded.
The posterior mean P = α / (α + β) is reported as the **evidence confidence**
for each claim.

Grade thresholds: A ≥ 0.75 · B ≥ 0.60 · C ≥ 0.45 · D ≥ 0.30 · F < 0.30


## 2. Empirical Claims by Concept

_Claims with grade A or B are recommended as preregistration hypotheses. Claims with grade C–D are exploratory. Claims graded F or unlinked should not appear as confirmatory hypotheses._

### Trust
_N claims: 30 · Mean posterior: 0.92 · Grade A/B: 30_

- **[TR-000001]** Trust is a recurring relational dimension of customer-based brand equity in integrated brand equity and behavioural mode…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000003]** Trust in a nonprofit mediates the relationship between positive nonprofit brand perceptions and donation intention.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000007]** Organisational and sectoral trust are strong predictors of charitable giving in nonprofit contexts.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000024]** The relationship between stakeholder trust and donation behaviour is not consistently positive and significant across al…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000029]** Trust in a nonprofit organization positively influences donation intention by reducing perceived uncertainty.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000030]** Perceived high administrative costs are a primary reason given by non-donors for not giving money to nonprofits.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000002]** Organizational and sector-level trust are associated with a higher propensity to give.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000004]** Trust in a charitable organization or donation platform increases the predictive validity of extended Theory of Planned …  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000005]** In online donation and crowdfunding environments, trust in the receiving organization or platform is a crucial facilitat…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000006]** Trust reduces perceived risk and uncertainty associated with donating.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000008]** Brand-related trust reduces perceived risk and uncertainty in donation decisions.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000010]** Trust in an NGO reduces donor uncertainty when donors cannot directly observe the organization’s service delivery or imp…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000011]** Stakeholder trust increases sustained support for nonprofit organisations.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000012]** International nonprofit brands function as trust proxies for donors who cannot directly observe the services or impact p…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000013]** Consistent fulfilment of the brand promise increases stakeholder trust in the brand.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000014]** The variance in public trust in a nonprofit organization is predominantly explained by individual-level factors rather t…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000015]** The stable context of a trustor accounts for a portion of variance in their trust evaluations that is approximately equa…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000016]** The objective characteristics of a nonprofit organization explain less than 10% of the total variance in public trust ev…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000017]** The public display of a recognized, third-party accountability certification is positively associated with public trust …  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000018]** A nonprofit mission focused on children is positively associated with public trust.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000019]** In a largely secular societal context, an explicit religious mission is negatively associated with trust from the genera…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000020]** Trust in nonprofit organizations is positively correlated with an individual's age.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000021]** Women report higher levels of trust in nonprofit organizations than men.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000022]** Trust in nonprofit organizations is negatively correlated with an individual's income level.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000023]** Organizational age is a weak but positive predictor of public trust in a nonprofit organization.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000025]** The effect of stakeholder trust on donation behaviour is moderated by other variables.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000026]** Perception of a nonprofit brand as a "Good Samaritan" archetype is positively associated with public trust in that brand…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000027]** Perception of a nonprofit brand as a "Marketer" archetype is negatively associated with public trust in that brand.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000028]** The negative effect on public trust from a "Marketer" perception is not significantly mitigated by the provision of fina…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408

- **[TR-000009]** Brand-related trust increases perceived behavioural control over the donation decision by reducing perceived risk.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 128 supporting, 5 contradicting, 21 mixed · N sources: 408


### Brand Equity
_N claims: 34 · Mean posterior: 0.91 · Grade A/B: 34_

- **[BE-000001]** Integrating customer-based brand equity constructs into IBM/TPB frameworks increases the explanatory power of models of …  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000002]** Customer-based brand equity functions as a multi-dimensional construct comprising perceptual, relational, and quality-re…  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000004]** Customer-based brand equity is a multi-dimensional construct that includes perceptual inputs, relational aspects, and qu…  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000005]** Integrating customer-based brand equity constructs into IBM or TPB models improves the explanatory power of models predi…  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000013]** Brand equity is commonly conceptualized as a hierarchical or sequential process grounded in an associative network memor…  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000015]** Brand equity research developed from financial conceptualisation in the 1980s to foundational customer-based and manager…  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000027]** Brand equity is conceptualised as a multidimensional construct comprising awareness, associations or image, and loyalty …  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000045]** Brand equity is used in the literature to denote at least three distinct constructs: brand value, brand strength, and br…  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000049]** Consumer-based brand equity can be operationalized as a three-dimensional construct comprising Brand Loyalty, Perceived …  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000050]** The constructs of Brand Awareness and Brand Associations, while conceptually distinct, lack empirical discriminant valid…  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000052]** Consumer-based brand equity, as measured by the Multidimensional Brand Equity (MBE) scale, is a significant positive cor…  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000062]** Commercial brand equity models require adaptation to account for mission- and trust-based dimensions to be effective in …  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000070]** The power of a brand resides in the knowledge structures held by customers in their minds.  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000071]** Brand equity is the differential effect of brand knowledge on customer response to marketing activities.  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000072]** A brand with positive equity elicits more favorable customer responses than an equivalent unbranded product or service.  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000073]** The primary function of branding is to create meaningful differences between products and services in the minds of custo…  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000074]** High brand equity leads to greater customer loyalty.  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000075]** The relative importance of different brand equity dimensions is moderated by the product or service category.  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000076]** The psychological processes for building brand equity are moderated by cultural context.  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000003]** Brand equity can be represented as a configural process consisting of brand building, brand understanding, and brand rel…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000006]** Brand equity is not a mandatory component of the Integrated Model of Behaviour.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000026]** Nonprofit brand equity is associated with giving intention.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000034]** University brand equity is built through brand awareness, perceived quality, brand trust, brand loyalty, and positive br…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000044]** Aggregate-level analysis of brand equity metrics conceals significant differences between consumer loyalty segments.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000046]** Brand equity consists of added value that a brand gives to a product or service beyond its functional attributes.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000047]** High brand equity increases customer loyalty relative to otherwise comparable low-equity brands.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000048]** High brand equity reduces customer susceptibility to competitors’ marketing actions.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000053]** The relative contribution of brand equity dimensions to the overall brand equity construct varies across cultures; Perce…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000054]** Brand loyalty is a positive antecedent of brand equity.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000055]** Models of brand equity formation that include brand trust as a mediating variable have better explanatory power than mor…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000058]** Perceived brand equity has a significant positive effect on an individual's intention to donate to a nonprofit organizat…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000059]** Perceived brand equity does not have a statistically significant direct effect on an individual's actual giving behavior…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000063]** There is no consistent evidence in the reviewed literature for a direct, causal effect of nonprofit brand equity on stak…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435

- **[BE-000066]** The multidimensional construct of nonprofit brand equity serves as a measurable proxy for the bundle of mixed motives dr…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 214 supporting, 14 contradicting, 49 mixed · N sources: 435


### Warm Glow Giving
_N claims: 1 · Mean posterior: 0.91 · Grade A/B: 1_

- **[WG-000009]** Donors derive private, emotional utility (warm glow) from the act of giving itself, independent of the actual outcome.  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 34 supporting, 2 contradicting, 5 mixed · N sources: 120


### Attitude
_N claims: 6 · Mean posterior: 0.91 · Grade A/B: 6_

- **[A-000005]** Customer-Based Brand Equity dimensions positively influence attitude toward performing a behavior.  
  P = 0.94 · A (strong) ⚠ conflict  
  EVIDs: 41 supporting, 0 contradicting, 5 mixed · N sources: 135

- **[A-000001]** Brand image is a significant antecedent of attitude toward a brand-related behaviour.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 41 supporting, 0 contradicting, 5 mixed · N sources: 135

- **[A-000002]** Brand associations are significant antecedents of attitude toward a brand-related behaviour.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 41 supporting, 0 contradicting, 5 mixed · N sources: 135

- **[A-000003]** Brand personality is a significant antecedent of attitude toward a brand-related behaviour.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 41 supporting, 0 contradicting, 5 mixed · N sources: 135

- **[A-000004]** Brand image, brand personality, and brand associations significantly predict attitude toward a behavior.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 41 supporting, 0 contradicting, 5 mixed · N sources: 135

- **[A-000006]** Brand image, brand personality, and perceived quality shape individual attitudes toward brand-related behaviours.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 41 supporting, 0 contradicting, 5 mixed · N sources: 135


### Solicitation
_N claims: 11 · Mean posterior: 0.90 · Grade A/B: 11_

- **[S-000004]** Being asked to donate is the strongest predictor of whether an individual in Austria donates.  
  P = 0.93 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 26

- **[S-000006]** The majority of charitable donations are made in response to a direct solicitation.  
  P = 0.93 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 26

- **[S-000014]** Direct verbal requests for donations increase giving.  
  P = 0.93 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 26

- **[S-000015]** Direct verbal requests for donations can trigger avoidance behaviour in potential donors.  
  P = 0.93 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 26

- **[S-000016]** The "unit asking" technique, which first asks for a contribution to one unit and then asks for the number of units, incr…  
  P = 0.93 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 26

- **[S-000017]** The likelihood of a potential donor avoiding a solicitor is moderated by the physical cost of avoidance.  
  P = 0.93 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 26

- **[S-000018]** Directly asking individuals to donate increases giving.  
  P = 0.93 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 26

- **[S-000005]** Direct solicitation moves individuals from latent prosocial intent to the action of donating.  
  P = 0.85 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 26

- **[S-000013]** Aversion to personal donation appeals is a contributing reason for non-donation.  
  P = 0.85 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 26

- **[S-000019]** The effectiveness of direct solicitation on giving is moderated by the stakeholder's perceived cost of avoiding the requ…  
  P = 0.85 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 26

- **[S-000020]** Repeated solicitations from the same source can decrease giving over time.  
  P = 0.85 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 26


### Intention
_N claims: 2 · Mean posterior: 0.90 · Grade A/B: 2_

- **[I-000004]** Intention is a necessary but insufficient predictor of behavior.  
  P = 0.90 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 5

- **[I-000006]** The strength of an intention moderates its likelihood of being translated into behavior.  
  P = 0.90 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 5


### Impure Altruism
_N claims: 2 · Mean posterior: 0.90 · Grade A/B: 2_

- **[IA-000001]** Charitable giving is better explained by an impure altruism model that combines concern for recipient welfare with warm …  
  P = 0.90 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 78

- **[IA-000002]** Charitable giving is better explained by an impure altruism model that combines concern for recipient welfare with warm …  
  P = 0.90 · A (strong)  
  EVIDs: 11 supporting, 0 contradicting, 0 mixed · N sources: 78


### Brand Image
_N claims: 28 · Mean posterior: 0.90 · Grade A/B: 28_

- **[BI-000005]** Positive nonprofit brand image is positively associated with potential donors' intention to donate.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000006]** A positive nonprofit brand image is a direct positive predictor of an individual's intention to donate money and time.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000023]** A positive university brand image is associated with higher student satisfaction.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000024]** A positive university brand image is associated with higher student loyalty.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000025]** A positive university brand image is associated with positive stakeholder behavioural intentions.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000047]** The conceptual basis for brand image has remained anchored in associative network models from the early 1990s, with limi…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000049]** Brand image is a critical marketing construct that influences key outcomes including brand trust, customer satisfaction,…  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000009]** Brand image is modeled as a direct predictor of charitable donation intention in some nonprofit donation studies.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000010]** Brand image functions as an evaluative heuristic that helps stakeholders form holistic impressions under incomplete info…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000012]** Brand image functions as an evaluative heuristic that stakeholders use to form holistic impressions of nonprofit organiz…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000018]** A nonprofit brand's perceived image is associated with resource provider support intentions.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000022]** A positive nonprofit brand image is positively associated with donation intention.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000027]** In the nonprofit sector, stakeholder perceptions of brand scale are positively associated with intentions to provide res…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000028]** In the nonprofit sector, stakeholder perceptions of brand character are not significantly associated with intentions to …  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000029]** Brand image is a multidimensional construct representing the overall mental perception of a brand held by consumers.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000030]** Brand image functions as an evaluative heuristic that helps stakeholders form support-related judgements under uncertain…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000031]** Heavy users possess a richer network of brand image associations than light users and non-users.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000032]** In high-intangibility and high-perceived-risk contexts, brand image increases choice propensity by reducing consumer unc…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000033]** Brand image represents a more complex cognitive structure than brand awareness because it consists of associations linke…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000040]** Nonprofit brand image consists of external stakeholder perceptions including awareness, trust, and support.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000041]** In co-created nonprofit brand equity models, brand image has a greater relative influence on brand equity for external s…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000042]** The influence of specific brand image dimensions on donation intentions is contingent on the specific nonprofit brand's …  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000050]** A clearly defined and communicated nonprofit brand image has a direct, positive influence on an individual's intention t…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000052]** Nonprofit brand image and trust influence donation intention primarily by shaping donor attitudes.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000054]** A nonprofit brand image characterized by high social standing and perceived popularity is positively associated with the…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000019]** Brand image can function as a heuristic that simplifies resource provider decision-making.  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000020]** Brand image shapes the evaluative content of donor attitudes toward a nonprofit organisation.  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197

- **[BI-000021]** Brand image shapes the social-symbolic content of subjective norms in donation decisions.  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 93 supporting, 6 contradicting, 10 mixed · N sources: 197


### Capital Conversion
_N claims: 1 · Mean posterior: 0.90 · Grade A/B: 1_

- **[CC-000009]** Monetary donation is a practice for converting economic capital into symbolic capital.  
  P = 0.90 · A (strong)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 33


### Mediation
_N claims: 1 · Mean posterior: 0.90 · Grade A/B: 1_

- **[M-000001]** Attitude mediates the relationship between brand equity and behavioral outcomes.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 1 contradicting, 6 mixed · N sources: 140


### Loyalty
_N claims: 3 · Mean posterior: 0.90 · Grade A/B: 3_

- **[L-000001]** Nonprofit brand equity research lacks sufficiently developed concepts of loyalty.  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 29 supporting, 1 contradicting, 3 mixed · N sources: 115

- **[L-000002]** Nonprofit brand equity research lacks sufficiently developed concepts of donor loyalty.  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 29 supporting, 1 contradicting, 3 mixed · N sources: 115

- **[L-000004]** The reviewed nonprofit brand equity literature lacks a sufficiently developed concept of loyalty.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 29 supporting, 1 contradicting, 3 mixed · N sources: 115


### Altruism
_N claims: 1 · Mean posterior: 0.89 · Grade A/B: 1_

- **[A-000007]** Pure altruism is insufficient to explain observed levels and patterns of charitable giving.  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 7 supporting, 0 contradicting, 3 mixed · N sources: 56


### Values
_N claims: 1 · Mean posterior: 0.89 · Grade A/B: 1_

- **[V-000001]** Alignment between a charity’s mission and a donor’s personal, moral, or political values supports charitable giving.  
  P = 0.89 · A (strong)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 8


### Moral Norms
_N claims: 6 · Mean posterior: 0.89 · Grade A/B: 6_

- **[MN-000002]** Adding moral norms to the Theory of Planned Behavior increases explained variance in charitable donation intention from …  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 1 contradicting, 3 mixed · N sources: 54

- **[MN-000004]** Moral norms positively predict charitable donation intention.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 1 contradicting, 3 mixed · N sources: 54

- **[MN-000005]** Adding moral norms increases the explanatory power of Theory of Planned Behavior models of charitable donation intention…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 1 contradicting, 3 mixed · N sources: 54

- **[MN-000006]** Moral norms are consistently strong predictors of charitable giving intentions.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 1 contradicting, 3 mixed · N sources: 54

- **[MN-000008]** The direct effect of moral norms on charitable giving intention is consistently stronger than the direct effect of socia…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 1 contradicting, 3 mixed · N sources: 54

- **[MN-000003]** Moral norms often predict charitable donation intention more strongly than subjective norms.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 1 contradicting, 3 mixed · N sources: 54


### Donation Intention
_N claims: 9 · Mean posterior: 0.89 · Grade A/B: 9_

- **[DI-000002]** An individual's intention to donate is positively predicted by attitude toward donating, perceived norms, and perceived …  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 150 supporting, 12 contradicting, 31 mixed · N sources: 227

- **[DI-000003]** The core Theory of Planned Behavior constructs explain approximately 44% of the variance in charitable donation intentio…  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 150 supporting, 12 contradicting, 31 mixed · N sources: 227

- **[DI-000004]** Charitable donation intention positively predicts actual charitable donation behavior.  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 150 supporting, 12 contradicting, 31 mixed · N sources: 227

- **[DI-000005]** Extended Theory of Planned Behavior models are a prevailing framework for explaining charitable donation intentions and …  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 150 supporting, 12 contradicting, 31 mixed · N sources: 227

- **[DI-000013]** The Theory of Planned Behavior, extended with moral norms, is a highly predictive cognitive framework for explaining var…  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 150 supporting, 12 contradicting, 31 mixed · N sources: 227

- **[DI-000014]** Attitude, subjective norm, and perceived behavioural control are significant positive predictors of charitable donation …  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 150 supporting, 12 contradicting, 31 mixed · N sources: 227

- **[DI-000015]** Adding moral norm and past behaviour to the standard Theory of Planned Behaviour model significantly increases the expla…  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 150 supporting, 12 contradicting, 31 mixed · N sources: 227

- **[DI-000016]** The effects of Perceived Behavioural Control and Moral Norm on charitable donation intention are more consistently signi…  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 150 supporting, 12 contradicting, 31 mixed · N sources: 227

- **[DI-000008]** Positive perceptions of nonprofit brand image are associated with stronger intentions to donate money to the nonprofit o…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 150 supporting, 12 contradicting, 31 mixed · N sources: 227


### Commitment
_N claims: 9 · Mean posterior: 0.89 · Grade A/B: 9_

- **[CO-000001]** Commitment reflects an enduring psychological desire to maintain a valued relationship with a nonprofit organization.  
  P = 0.89 · A (strong)  
  EVIDs: 37 supporting, 0 contradicting, 1 mixed · N sources: 182

- **[CO-000002]** Commitment transforms stakeholder support from a transactional exchange into a durable relational bond.  
  P = 0.89 · A (strong)  
  EVIDs: 37 supporting, 0 contradicting, 1 mixed · N sources: 182

- **[CO-000004]** Commitment reflects a stakeholder’s enduring psychological desire to maintain a valued relationship with a nonprofit org…  
  P = 0.89 · A (strong)  
  EVIDs: 37 supporting, 0 contradicting, 1 mixed · N sources: 182

- **[CO-000005]** Commitment directly increases donation intention.  
  P = 0.89 · A (strong)  
  EVIDs: 37 supporting, 0 contradicting, 1 mixed · N sources: 182

- **[CO-000007]** Donor commitment is positively associated with donation intention.  
  P = 0.89 · A (strong)  
  EVIDs: 37 supporting, 0 contradicting, 1 mixed · N sources: 182

- **[CO-000008]** Donor commitment is a proximal relational antecedent of long-term and recurring support.  
  P = 0.89 · A (strong)  
  EVIDs: 37 supporting, 0 contradicting, 1 mixed · N sources: 182

- **[CO-000009]** Commitment reflects a stakeholder’s enduring psychological desire to maintain a valued relationship with a nonprofit org…  
  P = 0.89 · A (strong)  
  EVIDs: 37 supporting, 0 contradicting, 1 mixed · N sources: 182

- **[CO-000010]** Perceived deviation of a nonprofit brand from the 'Good Samaritan' normative ideal is associated with decreased public c…  
  P = 0.89 · A (strong)  
  EVIDs: 37 supporting, 0 contradicting, 1 mixed · N sources: 182

- **[CO-000006]** Commitment influences moral norm through donor identity.  
  P = 0.87 · A (strong)  
  EVIDs: 37 supporting, 0 contradicting, 1 mixed · N sources: 182


### Behavioral Intention
_N claims: 3 · Mean posterior: 0.88 · Grade A/B: 3_

- **[BI-000004]** Overall brand equity has a direct positive effect on behavioral intention.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 14 supporting, 0 contradicting, 3 mixed · N sources: 48

- **[BI-000007]** Customer-Based Brand Equity has a positive influence on behavioral intention across multiple consumer-sector contexts.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 14 supporting, 0 contradicting, 3 mixed · N sources: 48

- **[BI-000008]** Brand equity can exert a direct positive effect on behavioral intention beyond its indirect effect through attitude.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 14 supporting, 0 contradicting, 3 mixed · N sources: 48


### Middle-Range Theory
_N claims: 1 · Mean posterior: 0.88 · Grade A/B: 1_

- **[MR-000001]** Middle-range theory provides the appropriate level of abstraction for building a testable and practically relevant model…  
  P = 0.88 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 15


### Behavioural Intention
_N claims: 4 · Mean posterior: 0.88 · Grade A/B: 4_

- **[BI-000001]** Overall brand equity has a direct positive effect on behavioural intention.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 18 supporting, 1 contradicting, 6 mixed · N sources: 73

- **[BI-000002]** Customer-based brand equity influences behavioural intention both directly and indirectly through IBM/TPB constructs.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 18 supporting, 1 contradicting, 6 mixed · N sources: 73

- **[BI-000011]** Nonprofit brand equity models commonly stop at intention or preference rather than actual observed behaviour.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 18 supporting, 1 contradicting, 6 mixed · N sources: 73

- **[BI-000013]** The reviewed nonprofit brand equity models do not provide an empirically tested path from brand perceptions to actual ob…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 18 supporting, 1 contradicting, 6 mixed · N sources: 73


### Perceived Efficacy
_N claims: 1 · Mean posterior: 0.88 · Grade A/B: 1_

- **[PE-000003]** Individuals give more to charitable organizations they perceive as having low overhead costs.  
  P = 0.88 · A (strong)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 30


### Knowledge Graph
_N claims: 1 · Mean posterior: 0.88 · Grade A/B: 1_

- **[KG-000001]** A knowledge graph, defined via a formal ontology, is an effective and powerful medium for operationalizing and represent…  
  P = 0.88 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 17


### Theory of Planned Behaviour
_N claims: 3 · Mean posterior: 0.88 · Grade A/B: 3_

- **[TO-000001]** The Theory of Planned Behaviour is an empirically credible framework for predicting charitable giving intentions.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 5 mixed · N sources: 51

- **[TO-000005]** Attitude, subjective norm, perceived behavioural control, and moral norms significantly predict donation intention.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 5 mixed · N sources: 51

- **[TO-000006]** Donation intention is predicted by attitudes, subjective norms, and perceived behavioural control.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 5 mixed · N sources: 51


### Psychological Benefits
_N claims: 2 · Mean posterior: 0.88 · Grade A/B: 2_

- **[PB-000016]** Internal psychological rewards from giving contribute to charitable donation behaviour.  
  P = 0.88 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 1

- **[PB-000035]** Framing a giving subsidy as a "match" is more effective at increasing donations than framing it as a "rebate".  
  P = 0.88 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 1


### Theory of Planned Behavior
_N claims: 7 · Mean posterior: 0.88 · Grade A/B: 7_

- **[TO-000002]** Brand-related factors influence the TPB antecedents of donation intention.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 34 supporting, 2 contradicting, 12 mixed · N sources: 126

- **[TO-000003]** Attitude, subjective norm, and perceived behavioral control positively predict charitable donation intention.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 34 supporting, 2 contradicting, 12 mixed · N sources: 126

- **[TO-000004]** Brand equity constructs function as antecedents to Theory of Planned Behavior components, especially attitude.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 34 supporting, 2 contradicting, 12 mixed · N sources: 126

- **[TO-000007]** An extended Theory of Planned Behavior model incorporating moral norms and past behavior explains significantly more var…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 34 supporting, 2 contradicting, 12 mixed · N sources: 126

- **[TO-000008]** The Theory of Planned Behavior's core constructs (attitude, subjective norm, perceived behavioral control) are strong pr…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 34 supporting, 2 contradicting, 12 mixed · N sources: 126

- **[TO-000009]** Extending the Theory of Planned Behavior to include moral norm and past behavior significantly increases its predictive …  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 34 supporting, 2 contradicting, 12 mixed · N sources: 126

- **[TO-000010]** Models like the Theory of Planned Behavior (TPB) and Theory of Reasoned Action (TRA) effectively explain intention forma…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 34 supporting, 2 contradicting, 12 mixed · N sources: 126


### Brand Attachment
_N claims: 11 · Mean posterior: 0.88 · Grade A/B: 11_

- **[BA-000030]** Brand Attachment and Brand Attitude Strength are empirically distinct psychological constructs.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 0 contradicting, 2 mixed · N sources: 7

- **[BA-000031]** Brand Attachment is constituted by the strength of the bond connecting a brand with the consumer’s self-concept.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 0 contradicting, 2 mixed · N sources: 7

- **[BA-000032]** Brand Attachment is indicated by Brand–Self Connection and Brand Prominence as two non-redundant components.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 0 contradicting, 2 mixed · N sources: 7

- **[BA-000033]** Brand Attachment predicts intentions to perform difficult brand-related behaviours more strongly than Brand Attitude Str…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 0 contradicting, 2 mixed · N sources: 7

- **[BA-000035]** Brand Attachment predicts actual consumer purchase behaviour more strongly than Brand Attitude Strength.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 0 contradicting, 2 mixed · N sources: 7

- **[BA-000036]** Brand Attachment predicts a brand’s purchase share against direct competitors more strongly than Brand Attitude Strength…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 0 contradicting, 2 mixed · N sources: 7

- **[BA-000037]** Brand Attachment predicts a brand’s need share against substitutable alternatives more strongly than Brand Attitude Stre…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 0 contradicting, 2 mixed · N sources: 7

- **[BA-000038]** Brand Attachment motivates consumers to invest financial, social, and temporal resources to maintain and protect the bra…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 0 contradicting, 2 mixed · N sources: 7

- **[BA-000040]** The Brand Attachment model in Park et al.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 0 contradicting, 2 mixed · N sources: 7

- **[BA-000039]** Brand Attachment involves hot affect linked to the self-concept, whereas Brand Attitude Strength involves colder evaluat…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 0 contradicting, 2 mixed · N sources: 7

- **[BA-000041]** Brand Attachment strengthens with relationship length more than Brand Attitude Strength does.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 24 supporting, 0 contradicting, 2 mixed · N sources: 7


### Symbolic Capital
_N claims: 5 · Mean posterior: 0.87 · Grade A/B: 5_

- **[SC-000020]** Corporate philanthropy is often a strategic mechanism for converting economic capital into symbolic capital (e.  
  P = 0.94 · A (strong)  
  EVIDs: 15 supporting, 0 contradicting, 0 mixed · N sources: 43

- **[SC-000025]** The primary behavioural function of a nonprofit brand is to serve as a store of symbolic capital, which facilitates the …  
  P = 0.87 · A (strong)  
  EVIDs: 15 supporting, 0 contradicting, 0 mixed · N sources: 43

- **[SC-000026]** The relative importance of a nonprofit's symbolic capital (brand) in driving stakeholder support, as compared to its rep…  
  P = 0.87 · A (strong)  
  EVIDs: 15 supporting, 0 contradicting, 0 mixed · N sources: 43

- **[SC-000018]** The conversion of a donor's economic capital into symbolic capital is moderated by the nonprofit's symbolic capital.  
  P = 0.84 · A (strong)  
  EVIDs: 15 supporting, 0 contradicting, 0 mixed · N sources: 43

- **[SC-000019]** In philanthropic fields characterized by high uncertainty, nonprofits with higher symbolic capital attract resources mor…  
  P = 0.84 · A (strong)  
  EVIDs: 15 supporting, 0 contradicting, 0 mixed · N sources: 43


### Customer-Based Brand Equity
_N claims: 6 · Mean posterior: 0.87 · Grade A/B: 6_

- **[CB-000002]** Integrating Customer-Based Brand Equity into the Theory of Planned Behavior explains more variance in behavioral intenti…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 21 supporting, 0 contradicting, 6 mixed · N sources: 125

- **[CB-000003]** Customer-Based Brand Equity functions as an antecedent structure within Theory of Planned Behavior models.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 21 supporting, 0 contradicting, 6 mixed · N sources: 125

- **[CB-000005]** Customer-based brand equity is defined as the differential effect of brand knowledge on consumer response to marketing a…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 21 supporting, 0 contradicting, 6 mixed · N sources: 125

- **[CB-000007]** Customer-based brand equity can be defined as a differential response to marketing efforts that manifests as a bias to b…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 21 supporting, 0 contradicting, 6 mixed · N sources: 125

- **[CB-000008]** Customer-based brand equity can be modelled as a cognitive process in which brand awareness and brand image increase pur…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 21 supporting, 0 contradicting, 6 mixed · N sources: 125

- **[CB-000016]** Customer-based brand equity resides in what customers have learned, felt, seen, and heard about a brand through their ex…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 21 supporting, 0 contradicting, 6 mixed · N sources: 125


### Psychological Framing
_N claims: 2 · Mean posterior: 0.87 · Grade A/B: 2_

- **[PF-000002]** Framing a price reduction for giving as a "matching grant" is more effective at increasing donations than framing it as …  
  P = 0.87 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 1

- **[PF-000003]** Asking for a contribution to a single "unit" before asking how many units a donor wishes to fund increases donations.  
  P = 0.87 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 1


### Planning
_N claims: 2 · Mean posterior: 0.87 · Grade A/B: 2_

- **[P-000001]** Action planning, the specification of 'when, where, and how' to act, is a mechanism for translating intention into behav…  
  P = 0.87 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[P-000002]** Coping planning, the anticipation of and preparation for barriers, is a mechanism for translating intention into behavio…  
  P = 0.87 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 3


### Price of Giving
_N claims: 1 · Mean posterior: 0.87 · Grade A/B: 1_

- **[PO-000002]** Lowering the material cost of giving (e.  
  P = 0.87 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 2


### Nonprofit Brand Image
_N claims: 12 · Mean posterior: 0.87 · Grade A/B: 12_

- **[NB-000012]** A positive nonprofit brand image increases a potential donor’s attitude toward donating to that organization.  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30

- **[NB-000015]** Social media marketing activities improve brand image, which subsequently increases brand trust and donation intention.  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30

- **[NB-000040]** Nonprofit brand image has a direct positive effect on an individual's giving intention.  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30

- **[NB-000044]** Nonprofit brand image does not have a significant effect on an individual donor's self-concept.  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30

- **[NB-000047]** A donor's self-concept does not mediate the relationship between nonprofit brand image and giving intention.  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30

- **[NB-000057]** Nonprofit brand image is empirically represented by six distinct first-order dimensions: Usefulness, Efficiency, Affect,…  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30

- **[NB-000060]** Conceptual models of nonprofit brand image that exclude Reliability and Ethicality have weaker explanatory power for don…  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30

- **[NB-000077]** The brand image of a nonprofit organization is a multidimensional construct composed of Usefulness, Efficiency, Affect, …  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30

- **[NB-000078]** A positive nonprofit brand image is a significant positive predictor of an individual's intention to donate money.  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30

- **[NB-000079]** A positive nonprofit brand image is a significant positive predictor of an individual's intention to donate time.  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30

- **[NB-000080]** The 'Efficiency' dimension of nonprofit brand image has a stronger positive effect on the intention to donate money than…  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30

- **[NB-000081]** The 'Affect' dimension of nonprofit brand image has a stronger positive effect on the intention to donate time than on t…  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 5 mixed · N sources: 30


### Internal Branding
_N claims: 3 · Mean posterior: 0.87 · Grade A/B: 3_

- **[IB-000024]** The implementation of internal branding strategies is positively associated with employee brand performance and intent t…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 1 contradicting, 1 mixed · N sources: 75

- **[IB-000021]** Internal branding activities embed the brand within organisational culture and foster brand-congruent employee behaviour…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 1 contradicting, 1 mixed · N sources: 75

- **[IB-000022]** The effect of an NPO's brand orientation behaviour on its organizational performance is fully mediated by the serial rel…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 1 contradicting, 1 mixed · N sources: 75


### Public Funding
_N claims: 1 · Mean posterior: 0.86 · Grade A/B: 1_

- **[PF-000001]** Service-providing nonprofits in Austria, particularly within the welfare sub-sector, are characterized by a high degree …  
  P = 0.86 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 4


### Efficacy
_N claims: 3 · Mean posterior: 0.86 · Grade A/B: 3_

- **[E-000001]** Donors are more likely to give when they perceive that their contribution will make a meaningful difference.  
  P = 0.90 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 5

- **[E-000008]** Donors give more to organizations that are perceived to have lower overhead costs.  
  P = 0.90 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 5

- **[E-000002]** Leadership gifts or seed money can increase subsequent donations by signalling the quality or efficacy of a charitable i…  
  P = 0.79 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 5


### Brand Awareness
_N claims: 35 · Mean posterior: 0.86 · Grade A/B: 35_

- **[BA-000002]** Nonprofit brand awareness, salience, or familiarity is positively associated with an individual's propensity to donate.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000005]** Brand awareness is a necessary but insufficient condition for stakeholder support.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000007]** Brand awareness is insufficient by itself to generate stakeholder support for nonprofit organizations.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000024]** Brand awareness is a necessary but insufficient condition for stakeholder support in nonprofit brand equity models.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000051]** Brand awareness is a foundational component of major customer-based brand equity models.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000071]** For volunteers who engage in an explicit search, higher brand awareness increases the probability of a nonprofit being i…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000003]** Brand awareness may be less salient for high-involvement products than for other consumer decision contexts.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000006]** Brand awareness can reduce support when the accessible brand associations are negative.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000008]** Brand awareness can reduce stakeholder support when the accessible brand knowledge associated with the organization is n…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000009]** Top-of-mind recall of a nonprofit brand is not a significant predictor of resource provider support intentions in Faircl…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000010]** Nonprofit brand awareness has heterogeneous effects on resource provider support intentions across awareness dimensions.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000014]** Brand awareness or familiarity alone is insufficient to generate positive nonprofit brand equity.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000015]** Brand familiarity can have a non-significant or negative effect on nonprofit brand equity when it is not accompanied by …  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000016]** Brand awareness is positively associated with donation intention.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000017]** In the nonprofit sector, top-of-mind brand recall is not significantly associated with intentions to provide resource su…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000018]** Brand awareness through recall and recognition increases the likelihood that a brand enters a consumer’s consideration s…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000019]** Brand categorization and brand awareness play a foundational role in consumer brand psychology.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000020]** Brand awareness is a customer-based dimension of brand equity.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000022]** Recognition is a more appropriate awareness measure for new or niche brands than for established brands.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000023]** Recall and top-of-mind awareness are more sensitive awareness measures for established brands than simple recognition.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000025]** Brand awareness can have detrimental effects on support when the accessible brand knowledge is predominantly unfavourabl…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000026]** Brand awareness alone is insufficient for NGO donor-based brand equity when it is not accompanied by positive familiarit…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000028]** Brand awareness functions as an initial prerequisite for brand consideration.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000052]** Top-of-mind awareness, unaided awareness, and aided awareness represent a hierarchy of brand-memory retrieval difficulty…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000053]** The relationship between aided, unaided, and top-of-mind brand awareness measures follows a logarithmic rather than a li…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000054]** A brand’s market share affects the relationship among aided, unaided, and top-of-mind awareness measures.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000055]** For high market-share brands, aided awareness is more stable over time than recall-based awareness measures.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000056]** For low market-share brands, recall-based awareness measures remain consistently low while aided awareness shows greater…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000063]** Brand awareness is one of the two primary sources of customer-based brand equity.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000066]** In co-created nonprofit brand equity models, brand awareness has a greater relative influence on brand equity for intern…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000068]** Donor-perceived brand awareness is positively associated with a charity brand's overall brand equity.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000077]** The relationship between brand awareness and brand equity is moderated by the valence of brand associations.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000079]** An increase in a nonprofit's brand awareness (cognitive accessibility) causes a positive increase in an individual's per…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000084]** Increased stakeholder awareness of a nonprofit brand enhances the perceived descriptive social norm of supporting that n…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177

- **[BA-000013]** Brand awareness or familiarity increases the cognitive accessibility of donor attitudes toward a nonprofit organisation.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 85 supporting, 8 contradicting, 14 mixed · N sources: 177


### University Brand
_N claims: 1 · Mean posterior: 0.86 · Grade A/B: 1_

- **[UB-000001]** Universities increasingly use brand management as a strategic response to global competition for students and staff.  
  P = 0.86 · A (strong)  
  EVIDs: 4 supporting, 0 contradicting, 1 mixed · N sources: 4


### Brand Knowledge
_N claims: 7 · Mean posterior: 0.86 · Grade A/B: 7_

- **[BK-000012]** Brand knowledge mediates the relationship between marketing activities and customer response.  
  P = 0.92 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 1 contradicting, 3 mixed · N sources: 82

- **[BK-000004]** Brand knowledge consists of brand awareness and brand image or associations in Keller's customer-based brand equity mode…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 1 contradicting, 3 mixed · N sources: 82

- **[BK-000005]** Brand knowledge can be conceptualized as an associative network in consumer memory.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 1 contradicting, 3 mixed · N sources: 82

- **[BK-000006]** Brand knowledge has a stronger influence on purchase propensity in subscription markets than in repertoire markets.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 1 contradicting, 3 mixed · N sources: 82

- **[BK-000007]** For brand non-users, brand knowledge has a weak or non-existent relationship with purchase propensity.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 1 contradicting, 3 mixed · N sources: 82

- **[BK-000008]** Brand knowledge alters customer responses to otherwise identical marketing activities.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 1 contradicting, 3 mixed · N sources: 82

- **[BK-000011]** Volunteer knowledge of a nonprofit brand is accumulated from national (Macro), local community (Micro), and personal (Me…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 1 contradicting, 3 mixed · N sources: 82


### Formal Ontology
_N claims: 1 · Mean posterior: 0.86 · Grade A/B: 1_

- **[FO-000001]** Formal ontology is a necessary and sufficient step to translate social science theory into a computationally tractable, …  
  P = 0.86 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 2


### Perceived Performance
_N claims: 1 · Mean posterior: 0.86 · Grade A/B: 1_

- **[PP-000004]** Perceived performance directly increases customer satisfaction in service encounters.  
  P = 0.86 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 7


### Brand Orientation
_N claims: 16 · Mean posterior: 0.86 · Grade A/B: 16_

- **[BO-000005]** An organization's internal brand orientation is a distinct and measurable construct that acts as an antecedent to market…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000006]** Brand Orientation is a strategic orientation where organizational processes are guided by the imperative to create, deve…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000007]** The adoption of a Brand Orientation strategy has a positive effect on a firm's financial performance.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000008]** Brand Orientation positively influences internal brand equity within business-to-business firms.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000009]** The successful implementation of a Brand Orientation strategy is negatively impacted by the presence of organizational s…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000010]** In the nonprofit sector, a higher degree of Brand Orientation is associated with superior organizational performance.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000012]** The interaction between Brand Orientation and Entrepreneurial Orientation on market performance is context-dependent.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000013]** Managerial vision and organizational culture are significant antecedents for the development of Brand Orientation.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000014]** A higher degree of nonprofit brand orientation is positively associated with measures of organizational performance.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000015]** A higher degree of nonprofit brand orientation is positively associated with fundraising success.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000001]** Nonprofit brand orientation can be conceptualised as a behavioural construct expressed through internal activities, stru…  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000002]** Successful branding requires internal firm-based characteristics that support brand-oriented behaviour.  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000003]** The adoption of a brand orientation mindset is a precondition for the long-term safeguarding of organisational brand equ…  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000004]** An NPO's internal brand orientation is a significant antecedent to the successful external implementation of its brand s…  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000011]** The direct effect of Brand Orientation on brand performance is non-significant in small firms.  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99

- **[BO-000016]** A nonprofit's strategic communication orientation moderates the long-term relationship between its brand activities and …  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 38 supporting, 4 contradicting, 4 mixed · N sources: 99


### Socio-Economic Resources
_N claims: 2 · Mean posterior: 0.86 · Grade A/B: 2_

- **[SE-000002]** Higher income is positively associated with both the likelihood of donating and the amount donated in Austria.  
  P = 0.86 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 21

- **[SE-000003]** Higher education is positively associated with both the likelihood of donating and the amount donated in Austria.  
  P = 0.86 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 21


### Sector Structure
_N claims: 1 · Mean posterior: 0.85 · Grade A/B: 1_

- **[SS-000004]** Social and health services form the economic core of the Austrian nonprofit sector in terms of value added, employment, …  
  P = 0.85 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 11


### Perceived Behavioural Control
_N claims: 6 · Mean posterior: 0.85 · Grade A/B: 6_

- **[PB-000033]** Perceived financial inability is a primary reason given by non-donors for not giving money to nonprofits.  
  P = 0.92 · A (strong)  
  EVIDs: 16 supporting, 0 contradicting, 1 mixed · N sources: 80

- **[PB-000001]** Brand awareness influences perceived behavioural control in integrated brand equity and IBM/TPB models.  
  P = 0.85 · A (strong)  
  EVIDs: 16 supporting, 0 contradicting, 1 mixed · N sources: 80

- **[PB-000002]** Brand trust influences perceived behavioural control in integrated brand equity and IBM/TPB models.  
  P = 0.85 · A (strong)  
  EVIDs: 16 supporting, 0 contradicting, 1 mixed · N sources: 80

- **[PB-000003]** Perceived brand quality influences perceived behavioural control in integrated brand equity and IBM/TPB models.  
  P = 0.85 · A (strong)  
  EVIDs: 16 supporting, 0 contradicting, 1 mixed · N sources: 80

- **[PB-000005]** Brand awareness, brand trust, and perceived quality influence perceived behavioural control.  
  P = 0.85 · A (strong)  
  EVIDs: 16 supporting, 0 contradicting, 1 mixed · N sources: 80

- **[PB-000004]** Brand-generated trust increases donors' perceived behavioural control by lowering informational burden and increasing co…  
  P = 0.81 · A (strong)  
  EVIDs: 16 supporting, 0 contradicting, 1 mixed · N sources: 80


### Perceived Quality
_N claims: 9 · Mean posterior: 0.85 · Grade A/B: 9_

- **[PQ-000001]** Perceived quality, effectiveness, transparency, and accountability are underdeveloped constructs in nonprofit brand equi…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 4 contradicting, 5 mixed · N sources: 111

- **[PQ-000002]** Nonprofit brand equity research has insufficiently developed perceived quality, effectiveness, transparency, and account…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 4 contradicting, 5 mixed · N sources: 111

- **[PQ-000010]** In nonprofit settings, higher stakeholder-perceived quality is a positive antecedent of perceived value.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 4 contradicting, 5 mixed · N sources: 111

- **[PQ-000003]** Perceived quality is a customer-based dimension of brand equity.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 4 contradicting, 5 mixed · N sources: 111

- **[PQ-000004]** Perceived quality, effectiveness, transparency, and accountability are underdeveloped constructs in the reviewed nonprof…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 4 contradicting, 5 mixed · N sources: 111

- **[PQ-000005]** Donors have difficulty assessing NGO service quality directly because they usually do not experience the services produc…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 4 contradicting, 5 mixed · N sources: 111

- **[PQ-000006]** Perceived quality is under-researched in nonprofit brand equity literature relative to awareness and associations.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 4 contradicting, 5 mixed · N sources: 111

- **[PQ-000007]** For juice, the effect of brand credibility on expected utility is mainly mediated by perceived quality.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 4 contradicting, 5 mixed · N sources: 111

- **[PQ-000009]** The direct positive relationship between donor-perceived service quality and a charity brand's overall brand equity is n…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 4 contradicting, 5 mixed · N sources: 111


### Prosocial Behaviour
_N claims: 1 · Mean posterior: 0.85 · Grade A/B: 1_

- **[PB-000023]** Marketing tools and concepts can be used to influence stakeholder behaviour toward individual and collective good.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 4 supporting, 0 contradicting, 2 mixed · N sources: 89


### Consumer-Based Brand Equity
_N claims: 14 · Mean posterior: 0.85 · Grade A/B: 14_

- **[CB-000020]** Consumer-Based Brand Equity is a higher-order construct composed of four distinct, correlated first-order dimensions: Br…  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000021]** Brand Awareness and Brand Associations are empirically distinct and separable dimensions of consumer-based brand equity.  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000022]** The psychological value of a brand to a consumer is a latent, multi-dimensional phenomenon that can be reliably measured…  
  P = 0.91 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000006]** Consumer-based brand equity develops through a sequential multi-stage process rather than functioning as a static monoli…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000009]** A consumer-based brand equity model comprising brand awareness, perceived quality, brand associations, and brand loyalty…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000010]** The factor loadings of a multidimensional consumer-based brand equity scale are equivalent between UK and Spanish consum…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000011]** A consumer-based brand equity scale validated in UK and Spanish samples has not been shown to be invariant in nonprofit,…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000012]** Consumer-based brand equity can be generated for offerings at any quality level when the brand credibly signals its actu…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000013]** Higher long-term advertising investment is positively associated with higher consumer-based brand equity among objective…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000014]** Brands with higher consumer-based brand equity generate greater consumer preference than functionally similar brands wit…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000015]** Brands with higher consumer-based brand equity generate stronger purchase intentions than functionally similar brands wi…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000017]** Aaker's (1991) four-dimensional model of consumer-based brand equity (awareness, associations, perceived quality, loyalt…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000018]** The lack of discriminant validity among the dimensions of Aaker's (1991) CBBE model is more severe for service and inter…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11

- **[CB-000019]** The universal applicability of a single, invariant structure for consumer-based brand equity is not supported across dif…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 0 contradicting, 2 mixed · N sources: 11


### Social Value
_N claims: 2 · Mean posterior: 0.85 · Grade A/B: 2_

- **[SV-000001]** Marketing functions extend beyond purely commercial goals to include the promotion of social value and the resolution of…  
  P = 0.85 · A (strong)  
  EVIDs: 4 supporting, 0 contradicting, 1 mixed · N sources: 12

- **[SV-000002]** Marketing policies and practices can be designed to enhance an organization's competitiveness while simultaneously advan…  
  P = 0.85 · A (strong)  
  EVIDs: 4 supporting, 0 contradicting, 1 mixed · N sources: 12


### Expectancy-Disconfirmation
_N claims: 1 · Mean posterior: 0.85 · Grade A/B: 1_

- **[ED-000001]** Satisfaction increases when perceived performance exceeds prior expectations and decreases when perceived performance fa…  
  P = 0.85 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 3


### Performance Measurement
_N claims: 1 · Mean posterior: 0.85 · Grade A/B: 1_

- **[PM-000002]** There is no consensus in the nonprofit marketing literature on a standardized set of performance metrics.  
  P = 0.85 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 1 mixed · N sources: 9


### Institutional Environment
_N claims: 1 · Mean posterior: 0.85 · Grade A/B: 1_

- **[IE-000002]** The Austrian nonprofit sector is defined by a corporatist welfare partnership with the state, creating deep structural i…  
  P = 0.85 · A (strong) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 3


### Past Behavior
_N claims: 3 · Mean posterior: 0.85 · Grade A/B: 3_

- **[PB-000028]** Past donation behavior is a direct predictor of future donation intention, with an effect size comparable to or exceedin…  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 11 supporting, 0 contradicting, 2 mixed · N sources: 54

- **[PB-000029]** Past donation behavior is a significant predictor of future donation intention and behavior.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 11 supporting, 0 contradicting, 2 mixed · N sources: 54

- **[PB-000010]** Past charitable donation behavior directly influences charitable donation intention and future charitable donation behav…  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 11 supporting, 0 contradicting, 2 mixed · N sources: 54


### Market Orientation
_N claims: 1 · Mean posterior: 0.85 · Grade A/B: 1_

- **[MO-000001]** The adoption of a market orientation by a nonprofit leads to improved organizational performance and resource attraction…  
  P = 0.85 · A (strong)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 32


### Brand Personality
_N claims: 20 · Mean posterior: 0.85 · Grade A/B: 20_

- **[BP-000002]** Nonprofit brand personality positively influences the likelihood that an organization receives contributions.  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000001]** Congruence between a donor's self-concept and a nonprofit's brand personality positively influences donation intention.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000003]** Brand personality functions as a cognitive shortcut in stakeholder support decisions.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000004]** Brand personality contributes to stakeholders’ evaluations of nonprofit brands by providing symbolic associations that i…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000005]** A nonprofit brand's perceived personality is associated with resource provider support intentions.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000006]** Nonprofit brand personality is positively associated with donation intention.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000007]** In the nonprofit sector, stakeholder perceptions of brand respect are positively associated with intentions to provide r…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000008]** In the nonprofit sector, stakeholder perceptions of brand differentiation are positively associated with intentions to p…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000010]** The distinction between brand personality and brand image remains conceptually ambiguous in the brand equity literature.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000011]** The factor structure of brand personality varies across cultural contexts.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000012]** Brand personality is more relevant as a brand equity measure when physical differentiation is low or social visibility i…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000013]** Brand personality contributes to stakeholder evaluations of nonprofit organisations by providing symbolic associations t…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000024]** The five-factor brand personality structure identified by Aaker (1997) for commercial brands does not replicate within t…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000025]** The brand personality of nonprofit organisations, in the German context, is best represented by a three-dimensional stru…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000026]** The primary and most encompassing dimension of nonprofit brand personality is 'Social Competence and Trust', which integ…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000027]** A stakeholder's perception of an NPO's 'Social Competence and Trust' is a significant positive predictor of their willin…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000028]** The perceived brand personality profiles of nonprofit organisations differ significantly from those of for-profit organi…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000029]** The alignment between a nonprofit's brand personality and a stakeholder's self-concept mediates the positive effect of b…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000030]** The behavioural effect of a nonprofit's brand personality is contingent on specific dimensions that signal competence, c…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174

- **[BP-000009]** Brand personality can operate as a relational heuristic when stakeholders perceive a brand as a relationship partner.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 59 supporting, 5 contradicting, 9 mixed · N sources: 174


### Brand Associations
_N claims: 9 · Mean posterior: 0.85 · Grade A/B: 9_

- **[BA-000083]** A brand can build equity by leveraging secondary associations, thereby transferring brand knowledge from another entity …  
  P = 0.88 · A (strong) ⚠ conflict  
  EVIDs: 44 supporting, 4 contradicting, 5 mixed · N sources: 126

- **[BA-000011]** In the tested NGO donor model, brand associations are empirically represented by perceived reputation, perceived differe…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 44 supporting, 4 contradicting, 5 mixed · N sources: 126

- **[BA-000021]** Brand associations are a customer-based dimension of brand equity.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 44 supporting, 4 contradicting, 5 mixed · N sources: 126

- **[BA-000027]** NGO brand associations should represent moral values and objectives rather than only brand personality traits.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 44 supporting, 4 contradicting, 5 mixed · N sources: 126

- **[BA-000029]** A three-factor model of brand associations comprising perceived value, brand personality, and organisational association…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 44 supporting, 4 contradicting, 5 mixed · N sources: 126

- **[BA-000042]** Higher advertising investment is associated with more favourable brand association structures among objectively similar …  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 44 supporting, 4 contradicting, 5 mixed · N sources: 126

- **[BA-000064]** Strong, favourable, and unique brand associations are one of the two primary sources of customer-based brand equity.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 44 supporting, 4 contradicting, 5 mixed · N sources: 126

- **[BA-000067]** The Brand Associations dimension of brand equity can be effectively measured by including items for brand personality an…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 44 supporting, 4 contradicting, 5 mixed · N sources: 126

- **[BA-000075]** Higher-order brand associations are stronger predictors of sustained donor support than lower-order factors like brand a…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 44 supporting, 4 contradicting, 5 mixed · N sources: 126


### Brand Salience
_N claims: 5 · Mean posterior: 0.84 · Grade A/B: 5_

- **[BS-000002]** The effect of nonprofit brand salience on donation choice is stronger among new donors than among established donors.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 1 contradicting, 0 mixed · N sources: 54

- **[BS-000003]** Brand-associated memory networks make a brand more salient and accessible during information processing.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 1 contradicting, 0 mixed · N sources: 54

- **[BS-000010]** In new donor acquisition for international aid charities, nonprofit brand salience positively predicts donor attitude to…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 1 contradicting, 0 mixed · N sources: 54

- **[BS-000011]** In new donor acquisition for international aid charities, nonprofit brand salience has a direct positive effect on brand…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 1 contradicting, 0 mixed · N sources: 54

- **[BS-000012]** For nonprofit brands in international aid, prominence contributes more strongly to salience for larger market-leading or…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 1 contradicting, 0 mixed · N sources: 54


### Perceived Market Orientation
_N claims: 2 · Mean posterior: 0.84 · Grade A/B: 2_

- **[PM-000003]** In the nonprofit sector, a member's positive perception of an organization's market orientation is positively and signif…  
  P = 0.84 · A (strong)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[PM-000004]** A member's perception of a nonprofit organization's market orientation is a direct and significant positive predictor of…  
  P = 0.84 · A (strong)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 3


### Reputation
_N claims: 11 · Mean posterior: 0.84 · Grade A/B: 11_

- **[R-000001]** Publicly observable donations increase giving relative to anonymous donation contexts.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 2 contradicting, 2 mixed · N sources: 143

- **[R-000003]** University reputation is a significant factor in attracting students and staff.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 2 contradicting, 2 mixed · N sources: 143

- **[R-000006]** Organizational reputation has both a direct positive effect on donation intention and an indirect positive effect mediat…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 2 contradicting, 2 mixed · N sources: 143

- **[R-000009]** The effect of "watching eyes" cues on increasing donations does not reliably replicate in larger online or field experim…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 2 contradicting, 2 mixed · N sources: 143

- **[R-000010]** Public recognition for donating does not reliably increase giving.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 2 contradicting, 2 mixed · N sources: 143

- **[R-000011]** The effect of donation observability on giving is moderated by cultural norms.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 2 contradicting, 2 mixed · N sources: 143

- **[R-000013]** Situational reputation cues such as "watching eyes" images do not reliably increase prosocial giving.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 2 contradicting, 2 mixed · N sources: 143

- **[R-000014]** Public recognition does not reliably increase prosocial giving.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 2 contradicting, 2 mixed · N sources: 143

- **[R-000002]** Reputational effects on giving are stronger when observers belong to the donor’s social network.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 2 contradicting, 2 mixed · N sources: 143

- **[R-000004]** Higher nonprofit brand orientation is positively associated with stronger nonprofit reputation among key stakeholders.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 2 contradicting, 2 mixed · N sources: 143

- **[R-000015]** The effect of public observability on giving is moderated by cultural norms.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 40 supporting, 2 contradicting, 2 mixed · N sources: 143


### Hierarchical Brand Equity
_N claims: 1 · Mean posterior: 0.84 · Grade A/B: 1_

- **[HB-000001]** Brand equity is widely modelled as a multi-level process in which foundational perceptions precede deeper relational out…  
  P = 0.84 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 18


### Context
_N claims: 1 · Mean posterior: 0.84 · Grade A/B: 1_

- **[C-000003]** Contextual factors, such as resource availability and time, can facilitate or inhibit the translation of intention into …  
  P = 0.84 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 3


### Tax Incentives
_N claims: 1 · Mean posterior: 0.84 · Grade A/B: 1_

- **[TI-000001]** The causal effect of Austrian tax deductibility rules on individual donation amounts and donation frequency is not estab…  
  P = 0.84 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 21


### Parental Modeling
_N claims: 1 · Mean posterior: 0.84 · Grade A/B: 1_

- **[PM-000001]** Parental modeling has a stronger effect on past blood donation compared to past volunteering of time or past financial d…  
  P = 0.84 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 2


### Branding
_N claims: 1 · Mean posterior: 0.83 · Grade A/B: 1_

- **[B-000001]** A strong nonprofit brand image is positively associated with stakeholder trust.  
  P = 0.83 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 9


### Charitable Giving
_N claims: 2 · Mean posterior: 0.83 · Grade A/B: 2_

- **[CG-000003]** Charitable giving is driven by multiple mechanisms rather than by a single motive.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 53 supporting, 7 contradicting, 8 mixed · N sources: 122

- **[CG-000006]** Charitable giving is driven by a mix of motives, including altruism, egoism (warm glow), values, trust, and social conte…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 53 supporting, 7 contradicting, 8 mixed · N sources: 122


### Internal Brand Management
_N claims: 3 · Mean posterior: 0.83 · Grade A/B: 3_

- **[IB-000017]** Perceived internal brand management practices in nonprofit organizations are positively correlated with volunteer role c…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 6 supporting, 0 contradicting, 2 mixed · N sources: 5

- **[IB-000018]** Perceived internal brand management practices in nonprofit organizations are positively correlated with volunteer brand …  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 6 supporting, 0 contradicting, 2 mixed · N sources: 5

- **[IB-000023]** Perceived management support and positive relational factors ("The H Factor") are key dimensions of internal brand manag…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 6 supporting, 0 contradicting, 2 mixed · N sources: 5


### Satisfaction
_N claims: 8 · Mean posterior: 0.83 · Grade A/B: 8_

- **[S-000010]** Customer satisfaction positively influences behavioural intentions such as repurchase and positive word-of-mouth.  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 0 mixed · N sources: 77

- **[S-000011]** Stakeholder satisfaction with a nonprofit is a positive predictor of repeat support behaviours.  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 0 mixed · N sources: 77

- **[S-000012]** Stakeholder satisfaction with a nonprofit is a positive predictor of positive word-of-mouth.  
  P = 0.89 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 0 mixed · N sources: 77

- **[S-000001]** Customer satisfaction partially mediates the relationship between brand equity and behavioural outcomes.  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 0 mixed · N sources: 77

- **[S-000002]** Customer satisfaction partially mediates the relationship between brand equity and behavioral outcomes such as repurchas…  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 0 mixed · N sources: 77

- **[S-000003]** Satisfaction partially mediates the relationship between brand equity and post-purchase or repeat behavioral outcomes.  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 0 mixed · N sources: 77

- **[S-000008]** Satisfaction is a driver of loyalty, particularly in service contexts.  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 0 mixed · N sources: 77

- **[S-000009]** The direct influence of satisfaction on behavioural intentions is stronger for individuals with high brand familiarity t…  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 0 mixed · N sources: 77


### Likelihood Paradigm
_N claims: 1 · Mean posterior: 0.83 · Grade A/B: 1_

- **[LP-000001]** The conceptual separation of evidence strength (Likelihood), degree of belief (Posterior), and recommended action (Decis…  
  P = 0.83 · A (strong) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Nonprofit Brand Equity
_N claims: 40 · Mean posterior: 0.83 · Grade A/B: 40_

- **[NB-000011]** Nonprofit brand equity positively predicts charitable donation intention.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000019]** Core brand equity concepts are adaptable from commercial branding to nonprofit, social, and employer-branding contexts.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000021]** Nonprofit brand equity resides in stakeholders' minds rather than in the organization as a financial asset.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000024]** Existing nonprofit brand equity models do not provide an empirically tested path from brand perceptions to actual observ…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000025]** Nonprofit brand equity resides in stakeholders' minds rather than as a direct financial asset of the nonprofit organizat…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000037]** Higher nonprofit customer-based brand equity is positively associated with donors' intention to donate.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000038]** Nonprofit brand equity is a multidimensional construct that includes brand awareness or familiarity and positive brand a…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000048]** Nonprofit brand equity is conceptualised in the reviewed models as a stakeholder-based mental asset rather than as a fin…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000101]** Causal claims about the effect of nonprofit brand equity on stakeholder support that are based solely on cross-sectional…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000102]** Brand equity models imported from commercial contexts are misspecified for the nonprofit sector when they omit essential…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000103]** A single measurement model for nonprofit brand equity is not invariant across key stakeholder groups such as donors, vol…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000106]** Higher levels of stakeholder-based brand equity are positively associated with supportive behavioral intentions.  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000003]** The evaluative content of nonprofit brand equity differs from commercial brand equity by emphasizing mission fit, moral …  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000020]** The reviewed brand equity literature focuses primarily on commercial contexts rather than nonprofit contexts.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000022]** Nonprofit brand equity is conceptually ambiguous when it is operationalised as behavioural intention.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000023]** A stakeholder-based model can define nonprofit brand equity as a relational asset composed of awareness, trust, and comm…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000026]** Brand-related antecedents explain variance in nonprofit resource provider support intentions after controlling for indiv…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000027]** For-profit brand equity concepts can be empirically applied to nonprofit resource provider support intentions.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000028]** Stakeholder-based nonprofit brand equity is a multidimensional construct composed of nonprofit brand awareness, nonprofi…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000032]** High nonprofit brand equity can function as a trust and quality seal for stakeholders evaluating nonprofit organizations…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000033]** Direct transfer of for-profit brand equity models to nonprofit organizations is insufficient because such models do not …  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000049]** Faircloth’s model defines nonprofit brand equity as a favourable bias toward support that blends brand equity with prefe…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000050]** Boenigk and Becker’s model defines nonprofit brand equity as a relational asset composed of awareness, trust, and commit…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000051]** Boenigk and Becker’s model does not empirically test the relationship between nonprofit brand equity and actual support …  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000052]** Rios Romero et al.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000062]** Strong brands are strategically important for nonprofit organizations.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000068]** A nonprofit brand’s value is tied to the level of trust it commands among stakeholders.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000069]** The perceived structure of nonprofit brand equity, defined by brand awareness and brand image, can be functionally simil…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000070]** Standard B2B brand equity measurement models may require modification to achieve construct validity in a nonprofit conte…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000096]** A stakeholder-based brand equity model incorporating context-specific dimensions like Brand Trust provides a more valid …  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000097]** From the perspective of the general public, nonprofit brand equity is a multidimensional construct comprising Brand Awar…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000098]** The dimensions of nonprofit brand equity are formed sequentially, with Brand Awareness acting as a necessary preconditio…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000105]** The relative importance and structure of brand equity dimensions are contingent on cultural context.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000002]** Nonprofit brand equity can be conceptualized as both an individual-level psychological state and an organization-level a…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000007]** Integrating nonprofit brand equity constructs into the Theory of Planned Behavior increases explanatory power for stakeh…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000008]** Nonprofit brand equity dimensions are antecedents of stakeholder attitude toward supportive behavior.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000009]** Attitude mediates the relationship between nonprofit brand equity and stakeholder behavioral intention.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000010]** Nonprofit brand equity has a direct positive influence on stakeholder behavioral intention independent of attitude.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000099]** The relational component of nonprofit brand equity can be modeled as a second-order formative construct created by Brand…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243

- **[NB-000104]** The relationship between a nonprofit's brand equity and stakeholders' supportive behaviours is negatively moderated by p…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 69 supporting, 8 contradicting, 11 mixed · N sources: 243


### Brand Commitment
_N claims: 8 · Mean posterior: 0.83 · Grade A/B: 8_

- **[BC-000001]** Attitudinal and emotional commitment are positive predictors of sustained nonprofit support behaviours.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 3 mixed · N sources: 10

- **[BC-000010]** Donor brand commitment toward an NGO is composed of attitudinal and emotional dimensions in the tested measurement model…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 3 mixed · N sources: 10

- **[BC-000014]** Volunteer brand commitment is more strongly correlated with relational internal brand management dimensions than with in…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 3 mixed · N sources: 10

- **[BC-000015]** Volunteer brand commitment positively predicts brand citizenship behaviour among formal nonprofit volunteers.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 3 mixed · N sources: 10

- **[BC-000016]** Volunteer brand commitment positively predicts volunteer satisfaction among formal nonprofit volunteers.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 3 mixed · N sources: 10

- **[BC-000017]** Volunteer brand commitment positively predicts intention to stay among formal nonprofit volunteers.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 3 mixed · N sources: 10

- **[BC-000018]** Volunteer brand commitment positively predicts positive word-of-mouth about the nonprofit organization.  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 3 mixed · N sources: 10

- **[BC-000041]** A volunteer's Brand Commitment is more strongly correlated with their positive word-of-mouth behaviour than their Role C…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 3 mixed · N sources: 10


### Perceived Behavioral Control
_N claims: 7 · Mean posterior: 0.83 · Grade A/B: 7_

- **[PB-000009]** Perceived behavioral control is frequently the strongest predictor of charitable donation intention among the core Theor…  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 7 mixed · N sources: 75

- **[PB-000011]** Perceived Behavioral Control positively predicts charitable donation intention.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 7 mixed · N sources: 75

- **[PB-000012]** Perceived Behavioral Control positively predicts charitable donation behavior.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 7 mixed · N sources: 75

- **[PB-000013]** Perceived behavioral control is a consistently strong predictor of charitable giving intentions.  
  P = 0.86 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 7 mixed · N sources: 75

- **[PB-000014]** Brand trust, reputation, and perceived quality reduce perceived risk and uncertainty.  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 7 mixed · N sources: 75

- **[PB-000015]** Brand trust, reputation, and perceived quality enhance perceived behavioral control and self-efficacy.  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 7 mixed · N sources: 75

- **[PB-000030]** The predictive power of Perceived Behavioral Control (PBC) on donation intention is heightened for behaviors that involv…  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 7 mixed · N sources: 75


### Social Inequality
_N claims: 1 · Mean posterior: 0.83 · Grade A/B: 1_

- **[SI-000010]** Volunteering practices reproduce existing social inequalities by favouring individuals with higher cultural and social c…  
  P = 0.83 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 7


### Brand Trust
_N claims: 34 · Mean posterior: 0.83 · Grade A/B: 34_

- **[BT-000001]** Nonprofit brand trust is a positive predictor of donation intention.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000002]** Brand trust mediates the relationship between nonprofit brand-building activities and donation intention.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000005]** Trust is often used as a proxy for perceived quality, effectiveness, transparency, and accountability in nonprofit brand…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000014]** University brand trust is positively linked to desirable stakeholder outcomes including satisfaction, loyalty, and posit…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000017]** Brand trust is a prerequisite for building donor relationships in nonprofit contexts.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000027]** An increase in a donor's perception of a nonprofit brand's integrity leads to a positive increase in their trust in that…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000028]** An increase in a donor's perception of a nonprofit's financial and operational transparency is positively associated wit…  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000030]** Donor trust in a nonprofit brand is a positive predictor of donation intention.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000036]** Trust in a nonprofit organization is a critical antecedent to a stakeholder's giving intention.  
  P = 0.90 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000003]** Brand trust reduces perceived donation risk when nonprofit performance and resource use are difficult for stakeholders t…  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000004]** Brand trust signals integrity, competence, and ethical conduct in nonprofit contexts.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000006]** Brand trust reduces perceived donation risk by signalling nonprofit integrity, competence, and ethical conduct under con…  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000007]** Brand trust is a central independent dimension of nonprofit brand equity in Boenigk and Becker’s stakeholder-based model…  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000008]** High consumer-brand trust is contingent upon a configuration of pre-existing brand reputation and strong brand associati…  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000009]** Brand trust increases donors' willingness to give by increasing confidence that donations will be used effectively and e…  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000010]** Trust is more central to nonprofit brand equity than perceived quality is in standard commercial brand-equity models.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000011]** Brand trust is positively associated with donation intention.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000012]** Brand trust reduces perceived donor risk in charitable giving.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000013]** Brand trust mediates the effects of other nonprofit brand signals on donation intention.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000015]** Brand trust reduces perceived donation risk by signalling organisational integrity, competence, and ethical conduct unde…  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000016]** Boenigk and Becker’s nonprofit brand equity model treats trust as an independent dimension of nonprofit brand equity.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000018]** Consistent and reliable delivery of a brand promise increases brand trust and contributes to brand equity.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000021]** Brand trust is a bi-dimensional construct comprising a reliability dimension and an intentions dimension.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000022]** Overall satisfaction with a brand is a positive antecedent of brand trust.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000023]** Brand trust is a partial mediator of the relationship between overall satisfaction and brand loyalty.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000025]** For nonprofit brands, Brand Trust is a distinct and more powerful explanatory dimension for stakeholder-brand relationsh…  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000026]** The primary function of Brand Trust within the nonprofit brand equity framework is to reduce stakeholder perceived risk …  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000029]** Donor trust in a nonprofit brand is a positive predictor of attitudinal commitment to the organization.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000031]** The positive effect of brand heritage on donation intention is mediated by brand trust.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000032]** The positive effect of brand anthropomorphism on donation intention is mediated by brand trust.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000033]** Brand trust positively influences stakeholder commitment and supportive intentions, particularly in contexts of high unc…  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000034]** Brand trust mediates the relationship between other brand perceptions, such as brand anthropomorphism, and supportive in…  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000037]** Brand trust mediates the effect of brand perceptions, such as brand heritage, on relational outcomes like commitment and…  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24

- **[BT-000035]** The perceived trustworthiness of a nonprofit brand positively influences donation intention by increasing positive Attit…  
  P = 0.76 · A (strong) ⚠ conflict  
  EVIDs: 20 supporting, 0 contradicting, 5 mixed · N sources: 24


### Normative Alignment
_N claims: 1 · Mean posterior: 0.82 · Grade A/B: 1_

- **[NA-000001]** The relationship between charitable donation intention and donation behavior is stronger when injunctive and descriptive…  
  P = 0.82 · A (strong) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 20


### NPO Success
_N claims: 2 · Mean posterior: 0.82 · Grade A/B: 2_

- **[NS-000002]** The presence of a written long-term financial plan is an indicator of NPO success.  
  P = 0.82 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 4

- **[NS-000003]** Engaging in systematic fundraising activities is an indicator of NPO success.  
  P = 0.82 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 4


### Cause Choice
_N claims: 1 · Mean posterior: 0.82 · Grade A/B: 1_

- **[CC-000005]** Experimental evidence on how framing, appeals, and context shift Austrian donors between competing causes is insufficien…  
  P = 0.82 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 21


### Brand Equity Dimensions
_N claims: 1 · Mean posterior: 0.82 · Grade A/B: 1_

- **[BE-000014]** Awareness, associations or image, perceived quality, and loyalty are recurrent dimensions of brand equity across commerc…  
  P = 0.82 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 30


### Nonprofit Brand Management
_N claims: 1 · Mean posterior: 0.82 · Grade A/B: 1_

- **[NB-000067]** Nonprofit branding serves strategic purposes beyond fundraising.  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 0 contradicting, 2 mixed · N sources: 10


### Digital Branding
_N claims: 1 · Mean posterior: 0.82 · Grade A/B: 1_

- **[DB-000008]** The behavioural effects of university digital marketing and online brand presence are not sufficiently established in th…  
  P = 0.82 · A (strong)  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 77


### Brand Usage
_N claims: 1 · Mean posterior: 0.82 · Grade A/B: 1_

- **[BU-000002]** Higher brand usage is associated with stronger brand perceptions and beliefs.  
  P = 0.82 · A (strong) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 14


### Integrated Behavioral Model
_N claims: 5 · Mean posterior: 0.82 · Grade A/B: 5_

- **[IB-000027]** The Integrated Behavioral Model (IBM), particularly its concepts of environmental constraints and skills, is empirically…  
  P = 0.86 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 1 mixed · N sources: 45

- **[IB-000002]** The Integrated Behavioral Model explains intention-to-behaviour conversion by incorporating enactment factors such as sk…  
  P = 0.84 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 1 mixed · N sources: 45

- **[IB-000008]** The reviewed charitable donation literature does not explicitly adopt Integrated Behavioral Model terminology.  
  P = 0.84 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 1 mixed · N sources: 45

- **[IB-000010]** A formal model explicitly integrating comprehensive brand equity with the full Integrated Behavioral Model is not establ…  
  P = 0.84 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 1 mixed · N sources: 45

- **[IB-000009]** Reviewed extended TPB donation models incorporate constructs that overlap with Integrated Behavioral Model components, i…  
  P = 0.72 · B (moderate)  
  EVIDs: 6 supporting, 0 contradicting, 1 mixed · N sources: 45


### Relationship Quality
_N claims: 1 · Mean posterior: 0.82 · Grade A/B: 1_

- **[RQ-000001]** The perceived quality of the relationship between a stakeholder and a nonprofit directly predicts loyalty and positive w…  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 3 supporting, 1 contradicting, 0 mixed · N sources: 69


### Collaboration
_N claims: 1 · Mean posterior: 0.82 · Grade A/B: 1_

- **[C-000001]** Inter-organizational collaboration allows nonprofits to pool resources and leverage partner capabilities, thereby extend…  
  P = 0.82 · A (strong) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 7


### Automaticity
_N claims: 1 · Mean posterior: 0.82 · Grade A/B: 1_

- **[A-000015]** Situational cues can trigger automatic processes that bypass or override deliberate intentions.  
  P = 0.82 · A (strong) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Motivation
_N claims: 1 · Mean posterior: 0.82 · Grade A/B: 1_

- **[M-000004]** Charitable giving is driven by a combination of motives, and cannot be sufficiently explained by pure, selfless altruism…  
  P = 0.82 · A (strong)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 1


### Replication
_N claims: 3 · Mean posterior: 0.82 · Grade A/B: 3_

- **[R-000007]** Formal replication studies constitute less than 1% of publications in philanthropy research.  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 1 supporting, 0 contradicting, 2 mixed · N sources: 24

- **[R-000008]** Approximately 60% of existing replication studies in philanthropy research confirm the conclusions of the original studi…  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 1 supporting, 0 contradicting, 2 mixed · N sources: 24

- **[R-000012]** Approximately 60% of replications in charitable giving research support the conclusions of the preceding original studie…  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 1 supporting, 0 contradicting, 2 mixed · N sources: 24


### Nonprofit Brand Trust
_N claims: 4 · Mean posterior: 0.81 · Grade A/B: 4_

- **[NB-000013]** Brand trust positively predicts charitable donation intention.  
  P = 0.81 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 28

- **[NB-000014]** Brand trust mediates the relationship between nonprofit brand perceptions and donation intention.  
  P = 0.81 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 28

- **[NB-000029]** Nonprofit brand trust is a more sector-specific dimension of nonprofit brand equity than general brand image or brand pe…  
  P = 0.81 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 28

- **[NB-000031]** Nonprofit brand trust reduces stakeholder-perceived risk by signalling that a nonprofit will act ethically, use funds ap…  
  P = 0.81 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 28


### Intention-Behavior Gap
_N claims: 11 · Mean posterior: 0.81 · Grade A/B: 11_

- **[IB-000004]** A measurable discrepancy exists between individuals' stated intentions to donate to charity and their subsequent donatio…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 5 contradicting, 8 mixed · N sources: 120

- **[IB-000005]** Theory of Planned Behavior models explain less variance in actual charitable giving behavior than in charitable giving i…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 5 contradicting, 8 mixed · N sources: 120

- **[IB-000006]** The Theory of Planned Behavior explains substantially less variance in actual charitable donation behavior than in chari…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 5 contradicting, 8 mixed · N sources: 120

- **[IB-000007]** Positive charitable donation intentions do not consistently translate into actual charitable donation behavior.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 5 contradicting, 8 mixed · N sources: 120

- **[IB-000025]** Intention-based models explain a systematically and substantially lower proportion of variance in actual donation behavi…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 5 contradicting, 8 mixed · N sources: 120

- **[IB-000026]** A significant gap exists between individuals' stated intention to donate and their actual donation behavior.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 5 contradicting, 8 mixed · N sources: 120

- **[IB-000031]** A significant and persistent gap exists between behavioral intentions and subsequent actions.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 5 contradicting, 8 mixed · N sources: 120

- **[IB-000033]** A substantial discrepancy exists between stated behavioral intentions and subsequent actions across diverse domains.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 5 contradicting, 8 mixed · N sources: 120

- **[IB-000034]** The intention-behavior gap is primarily driven by 'inclined abstainers'—individuals who form an intention but fail to en…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 5 contradicting, 8 mixed · N sources: 120

- **[IB-000035]** No single, universally accepted model adequately explains the intention-behavior gap across all behavioral domains.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 5 contradicting, 8 mixed · N sources: 120

- **[IB-000030]** The intention-behavior gap is a dynamic, within-person process that is inadequately explained by static, between-person …  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 5 contradicting, 8 mixed · N sources: 120


### Pro-social Behaviour
_N claims: 2 · Mean posterior: 0.81 · Grade A/B: 2_

- **[PS-000001]** Pro-social behaviours such as donating are better explained as socially embedded practices than as outcomes of isolated,…  
  P = 0.81 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 26

- **[PS-000002]** Pro-social practices, including charitable giving and volunteering, are stratified by socioeconomic status and tend to r…  
  P = 0.81 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 26


### Publication Bias
_N claims: 1 · Mean posterior: 0.81 · Grade A/B: 1_

- **[PB-000034]** There is a significant bias in philanthropy research towards incorrectly reporting non-significant findings as significa…  
  P = 0.81 · A (strong) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 1


### Nonprofit Brand Orientation
_N claims: 11 · Mean posterior: 0.81 · Grade A/B: 11_

- **[NB-000071]** Nonprofit Brand Orientation (NBO) is a higher-order construct that can be reliably and validly measured as three distinc…  
  P = 0.85 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[NB-000072]** Nonprofit Brand Orientation is an empirically distinguishable construct from Market Orientation.  
  P = 0.85 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[NB-000073]** A higher level of Nonprofit Brand Orientation is positively associated with higher self-reported overall organisational …  
  P = 0.85 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[NB-000074]** The Interaction and Orchestration dimensions of NBO are positively associated with a nonprofit's perceived ability to pr…  
  P = 0.85 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[NB-000075]** The Interaction, Orchestration, and Affect dimensions of NBO are all positively associated with a nonprofit's perceived …  
  P = 0.85 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[NB-000076]** For-profit brand management principles can be adapted into a valid and parsimonious measurement model for the nonprofit …  
  P = 0.85 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[NB-000055]** Nonprofit brand orientation is a strategic organisational orientation proposed to improve nonprofit performance under co…  
  P = 0.82 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[NB-000056]** Nonprofit brand orientation consists of orchestration and interaction as distinct organisational dimensions.  
  P = 0.82 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[NB-000085]** A nonprofit's brand orientation is strongly and positively correlated with stakeholder perceptions of its organizational…  
  P = 0.82 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[NB-000086]** Nonprofit Brand Orientation mediates the relationship between stakeholder attitudes toward marketing and perceived organ…  
  P = 0.69 · B (moderate)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[NB-000087]** The implementation of a nonprofit brand orientation is inhibited by organizational cultures characterized by high employ…  
  P = 0.69 · B (moderate)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 3


### Scientific Self-Correction
_N claims: 2 · Mean posterior: 0.81 · Grade A/B: 2_

- **[SS-000008]** Retractions of published studies in philanthropy research are rare.  
  P = 0.81 · A (strong)  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 1

- **[SS-000009]** Statistical reporting errors are more common in philanthropy research than in adjacent fields such as psychology.  
  P = 0.81 · A (strong)  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 1


### Crowding Out
_N claims: 1 · Mean posterior: 0.81 · Grade A/B: 1_

- **[CO-000003]** The effect of government funding on private charitable donations is empirically indeterminate across studies.  
  P = 0.81 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 1


### Mechanism Interaction
_N claims: 1 · Mean posterior: 0.81 · Grade A/B: 1_

- **[MI-000002]** The interactions among the major mechanisms of charitable giving are insufficiently understood in the existing literatur…  
  P = 0.81 · A (strong) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 1


### Added Value
_N claims: 1 · Mean posterior: 0.81 · Grade A/B: 1_

- **[AV-000001]** Accounting and marketing use the term added value to refer to different phenomena.  
  P = 0.81 · A (strong) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Attitude Toward Donating
_N claims: 2 · Mean posterior: 0.81 · Grade A/B: 2_

- **[AT-000003]** Attitude toward donating positively predicts charitable donation intention in extended Theory of Planned Behavior models…  
  P = 0.88 · A (strong)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 27

- **[AT-000002]** Attitude toward donating mediates the relationship between brand-related perceptions and donation intention.  
  P = 0.73 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 27


### Structural Equation Modeling
_N claims: 1 · Mean posterior: 0.81 · Grade A/B: 1_

- **[SE-000001]** Structural Equation Modeling is the standard methodological approach used to test integrated Customer-Based Brand Equity…  
  P = 0.81 · A (strong)  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 35


### Brand Identity
_N claims: 5 · Mean posterior: 0.81 · Grade A/B: 5_

- **[BI-000036]** A brand cannot become a strategic organisational asset unless its identity, purpose, and values are explicitly defined.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 0 contradicting, 2 mixed · N sources: 41

- **[BI-000037]** A clearly defined internal brand identity fosters organisational cohesion among nonprofit staff and volunteers.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 0 contradicting, 2 mixed · N sources: 41

- **[BI-000038]** Internal brand identity alone is insufficient to produce a strong external nonprofit brand image.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 0 contradicting, 2 mixed · N sources: 41

- **[BI-000039]** Nonprofit brand identity consists of internal elements including vision, values, culture, and leadership.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 0 contradicting, 2 mixed · N sources: 41

- **[BI-000043]** Brand Identity positively predicts Brand Meaning in the context of a nonprofit health-promotion brand.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 0 contradicting, 2 mixed · N sources: 41


### Brand Attitude Strength
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[BA-000034]** Brand Attitude Strength predicts easy-to-perform brand-related behaviours as effectively as Brand Attachment.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 8 supporting, 0 contradicting, 2 mixed · N sources: 1


### Digital Fundraising
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[DF-000003]** The effectiveness of digital platforms, crowdfunding, and AI-driven appeals in Austrian charitable giving is not establi…  
  P = 0.80 · A (strong)  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 74


### Negative Brand Perceptions
_N claims: 2 · Mean posterior: 0.80 · Grade A/B: 2_

- **[NB-000006]** The effects of negative or ambivalent brand perceptions on integrated brand-equity and behavioural models are not suffic…  
  P = 0.80 · A (strong)  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 66

- **[NB-000017]** The effect of negative or ambivalent nonprofit brand perceptions on TPB pathways to donation intention is not sufficient…  
  P = 0.80 · A (strong)  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 66


### Brand-Cause Fit
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[BC-000039]** The success of Cause-Related Marketing campaigns is moderated by the perceived fit between the sponsoring brand and the …  
  P = 0.80 · A (strong) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 9


### Aaker Brand Equity Model
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[AB-000001]** Aaker’s consumer-based brand equity model is the most common theoretical starting point for nonprofit brand equity resea…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Bayesian Evidence Synthesis
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[BE-000079]** Bayesian evidence synthesis provides a more rigorous, transparent, and epistemologically sound method for accumulating k…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Awareness; Brand Image; Donation Intention
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[BA-000078]** A nonprofit's brand image and brand awareness are positively associated with a potential donor's intention to donate.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Fragmentation
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[BE-000017]** No single universally accepted definition or measurement model of brand equity exists in the reviewed literature.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Model Adaptation
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[BE-000043]** For-profit brand equity models cannot be directly applied to nonprofit contexts without substantial adaptation.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Model Architecture
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[BE-000008]** Network and process-oriented brand equity models provide greater explanatory adequacy for consumer behaviour than static…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Paradigms
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[BE-000018]** Brand equity literature is divided between financial approaches that value brands as assets and customer-based approache…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Scale
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[BE-000051]** A 10-item scale composed of three loyalty items, two perceived quality items, and five awareness/associations items demo…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity–TPB Integration
_N claims: 2 · Mean posterior: 0.80 · Grade A/B: 2_

- **[BE-000010]** Models integrating brand equity constructs with Theory of Planned Behavior constructs explain donation intention more co…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BE-000011]** The reviewed literature does not use a single standardized structural model for integrating brand equity constructs with…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Image Measurement
_N claims: 4 · Mean posterior: 0.80 · Grade A/B: 4_

- **[BI-000044]** The scientific measurement of brand image is characterized by high methodological fragmentation, with the majority of st…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BI-000045]** The dominant paradigm for brand image measurement between 1991-2016 involved a two-stage process combining qualitative a…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BI-000046]** Academic brand image measurement has shown significant latency in adopting new data sources, relying almost exclusively …  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BI-000048]** The selection of an appropriate brand image measurement technique is contingent upon specific research goals and context…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Measurement
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[BM-000006]** The psychological structure of brand perception is context-dependent, requiring distinct measurement models for differen…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand as Signal
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[BA-000080]** Under conditions of high uncertainty about performance, a nonprofit's brand equity functions as a credible signal of tru…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Charitable Giving Prevalence
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[CG-000001]** Approximately two-thirds of the Austrian population donate to charitable causes annually.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Consumer Brand Disposition
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[CB-000023]** Consumers possess measurable, stable dispositions, such as brand schematicity or brand engagement in self-concept, that …  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Credence-Good Donation
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[CG-000004]** Charitable donations are credence-good exchanges in which donors cannot directly verify the quality or impact of the out…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Customer-Based Brand Equity Dimensions
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[CB-000004]** The relative influence of Customer-Based Brand Equity dimensions varies across product and service contexts.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Dynamic Brand Equity
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[DB-000003]** Existing nonprofit brand equity models are largely static and cross-sectional.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Evidence Boundary
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[EB-000005]** The university branding literature reviewed by Yaping et al.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Evidence-Theory-Ontology Workflow
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[ET-000001]** The Evidence-Theory-Ontology (ETO) workflow is a transparent, replicable, and logically sound procedure for transforming…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Hybrid Organisation
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[HO-000001]** A core strategic challenge for social enterprises is managing the inherent tension between their social and commercial o…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Identifiable_Victim_Effect
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[IV-000001]** An affective response to a specific, identifiable individual in need is a stronger trigger for giving than a cognitive r…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Integrated Giving Models
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[IG-000001]** Existing charitable giving research lacks formal models that integrate all major mechanisms of giving.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Longitudinal Donation Behaviour
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[LD-000001]** Longitudinal evidence on whether integrated brand equity and TPB models predict sustained giving behaviour is not suffic…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Model Standardisation
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[MS-000001]** The literature lacks a single standardized model for integrating customer-based brand equity with IBM or TPB constructs.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### NPO Competition
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[NC-000001]** Nonprofits primarily perceive competition in the fundraising market rather than in the client service delivery market.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### NPO Marketing Orientation
_N claims: 2 · Mean posterior: 0.80 · Grade A/B: 2_

- **[NM-000001]** Nonprofit practitioners often conflate marketing with fundraising, rather than viewing it as a strategic function for ma…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NM-000002]** Stakeholder resistance to funding marketing as an operational expense is a significant impediment to nonprofit marketing…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Negative Reputation
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[NR-000001]** Under negative CEO reputation, the factors predicting donation intention become more limited than under positive reputat…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Equity Ontology
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[NB-000053]** The reviewed nonprofit brand equity models lack a shared ontology that consistently distinguishes brand equity from beha…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Observed Donation Behaviour
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[OD-000001]** None of the reviewed nonprofit brand equity models provides a complete empirically tested path from brand perceptions to…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Past Donation Behavior
_N claims: 2 · Mean posterior: 0.80 · Grade A/B: 2_

- **[PD-000002]** Past donation behavior positively predicts future charitable donation intention.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[PD-000003]** Past donation behavior positively predicts future charitable donation behavior.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Post-Intentional Factors
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[PI-000005]** Explaining the intention-behavior gap requires incorporating post-intentional psychological constructs related to planni…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Relational Brand Drivers
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[RB-000001]** Satisfaction, trust, and commitment have stronger effects on donation intentions than on actual donation behavior.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Research Methods
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[RM-000002]** Most research on the intention-behavior gap uses between-person designs, which may not capture the dynamic, within-perso…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Research Quality
_N claims: 2 · Mean posterior: 0.80 · Grade A/B: 2_

- **[RQ-000002]** Replications and retractions each constitute less than 1% of publications in philanthropy research.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[RQ-000003]** Statistical reporting errors that favor study hypotheses are more common in philanthropy research than in adjacent field…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Routine Behaviour
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[RB-000005]** For recurring pro-social behaviours, the primary behavioural driver shifts from conscious intention to an incorporated, …  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Stakeholder Scope
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[SS-000003]** The reviewed nonprofit brand equity models are primarily developed from the perspective of individual donors or the gene…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Theory (Bourdieu)
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[TB-000001]** Sociological frameworks, such as Bourdieu's, provide explanatory power for philanthropic action beyond purely economic o…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Traditional Synthesis Methods
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[TS-000003]** NHST-based meta-analyses and purely narrative reviews are insufficient for building cumulative, computationally useful t…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Trust; Perceived Efficacy; Value Alignment; Donation Behavior
_N claims: 1 · Mean posterior: 0.80 · Grade A/B: 1_

- **[TP-000001]** Trust in a nonprofit, perceived organizational efficacy, and donor-brand value alignment are stronger direct predictors …  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Descriptive Social Norm
_N claims: 6 · Mean posterior: 0.80 · Grade A/B: 6_

- **[DS-000009]** Perceived descriptive social norms have a positive but modest statistical association with charitable donation intention…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DS-000010]** In the context of charitable giving, the influence of injunctive norms on donation intention is stronger than the influe…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DS-000011]** Descriptive norms (operating via social proof) and injunctive norms (operating via social approval) are conceptually and…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DS-000012]** Adding a distinct descriptive norm construct to models based on the Theory of Planned Behaviour improves the explained v…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DS-000013]** The influence of descriptive social norms on pro-social intention is moderated by referent group proximity, with proxima…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DS-000014]** The reported effect size of social norms on charitable giving is at risk of being inflated due to publication bias in no…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Habit
_N claims: 3 · Mean posterior: 0.79 · Grade A/B: 3_

- **[H-000002]** Habit, as an automatic response to contextual cues, can either support or undermine the enactment of deliberate intentio…  
  P = 0.90 · A (strong)  
  EVIDs: 10 supporting, 0 contradicting, 0 mixed · N sources: 96

- **[H-000001]** Commitment reinforces past donation behaviour and facilitates donation habit formation.  
  P = 0.74 · B (moderate)  
  EVIDs: 10 supporting, 0 contradicting, 0 mixed · N sources: 96

- **[H-000003]** Psychological habit automaticity has a significant predictive effect on future actual donation behaviour, independent of…  
  P = 0.74 · B (moderate)  
  EVIDs: 10 supporting, 0 contradicting, 0 mixed · N sources: 96


### Brand Authenticity
_N claims: 10 · Mean posterior: 0.79 · Grade A/B: 10_

- **[BA-000072]** Brand authenticity is a measurable, multi-dimensional construct distinct from traditional brand evaluation metrics like …  
  P = 0.89 · A (strong)  
  EVIDs: 20 supporting, 0 contradicting, 1 mixed · N sources: 33

- **[BA-000001]** Perceived nonprofit brand authenticity positively influences intentions to provide support to a nonprofit.  
  P = 0.78 · A (strong)  
  EVIDs: 20 supporting, 0 contradicting, 1 mixed · N sources: 33

- **[BA-000012]** Brand authenticity was not retained as a valid measurement component in the final donor-based NGO brand equity model.  
  P = 0.78 · A (strong)  
  EVIDs: 20 supporting, 0 contradicting, 1 mixed · N sources: 33

- **[BA-000043]** Brand authenticity is a unidimensional construct representing the perceived degree to which a brand object is the quinte…  
  P = 0.78 · A (strong)  
  EVIDs: 20 supporting, 0 contradicting, 1 mixed · N sources: 33

- **[BA-000044]** Multidimensional conceptualizations of brand authenticity risk confounding the core construct with its antecedents, cons…  
  P = 0.78 · A (strong)  
  EVIDs: 20 supporting, 0 contradicting, 1 mixed · N sources: 33

- **[BA-000045]** Brand authenticity is conferred by audience perception rather than determined solely by an organisation’s internal value…  
  P = 0.78 · A (strong)  
  EVIDs: 20 supporting, 0 contradicting, 1 mixed · N sources: 33

- **[BA-000046]** A brand can be perceived as authentic without being the pioneer or first entrant in its category.  
  P = 0.78 · A (strong)  
  EVIDs: 20 supporting, 0 contradicting, 1 mixed · N sources: 33

- **[BA-000047]** Perceived brand authenticity requires that the brand object be evaluated in relation to a recognizable category.  
  P = 0.78 · A (strong)  
  EVIDs: 20 supporting, 0 contradicting, 1 mixed · N sources: 33

- **[BA-000048]** The perception of which brand is the quintessential exemplar of a category may differ across stakeholder audiences.  
  P = 0.78 · A (strong)  
  EVIDs: 20 supporting, 0 contradicting, 1 mixed · N sources: 33

- **[BA-000050]** The nomological role of exemplar-based brand authenticity in relation to brand strength and behavioural outcomes remains…  
  P = 0.78 · A (strong)  
  EVIDs: 20 supporting, 0 contradicting, 1 mixed · N sources: 33


### Brand Love
_N claims: 1 · Mean posterior: 0.79 · Grade A/B: 1_

- **[BL-000012]** High-arousal affective states toward brands, such as brand love, are measurable constructs distinct from lower-arousal s…  
  P = 0.79 · A (strong) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 4


### Volunteer Role Identity
_N claims: 4 · Mean posterior: 0.79 · Grade A/B: 4_

- **[VR-000001]** A behavior-specific volunteer role identity is a positive and significant predictor of an individual's intention to volu…  
  P = 0.84 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 10

- **[VR-000002]** A behavior-specific volunteer role identity is a positive and significant predictor of volunteer behavioral outcomes, su…  
  P = 0.84 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 10

- **[VR-000003]** The act of volunteering initiates a behavioral feedback loop where role enactment strengthens volunteer role identity, w…  
  P = 0.84 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 10

- **[VR-000004]** The influence of antecedent factors on long-term volunteer performance is fully mediated by volunteer role identity and …  
  P = 0.64 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 10


### ETO Workflow
_N claims: 1 · Mean posterior: 0.79 · Grade A/B: 1_

- **[EW-000001]** The ETO workflow is a valid and rigorous methodology for moving from heterogeneous empirical inputs to a formal, reusabl…  
  P = 0.79 · A (strong)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 17


### Brand Resonance
_N claims: 4 · Mean posterior: 0.79 · Grade A/B: 4_

- **[BR-000016]** Building brand equity is a hierarchical psychological process that progresses through four levels: identity (salience), …  
  P = 0.86 · A (strong)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 3

- **[BR-000017]** The brand equity building process involves both rational and emotional psychological pathways.  
  P = 0.86 · A (strong)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 3

- **[BR-000013]** Brand Resonance with a nonprofit health-promotion brand positively predicts stakeholders' behavioural intentions to adop…  
  P = 0.71 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 3

- **[BR-000018]** The behavioural effectiveness of a brand is determined by the development of a hierarchical knowledge structure in stake…  
  P = 0.71 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 3


### Giving Intention
_N claims: 1 · Mean posterior: 0.79 · Grade A/B: 1_

- **[GI-000001]** Giving intention has a significant positive effect on subsequent giving behavior.  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 3 contradicting, 1 mixed · N sources: 22


### Signal Credibility
_N claims: 4 · Mean posterior: 0.79 · Grade A/B: 4_

- **[SC-000004]** In markets with informational asymmetry, consumer-based brand equity increases when consumers perceive a brand signal as…  
  P = 0.79 · A (strong)  
  EVIDs: 10 supporting, 0 contradicting, 0 mixed · N sources: 4

- **[SC-000005]** Brand signal credibility increases consumers’ perceived quality of the branded offering.  
  P = 0.79 · A (strong)  
  EVIDs: 10 supporting, 0 contradicting, 0 mixed · N sources: 4

- **[SC-000006]** Brand signal credibility reduces consumers’ perceived risk in evaluating a branded offering.  
  P = 0.79 · A (strong)  
  EVIDs: 10 supporting, 0 contradicting, 0 mixed · N sources: 4

- **[SC-000007]** Brand signal credibility reduces consumers’ information costs during decision-making.  
  P = 0.79 · A (strong)  
  EVIDs: 10 supporting, 0 contradicting, 0 mixed · N sources: 4


### Organizational Identification
_N claims: 5 · Mean posterior: 0.78 · Grade A/B: 5_

- **[OI-000005]** Higher organizational identification with a nonprofit is positively associated with higher donation intentions toward th…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 18 supporting, 2 contradicting, 3 mixed · N sources: 17

- **[OI-000006]** Higher organizational identification with a nonprofit is positively associated with non-monetary prosocial behaviors, in…  
  P = 0.84 · A (strong) ⚠ conflict  
  EVIDs: 18 supporting, 2 contradicting, 3 mixed · N sources: 17

- **[OI-000003]** Donor satisfaction is a causal antecedent to donor-nonprofit organizational identification.  
  P = 0.74 · B (moderate) ⚠ conflict  
  EVIDs: 18 supporting, 2 contradicting, 3 mixed · N sources: 17

- **[OI-000004]** Organizational Identification (a group-level construct) and Donor Identity Salience (an individual-level construct) are …  
  P = 0.74 · B (moderate) ⚠ conflict  
  EVIDs: 18 supporting, 2 contradicting, 3 mixed · N sources: 17

- **[OI-000007]** Organizational identification mediates the positive relationship between a stakeholder's perception of relationship inve…  
  P = 0.74 · B (moderate) ⚠ conflict  
  EVIDs: 18 supporting, 2 contradicting, 3 mixed · N sources: 17


### Awareness of Need
_N claims: 2 · Mean posterior: 0.78 · Grade A/B: 2_

- **[AO-000001]** Potential donors must become aware of a need for support before charitable giving can occur.  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 0 mixed · N sources: 2

- **[AO-000002]** Identifiable single victims generate stronger giving responses than statistical presentations of large numbers of victim…  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 0 mixed · N sources: 2


### Behavioural Loyalty
_N claims: 1 · Mean posterior: 0.78 · Grade A/B: 1_

- **[BL-000006]** The strength of the relationship between brand knowledge and purchase propensity increases as consumers move from non-us…  
  P = 0.78 · A (strong)  
  EVIDs: 10 supporting, 0 contradicting, 0 mixed · N sources: 41


### Identity
_N claims: 1 · Mean posterior: 0.78 · Grade A/B: 1_

- **[I-000005]** The degree to which a behavior is central to an individual's self-concept influences the translation of intention into a…  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 8 supporting, 0 contradicting, 2 mixed · N sources: 61


### Longitudinal Validation
_N claims: 1 · Mean posterior: 0.78 · Grade A/B: 1_

- **[LV-000001]** Existing integrated CBBE-IBM studies are predominantly cross-sectional and provide limited longitudinal evidence for cau…  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 88


### Field
_N claims: 3 · Mean posterior: 0.78 · Grade A/B: 3_

- **[F-000002]** Organizational philanthropy is a strategic practice aimed at securing legitimacy and competitive position within a socia…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 12 supporting, 2 contradicting, 1 mixed · N sources: 16

- **[F-000004]** Pro-social behaviour occurs within structured, competitive social spaces (fields) where organisations and individuals co…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 12 supporting, 2 contradicting, 1 mixed · N sources: 16

- **[F-000003]** The symbolic capital of a nonprofit brand is contingent on the structure of its philanthropic field and can change indep…  
  P = 0.72 · B (moderate) ⚠ conflict  
  EVIDs: 12 supporting, 2 contradicting, 1 mixed · N sources: 16


### Donor Satisfaction
_N claims: 4 · Mean posterior: 0.78 · Grade A/B: 4_

- **[DS-000008]** An organization's donor-oriented strategy positively influences donor satisfaction.  
  P = 0.87 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 3 mixed · N sources: 17

- **[DS-000002]** Donor satisfaction directly and positively influences donor loyalty in nonprofit contexts.  
  P = 0.75 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 3 mixed · N sources: 17

- **[DS-000003]** Donor satisfaction is a causal antecedent of donor-nonprofit identification in nonprofit contexts.  
  P = 0.75 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 3 mixed · N sources: 17

- **[DS-000007]** Donor satisfaction has a positive causal effect on organisational identification in nonprofit service contexts.  
  P = 0.75 · A (strong) ⚠ conflict  
  EVIDs: 13 supporting, 0 contradicting, 3 mixed · N sources: 17


### Self-Concept
_N claims: 2 · Mean posterior: 0.78 · Grade A/B: 2_

- **[SC-000002]** An individual donor's self-concept has a direct positive effect on their giving intention.  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 2 contradicting, 1 mixed · N sources: 84

- **[SC-000021]** Alignment between a nonprofit's brand identity and a stakeholder's self-concept positively predicts their giving intenti…  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 23 supporting, 2 contradicting, 1 mixed · N sources: 84


### NGO Brand Equity
_N claims: 1 · Mean posterior: 0.78 · Grade A/B: 1_

- **[NB-000054]** NGOs require a donor-based brand equity model that differs from general nonprofit brand equity models.  
  P = 0.78 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 1


### Brand Loyalty
_N claims: 8 · Mean posterior: 0.78 · Grade A/B: 8_

- **[BL-000002]** Brand loyalty manifests in customer behaviors such as repeat purchase, willingness to pay more, and willingness to recom…  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 2 contradicting, 2 mixed · N sources: 61

- **[BL-000005]** The construct of loyalty is less developed in nonprofit brand equity research than the constructs of awareness and assoc…  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 2 contradicting, 2 mixed · N sources: 61

- **[BL-000007]** Brand loyalty is a behavioural consequence of consumer-based brand equity rather than a constituent component of consume…  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 2 contradicting, 2 mixed · N sources: 61

- **[BL-000009]** The Brand Loyalty dimension of consumer-based brand equity can be validly measured as an attitudinal construct represent…  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 2 contradicting, 2 mixed · N sources: 61

- **[BL-000010]** Brand trust is a positive antecedent of brand loyalty.  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 2 contradicting, 2 mixed · N sources: 61

- **[BL-000011]** Donor-perceived brand loyalty is positively associated with a charity brand's overall brand equity.  
  P = 0.79 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 2 contradicting, 2 mixed · N sources: 61

- **[BL-000001]** Brand commitment is more appropriate than brand loyalty for capturing the donor-NGO relationship.  
  P = 0.75 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 2 contradicting, 2 mixed · N sources: 61

- **[BL-000008]** Brand loyalty results from brand awareness and brand associations rather than constituting a direct component of brand e…  
  P = 0.75 · A (strong) ⚠ conflict  
  EVIDs: 16 supporting, 2 contradicting, 2 mixed · N sources: 61


### Brand Attitude
_N claims: 3 · Mean posterior: 0.78 · Grade A/B: 3_

- **[BA-000004]** In some charitable giving studies, attitude toward the charitable organisation is a non-significant predictor of donatio…  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 14 supporting, 2 contradicting, 3 mixed · N sources: 33

- **[BA-000061]** In new donor acquisition for international aid charities, favourable donor attitude toward a nonprofit brand positively …  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 14 supporting, 2 contradicting, 3 mixed · N sources: 33

- **[BA-000062]** Brand attitude partially mediates the positive relationship between nonprofit brand salience and new donor brand choice …  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 14 supporting, 2 contradicting, 3 mixed · N sources: 33


### Habitus
_N claims: 8 · Mean posterior: 0.77 · Grade A/B: 8_

- **[H-000011]** Habitus, as a set of durable and class-based dispositions, is the primary driver of routine and sustained pro-social beh…  
  P = 0.83 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 2 contradicting, 5 mixed · N sources: 28

- **[H-000004]** An individual's habitus is the primary generator of their nonprofit supporter behaviour.  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 2 contradicting, 5 mixed · N sources: 28

- **[H-000006]** An individual's habitus is not static and can be modified, challenging purely deterministic models of social reproductio…  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 2 contradicting, 5 mixed · N sources: 28

- **[H-000009]** Strict social reproduction models of habitus are insufficient to fully explain philanthropic behaviour, as the acquisiti…  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 2 contradicting, 5 mixed · N sources: 28

- **[H-000010]** The effectiveness of a nonprofit's brand-enabled behaviour architecture is moderated by its alignment with the habitus o…  
  P = 0.78 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 2 contradicting, 5 mixed · N sources: 28

- **[H-000005]** The components of the Theory of Planned Behaviour (attitudes, subjective norms, perceived behavioural control) are shape…  
  P = 0.75 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 2 contradicting, 5 mixed · N sources: 28

- **[H-000007]** A nonprofit brand's behavioural effectiveness increases with its perceived alignment with the habitus of a target donor …  
  P = 0.75 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 2 contradicting, 5 mixed · N sources: 28

- **[H-000008]** An individual's habitus, shaped by their social trajectory, conditions their dispositions toward giving, influencing whi…  
  P = 0.75 · A (strong) ⚠ conflict  
  EVIDs: 19 supporting, 2 contradicting, 5 mixed · N sources: 28


### Fundraising Appeals
_N claims: 2 · Mean posterior: 0.77 · Grade A/B: 2_

- **[FA-000001]** Fundraising appeals that emphasize the donor’s emotional benefit generate higher participation or donation amounts than …  
  P = 0.77 · A (strong)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 63

- **[FA-000002]** Fundraising appeals that emphasize the donor's emotional benefit generate higher charitable response than appeals focuse…  
  P = 0.77 · A (strong)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 63


### Demographics
_N claims: 5 · Mean posterior: 0.77 · Grade A/B: 5_

- **[D-000001]** Compared to donors, non-donors are on average younger.  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 25

- **[D-000002]** Compared to donors, non-donors are more likely to be male.  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 25

- **[D-000003]** Compared to donors, non-donors tend to have lower levels of income.  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 25

- **[D-000004]** Compared to donors, non-donors tend to have lower levels of education.  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 25

- **[D-000005]** Compared to donors, non-donors are less likely to be religious.  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 25


### Nonprofit Brand Personality
_N claims: 8 · Mean posterior: 0.77 · Grade A/B: 8_

- **[NB-000039]** Nonprofit brand personality has a direct positive effect on an individual's giving intention.  
  P = 0.77 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 27

- **[NB-000042]** Nonprofit brand personality has a positive effect on an individual donor's self-concept.  
  P = 0.77 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 27

- **[NB-000045]** The effect of nonprofit brand personality on giving intention is partially mediated by the donor's self-concept.  
  P = 0.77 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 27

- **[NB-000088]** The perceived brand personality of a nonprofit organization is a four-dimensional construct consisting of Integrity, Nur…  
  P = 0.77 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 27

- **[NB-000089]** The five-factor brand personality structure developed for commercial brands is not directly applicable to the nonprofit …  
  P = 0.77 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 27

- **[NB-000090]** Nurturance is a core dimension of nonprofit brand personality that is not prominent in for-profit models.  
  P = 0.77 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 27

- **[NB-000091]** The Integrity dimension in nonprofit brand personality subsumes and reframes commercial brand sincerity, focusing on rel…  
  P = 0.77 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 27

- **[NB-000092]** Donors use the personification of a nonprofit into a brand personality as a cognitive heuristic to simplify evaluation u…  
  P = 0.77 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 27


### Donation Amount
_N claims: 1 · Mean posterior: 0.77 · Grade A/B: 1_

- **[DA-000002]** Per-capita charitable donation amounts in Austria are modest compared with liberal welfare regimes such as the United St…  
  P = 0.77 · A (strong)  
  EVIDs: 8 supporting, 0 contradicting, 1 mixed · N sources: 78


### Past Behaviour
_N claims: 6 · Mean posterior: 0.77 · Grade A/B: 6_

- **[PB-000018]** The intention to perform an institutionalized pro-social behavior is positively predicted by past behavior in the same d…  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 6 supporting, 1 contradicting, 1 mixed · N sources: 47

- **[PB-000027]** Past volunteering behavior is a positive and significant predictor of future volunteering behavior.  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 6 supporting, 1 contradicting, 1 mixed · N sources: 47

- **[PB-000031]** The statistical association between past donation frequency and future giving represents a compound effect of stable pre…  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 6 supporting, 1 contradicting, 1 mixed · N sources: 47

- **[PB-000032]** Past donation behaviour is a strong and reliable predictor of future donation behaviour.  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 6 supporting, 1 contradicting, 1 mixed · N sources: 47

- **[PB-000019]** Past behavior is the strongest predictor of future intentions for institutionalized pro-social behavior, relative to oth…  
  P = 0.68 · B (moderate) ⚠ conflict  
  EVIDs: 6 supporting, 1 contradicting, 1 mixed · N sources: 47

- **[PB-000017]** Past donation behaviour can be negatively associated with future donation intentions under certain conditions.  
  P = 0.62 · B (moderate) ⚠ conflict  
  EVIDs: 6 supporting, 1 contradicting, 1 mixed · N sources: 47


### Brand Familiarity
_N claims: 14 · Mean posterior: 0.76 · Grade A/B: 14_

- **[BF-000001]** Brand familiarity alone is insufficient to reliably increase donation intention without accompanying trust or positive b…  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000002]** Brand familiarity increases a nonprofit's likelihood of being considered for donation by increasing salience and perceiv…  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000003]** Nonprofit brand familiarity is positively associated with propensity to donate.  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000004]** Familiarity with a nonprofit brand is negatively associated with resource provider support intentions in Faircloth's exp…  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000005]** Brand familiarity does not have a significant direct effect on donor-based brand equity for childhood-related NGOs in th…  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000006]** Brand familiarity is positively associated with donation intention.  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000007]** In the nonprofit sector, greater stakeholder familiarity with an organization can be negatively associated with intentio…  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000009]** Brand familiarity can have non-significant or negative effects on nonprofit brand equity when familiarity is associated …  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000010]** Brand familiarity moderates the relationship between performance-expectation disconfirmation and customer satisfaction.  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000011]** The influence of performance-expectation disconfirmation on satisfaction is stronger for individuals with low brand fami…  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000012]** Brand familiarity is associated with accumulated direct and indirect brand-related experiences.  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000013]** High-familiarity consumers rely less on single-encounter disconfirmation when forming satisfaction than low-familiarity …  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000014]** Low-familiarity consumers update post-consumption expectations more strongly through service experiences than high-famil…  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122

- **[BF-000008]** The behavioural effect of nonprofit brand familiarity depends on the valence of stakeholders’ pre-existing perceptions o…  
  P = 0.74 · B (moderate) ⚠ conflict  
  EVIDs: 25 supporting, 4 contradicting, 8 mixed · N sources: 122


### Integrated Behavioural Model
_N claims: 2 · Mean posterior: 0.76 · Grade A/B: 2_

- **[IB-000016]** Behavioural enactment is influenced by knowledge, salience, environmental constraints, and habit.  
  P = 0.83 · A (strong)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 131

- **[IB-000013]** Brand awareness or familiarity increases donor knowledge of how and where to donate.  
  P = 0.70 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 131


### Internal Brand Socialization
_N claims: 1 · Mean posterior: 0.76 · Grade A/B: 1_

- **[IB-000011]** Employee buy-in is perceived by senior nonprofit marketers as necessary for delivering consistent brand-aligned stakehol…  
  P = 0.76 · A (strong) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 2


### Financial Brand Equity
_N claims: 1 · Mean posterior: 0.76 · Grade A/B: 1_

- **[FB-000001]** Financial brand equity approaches conceptualise brands as assets that create separable value through incremental cash fl…  
  P = 0.76 · A (strong)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 58


### Legitimacy
_N claims: 1 · Mean posterior: 0.76 · Grade A/B: 1_

- **[L-000003]** Nonprofit brands signal organisational legitimacy to stakeholders beyond individual donors.  
  P = 0.76 · A (strong)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 102


### Donation Behavior
_N claims: 1 · Mean posterior: 0.76 · Grade A/B: 1_

- **[DB-000009]** Attitudinal donor loyalty has a weak or non-significant statistical relationship with actual donation behavior.  
  P = 0.76 · A (strong) ⚠ conflict  
  EVIDs: 29 supporting, 7 contradicting, 8 mixed · N sources: 107


### Moral Norm
_N claims: 3 · Mean posterior: 0.76 · Grade A/B: 3_

- **[MN-000009]** An individual's internal sense of moral obligation is a powerful and significant predictor of their intention to donate.  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 4 supporting, 0 contradicting, 2 mixed · N sources: 34

- **[MN-000001]** Donation intention models that include moral norms explain more variance than models limited to subjective social norms.  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 4 supporting, 0 contradicting, 2 mixed · N sources: 34

- **[MN-000007]** Brand attitudes toward a nonprofit organisation can become non-significant predictors of donation outcomes when moral no…  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 4 supporting, 0 contradicting, 2 mixed · N sources: 34


### Habit Formation
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[HF-000001]** The stability of the donation context positively moderates the strength of the relationship between past behavior and co…  
  P = 0.75 · A (strong) ⚠ conflict  
  EVIDs: 1 supporting, 1 contradicting, 0 mixed · N sources: 4


### Brand Experience
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[BE-000037]** Brand experience includes sensory, affective, and behavioural dimensions.  
  P = 0.75 · A (strong)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 23


### Value Congruence
_N claims: 2 · Mean posterior: 0.75 · Grade A/B: 2_

- **[VC-000001]** Donors are more likely to align with organizations whose mission is congruent with their self-concept.  
  P = 0.75 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 0 contradicting, 2 mixed · N sources: 5

- **[VC-000002]** Value congruence between donor and NGO strengthens donor identification with the organization.  
  P = 0.75 · A (strong) ⚠ conflict  
  EVIDs: 10 supporting, 0 contradicting, 2 mixed · N sources: 5


### Integrated Behavior Model
_N claims: 2 · Mean posterior: 0.75 · Grade A/B: 2_

- **[IB-000028]** Comprehensive integrated behavior models do not offer substantially greater predictive validity for behavior than more p…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[IB-000029]** The primary theoretical value of integrated behavior models lies in identifying specific, context-dependent post-intenti…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Internal Brand Communication
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[IB-000019]** Effective internal communication supports a consistent understanding of brand positioning and values among nonprofit emp…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Internal Branding Implementation
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[IB-000020]** The primary branding challenge reported by senior marketing personnel in UK nonprofit organizations is the implementatio…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Mission-Brand Tension
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[MB-000001]** Internal resistance to nonprofit brand management arises when branding and marketing are perceived as commercial techniq…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Model Generalizability
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[MG-000001]** Nonprofit brand equity models built for specific organizations have limited generalizability across the nonprofit sector…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### NPO Brand Attitude
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[NB-000018]** Attitude toward the nonprofit organization is not consistently significant as a predictor of charitable donation intenti…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### NPO Brand Function
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[NB-000084]** A strong nonprofit brand reduces a potential volunteer's perceived risk and cognitive effort during the choice process.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### NPO Performance Measurement
_N claims: 2 · Mean posterior: 0.75 · Grade A/B: 2_

- **[NP-000007]** A performance measurement system for nonprofit donor behaviour should incorporate measures of both transactional satisfa…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NP-000008]** An augmented American Customer Satisfaction Index (ACSI) model, incorporating organisational identification, is a valid …  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Authenticity
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[NB-000063]** The exemplar-based definition of brand authenticity is applicable to nonprofit organisations as brand objects.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Awareness
_N claims: 4 · Mean posterior: 0.75 · Grade A/B: 4_

- **[NB-000030]** Nonprofit brand awareness is a prerequisite for the development of nonprofit brand trust and nonprofit brand commitment.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NB-000041]** Nonprofit brand awareness has a direct positive effect on an individual's giving intention.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NB-000043]** Nonprofit brand awareness has a positive effect on an individual donor's self-concept.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NB-000046]** The effect of nonprofit brand awareness on giving intention is partially mediated by the donor's self-concept.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Commitment
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[NB-000034]** Nonprofit brand commitment represents an enduring desire by stakeholders to maintain a valued relationship with a nonpro…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Effectiveness
_N claims: 3 · Mean posterior: 0.75 · Grade A/B: 3_

- **[NB-000064]** Nonprofit brand effectiveness increases when internal brand identity, brand performance, and external brand image are al…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NB-000065]** Nonprofit branding effectiveness cannot be adequately measured by brand image metrics alone.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NB-000066]** Nonprofit branding effectiveness cannot be adequately measured by brand identity metrics alone.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Equity Architecture
_N claims: 2 · Mean posterior: 0.75 · Grade A/B: 2_

- **[NB-000035]** Existing nonprofit brand equity models do not specify the psychological belief-formation mechanisms through which brand …  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NB-000036]** The internal structure of nonprofit brand equity is not settled across additive, relational, hierarchical, processual, a…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Image Measurement
_N claims: 2 · Mean posterior: 0.75 · Grade A/B: 2_

- **[NB-000058]** The four-dimension nonprofit brand image scale developed by Michel and Rieunier (2012) shows poor factor structure and i…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NB-000059]** A six-factor nonprofit brand image scale including Usefulness, Efficiency, Affect, Dynamism, Reliability, and Ethicality…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Image Scale
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[NB-000061]** The 18-item six-factor nonprofit brand image scale demonstrates reliability, convergent validity, discriminant validity,…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Personality; Donation Intention
_N claims: 2 · Mean posterior: 0.75 · Grade A/B: 2_

- **[NB-000094]** The perceived Integrity of a nonprofit brand is positively correlated with an individual's likelihood of contributing.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NB-000095]** The perceived Nurturance of a nonprofit brand is positively correlated with an individual's likelihood of contributing.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Personality; Trust
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[NB-000093]** The perceived Integrity of a nonprofit organization is a key antecedent of donor trust.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Salience
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[NB-000016]** Brand salience is particularly important for brand choice among new donors.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Typicality
_N claims: 2 · Mean posterior: 0.75 · Grade A/B: 2_

- **[NB-000082]** The perceived typicality of a nonprofit within its cause category is a significant positive predictor of an individual's…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NB-000083]** The perceived typicality of a nonprofit within its cause category is a significant positive predictor of an individual's…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand as Heuristic
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[NB-000001]** Nonprofit brands function as cognitive heuristics that reduce donors' perceived risk and decision-making costs.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Performance Measurement
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[NP-000001]** Nonprofit organisational performance cannot be adequately measured using financial metrics alone.  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Trust
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[NT-000001]** Trust in a charitable organization is a distinct positive antecedent of donation intention alongside attitude, norms, an…  
  P = 0.75 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Bayesian Evidence Aggregation
_N claims: 2 · Mean posterior: 0.75 · Grade A/B: 2_

- **[BE-000065]** A Bayesian evidence aggregation framework provides a more robust and scientifically sound basis for cumulative theory bu…  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 2 supporting, 0 contradicting, 2 mixed · N sources: 17

- **[BE-000080]** Bayesian updating, specifically Jeffrey Conditionalization, offers a coherent epistemological framework for integrating …  
  P = 0.67 · B (moderate) ⚠ conflict  
  EVIDs: 2 supporting, 0 contradicting, 2 mixed · N sources: 17


### Digital Brand Equity
_N claims: 1 · Mean posterior: 0.75 · Grade A/B: 1_

- **[DB-000002]** Digital brand equity requires metrics such as share of search, digital awareness, and online sentiment that are not capt…  
  P = 0.75 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 41


### Donor-Based Brand Equity
_N claims: 4 · Mean posterior: 0.75 · Grade A/B: 4_

- **[DB-000010]** An empirically validated model that integrates donor-based brand equity into the Theory of Planned Behavior framework fo…  
  P = 0.85 · A (strong) ⚠ conflict  
  EVIDs: 7 supporting, 0 contradicting, 3 mixed · N sources: 54

- **[DB-000004]** In the NGO context, brand associations have a significant positive effect on donor-based brand equity.  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 7 supporting, 0 contradicting, 3 mixed · N sources: 54

- **[DB-000005]** In the NGO context, brand commitment has a significant positive effect on donor-based brand equity.  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 7 supporting, 0 contradicting, 3 mixed · N sources: 54

- **[DB-000006]** A model using brand familiarity, brand associations, and brand commitment explains 56.  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 7 supporting, 0 contradicting, 3 mixed · N sources: 54


### Perceived Risk
_N claims: 2 · Mean posterior: 0.75 · Grade A/B: 2_

- **[PR-000001]** Reductions in perceived risk function as antecedents of consumer-based brand equity rather than as consequences of it.  
  P = 0.75 · B (moderate) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 3 mixed · N sources: 83

- **[PR-000002]** Brands reduce perceived risk in stakeholder decision-making.  
  P = 0.75 · B (moderate) ⚠ conflict  
  EVIDs: 13 supporting, 1 contradicting, 3 mixed · N sources: 83


### Costs and Benefits
_N claims: 2 · Mean posterior: 0.74 · Grade A/B: 2_

- **[CA-000003]** Reducing the net financial cost of giving generally increases the amount donated.  
  P = 0.82 · A (strong) ⚠ conflict  
  EVIDs: 2 supporting, 0 contradicting, 2 mixed · N sources: 1

- **[CA-000004]** Matching grants are generally more effective at increasing donations than economically equivalent rebate framings.  
  P = 0.67 · B (moderate) ⚠ conflict  
  EVIDs: 2 supporting, 0 contradicting, 2 mixed · N sources: 1


### Role-Identity
_N claims: 5 · Mean posterior: 0.74 · Grade A/B: 4_

- **[RI-000002]** The strength of a pro-social role-identity is positively predicted by an individual's past behavior in that domain.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[RI-000003]** The strength of a pro-social role-identity is positively predicted by perceived social expectations.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[RI-000004]** The strength of a pro-social role-identity is positively predicted by parental modeling of the behavior.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[RI-000005]** The strength of a pro-social role-identity is positively predicted by personal norms of moral obligation.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[RI-000001]** The intention to perform an institutionalized pro-social behavior is positively predicted by the strength of the associa…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Context Specificity
_N claims: 2 · Mean posterior: 0.74 · Grade A/B: 2_

- **[CS-000006]** The composition and relevance of brand equity dimensions vary across contexts such as retail, B2B, employee, and digital…  
  P = 0.84 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 9

- **[CS-000004]** The drivers and hierarchical structure of brand equity vary by sector and behavioural context.  
  P = 0.63 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 9


### Material Costs
_N claims: 2 · Mean posterior: 0.74 · Grade A/B: 2_

- **[MC-000003]** Charitable donations increase as the net cost of giving to the donor decreases.  
  P = 0.84 · A (strong) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1

- **[MC-000004]** The magnitude of tax-price elasticity on charitable giving is moderated by national context.  
  P = 0.63 · B (moderate) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Perceived Value
_N claims: 3 · Mean posterior: 0.74 · Grade A/B: 2_

- **[PV-000002]** Higher perceived value from a nonprofit is a positive antecedent of stakeholder satisfaction.  
  P = 0.84 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 17

- **[PV-000003]** Perceived value mediates the relationship between perceived quality and stakeholder satisfaction in nonprofit contexts.  
  P = 0.84 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 17

- **[PV-000001]** Perceived value can function as a distinct brand equity measure from perceived quality.  
  P = 0.53 · C (mixed)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 17


### Reliability
_N claims: 1 · Mean posterior: 0.74 · Grade A/B: 1_

- **[R-000005]** Reliability is a distinct dimension of nonprofit brand image rather than a peripheral association subsumed under other i…  
  P = 0.74 · B (moderate) ⚠ conflict  
  EVIDs: 11 supporting, 1 contradicting, 0 mixed · N sources: 36


### Brand Equity Measurement
_N claims: 2 · Mean posterior: 0.73 · Grade A/B: 2_

- **[BE-000039]** A comprehensive brand equity measurement system includes customer-based measures of loyalty, perceived quality, brand as…  
  P = 0.73 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 71

- **[BE-000040]** Short-term financial metrics are insufficient for managing brand equity because they do not directly capture customer-ba…  
  P = 0.73 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 71


### Non-profit Brand Image
_N claims: 5 · Mean posterior: 0.73 · Grade A/B: 5_

- **[NP-000002]** The conceptual structure of non-profit brand image comprises six distinct dimensions: usefulness, efficiency, affect, dy…  
  P = 0.76 · A (strong) ⚠ conflict  
  EVIDs: 4 supporting, 2 contradicting, 0 mixed · N sources: 6

- **[NP-000003]** The six-dimensional factor structure of non-profit brand image exhibits configural invariance across UK, Indian, and Bos…  
  P = 0.76 · A (strong) ⚠ conflict  
  EVIDs: 4 supporting, 2 contradicting, 0 mixed · N sources: 6

- **[NP-000004]** The measurement scale for non-profit brand image exhibits metric invariance across UK, Indian, and Bosnian-Herzegovinian…  
  P = 0.76 · A (strong) ⚠ conflict  
  EVIDs: 4 supporting, 2 contradicting, 0 mixed · N sources: 6

- **[NP-000005]** The measurement scale for non-profit brand image does not exhibit scalar invariance across UK, Indian, and Bosnian-Herze…  
  P = 0.76 · A (strong) ⚠ conflict  
  EVIDs: 4 supporting, 2 contradicting, 0 mixed · N sources: 6

- **[NP-000006]** Cultural dimensions, socio-economic factors, or religiosity may explain the lack of scalar invariance in non-profit bran…  
  P = 0.64 · B (moderate) ⚠ conflict  
  EVIDs: 4 supporting, 2 contradicting, 0 mixed · N sources: 6


### Actual Control
_N claims: 2 · Mean posterior: 0.73 · Grade A/B: 2_

- **[AC-000002]** Empirical studies testing integrated behavior models frequently fail to measure the 'actual control' component.  
  P = 0.84 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[AC-000001]** Actual control, defined as environmental constraints and individual skills, is a critical moderator of the intention-beh…  
  P = 0.62 · B (moderate)  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 3


### Subjective Norms
_N claims: 4 · Mean posterior: 0.73 · Grade A/B: 4_

- **[SN-000005]** Subjective and descriptive norms show inconsistent effects on donation behaviour across studies.  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 12 supporting, 3 contradicting, 2 mixed · N sources: 62

- **[SN-000002]** Brand awareness, brand trust, and perceived quality can shape subjective norms.  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 12 supporting, 3 contradicting, 2 mixed · N sources: 62

- **[SN-000003]** Subjective norms predict charitable donation intention in some charitable giving contexts.  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 12 supporting, 3 contradicting, 2 mixed · N sources: 62

- **[SN-000004]** The social meaning embedded in brand image and reputation influences individuals’ perceptions of social norms.  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 12 supporting, 3 contradicting, 2 mixed · N sources: 62


### Identifiable Victim Effect
_N claims: 2 · Mean posterior: 0.73 · Grade A/B: 2_

- **[IV-000002]** The claim that donating to a single, identifiable victim is more effective than donating to statistical victims is not s…  
  P = 0.73 · B (moderate) ⚠ conflict  
  EVIDs: 2 supporting, 1 contradicting, 0 mixed · N sources: 49

- **[IV-000003]** The identifiable victim effect fails to replicate consistently in field experiments.  
  P = 0.73 · B (moderate) ⚠ conflict  
  EVIDs: 2 supporting, 1 contradicting, 0 mixed · N sources: 49


### Subjective Norm
_N claims: 4 · Mean posterior: 0.73 · Grade A/B: 4_

- **[SN-000006]** Social information effects on charitable giving produce positive, null, or negative outcomes depending on context.  
  P = 0.74 · B (moderate) ⚠ conflict  
  EVIDs: 9 supporting, 1 contradicting, 6 mixed · N sources: 80

- **[SN-000008]** The influence of subjective norm on donation intention is inconsistent across different cultural and social contexts.  
  P = 0.74 · B (moderate) ⚠ conflict  
  EVIDs: 9 supporting, 1 contradicting, 6 mixed · N sources: 80

- **[SN-000009]** The positive effect of Subjective Norm on donation intention is moderated by cultural context.  
  P = 0.74 · B (moderate) ⚠ conflict  
  EVIDs: 9 supporting, 1 contradicting, 6 mixed · N sources: 80

- **[SN-000001]** The symbolic capital of a nonprofit brand influences whether giving to that organization is perceived as socially approp…  
  P = 0.70 · B (moderate) ⚠ conflict  
  EVIDs: 9 supporting, 1 contradicting, 6 mixed · N sources: 80


### ETO Pipeline
_N claims: 2 · Mean posterior: 0.73 · Grade A/B: 2_

- **[EP-000001]** An integrated Evidence-Theory-Ontology (ETO) pipeline is a more effective methodology for producing cumulative and compu…  
  P = 0.73 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 14

- **[EP-000002]** The effectiveness of the ETO methodology is conditional on the existence of a fragmented body of empirical literature in…  
  P = 0.73 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 14


### Employee-Based Brand Equity
_N claims: 1 · Mean posterior: 0.72 · Grade A/B: 1_

- **[EB-000001]** Traditional consumer-centric brand equity models are insufficient for analysing employees as brand equity stakeholders.  
  P = 0.72 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 29


### Donor Loyalty
_N claims: 6 · Mean posterior: 0.72 · Grade A/B: 6_

- **[DL-000004]** Donor satisfaction is a significant positive driver of donor loyalty.  
  P = 0.80 · A (strong) ⚠ conflict  
  EVIDs: 15 supporting, 4 contradicting, 7 mixed · N sources: 63

- **[DL-000001]** Donor loyalty is simultaneously and directly influenced by donor satisfaction, donor-nonprofit identification, and donor…  
  P = 0.70 · B (moderate) ⚠ conflict  
  EVIDs: 15 supporting, 4 contradicting, 7 mixed · N sources: 63

- **[DL-000002]** The relationship between donor loyalty and actual donation behavior is weak and context-dependent in the nonprofit conte…  
  P = 0.70 · B (moderate) ⚠ conflict  
  EVIDs: 15 supporting, 4 contradicting, 7 mixed · N sources: 63

- **[DL-000003]** Donor loyalty in nonprofits is positively influenced by both a direct effect from donor satisfaction and a parallel, ind…  
  P = 0.70 · B (moderate) ⚠ conflict  
  EVIDs: 15 supporting, 4 contradicting, 7 mixed · N sources: 63

- **[DL-000005]** Both organizational identification and donor identity salience exert direct, positive effects on donor loyalty.  
  P = 0.70 · B (moderate) ⚠ conflict  
  EVIDs: 15 supporting, 4 contradicting, 7 mixed · N sources: 63

- **[DL-000006]** The relative influence of satisfaction versus identity-based constructs on donor loyalty is contingent on the donation c…  
  P = 0.70 · B (moderate) ⚠ conflict  
  EVIDs: 15 supporting, 4 contradicting, 7 mixed · N sources: 63


### Self-Identity
_N claims: 1 · Mean posterior: 0.72 · Grade A/B: 1_

- **[SI-000004]** Donor self-identity directly influences charitable donation intention and future charitable donation behavior.  
  P = 0.72 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 25


### Volunteer Brand Equity
_N claims: 2 · Mean posterior: 0.72 · Grade A/B: 2_

- **[VB-000001]** The 13-dimensional Employee Brand Equity model is empirically applicable to formal volunteers in nonprofit organizations…  
  P = 0.72 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 18

- **[VB-000002]** Corporate employee brand equity measures require linguistic and conceptual adaptation before application to nonprofit vo…  
  P = 0.72 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 18


### Measurement Validity
_N claims: 2 · Mean posterior: 0.72 · Grade A/B: 2_

- **[MV-000001]** The Boenigk & Becker three-dimensional nonprofit brand equity model comprising Awareness, Trust, and Commitment fits Aus…  
  P = 0.72 · B (moderate)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 20

- **[MV-000002]** The Faircloth nonprofit brand equity model shows marginal model fit in the Austrian nonprofit context.  
  P = 0.72 · B (moderate)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 20


### Descriptive Norms
_N claims: 2 · Mean posterior: 0.72 · Grade A/B: 2_

- **[DN-000001]** Descriptive norm information has positive, null, or negative effects on charitable giving across reviewed studies.  
  P = 0.77 · A (strong) ⚠ conflict  
  EVIDs: 6 supporting, 2 contradicting, 2 mixed · N sources: 46

- **[DN-000005]** Descriptive norm appeals that reference a local or psychologically proximate group are more effective at increasing actu…  
  P = 0.66 · B (moderate) ⚠ conflict  
  EVIDs: 6 supporting, 2 contradicting, 2 mixed · N sources: 46


### Identity Salience
_N claims: 2 · Mean posterior: 0.72 · Grade A/B: 2_

- **[IS-000001]** Donor-nonprofit organizational identification is a causal antecedent to the salience of a donor's identity.  
  P = 0.72 · B (moderate) ⚠ conflict  
  EVIDs: 11 supporting, 1 contradicting, 3 mixed · N sources: 14

- **[IS-000002]** Donor identity salience functions as a direct predictor of donor loyalty, not as a moderator of the relationship between…  
  P = 0.72 · B (moderate) ⚠ conflict  
  EVIDs: 11 supporting, 1 contradicting, 3 mixed · N sources: 14


### Brand Infrastructure
_N claims: 4 · Mean posterior: 0.72 · Grade A/B: 4_

- **[BI-000014]** Senior nonprofit marketers in the UK perceive leadership support, clear vision, and employee buy-in as the most critical…  
  P = 0.72 · B (moderate) ⚠ conflict  
  EVIDs: 16 supporting, 0 contradicting, 2 mixed · N sources: 6

- **[BI-000015]** Senior nonprofit marketers in the UK do not perceive limited marketing budgets as the primary obstacle to successful non…  
  P = 0.72 · B (moderate) ⚠ conflict  
  EVIDs: 16 supporting, 0 contradicting, 2 mixed · N sources: 6

- **[BI-000016]** The primary branding challenge identified by senior nonprofit marketers is internal implementation rather than conceptua…  
  P = 0.72 · B (moderate) ⚠ conflict  
  EVIDs: 16 supporting, 0 contradicting, 2 mixed · N sources: 6

- **[BI-000035]** Effective nonprofit brand building requires internal organizational capabilities, processes, and cultural attributes tha…  
  P = 0.72 · B (moderate) ⚠ conflict  
  EVIDs: 16 supporting, 0 contradicting, 2 mixed · N sources: 6


### Brand Understanding
_N claims: 1 · Mean posterior: 0.71 · Grade A/B: 1_

- **[BU-000001]** Within the Brand Understanding Block, brand self-connection and brand associations function as core conditions directly …  
  P = 0.71 · B (moderate)  
  EVIDs: 6 supporting, 0 contradicting, 1 mixed · N sources: 45


### Social Norms
_N claims: 2 · Mean posterior: 0.71 · Grade A/B: 2_

- **[SN-000007]** Injunctive social norms are a more reliable and significant predictor of donation intention than descriptive social norm…  
  P = 0.73 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 0 contradicting, 5 mixed · N sources: 83

- **[SN-000010]** The independent effect of descriptive norms on donation behaviour, when controlling for injunctive norms, is not reliabl…  
  P = 0.68 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 0 contradicting, 5 mixed · N sources: 83


### Transparency
_N claims: 1 · Mean posterior: 0.70 · Grade A/B: 1_

- **[T-000002]** For existing nonprofit supporters or volunteers, brand strength influences bequest intention through transparency.  
  P = 0.70 · B (moderate)  
  EVIDs: 6 supporting, 0 contradicting, 1 mixed · N sources: 36


### Role Clarity
_N claims: 5 · Mean posterior: 0.70 · Grade A/B: 5_

- **[RC-000002]** Volunteer role clarity positively predicts brand citizenship behaviour among formal nonprofit volunteers.  
  P = 0.70 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 15

- **[RC-000003]** Volunteer role clarity positively predicts volunteer satisfaction among formal nonprofit volunteers.  
  P = 0.70 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 15

- **[RC-000004]** Volunteer role clarity positively predicts intention to stay among formal nonprofit volunteers.  
  P = 0.70 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 15

- **[RC-000005]** Volunteer role clarity is a weaker predictor of positive word-of-mouth than volunteer brand commitment.  
  P = 0.70 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 15

- **[RC-000008]** Role clarity provided to volunteers by a nonprofit is a positive predictor of their retention.  
  P = 0.70 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 15


### Measurement
_N claims: 2 · Mean posterior: 0.70 · Grade A/B: 2_

- **[M-000002]** Nonprofit brand equity research lacks validated generalizable scales for brand image and brand personality across nonpro…  
  P = 0.70 · B (moderate) ⚠ conflict  
  EVIDs: 19 supporting, 8 contradicting, 2 mixed · N sources: 134

- **[M-000003]** The lack of consistent operationalization of Bourdieusian concepts, particularly cultural and social capital, is a prima…  
  P = 0.70 · B (moderate) ⚠ conflict  
  EVIDs: 19 supporting, 8 contradicting, 2 mixed · N sources: 134


### Brand Relationship
_N claims: 2 · Mean posterior: 0.70 · Grade A/B: 2_

- **[BR-000004]** Trust, intimacy, relevance, and partner quality function as core causal conditions in configurations that lead to high o…  
  P = 0.73 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 27

- **[BR-000003]** A favourable nonprofit brand personality can legitimate the organisation as a trustworthy relationship partner for resou…  
  P = 0.67 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 27


### Institutional Framing
_N claims: 2 · Mean posterior: 0.70 · Grade A/B: 1_

- **[IF-000001]** Austria’s corporatist welfare state frames private donations as supplementing rather than replacing state responsibility…  
  P = 0.82 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 20

- **[IF-000002]** Austria’s corporatist welfare context is associated with broad participation in charitable giving but modest donation am…  
  P = 0.58 · C (mixed)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 20


### Social Identification
_N claims: 1 · Mean posterior: 0.70 · Grade A/B: 1_

- **[SI-000009]** The positive association between social identification and charitable giving is stronger for self-reported intentions th…  
  P = 0.70 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Warm_Glow_Giving
_N claims: 2 · Mean posterior: 0.70 · Grade A/B: 2_

- **[WG-000010]** Individuals derive private, self-regarding utility (warm glow) from the act of giving itself, independent of the outcome…  
  P = 0.70 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[WG-000011]** The presence of warm glow utility explains why individuals give even when their personal donation has no marginal impact…  
  P = 0.70 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Community
_N claims: 10 · Mean posterior: 0.70 · Grade A/B: 10_

- **[BC-000011]** University brand communities strengthen stakeholder relationships by fostering social bonds, shared values, rituals, and…  
  P = 0.75 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 10

- **[BC-000013]** Social-level brand engagement involves interpreting the brand in an interpersonal, communal, or socio-cultural context.  
  P = 0.75 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 10

- **[BC-000025]** A supporter's level of identification with a charity is positively associated with their level of behavioral involvement…  
  P = 0.69 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 10

- **[BC-000026]** A supporter's level of identification with a charity is positively and directly associated with their level of commitmen…  
  P = 0.69 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 10

- **[BC-000027]** A supporter's level of commitment to a charity is positively associated with their level of behavioral involvement in th…  
  P = 0.69 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 10

- **[BC-000028]** A supporter's level of behavioral involvement in a charity's activities is positively associated with their perceived se…  
  P = 0.69 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 10

- **[BC-000029]** A supporter's perceived sense of community with a charity is positively associated with their level of identification wi…  
  P = 0.69 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 10

- **[BC-000030]** A supporter's perceived sense of community with a charity is positively and directly associated with their level of comm…  
  P = 0.69 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 10

- **[BC-000031]** Supporter commitment can be developed via a cognitive-learning pathway initiated by identification with the charity.  
  P = 0.69 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 10

- **[BC-000032]** Supporter commitment can be developed via an experiential-learning pathway initiated by behavioral involvement in a char…  
  P = 0.69 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 0 mixed · N sources: 10


### Cause Substitution
_N claims: 1 · Mean posterior: 0.70 · Grade A/B: 1_

- **[CS-000005]** When a salient new cause emerges, donors divert funds from other causes rather than drawing entirely on new charitable r…  
  P = 0.70 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 20


### Ethicality
_N claims: 1 · Mean posterior: 0.70 · Grade A/B: 1_

- **[E-000004]** Ethicality is a distinct dimension of nonprofit brand image rather than a peripheral association subsumed under other im…  
  P = 0.70 · B (moderate)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 6


### Intention-Behaviour Gap
_N claims: 6 · Mean posterior: 0.69 · Grade A/B: 6_

- **[IB-000001]** Positive intentions to donate do not always translate into actual donation behaviour.  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 3 contradicting, 3 mixed · N sources: 125

- **[IB-000012]** Donation intentions explain substantially less variance in actual donation behaviour than in stated donation intention.  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 3 contradicting, 3 mixed · N sources: 125

- **[IB-000015]** Positive donation intentions do not consistently translate into realised donation behaviour.  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 3 contradicting, 3 mixed · N sources: 125

- **[IB-000032]** The relationship between donation intention and actual donation behaviour is significantly weaker than the relationship …  
  P = 0.71 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 3 contradicting, 3 mixed · N sources: 125

- **[IB-000003]** Donation intention positively predicts donation behaviour but does not fully explain actual donation behaviour.  
  P = 0.69 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 3 contradicting, 3 mixed · N sources: 125

- **[IB-000014]** Including brand-influenced IBM enactment conditions in a structural model partially explains the gap between donation in…  
  P = 0.64 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 3 contradicting, 3 mixed · N sources: 125


### Uncertainty Reduction
_N claims: 3 · Mean posterior: 0.69 · Grade A/B: 3_

- **[UR-000001]** Charitable giving decisions are made under conditions of incomplete information about nonprofit performance and impact.  
  P = 0.71 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 130

- **[UR-000002]** Nonprofit brands reduce donor decision complexity by functioning as heuristics under conditions of information asymmetry…  
  P = 0.71 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 130

- **[UR-000003]** Perceptions of nonprofit reliability and ethicality reduce donor uncertainty by increasing confidence that the organizat…  
  P = 0.65 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 130


### Fundraising
_N claims: 1 · Mean posterior: 0.69 · Grade A/B: 1_

- **[F-000001]** Digital fundraising methods, including crowdfunding, are an increasingly significant component of NPO funding strategies…  
  P = 0.69 · B (moderate)  
  EVIDs: 13 supporting, 0 contradicting, 1 mixed · N sources: 26


### Brand Heritage
_N claims: 1 · Mean posterior: 0.69 · Grade A/B: 1_

- **[BH-000002]** Nonprofit brand heritage increases donation intention through the formation of brand trust.  
  P = 0.69 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 26


### Brand Value
_N claims: 1 · Mean posterior: 0.69 · Grade A/B: 1_

- **[BV-000003]** Brand strength is an antecedent of brand value.  
  P = 0.69 · B (moderate) ⚠ conflict  
  EVIDs: 9 supporting, 1 contradicting, 2 mixed · N sources: 5


### Brand Meaning
_N claims: 1 · Mean posterior: 0.69 · Grade A/B: 1_

- **[BM-000005]** Brand Meaning positively predicts Brand Responses in the context of a nonprofit health-promotion brand.  
  P = 0.69 · B (moderate)  
  EVIDs: 6 supporting, 0 contradicting, 0 mixed · N sources: 31


### Resource Acquisition
_N claims: 1 · Mean posterior: 0.69 · Grade A/B: 1_

- **[RA-000001]** Higher nonprofit brand orientation is positively associated with stronger resource acquisition performance.  
  P = 0.69 · B (moderate)  
  EVIDs: 9 supporting, 0 contradicting, 1 mixed · N sources: 19


### Stakeholder Engagement
_N claims: 2 · Mean posterior: 0.68 · Grade A/B: 1_

- **[SE-000005]** Stakeholder engagement facilitated by social media platforms is a positive driver of fundraising success and stakeholder…  
  P = 0.81 · A (strong) ⚠ conflict  
  EVIDs: 4 supporting, 1 contradicting, 0 mixed · N sources: 29

- **[SE-000006]** For stakeholders with positive attitudes but perceived financial constraints, offering non-monetary engagement pathways …  
  P = 0.56 · C (mixed) ⚠ conflict  
  EVIDs: 4 supporting, 1 contradicting, 0 mixed · N sources: 29


### Expectations
_N claims: 3 · Mean posterior: 0.68 · Grade A/B: 3_

- **[E-000007]** Consumer expectations are updated through consumption experiences.  
  P = 0.84 · A (strong)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 24

- **[E-000005]** Post-consumption expectations have a stronger influence on behavioural intentions among low-familiarity consumers than a…  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 24

- **[E-000006]** The influence of pre-purchase expectations on satisfaction formation diminishes as brand familiarity increases.  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 24


### Information Costs
_N claims: 3 · Mean posterior: 0.68 · Grade A/B: 3_

- **[IC-000001]** Lower consumer information costs increase the expected utility associated with a branded offering.  
  P = 0.68 · B (moderate) ⚠ conflict  
  EVIDs: 6 supporting, 1 contradicting, 0 mixed · N sources: 4

- **[IC-000002]** Reductions in information costs function as antecedents of consumer-based brand equity rather than as consequences of it…  
  P = 0.68 · B (moderate) ⚠ conflict  
  EVIDs: 6 supporting, 1 contradicting, 0 mixed · N sources: 4

- **[IC-000003]** For jeans, the effect of brand credibility on expected utility is strongly mediated by information costs saved.  
  P = 0.68 · B (moderate) ⚠ conflict  
  EVIDs: 6 supporting, 1 contradicting, 0 mixed · N sources: 4


### Brand Management
_N claims: 4 · Mean posterior: 0.68 · Grade A/B: 4_

- **[BM-000003]** Measurements of brand strength and brand value can provide feedback for adjusting brand description and marketing mix de…  
  P = 0.72 · B (moderate)  
  EVIDs: 8 supporting, 0 contradicting, 1 mixed · N sources: 40

- **[BM-000007]** Sector-wide interventions aimed at increasing public confidence in nonprofits are likely ineffective if they do not firs…  
  P = 0.72 · B (moderate)  
  EVIDs: 8 supporting, 0 contradicting, 1 mixed · N sources: 40

- **[BM-000002]** Using brand value as a performance measure in brand management encourages a long-term strategic perspective.  
  P = 0.65 · B (moderate)  
  EVIDs: 8 supporting, 0 contradicting, 1 mixed · N sources: 40

- **[BM-000004]** Effective strategic brand management requires compatible terminology between marketing and accounting functions.  
  P = 0.65 · B (moderate)  
  EVIDs: 8 supporting, 0 contradicting, 1 mixed · N sources: 40


### Social Information
_N claims: 1 · Mean posterior: 0.68 · Grade A/B: 1_

- **[SI-000008]** Social information can have positive, null, or negative effects on donation amounts.  
  P = 0.68 · B (moderate) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 14


### Organizational Reputation
_N claims: 2 · Mean posterior: 0.68 · Grade A/B: 2_

- **[OR-000002]** Negative CEO reputation suppresses the influence of attitudes and moral norms on charitable donation intention.  
  P = 0.68 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 0 contradicting, 3 mixed · N sources: 56

- **[OR-000003]** Under negative CEO reputation, subjective norms and organizational identification become more salient predictors of char…  
  P = 0.68 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 0 contradicting, 3 mixed · N sources: 56


### Coping Planning
_N claims: 1 · Mean posterior: 0.68 · Grade A/B: 1_

- **[CP-000001]** Coping planning is a more significant mediator of the intention-behavior link than action planning in behavioral domains…  
  P = 0.68 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 2


### Market Share
_N claims: 1 · Mean posterior: 0.68 · Grade A/B: 1_

- **[MS-000002]** Market share can be a misleading indicator of brand health when it is increased through short-term tactics that erode lo…  
  P = 0.68 · B (moderate) ⚠ conflict  
  EVIDs: 6 supporting, 1 contradicting, 0 mixed · N sources: 2


### Brand Credibility
_N claims: 7 · Mean posterior: 0.68 · Grade A/B: 7_

- **[BC-000022]** An organisation’s perceived expertise and capability to deliver on its brand promise increases brand credibility.  
  P = 0.68 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 56

- **[BC-000034]** High brand credibility strengthens the positive relationship between donor brand loyalty and overall brand equity.  
  P = 0.68 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 56

- **[BC-000035]** High brand credibility establishes a positive relationship between perceived quality and brand equity that is otherwise …  
  P = 0.68 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 56

- **[BC-000036]** Brand credibility does not significantly moderate the positive relationship between brand awareness and brand equity.  
  P = 0.68 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 56

- **[BC-000037]** Brand credibility does not significantly moderate the positive relationship between brand association and brand equity.  
  P = 0.68 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 56

- **[BC-000038]** A nonprofit brand's perceived credibility reduces stakeholder uncertainty and increases the likelihood of resource provi…  
  P = 0.68 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 56

- **[BC-000042]** Brand credibility moderates the relationship between service quality and stakeholder behavioural outcomes.  
  P = 0.68 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 1 mixed · N sources: 56


### Attitude Toward the Charity
_N claims: 1 · Mean posterior: 0.68 · Grade A/B: 1_

- **[AT-000001]** A positive attitude toward a charity mediates the relationship between nonprofit brand perceptions and intention to dona…  
  P = 0.68 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 30


### Stakeholder Management
_N claims: 1 · Mean posterior: 0.68 · Grade A/B: 1_

- **[SM-000003]** Small nonprofits often fail to develop and integrate distinct marketing strategies for their volunteer constituency.  
  P = 0.68 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 10


### Social Media Marketing
_N claims: 3 · Mean posterior: 0.68 · Grade A/B: 3_

- **[SM-000001]** Nonprofit social media marketing influences donation intention through brand trust.  
  P = 0.68 · B (moderate) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 27

- **[SM-000004]** Nonprofits frequently use social media for one-way information dissemination rather than for two-way, dialogic communica…  
  P = 0.68 · B (moderate) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 27

- **[SM-000005]** The effectiveness of a nonprofit's social media strategy in generating engagement is positively related to the degree of…  
  P = 0.68 · B (moderate) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 27


### Behavioural Difficulty
_N claims: 1 · Mean posterior: 0.67 · Grade A/B: 1_

- **[BD-000003]** The predictive advantage of Brand Attachment over Brand Attitude Strength increases for behaviours requiring greater per…  
  P = 0.67 · B (moderate) ⚠ conflict  
  EVIDs: 3 supporting, 0 contradicting, 2 mixed · N sources: 1


### Donor Decision Involvement
_N claims: 2 · Mean posterior: 0.67 · Grade A/B: 2_

- **[DD-000005]** Donor decision involvement positively moderates the relationship between nonprofit brand attitude and new donor brand ch…  
  P = 0.67 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 7

- **[DD-000006]** The influence of nonprofit brand salience on new donor brand choice intention is stronger under low donor decision invol…  
  P = 0.67 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 7


### Source of Funds
_N claims: 1 · Mean posterior: 0.67 · Grade A/B: 1_

- **[SO-000001]** Donations made from earned income generate greater warm glow utility than donations made from windfall income.  
  P = 0.67 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 32


### Situational Salience
_N claims: 2 · Mean posterior: 0.67 · Grade A/B: 2_

- **[SS-000005]** The presence of cues providing social information about descriptive norms can causally alter actual donation behaviour.  
  P = 0.67 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 1 mixed · N sources: 12

- **[SS-000006]** The effect of situational cues on donation can differ for the decision to donate (extensive margin) versus the amount do…  
  P = 0.67 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 1 mixed · N sources: 12


### Brand Value Chain
_N claims: 2 · Mean posterior: 0.67 · Grade A/B: 1_

- **[BV-000006]** Brand value is created through a causal chain from marketing investment to customer mind-set, then to market performance…  
  P = 0.81 · A (strong)  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 4

- **[BV-000001]** Organisational marketing and communication investments build donor mindset, which in turn drives donation-related market…  
  P = 0.53 · C (mixed)  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 4


### Personal Norms
_N claims: 1 · Mean posterior: 0.67 · Grade A/B: 1_

- **[PN-000001]** Personal norms of moral obligation are a stronger predictor of a blood donor role-identity compared to a volunteer or fi…  
  P = 0.67 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 4


### Post-Intentional Friction
_N claims: 1 · Mean posterior: 0.67 · Grade A/B: 1_

- **[PI-000001]** Perceived practical barriers such as lack of time, limited resources, and required effort reduce the likelihood that don…  
  P = 0.67 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 20


### NPO Sustainability
_N claims: 1 · Mean posterior: 0.67 · Grade A/B: 1_

- **[NS-000001]** The long-term sustainability of a nonprofit organization is a function of its leadership, adaptability, and production c…  
  P = 0.67 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Strength
_N claims: 8 · Mean posterior: 0.67 · Grade A/B: 8_

- **[BS-000013]** Brand description is an antecedent of brand strength.  
  P = 0.67 · B (moderate) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 1 mixed · N sources: 29

- **[BS-000014]** High brand strength increases the probability of brand choice.  
  P = 0.67 · B (moderate) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 1 mixed · N sources: 29

- **[BS-000015]** High brand strength increases brand loyalty.  
  P = 0.67 · B (moderate) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 1 mixed · N sources: 29

- **[BS-000016]** High brand strength insulates a brand from competitive threats.  
  P = 0.67 · B (moderate) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 1 mixed · N sources: 29

- **[BS-000017]** High brand strength supports higher profit margins.  
  P = 0.67 · B (moderate) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 1 mixed · N sources: 29

- **[BS-000018]** High brand strength improves distribution access.  
  P = 0.67 · B (moderate) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 1 mixed · N sources: 29

- **[BS-000019]** High brand strength provides a platform for brand extensions.  
  P = 0.67 · B (moderate) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 1 mixed · N sources: 29

- **[BS-000009]** Brand strength is a potential positive antecedent of perceived brand authenticity understood as quintessential exemplari…  
  P = 0.60 · B (moderate) ⚠ conflict  
  EVIDs: 10 supporting, 1 contradicting, 1 mixed · N sources: 29


### Salience
_N claims: 1 · Mean posterior: 0.67 · Grade A/B: 1_

- **[S-000007]** Brand-related trust increases the salience of donation opportunities in the donor’s attentional landscape.  
  P = 0.67 · B (moderate) ⚠ conflict  
  EVIDs: 10 supporting, 0 contradicting, 2 mixed · N sources: 53


### Brand Identification
_N claims: 2 · Mean posterior: 0.67 · Grade A/B: 2_

- **[BI-000026]** Student identification with a university brand increases brand-supportive behaviours such as positive word-of-mouth, adv…  
  P = 0.67 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 1 mixed · N sources: 45

- **[BI-000051]** Donor identification with a nonprofit brand has a direct, positive effect on donation intention.  
  P = 0.67 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 1 mixed · N sources: 45


### Crisis Giving
_N claims: 1 · Mean posterior: 0.66 · Grade A/B: 1_

- **[CG-000002]** During the Covid-19 pandemic, donations were reallocated across causes rather than substantially increasing aggregate ch…  
  P = 0.66 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 20


### Mission Alignment
_N claims: 1 · Mean posterior: 0.66 · Grade A/B: 1_

- **[MA-000003]** International nonprofit brands are perceived as more legitimate when they are authentically linked to the organization’s…  
  P = 0.66 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 0 mixed · N sources: 19


### Self-Determination Theory
_N claims: 1 · Mean posterior: 0.66 · Grade A/B: 1_

- **[SD-000001]** An NPO's brand orientation behaviour functions as an extrinsic motivator that initiates a psychological process of motiv…  
  P = 0.66 · B (moderate) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 5


### Behaviour Architecture
_N claims: 1 · Mean posterior: 0.66 · Grade A/B: 1_

- **[BA-000070]** An effective Behaviour Architecture for an NPO must be based on a segmentation model that accounts for the complete port…  
  P = 0.66 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 21


### Warm Glow Utility
_N claims: 7 · Mean posterior: 0.66 · Grade A/B: 7_

- **[WG-000001]** A significant portion of charitable giving is motivated by the private, non-pecuniary utility an individual receives fro…  
  P = 0.70 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[WG-000006]** A significant portion of charitable giving is motivated by the private, non-pecuniary utility an individual receives fro…  
  P = 0.70 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[WG-000007]** Individuals donate even when their contribution has no marginal impact on the charity's total funds.  
  P = 0.70 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[WG-000002]** Individuals donate even when their contribution has no marginal effect on the charity’s total funds.  
  P = 0.62 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[WG-000003]** Donating personally earned funds generates greater warm glow utility than donating windfall funds.  
  P = 0.62 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[WG-000004]** Consumer skepticism negatively moderates the warm glow effect in cause-related marketing contexts.  
  P = 0.62 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[WG-000005]** The option to take resources from a charity reduces but does not eliminate warm glow giving.  
  P = 0.62 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Performance
_N claims: 4 · Mean posterior: 0.66 · Grade A/B: 4_

- **[BP-000017]** High-quality nonprofit service delivery increases stakeholder trust.  
  P = 0.66 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 1 contradicting, 1 mixed · N sources: 9

- **[BP-000018]** Transparent nonprofit communication increases stakeholder trust.  
  P = 0.66 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 1 contradicting, 1 mixed · N sources: 9

- **[BP-000019]** Brand performance mediates the relationship between nonprofit brand identity and nonprofit brand image.  
  P = 0.66 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 1 contradicting, 1 mixed · N sources: 9

- **[BP-000020]** Nonprofit brand performance consists of observable elements including service quality, communication, transparency, and …  
  P = 0.66 · B (moderate) ⚠ conflict  
  EVIDs: 8 supporting, 1 contradicting, 1 mixed · N sources: 9


### Resource Constraints
_N claims: 1 · Mean posterior: 0.65 · Grade A/B: 1_

- **[RC-000007]** The primary barriers to marketing implementation in small, local nonprofits are internal resource constraints, including…  
  P = 0.65 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 1 mixed · N sources: 91


### Brand Responses
_N claims: 1 · Mean posterior: 0.65 · Grade A/B: 1_

- **[BR-000012]** Brand Responses positively predict Brand Resonance in the context of a nonprofit health-promotion brand.  
  P = 0.65 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 1


### Static Brand Equity Indices
_N claims: 2 · Mean posterior: 0.65 · Grade A/B: 1_

- **[SB-000002]** Static brand equity models fail to represent causal pathways among brand equity dimensions.  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SB-000003]** Static brand equity indices are useful for high-level benchmarking when causal explanation is not the primary research o…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Platform Trust
_N claims: 1 · Mean posterior: 0.65 · Grade A/B: 1_

- **[PT-000001]** In digital donation contexts, trust in the technological platform positively predicts donation intention in addition to …  
  P = 0.65 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 27


### Brand Reputation
_N claims: 3 · Mean posterior: 0.65 · Grade A/B: 3_

- **[BR-000001]** Brand reputation helps stakeholders evaluate nonprofit organizations under conditions of uncertainty and incomplete info…  
  P = 0.65 · B (moderate) ⚠ conflict  
  EVIDs: 4 supporting, 1 contradicting, 1 mixed · N sources: 20

- **[BR-000014]** A strong brand reputation is a characteristic of a successful NPO.  
  P = 0.65 · B (moderate) ⚠ conflict  
  EVIDs: 4 supporting, 1 contradicting, 1 mixed · N sources: 20

- **[BR-000015]** An organization's reputation influences consumer perception of the fairness and sincerity of its social value initiative…  
  P = 0.65 · B (moderate) ⚠ conflict  
  EVIDs: 4 supporting, 1 contradicting, 1 mixed · N sources: 20


### Emotional Appeal
_N claims: 2 · Mean posterior: 0.65 · Grade A/B: 1_

- **[EA-000002]** Marketing communications that trigger psychological drivers such as empathy and altruism can increase support for social…  
  P = 0.79 · A (strong) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 1

- **[EA-000003]** The effect of emotional appeals on donation intentions is moderated by the congruence between the appeal's framing and t…  
  P = 0.51 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 1


### Brand Communication
_N claims: 2 · Mean posterior: 0.64 · Grade A/B: 2_

- **[BC-000021]** Internal and external communication of a brand’s defined meaning is required for shared understanding and stakeholder al…  
  P = 0.64 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 45

- **[BC-000040]** Public perception of nonprofits as 'Marketers' is linked to their use of corporate marketing language and competitive fr…  
  P = 0.64 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 45


### Value Co-Creation
_N claims: 1 · Mean posterior: 0.64 · Grade A/B: 1_

- **[VC-000005]** Social value is co-created with stakeholders rather than being unilaterally delivered by an organization.  
  P = 0.64 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 20


### Brand-Self Connection
_N claims: 1 · Mean posterior: 0.64 · Grade A/B: 1_

- **[BS-000008]** Brand–Self Connection captures the cognitive-emotional linkage between a brand and the consumer’s self-concept.  
  P = 0.64 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 1 mixed · N sources: 1


### Leadership
_N claims: 1 · Mean posterior: 0.64 · Grade A/B: 1_

- **[L-000005]** The effectiveness of an NPO's internal branding process is contingent on leadership style.  
  P = 0.64 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 16


### Accountability
_N claims: 1 · Mean posterior: 0.64 · Grade A/B: 1_

- **[A-000014]** The adoption of performance-based contracting in Austrian social services has increased the power of public funders rela…  
  P = 0.64 · B (moderate) ⚠ conflict  
  EVIDs: 4 supporting, 1 contradicting, 1 mixed · N sources: 7


### Brand Promise
_N claims: 1 · Mean posterior: 0.64 · Grade A/B: 1_

- **[BP-000023]** A brand functions as a public promise by an organisation regarding the performance and experience stakeholders can expec…  
  P = 0.64 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 0 mixed · N sources: 39


### CEO Reputation
_N claims: 1 · Mean posterior: 0.64 · Grade A/B: 1_

- **[CR-000002]** CEO reputation moderates the relationship between nonprofit brand perceptions and donation intention.  
  P = 0.64 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 1 mixed · N sources: 47


### Resource Provider Based Brand Equity
_N claims: 2 · Mean posterior: 0.64 · Grade A/B: 1_

- **[RP-000002]** In the nonprofit sector, brand-related perceptions are significantly associated with resource provider support intention…  
  P = 0.68 · B (moderate)  
  EVIDs: 7 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[RP-000001]** Resource provider based nonprofit brand equity can be conceptualised as a biased decision to support a nonprofit organis…  
  P = 0.60 · C (mixed)  
  EVIDs: 7 supporting, 0 contradicting, 0 mixed · N sources: 3


### Volunteer Choice
_N claims: 2 · Mean posterior: 0.63 · Grade A/B: 2_

- **[VC-000003]** Volunteer choice of a nonprofit brand is often automatic and non-compensatory when the brand is perceived as the categor…  
  P = 0.63 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 0 mixed · N sources: 5

- **[VC-000004]** A strong personal ("Mego") connection to a nonprofit or its cause triggers an automatic and non-compensatory volunteer c…  
  P = 0.63 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 0 mixed · N sources: 5


### Boundary Conditions
_N claims: 7 · Mean posterior: 0.63 · Grade A/B: 7_

- **[BC-000002]** Existing nonprofit brand equity models are primarily developed for individual donors or the general public rather than c…  
  P = 0.66 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 8 mixed · N sources: 112

- **[BC-000006]** Existing nonprofit brand equity models are primarily developed for individual donors or the general public rather than f…  
  P = 0.66 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 8 mixed · N sources: 112

- **[BC-000023]** The validity of the proposed nonprofit branding effectiveness model is bounded by the exclusion of government stakeholde…  
  P = 0.66 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 8 mixed · N sources: 112

- **[BC-000003]** Existing nonprofit brand equity theories are better suited to deliberative planned giving than to impulsive or emergency…  
  P = 0.61 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 8 mixed · N sources: 112

- **[BC-000004]** The relative importance of trust, identification, and brand personality may vary across cultural contexts.  
  P = 0.61 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 8 mixed · N sources: 112

- **[BC-000005]** Moral identification is more relevant for cause-based advocacy NGOs than for local service providers, hospitals, or arts…  
  P = 0.61 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 8 mixed · N sources: 112

- **[BC-000007]** Moral identification is more relevant for cause-based advocacy NGOs than for nonprofit organizations whose support depen…  
  P = 0.61 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 8 mixed · N sources: 112


### Brand Engagement
_N claims: 4 · Mean posterior: 0.63 · Grade A/B: 3_

- **[BE-000036]** Consumer engagement with brands can be differentiated into object-centered, self-centered, and social levels of psycholo…  
  P = 0.65 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 1 mixed · N sources: 6

- **[BE-000060]** A potential volunteer's level of Brand Engagement with a nonprofit determines their subsequent brand choice process (Bra…  
  P = 0.65 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 1 mixed · N sources: 6

- **[BE-000061]** High Brand Engagement ("Brand Wise") leads to an automatic, non-compensatory volunteer choice process where alternative …  
  P = 0.65 · B (moderate) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 1 mixed · N sources: 6

- **[BE-000038]** Consumer characteristics such as self-construal and general brand engagement tendency influence which level of brand eng…  
  P = 0.58 · C (mixed) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 1 mixed · N sources: 6


### Moral Identification
_N claims: 3 · Mean posterior: 0.63 · Grade A/B: 3_

- **[MI-000001]** Donors support cause-based NGOs partly because these brands allow them to express their own moral values and identity.  
  P = 0.63 · B (moderate) ⚠ conflict  
  EVIDs: 3 supporting, 0 contradicting, 3 mixed · N sources: 1

- **[MI-000003]** Donors support NGOs when the organization’s mission is congruent with their moral values and self-concept.  
  P = 0.63 · B (moderate) ⚠ conflict  
  EVIDs: 3 supporting, 0 contradicting, 3 mixed · N sources: 1

- **[MI-000004]** NGO brands enable donors to express moral values when the organisation’s mission is congruent with the donor’s self-conc…  
  P = 0.63 · B (moderate) ⚠ conflict  
  EVIDs: 3 supporting, 0 contradicting, 3 mixed · N sources: 1


### Brand Typicality
_N claims: 2 · Mean posterior: 0.63 · Grade A/B: 2_

- **[BT-000019]** The perceived typicality of a nonprofit brand is a stronger and more consistent predictor of the intention to donate tim…  
  P = 0.63 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 32

- **[BT-000020]** Brand typicality mediates the relationship between perceptions of a nonprofit's brand image and the intention to donate …  
  P = 0.63 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 32


### Interaction
_N claims: 1 · Mean posterior: 0.63 · Grade A/B: 1_

- **[I-000002]** Interaction enables nonprofit organisations to use stakeholder feedback to adapt value delivery to stakeholder needs.  
  P = 0.63 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 2


### Orchestration
_N claims: 1 · Mean posterior: 0.63 · Grade A/B: 1_

- **[O-000001]** Orchestration enables nonprofit organisations to deliver consistent brand messages to stakeholders through integrated ma…  
  P = 0.63 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 2


### Stakeholder Segmentation
_N claims: 1 · Mean posterior: 0.63 · Grade A/B: 1_

- **[SS-000007]** The population of monetary non-donors is not a homogeneous group and can be segmented into distinct clusters based on di…  
  P = 0.63 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 4


### Material Benefits
_N claims: 2 · Mean posterior: 0.62 · Grade A/B: 2_

- **[MB-000002]** The use of unconditional gifts or thank-you gifts as incentives does not reliably increase donations.  
  P = 0.62 · B (moderate) ⚠ thin-support, conflict  
  EVIDs: 0 supporting, 1 contradicting, 0 mixed · N sources: 1

- **[MB-000003]** Providing unconditional material benefits, such as thank-you gifts, can reduce subsequent donations.  
  P = 0.62 · B (moderate) ⚠ thin-support, conflict  
  EVIDs: 0 supporting, 1 contradicting, 0 mixed · N sources: 1


### Self-Image Enhancement
_N claims: 1 · Mean posterior: 0.62 · Grade A/B: 1_

- **[SI-000005]** Self-image motives primarily affect whether an individual participates in charitable giving.  
  P = 0.62 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Self-Image Motives
_N claims: 1 · Mean posterior: 0.62 · Grade A/B: 1_

- **[SI-000001]** Self-image motives primarily increase the likelihood that an individual participates in charitable giving.  
  P = 0.62 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Social Class
_N claims: 1 · Mean posterior: 0.62 · Grade A/B: 1_

- **[SC-000024]** The finding that individuals of higher social class are less generous has failed to replicate reliably.  
  P = 0.62 · B (moderate) ⚠ thin-support, conflict  
  EVIDs: 0 supporting, 1 contradicting, 0 mixed · N sources: 1


### Social-Image Management
_N claims: 2 · Mean posterior: 0.62 · Grade A/B: 2_

- **[SI-000006]** Social-image motives primarily affect the amount donated by individuals who have already decided to give.  
  P = 0.62 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SI-000007]** Observable charitable giving increases the relevance of social-image motives for donation behaviour.  
  P = 0.62 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Social-Image Motives
_N claims: 2 · Mean posterior: 0.62 · Grade A/B: 2_

- **[SI-000002]** Social-image motives primarily increase the amount donated among individuals who have already decided to give.  
  P = 0.62 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SI-000003]** Observable charitable giving generates social approval or prestige by signaling prosocial traits to others.  
  P = 0.62 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Warm Glow
_N claims: 1 · Mean posterior: 0.62 · Grade A/B: 1_

- **[WG-000008]** Fundraising appeals emphasizing donor-centric benefits (e.  
  P = 0.62 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Social Media Context
_N claims: 1 · Mean posterior: 0.62 · Grade A/B: 1_

- **[SM-000002]** Social media context moderates relationships between nonprofit brand-related variables and donation intention.  
  P = 0.62 · B (moderate) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 27


### Brand Association
_N claims: 1 · Mean posterior: 0.62 · Grade A/B: 1_

- **[BA-000069]** Donor-perceived brand association is positively associated with a charity brand's overall brand equity.  
  P = 0.62 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 15


### Trust Signals
_N claims: 2 · Mean posterior: 0.62 · Grade A/B: 2_

- **[TS-000001]** Formal charity labels are more influential for lesser-known nonprofits than for nonprofits with high pre-existing famili…  
  P = 0.62 · B (moderate) ⚠ conflict  
  EVIDs: 2 supporting, 0 contradicting, 2 mixed · N sources: 20

- **[TS-000002]** Formal trust labels are not universally decisive drivers of donation behaviour in Austria.  
  P = 0.62 · B (moderate) ⚠ conflict  
  EVIDs: 2 supporting, 0 contradicting, 2 mixed · N sources: 20


### Cultural Capital
_N claims: 2 · Mean posterior: 0.62 · Grade A/B: 1_

- **[CC-000010]** Empirical studies frequently lack consistent and valid operationalizations of key Bourdieusian concepts like cultural an…  
  P = 0.69 · B (moderate) ⚠ conflict  
  EVIDs: 3 supporting, 2 contradicting, 2 mixed · N sources: 11

- **[CC-000011]** The value of cultural and social capital in philanthropy is not fixed but is contingent on the specific structure and do…  
  P = 0.56 · C (mixed) ⚠ conflict  
  EVIDs: 3 supporting, 2 contradicting, 2 mixed · N sources: 11


### Involvement
_N claims: 1 · Mean posterior: 0.62 · Grade A/B: 1_

- **[I-000001]** Individual involvement moderates the effectiveness of norm-based charitable communication.  
  P = 0.62 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 1 mixed · N sources: 16


### Self-Regulation Failure
_N claims: 1 · Mean posterior: 0.62 · Grade A/B: 1_

- **[SR-000001]** Self-regulation failure reduces the likelihood that a charitable donation intention is translated into actual donation b…  
  P = 0.62 · B (moderate) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 20


### Brand Choice
_N claims: 1 · Mean posterior: 0.62 · Grade A/B: 1_

- **[BC-000043]** The choice of a specific nonprofit brand is guided by a 'taste' that reflects the supporter's habitus and class position…  
  P = 0.62 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 36


### Nonprofit Type
_N claims: 1 · Mean posterior: 0.62 · Grade A/B: 1_

- **[NT-000002]** Moral identification is more directly applicable to cause-based advocacy NGOs than to nonprofit organisations whose supp…  
  P = 0.62 · B (moderate) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 3


### Process-Based Brand Equity
_N claims: 3 · Mean posterior: 0.61 · Grade A/B: 1_

- **[PB-000006]** Process-based brand equity models predict willingness to pay a premium and repurchase intent better than static parallel…  
  P = 0.81 · A (strong) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1

- **[PB-000007]** Brand equity dimensions can operate as a causal sequence from brand building to consumer understanding to consumer-brand…  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1

- **[PB-000008]** Process-oriented brand equity models enable the diagnosis of breakdowns at specific stages of the brand-building process…  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Brand Name
_N claims: 1 · Mean posterior: 0.61 · Grade A/B: 1_

- **[BN-000001]** Brand name significantly influences consumer preference as a distinct attribute in multi-attribute choice contexts.  
  P = 0.61 · B (moderate) ⚠ conflict  
  EVIDs: 2 supporting, 0 contradicting, 2 mixed · N sources: 1


### Behavioural Inertia
_N claims: 1 · Mean posterior: 0.61 · Grade A/B: 1_

- **[BI-000053]** A significant portion of non-donation is characterized by a lack of conscious thought or activation rather than by activ…  
  P = 0.61 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 3


### Environmental Constraints
_N claims: 2 · Mean posterior: 0.61 · Grade A/B: 2_

- **[EC-000001]** Strong nonprofit brands can mitigate environmental constraints on donation behaviour by providing trusted and frictionle…  
  P = 0.61 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 31

- **[EC-000003]** Strong brand equity reduces perceived environmental constraints by making donation channels appear more efficient and ac…  
  P = 0.61 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 31


### Donor-Nonprofit Identification
_N claims: 3 · Mean posterior: 0.61 · Grade A/B: 3_

- **[DN-000002]** Donor-Nonprofit Identification and Donor Identity Salience are empirically distinct constructs in nonprofit donor behavi…  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 1

- **[DN-000003]** Donor-nonprofit identification directly and positively influences donor loyalty in nonprofit contexts.  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 1

- **[DN-000004]** Donor-nonprofit identification positively influences donor identity salience in nonprofit contexts.  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 1


### Equifinality
_N claims: 1 · Mean posterior: 0.61 · Grade A/B: 1_

- **[E-000003]** Multiple distinct configurations of antecedent brand conditions can produce high overall consumer-based brand equity.  
  P = 0.61 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 1


### Donor Orientation
_N claims: 2 · Mean posterior: 0.61 · Grade A/B: 2_

- **[DO-000001]** Donor orientation positively influences donor satisfaction in nonprofit contexts.  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 2

- **[DO-000002]** Donor orientation positively influences donor-nonprofit identification in nonprofit contexts.  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 2


### Brand Archetype
_N claims: 2 · Mean posterior: 0.61 · Grade A/B: 2_

- **[BA-000073]** Public perception of nonprofit brands is primarily structured by two opposing archetypes: the "Good Samaritan" (altruist…  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 2

- **[BA-000074]** The "Good Samaritan" archetype functions as the public's dominant normative ideal for nonprofit organisations.  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 2


### Injunctive Norms
_N claims: 1 · Mean posterior: 0.61 · Grade A/B: 1_

- **[IN-000001]** When both are measured, injunctive norms are a stronger and more consistent predictor of donation intention than descrip…  
  P = 0.61 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 1 mixed · N sources: 26


### Employee Buy-in
_N claims: 1 · Mean posterior: 0.60 · Grade A/B: 1_

- **[EB-000006]** Employee buy-in is perceived by senior marketing personnel in UK nonprofit organizations as critical for delivering the …  
  P = 0.60 · B (moderate)  
  EVIDs: 5 supporting, 0 contradicting, 0 mixed · N sources: 3


### Organizational Trust
_N claims: 1 · Mean posterior: 0.60 · Grade A/B: 1_

- **[OT-000001]** Organizational trust functions as an informational cue that reduces perceived risk in charitable donation decisions.  
  P = 0.60 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 29


### Expectation Management
_N claims: 2 · Mean posterior: 0.60 · Grade A/B: 2_

- **[EM-000001]** Positive disconfirmation between student expectations and actual university service experience strengthens student satis…  
  P = 0.60 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 2

- **[EM-000002]** A discrepancy between a university’s projected brand image and students’ experienced impression weakens brand management…  
  P = 0.60 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 2


### Volunteering Intention
_N claims: 1 · Mean posterior: 0.60 · Grade A/B: 1_

- **[VI-000001]** Positive perceptions of nonprofit brand image are associated with stronger intentions to donate time to the nonprofit or…  
  P = 0.60 · B (moderate)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 4


### Nonprofit Brand Equity Dynamics
_N claims: 1 · Mean posterior: 0.60 · Grade A/B: 1_

- **[NB-000100]** The relative influence of core brand equity drivers on donor behaviour changes systematically over multi-year periods.  
  P = 0.60 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Brand Value Chain
_N claims: 2 · Mean posterior: 0.60 · Grade A/B: 2_

- **[NB-000004]** In nonprofit contexts, brand-building investments shape stakeholder mindsets such as awareness, attitudes, and trust.  
  P = 0.60 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[NB-000005]** Stakeholder mindsets shaped by nonprofit brand-building investments influence supportive behaviours such as donations an…  
  P = 0.60 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Heuristic
_N claims: 2 · Mean posterior: 0.60 · Grade A/B: 0_

- **[BH-000001]** A strong brand can function as a heuristic that simplifies consumer decision-making.  
  P = 0.60 · C (mixed)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 2

- **[BH-000003]** A well-known and trusted nonprofit brand reduces the perceived risk and complexity of the donation decision.  
  P = 0.60 · C (mixed)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 2


### Context Dependency
_N claims: 5 · Mean posterior: 0.60 · Grade A/B: 0_

- **[CD-000001]** Cultural dimensions moderate the relative importance of brand equity blocks for behavioural outcomes.  
  P = 0.60 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 0 contradicting, 8 mixed · N sources: 45

- **[CD-000002]** Consumer price perception moderates the relationship between brand equity dimensions and purchase intention.  
  P = 0.60 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 0 contradicting, 8 mixed · N sources: 45

- **[CD-000003]** Customer demographics moderate the strength of the relationship between brand equity and behaviour.  
  P = 0.60 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 0 contradicting, 8 mixed · N sources: 45

- **[CD-000004]** Omnichannel integration quality alters the pathways between brand equity and behavioural outcomes.  
  P = 0.60 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 0 contradicting, 8 mixed · N sources: 45

- **[CD-000005]** Ecological consciousness alters the pathways between brand equity and behavioural outcomes.  
  P = 0.60 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 0 contradicting, 8 mixed · N sources: 45


### Brand Respect
_N claims: 1 · Mean posterior: 0.60 · Grade A/B: 0_

- **[BR-000002]** The perceived respectability of a nonprofit brand is positively associated with resource provider support intentions.  
  P = 0.60 · C (mixed)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 2


### Measurement Invariance
_N claims: 1 · Mean posterior: 0.60 · Grade A/B: 0_

- **[MI-000005]** Measurement invariance testing is required before consumer-based brand equity scores are compared across national sample…  
  P = 0.60 · C (mixed) ⚠ conflict  
  EVIDs: 7 supporting, 5 contradicting, 1 mixed · N sources: 46


### Jeffrey Conditionalization
_N claims: 1 · Mean posterior: 0.59 · Grade A/B: 0_

- **[JC-000001]** Gradual belief updating via Jeffrey Conditionalization is a more adequate formal model for integrating uncertain empiric…  
  P = 0.59 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Awareness
_N claims: 5 · Mean posterior: 0.59 · Grade A/B: 4_

- **[A-000009]** Public awareness of nonprofit organizations is a positive and significant predictor of public confidence in their perfor…  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 39

- **[A-000010]** An individual's top-of-mind awareness of nonprofit organizations is positively correlated with their level of education …  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 39

- **[A-000011]** Individuals identifying as White exhibit significantly higher top-of-mind awareness of nonprofit organizations compared …  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 39

- **[A-000013]** Employment in the nonprofit sector is not a significant predictor of an individual's top-of-mind awareness of nonprofit …  
  P = 0.61 · B (moderate)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 39

- **[A-000012]** Low public awareness of nonprofit organizations can act as a barrier to service utilization by potential beneficiaries.  
  P = 0.51 · C (mixed)  
  EVIDs: 3 supporting, 0 contradicting, 1 mixed · N sources: 39


### Charismatic Leadership
_N claims: 2 · Mean posterior: 0.59 · Grade A/B: 0_

- **[CL-000001]** Charismatic leadership strengthens the positive relationship between an NPO's brand orientation behaviour and staff's em…  
  P = 0.59 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 5

- **[CL-000002]** Charismatic leadership strengthens the positive relationship between staff's emotional brand attachment and their servic…  
  P = 0.59 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 5


### Brand Differentiation
_N claims: 9 · Mean posterior: 0.59 · Grade A/B: 2_

- **[BD-000006]** Greater perceived brand differentiation among competing nonprofits increases donor attraction and giving likelihood.  
  P = 0.73 · B (moderate) ⚠ conflict  
  EVIDs: 9 supporting, 2 contradicting, 0 mixed · N sources: 29

- **[BD-000014]** The direct effect of perceived brand differentiation on actual stakeholder donation behaviour is not sufficiently suppor…  
  P = 0.73 · B (moderate) ⚠ conflict  
  EVIDs: 9 supporting, 2 contradicting, 0 mixed · N sources: 29

- **[BD-000001]** The perceived differentiation of a nonprofit brand from competing organisations is positively associated with resource p…  
  P = 0.59 · C (mixed) ⚠ conflict  
  EVIDs: 9 supporting, 2 contradicting, 0 mixed · N sources: 29

- **[BD-000013]** Perceived brand differentiation of a nonprofit has a positive effect on stakeholders' intention to donate and their comm…  
  P = 0.59 · C (mixed) ⚠ conflict  
  EVIDs: 9 supporting, 2 contradicting, 0 mixed · N sources: 29

- **[BD-000002]** Declines in perceived brand differentiation can precede declines in other brand equity measures and market performance.  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 9 supporting, 2 contradicting, 0 mixed · N sources: 29

- **[BD-000005]** In the Y&R Brand Asset Valuator model, perceived differentiation must be established before relevance can be built.  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 9 supporting, 2 contradicting, 0 mixed · N sources: 29

- **[BD-000010]** The direct causal effect of perceived nonprofit brand uniqueness on subsequent observed donation behaviour is not curren…  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 9 supporting, 2 contradicting, 0 mixed · N sources: 29

- **[BD-000011]** Perceived brand differentiation has a positive and statistically significant direct effect on an individual's actual don…  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 9 supporting, 2 contradicting, 0 mixed · N sources: 29

- **[BD-000012]** The effect of perceived brand differentiation on actual donation behaviour is mediated by the individual's perceived eff…  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 9 supporting, 2 contradicting, 0 mixed · N sources: 29


### Brand-Enabled Behaviour
_N claims: 2 · Mean posterior: 0.59 · Grade A/B: 1_

- **[BE-000081]** A significant intention-behaviour gap exists in nonprofit brand research, with most studies measuring attitudinal or int…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BE-000064]** A strong nonprofit brand fosters future donation behavior by simultaneously (a) increasing relational commitment and (b)…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Stakeholder Perception
_N claims: 1 · Mean posterior: 0.59 · Grade A/B: 0_

- **[SP-000003]** Stakeholder groups differ in their ability to assess a nonprofit's brand orientation and performance, with donors exhibi…  
  P = 0.59 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 2


### Brand Recognition
_N claims: 1 · Mean posterior: 0.59 · Grade A/B: 0_

- **[BR-000011]** Low brand recognition is a primary marketing challenge for small nonprofits, limiting their stakeholder engagement.  
  P = 0.59 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 1 mixed · N sources: 21


### Brand Prominence
_N claims: 3 · Mean posterior: 0.58 · Grade A/B: 1_

- **[BP-000014]** Brand Prominence captures the salience and accessibility of brand-related thoughts and feelings.  
  P = 0.64 · B (moderate)  
  EVIDs: 4 supporting, 0 contradicting, 1 mixed · N sources: 1

- **[BP-000015]** Brand Prominence increases the accessibility of relationship-sustaining brand behaviours by making brand-related thought…  
  P = 0.56 · C (mixed)  
  EVIDs: 4 supporting, 0 contradicting, 1 mixed · N sources: 1

- **[BP-000016]** Brand Prominence is especially important when Brand–Self Connection is based on instrumentality rather than identity.  
  P = 0.56 · C (mixed)  
  EVIDs: 4 supporting, 0 contradicting, 1 mixed · N sources: 1


### Brand Description
_N claims: 1 · Mean posterior: 0.58 · Grade A/B: 0_

- **[BD-000004]** Marketing mix activities shape brand description by creating or modifying consumer associations and beliefs about a bran…  
  P = 0.58 · C (mixed) ⚠ conflict  
  EVIDs: 5 supporting, 1 contradicting, 0 mixed · N sources: 3


### Leadership Support
_N claims: 1 · Mean posterior: 0.58 · Grade A/B: 0_

- **[LS-000002]** Senior marketing personnel in UK nonprofit organizations identify leadership support as one of the most critical interna…  
  P = 0.58 · C (mixed)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 4


### Brand Scale
_N claims: 1 · Mean posterior: 0.58 · Grade A/B: 0_

- **[BS-000004]** The perceived scale of a nonprofit brand is positively associated with resource provider support intentions.  
  P = 0.58 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 1


### Service Quality
_N claims: 2 · Mean posterior: 0.58 · Grade A/B: 0_

- **[SQ-000001]** Perceived service quality is a strong, positive antecedent of stakeholder satisfaction in nonprofit service contexts.  
  P = 0.58 · C (mixed)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 2

- **[SQ-000002]** Improving the perceived quality of service delivery is an effective strategy for a nonprofit to increase donor loyalty.  
  P = 0.58 · C (mixed)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 2


### Cognitive Salience
_N claims: 1 · Mean posterior: 0.58 · Grade A/B: 0_

- **[CS-000001]** Heightened awareness of a charitable cause can trigger donation behavior among individuals without prior donation intent…  
  P = 0.58 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 20


### Emotional Activation
_N claims: 1 · Mean posterior: 0.58 · Grade A/B: 0_

- **[EA-000001]** Acute emotional responses such as empathy or guilt can trigger charitable donation behavior among individuals without pr…  
  P = 0.58 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 20


### Signalling Theory
_N claims: 1 · Mean posterior: 0.58 · Grade A/B: 0_

- **[ST-000001]** Stakeholder evaluation of nonprofit brand equity is a nonlinear function of its constituent signals, with signals exhibi…  
  P = 0.58 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 1 mixed · N sources: 14


### Perceived Efficiency
_N claims: 1 · Mean posterior: 0.57 · Grade A/B: 0_

- **[PE-000002]** Perceived operational efficiency does not have a significant positive effect on giving intention or giving behavior.  
  P = 0.57 · C (mixed)  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 2


### Past Donation Behaviour
_N claims: 1 · Mean posterior: 0.57 · Grade A/B: 0_

- **[PD-000001]** Past donation behaviour improves the explanation of future donation intention and future donation behaviour.  
  P = 0.57 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 27


### Moral Value Alignment
_N claims: 1 · Mean posterior: 0.57 · Grade A/B: 0_

- **[MV-000003]** Donors are more likely to support NGOs whose causes and moral objectives align with their personal values.  
  P = 0.57 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 2


### Organisational Associations
_N claims: 2 · Mean posterior: 0.57 · Grade A/B: 0_

- **[OA-000001]** Organizational associations are more important brand equity measures for services, durable goods, and corporate brands t…  
  P = 0.57 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1

- **[OA-000002]** Organisational associations can be empirically distinguished from perceived value and brand personality within a consume…  
  P = 0.57 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Perceived Brand Orientation
_N claims: 3 · Mean posterior: 0.57 · Grade A/B: 0_

- **[PB-000024]** A member's perception of a nonprofit organization's brand orientation has no significant direct effect on the personal b…  
  P = 0.57 · C (mixed) ⚠ conflict  
  EVIDs: 3 supporting, 1 contradicting, 0 mixed · N sources: 3

- **[PB-000025]** The relationship between a member's perception of a nonprofit's brand orientation and their perceived benefits is fully …  
  P = 0.57 · C (mixed) ⚠ conflict  
  EVIDs: 3 supporting, 1 contradicting, 0 mixed · N sources: 3

- **[PB-000026]** The strategic orientations of a nonprofit organization, specifically market orientation and brand orientation, can be co…  
  P = 0.57 · C (mixed) ⚠ conflict  
  EVIDs: 3 supporting, 1 contradicting, 0 mixed · N sources: 3


### B2B Brand Equity
_N claims: 1 · Mean posterior: 0.56 · Grade A/B: 0_

- **[BB-000001]** Brand equity models developed for consumer goods markets may not apply directly to B2B markets because factors such as p…  
  P = 0.56 · C (mixed) ⚠ conflict  
  EVIDs: 2 supporting, 1 contradicting, 0 mixed · N sources: 29


### Brand Equity Antecedents
_N claims: 1 · Mean posterior: 0.56 · Grade A/B: 0_

- **[BE-000035]** Brand image, brand awareness, and brand personality function as antecedents of brand equity in customer-based brand equi…  
  P = 0.56 · C (mixed) ⚠ conflict  
  EVIDs: 2 supporting, 0 contradicting, 2 mixed · N sources: 5


### Experiential Branding
_N claims: 3 · Mean posterior: 0.56 · Grade A/B: 0_

- **[EB-000007]** Nonprofit organizations use experiential, emotional, and reputational branding approaches as cost-effective alternatives…  
  P = 0.60 · C (mixed)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[EB-000008]** The translation of brand experience into actionable organizational programmes is a major implementation challenge for no…  
  P = 0.60 · C (mixed)  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 3

- **[EB-000002]** Nonprofit organizations are perceived as well suited to experiential and emotional branding because their missions and v…  
  P = 0.49 · C (mixed) ⚠ uncertain  
  EVIDs: 4 supporting, 0 contradicting, 0 mixed · N sources: 3


### Religious Giving
_N claims: 2 · Mean posterior: 0.56 · Grade A/B: 0_

- **[RG-000001]** Warm glow utility does not fully explain charitable giving in some religious contexts where duty or salvation motives ar…  
  P = 0.56 · C (mixed)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 33

- **[RG-000002]** Religious giving contexts can involve moral motivations such as duty or salvation that are not fully captured by the war…  
  P = 0.56 · C (mixed)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 33


### Asymmetry
_N claims: 1 · Mean posterior: 0.56 · Grade A/B: 0_

- **[A-000008]** The configurations of brand conditions that lead to high consumer-based brand equity are not the logical inverse of the …  
  P = 0.56 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Cultural Context
_N claims: 5 · Mean posterior: 0.56 · Grade A/B: 0_

- **[CC-000001]** Cultural dimensions such as individualism and collectivism moderate the relative importance of brand equity blocks and t…  
  P = 0.59 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 1 contradicting, 12 mixed · N sources: 147

- **[CC-000003]** Cultural context moderates the predictive salience of Theory of Planned Behavior constructs for charitable donation inte…  
  P = 0.59 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 1 contradicting, 12 mixed · N sources: 147

- **[CC-000002]** The predictive validity of standard intention-based donation models is moderated by cultural context.  
  P = 0.54 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 1 contradicting, 12 mixed · N sources: 147

- **[CC-000004]** In some non-Western charitable giving contexts, income and religiosity are more salient predictors than traditional Theo…  
  P = 0.54 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 1 contradicting, 12 mixed · N sources: 147

- **[CC-000007]** Cultural values can condition the generalizability of nonprofit brand equity findings.  
  P = 0.54 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 1 contradicting, 12 mixed · N sources: 147


### Brand_Equity
_N claims: 3 · Mean posterior: 0.56 · Grade A/B: 1_

- **[BE-000068]** The behavioural importance of brand equity as a heuristic for trust and efficacy increases under conditions of high unce…  
  P = 0.80 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BE-000067]** A nonprofit's brand serves as the institutional locus facilitating the conversion of a donor's economic capital into sym…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BE-000069]** A high-equity nonprofit brand can partially mitigate the identifiable victim effect, increasing stakeholder willingness …  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand as Heuristic
_N claims: 1 · Mean posterior: 0.56 · Grade A/B: 0_

- **[BA-000081]** For non-expert stakeholders, brand trust acts as a cognitive heuristic that substitutes for detailed evaluation of organ…  
  P = 0.56 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 14


### Brand Investments
_N claims: 1 · Mean posterior: 0.56 · Grade A/B: 0_

- **[BI-000034]** Brand investments increase brand signal credibility by signalling organisational commitment.  
  P = 0.56 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Marketing Mix Consistency
_N claims: 2 · Mean posterior: 0.56 · Grade A/B: 0_

- **[MM-000001]** Consistency of a firm’s marketing mix over time increases brand signal credibility.  
  P = 0.56 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1

- **[MM-000002]** Consistency of a firm’s marketing mix over time is a stronger driver of brand signal credibility than brand investments …  
  P = 0.56 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Signal Clarity
_N claims: 1 · Mean posterior: 0.56 · Grade A/B: 0_

- **[SC-000008]** Brand signal clarity increases brand signal credibility.  
  P = 0.56 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Self-Congruence
_N claims: 1 · Mean posterior: 0.56 · Grade A/B: 0_

- **[SC-000001]** Donors report higher donations to nonprofits whose brand personality is congruent with their actual or ideal self-concep…  
  P = 0.56 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 17


### Social Capital
_N claims: 1 · Mean posterior: 0.56 · Grade A/B: 0_

- **[SC-000003]** Higher nonprofit brand orientation is positively associated with greater generation of social capital.  
  P = 0.56 · C (mixed) ⚠ conflict  
  EVIDs: 4 supporting, 2 contradicting, 0 mixed · N sources: 16


### Motive Attribution
_N claims: 1 · Mean posterior: 0.55 · Grade A/B: 0_

- **[MA-000006]** Perceptions of a nonprofit brand as a "Marketer" are more strongly associated with attributions of self-serving motives …  
  P = 0.55 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 2


### Value Alignment
_N claims: 1 · Mean posterior: 0.55 · Grade A/B: 0_

- **[VA-000001]** The perceived value-alignment between a nonprofit and a for-profit brand moderates the success of cross-sector partnersh…  
  P = 0.55 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 10


### Hierarchy of Effects
_N claims: 1 · Mean posterior: 0.55 · Grade A/B: 0_

- **[HO-000002]** Public perception of nonprofits follows a sequential process where cognitive awareness precedes the formation of affecti…  
  P = 0.55 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 3


### Situational Cues
_N claims: 1 · Mean posterior: 0.55 · Grade A/B: 0_

- **[SC-000017]** Situational cues indicating social observation, such as eye images, increase the amount of money donated in public setti…  
  P = 0.55 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Associative Network Memory
_N claims: 1 · Mean posterior: 0.55 · Grade A/B: 0_

- **[AN-000001]** Brand awareness creates a memory node, and brand associations build a network of meanings around that node.  
  P = 0.55 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 16


### Donor Self-Identification
_N claims: 1 · Mean posterior: 0.55 · Grade A/B: 0_

- **[DS-000001]** Donor self-identification with an NGO’s cause strengthens donation intention.  
  P = 0.55 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 1


### Brand Consistency
_N claims: 1 · Mean posterior: 0.54 · Grade A/B: 0_

- **[BC-000024]** Consistency, clarity, and convergence across marketing activities increase brand equity strength.  
  P = 0.54 · C (mixed)  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 1


### Policy Impact
_N claims: 1 · Mean posterior: 0.54 · Grade A/B: 0_

- **[PI-000003]** Higher nonprofit brand orientation is positively associated with greater nonprofit policy impact.  
  P = 0.54 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 1


### Cause Commitment
_N claims: 1 · Mean posterior: 0.54 · Grade A/B: 0_

- **[CC-000006]** Donor loyalty in NGO contexts can be directed toward the underlying cause rather than toward a single NGO brand.  
  P = 0.54 · C (mixed)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 2


### Strategic Planning
_N claims: 1 · Mean posterior: 0.54 · Grade A/B: 0_

- **[SP-000002]** The presence of a formal strategic plan in a nonprofit organization is a positive predictor of the presence of a long-te…  
  P = 0.54 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 4


### Donation Channel
_N claims: 2 · Mean posterior: 0.54 · Grade A/B: 0_

- **[DC-000002]** In online crowdfunding donation contexts, social presence and platform trust become important predictors of donation int…  
  P = 0.54 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1

- **[DC-000003]** Traditional subjective norms are weaker predictors of money donation intention in online donation contexts than in some …  
  P = 0.54 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Price Perception
_N claims: 2 · Mean posterior: 0.54 · Grade A/B: 0_

- **[PP-000001]** Consumer price perception moderates the relationship between brand equity dimensions and purchase intention.  
  P = 0.54 · C (mixed) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 3 mixed · N sources: 39

- **[PP-000002]** Price perception moderates relationships within integrated Customer-Based Brand Equity and Theory of Planned Behavior mo…  
  P = 0.54 · C (mixed) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 3 mixed · N sources: 39


### Perceived Benefits
_N claims: 3 · Mean posterior: 0.53 · Grade A/B: 0_

- **[PB-000020]** Perceived familial benefit from a donation has a significant positive effect on giving intention.  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 2 supporting, 1 contradicting, 0 mixed · N sources: 3

- **[PB-000021]** Perceived familial benefit from a donation does not have a significant direct effect on actual giving behavior.  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 2 supporting, 1 contradicting, 0 mixed · N sources: 3

- **[PB-000022]** Perceived demonstrable and emotional benefits do not have a significant effect on giving intention or giving behavior.  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 2 supporting, 1 contradicting, 0 mixed · N sources: 3


### Brand Valuation
_N claims: 2 · Mean posterior: 0.53 · Grade A/B: 0_

- **[BV-000004]** Nonprofit brand valuation is used to estimate a brand’s capacity to mobilize financial resources and strengthen leverage…  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 3 supporting, 2 contradicting, 0 mixed · N sources: 29

- **[BV-000005]** Existing nonprofit brand valuation methods do not adequately capture non-financial behaviours such as volunteering, advo…  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 3 supporting, 2 contradicting, 0 mixed · N sources: 29


### Donor Involvement
_N claims: 1 · Mean posterior: 0.53 · Grade A/B: 0_

- **[DI-000001]** Donor involvement level moderates which nonprofit brand cues influence supportive behavioural intention.  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 2 supporting, 1 contradicting, 0 mixed · N sources: 36


### Choice Architecture
_N claims: 1 · Mean posterior: 0.53 · Grade A/B: 0_

- **[CA-000002]** The availability of an option to take resources from a charity reduces but does not eliminate warm glow giving.  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 32


### Perceived Inequality
_N claims: 1 · Mean posterior: 0.53 · Grade A/B: 0_

- **[PI-000002]** Perceived income inequality has no direct effect on charitable giving in Austria and Germany.  
  P = 0.53 · C (mixed) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 20


### Brand Equity Structure
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[BE-000033]** The structural form of nonprofit brand equity is not sufficiently established in the reviewed literature.  
  P = 0.52 · C (mixed)  
  EVIDs: 1 supporting, 0 contradicting, 1 mixed · N sources: 85


### BEBA
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[B-000002]** The effectiveness of a brand-enabled behaviour architecture is contingent on the attitudinal and resource-based characte…  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 17


### Managerial Experience
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[ME-000001]** Senior managers' brand-related experience is positively associated with the adoption of nonprofit brand orientation.  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Managerial Skills
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[MS-000003]** Senior managers' communication and managerial skills are positively associated with the adoption of nonprofit brand orie…  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Managerial Vision
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[MV-000004]** Senior managers' personal vision is positively associated with the adoption of nonprofit brand orientation.  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Measurement Adaptation
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[MA-000002]** General brand equity measures require adaptation to the specific brand, product category, and market context to remain v…  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Loyalty Segmentation
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[LS-000001]** Brand equity measures are more sensitive and interpretable when analyzed separately for loyalty segments than when analy…  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Demographic Factors
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[DF-000001]** Demographic factors moderate relationships within integrated Customer-Based Brand Equity and Theory of Planned Behavior …  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 21


### Income
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[I-000003]** Household income moderates new donor brand choice pathways such that high-income donors rely more strongly on brand atti…  
  P = 0.52 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 1 contradicting, 1 mixed · N sources: 46


### Donation Context
_N claims: 3 · Mean posterior: 0.52 · Grade A/B: 0_

- **[DC-000001]** The relative influence of nonprofit brand equity dimensions on donation intention varies across donation contexts.  
  P = 0.52 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 1 contradicting, 2 mixed · N sources: 65

- **[DC-000005]** Identification-based constructs have a stronger total effect on donor loyalty than satisfaction in the money donation co…  
  P = 0.52 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 1 contradicting, 2 mixed · N sources: 65

- **[DC-000006]** Donor satisfaction has a stronger effect on donor loyalty than identification-based constructs in the blood donation con…  
  P = 0.52 · C (mixed) ⚠ conflict  
  EVIDs: 1 supporting, 1 contradicting, 2 mixed · N sources: 65


### Donor Demographics
_N claims: 2 · Mean posterior: 0.52 · Grade A/B: 0_

- **[DD-000003]** The effect of donor identity salience on donor loyalty is stronger for older donors in the money donation context studie…  
  P = 0.52 · C (mixed) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 1

- **[DD-000004]** The effects of satisfaction and identification on donor loyalty are stronger for older donors and higher-income donors i…  
  P = 0.52 · C (mixed) ⚠ conflict  
  EVIDs: 0 supporting, 0 contradicting, 2 mixed · N sources: 1


### Ecological Consciousness
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[EC-000002]** A consumer's level of ecological consciousness alters the pathways and strength of brand-equity effects.  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 22


### Omnichannel Integration
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[OI-000001]** Integration quality in an omnichannel environment alters the pathways and strength of brand-equity effects.  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 22


### Brand Co-Creation
_N claims: 1 · Mean posterior: 0.52 · Grade A/B: 0_

- **[BC-000033]** The co-creation of nonprofit brand equity is facilitated when internal stakeholders transition to become members of the …  
  P = 0.52 · C (mixed) ⚠ thin-support  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Materialistic Attitude
_N claims: 1 · Mean posterior: 0.51 · Grade A/B: 0_

- **[MA-000001]** Materialistic attitude moderates the influence of a corporate brand on donation intention.  
  P = 0.51 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 27


### Moral Capital
_N claims: 1 · Mean posterior: 0.51 · Grade A/B: 0_

- **[MC-000002]** NGOs are differentiated from other nonprofit organizations by donors’ heightened demand for moral capital.  
  P = 0.51 · C (mixed)  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 1


### Brand Leadership
_N claims: 2 · Mean posterior: 0.51 · Grade A/B: 0_

- **[BL-000003]** Brand leadership captures perceptions that a brand is leading, innovative, and growing in popularity.  
  P = 0.51 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 1

- **[BL-000004]** Brand leadership can reveal market dynamics that are not captured by perceived quality alone.  
  P = 0.51 · C (mixed)  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 1


### Brand Narrative
_N claims: 1 · Mean posterior: 0.51 · Grade A/B: 0_

- **[BN-000003]** A coherent brand narrative that integrates an organization's past, present, and future is a primary mechanism for buildi…  
  P = 0.51 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 1


### Communication Framing
_N claims: 1 · Mean posterior: 0.51 · Grade A/B: 0_

- **[CF-000001]** The effect of injunctive norm appeals on charitable donation responses is moderated by audience involvement and pre-exis…  
  P = 0.51 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 1


### Brand Activism
_N claims: 1 · Mean posterior: 0.51 · Grade A/B: 0_

- **[BA-000076]** The impact of a nonprofit's sociopolitical advocacy on its brand equity is contingent on stakeholders' perception of the…  
  P = 0.51 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 14


### Brand Culture
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BC-000020]** Cultural resistance and staff cynicism impede the implementation of branding in nonprofit organizations.  
  P = 0.50 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 1


### Price Premium
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[PP-000003]** The price premium a customer is willing to pay for a brand over a competitor reflects the combined influence of multiple…  
  P = 0.50 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 13

- **[PP-000005]** High-equity brands can command larger price margins than low-equity brands.  
  P = 0.50 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 13


### Brand Equity Index
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BE-000041]** A single summary brand equity score requires unresolved decisions about construct inclusion, construct weighting, and ag…  
  P = 0.50 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 1


### Dynamic Feedback
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[DF-000002]** The reviewed brand-behaviour models primarily specify unidirectional paths from brand constructs to intention and behavi…  
  P = 0.50 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 14


### Actual Donation Behavior
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[AD-000001]** Boenigk and Helmig’s structural model explains only 4–5% of the variance in actual donation behavior.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Advocacy Brand Architecture
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[AB-000002]** Advocacy nonprofit brands tend to rely on proactive and cerebral communication strategies that tightly link the brand to…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Attitude toward Charity
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[AT-000004]** Stakeholder attitude toward the charity mediates the positive effect of brand orientation on donation intention.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### BEBA Methodological Framework
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BM-000008]** The synthesis of Bayesian epistemology, the ETO workflow, and knowledge graph representation constitutes a novel and coh…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### BEBA Research Design
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BR-000019]** A research design that integrates Bayesian evidence aggregation, a structured ETO workflow, and a knowledge graph repres…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BR-000020]** The BEBA research design provides a practical application of the semantic view of scientific theories, where the ETO wor…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Behavioural Constraint
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BC-000019]** The effect of donor loyalty on actual donation behavior can become non-significant when physical or regulatory ceilings …  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Behavioural Enablement
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BE-000078]** A Brand-Enabled Behaviour Architecture influences stakeholder behaviour through two distinct pathways: a pre-reflexive, …  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Behavioural Feedback Loop
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BF-000015]** The act of donating to a nonprofit organization positively reinforces the donor's perception of brand equity, an effect …  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Behavioural Types
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BT-000024]** The antecedent model for donating time is more similar to the model for donating money than either is to the model for d…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Authenticity Measurement
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BA-000049]** A valid measurement scale for brand authenticity should measure perceived category exemplarity rather than multiple hete…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Awareness Measurement
_N claims: 4 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BA-000057]** Brand awareness measures are most interchangeable for medium market-share brands and least interchangeable for small and…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BA-000058]** Changes in a brand’s more volatile awareness measure may reflect random noise rather than systematic brand-performance c…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BA-000059]** The optimal awareness metric for a global brand differs across national markets when the brand’s market share differs ac…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BA-000060]** Tracking the most stable awareness measure can provide a more reliable indicator of meaningful brand change than trackin…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Connection
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BC-000012]** Object-centered brand engagement is associated with brand attitude, self-centered brand engagement is associated with br…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Differentiation; Self-Concept Congruence; Donation Intention
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BD-000007]** The relationship between perceived nonprofit brand differentiation and donation intention is mediated by donor-brand sel…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Differentiation; Situational Salience; Donation Behavior
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BD-000008]** The effect of perceived brand differentiation on the probability of donation is positively moderated by situational sali…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Architecture
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BE-000007]** Brand equity operates through interconnected blocks of brand building, brand understanding, and brand relationship rathe…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Assets
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BE-000016]** Aaker's brand equity model treats loyalty, awareness, perceived quality, and associations as assets linked to a brand's …  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Components
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BE-000020]** Customer-based brand equity models differ in their specified dimensions, with Aaker emphasising loyalty, awareness, perc…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Creation Process
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BE-000025]** The brand equity creation process consists of three causally related sub-systems: Brand Building, Brand Understanding, a…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Dynamics
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BE-000042]** The reviewed nonprofit brand equity models are largely static and do not model how support experiences feed back into br…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Integration
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BE-000019]** The brand equity literature has not integrated financial and customer-based perspectives into a single coherent model.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Measurement Standardisation
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BE-000009]** Lack of standardized components and measures across brand equity process models hinders comparison and meta-analysis acr…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Pyramid
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BE-000056]** The sequential, hierarchical structure of the brand equity pyramid (Identity → Meaning → Responses → Resonance) is a val…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BE-000057]** The positive effect of Brand Identity on Brand Resonance is fully mediated by the intermediate stages of Brand Meaning a…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Research Gap
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BE-000021]** The connection between digital signals such as search volume or social media sentiment and theory-driven brand equity di…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Infrastructure Failure
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BI-000017]** Staff cynicism and lack of shared brand understanding are perceived barriers to effective nonprofit brand implementation…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Knowledge Network
_N claims: 3 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BK-000001]** Brand equity is represented in consumer memory as a network of brand knowledge associations.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BK-000002]** The strength, density, and configuration of brand associations influence consumer responses to a brand.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BK-000003]** Brand stimuli activate specific patterns within consumers’ brand knowledge networks.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Knowledge Structure
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BK-000009]** The constructs of brand awareness and brand associations, as measured by standard survey items based on Aaker (1991), la…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BK-000010]** The empirical lack of discriminant validity between brand awareness and brand associations stems from a conceptual depen…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Name as Heuristic
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BN-000002]** The relative importance of brand name as a determinant of consumer preference is greater in low-involvement product cate…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Recovery
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BR-000008]** Effective recovery from perceived breaches of a brand promise safeguards organisational reputation and long-term brand e…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Research Integration
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BR-000007]** Brand research has generated many domain-specific constructs without adequately specifying how those constructs relate w…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Signaling
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BS-000021]** In the Austrian context, the effectiveness of third-party charity labels is greater for lesser-known nonprofit organizat…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Signalling
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BS-000005]** Nonprofit brands function as signals of reliability, trustworthiness, and impact for potential donors.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BS-000006]** Brand signals reduce information asymmetry in charitable giving contexts.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Signification
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BS-000007]** Brands can function as informational cues, identity signals, and cultural symbols.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Vision
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BV-000002]** Senior marketing personnel in UK nonprofit organizations identify a clear organizational vision as one of the most criti…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Branding Philosophy
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[BP-000021]** A holistic branding approach treats the brand as the central focus for coordinating the marketing mix.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BP-000022]** A product-plus branding approach treats branding as an addition to a product.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Charitable Giving as Credence Good
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[CG-000005]** Charitable giving involves substantial donor uncertainty because donors cannot fully verify how contributions are used o…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Co-creation
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[CC-000008]** Brand strategies that are co-created with key stakeholders are more robust and effective than those developed solely by …  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Cognitive Efficiency
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[CE-000001]** Brands reduce search costs and simplify customer decision-making.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Competitive Nonprofit Environment
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[CN-000001]** Nonprofit organisations increasingly face competition for financial resources and volunteers.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Computational Brand Modelling
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[CB-000001]** Computational and neurocognitive methods reveal that brand knowledge is multi-process and networked.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Construct Redundancy
_N claims: 3 · Mean posterior: 0.50 · Grade A/B: 0_

- **[CR-000003]** Brand respect and brand differentiation in the Faircloth model lack discriminant validity in the Austrian nonprofit cont…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[CR-000004]** The Romero et al.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[CR-000005]** The Romero et al.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Crisis Resilience
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[CR-000007]** The 2008 financial crisis was associated with an increase in market concentration within the Austrian social services su…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[CR-000008]** The corporatist state-nonprofit partnership acts as a stabilizing financial and institutional force for affiliated nonpr…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Cultural and Economic Context
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[CA-000001]** The relative predictive strength of attitude, subjective norms, and Perceived Behavioral Control varies across cultural,…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Decision Making Theory
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[DM-000002]** High-involvement decisions, such as choosing a regular volunteer role, do not necessarily entail a complex, rational, or…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Demographic Moderation
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[DM-000001]** Customer demographics moderate the strength of the relationship between brand equity and behavior.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Digital Brand Presence
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[DB-000001]** The perceived quality of a nonprofit's digital presence influences donation intention by shaping brand image and brand t…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Digital Engagement
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[DE-000001]** The effectiveness of digital communication in building nonprofit brand equity is contingent on its use for fostering eng…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Donation Type
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[DT-000002]** The psychological antecedents for donating time differ systematically from the antecedents for donating money.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Donor Decision Models
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[DD-000001]** Early charitable giving models explain giving primarily through donor-centric psychological processes.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Donor Dispositions
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[DD-000002]** Dispositional factors such as empathy and trust influence cause choice more strongly than the level of charitable giving…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Donor Identity Salience
_N claims: 6 · Mean posterior: 0.50 · Grade A/B: 0_

- **[DI-000006]** Donor identity salience directly and positively influences donor loyalty in nonprofit contexts.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DI-000007]** Donor identity salience does not significantly moderate the relationship between donor-nonprofit identification and dono…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DI-000009]** An increase in the salience of a specific "donor" identity is positively associated with an individual's intention to pe…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DI-000010]** Behavior-specific identity salience is a stronger predictor of corresponding prosocial behavior than general prosocial i…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DI-000011]** Externally priming a relevant donor identity at the point of decision increases giving behavior.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DI-000012]** Donor identity salience mediates the relationship between past relationship satisfaction and future prosocial intentions…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Donor Segmentation
_N claims: 3 · Mean posterior: 0.50 · Grade A/B: 0_

- **[DS-000004]** The population of nonprofit supporters is not a single group but is composed of distinct behavioural segments, including…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DS-000005]** Individuals who engage in multiple forms of donation (e.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DS-000006]** Analysing different pro-social behaviours (e.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### ETO Methodology
_N claims: 4 · Mean posterior: 0.50 · Grade A/B: 0_

- **[EM-000003]** Bayesian evidence synthesis provides a more coherent epistemological foundation for cumulative social science than NHST-…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[EM-000004]** The Evidence-Theory-Ontology (ETO) pipeline provides a transparent, replicable, and traceable methodology for converting…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[EM-000005]** A middle-range theory-building stage is a necessary intermediary step to bridge quantitative statistical evidence and fo…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[EM-000006]** Formalising a social science theory as a computational ontology transforms it from a static narrative into a dynamic, ve…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Effective_Altruism
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[EA-000004]** Giving can be motivated by the rational, impartial goal of maximizing positive outcomes based on evidence.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Emotional Brand Attachment
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[EB-000009]** The development of staff emotional brand attachment is a direct antecedent of staff service involvement in the nonprofit…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Employer Brand
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[EB-000003]** A university’s employer brand is positively associated with employee commitment.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[EB-000004]** A university’s employer brand is positively associated with employee retention.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Giving Ecosystem
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[GE-000001]** Contemporary charitable giving frameworks account for micro-, meso-, and macro-level influences on giving behaviour.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Global Brand Consistency
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[GB-000001]** Efforts to implement a consistent global nonprofit brand can create conflict between headquarters and decentralized coun…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Goods and Services Delivery
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[GA-000001]** Higher nonprofit brand orientation is positively associated with more effective delivery of goods and services.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Incentive Moderation
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[IM-000001]** Extrinsic monetary incentives weaken the positive effect of nonprofit brand personality on donation intention.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Knowledge Graph Representation
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[KG-000002]** Representing a developing social science theory as a knowledge graph provides a more precise, communicable, and extensib…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Leadership-Driven Value Translation
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[LD-000003]** Senior leadership support is perceived as necessary for translating nonprofit brand values from abstract mission stateme…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Mediating Constructs
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[MC-000001]** The relationship between brand-building activities and behavioural outcomes is mediated by cognitive and relational bran…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Moral_Duty
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[MD-000001]** Charitable giving can be motivated by the fulfillment of a moral duty, independent of a calculation of its consequences.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Nonprofit Organization Type
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[NO-000001]** Treating foundations, charities, and NGOs as a single NPO category obscures theoretically relevant differences in nonpro…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Organisational Cohesion
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[OC-000001]** Organisational cohesion improves a nonprofit organisation’s capacity to use resources efficiently.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[OC-000002]** In decentralized international nonprofits, the brand provides a shared identity that supports internal cohesion across s…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Organisational Identification
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[OI-000002]** The positive effect of organisational identification on donor loyalty is comparable in magnitude to the direct positive …  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Organisational Performance
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[OP-000001]** Higher nonprofit brand orientation is positively associated with higher organisational performance.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Organisational Professionalism
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[OP-000002]** An NPO's level of professionalization is positively associated with its reliance on public funding sources.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[OP-000003]** An NPO's level of professionalization is negatively associated with its reliance on individual donations.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Organisational Reputation
_N claims: 4 · Mean posterior: 0.50 · Grade A/B: 0_

- **[OR-000001]** Negative organizational reputation weakens the positive effect of nonprofit brand factors on donation intention.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[OR-000004]** Organisational reputation moderates the predictors of donation intention.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[OR-000005]** A nonprofit organization's perceived reputation is a positive and significant predictor of an individual's willingness t…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[OR-000006]** The positive effect of a nonprofit's reputation on volunteer retention is mediated by the feeling of organizational prid…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Perceived Effectiveness
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[PE-000001]** Perceived operational effectiveness has a significant positive effect on both giving intention and giving behavior.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Perceived Organisational Support
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[PO-000001]** Perceived organisational support from a nonprofit is a positive predictor of volunteer retention.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Philanthropy_as_Power
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[PA-000002]** Large-scale philanthropy functions as a private exercise of power that influences public policy outside of democratic pr…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[PA-000003]** The critique of philanthropy as a threat to democracy is primarily applicable to large-scale, agenda-setting donors and …  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Product Quality
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[PQ-000008]** Brand-building cannot compensate for an offering that fails to deliver the brand promise.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Product Type
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[PT-000002]** The relative importance of brand equity mechanisms differs between product categories.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Relational Commitment
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[RC-000009]** Relational constructs, including trust and commitment, have greater predictive power for ongoing giving behaviour than p…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Relational Development
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[RD-000001]** Initial nonprofit brand awareness and positive brand image foster donor trust.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[RD-000002]** Donor trust fosters donor commitment.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Relief Brand Architecture
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[RB-000004]** Relief and development nonprofit brands tend to rely on reactive and emotional communication strategies.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Resource Mobilisation
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[RM-000001]** Strong nonprofit brands improve an international nonprofit organization’s ability to mobilize financial, human, and rela…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Resource-Constrained Branding
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[RC-000006]** Senior marketing personnel in UK nonprofit organizations do not perceive limited marketing budgets as a major impediment…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Retailer Brand Equity
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[RB-000002]** Retailer brand equity requires construct specifications that account for retail-specific factors such as in-store experi…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Social Expectations
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[SE-000004]** Perceived social expectations have a stronger effect on past volunteering of time compared to past donations of blood or…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Social_Obligation
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[SO-000002]** Acts of giving create social bonds and implicit obligations of reciprocity between the giver and the recipient or commun…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Sponsorship Fit
_N claims: 6 · Mean posterior: 0.50 · Grade A/B: 0_

- **[SF-000001]** High perceived fit between a nonprofit and a for-profit sponsor strengthens the nonprofit's brand equity.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SF-000002]** Low perceived fit between a nonprofit and a for-profit sponsor weakens or dilutes the nonprofit's brand equity.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SF-000003]** The effect of sponsor-nonprofit fit on nonprofit brand equity is mediated by cognitive consistency.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SF-000004]** The brand equity damage from a low-fit sponsorship primarily impacts abstract, trust-related brand associations like sin…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SF-000005]** High perceived fit between a sponsor and a nonprofit positively influences stakeholder behavioural intentions, including…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SF-000006]** Strategic communication providing a plausible rationale for a low-fit sponsorship ("created fit") can mitigate negative …  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Stakeholder Complexity
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[SC-000009]** Nonprofit organisations engage with a more diverse set of stakeholders than typical for-profit firms.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SC-000010]** International nonprofit brands must address a broader set of stakeholders than typical for-profit brands, including dono…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Stakeholder-Specific Brand Equity
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[SS-000001]** The definition and measurement of brand equity depend on the stakeholder group being studied.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Supportive Behaviour Type
_N claims: 1 · Mean posterior: 0.50 · Grade A/B: 0_

- **[SB-000001]** The relative importance of nonprofit brand dimensions differs between monetary donation and volunteering.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Volunteer Brand Equity (VBE)
_N claims: 2 · Mean posterior: 0.50 · Grade A/B: 0_

- **[VB-000003]** The conceptual dimensions of Employee Brand Equity (EBE) are applicable to formal volunteers in nonprofit organizations …  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[VB-000004]** Volunteer Role Clarity and Brand Commitment mediate the relationship between internal brand management practices and bra…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Trustworthiness
_N claims: 2 · Mean posterior: 0.49 · Grade A/B: 0_

- **[T-000001]** Perceived trustworthiness is not a significant predictor of propensity to donate when familiarity is accounted for in Ka…  
  P = 0.49 · C (mixed) ⚠ conflict, uncertain  
  EVIDs: 1 supporting, 1 contradicting, 0 mixed · N sources: 19

- **[T-000003]** A high level of perceived trustworthiness is a characteristic of a successful NPO.  
  P = 0.49 · C (mixed) ⚠ conflict, uncertain  
  EVIDs: 1 supporting, 1 contradicting, 0 mixed · N sources: 19


### Context Dependence
_N claims: 1 · Mean posterior: 0.49 · Grade A/B: 0_

- **[CD-000006]** The psychometric validity of nonprofit brand equity models differs across geographic and cultural contexts.  
  P = 0.49 · C (mixed) ⚠ conflict, uncertain  
  EVIDs: 1 supporting, 0 contradicting, 3 mixed · N sources: 36


### Sector Classification
_N claims: 6 · Mean posterior: 0.48 · Grade A/B: 0_

- **[SC-000011]** A classification system's utility for comparative nonprofit research is a function of its optimised balance between econ…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SC-000012]** Standard industrial classifications like ISIC systematically underestimate the heterogeneity of the nonprofit sector by …  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SC-000013]** Nationally-specific, highly detailed taxonomies like the NTEE are not robust for international comparison due to a lack …  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SC-000014]** The nonprofit sectors of developing countries cannot be accurately represented without a distinct category for developme…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SC-000015]** Classifying nonprofit organisations by their primary economic activity at the establishment level produces more valid cr…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SC-000016]** The ICNPO framework can be reliably applied across diverse national contexts to produce comparable data on the compositi…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Donor Profile
_N claims: 1 · Mean posterior: 0.48 · Grade A/B: 0_

- **[DP-000001]** The profile of a "blood only" donor (younger, higher risk-propensity, unmarried) is significantly different from the pro…  
  P = 0.48 · C (mixed) ⚠ conflict, uncertain  
  EVIDs: 2 supporting, 3 contradicting, 0 mixed · N sources: 3


### Peer Identification
_N claims: 1 · Mean posterior: 0.46 · Grade A/B: 0_

- **[PI-000004]** In nonprofit contexts with a strong member-service component, organizational identification is positively associated wit…  
  P = 0.46 · C (mixed) ⚠ thin-support, conflict, uncertain  
  EVIDs: 0 supporting, 1 contradicting, 0 mixed · N sources: 12


### Contextual Moderation
_N claims: 3 · Mean posterior: 0.46 · Grade A/B: 0_

- **[CM-000001]** Cultural context moderates relationships within process-based brand equity models.  
  P = 0.50 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 27

- **[CM-000002]** Industry, platform, and national culture can alter the relevance and structure of brand equity process models.  
  P = 0.50 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 27

- **[CM-000004]** The predictive power of the BEBA model is greater in fundraising contexts characterised by high competitive crowding and…  
  P = 0.38 · D (weak) ⚠ thin-support, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 27


### Brand Equity Ontology
_N claims: 3 · Mean posterior: 0.46 · Grade A/B: 0_

- **[BE-000023]** Boenigk and Becker’s model defines nonprofit brand equity as a stakeholder-based relational asset that is conceptually d…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BE-000024]** Rios Romero et al.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BE-000022]** Faircloth’s model conceptually blends nonprofit brand equity with stakeholder preference and support intention.  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Donor Commitment
_N claims: 3 · Mean posterior: 0.46 · Grade A/B: 0_

- **[DC-000004]** Commitment is a central dimension of nonprofit brand equity.  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DC-000007]** Donor brand commitment is a positive predictor of a portfolio of supportive intentions, including donation, volunteering…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[DC-000008]** For nonprofit brands, attitudinal commitment is a more robust measure of donor loyalty than exclusive repeat-donation fr…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Dual-Process Model
_N claims: 2 · Mean posterior: 0.46 · Grade A/B: 0_

- **[DP-000003]** Cognitive-intentional models best explain supporter behaviour in novel situations, while practice-based models best expl…  
  P = 0.51 · C (mixed) ⚠ thin-support  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 14

- **[DP-000002]** The total effect of past donation on future donation is mediated by two distinct pathways: (a) cognitive automaticity an…  
  P = 0.40 · D (weak) ⚠ thin-support, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 14


### Brand Relevance
_N claims: 1 · Mean posterior: 0.45 · Grade A/B: 0_

- **[BR-000009]** In the Y&R Brand Asset Valuator model, differentiation and relevance together constitute brand strength.  
  P = 0.45 · C (mixed) ⚠ conflict, uncertain  
  EVIDs: 2 supporting, 1 contradicting, 0 mixed · N sources: 30


### Brand Character
_N claims: 1 · Mean posterior: 0.45 · Grade A/B: 0_

- **[BC-000008]** The perceived character of a nonprofit brand is not a significant predictor of resource provider support intentions in F…  
  P = 0.45 · D (weak) ⚠ conflict, uncertain  
  EVIDs: 0 supporting, 1 contradicting, 1 mixed · N sources: 1


### Volunteer Typology
_N claims: 1 · Mean posterior: 0.44 · Grade A/B: 0_

- **[VT-000001]** Potential volunteers can be classified into distinct typologies based on their brand-driven decision-making process.  
  P = 0.44 · D (weak) ⚠ thin-support, uncertain  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 5


### Brand-Related Psychological Processes
_N claims: 2 · Mean posterior: 0.44 · Grade A/B: 0_

- **[BR-000005]** Consumer psychology of brands can be organized around five core processes: identifying, experiencing, integrating, signi…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BR-000006]** Brand-related psychological processes do not necessarily occur in a fixed linear sequence.  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Marketing Attitude
_N claims: 2 · Mean posterior: 0.44 · Grade A/B: 0_

- **[MA-000005]** There is no significant direct statistical relationship between stakeholder attitudes toward marketing and their percept…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[MA-000004]** Positive stakeholder attitudes toward marketing are positively associated with perceptions of the nonprofit's brand orie…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Symbolic_Capital
_N claims: 2 · Mean posterior: 0.44 · Grade A/B: 0_

- **[SC-000022]** Charitable giving functions as a mechanism for converting a donor's economic capital into symbolic capital such as prest…  
  P = 0.50 · unlinked ⚠ no-evidence  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[SC-000023]** Nonprofit Brand Equity functions as organizational Symbolic Capital, which stakeholders convert into their own symbolic …  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Congruence
_N claims: 1 · Mean posterior: 0.43 · Grade A/B: 0_

- **[BC-000009]** Resource providers are more inclined to support a nonprofit when the nonprofit brand personality matches their self-conc…  
  P = 0.43 · D (weak) ⚠ uncertain  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 4


### Recursive Causality
_N claims: 1 · Mean posterior: 0.43 · Grade A/B: 0_

- **[RC-000001]** Aggregate nonprofit market performance can reinforce individual-level brand perceptions by acting as a social proof sign…  
  P = 0.43 · D (weak) ⚠ uncertain  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 2


### External Environment
_N claims: 1 · Mean posterior: 0.43 · Grade A/B: 0_

- **[EE-000001]** The relationship between nonprofit brand orientation and performance outcomes is moderated by the organisation's externa…  
  P = 0.43 · D (weak) ⚠ uncertain  
  EVIDs: 2 supporting, 0 contradicting, 0 mixed · N sources: 1


### Perceived Accountability
_N claims: 1 · Mean posterior: 0.42 · Grade A/B: 0_

- **[PA-000001]** Accountability and reporting tools function as signals that donors can use to infer NGO reliability and integrity.  
  P = 0.42 · D (weak) ⚠ uncertain  
  EVIDs: 3 supporting, 0 contradicting, 0 mixed · N sources: 1


### Cause-Related Marketing
_N claims: 2 · Mean posterior: 0.41 · Grade A/B: 0_

- **[CR-000001]** In cause-related marketing contexts, donation amounts perceived as too large or overly publicized increase consumer skep…  
  P = 0.41 · D (weak) ⚠ conflict, uncertain  
  EVIDs: 2 supporting, 3 contradicting, 1 mixed · N sources: 49

- **[CR-000006]** Cause-Related Marketing (CRM) campaigns can be perceived by consumers as more selfish than direct corporate donations.  
  P = 0.41 · D (weak) ⚠ conflict, uncertain  
  EVIDs: 2 supporting, 3 contradicting, 1 mixed · N sources: 49


### Internal Environment
_N claims: 1 · Mean posterior: 0.40 · Grade A/B: 0_

- **[IE-000001]** The relationship between nonprofit brand orientation and performance outcomes is moderated by the organisation's interna…  
  P = 0.40 · D (weak) ⚠ thin-support, uncertain  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Value Proposition
_N claims: 1 · Mean posterior: 0.40 · Grade A/B: 0_

- **[VP-000001]** For stakeholders with financial capacity but low intrinsic motivation, a brand must frame support as a compelling value …  
  P = 0.40 · D (weak) ⚠ thin-support, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 9


### Behavioural Infrastructure
_N claims: 1 · Mean posterior: 0.39 · Grade A/B: 0_

- **[BI-000003]** Nonprofit brand equity can be conceptualized as a behavioural infrastructure that facilitates the conversion of donation…  
  P = 0.39 · D (weak) ⚠ thin-support, uncertain  
  EVIDs: 1 supporting, 0 contradicting, 0 mixed · N sources: 1


### Entrepreneurial Orientation
_N claims: 1 · Mean posterior: 0.39 · Grade A/B: 0_

- **[EO-000001]** An entrepreneurial orientation within a nonprofit positively influences its marketing capabilities and long-term sustain…  
  P = 0.39 · D (weak) ⚠ thin-support, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 1 mixed · N sources: 5


### Shared Brand Equity
_N claims: 1 · Mean posterior: 0.39 · Grade A/B: 0_

- **[SB-000004]** The mechanisms of shared brand equity in nonprofit-corporate or multi-NGO collaborations are underdeveloped in the revie…  
  P = 0.39 · D (weak) ⚠ uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 40


### Brand Equity Elasticity
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BE-000077]** A brand's ability to consistently enable behaviour across diverse stakeholder segments, behavioural types, and engagemen…  
  P = 0.38 · D (weak) ⚠ thin-support, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 1


### Brand Platform
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BP-000031]** Brands that evolve from a narrow, activity-based identity to a higher-order, solution-based brand platform achieve great…  
  P = 0.38 · D (weak) ⚠ thin-support, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 1


### Stakeholder Perspective
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[SP-000001]** Donor-based brand equity captures a different stakeholder perspective than volunteer-based, beneficiary-based, or staff-…  
  P = 0.38 · D (weak) ⚠ uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 1


### Behavioural Salience
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BS-000001]** Brand awareness increases the salience of donating to a nonprofit by making the organization more likely to come to mind…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Audit
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BA-000065]** Brand audits can identify gaps between intended brand meaning and stakeholder perceptions.  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Differentiation; Trust; Perceived Efficacy; Self-Concept Congruence; Donation Behavior
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BD-000009]** The effect of perceived brand differentiation on donation behavior is fully mediated by its influence on perceived trust…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Model Portability
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BE-000028]** The nonprofit brand equity model by Rios Romero et al.  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity Structural Form
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BE-000032]** A processual or network-based specification of nonprofit brand equity demonstrates superior model fit and explanatory po…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Equity-Behavior Integration
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BE-000012]** The reviewed literature does not provide a systematic theory-driven integration of a multi-dimensional brand equity fram…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Repositioning
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BR-000010]** Strong existing brand associations make radical brand repositioning less effective than incremental repositioning.  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Stature
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BS-000020]** In the Y&R Brand Asset Valuator model, brand strength is a prerequisite for developing esteem and knowledge.  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Uniqueness
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BU-000004]** A donor's perception of a nonprofit brand's uniqueness has a causal effect on their subsequent actual donation behaviour…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand Uniqueness; Donor Retention; Repeat Donation
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BU-000003]** Controlling for trust and prior giving history, perceived brand uniqueness has a positive effect on donor retention and …  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand-Enabled Behavioural Architecture
_N claims: 3 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BE-000029]** Brand equity constructs explain variance in donation behaviour beyond their indirect effects through donation intention.  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BE-000030]** IBM enactment conditions mediate the residual effect of brand equity constructs on donation behaviour after controlling …  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0

- **[BE-000031]** Relational brand equity constructs are more strongly associated with IBM enactment conditions than cognitive-evaluative …  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand_Architecture
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BA-000082]** The behavioural effectiveness of a nonprofit brand is a function of its architecture's capacity to simultaneously satisf…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand_Framing
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[BF-000016]** Brand communications that frame stakeholder action as reparative justice will foster higher long-term commitment than co…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Comparative Model Testing
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[CM-000003]** The reviewed literature rarely compares competing models such as brand-dominant and moral-norm-dominant explanations of …  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Confidence
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[C-000002]** Nonprofit employees are less likely to have confidence in the ability of nonprofit organizations to spend money wisely c…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Digital Trust
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[DT-000001]** Platform credibility and trust in the system are necessary preconditions for the Theory of Planned Behavior logic to app…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Donation Knowledge and Skills
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[DK-000001]** Brand communication can provide donors with the knowledge and skills needed to complete a donation.  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Donor Attitude
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[DA-000001]** Brand understanding shapes a donor's attitude toward giving to a specific nonprofit organization.  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Donor-Beneficiary-Organisation Triad
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[DB-000007]** Donor attitudes toward beneficiaries are relevant to explaining nonprofit brand equity and donor behaviour.  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Financial Performance Integration
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[FP-000001]** Behavioural process models of brand equity are not sufficiently integrated with financial and business performance metri…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Integrated Model Sufficiency
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[IM-000002]** An integrated Brand Equity to TPB to IBM to Behaviour model explains donation behaviour more adequately than single-comp…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Lighthouse Mechanism
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[LM-000001]** In crowded fundraising environments, strong nonprofit brands reduce donor choice complexity by orienting donors toward f…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Longitudinal Donation Behavior
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[LD-000002]** The ability of Theory of Planned Behavior constructs to predict long-term sustained charitable donation behavior is less…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Mission Field Contingency
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[MF-000001]** The relative influence of nonprofit brand equity dimensions on Theory of Planned Behavior constructs depends on the nonp…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Organisational Scope
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[OS-000001]** Nonprofit brand equity dynamics differ between large, well-known nonprofits and smaller community-based or grassroots or…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Relational Brand Equity
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[RB-000003]** Trust and commitment are more proximal predictors of sustained giving than purely cognitive-evaluative brand constructs.  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Resource Reallocation
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[RR-000001]** Nonprofit organizations can substitute large-scale paid communication with internal culture, mission strength, employee …  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Social Signalling
_N claims: 1 · Mean posterior: 0.38 · Grade A/B: 0_

- **[SS-000002]** Donating to a nonprofit brand enables individuals to express values, signal group membership, and reinforce social ident…  
  P = 0.38 · unlinked ⚠ no-evidence, uncertain  
  EVIDs: 0 supporting, 0 contradicting, 0 mixed · N sources: 0


### Brand-Mission Tension
_N claims: 1 · Mean posterior: 0.37 · Grade A/B: 0_

- **[BM-000001]** Perceived commercialisation or mission drift can undermine authenticity and trust in nonprofit brands.  
  P = 0.37 · D (weak) ⚠ conflict, uncertain  
  EVIDs: 0 supporting, 1 contradicting, 1 mixed · N sources: 2


### Consumer Skepticism
_N claims: 2 · Mean posterior: 0.36 · Grade A/B: 0_

- **[CS-000002]** In cause-related marketing contexts, high donation amounts can trigger consumer skepticism that reduces the warm glow ef…  
  P = 0.36 · D (weak) ⚠ conflict, uncertain  
  EVIDs: 0 supporting, 2 contradicting, 0 mixed · N sources: 32

- **[CS-000003]** In cause-related marketing contexts, consumer skepticism toward donation claims reduces subsequent purchase intention.  
  P = 0.36 · D (weak) ⚠ conflict, uncertain  
  EVIDs: 0 supporting, 2 contradicting, 0 mixed · N sources: 32



## 3. Literature Map (Verified Sources)

The following 517 sources appear in at least one verified (`supported`) EVID. They are sorted by aggregate evidence weight (strength × number of verified findings).

| Rank | Source | Verified EVIDs | Concepts | Weight |
|---|---|---|---|---|
| 1 | White, K., Sutton, L. S. C., & Zhao, X. (2023) | 84 | ability; agency; altruism; attitude +111 | 59.75 |
| 2 | Romero, M. J. R., Abril, C., & Urquia-Grande, E. (2023) | 119 | aaker brand equity; accountability; advertising; advocacy +185 | 58.00 |
| 3 | Mittelman and Rojas‐Méndez (2018) | 74 | ability; altruism; attitude; attitude toward organization +90 | 50.65 |
| 4 | Kim, H. H., & Han, E. (2020) | 76 | ability; altruism; attitude; attitude toward donating +116 | 49.85 |
| 5 | Millán, Á., Retamosa, M., & Carranza, R. (2023) | 69 | ability; advocacy; affective response; altruism +98 | 42.15 |
| 6 | Smith and McSweeney (2007) | 49 | attitude; attitude toward organization; behavioral intention; behavioral model +70 | 34.90 |
| 7 | List, J., Murphy, J., Price, M. K., & James, A. G. (2021) | 54 | ability; affective utility; altruism; altruistic concern +58 | 34.80 |
| 8 | Van Steenburg, E., & Spears, N. (2021) | 52 | attitude; attitude toward donating; attitude toward organization; behavioral intention +80 | 34.30 |
| 9 | Bekkers and Wiepking (2011) | 39 | altruism; anonymity; awareness of need; behavioural intention +76 | 33.35 |
| 10 | Amonhaemanon, D., Khongkaew, P., Akartwipart, A., & Thamthanakoon, N. (2024) | 50 | ability; affective utility; altruism; altruistic concern +58 | 31.70 |
| 11 | Carpenter, J. (2021) | 50 | ability; affective utility; altruism; altruistic concern +58 | 31.70 |
| 12 | Chen, Y., Dai, R., Yao, J., & Li, Y. (2019) | 47 | ability; altruism; attitude; attitude toward organization +73 | 30.65 |
| 13 | Gregory et al. (2019) | 51 | affective response; attitude; attitude toward donating; attitude toward the charity +107 | 29.00 |
| 14 | Burmann et al. (2009) | 54 | asset-liability management; associative memory; attitude; b2b brand equity +80 | 27.95 |
| 15 | Michel and Rieunier (2012) | 44 | affective response; attitude; attitude toward donating; attitude toward the charity +79 | 27.30 |
| 16 | Wu et al. (2020) | 48 | aaker brand equity; antecedent; attitude; behavioral intention +64 | 26.95 |
| 17 | Andreoni, J (1989) | 39 | affective utility; altruism; altruistic concern; authenticity +42 | 25.10 |
| 18 | Li et al. (2022) | 36 | ability; altruism; attitude; benevolence +48 | 25.05 |
| 19 | Zheng et al. (2025) | 44 | antecedent; attitude; behavioral intention; behavioral outcomes +56 | 24.20 |
| 20 | Konow, J (2010) | 38 | affective utility; altruism; altruistic concern; authenticity +41 | 24.10 |
| 21 | Venable et al. (2005) | 41 | advocacy; affective response; attitude; attitude toward the charity +61 | 22.95 |
| 22 | Jiang et al. (2017) | 40 | antecedent; attitude; behavioral intention; behavioral outcomes +51 | 22.35 |
| 23 | Rambocas et al. (2017) | 40 | antecedent; attitude; behavioral intention; behavioral outcomes +51 | 22.35 |
| 24 | Huang, S.-L., & Ku, H.-H. (2016) | 38 | affective response; attitude; attitude toward donating; attitude toward the charity +70 | 22.20 |
| 25 | Andreoni (1990) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 26 | Bianchi et al. (2023) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 27 | Bischoff, I., & Krauskopf, T (2015) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 28 | Chaabouni et al. (2020) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 29 | Crumpler and Grossman (2008) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 30 | Ferguson, E., & Flynn, N (2016) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 31 | Ferguson, E., Lawrence, C., Bowen, S., Gemelli, C., Rozsa, A., Niekrasz, K., Van Dongen, A., Williams, L., Thijsen, A., Guerin, N., Masser, B., & Davison, T (2023) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 32 | Fraser (2018) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 33 | Fraser (2022) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 34 | Gandullia, L (2019) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 35 | Giebelhausen, M., Lawrence, B., Chun, H., & Hsu, L (2017) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 36 | Gråd, E., Erlandsson, A., & Tinghög, G (2021) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 37 | Grossman, P., & Levy, J. (2024) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 38 | Harbaugh (1998) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 39 | Harbaugh, W., Mayr, U., & Burghart, D (2007) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 40 | Hartmann, P., Eisend, M., Apaolaza, V., & D'souza, C (2017) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 41 | Imas, A (2014) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 42 | Konow, J (2006) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 43 | Lilley, A., & Slonim, R (2014) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 44 | Luccasen, and Grossman (2017) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 45 | Mayo, J., & Tinsley, C (2009) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 46 | Null, C (2011) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 47 | Ranga, G., Khandeparkar, K., Motiani, M., & Sharma, P (2025) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 48 | Scharf, K (2013) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 49 | Wilhelm et al. (2014) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 50 | Winterich, K., & Barone, M (2011) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 51 | Wu, S.-I., Lu, C.-L., & Wu, C.-C. (2022) | 36 | affective utility; altruistic concern; authenticity; behavioural effectiveness +37 | 22.10 |
| 52 | Crawford and Jackson (2025) | 37 | affective response; attitude; attitude toward donating; attitude toward the charity +72 | 22.00 |
| 53 | Södergren, J. (2021) | 33 | attitude; attitude toward organization; behavioral intention; behavioral model +59 | 21.95 |
| 54 | Ngo et al. (2021) | 35 | affective response; attitude; attitude toward donating; attitude toward the charity +67 | 21.25 |
| 55 | Kutlu and Özcan (2024) | 37 | advocacy; affective response; attitude; attitude toward the charity +58 | 20.75 |
| 56 | Wymer and Čačija (2025) | 37 | advocacy; affective response; attitude; attitude toward the charity +58 | 20.75 |
| 57 | Ali et al. (2022) | 34 | affective response; attitude; attitude toward donating; attitude toward the charity +66 | 20.70 |
| 58 | Bilgin and Kethüda (2022) | 34 | affective response; attitude; attitude toward donating; attitude toward the charity +66 | 20.70 |
| 59 | Shehu et al. (2016) | 34 | affective response; attitude; attitude toward donating; attitude toward the charity +66 | 20.70 |
| 60 | Chatzipanagiotou et al. (2019) | 42 | associative memory; attitude; behaviour; behavioural intention +67 | 20.00 |
| 61 | Knowles et al. (2012) | 30 | attitude; attitude toward organization; behavioral intention; behavioral model +52 | 19.85 |
| 62 | Lee, Z., Spry, A., Ekinci, Y., & Vredenburg, J. (2023) | 30 | altruism; attitude; attitude toward organization; awareness +57 | 19.85 |
| 63 | Musamuxamedov et al. (2025) | 32 | attitude; attitude toward organization; behavioral intention; behavioral model +53 | 19.70 |
| 64 | Fehresti, S., Takian, A., Jaafaripooyan, E., Parsaeian, M., & Jalilian, H. (2021) | 26 | attitude; behaviour architecture; boundary conditions; charitable giving +35 | 19.45 |
| 65 | Chatzipanagiotou et al. (2025) | 39 | associative memory; attitude; behaviour; behavioural intention +60 | 19.05 |
| 66 | Xu et al. (2022) | 39 | associative memory; attitude; behaviour; behavioural intention +60 | 19.05 |
| 67 | Lee, J. Y., & Kim, S. S. (2023) | 31 | ability; altruism; attitude; benevolence +48 | 19.00 |
| 68 | Anggraeni and Kuklienė (2024) | 30 | attitude; attitude toward organization; behavioral intention; behavioral model +52 | 18.50 |
| 69 | Ha, Q.-A., Pham, P., & Le, L. (2022) | 31 | advocacy; attitude toward donating; attitude toward the charity; behavioural outcomes +51 | 18.15 |
| 70 | De, T., & Verma, A. (2021) | 30 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 17.80 |
| 71 | Dean (2016) | 28 | attitude; attitude toward donating; attitude toward organization; behavioral intention +59 | 17.75 |
| 72 | Hou et al. (2009) | 32 | actual giving behaviour; altruism; attitude toward the charity; behavioural intention +41 | 17.65 |
| 73 | Keller, K.L. (1993) | 41 | asset-liability management; associative memory; attitude formation; b2b brand equity +67 | 17.25 |
| 74 | Faircloth (2005) | 59 | additive model; altruistic disposition; altruistic volunteerism; antecedent model +74 | 17.15 |
| 75 | Veludo-De-Oliveira, T., Alhaidari, I. S., Yani-De-Soriano, M., & Yousafzai, S. Y. (2016) | 23 | attitude; boundary conditions; cross-cultural generalizability; cultural context +28 | 16.90 |
| 76 | Chapman et al. (2022) | 29 | attitude; attitude toward organization; austrian giving context; behavioral intention +56 | 16.70 |
| 77 | Tanouri et al. (2019) | 31 | attitude; behaviour; behavioural intention; behavioural outcomes +44 | 16.05 |
| 78 | Katz (2017) | 27 | affective response; attitude; attitude toward the charity; behavioural outcomes +51 | 15.95 |
| 79 | Algharabat, R., Rana, N., Alalwan, A., Baabdullah, A., & Gupta, A (2020) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 80 | Boukis, A., & Christodoulides, G (2018) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 81 | Butt, M., Mushtaq, S., Afzal, A., Khong, K., Ong, F., & Ng, P (2017) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 82 | Das, S., Stenger, C., & Ellis, C (2009) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 83 | Ha, M (2021) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 84 | Hsu, L (2023) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 85 | Martín, H., Herrero, Á., & Del Mar García De Los Salmones, M (2019) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 86 | Rodrigues, P., & Martins, F (2016) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 87 | Satar, M., Rather, R., Parrey, S., Khan, H., & Rasul, T (2023) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 88 | Singh et al. (2023) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 89 | Wu, J., Yasin, M., & Ng, C (2025) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 90 | Yang, D., Sonmez, M., Gonzalez, M., Liu, Y., & Yoder, C (2019) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 91 | Yeğin and Ikram (2022) | 30 | attitude; behaviour; behavioural intention; behavioural outcomes +42 | 15.50 |
| 92 | D'souza et al. (2021) | 26 | affective response; attitude; attitude toward the charity; behavioural outcomes +50 | 15.40 |
| 93 | Stebbins and Hartman (2013) | 26 | affective response; attitude; attitude toward the charity; behavioural outcomes +50 | 15.40 |
| 94 | Benli, B., & Kocaman, R. (2025) | 23 | ability; altruism; attitude; benevolence +39 | 15.20 |
| 95 | Aaker (1991) | 36 | aggregation; asset-liability management; associative memory; b2b brand equity +70 | 15.20 |
| 96 | Chapman, C., Hornsey, M., & Gillespie, N. (2021) | 25 | ability; altruism; austrian giving context; benevolence +42 | 14.95 |
| 97 | Gutiérrez et al. (2023) | 28 | asset-liability management; associative memory; b2b brand equity; behaviour +55 | 14.75 |
| 98 | Aaker, David A. (1991) | 33 | aggregation; antecedents; attitude formation; behavioural loyalty +57 | 14.30 |
| 99 | Sargeant, A., West, D. C., & Ford, J. B. (2008) | 21 | altruism; attitude toward donating; attitude toward the charity; behavioural intention +42 | 14.25 |
| 100 | Tasci (2020) | 27 | asset-liability management; associative memory; b2b brand equity; behaviour +53 | 14.20 |
| 101 | Van Teunenbroek et al. (2020) | 22 | attitude; attitude toward organization; behavioral intention; behavioral model +44 | 14.00 |
| 102 | Boenigk and Helmig (2013) | 28 | behavioral constraints; blood donation; customer loyalty; customer-company identification +26 | 14.00 |
| 103 | Gugenishvili (2022) | 16 | behaviour architecture; boundary conditions; descriptive norms; donation behavior +17 | 13.75 |
| 104 | Park, C. Whan; MacInnis, Deborah J.; Priester, Joseph; Eisingerich, Andreas B.; Iacobucci, Dawn (2010) | 27 | accessibility; actual behaviour; alternative inhibition; attachment measurement +45 | 13.10 |
| 105 | Romero, M. J. R., & Abril, C. (2024) | 24 | aaker brand equity; advocacy; brand anthropomorphism; brand as heuristic +41 | 12.80 |
| 106 | Ajzen, I. (2002) | 17 | attitude; behaviour architecture; charitable giving; cross-cultural generalizability +29 | 12.70 |
| 107 | Cornwell et al. (2022) | 25 | asset-liability management; associative memory; b2b brand equity; behaviour +47 | 12.65 |
| 108 | Christodoulides, Cadogan, and Veloutsou (2015) | 26 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +43 | 12.55 |
| 109 | Watanuki and Akama (2022) | 24 | asset-liability management; associative memory; b2b brand equity; behaviour +43 | 12.45 |
| 110 | Maleki and Hosseini (2020) | 19 | attitude toward donating; attitude toward the charity; behavioural outcomes; brand choice +37 | 12.25 |
| 111 | Stocchi and Fuller (2017) | 24 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +41 | 11.80 |
| 112 | SRC-000885 (n.d.) | 24 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +41 | 11.80 |
| 113 | Bird, M., Channon, C., & Ehrenberg, A. S. C. (1970) | 24 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +41 | 11.80 |
| 114 | Dobni and Zinkhan (1990) | 24 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +41 | 11.80 |
| 115 | SRC-000889 (n.d.) | 24 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +41 | 11.80 |
| 116 | SRC-000890 (n.d.) | 24 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +41 | 11.80 |
| 117 | SRC-000891 (n.d.) | 24 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +41 | 11.80 |
| 118 | SRC-000892 (n.d.) | 24 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +41 | 11.80 |
| 119 | SRC-000893 (n.d.) | 24 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +41 | 11.80 |
| 120 | Romaniuk & Nenycz-Thiel (2013) | 24 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +41 | 11.80 |
| 121 | SRC-000894 (n.d.) | 24 | aggregation; antecedents; behavioural loyalty; behavioural outcomes +41 | 11.80 |
| 122 | Lakew, G., Gebretsadkan, B. T., Alemu, G. G., Bazezew, A. M., Yirsaw, A. N., Wondie, W., Mengistie, B. A., Dagnaw, T. E., Aweke, M. N., & Baykemagn, N. D. (2026) | 14 | boundary conditions; descriptive norms; donation behavior; donation intention +12 | 11.75 |
| 123 | Boenigk and Becker (2016) | 28 | accountability; advocacy; attitude formation; awareness +52 | 11.20 |
| 124 | Schmitt (2011) | 23 | affect; brand attachment; brand attitude; brand awareness +41 | 10.90 |
| 125 | Kashif et al. (2018) | 18 | attitude toward donating; awareness; brand association; brand awareness +27 | 10.45 |
| 126 | Feldwick (1996) | 21 | asset-liability management; b2b brand equity; behavioural effectiveness; boundary conditions +36 | 10.10 |
| 127 | Parris and Guzmán (2022) | 17 | asset-liability management; b2b brand equity; boundary conditions; brand association +26 | 10.00 |
| 128 | Gugenishvili, I., & Colliander, J. (2022) | 12 | boundary conditions; descriptive norms; donation behavior; donation intention +11 | 9.75 |
| 129 | Kusuma, H., & Anafisati, V. ( (2020) | 12 | boundary conditions; descriptive norms; donation behavior; donation intention +11 | 9.75 |
| 130 | Ghoorah, U., Talukder, M. H., & Khan, A. (2021) | 14 | ability; altruism; benevolence; brand identification +20 | 9.60 |
| 131 | Li, W., Yang, D.-H., & Sun, Y. (2022) | 14 | ability; altruism; benevolence; brand identification +20 | 9.60 |
| 132 | Robson, A., & Hart, D. (2020) | 14 | ability; altruism; benevolence; brand identification +20 | 9.60 |
| 133 | France et al. (2025) | 16 | asset-liability management; b2b brand equity; boundary conditions; brand as heuristic +26 | 9.45 |
| 134 | Sargeant (1999) | 12 | attitude; behaviour architecture; cross-cultural generalizability; cultural context +22 | 9.40 |
| 135 | Zhou, L., & Xue, F. (2025) | 15 | attitude; attitude toward donating; brand choice; brand equity +27 | 9.35 |
| 136 | Erdem & Swait (1998) | 19 | behavioural outcome; brand associations; brand equity; brand equity theory +20 | 9.05 |
| 137 | Mikul and Mittal (2023) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 138 | Rojas-Lamorena et al. (2022) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 139 | Ansary, A., & Hashim, N. N. H. N (2018) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 140 | Baalbaki, S., & Guzmán, F (2016) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 141 | Barwise (1993) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 142 | Bendixen, M., Bukasa, K. A., & Abratt, R (2004) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 143 | Davcik, N. S., Silva, R., & Hair, J. F (2015) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 144 | Hanaysha, J., Abdullah, H. H., & Ghani, N. H. A (2013) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 145 | Ishaq, M., & Di Maria, E (2020) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 146 | Jara and Cliquet (2015) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 147 | Keller, K. L. ( (2016) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 148 | Keller, K. L (2020) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 149 | Medhi and Kakati (2025) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 150 | Motameni and Shahrokhi (1998) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 151 | Simon and Sullivan (1993) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 152 | Sousa and Ferreira (2023) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 153 | Tuominen, P. (1999) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 154 | Willmott, H (2010) | 15 | asset-liability management; b2b brand equity; boundary conditions; brand awareness +22 | 8.90 |
| 155 | SRC-000873 (n.d.) | 18 | behavioural evidence; boundary conditions; brand attitude; brand choice intention +45 | 8.85 |
| 156 | Baghi, I. and Gabrielli, V (2018) | 18 | behavioural evidence; boundary conditions; brand attitude; brand choice intention +45 | 8.85 |
| 157 | Diamantopoulos, A. and Winklhofer, H.M (2001) | 18 | behavioural evidence; boundary conditions; brand attitude; brand choice intention +45 | 8.85 |
| 158 | Hoeffler, S., & Keller, K. L. (2003) | 18 | behavioural evidence; boundary conditions; brand attitude; brand choice intention +45 | 8.85 |
| 159 | Roberts, J.H. and Lattin, J.M (1997) | 18 | behavioural evidence; boundary conditions; brand attitude; brand choice intention +45 | 8.85 |
| 160 | SRC-000879 (n.d.) | 18 | behavioural evidence; boundary conditions; brand attitude; brand choice intention +45 | 8.85 |
| 161 | Hommerová, D., Alaimo, S., & Sojková, O. M. (2025) | 17 | advocacy; awareness; brand anthropomorphism; brand as heuristic +29 | 8.75 |
| 162 | Da Silva, L. C., Mainardes, E., Teixeira, A., & Costa, L. (2020) | 14 | attitude toward the charity; behavioural outcomes; brand equity; brand familiarity +21 | 8.60 |
| 163 | Michel and Rieunier (2015) | 15 | affective response; attitude; bequest intention; brand awareness +36 | 8.45 |
| 164 | Barman, E. (2016) | 10 | capital; charitable giving; corporate philanthropy; cultural capital +11 | 7.75 |
| 165 | Carroll, A., & Shabana, K. (2010) | 10 | capital; charitable giving; corporate philanthropy; cultural capital +11 | 7.75 |
| 166 | Dika, S. L., & Singh, K. (2002) | 10 | capital; charitable giving; corporate philanthropy; cultural capital +11 | 7.75 |
| 167 | Edelmann, A., Wolff, T., Montagne, D., & Bail, C. (2020) | 10 | capital; charitable giving; corporate philanthropy; cultural capital +11 | 7.75 |
| 168 | Kingston, P. (2001) | 10 | capital; charitable giving; corporate philanthropy; cultural capital +11 | 7.75 |
| 169 | Lin, C., & Hai, Y. (2023) | 10 | capital; charitable giving; corporate philanthropy; cultural capital +11 | 7.75 |
| 170 | Risi, D., Vigneau, L., Bohn, S., & Wickert, C. (2022) | 10 | capital; charitable giving; corporate philanthropy; cultural capital +11 | 7.75 |
| 171 | Torras-Gómez, E., Ruiz-Eugenio, L., Sordé-Martí, T., & Duque, E. (2021) | 10 | capital; charitable giving; corporate philanthropy; cultural capital +11 | 7.75 |
| 172 | Wolniak, M., & Houston, S. (2022) | 10 | capital; charitable giving; corporate philanthropy; cultural capital +11 | 7.75 |
| 173 | Paço et al. (2014) | 12 | attitude toward the charity; behavioural outcomes; brand awareness; brand equity +19 | 7.50 |
| 174 | Liu, L., Suh, A., & Wagner, C (2018) | 10 | attitude; behaviour architecture; cross-cultural generalizability; cultural context +20 | 7.40 |
| 175 | Nguyen et al. (2022) | 10 | attitude; behaviour architecture; cross-cultural generalizability; cultural context +20 | 7.40 |
| 176 | García-Madariaga et al. (2023) | 12 | attitude toward the charity; behavioural outcomes; brand equity; brand familiarity +20 | 7.15 |
| 177 | Liu et al. (2017) | 11 | antecedent; attitude; behavioral intention; behavioral outcomes +20 | 7.05 |
| 178 | Dalman, M., & Ray, S (2021) | 11 | attitude toward the charity; behavioural outcomes; brand equity; brand familiarity +18 | 6.95 |
| 179 | Kusumasondjaja, S., & Krisnawati, W (2024) | 11 | attitude toward the charity; behavioural outcomes; brand equity; brand familiarity +18 | 6.95 |
| 180 | Michaelidou, Micevski, and Cadogan (2015) | 11 | attitude toward the charity; behavioural outcomes; brand equity; brand familiarity +18 | 6.95 |
| 181 | Ramayanti et al. (2024) | 11 | attitude toward the charity; behavioural outcomes; brand equity; brand familiarity +18 | 6.95 |
| 182 | Wymer and Akbar (2019) | 11 | attitude toward the charity; behavioural outcomes; brand equity; brand familiarity +18 | 6.95 |
| 183 | Abdullah, M., Sarfraz, M., Arif, A., & Azam, A (2018) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 184 | Ajzen, I (2016) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 185 | Biscaia, R., Ross, S., Yoshida, M., Correia, A., Rosado, A., & Marôco, J (2016) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 186 | Goyal, A., & Verma, P (2021) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 187 | Hue, T., & Huyen, N (2025) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 188 | Louvet (2023) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 189 | Park, J., Sung, J., Son, J., Na, K., & Kim, S (2019) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 190 | Phung, M., Ly, P., & Nguyen, T (2019) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 191 | Rizwan et al. (2021) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 192 | Rozenkowska, K (2023) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 193 | Ruangkanjanases et al. (2022) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 194 | Saeed, M., & Azmi, I (2019) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 195 | Santos, L., Holanda, F., De Santana Oliveira, C., Pedrotti, A., De Menezes, P., & Villwock, A (2023) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 196 | Thanh, B., Hieu, L., & Lan, L (2026) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 197 | Ulker‐Demirel, E., & Ciftci, G (2020) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 198 | Zhang, Y., Li, J., Liu, C., Shen, Y., & Li, G (2020) | 10 | antecedent; attitude; behavioral intention; behavioral outcomes +16 | 6.85 |
| 199 | Ghoorah, U., Mariyani-Squire, E., & Amin, S. Z. (2025) | 14 | advocacy; brand anthropomorphism; brand association; brand awareness +22 | 6.65 |
| 200 | SRC-000517 (n.d.) | 11 | community identification; donation intention; identity salience; intention to volunteer +15 | 6.60 |
| 201 | Al-Shamali, S., & Kashif, M (2023) | 8 | attitude; behaviour architecture; charitable giving; cross-cultural validation +12 | 6.30 |
| 202 | Sheeran and Webb (2016) | 6 | behavioral models; behaviour architecture; donation behavior; donation intention +7 | 6.00 |
| 203 | Chapman, C., Spence, J. L., Hornsey, M., & Dixon, L. J. (2025) | 11 | austrian giving context; brand recognition; charitable giving; donation amount +18 | 5.70 |
| 204 | Kessler, J. B., & Milkman, K. L. (2016) | 11 | austrian giving context; brand recognition; charitable giving; donation amount +18 | 5.70 |
| 205 | Romaniuk, Wight, & Faulkner (2017) | 12 | aided awareness; brand awareness; brand equity measurement; context-dependent measurement +22 | 5.55 |
| 206 | Sargeant, A., West, D. C., & Ford, J. B. (2006) | 12 | advocacy; awareness; brand anthropomorphism; brand equity +17 | 5.55 |
| 207 | Anselmsson et al. (2017) | 13 | associative memory; behaviour; brand associations; brand awareness +31 | 5.40 |
| 208 | ( (2025) | 11 | advocacy; brand anthropomorphism; brand equity; brand familiarity +15 | 5.35 |
| 209 | Anshori, M. Y., Karya, D. F., Rahmania, A. A., & Elfita, R. A. (2022) | 11 | advocacy; brand anthropomorphism; brand equity; brand familiarity +15 | 5.35 |
| 210 | O’Neil, J. (2009) | 11 | advocacy; brand anthropomorphism; brand equity; brand familiarity +15 | 5.35 |
| 211 | Balaskas, S., Koutroumani, M., & Rigou, M (2024) | 8 | attitude toward donating; brand choice; brand equity; brand perceptions +18 | 5.30 |
| 212 | Lichtenstein, D., Drumwright, M., & Braig, B (2004) | 8 | attitude toward donating; brand choice; brand equity; brand perceptions +18 | 5.30 |
| 213 | Panda, T., Kumar, A., Jakhar, S., Luthra, S., Garza‐Reyes, J., Kazancoglu, I., & Nayak, S (2020) | 8 | attitude toward donating; brand choice; brand equity; brand perceptions +18 | 5.30 |
| 214 | Prasetio and Azmi (2024) | 8 | attitude toward donating; brand choice; brand equity; brand perceptions +18 | 5.30 |
| 215 | Pratono and Tjahjono (2017) | 8 | attitude toward donating; brand choice; brand equity; brand perceptions +18 | 5.30 |
| 216 | Schamp, C., Heitmann, M., Bijmolt, T., & Katzenstein, R (2022) | 8 | attitude toward donating; brand choice; brand equity; brand perceptions +18 | 5.30 |
| 217 | Stollar et al. (2024) | 8 | attitude toward donating; brand choice; brand equity; brand perceptions +18 | 5.30 |
| 218 | Zhu, L., He, Y., Chen, Q., & Hu, M (2017) | 8 | attitude toward donating; brand choice; brand equity; brand perceptions +18 | 5.30 |
| 219 | Tam (2008) | 12 | behavioral intentions; brand familiarity; brand-enabled behaviour architecture; cognitive effort +17 | 5.20 |
| 220 | Chatzipanagiotou, Veloutsou, and Christodoulides (2016) | 13 | associative memory; behaviour; behavioural outcomes; brand associations +33 | 5.05 |
| 221 | Bang, H., Lee, C., Won, D., Chiu, W., & Chen, L. (2022) | 8 | community identification; intention to volunteer; organizational pride; past behaviour +9 | 4.95 |
| 222 | Groza, M. P., & Groza, M. D. (2021) | 8 | community identification; intention to volunteer; organizational pride; past behaviour +9 | 4.95 |
| 223 | Grube, J. A., & Piliavin, J. A. (2000) | 8 | community identification; intention to volunteer; organizational pride; past behaviour +9 | 4.95 |
| 224 | Marta, E., Manzi, C., Pozzi, M., & Vignoles, V. (2014) | 8 | community identification; intention to volunteer; organizational pride; past behaviour +9 | 4.95 |
| 225 | Schloderer, M., Sarstedt, M., & Ringle, C. (2014) | 8 | community identification; intention to volunteer; organizational pride; past behaviour +9 | 4.95 |
| 226 | Thoits, P. (2012) | 8 | community identification; intention to volunteer; organizational pride; past behaviour +9 | 4.95 |
| 227 | Thoits, P. (2021) | 8 | community identification; intention to volunteer; organizational pride; past behaviour +9 | 4.95 |
| 228 | Van Ingen, E., & Wilson, J. (2017) | 8 | community identification; intention to volunteer; organizational pride; past behaviour +9 | 4.95 |
| 229 | Wakefield, J., Bowe, M., & Kellezi, B. (2021) | 8 | community identification; intention to volunteer; organizational pride; past behaviour +9 | 4.95 |
| 230 | Stötzer et al. (2021) | 10 | austrian giving context; brand equity; brand familiarity; brand recognition +17 | 4.80 |
| 231 | Garg, Swami, and Malhotra (2019) | 23 | alignment; beneficiaries; brand effectiveness; brand equity +45 | 4.60 |
| 232 | Wu, L (2011) | 8 | attitude; charitable giving; cross-cultural validation; donation behavior +5 | 4.60 |
| 233 | Chapleo, C. (2015) | 17 | behavioural construct; brand equity; brand experience; brand implementation +41 | 4.45 |
| 234 | Paschina (2025) | 11 | associative memory; behaviour; brand associations; brand awareness +27 | 4.30 |
| 235 | Juntunen, M., Juntunen, J., and Autere, J. (2013) | 7 | brand awareness; brand equity; brand equity model; brand image +9 | 4.30 |
| 236 | Chaudhuri, A (2002) | 12 | associative memory; behaviour; brand associations; brand credibility +26 | 4.15 |
| 237 | De Oliveira, M. O. R., Heldt, R., Silveira, C. S., & Luce, F. B. (2023) | 10 | associative memory; behaviour; brand as heuristic; brand associations +24 | 4.10 |
| 238 | Litofcenko et al. (2023) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 239 | Blanco et al. (2021) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 240 | DellaVigna et al. (2012) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 241 | Heitzmann and Simsa (2004) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 242 | Kerres, C., & Proell, F (2008) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 243 | Neumayr, M., & Handy, F (2017) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 244 | Neumayr (2015) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 245 | Neumayr and Schröder (2025) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 246 | Neumayr and Pennerstorfer (2020) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 247 | Petritz and Kampitsch (2016) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 248 | Petritz, M., & Malaschofsky, M (2017) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 249 | Roodman, D., & Standley, S (2006) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 250 | Manning (2009) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 251 | Stötzer, S., Andeßner, R. C., & Scheichl, S (2020) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 252 | Wit, A., & Bekkers, R (2016) | 8 | austrian giving context; brand recognition; charitable giving; donation amount +11 | 4.05 |
| 253 | Buil, de Chernatony, and Martínez (2008) | 8 | behavioural consequences; brand associations; brand awareness; brand loyalty +16 | 4.05 |
| 254 | Adomavičiūtė and Urbonavičius (2023) | 4 | behaviour architecture; donation behavior; donation intention; donation models +6 | 4.00 |
| 255 | Blake, P (2018) | 4 | behaviour architecture; donation behavior; donation intention; donation models +6 | 4.00 |
| 256 | Labban, A., Novell, C., & Bauer, S (2022) | 4 | behaviour architecture; donation behavior; donation intention; donation models +6 | 4.00 |
| 257 | Nilsson, A., Erlandsson, A., & Västfjäll, D (2016) | 4 | behaviour architecture; donation behavior; donation intention; donation models +6 | 4.00 |
| 258 | Shang et al. (2019) | 4 | behaviour architecture; donation behavior; donation intention; donation models +6 | 4.00 |
| 259 | Willer, R., Wimer, C., & Owens, L (2015) | 4 | behaviour architecture; donation behavior; donation intention; donation models +6 | 4.00 |
| 260 | Eisenhardt, K. M. (1989) | 4 | bayesian inference; cumulative knowledge; evidence; evidence aggregation +2 | 4.00 |
| 261 | Templier, M., & Paré, G. (2015) | 4 | bayesian inference; cumulative knowledge; evidence; evidence aggregation +2 | 4.00 |
| 262 | Krishnan (1996) | 10 | associative memory; associative network theory; behaviour; brand associations +22 | 3.75 |
| 263 | Fennis, Bob M. and Janssen, Loes and Vohs, Kathleen D. (2009) | 10 | associative memory; behaviour; brand associations; brand equity +24 | 3.75 |
| 264 | Shehu et al. (2015) | 6 | behavioral segmentation; blood donation; donation behavior; donor profile +3 | 3.75 |
| 265 | Davcik et al. (2015) | 5 | brand equity; conceptual fragmentation; construct definition; construct measurement +5 | 3.65 |
| 266 | Washburn, J. H., & Plank, R. E. (2002) | 5 | brand associations; brand awareness; brand equity; brand loyalty +4 | 3.65 |
| 267 | Cobb-Walgren, Ruble, and Donthu (1995) | 9 | advertising investment; behavioural measures; behavioural precursors; brand associations +20 | 3.55 |
| 268 | Buil, I., Martínez, E., & Chernatony, L (2013) | 9 | associative memory; behaviour; brand associations; brand equity +20 | 3.55 |
| 269 | Çifci, S., Ekinci, Y., Whyatt, G., Japutra, A., Molinillo, S., & Siala, H (2016) | 9 | associative memory; behaviour; brand associations; brand equity +20 | 3.55 |
| 270 | French and Smith (2013) | 9 | associative memory; behaviour; brand associations; brand equity +20 | 3.55 |
| 271 | Guhl, D (2024) | 9 | associative memory; behaviour; brand associations; brand equity +20 | 3.55 |
| 272 | Han et al. (2021) | 9 | associative memory; behaviour; brand associations; brand equity +20 | 3.55 |
| 273 | Keller and Brexendorf (2019) | 9 | associative memory; behaviour; brand associations; brand equity +20 | 3.55 |
| 274 | Petersen, A (2025) | 9 | associative memory; behaviour; brand associations; brand equity +20 | 3.55 |
| 275 | Pournarakis, D (2017) | 9 | associative memory; behaviour; brand associations; brand equity +20 | 3.55 |
| 276 | Zollo, L., Filieri, R., Rialti, R., & Yoon, S (2020) | 9 | associative memory; behaviour; brand associations; brand equity +20 | 3.55 |
| 277 | Alhidari, I., Veludo-De-Oliveira, T., Yousafzai, S., & Yani-De-Soriano, M (2018) | 6 | attitude; cross-cultural generalizability; cultural context; digital donation +11 | 3.40 |
| 278 | Chetioui et al. (2022) | 6 | attitude; cross-cultural generalizability; cultural context; digital donation +11 | 3.40 |
| 279 | Cohen, D., Campbell, M., & Quinlan, P (2023) | 6 | attitude; cross-cultural generalizability; cultural context; digital donation +11 | 3.40 |
| 280 | Gui, P., Yang, Z., & Che, J (2022) | 6 | attitude; cross-cultural generalizability; cultural context; digital donation +11 | 3.40 |
| 281 | Huang, Q., Li, D., Zhou, C., Xu, Q., Li, P., & Warren, C (2021) | 6 | attitude; cross-cultural generalizability; cultural context; digital donation +11 | 3.40 |
| 282 | Middleton, G., & Lee, H (2020) | 6 | attitude; cross-cultural generalizability; cultural context; digital donation +11 | 3.40 |
| 283 | Rocha, A., & Monteiro, L (2023) | 6 | attitude; cross-cultural generalizability; cultural context; digital donation +11 | 3.40 |
| 284 | Talie et al. (2020) | 6 | attitude; cross-cultural generalizability; cultural context; digital donation +11 | 3.40 |
| 285 | Zhao, H., Jin, B., Liu, Q., Ge, Y., Chen, E., Zhang, X., & Xu, T (2020) | 6 | attitude; cross-cultural generalizability; cultural context; digital donation +11 | 3.40 |
| 286 | Wood (2000) | 16 | added value; behavioural effectiveness; brand; brand asset +27 | 3.20 |
| 287 | Webb and Sheeran (2006) | 4 | behavioural enactment; brand equity; brand familiarity; choice complexity +7 | 3.20 |
| 288 | Wymer and Akbar (2017) | 15 | antecedents; behavioural outcomes; brand authenticity; brand category +23 | 3.00 |
| 289 | Croson, R., Handy, F., & Shang, J. (2009) | 3 | behavioral models; donation intention; donor-based brand equity; integrated behavioral model +2 | 3.00 |
| 290 | Rooney, P. M., Wang, X., & Ottoni-Wilhelm, M. (2021) | 3 | behavioral models; donation intention; donor-based brand equity; integrated behavioral model +2 | 3.00 |
| 291 | Andreoni, James (1990) | 3 | altruism; behavioural intention; impure altruism; social norms +3 | 3.00 |
| 292 | Small, Deborah A., Loewenstein, George & Slovic, Paul (2007) | 3 | altruism; behavioural intention; impure altruism; social norms +3 | 3.00 |
| 293 | Cohen, J. (1994) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 294 | Edwards, W., Lindman, H., & Savage, L. J. (1963) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 295 | Ehrlinger, L., & Wöß, W. (2016) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 296 | Gioia, D. A., Corley, K. G., & Hamilton, A. L. (2013) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 297 | Goodman, S. N. (1999) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 298 | Gruber, T. R. (1993) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 299 | Higgins, J. P. T., Thomas, J., Chandler, J., Cumpston, M., Li, T., Page, M. J., & Welch, V. A. (Hrsg.) (2019) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 300 | Jeffrey, R. C. (1965) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 301 | Mouton, J., & Marais, H. C. (1990) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 302 | SRC-001029 (n.d.) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 303 | Royall, R. M. (1997) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 304 | Suppe, F. (1977) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 305 | Tranfield, D., Denyer, D., & Smart, P. (2003) | 3 | bayesian inference; cumulative knowledge; evidence; evidence aggregation | 3.00 |
| 306 | Salamon and Anheier (1992) | 6 | classification; comparative research; icnpo; nonprofit sector +3 | 2.60 |
| 307 | Akingbola, K. ( (2013) | 3 | collaboration; competition; nonprofit marketing; performance measurement +1 | 2.55 |
| 308 | Bernardi, C. L., & Alhamdan, N. ( (2022) | 3 | collaboration; competition; nonprofit marketing; performance measurement +1 | 2.55 |
| 309 | Felício, J. A., Martins Gonçalves, H., & da Conceição Gonçalves, V. ( (2013) | 3 | collaboration; competition; nonprofit marketing; performance measurement +1 | 2.55 |
| 310 | SRC-000760 (n.d.) | 3 | collaboration; competition; nonprofit marketing; performance measurement +1 | 2.55 |
| 311 | Men, L. R., & Tsai, W. H. S. ( (2014) | 3 | collaboration; competition; nonprofit marketing; performance measurement +1 | 2.55 |
| 312 | Shah, D., & George, M. (2020) | 3 | collaboration; competition; nonprofit marketing; performance measurement +1 | 2.55 |
| 313 | Wymer, W., Knowles, P., & Gomes, R. ( (2014) | 3 | collaboration; competition; nonprofit marketing; performance measurement +1 | 2.55 |
| 314 | C., M., Babar, K., & G., C (2023) | 4 | attitude; charitable giving; cross-cultural validation; donation behavior +5 | 2.30 |
| 315 | Holdershaw et al. (2011) | 4 | attitude; charitable giving; cross-cultural validation; donation behavior +5 | 2.30 |
| 316 | Hyde et al. (2013) | 4 | attitude; charitable giving; cross-cultural validation; donation behavior +5 | 2.30 |
| 317 | Li, H., Kinoshita, T., Chen, J., Xie, J., Luo, S., & Su, D (2024) | 4 | attitude; charitable giving; cross-cultural validation; donation behavior +5 | 2.30 |
| 318 | Metawie, M., & Mostafa, R (2015) | 4 | attitude; charitable giving; cross-cultural validation; donation behavior +5 | 2.30 |
| 319 | Pérez, L., & Egea, P (2019) | 4 | attitude; charitable giving; cross-cultural validation; donation behavior +5 | 2.30 |
| 320 | Santos, R., Campo, R., Cruz, M., Montante, R., & Santos, S (2025) | 4 | attitude; charitable giving; cross-cultural validation; donation behavior +5 | 2.30 |
| 321 | Gardner, B. (2014) | 3 | brand equity; brand familiarity; choice complexity; donation intention +5 | 2.20 |
| 322 | Nogueira, M., Santarém, F., & Gomes, S. (2020) | 3 | brand as heuristic; brand equity; brand equity model; commitment +7 | 2.10 |
| 323 | Sargeant and Woodliffe (2007) | 5 | brand associations; cause commitment; commitment; donation behaviour +15 | 2.05 |
| 324 | Leliveld, M. C., & Risselada, H. (2017) | 2 | donation intention; donor-based brand equity; integrated behavioral model; theory of planned behavior | 2.00 |
| 325 | Powell, K. L., Roberts, G., & Nettle, D. (2012) | 2 | donation intention; donor-based brand equity; integrated behavioral model; theory of planned behavior | 2.00 |
| 326 | SRC-000657 (n.d.) | 2 | donation intention; donor-based brand equity; integrated behavioral model; theory of planned behavior | 2.00 |
| 327 | Ajzen, I. (2001) | 2 | donation intention; donor-based brand equity; integrated behavioral model; theory of planned behavior | 2.00 |
| 328 | Gigerenzer & Goldstein (2002) | 2 | donation intention; donor-based brand equity; integrated behavioral model; theory of planned behavior | 2.00 |
| 329 | Sargeant, Ford & West (2006) | 2 | donation intention; donor-based brand equity; integrated behavioral model; theory of planned behavior | 2.00 |
| 330 | Richter, Schömann et al. (2016) | 2 | donation intention; donor-based brand equity; integrated behavioral model; theory of planned behavior | 2.00 |
| 331 | Randle & Dolnicar (2019) | 2 | donation intention; donor-based brand equity; integrated behavioral model; theory of planned behavior | 2.00 |
| 332 | Wood, W., & Rünger, D. (2016) | 2 | behavioral models; intention-behavior gap | 2.00 |
| 333 | Caviola, L., Schubert, S., & Greene, J. (2021) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 334 | Chan, M., & Feldman, G. (2025) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 335 | Chapman, C., Louis, W., Masser, B., & Thomas, E. F. (2022) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 336 | Etheredge, H. (2021) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 337 | Eyigunlu, M. (2023) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 338 | Faseur, T., De Bock, T., & Timmermans, G. (2025) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 339 | Ferrara, I., & Missios, P. (2020) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 340 | Gabriel, I. (2017) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 341 | Harvey, C., Gordon, J., & Maclean, M. (2020) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 342 | Hill, T. E. (2021) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 343 | Jaafar, S. B. (2025) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 344 | Martin, M. W. (1994) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 345 | McGoey, L. (2021) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 346 | Mukherjee, S. (2013) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 347 | Pearlman, S. (2023) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 348 | Sargeant, A., West, D. C., & Ford, J. B. (2004) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 349 | White, K., Habib, R., & Hardisty, D. J. (2023) | 2 | altruism; behavioural intention; impure altruism; social norms +2 | 2.00 |
| 350 | Balochi, H., Hadizadeh-Talasaz, F., Bahri, N., & Mohammadzadeh, F (2023) | 3 | cultural context; donation intention; perceived behavioural control; subjective norm +1 | 1.75 |
| 351 | Wedel, M., Kannan, P., & Tyser, R. J. (2016) | 3 | cultural context; donation intention; perceived behavioural control; subjective norm +1 | 1.75 |
| 352 | Shaamirova, S., Pulatova, M., & Tursunov, A. (2026) | 3 | cultural context; donation intention; perceived behavioural control; subjective norm +1 | 1.75 |
| 353 | Torrent Sellens, J., Salazar-Concha, C., Ficapal Cusí, P., & Saigí-Rubió, F (2021) | 3 | cultural context; donation intention; perceived behavioural control; subjective norm +1 | 1.75 |
| 354 | Berry (2000) | 5 | brand credibility; brand delivery; brand equity; brand knowledge +9 | 1.70 |
| 355 | Barnard & Ehrenberg (1990) | 3 | behavioural loyalty; brand associations; brand beliefs; brand experience +4 | 1.65 |
| 356 | Laurent et al. (1995) | 3 | brand awareness; longitudinal measurement; market share; measurement interchangeability +4 | 1.65 |
| 357 | Chell, K., Mortimer, G., Masser, B., & Russell–Bennett, R. (2021) | 3 | donation intention; identity salience; loyalty; organizational identification +3 | 1.65 |
| 358 | Fang, D., Fombelle, P. W., & Bolton, R. N. (2020) | 3 | donation intention; identity salience; loyalty; organizational identification +3 | 1.65 |
| 359 | SRC-000527 (n.d.) | 3 | donation intention; identity salience; loyalty; organizational identification +3 | 1.65 |
| 360 | Lai, C.-S., & Nguyen, D. T. (2024) | 3 | donation intention; identity salience; loyalty; organizational identification +3 | 1.65 |
| 361 | Taylor, J. A., & Miller Stevens, K. (2018) | 3 | donation intention; identity salience; loyalty; organizational identification +3 | 1.65 |
| 362 | Tidwell, M. (2005) | 3 | donation intention; identity salience; loyalty; organizational identification +3 | 1.65 |
| 363 | Botner, K. A., Mishra, A., & Mishra, H. (2015) | 3 | brand orientation; brand strategy; fundraising; organizational performance | 1.65 |
| 364 | Brady, E., Brace-Govan, J., Brennan, L., & Conduit, J. (2011) | 3 | brand orientation; brand strategy; fundraising; organizational performance | 1.65 |
| 365 | Ewing & Napoli (2005) | 3 | brand orientation; brand strategy; fundraising; organizational performance | 1.65 |
| 366 | Jones, R. (2005) | 2 | brand equity; brand equity model; construct validity; generalizability +3 | 1.55 |
| 367 | Naidoo, C., & Abratt, R. (2017) | 2 | brand equity; brand equity model; construct validity; generalizability +3 | 1.55 |
| 368 | Rindfleisch, A., Malter, A., Ganesan, S., & Moorman, C. (2008) | 2 | brand equity; brand equity model; construct validity; generalizability +3 | 1.55 |
| 369 | Yen, W.-H., Caskey, D., & Warden, C. A. (2022) | 2 | brand equity; brand equity model; construct validity; generalizability +3 | 1.55 |
| 370 | Ajzen (1991) | 3 | attitude; brand equity; brand familiarity; choice complexity +9 | 1.40 |
| 371 | Sargeant, A. & Lee, S. (2004) | 3 | brand awareness; brand equity; brand familiarity; brand image +6 | 1.30 |
| 372 | Fournier (1998) | 4 | brand differentiation; brand personality; brand preference; brand relationship +10 | 1.15 |
| 373 | Sargeant et al. (2007) | 2 | brand personality; donation intention; identity congruence; nonprofit brand equity +1 | 1.10 |
| 374 | Neumayr and Handy (2017) | 2 | austrian giving context; charitable giving; donation amount; donation incidence | 1.10 |
| 375 | Marin, Ruiz, & Rubio (2008) | 2 | donor loyalty; identity salience; organizational identification | 1.10 |
| 376 | Onkovist & Shaw (1989) | 2 | brand equity; brand knowledge; intangibility; perceived risk +3 | 1.10 |
| 377 | Gardberg, N. A., Zyglidopoulos, S. C., Symeou, P., & Schepers, D. H. (2019) | 2 | brand association; brand awareness; brand equity; cross-cultural validation +2 | 1.10 |
| 378 | Gleasure, R., & Feller, J. (2016) | 2 | brand association; brand awareness; brand equity; cross-cultural validation +2 | 1.10 |
| 379 | Holiday, S., Hayes, J. L., Britt, B. C., & Lyu, Y. (2020) | 2 | brand association; brand awareness; brand equity; cross-cultural validation +2 | 1.10 |
| 380 | Luffarelli, J., Delre, S., & Landgraf, P. (2022) | 2 | brand association; brand awareness; brand equity; cross-cultural validation +2 | 1.10 |
| 381 | Rama, A., Ali, H., & Syafruddin, S. (2026) | 2 | brand association; brand awareness; brand equity; cross-cultural validation +2 | 1.10 |
| 382 | Wu, X., Wu, T., Guo, X., & Yang, H. ( (2025) | 2 | brand association; brand awareness; brand equity; cross-cultural validation +2 | 1.10 |
| 383 | Bekkers (2010) | 1 | donation behavior; donor profile | 1.00 |
| 384 | Piper & Schnepf (2008) | 1 | donation behavior; donor profile | 1.00 |
| 385 | Churchill, Gilbert A., Jr. (1979) | 1 | brand attachment; brand attitude; brand emotions; brand equity +3 | 1.00 |
| 386 | Rossiter, John R. (2012) | 1 | brand attachment; brand attitude; brand emotions; brand equity +3 | 1.00 |
| 387 | Edell, J., & Burke, M. ( (1987) | 1 | brand attachment; brand attitude; brand emotions; brand equity +3 | 1.00 |
| 388 | Berkey, Brian (2018) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 389 | Cordelli, Chiara (2016) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 390 | Cordelli, Chiara (2020) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 391 | Darwall, Stephen (2024) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 392 | Friedman, Milton (1970) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 393 | Heath, Joseph (2014) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 394 | Hill, Jr., Thomas E. (2018) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 395 | Lechterman, T. M. (2022) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 396 | Lechterman, T. M., Saunders-Hastings, E., & Reich, R. (2024) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 397 | MacAskill, William (2019) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 398 | Mauss, Marcel (1990) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 399 | Nozick, Robert (1974) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 400 | Pettit, Philip (1997) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 401 | Pevnick, Ryan (2013) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 402 | Pevnick, Ryan (2016) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 403 | Reich, Rob (2018) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 404 | Rubenstein, Jennifer (2022) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 405 | Saunders-Hastings, Emma (2022) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 406 | Setiya, Kieran (2022) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 407 | Singer, Peter (1972) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 408 | Singer, Peter (2019) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 409 | Tarsney, Christian (2023) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 410 | Taylor, Robert S. (2018) | 1 | impure altruism; symbolic capital; warm glow giving | 1.00 |
| 411 | Fishbein and Yzer (2003) | 3 | behavioural enactment; brand equity; brand familiarity; choice complexity +8 | 0.95 |
| 412 | Shrestha et al. (2023) | 2 | brand equity; brand familiarity; choice complexity; commitment +4 | 0.75 |
| 413 | Theurer et al. (2018) | 2 | brand equity; brand familiarity; choice complexity; employer branding +4 | 0.75 |
| 414 | Hankinson, Philippa (2001) | 2 | cross-cultural validation; generalizability; identity; self-concept +3 | 0.75 |
| 415 | Romaniuk et al. (2004) | 2 | brand awareness; managerial decision-making; measurement noise; measurement reliability +2 | 0.75 |
| 416 | Erdem & Swait (2004) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 417 | Aaker, D. A., & Joachimsthaler, E. (2000) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 418 | Vargo & Lusch (2004) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 419 | Kohli, A.K. and Jaworski, B.J (1990) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 420 | Gronroos, C (1994) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 421 | SRC-000820 (n.d.) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 422 | Berry, L.L (1995) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 423 | Duncan, T. and Moriarty, S.E (1998) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 424 | Parasuraman, A., Zeithaml, V. A., & Berry, L. L. (1988) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 425 | SRC-000823 (n.d.) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 426 | Hunt, S.D. and Morgan, R.M (1995) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 427 | Achrol, R.S. and Kotler, P (1999) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 428 | Brodie, R.J., Whittome, J.R.M., and Brush, G.J. (2006) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 429 | SRC-000826 (n.d.) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 430 | Aaker, D (1992) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 431 | de Chernatony, L., & Riley, F. D. O. (1998) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 432 | Urde (1999) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 433 | Wong, H.Y. and Merrilees, B (2007) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 434 | de Chernatony, L. (1999) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 435 | SRC-000831 (n.d.) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 436 | SRC-000832 (n.d.) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 437 | Ulrich, D. and Smallwood, N (2007) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 438 | Delgado-Ballester, Elena; Munuera-Alemán, José Luis (2005) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 439 | Shostack, G.L (1987) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 440 | Berry, L (1999) | 3 | brand credibility; brand delivery; brand promise; organisational capability +2 | 0.60 |
| 441 | Bennett & Gabriel (2003) | 1 | brand equity; donation intention; donor loyalty; fundraising success | 0.55 |
| 442 | Sargeant & Woodliffe (2007) | 1 | brand equity; commitment; nonprofit brand; trust | 0.55 |
| 443 | Sargeant (2001) | 1 | brand associations; donor relationships; nonprofit brand equity; trust | 0.55 |
| 444 | Homburg, Wieseke, and Hoyer (2009) | 1 | customer loyalty; customer-company identification | 0.55 |
| 445 | Anderson & Sullivan (1993) | 1 | customer satisfaction; dynamic expectations; expectations; learning | 0.55 |
| 446 | Hoyer & Brown (1990) | 1 | brand familiarity; brand salience; choice; heuristic decision-making +1 | 0.55 |
| 447 | Andreasen, A. R. (2012) | 1 | identity; self-concept; symbolic consumption; volunteer choice | 0.55 |
| 448 | Barwise, P., & Meehan, S. (2004) | 1 | identity; self-concept; symbolic consumption; volunteer choice | 0.55 |
| 449 | Mandel, N., & Johnson, E. J. ( (2002) | 1 | identity; self-concept; symbolic consumption; volunteer choice | 0.55 |
| 450 | Sargeant, A. (2009) | 1 | identity; self-concept; symbolic consumption; volunteer choice | 0.55 |
| 451 | Exploring awareness–confidence relationship
Kramer RM (2000) | 1 | brand equity; hierarchy of effects; nonprofit awareness; public confidence | 0.55 |
| 452 | Ou, J., Wong, I., Prentice, C., & Liu, M. (2020) | 1 | brand as heuristic; commitment; trust; uncertainty reduction | 0.55 |
| 453 | Park, C.-I., & Namkung, Y. (2022) | 1 | brand as heuristic; commitment; trust; uncertainty reduction | 0.55 |
| 454 | Samballkhundev, S., Choe, Y., & Kim, D.-H. (2024) | 1 | brand as heuristic; commitment; trust; uncertainty reduction | 0.55 |
| 455 | Shen, Z., Li, H., & Zhang, Y. (2025) | 1 | brand as heuristic; commitment; trust; uncertainty reduction | 0.55 |
| 456 | Schmitt (1999) | 2 | brand equity; emotional branding; emotional resonance; experiential branding +5 | 0.40 |
| 457 | Harris and de Chernatony (2001) | 2 | employee buy-in; internal brand socialization; internal branding; internal communication +3 | 0.40 |
| 458 | Sirgy (1982) | 2 | brand personality; brand preference; choice behaviour; donor behaviour +2 | 0.40 |
| 459 | Burmann & Zeplin (2005) | 2 | brand effectiveness; brand identity; brand image; measurement +1 | 0.40 |
| 460 | Keller and Lehmann (2003) | 1 | attitudes; awareness; brand building; stakeholder mindset +1 | 0.20 |
| 461 | Laidler-Kylander, Quelch, and Simonin (2007) | 1 | donation channels; enactment; environmental constraints; frictionless giving +1 | 0.20 |
| 462 | Yoo, Boonghee; Donthu, Naveen (2001) | 1 | brand equity; measurement; nonprofit customer-based brand equity; scale development | 0.20 |
| 463 | Bridson and Evans (2004) | 1 | behavioural construct; brand orientation; brand-building activities; internal structures | 0.20 |
| 464 | Wymer et al. (2021) | 1 | donor-based brand equity; identification; mission alignment; value congruence | 0.20 |
| 465 | Sundar et al. (2014) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 466 | Netemeyer et al. (2004) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 467 | Bekkers & Wiepking (2011) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 468 | Breeze (2013) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 469 | Barman (2007) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 470 | Connelly et al. (2011) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 471 | Ostrower (1995) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 472 | Mette (2013) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 473 | Charbonneau & Smith (2012) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 474 | Gillespie & Hillyer (2002) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 475 | Vogel (2018) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 476 | Schervish (1997) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 477 | Taylor (2005) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 478 | Mato-Santiso, V., Maseda-Moreno, A., & Iturralde-Jaiker, T. (2021) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 479 | Morgan and Hunt (1994) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 480 | Karakayali (2017) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 481 | Healy (2000) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 482 | Busby (2010) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 483 | Suarez & Valentin (2019) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 484 | Chad, Paul and Motion, Judy and Kyriazis, Elias (2013) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 485 | Hersberger-Langloh, Sophie (2020) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 486 | Spence (1973) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 487 | Cambefort, Marine and Roux, Elyette (2019) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 488 | Fisher, Robert J. and Vandenbosch, Mark and Antia, Kersi D. (2008) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 489 | Gabrielli, Veronica and Baghi, Ilaria and Bergianti, Francesca (2021) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 490 | Chad, Paul and Kyriazis, Elias and Motion, Judy (2013) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 491 | Strahilevitz, Michal and Myers, John G. (1998) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 492 | Green, Corliss L. and Webb, Deborah J. (1997) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 493 | Gershon, Rachel and Cryder, Cynthia (2017) | 1 | brand equity; brand familiarity; choice complexity; information overload +1 | 0.20 |
| 494 | Aaker, J. L. (1997) | 1 | brand personality; construct dimensionality; nonprofit brand equity | 0.20 |
| 495 | Liao-Troth (2001) | 1 | affective commitment; employees; organizational justice; volunteers | 0.20 |
| 496 | Anderson, D. R., Sweeney, D. J., & Williams, T. A. (2007) | 1 | cross-cultural validation; generalizability; volunteer brand equity | 0.20 |
| 497 | Castro, C. B., Armario, E. M., & Del Rio, M. E. S. (2005) | 1 | cross-cultural validation; generalizability; volunteer brand equity | 0.20 |
| 498 | Liu, G.; Chapleo, C.; Ko, W. W.; Ngugi, I. K. (2015) | 1 | cross-cultural validation; generalizability; volunteer brand equity | 0.20 |
| 499 | Riecken, G., Babakus, E., & Yavas, U. ( (1994) | 1 | cross-cultural validation; generalizability; volunteer brand equity | 0.20 |
| 500 | Mael, F., & Ashforth, B. E. (1992) | 1 | measurement scale; organizational identification | 0.20 |
| 501 | Thomson, Matthew; MacInnis, Deborah J.; Park, C. Whan (2005) | 1 | attachment measurement; brand attachment; emotion-based measurement | 0.20 |
| 502 | Alba & Hutchinson (1987) | 1 | brand familiarity; cognitive effort; heuristic processing; knowledge structure | 0.20 |
| 503 | Styles & Ambler (1995) | 1 | brand description; holistic branding; marketing mix; strategic alignment | 0.20 |
| 504 | Campbell, D. T., & Fiske, D. W. (1959) | 1 | brand equity; brand loyalty; construct dimensionality | 0.20 |
| 505 | Graça, S. S. (2022) | 1 | awareness; brand equity; commitment; perceived quality +1 | 0.20 |
| 506 | Hume, M., & Mort, G. S. (2010) | 1 | awareness; brand equity; commitment; perceived quality +1 | 0.20 |
| 507 | Jibran, R., Rasul, M., Hussain, M., Shahid, R., & Yasin, M. (2025) | 1 | awareness; brand equity; commitment; perceived quality +1 | 0.20 |
| 508 | Jones, J. L., & Shandiz, M. (2015) | 1 | awareness; brand equity; commitment; perceived quality +1 | 0.20 |
| 509 | Kim, M., Yoon, Y., & Zhang, J. J. (2023) | 1 | awareness; brand equity; commitment; perceived quality +1 | 0.20 |
| 510 | Kusuma, I. E. T., Yasmari, N. N. W., Agung, A., & Landra, N. (2021) | 1 | awareness; brand equity; commitment; perceived quality +1 | 0.20 |
| 511 | Marcos, A., & Coelho, A. (2021) | 1 | awareness; brand equity; commitment; perceived quality +1 | 0.20 |
| 512 | Min, D. (2022) | 1 | awareness; brand equity; commitment; perceived quality +1 | 0.20 |
| 513 | Oktaviani, N., & Nisa, P. C. (2024) | 1 | awareness; brand equity; commitment; perceived quality +1 | 0.20 |
| 514 | Shabbir, H., Palihawadana, D., & Thwaites, D. (2007) | 1 | awareness; brand equity; commitment; perceived quality +1 | 0.20 |
| 515 | Andreoni, J., & Rao, J. M (2011) | 1 | affordance; attention; solicitation | 0.20 |
| 516 | Harrington, M., Sweeney, M. R., Bailie, K., Morris, K., Kennedy, A., Boilson, A., O’Riordan, J., & Staines, A (2007) | 1 | affordance; attention; solicitation | 0.20 |
| 517 | Riecken, G., & Yavas, U (2005) | 1 | affordance; attention; solicitation | 0.20 |

## 4. Reference List (Verified Sources Only)

_Only sources that appear in at least one verified (`supported`) EVID are listed. Sorted alphabetically by first author._

- ( (2025). *https://doi.org/10.1002/nba.33060*. *Nonprofit Business Advisor*, *2025*(434), 7-12. https://doi.org/10.1002/nba.33060
- Aaker (1991). *MEASURING BRAND EQUITY ACROSS PRODUCTS AND MARKETS*. *California Management Review*, *38*(3), 102�120. https://doi.org/10.2307/41165845
- Aaker, D (1992). *The value of brand equity*. *Journal of Business Strategy*, *13*(4), 27-32. https://doi.org/10.1108/eb039503
- Aaker, D. A., & Joachimsthaler, E. (2000). *Brand Leadership
Leadership'*. Free Press.
- Aaker, David A. (1991). *Managing brand equity : capitalizing on the value of a brand name.*. *New York, NY*, *38*(3), 112.
- Aaker, J. L. (1997). *Dimensions of brand personality*. *SSRN Electronic Journal*. https://doi.org/10.2139/ssrn.945432
- Abdullah, M., Sarfraz, M., Arif, A., & Azam, A (2018). *AN EXTENSION OF THE THEORY OF PLANNED BEHAVIOR TOWARDS BRAND EQUITY AND PREMIUM PRICE. *Polish Journal of Management Studies*. <https://doi.org/10.17512/pjms.2018.18.1.02>*. *Polish Journal of Management Studies*, *18*(1), 20-32. https://doi.org/10.17512/pjms.2018.18.1.02
- Achrol, R.S. & Kotler, P (1999). *Marketing in
the network economy*. *Journal of Marketing*, *63*, 146. https://doi.org/10.2307/1252108
- Adomavičiūtė & Urbonavičius (2023). *Does the intention to purchase cause‐related products compared to charity donations indicate higher morality?*. *Journal of Philanthropy and Marketing*, *28*(4). https://doi.org/10.1002/nvsm.1811
- Ajzen (1991). *The Theory of Planned Behavior*. *Organizational Behavior and Human Decision Processes*, *50*(2), 179--211. https://doi.org/10.1016/0749-5978(91)90020-T
- Ajzen, I (2016). *Consumer attitudes and behavior: the theory of planned behavior applied to food consumption decisions. *, 70*, 121-138. <https://doi.org/10.13128/rea-18003>*. *Italian Review of Agricultural Economics*, *70*(2), 121-138. https://doi.org/10.13128/rea-18003
- Ajzen, I. (2002). *Residual Effects of Past on Later Behavior: Habituation and Reasoned Action Perspectives*. *Personality and Social Psychology Review*. https://doi.org/10.1207/s15327957pspr0602_02
- Ajzen, I. (2001). *Nature and operation of attitudes*. *Annual review of psychology*. https://doi.org/10.1146/annurev.psych.52.1.27
- Akingbola, K. ( (2013). *A model of strategic nonprofit human resource management*. *Voluntas:
  International Journal of Voluntary and Nonprofit Organizations*. https://doi.org/10.1016/j.brq.2017.01.001
- Al-Shamali, S., & Kashif, M (2023). *Intentions and donations: monetary charity in Kuwait during the COVID-19 pandemic. *Journal of Islamic Accounting and Business Research*. <https://doi.org/10.1108/jiabr-09-2021-0249>*. *Journal of Islamic Accounting and Business Research*, *15*(1), 79-99. https://doi.org/10.1108/jiabr-09-2021-0249
- Alba & Hutchinson (1987). *Dimensions of consumer expertise*. *Journal of Consumer Research*, *13*(4), 411–454. https://doi.org/10.1086/209080
- Algharabat, R., Rana, N., Alalwan, A., Baabdullah, A., & Gupta, A (2020). *Investigating the antecedents of customer brand engagement and consumer-based brand equity in social media. *Journal of Retailing and Consumer Services, 53*. <https://doi.org/10.1016/j.jretconser.2019.01.016>*. *Journal of Retailing and Consumer Services*, *53*, 101767. https://doi.org/10.1016/j.jretconser.2019.01.016
- Alhidari, I., Veludo-De-Oliveira, T., Yousafzai, S., & Yani-De-Soriano, M (2018). *Modeling the Effect of Multidimensional Trust on Individual Monetary Donations to Charitable Organizations. *Nonprofit and Voluntary Sector Quarterly, 47*, 623 - 644. <https://doi.org/10.1177/0899764017753559>*. *Nonprofit and Voluntary Sector Quarterly*, *47*(3), 623-644. https://doi.org/10.1177/0899764017753559
- Ali, et al. (2022). *The effect of charity brand experience on donors behavioral intentions: The mediating role of charity brand personality and donors satisfaction*. *International Review on Public and Nonprofit Marketing*, *20*(4), 875903. https://doi.org/10.1007/s12208-022-00356-0
- Amonhaemanon, D., Khongkaew, P., Akartwipart, A., & Thamthanakoon, N. (2024). *Distinguishing altruism from warm glow: psychological motivations for money donations to Thailand’s Buddhist society*. *Review of Behavioral Finance*. https://doi.org/10.1108/rbf-07-2024-0185
- Anderson & Sullivan (1993). *Imagined Communities: Reflections on the Origin and Spread of Nationalism*. *Marketing Science*, *12*(2), 125–143. https://doi.org/10.1287/mksc.12.2.125
- Anderson, D. R., Sweeney, D. J., & Williams, T. A. (2007). *Estatística Aplicada à Administração e Economia*. Thomson.
- Andreasen, A. R. (2012). *Rethinking the relationship between social/nonprofit marketing and commercial marketing*. *Journal of Public Policy & Marketing*, *31*(1), 36–41. https://doi.org/10.1509/jppm.09.035
- Andreoni (1990). *Philanthropy*. *Handbook of the Economics of Giving, Altruism and Reciprocity*, *2*(401), 1201--1269. https://doi.org/10.1016/S1574-0714(06)02018-5
- Andreoni, J (1989). *Giving with Impure Altruism: Applications to Charity and Ricardian Equivalence. *Journal of Political Economy, 97*, 1447 - 1458. <https://doi.org/10.1086/261662>*. *Journal of Political Economy*, *97*(6), 1447-1458. https://doi.org/10.1086/261662
- Andreoni, J., & Rao, J. M (2011). *The power of asking: How communication affects selfishness, empathy, and altruism*. *Journal of Public Economics*, *95*(7-8), 513-520. https://doi.org/10.1016/j.jpubeco.2010.11.003
- Andreoni, James (1990). *Impure Altruism and Donations to Public Goods: A Theory of Warm-Glow Giving*. *The Economic Journal*, *100*(401), 464-477. https://doi.org/10.2307/2234133
- Anggraeni & Kuklienė (2024). *Multidimensional Analysis of Charitable Behavior: Integration of Altruism, Religiosity, and Economy in Global Social Context*. *Potret Pemikiran*. https://doi.org/10.30984/pp.v28i2.3250
- Ansary, A., & Hashim, N. N. H. N (2018). *Brand image and equity: the mediating role of brand equity drivers and moderating effects of product type and word of mouth. *Review of Managerial Science, 12*, 969-1002. <https://doi.org/10.1007/s11846-017-0235-2>*. *Review of Managerial Science*, *12*(4), 969-1002. https://doi.org/10.1007/s11846-017-0235-2
- Anselmsson, et al. (2017). *An Integrated Retailer Image and Brand Equity Framework: Re-examining, Extending, and Restructuring Retailer Brand Equity*. *Journal of Retailing and Consumer Services*, *38*, 194--203. https://doi.org/10.1016/j.jretconser.2017.06.007
- Anshori, M. Y., Karya, D. F., Rahmania, A. A., & Elfita, R. A. (2022). *Analisis Loyalitas Donatur dan Brand Trust: Studi pada YDSF Al-Falah Surabaya*. *Journal of Management and Business Review*. https://doi.org/10.34149/jmbr.v19i2.316
- Baalbaki, S., & Guzmán, F (2016). *A consumer-perceived consumer-based brand equity scale. *Journal of Brand Management, 23*, 229-251. <https://doi.org/10.1057/bm.2016.11>*. *Journal of Brand Management*, *23*(3), 229-251. https://doi.org/10.1057/bm.2016.11
- Baghi, I. & Gabrielli, V (2018). *“Brand prominence in cause-related marketing: luxury versus non-luxury”, Journal of Product & Brand Management, Vol. 27 No. 6, pp. 716-731*. *Bendapudi, N., Singh, S. and Bendapudi, V. (1996), “Enhancing helping behavior: an integrative framework for promotion planning”, Journal of Marketing, Vol*, *27*(6), 716-731. https://doi.org/10.1108/jpbm-07-2017-1512
- Balaskas, S., Koutroumani, M., & Rigou, M (2024). *The Mediating Role of Emotional Arousal and Donation Anxiety on Blood Donation Intentions: Expanding on the Theory of Planned Behavior. *Behavioral Sciences, 14*. <https://doi.org/10.3390/bs14030242>*. *Behavioral Sciences*, *14*(3), 242. https://doi.org/10.3390/bs14030242
- Balochi, H., Hadizadeh-Talasaz, F., Bahri, N., & Mohammadzadeh, F (2023). *Applying the theory of planned behavior for prediction of oocyte donation intention among Iranian women*. *BMC Pregnancy and Childbirth*. https://doi.org/10.1186/s12884-023-05836-7
- Bang, H., Lee, C., Won, D., Chiu, W., & Chen, L. (2022). *Exploring Attitudes of Mandatory Volunteers: The Role of Perceived Organizational Support, Role Clarity, and Self-Efficacy Toward Service*. *Nonprofit and Voluntary Sector Quarterly*. https://doi.org/10.1177/08997640221093797
- Barman (2007). *Untitled*.
- Barman, E. (2016). *Varieties of Field Theory and the Sociology of the Non profit Sector*. *Sociology Compass*. https://doi.org/10.1111/soc4.12377
- Barnard & Ehrenberg (1990). *“Robust measures of consumer brand*. *Journal of Marketing Research*, *27*(4), 477. https://doi.org/10.2307/3172632
- Barwise (1993). *Brand equity: Snark or boojum?*. *International Journal of Research in Marketing*, *10*(1), 93-104. https://doi.org/10.1016/0167-8116(93)90036-x
- Barwise, P., & Meehan, S. (2004). *Don’t be unique, be better*. *MIT Sloan Management Review*, *‘45’*(Summer 2004), 23-26. https://doi.org/‘’
- Bekkers (2010). *Untitled*.
- Bekkers & Wiepking (2011). *Untitled*. *Nonprofit and Voluntary Sector Quarterly*. https://doi.org/10.1002/nvsm.428
- Bekkers & Wiepking (2011). *A Literature Review of Empirical Studies of Philanthropy*. *Nonprofit and Voluntary Sector Quarterly*, *40*(5), 924--973. https://doi.org/10.1177/0899764010380927
- Bendixen, M., Bukasa, K. A., & Abratt, R (2004). *Brand equity in the business-to-business market. *Industrial Marketing Management, 33*, 371-380. <https://doi.org/10.1016/j.indmarman.2003.10.001>*. *Industrial Marketing Management*, *33*(5), 371-380. https://doi.org/10.1016/j.indmarman.2003.10.001
- Benli, B., & Kocaman, R. (2025). *Key Drivers Underpinning the Donation Behavior: A Systematic Literature Review and Agenda for Future Research Using the TCCM Framework*. *International Journal of Consumer Studies*. https://doi.org/10.1111/ijcs.70157
- Bennett & Gabriel (2003). *Image and Reputational Characteristics of UK Charitable Organizations: An Empirical Study*. *Corporate Reputation Review*, *6*(3), 276--289. https://doi.org/10.1057/palgrave.crr.1540206
- Berkey, Brian (2018). *Untitled*.
- Bernardi, C. L., & Alhamdan, N. ( (2022). *Social media analytics for nonprofit marketing:
  #Downsyndrome on twitter and instagram*. *Journal of Philanthropy and Marketing*. https://doi.org/10.1002/nvsm.1739
- Berry (2000). *Cultivating Service Brand Equity*. *Journal of the Academy of Marketing Science*, *28*(1), 128-137. https://doi.org/10.1177/0092070300281012
- Berry, L (1999). *Discovering the Soul of Service*. *New
York: Free Press*, *49*(2), 148-151. https://doi.org/10.1111/j.1460-2466.1999.tb02800.x
- Berry, L.L (1995). *Relationship marketing of services: Growing interest, emerging perspectives*. *Journal
of Academy of Marketing Science*, *23*(4), 236-245. https://doi.org/10.1177/009207039502300402
- Bianchi, et al. (2023). *Is the warm glow actually warm? An experimental investigation into the nature and determinants of warm glow feelings*. *International Journal of Wellbeing*. https://doi.org/10.5502/ijw.v13i3.2565
- Bilgin & Kethüda (2022). *Charity Social Media Marketing and Its Influence on Charity Brand Image, Brand Trust, and Donation Intention*. *VOLUNTAS: International Journal of Voluntary and Nonprofit Organizations*, *33*, 1091--1102. https://doi.org/10.1007/s11266-021-00426-7
- Bird, M., Channon, C., & Ehrenberg, A. S. C. (1970). *Brand image and brand usage*. *Journal of Marketing Research*, *7*(3), 307-314.
- Biscaia, R., Ross, S., Yoshida, M., Correia, A., Rosado, A., & Marôco, J (2016). *Investigating the role of fan club membership on perceptions of team brand equity in football. *Sport Management Review, 19*, 157-170. <https://doi.org/10.1016/j.smr.2015.02.001>*. *Sport Management Review*, *19*(2), 157-170. https://doi.org/10.1016/j.smr.2015.02.001
- Bischoff, I., & Krauskopf, T (2015). *Warm glow of giving collectively – An experimental study. *Journal of Economic Psychology, 51*, 210-218. <https://doi.org/10.1016/j.joep.2015.09.001>*. *Journal of Economic Psychology*, *51*, 210-218. https://doi.org/10.1016/j.joep.2015.09.001
- Blake, P (2018). *Giving what one should: explanations for the knowledge-behavior gap for altruistic giving.. *Current opinion in psychology, 20*, 1-5. <https://doi.org/10.1016/j.copsyc.2017.07.041>*. *Current Opinion in Psychology*, *20*, 1-5. https://doi.org/10.1016/j.copsyc.2017.07.041
- Blanco, et al. (2021). *Substitution of social sustainability concerns under the Covid-19 pandemic*. *Ecological Economics*, *192*, 107259-107259. https://doi.org/10.1016/j.ecolecon.2021.107259
- Boenigk & Becker (2016). *Toward the Importance of Nonprofit Brand Equity: Results from a Study of German Nonprofit Organizations*. *Nonprofit Management and Leadership*, *27*(2), 181�198. https://doi.org/10.1002/nml.21233
- Boenigk & Helmig (2013). *Why Do Donors Donate?*. *Journal of Service Research*, *16*(4), 533--548. https://doi.org/10.1177/1094670513486169
- Botner, K. A., Mishra, A., & Mishra, H. (2015). *What's in a Message? The Longitudinal Influence of a Supportive versus Combative Orientation on the Performance of Nonprofits*. *Journal of Marketing Research*. https://doi.org/10.1509/jmr.13.0211
- Boukis, A., & Christodoulides, G (2018). *Investigating Key Antecedents and Outcomes of Employee‐based Brand Equity. *European Management Review*. <https://doi.org/10.1111/emre.12327>*. *European Management Review*, *17*(1), 41-55. https://doi.org/10.1111/emre.12327
- Brady, E., Brace-Govan, J., Brennan, L., & Conduit, J. (2011). *Market orientation and marketing in nonprofit organizations. Indications for fundraising from Victoria*. *International Journal of Nonprofit and Voluntary Sector Marketing*. https://doi.org/10.1002/nvsm.403
- Breeze (2013). *Untitled*.
- Bridson & Evans (2004). *The Secret to a Fashion Advantage is Brand Orientation*. *International Journal of Retail and Distribution Management*, *32*(8), 403–.
- Brodie, R.J., Whittome, J.R.M., & Brush, G.J. (2006). *The service brand and the service-dominant logic: missing fundamental premise or the need for stronger theory?*. *Marketing Theory*, *6*(3), 363-379. https://doi.org/10.1177/1470593106066797
- Buil, de Chernatony, & Martínez (2008). *A cross--national validation of the consumer--based brand equity scale*. *Journal of Product \& Brand Management*, *17*(6), 384--392. https://doi.org/10.1108/10610420810904121
- Buil, I., Martínez, E., & Chernatony, L (2013). *The influence of brand equity on consumer responses. *Journal of Consumer Marketing, 30*, 62-74. <https://doi.org/10.1108/07363761311290849>*. *Journal of Consumer Marketing*, *30*(1), 62-74. https://doi.org/10.1108/07363761311290849
- Burmann & Zeplin (2005). *Building brand commitment: a behavioural approach to internal measurement brand management*. *Journal of Brand Management*, *12*(4), 279–300. https://doi.org/10.1057/palgrave.bm.2540223
- Burmann, et al. (2009). *Towards an identity-based brand equity model*. *Journal of Business Research*, *62*(3), 390�397. https://doi.org/10.1016/j.jbusres.2008.06.009
- Busby (2010). *Untitled*. *Health:*.
- Butt, M., Mushtaq, S., Afzal, A., Khong, K., Ong, F., & Ng, P (2017). *Integrating Behavioural and Branding Perspectives to Maximize Green Brand Equity: A Holistic Approach. *Business Strategy and The Environment, 26*, 507-520. <https://doi.org/10.1002/bse.1933>*. *Business Strategy and the Environment*, *26*(4), 507-520. https://doi.org/10.1002/bse.1933
- C., M., Babar, K., & G., C (2023). *Donors Behaviour towards Donation Based Crowdfunding: An Empirical Study using Extended Theory of Planned Behaviour. *Journal of Commerce and Accounting Research*. <https://doi.org/10.21863/jcar/2024.13.1.003>*. *Journal of Commerce and Accounting Research*, *13*(1), 24-34. https://doi.org/10.21863/jcar/2024.13.1.003
- Cambefort, Marine & Roux, Elyette (2019). *A typology of the perceived risks in the context of consumer brand resistance*. *Journal of Product &amp; Brand Management*, *28*(5), 575-585. https://doi.org/10.1108/jpbm-03-2018-1792
- Campbell, D. T., & Fiske, D. W. (1959). *Convergent and discriminant validation by the multitrait-multimethod matrix*. *Psychological Bulletin*, *56*(2), 81–105. https://doi.org/10.1037/h0046016
- Carpenter, J. (2021). *The shape of warm glow: Field experimental evidence from a fundraiser*. *Journal of Economic Behavior & Organization*. https://doi.org/https://doi.org/10.1016/j.jebo.2021.09.020
- Carroll, A., & Shabana, K. (2010). *The Business Case for Corporate Social Responsibility: A Review of Concepts, Research and Practice*. *International Journal of Management Reviews*. https://doi.org/10.1111/j.1468-2370.2009.00275.x
- Castro, C. B., Armario, E. M., & Del Rio, M. E. S. (2005). *Consequences of market orientation for customers and employees*. *European Journal of Marketing*. https://doi.org/10.1108/03090560510590755
- Caviola, L., Schubert, S., & Greene, J. (2021). *The Psychology of (In)Effective Altruism*. *Trends in cognitive sciences*. https://doi.org/10.1016/j.tics.2021.03.015
- Chaabouni, et al. (2020). *Cause-related marketing: scepticism and warm glow as impacts of donation size on purchase intention*. *International Review on Public and Nonprofit Marketing*, *18*, 129--150. https://doi.org/10.1007/s12208-020-00262-3
- Chad, Paul & Kyriazis, Elias & Motion, Judy (2013). *Development of a Market Orientation Research Agenda for the Nonprofit Sector*. *Journal of Nonprofit &amp; Public Sector Marketing*, *25*(1), 1-27. https://doi.org/10.1080/10495142.2013.759814
- Chad, Paul & Motion, Judy & Kyriazis, Elias (2013). *A Praxis Framework for Implementing Market Orientation Into Charities*. *Journal of Nonprofit &amp; Public Sector Marketing*, *25*(1), 28-55. https://doi.org/10.1080/10495142.2013.759816
- Chan, M., & Feldman, G. (2025). *Factors impacting effective altruism*. *Royal Society Open Science, 12*.
- Chapleo, C. (2015). *Brand ‘infrastructure’ in non-profit organizations: challenges to successful brand building?*. *Journal of Marketing Communications*. https://doi.org/10.1080/13527266.2012.741609
- Chapman et al. (2022). *Charitable Triad Theory: How Donors, Beneficiaries, and Fundraisers Influence Charitable Giving*. *Psychology \& Marketing*, *39*(9), 1827--1848. https://doi.org/10.1002/mar.21701
- Chapman, C., Hornsey, M., & Gillespie, N. (2021). *To What Extent Is Trust a Prerequisite for Charitable Giving? A Systematic Review and Meta-Analysis*. *Nonprofit and Voluntary Sector Quarterly*. https://doi.org/https://doi.org/10.1177/08997640211003250
- Chapman, C., Louis, W., Masser, B., & Thomas, E. F. (2022). *Charitable Triad Theory*. *Psychology & Marketing*.
- Chapman, C., Spence, J. L., Hornsey, M., & Dixon, L. J. (2025). *Social Identification and Charitable Giving: A Systematic Review and Meta-Analysis*. *Nonprofit and Voluntary Sector Quarterly*. https://doi.org/https://doi.org/10.1177/08997640251317403
- Charbonneau & Smith (2012). *Untitled*. *Sociology of Health & Illness*.
- Chatzipanagiotou, et al. (2019). *Managing the Consumer-Based Brand Equity Process: A Cross-Cultural Perspective*. *International Business Review*, *28*(2), 328--343. https://doi.org/10.1016/j.ibusrev.2018.10.005
- Chatzipanagiotou, et al. (2025). *Managing Brand Assets Internally: Turning Employees Into an Integral Source of Brand Equity*. *British Journal of Management*. https://doi.org/10.1111/1467-8551.70007
- Chatzipanagiotou, Veloutsou, & Christodoulides (2016). *Decoding the complexity of the consumer-based brand equity process*. *Journal of Business Research*, *69*(11), 5479-5486. https://doi.org/10.1016/j.jbusres.2016.04.159
- Chaudhuri, A (2002). *How brand reputation
affects the advertising-brand equity link*. *Journal of
Advertising Research*, *42*(3), 33-43. https://doi.org/10.2501/jar-42-3-33-43
- Chell, K., Mortimer, G., Masser, B., & Russell–Bennett, R. (2021). *An Identity-Based Model Explaining Online Donor Appreciation*. *Australasian Marketing Journal*. https://doi.org/10.1177/18393349211027670
- Chen, Y., Dai, R., Yao, J., & Li, Y. (2019). *Donate Time or Money? The Determinants of Donation Intention in Online Crowdfunding*. *Sustainability*. https://doi.org/10.3390/su11164269
- Chetioui, et al. (2022). *Antecedents of giving charitable donations (Sadaqah) during the COVID-19 pandemic: does Islamic religiosity matter?*. *Journal of Islamic Marketing*. https://doi.org/10.1108/jima-09-2021-0296
- Christodoulides, Cadogan, & Veloutsou (2015). *Consumer-based brand equity measurement: lessons learned from an international study*. *International Marketing Review*, *32*(3/4), 307�328. https://doi.org/10.1108/imr-10-2013-0242
- Churchill, Gilbert A., Jr. (1979). *A Paradigm for Developing Better Measures of Marketing Constructs*. *Journal of Marketing Research*, *16*(1), 64. https://doi.org/10.2307/3150876
- Cobb-Walgren, Ruble, & Donthu (1995). *Brand Equity, Brand Preference, and Purchase Intent*. *Journal of Advertising*, *24*(3), 25--40. https://doi.org/10.1080/00913367.1995.10673481
- Cohen, D., Campbell, M., & Quinlan, P (2023). *Psychological value theory: A computational cognitive model of charitable giving. *Cognitive Psychology, 145*. <https://doi.org/10.1016/j.cogpsych.2023.101593>*. *Cognitive Psychology*, *145*, 101593. https://doi.org/10.1016/j.cogpsych.2023.101593
- Cohen, J. (1994). *The earth is round (p < .05)*. *American Psychologist*, *49*(12), 997-1003. https://doi.org/10.1037/0003-066x.49.12.997
- Connelly et al. (2011). *Signaling Theory: A Review and Assessment*. *Journal of Management*, *37*(1), 39--67. https://doi.org/10.1177/0149206310388419
- Cordelli, Chiara (2016). *Untitled*.
- Cordelli, Chiara (2020). *Untitled*.
- Cornwell, et al. (2022). *Shared Brand Equity*. *Journal of Advertising*, *52*(3), 311--329. https://doi.org/10.1080/00913367.2022.2131656
- Crawford & Jackson (2025). *Reflections on brand image: the influence of donor ideal and perceived charity brand congruence on charitable giving*. *Frontiers in Communication*. https://doi.org/10.3389/fcomm.2025.1682863
- Croson, R., Handy, F., & Shang, J. (2009). *Keeping up with the Joneses: The relationship of perceived descriptive social norms, social information, and charitable giving*. *Nonprofit Management and Leadership*. https://doi.org/10.1002/nml.232
- Crumpler & Grossman (2008). *An experimental test of warm glow giving*. *Journal of Public Economics*, *92*, 1011--1021. https://doi.org/10.1016/j.jpubeco.2007.12.014
- D'souza, et al. (2021). *The Effects of Religious Participation and Brand Image on Commitment to Donate to Faith-Based Charities*. *Journal of Nonprofit \& Public Sector Marketing*, *35*, 81--109. https://doi.org/10.1080/10495142.2021.1953670
- Da Silva, L. C., Mainardes, E., Teixeira, A., & Costa, L. (2020). *Brand orientation of nonprofit organizations and its relationship with the attitude toward charity and donation intention*. *International Review on Public and Nonprofit Marketing*. https://doi.org/10.1007/s12208-020-00251-6
- Dalman, M., & Ray, S (2021). *To donate or not to donate? How cosmopolitanism and brand anthropomorphism influence donation intentions for international humanitarian causes. *Management Research Review*. <https://doi.org/10.1108/mrr-04-2020-0240>*. *Management Research Review*, *45*(4), 524-544. https://doi.org/10.1108/mrr-04-2020-0240
- Darwall, Stephen (2024). *Untitled*.
- Das, S., Stenger, C., & Ellis, C (2009). *Managing tomorrow's brands: Moving from measurement towards an integrated system of brand equity. *Journal of Brand Management, 17*, 26-38. <https://doi.org/10.1057/bm.2009.13>*. *Journal of Brand Management*, *17*(1), 26-38. https://doi.org/10.1057/bm.2009.13
- Davcik, et al. (2015). *How much do Product Differentiation, Marketing Investments and Brand Equity Actually Affect Price? An Empirical Study in the Consumer Market*. *Developments in Marketing Science: Proceedings of the Academy of Marketing Science*, 619-619. https://doi.org/10.1007/978-3-319-24184-5_153
- Davcik, N. S., Silva, R., & Hair, J. F (2015). *Towards a unified theory of brand equity: conceptualizations, taxonomy and avenues for future research. *Journal of Product & Brand Management, 24*, 3-17. <https://doi.org/10.1108/jpbm-06-2014-0639>*. *Journal of Product &amp; Brand Management*, *24*(1), 3-17. https://doi.org/10.1108/jpbm-06-2014-0639
- de Chernatony, L. (1999). *Brand management through narrowing the gap between brand identity and brand reputation
through narrowing the gap between brand identity
and brand reputation'*. *Journal of Marketing Management*, *15*(1-3), 157-179. https://doi.org/10.1362/026725799784870432
- de Chernatony, L., & Riley, F. D. O. (1998). *Modelling the components of the brand*. *European Journal of Marketing
Journal of Marketing'*, *32*(11/12), 1074-1090. https://doi.org/10.1108/03090569810243721
- De Oliveira, M. O. R., Heldt, R., Silveira, C. S., & Luce, F. B. (2023). *Brand equity chain and brand equity measurement approaches*. *Marketing Intelligence & Planning*. https://doi.org/10.1108/mip-06-2022-0222
- De, T., & Verma, A. (2021). *Integrating Brand Communication and Brand Equity: A Systematic Review from 2000–2020*. *Journal of Content, Community & Communication*, *13*, 27-40.
- Dean (2016). *Untitled*. *Sociology*.
- Delgado-Ballester, Elena; Munuera-Alemán, José Luis (2005). *Does brand trust matter to brand equity?*. *Journal of Product \& Brand Management*, *14*(3), 187--196. https://doi.org/10.1108/10610420510601058
- DellaVigna, et al. (2012). *Testing for Altruism and Social Pressure in Charitable Giving*. *The Quarterly Journal of Economics*, *127*(1), 1-56. https://doi.org/10.1093/qje/qjr050
- Diamantopoulos, A. & Winklhofer, H.M (2001). *“Index construction with formative indicators: an alternative to scale development”, Journal of Marketing Research, Vol. 38 No. 2, pp. 269-277*. *Diamond, W.D. and Gooding-Williams, S. (2002), “Using advertising constructs and methods to understand direct mail fundraising appeals”, Nonproﬁt Management and Leadership, Vol*, *38*(2), 269-277. https://doi.org/10.1509/jmkr.38.2.269.18845
- Dika, S. L., & Singh, K. (2002). *Applications of Social Capital in Educational Literature: A Critical Synthesis*. *Review of Educational Research*. https://doi.org/10.3102/00346543072001031
- Dobni & Zinkhan (1990). *In search of brand image: a foundation analysis*. *Advances in Consumer Research*, *17*, 110--119.
- Duncan, T. & Moriarty, S.E (1998). *A
communication-based marketing model for managing
relationships*. *Journal of Marketing*, *62*(2), 1-13. https://doi.org/10.1177/002224299806200201
- Edell, J., & Burke, M. ( (1987). *The power of feelings in understanding advertising effects*. *Journal of Consumer Research*. https://doi.org/10.1007/s11002-014-9283-4
- Edelmann, A., Wolff, T., Montagne, D., & Bail, C. (2020). *Computational Social Science and Sociology*. *Annual review of sociology*.
- Edwards, W., Lindman, H., & Savage, L. J. (1963). *Bayesian statistical inference for psychological research*. *Psychological Review*, *70*(3), 193-242. https://doi.org/10.1037/h0044139
- Ehrlinger, L., & Wöß, W. (2016). *Towards a definition of knowledge graphs*. CEUR-WS.
- Eisenhardt, K. M. (1989). *Building theories from case study research*. *Academy of Management Review*, *14*(4), 532-550. https://doi.org/10.5465/amr.1989.4308385
- Erdem & Swait (1998). *Brand Equity as a Signaling Phenomenon*. *Journal of Consumer Psychology*, *7*(2), 131--157. https://doi.org/10.1207/s15327663jcp0702\textunderscore 02
- Erdem & Swait (2004). *Brand credibility, brand consideration, and choice*. *Journal of Consumer Research*, *31*(1), 191-198. https://doi.org/10.1086/383434
- Etheredge, H. (2021). *Assessing Global Organ Donation Policies*. *Risk Management and Healthcare Policy, 14*.
- Ewing & Napoli (2005). *Developing and validating a multidimensional nonprofit brand orientation scale*. *Journal of Business Research*, *58*(6), 841-853. https://doi.org/10.1016/j.jbusres.2003.09.012
- Exploring awareness–confidence relationship
Kramer RM (2000). *A Third Sector in the Third Millennium?
VOLUNTAS: International Journal of Voluntary and
Nonprofit Organizations 11: 1–23.*. *Nonprofit and Voluntary Sector Quarterly*, *43*(4), 672-692. https://doi.org/10.1177/0899764013479830
- Eyigunlu, M. (2023). *Towards a Sociology of Moral Giving*. *Sociology Lens*.
- Faircloth (2005). *The Effect of Brand Attitude and Brand Image on Brand Equity*. *Journal of Marketing Theory and Practice*, *9*(3), 1�15. https://doi.org/10.1080/10696679.2001.11501897
- Fang, D., Fombelle, P. W., & Bolton, R. N. (2020). *Member Retention and Donations in Nonprofit Service Organizations: The Balance Between Peer and Organizational Identification*. *Journal of Service Research*. https://doi.org/10.1177/1094670520933676
- Faseur, T., De Bock, T., & Timmermans, G. (2025). *Fundraising Ethics*. *Nonprofit and Voluntary Sector Quarterly, 54*.
- Fehresti, S., Takian, A., Jaafaripooyan, E., Parsaeian, M., & Jalilian, H. (2021). *Predicting donors’ behavior in contributing to health compared to non-health sectors: an application of revised theory of planned behavior in Iran*. *International Journal of Ethics and Systems*. https://doi.org/10.1108/ijoes-02-2021-0034
- Feldwick (1996). *What is Brand Equity Anyway, and how do you Measure it?*. *Market Research Society. Journal.*, *38*(2), 1-17. https://doi.org/10.1177/147078539603800201
- Felício, J. A., Martins Gonçalves, H., & da Conceição Gonçalves, V. ( (2013). *Social value and
   organizational performance in non-profit social organizations: Social entrepreneurship,
   leadership, and socioeconomic context effects*. *Journal of Business Research*. https://doi.org/10.1016/j.jbusres.2013.02.040
- Fennis, Bob M. & Janssen, Loes & Vohs, Kathleen D. (2009). *Acts of Benevolence: A Limited-Resource Account of Compliance with Charitable Requests*. *Journal of Consumer Research*, *35*(6), 906-924. https://doi.org/10.1086/593291
- Ferguson, E., & Flynn, N (2016). *Moral relativism as a disconnect between behavioural and experienced warm glow. *Journal of Economic Psychology, 56*, 163-175. <https://doi.org/10.1016/j.joep.2016.06.002>*. *Journal of Economic Psychology*, *56*, 163-175. https://doi.org/10.1016/j.joep.2016.06.002
- Ferguson, E., Lawrence, C., Bowen, S., Gemelli, C., Rozsa, A., Niekrasz, K., Van Dongen, A., Williams, L., Thijsen, A., Guerin, N., Masser, B., & Davison, T (2023). *Warming up cool cooperators. *Nature Human Behaviour, 7*, 1917 - 1932. <https://doi.org/10.1038/s41562-023-01687-6>*. *Nature Human Behaviour*, *7*(11), 1917-1932. https://doi.org/10.1038/s41562-023-01687-6
- Ferrara, I., & Missios, P. (2020). *Trust, ability-to-pay, and charitable giving*. *Journal of Public Economic Theory*.
- Fishbein & Yzer (2003). *Using Theory to Design Effective Health Behavior Interventions*. *Communication Theory*, *13*(2), 164--183. https://doi.org/10.1111/j.1468-2885.2003.tb00287.x
- Fisher, Robert J. & Vandenbosch, Mark & Antia, Kersi D. (2008). *An Empathy-Helping Perspective on Consumers' Responses to Fund-Raising Appeals*. *Journal of Consumer Research*, *35*(3), 519-531. https://doi.org/10.1086/586909
- Fournier (1998). *Consumers and Their Brands: Developing Relationship Theory in Consumer Research*. *Journal of Consumer Research*, *24*(4), 343--353. https://doi.org/10.1086/209515
- France, et al. (2025). *Digital brand equity: The concept, antecedents, measurement, and future development*. *Journal of Business Research*. https://doi.org/10.1016/j.jbusres.2025.115273
- Fraser (2018). *Faith, Hope, and Christian Charity: How Religion Explains Giving When Warm Glow and Impure Altruism Do Not*. *Social \& Political Philosophy eJournal*. https://doi.org/10.2139/ssrn.3164327
- Fraser (2022). *Faith? Hope? Charity? Religion explains giving when warm glow and impure altruism do not*. *The Manchester School*. https://doi.org/10.1111/manc.12415
- French & Smith (2013). *Measuring brand association strength: a consumer based brand equity approach*. *European Journal of Marketing*, *47*, 1356-1367. https://doi.org/10.1108/03090561311324363
- Friedman, Milton (1970). *Untitled*.
- Gabriel, I. (2017). *Effective Altruism and its Critics*. *Journal of Applied Philosophy, 34*.
- Gabrielli, Veronica & Baghi, Ilaria & Bergianti, Francesca (2021). *Brand scandals within a corporate social responsibility partnership: asymmetrical effects on for-profit and non-profit brands*. *Journal of Marketing Management*, *37*(15-16), 1573-1604. https://doi.org/10.1080/0267257x.2021.1928267
- Gandullia, L (2019). *The price elasticity of warm-glow giving. *Economics Letters*. <https://doi.org/10.1016/j.econlet.2019.05.046>*. *Economics Letters*, *182*, 30-32. https://doi.org/10.1016/j.econlet.2019.05.046
- García-Madariaga, et al. (2023). *How Brand Familiarity Influences Advertising Effectiveness of Non-Profit Organizations*. *International Review on Public and Nonprofit Marketing*, *21*(2), 279--293. https://doi.org/10.1007/s12208-023-00380-8
- Gardberg, N. A., Zyglidopoulos, S. C., Symeou, P., & Schepers, D. H. (2019). *The Impact of Corporate Philanthropy on Reputation for Corporate Social Performance*. *Business & Society*. https://doi.org/10.1177/0007650317694856
- Gardner, B. (2014). *A review and analysis of the use of ‘habit’ in understanding, predicting and influencing health-related behaviour*. *Health Psychology Review*. https://doi.org/10.1080/17437199.2013.876238
- Garg, Swami, & Malhotra (2019). *Branding effectiveness measurement in non-profit environment.*. *Journal of Advances in Management Research*, *16*(1), 4-22. https://doi.org/10.1108/JAMR-05-2018-0039
- Gershon, Rachel & Cryder, Cynthia (2017). *Goods Donations Increase Charitable Credit for Low-Warmth Donors*. *Journal of Consumer Research*, *45*(2), 451-469. https://doi.org/10.1093/jcr/ucx126
- Ghoorah, U., Mariyani-Squire, E., & Amin, S. Z. (2025). *Relationships between financial transparency, trust, and performance: an examination of donors’ perceptions*. *Humanities and Social Sciences Communications*. https://doi.org/10.1057/s41599-025-04640-2
- Ghoorah, U., Talukder, M. H., & Khan, A. (2021). *Donors’ perceptions of financial disclosures and links to donation intentions*. *Accounting Forum*. https://doi.org/https://doi.org/10.1080/01559982.2021.1872892
- Giebelhausen, M., Lawrence, B., Chun, H., & Hsu, L (2017). *The Warm Glow of Restaurant Checkout Charity. *Cornell Hospitality Quarterly, 58*, 329 - 341. <https://doi.org/10.1177/1938965517704533>*. *Cornell Hospitality Quarterly*, *58*(4), 329-341. https://doi.org/10.1177/1938965517704533
- Gigerenzer & Goldstein (2002). *Untitled*. *Psychological Review*. https://doi.org/10.1037/0033-295x.109.1.75
- Gillespie & Hillyer (2002). *Untitled*. *Transfusion*.
- Gioia, D. A., Corley, K. G., & Hamilton, A. L. (2013). *Seeking qualitative rigor in inductive research: Notes on the Gioia methodology*. *Organizational Research Methods*, *16*(1), 15-31. https://doi.org/10.1177/1094428112452151
- Gleasure, R., & Feller, J. (2016). *Does Heart or Head Rule Donor Behaviors in Charitable Crowdfunding Markets?*. *International Journal of Electronic Commerce*. https://doi.org/10.1080/10864415.2016.1171975
- Goodman, S. N. (1999). *Toward evidence-based medical statistics 1: The P value fallacy*. *Annals of Internal Medicine*, *130*(12), 995-1004. https://doi.org/10.7326/0003-4819-130-12-199906150-00008
- Goyal, A., & Verma, P (2021). *Impact of Brand Engagement on Behavioral Loyalty, Brand Equity and WOM Through Attitudinal Loyalty. *Journal of International Food & Agribusiness Marketing, 35*, 88 - 109. <https://doi.org/10.1080/08974438.2021.1956667>*. *Journal of International Food &amp; Agribusiness Marketing*, *35*(1), 88-109. https://doi.org/10.1080/08974438.2021.1956667
- Graça, S. S. (2022). *Increasing donor’s perceived value from charitable involvement: a multi-segment approach to the American donor market*. *International Review on Public and Nonprofit Marketing*. https://doi.org/10.1007/s12208-022-00355-1
- Green, Corliss L. & Webb, Deborah J. (1997). *Factors Influencing Monetary Donations to Charitable Organizations*. *Journal of Nonprofit &amp; Public Sector Marketing*, *5*(3), 19-40. https://doi.org/10.1300/j054v05n03_03
- Gregory, et al. (2019). *Branding for non-profits: explaining new donor decision-making in the charity sector*. *Journal of Product &amp; Brand Management*, *29*(5), 583�600. https://doi.org/10.1108/jpbm-09-2018-2011
- Gronroos, C (1994). *From marketing mix to
relationship marketing: Towards a paradigm shift
in marketing*. *Asia-Australia Marketing Journal*, *2*(1), 9-29. https://doi.org/10.1016/s1320-1646(94)70275-6
- Grossman, P., & Levy, J. (2024). *It's not you (well, it is a bit you), it's me: Self- versus social image in warm-glow giving*. *PLOS ONE*, *19*(3), e0300868. https://doi.org/10.1371/journal.pone.0300868
- Groza, M. P., & Groza, M. D. (2021). *Enhancing Volunteer Pride and Retention Rates: The Role of Organizational Reputation, Task Significance, and Skill Variety*. *Journal of Nonprofit & Public Sector Marketing*. https://doi.org/10.1080/10495142.2021.1926043
- Grube, J. A., & Piliavin, J. A. (2000). *Role Identity, Organizational Experiences, and Volunteer Performance*. *Personality and Social Psychology Bulletin*. https://doi.org/10.1177/01461672002611007
- Gruber, T. R. (1993). *A translation approach to portable ontology specifications*. *Knowledge Acquisition*, *5*(2), 199-220. https://doi.org/10.1006/knac.1993.1008
- Gråd, E., Erlandsson, A., & Tinghög, G (2021). *Do nudges crowd out prosocial behavior?. *Behavioural Public Policy*. <https://doi.org/10.1017/bpp.2021.10>*. *Behavioural Public Policy*, *8*(1), 107-120. https://doi.org/10.1017/bpp.2021.10
- Gugenishvili (2022). *I Was Thinking to Help but Then I Changed My Mind! The Influence of Injunctive and Descriptive Norms on the Donation Intention-behavior Link*. *Journal of Nonprofit \& Public Sector Marketing*, *35*, 308--327. https://doi.org/10.1080/10495142.2022.2066599
- Gugenishvili, I., & Colliander, J. (2022). *I will only help if others tell me to do so! The simultaneous influence of injunctive and descriptive norms on donations*. *Voluntary Sector Review*. https://doi.org/10.1332/204080521x16442337687557
- Guhl, D (2024). *Tracking time-varying brand equity using household panel data. *Journal of Business Research*. <https://doi.org/10.1016/j.jbusres.2024.114799>*. *Journal of Business Research*, *182*, 114799. https://doi.org/10.1016/j.jbusres.2024.114799
- Gui, P., Yang, Z., & Che, J (2022). *Research on the path choice behavior of donated materials under major epidemics. *Kybernetes, 52*, 3338-3361. <https://doi.org/10.1108/k-02-2021-0133>*. *Kybernetes*, *52*(9), 3338-3361. https://doi.org/10.1108/k-02-2021-0133
- Gutiérrez, et al. (2023). *Models of Brand Equity: A Systematic and Critical Review*. *Cogent Business \& Management*, *11*(1). https://doi.org/10.1080/23311975.2024.2433168
- Ha, M (2021). *Optimizing Green Brand Equity: The Integrated Branding and Behavioral Perspectives. *SAGE Open, 11*. <https://doi.org/10.1177/21582440211036087>*. *Sage Open*, *11*(3). https://doi.org/10.1177/21582440211036087
- Ha, Q.-A., Pham, P., & Le, L. (2022). *What facilitate people to do charity? The impact of brand anthropomorphism, brand familiarity and brand trust on charity support intention*. *International Review on Public and Nonprofit Marketing*. https://doi.org/10.1007/s12208-021-00331-1
- Han, et al. (2021). *The interaction between individual cultural values and the cognitive and social processes of global restaurant brand equity*. *International Journal of Hospitality Management*, *94*. https://doi.org/10.1016/j.ijhm.2020.102847
- Hanaysha, J., Abdullah, H. H., & Ghani, N. H. A (2013). *Assessing the literature on brand equity: From past, present to future.*.
- Hankinson, Philippa (2001). *Brand orientation in the charity sector: A framework for discussion and research*. *International Journal of Nonprofit & Voluntary Sector Marketing*, *6*(3), 231–242. https://doi.org/10.1002/nvsm.149
- Harbaugh (1998). *What do donations buy?: A model of philanthropy based on prestige and warm glow*. *Journal of Public Economics*, *67*, 269--284. https://doi.org/10.1016/s0047-2727(97)00062-5
- Harbaugh, W., Mayr, U., & Burghart, D (2007). *Neural Responses to Taxation and Voluntary Giving Reveal Motives for Charitable Donations. *Science, 316*, 1622 - 1625. <https://doi.org/10.1126/science.1140738>*. *Science*, *316*(5831), 1622-1625. https://doi.org/10.1126/science.1140738
- Harrington, M., Sweeney, M. R., Bailie, K., Morris, K., Kennedy, A., Boilson, A., O’Riordan, J., & Staines, A (2007). *What would encourage blood donation in Ireland? Vox Sanguinis, 92(4), 361–367*. *Harrison, T., & Thornton, J. (2022)*. https://doi.org/10.1177/08997640241227166
- Harris & de Chernatony (2001). *Corporate Branding and Corporate Brand Performance*. *European Journal of Marketing*, *35*(3/4), 441–. https://doi.org/10.1108/03090560110382101
- Hartmann, P., Eisend, M., Apaolaza, V., & D'souza, C (2017). *Warm glow vs. altruistic values: How important is intrinsic emotional reward in proenvironmental behavior?. *Journal of Environmental Psychology, 52*, 43-55. <https://doi.org/10.1016/j.jenvp.2017.05.006>*. *Journal of Environmental Psychology*, *52*, 43-55. https://doi.org/10.1016/j.jenvp.2017.05.006
- Harvey, C., Gordon, J., & Maclean, M. (2020). *The Ethics of Entrepreneurial Philanthropy*. *Journal of Business Ethics*.
- Healy (2000). *Untitled*. *American Journal of Sociology*.
- Heath, Joseph (2014). *Untitled*.
- Heitzmann & Simsa (2004). *From Corporatist Security to Civil Society Creativity: The Nonprofit Sector in Austria*. *Future of Civil Society*, 713-731. https://doi.org/10.1007/978-3-322-80980-3_34
- Hersberger-Langloh, Sophie (2020). *A Stakeholder Perspective on the Market Orientation of Swiss Nonprofit Organizations*. *Journal of Nonprofit &amp; Public Sector Marketing*, *34*(4), 395-420. https://doi.org/10.1080/10495142.2020.1865239
- Higgins, J. P. T., Thomas, J., Chandler, J., Cumpston, M., Li, T., Page, M. J., & Welch, V. A. (Hrsg.) (2019). *Cochrane Handbook for Systematic Reviews of Interventions*. *Wiley-Blackwell / Cochrane*. https://doi.org/10.1002/9781119536604
- Hill, Jr., Thomas E. (2018). *Untitled*.
- Hill, T. E. (2021). *Duties and Choices in Philanthropic Giving*. *In Beyond Duty. Oxford University Press*.
- Hoeffler, S., & Keller, K. L. (2003). *The marketing advantages of strong brands 10 No. 6, pp. 421-445*. *Journal of Brand Management can evoke the brand”, Advances in Consumer Research, Vol*, *10*(6), 421-445. https://doi.org/10.1057/palgrave.bm.2540139
- Holdershaw, et al. (2011). *Predicting blood donation behaviour: further application of the theory of planned behaviour*. *Journal of Social Marketing*, *1*, 120--132. https://doi.org/10.1108/20426761111141878
- Holiday, S., Hayes, J. L., Britt, B. C., & Lyu, Y. (2020). *The cause effect: the impact of corporate social responsibility advertising on cause consumer engagement behavior after brand affiliation ceases*. *International Journal of Advertising*. https://doi.org/10.1080/02650487.2020.1769408
- Homburg, Wieseke, & Hoyer (2009). *Social Identity and the Service-Profit Chain,*. *Journal of Marketing*, *73*(2), 38–54. https://doi.org/10.1509/jmkg.73.2.38
- Hommerová, D., Alaimo, S., & Sojková, O. M. (2025). *Determining brand equity of nonprofit organizations: An inquiry of Czech citizens*. *Communications*. https://doi.org/10.1515/commun-2024-0153
- Hou et al. (2009). *The effects of nonprofit brand equity on individual giving intention: mediating by the self--concept of individual donor*. *International Journal of Nonprofit and Voluntary Sector Marketing*, *14*(3), 215--229. https://doi.org/10.1002/nvsm.356
- Hoyer & Brown (1990). *Effects of brand awareness on choice for a common, repeat-purchase product*. *Journal of Consumer Research*, *17*(2), 141–148. https://doi.org/10.1086/208544
- Hsu, L (2023). *An integrative model for online community citizenship behavior of luxury fashion brands on Instagram. *Journal of Fashion Marketing and Management: An International Journal*. <https://doi.org/10.1108/jfmm-12-2022-0263>*. *Journal of Fashion Marketing and Management: An International Journal*, *28*(2), 357-378. https://doi.org/10.1108/jfmm-12-2022-0263
- Huang, Q., Li, D., Zhou, C., Xu, Q., Li, P., & Warren, C (2021). *Multivariate pattern analysis of electroencephalography data reveals information predictive of charitable giving. *NeuroImage, 242*. <https://doi.org/10.1016/j.neuroimage.2021.118475>*. *NeuroImage*, *242*, 118475. https://doi.org/10.1016/j.neuroimage.2021.118475
- Huang, S.-L., & Ku, H.-H. (2016). *Brand image management for nonprofit organizations: Exploring the relationships between websites, brand images and donations*. *Journal of Electronic Commerce Research*.
- Hue, T., & Huyen, N (2025). *What drives green brand equity? Insights from the Delphi method and analytic hierarchy process. *Discover Sustainability, 6*. <https://doi.org/10.1007/s43621-025-01865-8>*. *Discover Sustainability*, *6*(1). https://doi.org/10.1007/s43621-025-01865-8
- Hume, M., & Mort, G. S. (2010). *The consequence of appraisal emotion, service quality, perceived value and customer satisfaction on repurchase intent in the performing arts*. *Journal of Services Marketing*. https://doi.org/10.1108/08876041011031136
- Hunt, S.D. & Morgan, R.M (1995). *The comparative advantage theory of competition*. *Journal
of Marketing*, *59*(2), 1-15. https://doi.org/10.1177/002224299505900201
- Hyde, et al. (2013). *Donating blood and organs: using an extended theory of planned behavior perspective to identify similarities and differences in individual motivations to donate*. *Health education research*, *28 6*, 1092--1104. https://doi.org/10.1093/her/cyt078
- Imas, A (2014). *Working for the “warm glow”: On the benefits and limits of prosocial incentives. *Journal of Public Economics, 114*, 14-18. <https://doi.org/10.2139/ssrn.2343445>*. *SSRN Electronic Journal*. https://doi.org/10.2139/ssrn.2343445
- Ishaq, M., & Di Maria, E (2020). *Sustainability countenance in brand equity: a critical review and future research directions. *Journal of Brand Management, 27*, 15-34. <https://doi.org/10.1057/s41262-019-00167-5>*. *Journal of Brand Management*, *27*(1), 15-34. https://doi.org/10.1057/s41262-019-00167-5
- Jaafar, S. B. (2025). *The practice of strategic philanthropy*. *Society and Business Review*.
- Jara & Cliquet (2015). *Retail brand equity: Conceptualization and measurement*. *Journal of Retailing and Consumer Services*, *19*, 140-149. https://doi.org/10.1016/j.jretconser.2011.11.003
- Jeffrey, R. C. (1965). *New Foundations for Bayesian Decision Theory*. North-Holland.
- Jiang, et al. (2017). *Validating a multidimensional perspective of brand equity on motivation, expectation, and behavioural intention: a practical examination of culinary tourism*. *Asia Pacific Journal of Tourism Research*, *22*, 524--539. https://doi.org/10.1080/10941665.2017.1287106
- Jibran, R., Rasul, M., Hussain, M., Shahid, R., & Yasin, M. (2025). *Impact of Perceived Service Quality on Repurchase Intention and Word of Mouth: Mediating Role of Customer Satisfaction*. *Qlantic Journal of Social Sciences*. https://doi.org/10.55737/qjss.vi-iii.25385
- Jones, J. L., & Shandiz, M. (2015). *Service Quality Expectations: Exploring the Importance of SERVQUAL Dimensions from Different Nonprofit Constituent Groups*. *Journal of Nonprofit & Public Sector Marketing*. https://doi.org/10.1080/10495142.2014.925762
- Jones, R. (2005). *Finding sources of brand value: Developing a stakeholder model of brand equity*. *Journal of Brand Management*. https://doi.org/10.1057/palgrave.bm.2540243
- Juntunen, M., Juntunen, J., & Autere, J. (2013). *Co-creation of brand equity in a nonprofit context*. *International Journal of Nonprofit and Voluntary Sector Marketing*, *18*(2), 122--132. https://doi.org/10.1002/nvsm.1453
- Karakayali (2017). *Untitled*. *Journal of Civil Society*.
- Kashif et al. (2018). *Finding greener grass on the other side of hill*. *Asia Pacific Journal of Marketing and Logistics*, *30*(4), 988--1012. https://doi.org/10.1108/APJML-10-2017-0231
- Katz (2017). *The Impact of Familiarity and Perceived Trustworthiness and Influence on Donations to Nonprofits: An Unaided Recall Study*. *Journal of Nonprofit &amp; Public Sector Marketing*, *30*(2), 187�199. https://doi.org/10.1080/10495142.2017.1326874
- Keller & Brexendorf (2019). *Measuring Brand Equity*. *Handbuch Markenführung*, 978-3. https://doi.org/10.1007/978-3-658-13342-9_72
- Keller & Lehmann (2003). *How Do Brands Create Value?*. *Marketing Management*, *12*(3), 26--31.
- Keller, K. L (2020). *Leveraging secondary associations to build brand equity: theoretical perspectives and practical applications. *International Journal of Advertising, 39*, 448 - 465. <https://doi.org/10.1080/02650487.2019.1710973>*. *International Journal of Advertising*, *39*(4), 448-465. https://doi.org/10.1080/02650487.2019.1710973
- Keller, K.L. (1993). *“Conceptualizing, measuring, and managing customer-based brand*. *Journal of Marketing*, *57*(1), 1-22. https://doi.org/10.1177/002224299305700101
- Keller, K. L. ( (2016). *Reflections on customer-based brand equity:
perspectives, progress, and priorities. *AMS Review*, *6*(1-2), 1–16.
https://doi.org/10.1007/s13162-016-0078-z*. *AMS Review*, *6*(1-2), 1-16. https://doi.org/10.1007/s13162-016-0078-z
- Kerres, C., & Proell, F (2008). *The Austrian Donations Tax Act 2008 for Foundations and Comparable Entities. *Trusts & Trustees, 14*, 599-604. <https://doi.org/10.1093/tandt/ttn103>*. *Trusts &amp; Trustees*, *14*(8), 599-604. https://doi.org/10.1093/tandt/ttn103
- Kessler, J. B., & Milkman, K. L. (2016). *Identity in Charitable Giving*. *Manag. Sci.*. https://doi.org/10.1287/mnsc.2016.2582
- Kim, H. H., & Han, E. (2020). *The Application of the Theory of Planned Behavior to Identify Determinants of Donation Intention: Towards the Comparative Examination of Positive and Negative Reputations of Nonprofit Organizations CEO*. *Sustainability*. https://doi.org/10.3390/su12219134
- Kim, M., Yoon, Y., & Zhang, J. J. (2023). *The Influence of Perceived Relationship Quality on Donor Behavior in the Context of Charitable Nonprofit Organizations Established by Professional Sport Entities*. *Journal of Relationship Marketing*. https://doi.org/10.1080/15332667.2023.2257099
- Kingston, P. (2001). *The Unfulfilled Promise of Cultural Capital Theory*. *Sociology Of Education*. https://doi.org/10.2307/2673255
- Knowles, et al. (2012). *Predictors of Young People's Charitable Intentions to Donate Money: An Extended Theory of Planned Behavior Perspective*. *Journal of Applied Social Psychology*, *42*(9), 2096--2110. https://doi.org/10.1111/j.1559-1816.2012.00932.x
- Kohli, A.K. & Jaworski, B.J (1990). *Market orientation: The construct, research propositions, and
managerial implications*. *Journal of Marketing*, *54*(2), 1-18. https://doi.org/10.1177/002224299005400201
- Konow, J (2010). *Mixed feelings: Theories of and evidence on giving. *Journal of Public Economics, 94*, 279-297. <https://doi.org/10.1016/j.jpubeco.2009.11.008>*. *Journal of Public Economics*, *94*(3-4), 279-297. https://doi.org/10.1016/j.jpubeco.2009.11.008
- Konow, J (2006). *Mixed Feelings: Theories and Evidence of Warm Glow and Altruism. *Microeconomic Theory eJournal*. <https://doi.org/10.2139/ssrn.980349>*. *SSRN Electronic Journal*. https://doi.org/10.2139/ssrn.980349
- Krishnan (1996). *Characteristics of memory associations: A consumer-based brand equity perspective*. *International Journal of Research in Marketing*, *13*(4), 389--405. https://doi.org/10.1016/S0167-8116(96)00021-3
- Kusuma, H., & Anafisati, V. ( (2020). *DONOR'S INTENTION ON THE CROWDFUNDINGAMONG UNIVERSITY
STUDENTS: AN EXTENSION OF THE THEORY OF PLANNED BEHAVIOUR*. *Humanities and social sciences*. https://doi.org/10.18510/hssr.2020.8470
- Kusuma, I. E. T., Yasmari, N. N. W., Agung, A., & Landra, N. (2021). *When Satisfaction Is Not Enough to Build a Word of Mouth and Repurchase Intention*. *Asia Pacific Management and Business Application*. https://doi.org/10.21776/ub.apmba.2021.010.01.1
- Kusumasondjaja, S., & Krisnawati, W (2024). *Pengaruh Social Distance dan Brand Familiarity terhadap Perceived Credibility, Trust dan Niat Berdonasi dimoderasi oleh Intrinsic Religiosity. *Prosiding Seminar Nasional Forum Manajemen Indonesia - e-ISSN 3026-4499*. <https://doi.org/10.47747/snfmi.v2i1.2342>*. *Prosiding Seminar Nasional Forum Manajemen Indonesia - e-ISSN 3026-4499*, *2*, 624-641. https://doi.org/10.47747/snfmi.v2i1.2342
- Kutlu & Özcan (2024). *The Effect of Brand Heritage on Intention to Donate in Non-Profit Organizations: An Evaluation within the Context of Temporal Focus and Brand Trust*. *Journal of Nonprofit \& Public Sector Marketing*, *37*, 221--244. https://doi.org/10.1080/10495142.2024.2353384
- Labban, A., Novell, C., & Bauer, S (2022). *Examining the impact of mindsets on donation intentions to homelessness charities via parallel serial mediation. *International Review on Public and Nonprofit Marketing, 20*, 225 - 244. <https://doi.org/10.1007/s12208-022-00336-4>*. *International Review on Public and Nonprofit Marketing*, *20*(1), 225-244. https://doi.org/10.1007/s12208-022-00336-4
- Lai, C.-S., & Nguyen, D. T. (2024). *The Impact of Perceived Relationship Investment and Organizational Identification on Behavioral Outcomes in Nonprofit Organizations: The Moderating Role of Relationship Proneness*. *Nonprofit Management and Leadership*. https://doi.org/10.1002/nml.21632
- Laidler-Kylander, Quelch, & Simonin (2007). *The brand IDEA: Managing nonprofit brands with integrity, democracy, and affinity*. *Nonprofit Management and Leadership*, *17*(3), 253--277. https://doi.org/10.1002/nml.149
- Lakew, G., Gebretsadkan, B. T., Alemu, G. G., Bazezew, A. M., Yirsaw, A. N., Wondie, W., Mengistie, B. A., Dagnaw, T. E., Aweke, M. N., & Baykemagn, N. D. (2026). *Blood donation practices and behavioral intentions: A scoping review using the theory of planned behavior*. *PLOS One*. https://doi.org/10.1371/journal.pone.0333426
- Laurent et al. (1995). *The underlying structure of brand awareness scores*. *Marketing Science*, *14*(3_supplement), G170-G179. https://doi.org/10.1287/mksc.14.3.g170
- Lechterman, T. M. (2022). *Untitled*.
- Lechterman, T. M., Saunders-Hastings, E., & Reich, R. (2024). *Philanthropy*. *The Stanford Encyclopedia of Philosophy*.
- Lee, J. Y., & Kim, S. S. (2023). *The effect of multidimensions of trust and donors' motivation on donation attitudes and intention toward charitable organizations*. *Nonprofit Management and Leadership*. https://doi.org/10.1002/nml.21567
- Lee, Z., Spry, A., Ekinci, Y., & Vredenburg, J. (2023). *From warmth to warrior: impacts of non-profit brand activism on brand bravery, brand hypocrisy and brand equity*. *Journal of Brand Management*. https://doi.org/10.1057/s41262-023-00319-8
- Leliveld, M. C., & Risselada, H. (2017). *Dynamics in charity donation decisions: Insights from a large longitudinal data set*. *Science Advances*. https://doi.org/10.1126/sciadv.1700077
- Li, et al. (2022). *Understanding the intention to donate online in the Chinese context: The influence of norms and trust*. *Cyberpsychology: Journal of Psychosocial Research on Cyberspace*. https://doi.org/10.5817/cp2022-1-7
- Li, H., Kinoshita, T., Chen, J., Xie, J., Luo, S., & Su, D (2024). *What promotes residents’ donation behavior for adaptive reuse of cultural heritage projects? An application of the extended theory of planned behavior. *Sustainable Cities and Society*. <https://doi.org/10.1016/j.scs.2024.105213>*. *Sustainable Cities and Society*, *102*, 105213. https://doi.org/10.1016/j.scs.2024.105213
- Li, W., Yang, D.-H., & Sun, Y. (2022). *Influence mechanism of charitable crowdfunding context on individual donation intention: BASED on the SOR framework*. *Journal of Decision Systems*. https://doi.org/https://doi.org/10.1080/12460125.2022.2140908
- Liao-Troth (2001). *Attitude differences between paid workers and volunteers.*. *Nonprofit Management and Leadership*, *11*(4), 423-442. https://doi.org/10.1002/nml.11403
- Lichtenstein, D., Drumwright, M., & Braig, B (2004). *The Effect of Corporate Social Responsibility on Customer Donations to Corporate-Supported Nonprofits. *Journal of Marketing, 68*, 16 - 32. <https://doi.org/10.1509/jmkg.68.4.16.42726>*. *Journal of Marketing*, *68*(4), 16-32. https://doi.org/10.1509/jmkg.68.4.16.42726
- Lilley, A., & Slonim, R (2014). *The Price of Warm Glow. *Behavioral & Experimental Finance eJournal*. <https://doi.org/10.1016/j.jpubeco.2013.12.004>*. *Journal of Public Economics*, *114*, 58-74. https://doi.org/10.1016/j.jpubeco.2013.12.004
- Lin, C., & Hai, Y. (2023). *Research on the Influence of Cultural Capital on Human Sports Practice*. *SHS Web of Conferences*.
- List, J., Murphy, J., Price, M. K., & James, A. G. (2021). *An experimental test of fundraising appeals targeting donor and recipient benefits*. *Nature Human Behaviour*. https://doi.org/10.1038/s41562-021-01095-8
- Litofcenko, et al. (2023). *Charitable Giving in Times of Covid-19: Do Crises Forward the Better or the Worse in Individuals?*. *Voluntas: International Journal of Voluntary and Nonprofit Organizations*, *34*(6), 1322-1334. https://doi.org/10.1007/s11266-023-00558-y
- Liu, et al. (2017). *Applying Consumer-Based Brand Equity in Luxury Hotel Branding*. *Journal of Business Research*, *81*, 192--202. https://doi.org/10.1016/j.jbusres.2017.06.014
- Liu, G.; Chapleo, C.; Ko, W. W.; Ngugi, I. K. (2015). *The Role of Internal Branding in Nonprofit Brand Management*. *Nonprofit and Voluntary Sector Quarterly*, *44*(2), 319--339. https://doi.org/10.1177/0899764013511303
- Liu, L., Suh, A., & Wagner, C (2018). *Empathy or perceived credibility? An empirical study on individual donation behavior in charitable crowdfunding. *Internet Res., 28*, 623-651. <https://doi.org/10.1108/intr-06-2017-0240>*. *Internet Research*, *28*(3), 623-651. https://doi.org/10.1108/intr-06-2017-0240
- Louvet (2023). *The effects of brand equity on millennials' purchase decision for sports nutrition products in Ireland*. *DBS Business Review*. https://doi.org/10.22375/dbr.v5i.87
- Luccasen, & Grossman (2017). *Warm‐Glow Giving: Earned Money and the Option to Take*. *ERN: Other Macroeconomics: Monetary & Fiscal Policies (Topic)*. https://doi.org/10.1111/ecin.12417
- Luffarelli, J., Delre, S., & Landgraf, P. (2022). *How has the effect of brand personality on customer-based brand equity changed over time? Longitudinal evidence from a panel data set spanning 18 years*. *Journal of the Academy of Marketing Science*. https://doi.org/10.1007/s11747-022-00895-2
- MacAskill, William (2019). *The Definition of Effective Altruism*. *Effective Altruism: Philosophical Issues*.
- Mael, F., & Ashforth, B. E. (1992). *Alumni and Their Alma - Mater: A Partial Test of the Reformulated Model of Organizational Identification,*. *Journal of Organizational Behavior*, *13*(2), 103–123. https://doi.org/10.1002/job.4030130202
- Maleki & Hosseini (2020). *Charity donation intention via m-payment apps: donor-related, m-payment system-related, or charity brand-related factors, which one is overkill?*. *International Review on Public and Nonprofit Marketing*, *17*, 409--443. https://doi.org/10.1007/s12208-020-00254-3
- Mandel, N., & Johnson, E. J. ( (2002). *When web pages influence choice: effects of visual primes on
   experts and novices*. *Journal of Consumer Research*. https://doi.org/10.1086/
- Manning (2009). *Untitled*.
- Marcos, A., & Coelho, A. (2021). *Service quality, customer satisfaction and customer value: holistic determinants of loyalty and word-of-mouth in services*. *The TQM Journal*. https://doi.org/10.1108/tqm-10-2020-0236
- Marin, Ruiz, & Rubio (2008). *‘‘The Role of Identity Salience in the Effects of Corporate Social Responsibility on Consumer Behavior’’*. *Journal of Business Ethics*, *84*(1), 65-78. https://doi.org/10.1007/s10551-008-9673-8
- Marta, E., Manzi, C., Pozzi, M., & Vignoles, V. (2014). *Identity and the Theory of Planned Behavior: Predicting Maintenance of Volunteering After Three Years*. *The Journal of Social Psychology*. https://doi.org/10.1080/00224545.2014.881769
- Martin, M. W. (1994). *Virtuous Giving: Philanthropy, Voluntary Service, and Caring*.
- Martín, H., Herrero, Á., & Del Mar García De Los Salmones, M (2019). *An integrative model of destination brand equity and tourist satisfaction. *Current Issues in Tourism, 22*, 1992 - 2013. <https://doi.org/10.1080/13683500.2018.1428286>*. *Current Issues in Tourism*, *22*(16), 1992-2013. https://doi.org/10.1080/13683500.2018.1428286
- Mato-Santiso, V., Maseda-Moreno, A., & Iturralde-Jaiker, T. (2021). *Volunteer Omnichannel Behavior in Nonprofit Organizations: Key Antecedents and Implications for Management*. *Nonprofit Management and Leadership*, *33*(3), 573--595. https://doi.org/10.1002/nml.21579
- Mauss, Marcel (1990). *The Gift: The Form and Reason for Exchange in Archaic Societies*. *Routledge*.
- Mayo, J., & Tinsley, C (2009). *Warm glow and charitable giving: Why the wealthy do not give more to charity?. *Journal of Economic Psychology, 30*, 490-499. <https://doi.org/10.1016/j.joep.2008.06.001>*. *Journal of Economic Psychology*, *30*(3), 490-499. https://doi.org/10.1016/j.joep.2008.06.001
- McGoey, L. (2021). *Philanthrocapitalism and the Separation of Powers*. *Annual Review of Law and Social Science*.
- Medhi & Kakati (2025). *A Revisit into the Concepts, Measurements and Valuation of Customer Based Brand Equity and Financial Based Brand Equity*. *International Journal For Multidisciplinary Research*. https://doi.org/10.36948/ijfmr.2025.v07i01.37352
- Men, L. R., & Tsai, W. H. S. ( (2014). *Perceptual, attitudinal, and behavioral outcomes of
   organization–public engagement on corporate social networking sites*. *Journal of Public
   Relations Research*. https://doi.org/10.1080/1062726x.2014.951047
- Metawie, M., & Mostafa, R (2015). *Predictors of Egyptian University Students’ Charitable Intentions: Application of Theory of Planned Behaviour. \*\*.*.
- Mette (2013). *Untitled*. *Springer VS*.
- Michaelidou, Micevski, & Cadogan (2015). *Consumers' Intention to Donate to two Children’s Charity Brands: A Comparison of Barnardo’s and BBC Children in Need*. *Journal of Product & Brand Management*, *24*, 134-146. https://doi.org/10.1108/jpbm-04-2014-0573
- Michel & Rieunier (2012). *Nonprofit brand image and typicality influences on charitable giving*. *Journal of Business Research*, *65*(5), 701707. https://doi.org/10.1016/j.jbusres.2011.04.002
- Michel & Rieunier (2015). *Nonprofit Brands: The Importance of Brand Image in Charitable Giving*. *Developments in marketing science: proceedings of the Academy of Marketing Science*, 22. https://doi.org/10.1007/978-3-319-10864-3_14
- Middleton, G., & Lee, H (2020). *Non-profit organization’s innovative donor management-the identification of salient factors that drive donor loyalty. *, 14*, 93-106. <https://doi.org/10.1108/apjie-01-2020-0010>*. *Asia Pacific Journal of Innovation and Entrepreneurship*, *14*(1), 93-106. https://doi.org/10.1108/apjie-01-2020-0010
- Mikul & Mittal (2023). *The Saga of Brand Equity: A Comprehensive Bibliometric Analysis*. *NMIMS Management Review*, *31*(3), 165--177. https://doi.org/10.1177/0974150X231205447
- Millán, Á., Retamosa, M., & Carranza, R. (2023). *What About NPOs? Identifying Factors in the Intention to Donate: The Role of Brand Identification and Past Behavior*. *VOLUNTAS: International Journal of Voluntary and Nonprofit Organizations*. https://doi.org/10.1007/s11266-023-00586-8
- Min, D. (2022). *Exploring the Structural Relationships between Service Quality, Perceived Value, Satisfaction, and Loyalty in Nonprofit Sport Clubs: Empirical Evidence from Germany*. *Sport Marketing Quarterly*. https://doi.org/10.32731/smq.313.0922.03
- Mittelman & Rojas‐Méndez (2018). *Why Canadians Give to Charity: An Extended Theory of Planned Behaviour Model*. *International Review on Public and Nonprofit Marketing*, *15*(2), 189--204. https://doi.org/10.1007/s12208-018-0197-3
- Morgan & Hunt (1994). *The Commitment-Trust Theory of Relationship Marketing*. *Journal of Marketing*, *58*(3), 20--38. https://doi.org/10.1177/002224299405800302
- Motameni & Shahrokhi (1998). *Brand equity valuation: a global perspective*. *Journal of Product &amp; Brand Management*, *7*(4), 275-290. https://doi.org/10.1108/10610429810229799
- Mouton, J., & Marais, H. C. (1990). *Basic Concepts in the Methodology of the Social Sciences*. Human Sciences Research Council.
- Mukherjee, S. (2013). *Concerns with attempts by neuroeconomics to answer the philosophical question "Is it rational to donate money for charity?"*. *Frontiers in Psychology, 4*.
- Musamuxamedov, et al. (2025). *The Role of Income, Happiness, and Norms in Fostering Pro-Social Behavior: A PLS-SEM Analysis of Charitable Giving and Its Contribution to Sustainable Development in Uzbekistan*. *Sustainability*. https://doi.org/10.3390/su17219440
- Naidoo, C., & Abratt, R. (2017). *Brands that do good: insight into social brand equity*. *Journal of Brand Management*. https://doi.org/10.1057/s41262-017-0072-2
- Netemeyer et al. (2004). *Untitled*. *Journal of Product & Brand Management*.
- Neumayr (2015). *Giving in Austria: A Corporatist Relationship between the Nonprofit Sector and the State*. *The Palgrave Handbook of Global Philanthropy*, 100--117. https://doi.org/10.1057/9781137341532_7
- Neumayr & Handy (2017). *Examining the Association of Welfare State Expenditure, Non-profit Regimes and Charitable Giving*. *Voluntas: International Journal of Voluntary and Nonprofit Organizations*, *28*(2), 532-555. https://doi.org/10.1007/s11266-016-9739-7
- Neumayr & Pennerstorfer (2020). *The Relation Between Income and Donations as a Proportion of Income Revisited: Literature Review and Empirical Application*. *Nonprofit and Voluntary Sector Quarterly*, *50*(3), 551-577. https://doi.org/10.1177/0899764020977667
- Neumayr & Schröder (2025). *How perceived income inequality affects charitable giving and volunteering: assessing four mechanisms*. *European Societies*. https://doi.org/10.1162/euso.a.22
- Neumayr, M., & Handy, F (2017). *Charitable Giving: What Influences Donors’ Choice Among Different Causes?. *VOLUNTAS: International Journal of Voluntary and Nonprofit Organizations, 30*, 783 - 799. <https://doi.org/10.1007/s11266-017-9843-3>*. *Voluntas: International Journal of Voluntary and Nonprofit Organizations*, *30*(4), 783-799. https://doi.org/10.1007/s11266-017-9843-3
- Ngo, et al. (2021). *Understanding the Role of Brand Salience in Brand Choice Decisions in the Charity Sector*. *Australasian Marketing Journal*, *30*, 258--270. https://doi.org/10.1177/1839334921999477
- Nguyen, et al. (2022). *Mind the gap: Understanding the gap between intentions and behaviour in the charity context*. *Journal of Business Research*, *148*, 216--224. https://doi.org/10.1016/j.jbusres.2022.04.044
- Nilsson, A., Erlandsson, A., & Västfjäll, D (2016). *The congruency between moral foundations and intentions to donate, self-reported donations, and actual donations to charity. *Journal of Research in Personality, 65*, 22-29. <https://doi.org/10.1016/j.jrp.2016.07.001>*. *Journal of Research in Personality*, *65*, 22-29. https://doi.org/10.1016/j.jrp.2016.07.001
- Nogueira, M., Santarém, F., & Gomes, S. (2020). *Volunteer Brand Equity? Exploring the Adoption of Employee Brand Equity (EBE) Dimensions to Understand Volunteers’ Contributions to Build Nonprofit Organizations’ Brands*. *Journal of Nonprofit & Public Sector Marketing*. https://doi.org/10.1080/10495142.2019.1689222
- Nozick, Robert (1974). *Untitled*.
- Null, C (2011). *Warm glow, information, and inefficient charitable giving. *Journal of Public Economics, 95*, 455-465. <https://doi.org/10.1016/j.jpubeco.2010.06.018>*. *Journal of Public Economics*, *95*(5-6), 455-465. https://doi.org/10.1016/j.jpubeco.2010.06.018
- Oktaviani, N., & Nisa, P. C. (2024). *The Effect of Service Quality, Perceived Value, and Customer Satisfaction on Loyalty and Word of Mouth (WOM)*. *International Journal of Economics, Management and Accounting (IJEMA)*. https://doi.org/10.47353/ijema.v1i9.107
- Onkovist & Shaw (1989). *Service Marketing: Image, Branding, and Competition.*. *Business Horizons*, *32*(1), 13-18. https://doi.org/10.1016/0007-6813(89)90018-9
- Ostrower (1995). *Untitled*.
- Ou, J., Wong, I., Prentice, C., & Liu, M. (2020). *Customer Engagement and its Outcomes: The Cross-Level Effect of Service Environment and Brand Equity*. *Journal of Hospitality & Tourism Research*. https://doi.org/10.1177/1096348019897360
- O’Neil, J. (2009). *Linking Public Relations Tactics to Long-Term Success: An Investigation of How Communications Contribute to Trust, Satisfaction, and Commitment in a Nonprofit Organization*. *Journal of Promotion Management*. https://doi.org/10.1080/10496490802623358
- Panda, T., Kumar, A., Jakhar, S., Luthra, S., Garza‐Reyes, J., Kazancoglu, I., & Nayak, S (2020). *Social and environmental sustainability model on consumers’ altruism, green purchase intention, green brand loyalty and evangelism. *Journal of Cleaner Production*. <https://doi.org/10.1016/j.jclepro.2019.118575>*. *Journal of Cleaner Production*, *243*, 118575. https://doi.org/10.1016/j.jclepro.2019.118575
- Parasuraman, A., Zeithaml, V. A., & Berry, L. L. (1988). *SERVQUAL: A Multiple-Item Scale for Measuring Consumer Perceptions of Service Quality*. *Journal of Retailing*, *64*(1), 12–40.
- Park, C. Whan; MacInnis, Deborah J.; Priester, Joseph; Eisingerich, Andreas B.; Iacobucci, Dawn (2010). *Brand Attachment and Brand Attitude Strength: Conceptual and Empirical Differentiation of Two Critical Brand Equity Drivers*. *Journal of Marketing*, *74*(6), 1–17. https://doi.org/10.1509/jmkg.74.6.1
- Park, C.-I., & Namkung, Y. (2022). *The Effects of Instagram Marketing Activities on Customer-Based Brand Equity in the Coffee Industry*. *Sustainability*. https://doi.org/10.3390/su14031657
- Park, J., Sung, J., Son, J., Na, K., & Kim, S (2019). *Athletes’ brand equity, spectator satisfaction, and behavioral intentions. *Asia Pacific Journal of Marketing and Logistics*. <https://doi.org/10.1108/apjml-05-2018-0176>*. *Asia Pacific Journal of Marketing and Logistics*, *31*(2), 541-558. https://doi.org/10.1108/apjml-05-2018-0176
- Parris & Guzmán (2022). *Evolving brand boundaries and expectations: looking back on brand equity, brand loyalty, and brand image research to move forward*. *Journal of Product & Brand Management*. https://doi.org/10.1108/jpbm-06-2021-3528
- Paschina (2025). *Brand Equity Measurement Models: A Systematic Review*. *International Journal of Business and Management*. https://doi.org/10.5539/ijbm.v20n5p1
- Paço, et al. (2014). *Branding in NGOs - its Influence on the Intention to Donate*. *ECONOMICS &amp; SOCIOLOGY*, *7*(3), 11-21. https://doi.org/10.14254/2071-789x.2014/7-3/1
- Pearlman, S. (2023). *Solidarity Over Charity*. *Kennedy Institute of Ethics Journal, 33*.
- Petersen, A (2025). *University digital media co-occurrence networks reveal structure and dynamics of brand visibility in the attention economy. *Humanities and Social Sciences Communications, 12*. <https://doi.org/10.1057/s41599-025-04419-5>*. *Humanities and Social Sciences Communications*, *12*(1). https://doi.org/10.1057/s41599-025-04419-5
- Petritz & Kampitsch (2016). *The Austrian Charitable Foundation reform of 2015*. *Trusts &amp; Trustees*, *22*(6), 626-630. https://doi.org/10.1093/tandt/ttw090
- Petritz, M., & Malaschofsky, M (2017). *The Austrian philanthropic Innovation Foundation for Education. *Trusts & Trustees, 23*, 632-636. <https://doi.org/10.1093/tandt/ttx081>*. *Trusts &amp; Trustees*, *23*(6), 632-636. https://doi.org/10.1093/tandt/ttx081
- Pettit, Philip (1997). *Untitled*.
- Pevnick, Ryan (2013). *Untitled*.
- Pevnick, Ryan (2016). *Untitled*.
- Phung, M., Ly, P., & Nguyen, T (2019). *The effect of authenticity perceptions and brand equity on brand choice intention. *Journal of Business Research*. <https://doi.org/10.1016/j.jbusres.2019.01.002>*. *Journal of Business Research*, *101*, 726-736. https://doi.org/10.1016/j.jbusres.2019.01.002
- Piper & Schnepf (2008). *Untitled*.
- Pournarakis, D (2017). *Brand equity assessment: a computational model for mining consumer perceptions in social media. \*\*.*. *Decision Support Systems*, *93*, 98-110. https://doi.org/10.1016/j.dss.2016.09.018
- Powell, K. L., Roberts, G., & Nettle, D. (2012). *Eye images increase charitable donations: Evidence from an opportunistic field experiment in a supermarket*. *Ethology*. https://doi.org/10.1111/eth.12011
- Prasetio & Azmi (2024). *The role of engagement intention in mediating the relationship between brand equity and engagement behavior moderated by social media context*. *International Journal of Data and Network Science*. https://doi.org/10.5267/j.ijdns.2023.12.003
- Pratono & Tjahjono (2017). *How does materialistic attitude influence the impact of corporate brand on the customers' intention to donate to corporates' charity?*. *Humanomics*, *33*, 484--498. https://doi.org/10.1108/h-07-2016-0052
- Pérez, L., & Egea, P (2019). *About Intentions to Donate for Sustainable Rural Development: An Exploratory Study. *Sustainability*. <https://doi.org/10.3390/su11030765>*. *Sustainability*, *11*(3), 765. https://doi.org/10.3390/su11030765
- Rama, A., Ali, H., & Syafruddin, S. (2026). *Enhancing charitable crowdfunding performance: the role of signaling information*. *Management Decision*. https://doi.org/10.1108/md-07-2024-1726
- Ramayanti, et al. (2024). *The Influence of Brand Orientation to Donation Intention with Attitude Toward Charity as Mediator*. *International Research Journal of Business Studies*. https://doi.org/10.21632/irjbs.17.3.267-280
- Rambocas, et al. (2017). *Brand equity and customer behavioral intentions: a mediated moderated model*. *International Journal of Bank Marketing*, *36*, 00. https://doi.org/10.1108/ijbm-09-2016-0139
- Randle & Dolnicar (2019). *Untitled*. *Voluntas*.
- Ranga, G., Khandeparkar, K., Motiani, M., & Sharma, P (2025). *Gifting a warm-glow effect: how identity influences charitable gifting. *Marketing Intelligence & Planning*. <https://doi.org/10.1108/mip-07-2023-0325>*. *Marketing Intelligence &amp; Planning*, *43*(5), 996-1012. https://doi.org/10.1108/mip-07-2023-0325
- Reich, Rob (2018). *Just Giving: Why Philanthropy Is Failing Democracy and How It Can Do Better*. *Princeton University Press*.
- Richter, Schömann et al. (2016). *Untitled*. *Frontiers in Psychology*.
- Riecken, G., & Yavas, U (2005). *The attitudes of donors and non-donors to the March of Dimes Charity in the United States: A case study in non-profit marketing*. *International Journal of Management*. https://doi.org/10.1002/nvsm.1672
- Riecken, G., Babakus, E., & Yavas, U. ( (1994). *Facing resource attraction challenges in the
   non-profit sector: A behaviouristic approach to fundraising and volunteer recruitment*. *Journal of Professional Services Marketing*. https://doi.org/10.1080/15332969.1994.9985141
- Rindfleisch, A., Malter, A., Ganesan, S., & Moorman, C. (2008). *Cross-Sectional versus Longitudinal Survey Research: Concepts, Findings, and Guidelines*. *Journal of Marketing Research*. https://doi.org/10.1509/jmkr.45.3.261
- Risi, D., Vigneau, L., Bohn, S., & Wickert, C. (2022). *Institutional theory based research on corporate social responsibility: Bringing values back in*. *International Journal of Management Reviews*. https://doi.org/10.1111/ijmr.12299
- Rizwan, et al. (2021). *Impact of brand equity on purchase intentions: empirical evidence from the health takāful industry of the United Arab Emirates*. *ISRA International Journal of Islamic Finance*. https://doi.org/10.1108/ijif-07-2019-0105
- Roberts, J.H. & Lattin, J.M (1997). *“Review of research and prospects for future insights”, Journal of Marketing Research, Vol. 34 No. 3, pp. 406-410*. *Romaniuk, J. and Sharp, B. (2003), “Measuring brand perceptions: testing quantity and quality”, Journal of Targeting, Measurement and Analysis for Marketing, Vol*, *34*(3), 406-410. https://doi.org/10.1177/002224379703400309
- Robson, A., & Hart, D. (2020). *Understanding the Correlates of Donor Intention: A Comparison of Local, National, and International Charity Destinations*. *Nonprofit and Voluntary Sector Quarterly*. https://doi.org/https://doi.org/10.1177/0899764020927097
- Rocha, A., & Monteiro, L (2023). *On the spread of charitable behavior in a social network: a model based on game theory. *Networks Heterog*. *Media*. https://doi.org/10.3934/nhm.2023036
- Rodrigues, P., & Martins, F (2016). *Perceptual and behavioural dimensions: measuring brand equity consumer based. *Journal of Fashion Marketing and Management, 20*, 507-519. <https://doi.org/10.1108/jfmm-03-2016-0019>*. *Journal of Fashion Marketing and Management: An International Journal*, *20*(4), 507-519. https://doi.org/10.1108/jfmm-03-2016-0019
- Rojas-Lamorena, et al. (2022). *A review of three decades of academic research on brand equity: A bibliometric approach using co-word analysis and bibliographic coupling*. *Journal of Business Research*, *139*, 1067--1083. https://doi.org/10.1016/j.jbusres.2021.10.025
- Romaniuk & Nenycz-Thiel (2013). *Modeling mental market share*. *Journal of Business Research*, *66*(2), 188-195. https://doi.org/10.1016/j.jbusres.2012.07.012
- Romaniuk et al. (2004). *Brand and advertising awareness: A replication and extension of a known empirical generalisation*. *Australasian Marketing Journal*, *12*(3), 70-80. https://doi.org/10.1016/s1441-3582(04)70107-x
- Romaniuk, Wight, & Faulkner (2017). *Brand awareness: revisiting an old metric for a new world*. *Journal of Product \& Brand Management*, *26*(5), 469--476. https://doi.org/10.1108/JPBM-06-2016-1242
- Romero, M. J. R., & Abril, C. (2024). *Exploring the dimensions of NGO donor-based brand equity: A literature review*. *Nonprofit Management and Leadership*, *35*(1), 219–235. https://doi.org/10.1002/nml.21601
- Romero, M. J. R., Abril, C., & Urquia-Grande, E. (2023). *Insights on NGO brand equity: A donor-based brand equity model*. *European Journal of Management and Business Economics*, *32*(4), 452–468. https://doi.org/10.1108/EJMBE-08-2022-0261
- Roodman, D., & Standley, S (2006). *Tax policies to promote private charitable giving in DAC countries. <https://doi.org/10.2139/ssrn.984021>*. *SSRN Electronic Journal*. https://doi.org/10.2139/ssrn.984021
- Rooney, P. M., Wang, X., & Ottoni-Wilhelm, M. (2021). *Dynamics of American giving: Descriptive evidence*. *Nonprofit and Voluntary Sector Quarterly*. https://doi.org/10.1177/0899764020977661
- Rossiter, John R. (2012). *Untitled*.
- Royall, R. M. (1997). *Statistical Evidence: A Likelihood Paradigm*. Chapman & Hall.
- Rozenkowska, K (2023). *Theory of planned behavior in consumer behavior research: A systematic literature review. *International Journal of Consumer Studies*. <https://doi.org/10.1111/ijcs.12970>*. *International Journal of Consumer Studies*, *47*(6), 2670-2700. https://doi.org/10.1111/ijcs.12970
- Ruangkanjanases, et al. (2022). *Creating behavioral engagement among higher education's prospective students through social media marketing activities: The role of brand equity as mediator*. *Frontiers in Psychology*, *13*. https://doi.org/10.3389/fpsyg.2022.1004573
- Rubenstein, Jennifer (2022). *Untitled*.
- Saeed, M., & Azmi, I (2019). *The nexus between customer equity and brand switching behaviour of millennial Muslim consumers. *South Asian Journal of Business Studies*. <https://doi.org/10.1108/sajbs-04-2018-0046>*. *South Asian Journal of Business Studies*, *8*(1), 62-80. https://doi.org/10.1108/sajbs-04-2018-0046
- Salamon & Anheier (1992). *In search of the non-profit sector II: The problem of classification*. *Voluntas*, *3*(3), 267--309. https://doi.org/10.1007/BF01397460
- Samballkhundev, S., Choe, Y., & Kim, D.-H. (2024). *Research on the Relationship between Customer-based Tourism Destination Brand Equity and Tourist’ Behavioral Intentions*. *Journal of Hotel & Resort*. https://doi.org/10.62532/khrc.2024.02.23.1.81
- Santos, L., Holanda, F., De Santana Oliveira, C., Pedrotti, A., De Menezes, P., & Villwock, A (2023). *Purchase intention of Amazon sustainable brands: a hybrid approach of structural equation modeling and Rasch model. *SN Business & Economics, 3*. <https://doi.org/10.1007/s43546-023-00588-0>*. *SN Business &amp; Economics*, *3*(12). https://doi.org/10.1007/s43546-023-00588-0
- Santos, R., Campo, R., Cruz, M., Montante, R., & Santos, S (2025). *Intentions of Potential Partners to Participate in a Donation Program. *International Multidisciplinary Research Journal*. <https://doi.org/10.54476/ioer-imrj/039833>*. *International Multidisciplinary Research Journal*, *7*(2). https://doi.org/10.54476/ioer-imrj/039833
- Sargeant (1999). *Charitable Giving: Towards a Model of Donor Behaviour*. *Journal of Marketing Management*, *15*(4), 215�238. https://doi.org/10.1362/026725799784870351
- Sargeant (2001). *Relationship Fundraising: How to Keep Donors Loyal*. *Nonprofit Management and Leadership*, *12*(2), 177--192. https://doi.org/10.1002/nml.12204
- Sargeant & Woodliffe (2007). *Individual giving behaviour: A multi-disciplinary review. In A. Sargeant & W. Wymer (Eds.),*. *The nonprofit marketing companion.*.
- Sargeant, et al. (2007). *Conceptualizing brand values in the charity sector: the relationship between sector, cause and organization*. *The Service Industries Journal*, *28*(3), 468�491. https://doi.org/10.1080/02642060801988142
- Sargeant & Woodliffe (2007). *Gift giving: an interdisciplinary review*. *International Journal of Nonprofit and Voluntary Sector Marketing*, *12*(4), 275--307. https://doi.org/10.1002/nvsm.308
- Sargeant, A. (2009). *Marketing management for nonprofit organizations (Third ed.)*. Oxford University Press.
- Sargeant, A. & Lee, S. (2004). *Trust and relationship commitment in the United Kingdom voluntary sector: Determinants of donor behavior*. *Psychology and Marketing, 21,*, *21*(8), 613-635. https://doi.org/10.1002/mar.20021
- Sargeant, A., West, D. C., & Ford, J. B. (2008). *Charity Brand Personality: The Relationship With Giving Behavior*. *Nonprofit and Voluntary Sector Quarterly*, *37*, 468--491. https://doi.org/10.1177/0899764007310732
- Sargeant, A., West, D. C., & Ford, J. B. (2006). *Perceptual determinants of nonprofit giving behavior*. *Journal of Business Research*, *59*, 155--165. https://doi.org/10.1016/j.jbusres.2005.04.006
- Sargeant, A., West, D. C., & Ford, J. B. (2004). *Does perception matter? An empirical analysis of donor behavior*. *The Service Industries Journal*, *24*(6), 19-36. https://doi.org/10.1080/0264206042000299167
- Sargeant, Ford & West (2006). *Untitled*. *International Journal of Nonprofit and Voluntary Sector Marketing*. https://doi.org/10.1016/j.jbusres.2005.04.006
- Satar, M., Rather, R., Parrey, S., Khan, H., & Rasul, T (2023). *Eliciting consumer-engagement and experience to foster consumer-based-brand-equity: moderation of perceived-health-beliefs. *The Service Industries Journal, 45*, 277 - 302. <https://doi.org/10.1080/02642069.2023.2191953>*. *The Service Industries Journal*, *45*(2), 277-302. https://doi.org/10.1080/02642069.2023.2191953
- Saunders-Hastings, Emma (2022). *Untitled*.
- Schamp, C., Heitmann, M., Bijmolt, T., & Katzenstein, R (2022). *The Effectiveness of Cause-Related Marketing: A Meta-Analysis on Consumer Responses. *Journal of Marketing Research, 60*, 189 - 215. <https://doi.org/10.1177/00222437221109782>*. *Journal of Marketing Research*, *60*(1), 189-215. https://doi.org/10.1177/00222437221109782
- Scharf, K (2013). *Impure Prosocial Motivation in Charity Provision: Warm-Glow Charities and Implications for Public Funding. *Public Choice: Public Goods eJournal*. <https://doi.org/10.1016/j.jpubeco.2013.10.002>*. *Journal of Public Economics*, *114*, 50-57. https://doi.org/10.1016/j.jpubeco.2013.10.002
- Schervish (1997). *Untitled*.
- Schloderer, M., Sarstedt, M., & Ringle, C. (2014). *The relevance of reputation in the nonprofit sector: the moderating effect of socio-demographic characteristics*. *International Journal of Nonprofit and Voluntary Sector Marketing*. https://doi.org/10.1002/nvsm.1491
- Schmitt (1999). *Experiential Marketing*. *Journal of Marketing Management*, *15*(1-3), 53. https://doi.org/10.1362/026725799784870496
- Schmitt (2011). *Untitled*.
- Setiya, Kieran (2022). *Untitled*.
- Shaamirova, S., Pulatova, M., & Tursunov, A. (2026). *Understanding Muslim philanthropic behavior: An extended theory of planned behavior approach to waqf in Uzbekistan*. *Journal of Islamic Accounting and Business Research*, 1-21. https://doi.org/10.1108/JIABR-10-2025-0675
- Shabbir, H., Palihawadana, D., & Thwaites, D. (2007). *Determining the antecedents and consequences of donor‐perceived relationship quality—A dimensional qualitative research approach*. *Psychology & Marketing*. https://doi.org/10.1002/mar.20161
- Shah, D., & George, M. (2020). *Linking Marketing to Nonprofit Performance*. *Journal of Public Policy & Marketing*. https://doi.org/10.1177/0743915620978538
- Shang, et al. (2019). *Giving Intention Versus Giving Behavior: How Differently Do Satisfaction, Trust, and Commitment Relate to Them?*. *Nonprofit and Voluntary Sector Quarterly*, *48*, 1023--1044. https://doi.org/10.1177/0899764019843340
- Sheeran & Webb (2016). *The Intention--Behavior Gap*. *Social and Personality Psychology Compass*, *10*, 503--518. https://doi.org/10.1111/spc3.12265
- Shehu, et al. (2016). *The Brand Personality of Nonprofit Organizations and the Influence of Monetary Incentives*. *Journal of Business Ethics*, *138*, 589--600. https://doi.org/10.1007/s10551-015-2595-3
- Shehu et al. (2015). *Profiling Donors of Blood, Money, and Time*. *Nonprofit Management and Leadership*, *25*(3), 269--295. https://doi.org/10.1002/nml.21126
- Shen, Z., Li, H., & Zhang, Y. (2025). *The mediating role of brand equity in corporate social responsibility and customer purchase intention based on text-CNN model*. *Scientific Reports*. https://doi.org/10.1038/s41598-025-28118-y
- Shostack, G.L (1987). *Service positioning through
structural change*. *Journal of Marketing*, *51*(1), 34-43. https://doi.org/10.1177/002224298705100103
- Shrestha, et al. (2023). *A Two-Phase Confirmatory Factor Analysis and Structural Equation Modelling for Customer-Based Brand Equity Framework in the Smartphone Industry*. *Decision Analytics Journal*. https://doi.org/10.1016/j.dajour.2023.100306
- Simon & Sullivan (1993). *The Measurement and Determinants of Brand Equity: A Financial Approach*. *Marketing Science*, *12*, 28-52. https://doi.org/10.1287/mksc.12.1.28
- Singer, Peter (1972). *Famine, Affluence, and Morality*. *Philosophy & Public Affairs*.
- Singer, Peter (2019). *Untitled*.
- Singh, et al. (2023). *Brand equity determinants and ecologically conscious consumer behavior in ridesharing: serial mediation and moderation analysis*. *Management of Environmental Quality: An International Journal*. https://doi.org/10.1108/meq-06-2023-0165
- Sirgy (1982). *Self-Concept in Consumer Behavior: A Critical Review*. *Journal of Consumer Research*, *9*(3), 287. https://doi.org/10.1086/208924
- Small, Deborah A., Loewenstein, George & Slovic, Paul (2007). *Sympathy and callousness: The impact of deliberative thought on donations to identifiable and statistical victims*. *Organizational Behavior and Human Decision Processes*.
- Smith & McSweeney (2007). *Charitable Giving: The Effectiveness of a Revised Theory of Planned Behaviour Model in Predicting Donating Intentions and Behaviour*. *Journal of Community and Applied Social Psychology*, *17*(5), 363--386. https://doi.org/10.1002/casp.906
- Sousa & Ferreira (2023). *Employee based brand equity: a systematic review of literature, framework development, and implications for future research*. *Journal of Management History*, *30*(3), 475�492. https://doi.org/10.1108/jmh-07-2023-0069
- Spence (1973). *Job Market Signaling*. *Quarterly Journal of Economics*, *87*(3), 355--374. https://doi.org/10.2307/1882010
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Unknown Author (n.d.). *Untitled*.
- Stebbins & Hartman (2013). *Charity brand personality: can smaller charitable organizations leverage their brand's personality to influence giving*. *International Journal of Nonprofit and Voluntary Sector Marketing*, *18*(3), 203--215. https://doi.org/10.1002/nvsm.1468
- Stocchi & Fuller (2017). *A comparison of brand equity strength across consumer segments and markets*. *Journal of Product \& Brand Management*, *26*(5), 453--468. https://doi.org/10.1108/JPBM-06-2016-1220
- Stollar, et al. (2024). *Understanding how Branding Influences Gen Z's Behavioral Intent with Charitable Food Organizations*. *Journal of Applied Communications*. https://doi.org/10.4148/1051-0834.2551
- Strahilevitz, Michal & Myers, John G. (1998). *Donations to Charity as Purchase Incentives: How Well They Work May Depend on What You Are Trying to Sell*. *Journal of Consumer Research*, *24*(4), 434-446. https://doi.org/10.1086/209519
- Styles & Ambler (1995). *Untitled*.
- Stötzer, et al. (2021). *Using Certifications to Signal Trustworthiness and Reduce the Perceived Risk of Donors: An Exploratory Investigation into the Impact of Charity Labels*. *Journal of Nonprofit \& Public Sector Marketing*, *35*(3), 265--289. https://doi.org/10.1080/10495142.2021.1954131
- Stötzer, S., Andeßner, R. C., & Scheichl, S (2020). *Charity flea markets – an amalgamation of product philanthropy and volunteering. *International Review on Public and Nonprofit Marketing, 17*, 203-224. <https://doi.org/10.1007/s12208-019-00242-2>*. *International Review on Public and Nonprofit Marketing*, *17*(2), 203-224. https://doi.org/10.1007/s12208-019-00242-2
- Suarez & Valentin (2019). *Untitled*. *Social & Cultural Geography*.
- Sundar et al. (2014). *Untitled*. *Computers in Human Behavior*.
- Suppe, F. (1977). *The Structure of Scientific Theories*. University of Illinois Press.
- Södergren, J. (2021). *Brand authenticity: 25 Years of research*. *International Journal of Consumer Studies*. https://doi.org/10.1111/ijcs.12651
- Talie, et al. (2020). *Voluntary blood donation among Bahir Dar University students: Application of integrated behavioral model, Bahir Dar, Northwest Ethiopia*. *Journal of Blood Medicine*, *11*, 429--437. https://doi.org/10.2147/JBM.S277411
- Tam (2008). *Brand familiarity: its effects on satisfaction evaluations*. *Journal of Services Marketing*, *22*(1), 3--12. https://doi.org/10.1108/08876040810851914
- Tanouri, et al. (2019). *Transformative gamification services for social behavior brand equity: a hierarchical model*. *Journal of Service Theory and Practice*. https://doi.org/10.1108/jstp-06-2018-0140
- Tarsney, Christian (2023). *Untitled*.
- Tasci (2020). *A Critical Review and Reconstruction of Perceptual Brand Equity*. *International Journal of Contemporary Hospitality Management*, *32*(5), 1992--2015. https://doi.org/10.1108/ijchm-03-2020-0186
- Taylor (2005). *Untitled*. *Nonprofit and Voluntary Sector Quarterly*.
- Taylor, J. A., & Miller Stevens, K. (2018). *Relational exchange in nonprofits: The role of identity saliency and relationship satisfaction*. *International Journal of Nonprofit and Voluntary Sector Marketing*. https://doi.org/https://doi.org/10.1002/nvsm.1618
- Taylor, Robert S. (2018). *Untitled*.
- Templier, M., & Paré, G. (2015). *A framework for guiding and evaluating literature reviews*. *Communications of the Association for Information Systems*, *37*. https://doi.org/10.17705/1cais.03706
- Thanh, B., Hieu, L., & Lan, L (2026). *The Impact of Brand Equity Dimensions on Purchase Intention: Empirical Evidence from the Vietnamese Life Insurance Market. *European Journal of Management, Economics and Business*. <https://doi.org/10.59324/ejmeb.2026.3(1).18>*. *European Journal of Management, Economics and Business*, *3*(1), 213-226. https://doi.org/10.59324/ejmeb.2026.3(1).18
- Theurer, et al. (2018). *Employer Branding: A Brand Equity--based Literature Review and Research Agenda*. *International Journal of Management Reviews*, *20*(1), 155--179. https://doi.org/10.1111/ijmr.12121
- Thoits, P. (2012). *Role-Identity Salience, Purpose and Meaning in Life, and Well-Being among Volunteers*. *Social Psychology Quarterly*. https://doi.org/10.1177/0190272512459662
- Thoits, P. (2021). *Motivations for Peer-Support Volunteering: Social Identities and Role-Identities as Sources of Motivation*. *Nonprofit and Voluntary Sector Quarterly*. https://doi.org/10.1177/0899764020983897
- Thomson, Matthew; MacInnis, Deborah J.; Park, C. Whan (2005). *The Ties That Bind: Measuring the Strength of Consumers’ Emotional Attachments to Brands*. *Journal of Consumer Psychology*, *15*(1), 77–91. https://doi.org/10.1207/s15327663jcp1501_10
- Tidwell, M. (2005). *A social identity model of prosocial behaviors within nonprofit organizations.*. *Nonprofit Management and Leadership*. https://doi.org/10.1002/nml.82
- Torras-Gómez, E., Ruiz-Eugenio, L., Sordé-Martí, T., & Duque, E. (2021). *Challenging Bourdieu’s Theory: Dialogic Interaction as a Means to Provide Access to Highbrow Culture for All*. *SAGE Open*. https://doi.org/10.1177/21582440211010739
- Torrent Sellens, J., Salazar-Concha, C., Ficapal Cusí, P., & Saigí-Rubió, F (2021). *Using Digital Platforms to Promote Blood Donation: Motivational and Preliminary Evidence from Latin America and Spain*. *International Journal of Environmental Research and Public Health*. https://doi.org/10.3390/ijerph18084270
- Tranfield, D., Denyer, D., & Smart, P. (2003). *Towards a methodology for developing evidence-informed management knowledge by means of systematic review by means of systematic review*. *British Journal of Management*, *14*(3), 207-222. https://doi.org/10.1111/1467-8551.00375
- Tuominen, P. (1999). *Managing Brand Equity*. *Liiketaloudellinen aikakauskirja LTA - Finnish Journal of Business Economics is now Nordic Journal of Business*.
- Ulker‐Demirel, E., & Ciftci, G (2020). *A systematic literature review of the theory of planned behavior in tourism, leisure and hospitality management research. *Journal of Hospitality and Tourism Management*. <https://doi.org/10.1016/j.jhtm.2020.04.003>*. *Journal of Hospitality and Tourism Management*, *43*, 209-219. https://doi.org/10.1016/j.jhtm.2020.04.003
- Ulrich, D. & Smallwood, N (2007). *Building
a leadership brand*. *Harvard Business Review*, *85*(7-8), 92–100, 192.
- Urde (1999). *Brand orientation: a mindset for building brands into strategic resources*. *Journal of Marketing Management*, *15*(1-3), 117-133. https://doi.org/10.1362/026725799784870504
- Van Ingen, E., & Wilson, J. (2017). *I Volunteer, Therefore I am? Factors Affecting Volunteer Role Identity*. *Nonprofit and Voluntary Sector Quarterly*. https://doi.org/10.1177/0899764016659765
- Van Steenburg, E., & Spears, N. (2021). *How preexisting beliefs and message involvement drive charitable donations: an integrated model*. *European Journal of Marketing*. https://doi.org/10.1108/ejm-01-2020-0031
- Van Teunenbroek, et al. (2020). *Look to Others Before You Leap: A Systematic Literature Review of Social Information Effects on Donation Amounts*. *Nonprofit and Voluntary Sector Quarterly*, *49*(1), 53--73. https://doi.org/10.1177/0899764019869537
- Vargo & Lusch (2004). *Evolving to a new dominant logic for marketing*. *Journal of Marketing*, *68*(1), 1. https://doi.org/10.1509/jmkg.68.1.1.24036
- Veludo-De-Oliveira, T., Alhaidari, I. S., Yani-De-Soriano, M., & Yousafzai, S. Y. (2016). *Comparing the Explanatory and Predictive Power of Intention-Based Theories of Personal Monetary Donation to Charitable Organizations*. *VOLUNTAS: International Journal of Voluntary and Nonprofit Organizations*. https://doi.org/10.1007/s11266-016-9690-7
- Venable, et al. (2005). *The role of brand personality in charitable giving: An assessment and validation*. *Journal of the Academy of Marketing Science*, *33*(3), 295�312. https://doi.org/10.1177/0092070305276147
- Vogel (2018). *Untitled*. *Voluntas: International Journal of Voluntary and Nonprofit Organizations*.
- Wakefield, J., Bowe, M., & Kellezi, B. (2021). *Who helps and why? A longitudinal exploration of volunteer role‐identity, between‐group closeness, and community identification as predictors of coordinated helping during the COVID‐19 pandemic*. *The British Journal of Social Psychology*. https://doi.org/10.1111/bjso.12523
- Washburn, J. H., & Plank, R. E. (2002). *Measuring Brand Equity: An Evaluation of a Consumer-Based Brand Equity Scale*. *Journal of Marketing Theory and Practice*, *10*(1), 46--62. https://doi.org/10.1080/10696679.2002.11501909
- Watanuki & Akama (2022). *Neural substrates of brand equity: applying a quantitative meta-analytical method for neuroimage studies*. *Heliyon*, *8*. https://doi.org/10.1016/j.heliyon.2022.e09702
- Webb & Sheeran (2006). *Does changing behavioral intentions engender behavior change? A meta-analysis of the experimental evidence*. *Psychological Bulletin*, *132*(2), 249--268. https://doi.org/10.1037/0033-2909.132.2.249
- Wedel, M., Kannan, P., & Tyser, R. J. (2016). *Marketing Analytics for Data-Rich Environments*. *Journal of Marketing*. https://doi.org/10.1509/jm.15.0413
- White, K., Habib, R., & Hardisty, D. J. (2023). *[Motivpluralismus im Spendenverhalten]*.
- White, K., Sutton, L. S. C., & Zhao, X. (2023). *Charitable donations and the theory of planned behaviour: A systematic review and meta-analysis*. *PLOS ONE*. https://doi.org/10.1371/journal.pone.0286053
- Wilhelm, et al. (2014). *Why Do People Give? Testing Pure and Impure Altruism*. *AARN: The Evolution of Social Behavior (Topic)*. https://doi.org/10.1257/aer.20141222
- Willer, R., Wimer, C., & Owens, L (2015). *What drives the gender gap in charitable giving? Lower empathy leads men to give less to poverty relief.. *Social science research, 52*, 83-98. <https://doi.org/10.1016/j.ssresearch.2014.12.014>*. *Social Science Research*, *52*, 83-98. https://doi.org/10.1016/j.ssresearch.2014.12.014
- Willmott, H (2010). *Creating ‘value’ beyond the point of production: branding, financialization and market capitalization. *Organization, 17*, 517 - 542. <https://doi.org/10.1177/1350508410374194>*. *Organization*, *17*(5), 517-542. https://doi.org/10.1177/1350508410374194
- Winterich, K., & Barone, M (2011). *Warm Glow or Cold, Hard Cash? Social Identity Effects on Consumer Choice for Donation versus Discount Promotions. *Journal of Marketing Research, 48*, 855 - 868. <https://doi.org/10.1509/jmkr.48.5.855>*. *Journal of Marketing Research*, *48*(5), 855-868. https://doi.org/10.1509/jmkr.48.5.855
- Wit, A., & Bekkers, R (2016). *Government Support and Charitable Donations: A Meta-Analysis of the Crowding-out Hypothesis. *Journal of Public Administration Research and Theory, 27*, 301-319. <https://doi.org/10.1093/jopart/muw044>*. *Journal of Public Administration Research and Theory*, muw044. https://doi.org/10.1093/jopart/muw044
- Wolniak, M., & Houston, S. (2022). *A sociologist in the field of social work: Pierre Bourdieu's theory and its relevance for social work practice*. *Critical and Radical Social Work*.
- Wong, H.Y. & Merrilees, B (2007). *Closing the
marketing strategy to performance gap: The role
of brand orientation*. *Journal of Strategic Marketing*, *15*(5), 387-402. https://doi.org/10.1080/09652540701726942
- Wood (2000). *Brands and brand equity: definition and management*. *Management Decision*, *38*(9), 662--669. https://doi.org/10.1108/00251740010379100
- Wood, W., & Rünger, D. (2016). *Psychology of Habit*. *Annual review of psychology*. https://doi.org/10.1146/annurev-psych-122414-033417
- Wu, et al. (2020). *An Integrated Framework of Customer-based Brand Equity and Theory of Planned Behavior: A Meta-analysis Approach*. *The Journal of Asian Finance, Economics and Business*, *7*(8), 371--381. https://doi.org/10.13106/JAFEB.2020.VOL7.NO8.371
- Wu, J., Yasin, M., & Ng, C (2025). *Integrating Social Cognitive Theory and Brand Equity Models: A Framework for Analyzing Audience Engagement Behavior in IP Animated Films. *International Journal of Academic Research in Business and Social Sciences*. <https://doi.org/10.6007/ijarbss/v15-i8/26139>*. *International Journal of Academic Research in Business and Social Sciences*, *15*(8). https://doi.org/10.6007/ijarbss/v15-i8/26139
- Wu, L (2011). *Analysis of Influencing Factors of Civic Charitable Donation Based on Theory of Planned Behavior: Data from Liaoning Province*. *Soft Science*.
- Wu, S.-I., Lu, C.-L., & Wu, C.-C. (2022). *Optimization and selection of cause marketing mode with the warm glow effect*. *PloS one*, *17*. https://doi.org/10.1371/journal.pone.0272724
- Wu, X., Wu, T., Guo, X., & Yang, H. ( (2025). *Signaling to the Crowd: Disclosure of Donors’ Hierarchical Virtual Badges in
Charitable Crowdfunding*. *International Journal of Electronic Commerce*. https://doi.org/10.1080/10864415.2025.2594330
- Wymer & Akbar (2019). *Brand authenticity's influence on charity support intentions*. *Journal of Nonprofit \& Public Sector Marketing*, *31*(5), 507--527. https://doi.org/10.1080/10495142.2018.1526754
- Wymer & Akbar (2017). *Brand authenticity, its conceptualization, and its relevance to nonprofit marketing*. *International Review on Public and Nonprofit Marketing*, *14*(3), 359--374. https://doi.org/10.1007/s12208-017-0177-z
- Wymer, et al. (2021). *The antecedents of charity trust and its influence on charity supportive behavior*. *International Journal of Nonprofit and Voluntary Sector Marketing*, *1*(7). https://doi.org/10.1002/nvsm.1690
- Wymer & Čačija (2025). *Brand Strength's Influence on Volunteers' Retention and Support Intentions*. *Journal of Nonprofit \& Public Sector Marketing*, *37*, 818--852. https://doi.org/10.1080/10495142.2024.2448420
- Wymer, W., Knowles, P., & Gomes, R. ( (2014). *Introduction to nonprofit marketing*. *Nonprofit
  Marketing: Marketing Management for Charitable and Nongovernmental Organizations*. https://doi.org/10.4135/9781483329031.n1
- Xu, et al. (2022). *Machine learning based customer meta-combination brand equity analysis for marketing behavior evaluation*. *Inf. Process. Manag.*, *59*, 102800. https://doi.org/10.1016/j.ipm.2021.102800
- Yang, D., Sonmez, M., Gonzalez, M., Liu, Y., & Yoder, C (2019). *Consumer-based brand equity and consumer-based brand performance: evidence from smartphone brands in the USA. *Journal of Brand Management*, 1-16. <https://doi.org/10.1057/s41262-019-00154-w>*. *Journal of Brand Management*, *26*(6), 717-732. https://doi.org/10.1057/s41262-019-00154-w
- Yen, W.-H., Caskey, D., & Warden, C. A. (2022). *Development and Empirical Study of Religion Affiliated Nonprofit Organizations’ Brand Equity Questionnaire: Testing Brand Awareness and Trust Among Non-members*. *VOLUNTAS: International Journal of Voluntary and Nonprofit Organizations*. https://doi.org/10.1007/s11266-022-00527-x
- Yeğin & Ikram (2022). *Developing a Sustainable Omnichannel Strategic Framework toward Circular Revolution: An Integrated Approach*. *Sustainability*. https://doi.org/10.3390/su141811578
- Yoo, Boonghee; Donthu, Naveen (2001). *Developing and validating a multidimensional consumer-based brand equity scale*. *Journal of Business Research*, *52*(1), 1--14. https://doi.org/10.1016/S0148-2963(99)00098-3
- Zhang, Y., Li, J., Liu, C., Shen, Y., & Li, G (2020). *The effect of novelty on travel intention: the mediating effect of brand equity and travel motivation. *Management Decision*. <https://doi.org/10.1108/md-09-2018-1055>*. *Management Decision*, *59*(6), 1271-1290. https://doi.org/10.1108/md-09-2018-1055
- Zhao, H., Jin, B., Liu, Q., Ge, Y., Chen, E., Zhang, X., & Xu, T (2020). *Voice of Charity: Prospecting the Donation Recurrence & Donor Retention in Crowdfunding. *IEEE Transactions on Knowledge and Data Engineering, 32*, 1652-1665. <https://doi.org/10.1109/tkde.2019.2906199>*. *IEEE Transactions on Knowledge and Data Engineering*, *32*(8), 1652-1665. https://doi.org/10.1109/tkde.2019.2906199
- Zheng, et al. (2025). *Integrating Customer-Based Brand Equity and the Theory of Planned Behavior to Predict Electric Vehicle Adoption in China: The Moderating Role of Perceived Price*. *PloS one*, *20*(3), Article e0329224. https://doi.org/10.1371/journal.pone.0329224
- Zhou, L., & Xue, F. (2025). *Make a Charitable Birthday Wish on Facebook: An Extended Theory of Planned Behavior*. *Journal of Nonprofit & Public Sector Marketing*, *37*(2), 245-269. https://doi.org/10.1080/10495142.2024.2360197
- Zhu, L., He, Y., Chen, Q., & Hu, M (2017). *It's the thought that counts: The effects of construal level priming and donation proximity on consumer response to donation framing. *Journal of Business Research, 76*, 44-51. <https://doi.org/10.1016/j.jbusres.2017.03.007>*. *Journal of Business Research*, *76*, 44-51. https://doi.org/10.1016/j.jbusres.2017.03.007
- Zollo, L., Filieri, R., Rialti, R., & Yoon, S (2020). *Unpacking the relationship between social media marketing and brand equity: The mediating role of consumers’ benefits and experience. *Journal of Business Research*. <https://doi.org/10.1016/j.jbusres.2020.05.001>*. *Journal of Business Research*, *117*, 256-267. https://doi.org/10.1016/j.jbusres.2020.05.001
- Çifci, S., Ekinci, Y., Whyatt, G., Japutra, A., Molinillo, S., & Siala, H (2016). *A cross validation of Consumer-Based Brand Equity models: Driving customer equity in retail brands. *Journal of Business Research, 69*, 3740-3747. <https://doi.org/10.1016/j.jbusres.2015.12.066>*. *Journal of Business Research*, *69*(9), 3740-3747. https://doi.org/10.1016/j.jbusres.2015.12.066