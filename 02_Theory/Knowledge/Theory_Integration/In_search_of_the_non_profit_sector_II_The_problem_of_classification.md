---
concept: In_search_of_the_non_profit_sector_II_The_problem_of_classification
review: REVIEW-000070
claim_count: 6
claim_ids:
- SC-000011
- SC-000012
- SC-000013
- SC-000014
- SC-000015
- SC-000016
status: accepted
review_status: reviewed
reviewed_at: '2026-07-12T10:12:59.497100+00:00'
reviewed_by: human
---

# Input Reviewed

The reviewed input consists of a set of six candidate claims (SC-000011 to SC-000016) concerning the theory and application of nonprofit sector classification. The claims collectively argue for a specific approach to classification, advocating for a system like the International Classification of Nonprofit Organizations (ICNPO) over standard industrial codes (e.g., ISIC) or nationally-specific taxonomies (e.g., NTEE). The core arguments are based on the need for a system that is internationally comparable, sensitive to the sector's heterogeneity, and based on the organisation's primary economic activity.

# Core Theoretical Implication

The central implication for BEBA is that **sector classification is not merely a methodological choice but a foundational theoretical act.** The way we segment the nonprofit universe pre-determines the boundaries of our analysis, the validity of our comparisons, and the generalizability of our findings. Adopting a rigorous, internationally-validated system like ICNPO provides a stable and theoretically defensible framework for defining the operational environment in which nonprofit brands and behaviours are studied. It moves the concept of "sector" from an unexamined assumption to a structured, measurable variable.

# BEBA Layer Affected

This integration primarily affects two BEBA layers:

1.  **Societal Layer:** The choice of a classification system is a macro-level decision that defines how the nonprofit sector is situated within the broader society and across national contexts. It provides the vocabulary for comparative societal analysis.
2.  **Organisational Layer:** The application of the classification system (e.g., assigning an ICNPO code to an NPO) directly structures any analysis at the organisational level. It becomes a key characteristic of the organisation itself, influencing its strategic context, competitive set, and stakeholder environment.

# Existing Claims Supported

These claims provide foundational support for any BEBA claims that rely on:
-   **Generalizability:** Claims that posit BEBA mechanisms as being applicable across different types of nonprofits or national contexts. This claim set provides the *warrant* to make such comparisons in a structured way.
-   **Comparative Analysis:** Any claim that compares the effectiveness of branding between different subsectors (e.g., "Brand trust is more critical for fundraising behaviour in international aid NPOs than in local arts NPOs").
-   **Context-Sensitivity:** Claims that argue organisational context matters. This provides a specific, operational way to define that context.

# Existing Claims Challenged

These claims implicitly challenge any BEBA claims that:
-   Treat the nonprofit sector as a monolithic entity, ignoring internal heterogeneity.
-   Rely on data or findings derived from standard industrial classifications (ISIC/NACE) or US-centric classifications (NTEE) to make general statements about nonprofit branding.
-   Assume that legal status is the most important classifier for understanding organisational behaviour, as opposed to primary economic activity.

# New Candidate Claims

This integration suggests several new candidate claims for BEBA:

-   **BEBA-C-Moderation-ICNPO:** The functional relationship between brand equity dimensions (e.g., awareness, trust, identity) and stakeholder behaviours (e.g., donating, volunteering) is moderated by the nonprofit's primary field of activity, as defined by its ICNPO group.
-   **BEBA-C-Variance-ICNPO:** A significant portion of the variance in brand-enabled behaviour across the nonprofit sector can be explained by an organisation's ICNPO classification.
-   **BEBA-C-Architecture-ICNPO:** Different ICNPO groups represent distinct "behavioural arenas" which may require different brand-enabled behaviour architectures for optimal effectiveness.

# Boundary Conditions

The ICNPO classification system itself introduces a critical set of **boundary conditions** for the BEBA theory. The theory's propositions may not apply uniformly across all ICNPO groups. For example, the mechanisms by which a brand enables behaviour for a hospital (ICNPO Group 2: Health) may differ fundamentally from those for a political advocacy group (ICNPO Group 7: Law, Advocacy and Politics). The ICNPO groups thus serve as theoretically-grounded parameters for testing the limits and scope of BEBA's explanatory power.

