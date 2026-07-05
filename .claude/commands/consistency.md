# /consistency

## Purpose

Check the repository for conceptual, terminology and structure drift.

## Usage

`/consistency`

## Instructions

Review:

- `glossary.md`
- `ConstructLedger.md`
- `01_THEORETICAL_MAP.md`
- `02_Theory/Active/core.md`
- `02_Theory/Knowledge/Concepts/`
- `02_Theory/Knowledge/Claims/`
- `05_Chapters/`
- `06_Papers/`

## Check For

1. Different definitions of the same concept.
2. Abbreviations missing from glossary.
3. Constructs missing from ConstructLedger.
4. Claims not mapped to concepts.
5. Concepts without BEBA layer.
6. Chapter claims not supported by Knowledge objects.
7. Empirical claims without pipeline source.
8. Terminology drift between German and English texts.

## Output

Create or update:

`02_Theory/Knowledge/CONSISTENCY_REPORT.md`

## Rule

Report inconsistencies. Do not automatically rewrite canonical files unless explicitly instructed.
