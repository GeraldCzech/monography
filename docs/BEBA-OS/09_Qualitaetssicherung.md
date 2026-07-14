# Qualitätssicherung

## Validator

Implementiert in: `beba/validator.py`

`validate_knowledge_base(knowledge_path)` prüft die gesamte Wissensbasis auf strukturelle Integrität.

### Was geprüft wird

| Prüfung | Beschreibung |
|---|---|
| `broken_evidence_refs` | EVID-Objekte referenzieren REVIEW-IDs, die nicht existieren |
| `broken_review_refs` | REVIEW-Objekte referenzieren SRC-IDs, die nicht in `Sources/` liegen |
| `duplicate_bibtex_keys` | Mehrere BibTeX-Einträge mit identischem Key in `master.bib` |
| `invalid_yaml_files` | YAML-Frontmatter in Objekt-Dateien kann nicht geparst werden |
| `missing_required_fields` | Pflichtfelder fehlen in Frontmatter |
| `duplicate_ids` | Mehrere Dateien mit derselben ID |

### Datei-Filterung

Der Validator ignoriert Nicht-Objekt-Dateien im Claims-Verzeichnis (wie `README.md`, `initial-claims.md`, Blob-Dateien). Nur Dateien, die dem Muster `^[A-Z]{2,3}-\d{6}\.md$` entsprechen, werden validiert.

### Rückgabe

```python
@dataclass
class ValidationReport:
    broken_evidence_refs: list[str]
    broken_review_refs: list[str]
    duplicate_bibtex_keys: list[str]
    invalid_yaml_files: list[str]
    missing_required_fields: list[str]
    duplicate_ids: list[str]
    
    def total_violations(self) -> int: ...
    def is_clean(self) -> bool: ...
```

## Regression

Implementiert in: `beba/regression.py`

`beba regression` führt strukturelle Tests gegen eine Baseline durch.

### Baseline

**Datei:** `tests/warm_glow/expected.yaml`

```yaml
review_stem: LoitRev_Warm_Glow_Giving
input_file: ~/research/literature/markdown/LoitRev_Warm_Glow_Giving.md
concept: Warm_Glow_Giving
min_sources: 5
min_evidence: 5
min_claims: 5
required_evidence_fields:
  - id
  - review
  - type
  - status
  - extraction_confidence
required_source_fields:
  - id
  - authors
  - year
  - status
required_claim_fields:
  - id
  - concept
  - status
required_review_fields:
  - id
  - status
```

### Scope-Verhalten

Standardmäßig wird nur der **letzte Review** geprüft (neueste REVIEW-ID in den Manifesten). Legacy-Objekte aus früheren Läufen verursachen keine Fehlschläge.

```bash
beba regression                          # letzter Review
beba regression --review REVIEW-000003  # spezifischer Review
beba regression --validate-only         # ohne Workflow-Neuausführung
```

### Zero-Claims-Check

Ein abgeschlossener Review ohne Claims gilt als Extraktionsfehler. Der Test schlägt fehl, wenn:

- das Manifest `status: complete` hat
- `claim_ids` leer ist
- das Manifest kein `claims_unavailable: true` enthält

### Ausgabe

```
BEBA Regression Suite — Warm Glow Giving
  Baseline: tests/warm_glow/expected.yaml
  Scope: REVIEW-000005 (latest)

  Warnings (1):
    - Scoped to REVIEW-000005 (latest)

  PASS  All structural checks passed.
```

## Projekt-Reset

`beba reset --yes` entfernt alle generierten Objekte und stellt die leere Verzeichnisstruktur wieder her.

Vor der Löschung wird ein Backup in `monography/02_Theory/archive/<timestamp>/knowledge_base.tar.gz` angelegt.

```bash
beba reset              # Dry-run (zeigt, was gelöscht würde)
beba reset --yes        # Führt Reset durch
beba reset --yes --no-backup  # Ohne Backup (nicht empfohlen)
```

## YAML-Integrität

Alle Objekt-Dateien verwenden YAML-Frontmatter zwischen `---`-Trennern. Ungültiges YAML wird vom Validator erkannt.

Pflichtfelder pro Objekttyp:

| Typ | Pflichtfelder |
|---|---|
| REVIEW | `id`, `status` |
| SRC | `id`, `authors`, `year`, `status` |
| EVID | `id`, `review`, `type`, `status` |
| Claim | `id`, `concept`, `status` |
