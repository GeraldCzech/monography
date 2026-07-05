# /extract

## Purpose

Transform one literature review into structured BEBA knowledge objects.

## Usage

`/extract literature/markdown/<file>.md`

## Instructions

1. Read `CLAUDE.md`.
2. Read `.claude/agents/literature-analyst.md`.
3. Read the available protocols in `literature/prompts/` if present.
4. Read the target markdown review.
5. Produce:
   - Evidence Map
   - Claim candidates
   - Scientific Knowledge Unit if warranted
   - Ontology Candidate
   - Processing note

## Target Directories

- Evidence Map: `literature/evidence/<same_filename>.md`
- Scientific Knowledge Unit: `literature/synthesized/<same_filename>.md`
- Ontology Candidate: `literature/ontology/<same_filename>.md`
- Claim candidates: `02_Theory/Knowledge/Claims/<topic>-claims.md`

## Quality Rules

- Never invent literature.
- Never invent citations.
- If information is absent, write: `Not sufficiently covered in the reviewed literature.`
- Do not update canonical ontology automatically.
