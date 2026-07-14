# Literaturpipeline

## Überblick

Der Literatur-Workflow verarbeitet eine Markdown-Datei in 7 aufeinanderfolgenden Schritten und erzeugt strukturierte Knowledge-Objekte.

```
beba literature <datei.md> [--concept Warm_Glow_Giving] [--force]
```

Implementiert in: `beba/literature_workflow.py` → `run_literature_workflow()`

## Die 7 Schritte

### Schritt 1: Literatursynthese

**Input:** Rohe Literaturreview-Markdown  
**Output:** `literature/synthesized/<stem>.md`  
**Provider-Task:** `literature`

Der KI-Provider synthetisiert die Rohliteratur zu einer strukturierten Zusammenfassung. Diese Synthese dient als Eingabe für alle weiteren Schritte.

Wird übersprungen, wenn die Ausgabedatei bereits existiert (es sei denn, `--force`).

### Schritt 2: Evidenz und Quellen

**Input:** `literature/synthesized/<stem>.md`  
**Output:** `Knowledge/Sources/SRC-XXXXXX.md`, `BibTeX/SRC-XXXXXX.bib`, `Knowledge/Evidence/EVID-XXXXXX.md`  
**Provider-Task:** `evidence`

Dreistufige Verarbeitung:

**Quellen-Parser (Tier-1 → Tier-2 → Tier-3):**

1. Strukturierter `## SOURCES` / `### SOURCE`-Block (v2-Protokoll)
2. Legacy Key-References-Parser
3. Inline-Zitationen als letzter Fallback

**Evidenz-Parser:**

1. Strukturierter `## EVIDENCE_ITEMS` / `### EVIDENCE`-Block
2. Legacy Positiv/Gemischt/Negativ-Parser

Jedes EVID-Objekt erhält ein `extraction_confidence`-Feld (`high`, `medium`, `low`).

**Quellen-Dedup:** Bestehende Quellen werden über `{nachname_lower}_{jahr}` erkannt und nicht doppelt angelegt.

### Schritt 3: Claim-Objekte

**Input:** `literature/synthesized/<stem>.md`  
**Output:** `Knowledge/Claims/<Präfix>-XXXXXX.md`  
**Provider-Task:** `claims`

Dreistufige Verarbeitung:

1. Strukturierter `## CLAIMS` / `### CLAIM`-Block (v2-Protokoll, bevorzugt)
2. Legacy `---`-Separator-Format mit `## Claim ID`-Überschriften
3. Heuristischer Parser: Überschriftenbasiert oder `**Fettdruck**`-Schlüssel

**Normalisierung:** Claims werden über `normalize_claims()` dedupliziert (Schlüssel: normalisierter Statement-Text). Duplikate werden zusammengeführt, der höhere Confidence-Wert wird beibehalten.

**ID-Vergabe:** Stable IDs werden konzeptbasiert vergeben:

| Konzept | Präfix | Beispiel |
|---|---|---|
| Warm_Glow_Giving | WG | WG-000001 |
| Trust | TR | TR-000001 |
| Brand_Equity | BE | BE-000001 |
| Commitment | CO | CO-000001 |
| Epistemic_Uncertainty | EU | EU-000001 |

Fallback: Initialen der ersten zwei Wörter des Konzepts.

**Blob-Fallback:** Wenn kein Parser Claims extrahiert, wird eine Blob-Datei `REVIEW-XXXXXX-claims.md` angelegt und ein TODO ins Manifest eingetragen.

### Schritt 4: Theorieintegration

**Input:** Claim-Objekte des aktuellen Reviews  
**Output:** `Knowledge/Theory_Integration/<Konzept>.md`  
**Provider-Task:** `theory`

KI synthetisiert Claims zu einem konzeptbezogenen Theorieintegrationsdokument. Wird übersprungen, wenn die Datei bereits existiert (TODO wird eingetragen).

### Schritt 5: Ontologie-Kandidat

**Input:** `Knowledge/Theory_Integration/<Konzept>.md`  
**Output:** `Knowledge/Ontology_Candidates/<Konzept>.md`  
**Provider-Task:** `ontology`

Abgeleitet aus der Theory Integration. Bleibt Kandidat bis zum manuellen Review.

### Schritt 6: Review-Objekt

**Output:** `Knowledge/Reviews/REVIEW-XXXXXX.md`

Protokollobjekt mit Zeitstempeln, Objekt-IDs, Status und primärem Konzept.

### Schritt 7: Index, Bibliographie, Manifest

**Outputs:**
- `Knowledge/INDEX.yaml` (aktualisiert)
- `Knowledge/Bibliography/master.bib` (neu aufgebaut)
- `literature/processing/<stem>.yaml` (Manifest)

`master.bib` wird bei jedem Lauf vollständig aus allen `BibTeX/SRC-*.bib`-Stubs neu aufgebaut.

## Idempotenz

Alle Schritte prüfen, ob Ausgabedateien bereits existieren. Existierende Dateien werden übersprungen (mit Ausgabe `skip`). `--force` erzwingt Neuschreibung.

## Pipeline Quality Summary

Am Ende jedes Laufs wird eine Qualitätszusammenfassung ausgegeben:

```
Sources:           12
Evidence:          28
Claims:            15
Duplicate claims:   2
Broken refs:        0
Invalid YAML:       0
Unresolved srcs:    3
Warnings:           1
Validation:        PASS
```

## Telemetrie

Für jeden API-Aufruf wird automatisch ein Telemetrie-Datensatz geschrieben (siehe Kapitel Observability). Fehler in der Telemetrie beeinflussen die Pipeline nicht.
