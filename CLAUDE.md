# CLAUDE.md - BEBA Monography Repository

## Role

You are working inside the BEBA Research Operating System (BEBA-ROS).

This repository is not a normal dissertation folder. It is a knowledge-centric research system for developing the monograph and related papers on **Nonprofit Brand Equity as a Brand-Enabled Behaviour Architecture (BEBA)**.

## Core Rule

Git is the research memory. Chat history is not research memory.

Do not treat generated text as part of the project until it is written to the repository and committed.

## Repository Function

This repository contains:

- theory development
- monograph structure
- knowledge architecture
- ontology candidates
- concept files
- claims
- relationships
- research compass files
- ADRs
- publication strategy

It does **not** contain:

- raw survey data
- local DuckDB databases
- operational CFA/SEM execution files
- sensitive data

The empirical pipeline lives separately in `/home/Gerald/Pipeline` and/or `GeraldCzech/BrandEquityPipeline`.

## Read First

Before doing substantial work, read:

1. `START_HERE.md`
2. `README.md`
3. `00_MASTER_OUTLINE.md`
4. `01_THEORETICAL_MAP.md`
5. `ConstructLedger.md`
6. `glossary.md`
7. `02_Theory/Knowledge_Architecture/BEBA_INFORMATION_MODEL_v1.md`
8. `02_Theory/Knowledge_Architecture/BEBA_KNOWLEDGE_ENGINEERING_GUIDE_v1.md`
9. `02_Theory/Knowledge_Architecture/BEBA_RELATIONSHIP_MODEL_v1.md`
10. `02_Theory/Knowledge_Architecture/BEBA_ONTOLOGY_GUIDE_v1.md`

## Research Principles

- Theory before models.
- Behaviour before brands.
- Explanation before prediction.
- Competing explanations over single models.
- Evidence before preference.
- Replication before novelty.
- Transparency over convenience.
- One canonical definition per construct.
- AI supports science; it does not define the theory.

## Knowledge Pipeline

Use this logic:

```text
Raw literature
-> Markdown
-> Evidence Map
-> Claims
-> Concept Workspace
-> Theory Integration
-> Ontology Candidate
-> Manual Review
-> Canonical Ontology
-> Chapters / Papers
```

Never jump directly from a literature review to a chapter.

## Object Types

The BEBA information model distinguishes:

- Concept
- Theory
- Model
- Construct
- Scale
- Claim
- Evidence
- Paper
- Chapter
- Figure

When creating files, make clear which object type you are producing.

## Literature Rules

- Never invent literature.
- Never invent citations.
- If evidence is missing, write: `Not sufficiently covered in the reviewed literature.`
- Keep evidence, interpretation and future research separate.
- Literature is stored and verified via Citavi/BibTeX/Crossref where applicable.

## Empirical Rules

- Never invent sample sizes, coefficients, fit indices, p-values or model comparisons.
- Empirical claims must come from verified pipeline outputs.
- Do not move raw data into this repository.
- If numbers are needed and unavailable, state that the pipeline output must be consulted.

## Writing Rules

- German working drafts are acceptable.
- English is preferred for platform architecture and publication-ready theory objects.
- Use APA 7 logic for citations.
- Avoid internal references to proposals or interim reports in dissertation-style text.
- Chapters must begin from scientific questions, not from lists of literature.

## Change Rules

Significant changes to definitions, construct mappings, model architecture or theory status require:

- ADR if architectural/theoretical,
- DecisionLog if operational/minor,
- ConstructLedger update if measurement-related,
- glossary update if terminology changes.

## Output Discipline

When asked to create or modify content:

1. Identify the correct object type.
2. Identify the correct target directory.
3. Preserve existing canonical files unless explicitly asked to update them.
4. Prefer candidate files before changing ontology or core theory.
5. Summarise what changed.

## Current Research Question

How do nonprofit brands become behaviourally effective under conditions of uncertainty?