# Model Competition Implications

This integration enriches the potential for model competition within the BEBA framework. It moves beyond simply comparing `Model A` vs. `Model B`. It introduces a multi-group comparison logic:

1.  **Universal vs. Specific Models:** We can now formally test a universal BEBA model (hypothesized to fit well across all NPOs) against a set of sector-specific models (where parameters are allowed to vary across ICNPO groups).
2.  **Factorial Designs:** ICNPO classification can be used as a key factor in research designs to test for interaction effects. For example, does a specific brand intervention work equally well in Group 1 (Culture) and Group 4 (Social Services)?
3.  **Explanation of Heterogeneity:** If a single model shows poor overall fit, ICNPO provides a structured way to investigate if the misfit is systematic and can be explained by inter-group differences.

# Ontology Candidate Implications

This analysis strongly suggests that `ICNPO Group` should be elevated to a core concept within the BEBA ontology.

-   **New Concept Candidate:** `Concept: ICNPO_Group`. This would be an enumerated type with 12 primary values (e.g., `ICNPO-01: Culture and Recreation`, `ICNPO-02: Education and Research`, etc.).
-   **Relationship:** The `Organisation` concept should have a mandatory relationship, such as `hasPrimaryActivity (Organisation, ICNPO_Group)`.
-   **Significance:** Treating ICNPO classification as an ontological element, rather than just metadata, ensures that it is systematically considered in all future theory development and empirical modeling.

# Recommendation

1.  **Formal Adoption:** Formally adopt the International Classification of Nonprofit Organizations (ICNPO) as the canonical system for segmenting the nonprofit sector within the BEBA research program. This decision should be recorded in an ADR.
2.  **Ontology Development:** Create a new ontology candidate file for `ICNPO_Group` and establish its relationship to the `Organisation` concept in the BEBA Information Model.
3.  **Incorporate into Research Design:** Mandate the inclusion of ICNPO classification as a key descriptive and potentially moderating variable in all future empirical studies. This strengthens the BEBA project's commitment to comparative research and transparency.
4.  **Update Guiding Documents:** The `01_THEORETICAL_MAP.md` and related knowledge engineering guides should be updated to reflect the foundational role of this classification system in defining the organisational layer of the BEBA framework.

## Integration from REVIEW-000070

**Integrated:** 2026-07-13T19:03:53.689054+00:00

**Accepted claims (6):**
- SC-000011: A classification system's utility for comparative nonprofit research is a function of its optimised 
- SC-000012: Standard industrial classifications like ISIC systematically underestimate the heterogeneity of the 
- SC-000013: Nationally-specific, highly detailed taxonomies like the NTEE are not robust for international compa
- SC-000014: The nonprofit sectors of developing countries cannot be accurately represented without a distinct ca
- SC-000015: Classifying nonprofit organisations by their primary economic activity at the establishment level pr
- SC-000016: The ICNPO framework can be reliably applied across diverse national contexts to produce comparable d

**Accepted evidence (8):**
- EVID-001602: A classification system's utility for comparative nonprofit research is a function of its optimised 
- EVID-001603: Standard industrial classifications, such as ISIC and NACE, are inadequate for detailed nonprofit se
- EVID-001604: Highly detailed, nationally-specific taxonomies, such as the US NTEE, are not suitable for internati
- EVID-001605: To accurately represent the global nonprofit sector, a classification system must include a distinct
- EVID-001606: Classifying nonprofit organisations based on the 'primary economic activity' of the 'establishment' 
- EVID-001607: There is a general consensus in the research field that systematic classification is an essential pr
- EVID-001608: Classification should be viewed not as a mere administrative task, but as a fundamental 'technology 
- EVID-001609: The proposed International Classification of Nonprofit Organizations (ICNPO) provides a robust and w

**Accepted sources (1):**
- SRC-000331: Salamon and Anheier (1992)

