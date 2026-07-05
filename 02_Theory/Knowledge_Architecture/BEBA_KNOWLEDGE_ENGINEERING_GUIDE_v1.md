# BEBA Knowledge Engineering Guide v1

Status: canonical working architecture

## Purpose

This guide defines how literature, empirical evidence, claims, concepts, ontology candidates, and dissertation chapters are connected in the BEBA research system.

The goal is to transform literature into reusable scientific knowledge rather than document summaries.

## Core Pipeline

Raw literature review -> Markdown -> Evidence Map -> Claim Extraction -> Concept Workspace -> Theory Integration -> Ontology Candidate -> Manual Review -> Canonical Ontology -> Chapters and Papers

## Main Principle

Do not move directly from a literature review to a dissertation chapter. First transform the review into structured knowledge.

## Artefact Types

### Evidence Map

A non-interpretive extraction of what is supported, mixed, contradicted, or missing.

### Claim

A minimal scientific statement with evidence and confidence.

### Concept Workspace

A stable home for all knowledge about one concept.

### Theory Integration Unit

A reflection on how a concept changes, supports, or challenges BEBA.

### Ontology Candidate

A proposed stable concept entry. It is not canonical until manually reviewed.

## Concept Workspace Structure

Each important concept may receive a workspace:

```text
02_Theory/Knowledge/Concepts/<concept>/
  README.md
  claims.md
  evidence.md
  definitions.md
  boundary_conditions.md
  measurement.md
  relationships.md
  ontology_candidate.md
```

For the dissertation phase, compact single-file concept entries are acceptable when the concept is not yet central.

## Claim Structure

Each claim should contain:

- Claim ID
- Concept
- Statement
- BEBA Layer
- Relationship type
- Evidence
- Confidence
- Status
- Implications for BEBA

## Confidence Levels

High:
Supported by multiple sources, strong theoretical grounding, and limited contradiction.

Medium:
Supported but context-dependent, contested, or methodologically limited.

Low:
Plausible but under-supported, speculative, or only weakly evidenced.

## Manual Review Rule

Only the researcher can promote a candidate claim, concept, or ontology entry to canonical status.

AI systems may generate candidates, but they do not define the theory.

## Dissertation Rule

Chapters are outputs of the knowledge base. They do not become the knowledge base.

## Current Implementation Stage

During the dissertation phase, the system remains lightweight:

- Markdown first.
- Git versioning.
- Concept files before databases.
- Ontology candidates before canonical ontology.
- No automatic rewriting of core theory.

## Future Extension

If the system grows, claims and relationships can later be moved into YAML, CSV, DuckDB, Obsidian Dataview, or a graph database. The information model should remain stable even if the storage technology changes.
