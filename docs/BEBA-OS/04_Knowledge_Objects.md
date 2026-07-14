# Knowledge Objects

Alle Wissensobjekte werden als Markdown-Dateien mit YAML-Frontmatter gespeichert. Der zentrale Index liegt in `02_Theory/Knowledge/INDEX.yaml`.

## Objekttypen

### REVIEW — Literatur-Review-Objekt

**Datei:** `Knowledge/Reviews/REVIEW-XXXXXX.md`  
**Erzeugt in:** Schritt 6 des Literatur-Workflows

```yaml
id: REVIEW-000001
source_file: /home/gerald/research/literature/markdown/LoitRev_Warm_Glow_Giving.md
stem: LoitRev_Warm_Glow_Giving
started: '2026-07-05T16:13:13+00:00'
finished: '2026-07-05T16:45:20+00:00'
status: complete
primary_concept: Warm_Glow_Giving
source_ids: [SRC-000001, SRC-000002, ...]
evidence_ids: [EVID-000001, EVID-000002, ...]
claim_ids: [WG-000001, WG-000002, ...]
```

### SRC — Source-Objekt

**Datei:** `Knowledge/Sources/SRC-XXXXXX.md`  
**BibTeX-Stub:** `Knowledge/Sources/BibTeX/SRC-XXXXXX.bib`  
**Erzeugt in:** Schritt 2 des Literatur-Workflows

```yaml
id: SRC-000001
dedup_key: andreoni_1990
authors: Andreoni, J.
year: '1990'
title: Impure Altruism and Donations to Public Goods
journal: The Economic Journal
doi: __PLACEHOLDER__
url: __PLACEHOLDER__
review: REVIEW-000001
status: stub
```

**Dedup-Schlüssel:** `{nachname_lower}_{jahr}` — verhindert doppelte Quellen über mehrere Reviews hinweg.

### EVID — Evidenz-Objekt

**Datei:** `Knowledge/Evidence/EVID-XXXXXX.md`  
**Erzeugt in:** Schritt 2 des Literatur-Workflows

```yaml
id: EVID-000001
review: REVIEW-000001
type: positive
sources: [SRC-000001, SRC-000002]
status: candidate
extraction_confidence: high
finding: Donors respond to warm glow independently of public good provision.
direction: positive
strength: strong
concepts: [Warm_Glow_Giving, Impure_Altruism]
limitations: Laboratory setting; WEIRD sample.
```

**Confidence-Werte:**

| Wert | Bedeutung |
|---|---|
| `high` | Strukturierter Block + aufgelöste Quellen |
| `medium` | Strukturierter Block oder aufgelöste Quellen |
| `low` | Blob-Fallback oder keine Attribution |

**Typen:** `positive`, `negative`, `mixed`, `neutral`, `report`

### Claim — Wissenschaftliche Aussage

**Datei:** `Knowledge/Claims/<Präfix>-XXXXXX.md`  
**Präfixe:** `WG` (Warm Glow), `TR` (Trust), `BE` (Brand Equity), `CO` (Commitment), `EU` (Epistemic Uncertainty)  
**Erzeugt in:** Schritt 3 des Literatur-Workflows

```yaml
id: WG-000001
original_id: WG-01
review: REVIEW-000001
concept: Warm Glow Giving
confidence: high
layer: Individual
relationship_type: foundational
sources: [SRC-000001, SRC-000002]
status: candidate
```

Claim-Körper (Markdown):

```markdown
## Statement

Donors derive utility from the act of giving itself, independently of the
outcome for the public good.

## Evidence

Andreoni (1990) demonstrates incomplete crowd-out consistent with impure
altruism. ...

## Implications for BEBA

Warm glow is separable from impact attribution, which decouples donation
motivation from organisational effectiveness signals.
```

**Status-Werte:** `candidate` → `active` → `archived` (manuell)

**Confidence-Werte:** `high`, `medium`, `low` (nach CLAIM_EXTRACTION_PROTOCOL v2)

### Concept

**Datei:** `Knowledge/Concepts/<slug>.md`  
Compact-Einträge für Konzepte, die noch nicht im vollen Workspace entwickelt sind.

### Theory Integration

**Datei:** `Knowledge/Theory_Integration/<Konzept>.md`  
**Erzeugt in:** Schritt 4  
Synthetisiert Claims zu einem konzeptbezogenen Theorieintegrationsdokument.

```yaml
concept: Warm_Glow_Giving
review: REVIEW-000001
claim_count: 15
claim_ids: [WG-000001, ..., WG-000015]
status: candidate
```

### Ontology Candidate

**Datei:** `Knowledge/Ontology_Candidates/<Konzept>.md`  
**Erzeugt in:** Schritt 5  
Abgeleitet aus der Theory Integration. Wird nach manuellem Review Teil der kanonischen Ontologie.

```yaml
concept: Warm_Glow_Giving
review: REVIEW-000001
theory_source: Theory_Integration/Warm_Glow_Giving.md
status: candidate
```

### Manifest

**Datei:** `~/research/literature/processing/<stem>.yaml`  
**Erzeugt in:** Schritt 7  
Prozessprotokoll für einen Review-Lauf.

```yaml
id: REVIEW-000001
source_file: ...
started: '2026-07-05T16:13:13+00:00'
finished: '2026-07-05T16:45:20+00:00'
status: complete
source_ids: [...]
evidence_ids: [...]
claim_ids: [...]
theory_integration: ...
ontology_candidate: ...
todos: [...]
warnings: [...]
```

### INDEX.yaml

**Datei:** `Knowledge/INDEX.yaml`  
Zentraler Navigationsindex aller Objekte.

```yaml
sequences:
  review: 5
  evidence: 118
  src: 46
claim_sequences:
  WG: 31
  TR: 5
  BE: 3
reviews:
  REVIEW-000001:
    stem: LoitRev_Warm_Glow_Giving
    added: '2026-07-05T16:13:13+00:00'
sources:
  SRC-000001:
    dedup_key: andreoni_1990
    bibtex_key: Andreoni1990_SRC-000001
    reviews: [REVIEW-000001]
evidence:
  EVID-000001:
    review: REVIEW-000001
    type: positive
claims:
  WG-000001:
    review: REVIEW-000001
    concept: Warm Glow Giving
```

Der INDEX wird von `beba reset` auf Nullwerte zurückgesetzt.
