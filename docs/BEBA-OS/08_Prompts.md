# Prompts

## Prompt-Loader

Implementiert in: `beba/prompt_loader.py` (nicht ändern)

Der Prompt-Loader lädt für einen gegebenen Task das zugehörige Protokoll-Dokument und kombiniert es mit dem Inhalt der Eingabedatei zu einem vollständigen Prompt.

```python
load_prompt(task, source_path)
# → task-Protokoll + Inhalt von source_path
```

## Protokolldateien

Protokolldateien liegen in:

```
~/research/monography/prompts/literature/
```

Aktuelle Protokolle:

| Datei | Verwendung |
|---|---|
| `CLAIM_EXTRACTION_PROTOCOL.md` | Task `claims` — Claim-Extraktion |
| `EVIDENCE_EXTRACTION_PROTOCOL.md` | Task `evidence` — Evidenz- und Quellenextraktion |

## CLAIM_EXTRACTION_PROTOCOL v2

Das Protokoll schreibt ein striktes Ausgabeformat vor:

```markdown
## CLAIMS

### CLAIM
id_hint: WG-01
concept: Warm_Glow_Giving
statement: <eine präzise, falsifizierbare Aussage>
confidence: high | medium | low
layer: Individual | Organisational | Market | Societal
relationship_type: supports | challenges | qualifies | extends | foundational
evidence_ids:
source_ids: <Referenzstrings aus dem Material>
status: candidate
implications_for_BEBA: <ein Satz zur Relevanz für BEBA>
notes: <optional>
```

**Wichtig:** Ohne `## CLAIMS` / `### CLAIM`-Marker fällt der Parser auf die Legacy- oder heuristische Methode zurück (Qualitätsabfall).

## EVIDENCE_EXTRACTION_PROTOCOL v2

```markdown
## SOURCES

### SOURCE
reference_string: Andreoni, 1990
authors: Andreoni, J.
year: 1990
title: ...
journal: ...

## EVIDENCE_ITEMS

### EVIDENCE
finding: <Kernbefund>
direction: positive | negative | mixed | neutral
strength: strong | moderate | weak
concepts: [Warm_Glow_Giving, ...]
sources: Andreoni, 1990; ...
limitations: ...
notes: ...
```

## Protokolle aktualisieren

Protokolldateien können direkt bearbeitet werden. Sie beeinflussen die Qualität der KI-Ausgaben erheblich.

**Richtlinien:**

- Immer ein Ausgabeformat mit konkretem Beispiel angeben
- Marker (`## CLAIMS`, `### CLAIM`) explizit benennen
- Felder vollständig definieren
- Verbotene Verhaltensweisen explizit ausschließen (z.B. „Do not invent claims")

## Prompt-Größen und Kosten

Die Synthesedatei (`literature/synthesized/<stem>.md`) ist die primäre Eingabe für Steps 2–5. Bei langen Reviews kann diese mehrere Tausend Tokens umfassen, was die Kosten pro Review wesentlich bestimmt.

Tokengrößen werden in der Telemetrie geschätzt (ca. 4 Zeichen pro Token).
