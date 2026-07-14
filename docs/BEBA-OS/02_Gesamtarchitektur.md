# Gesamtarchitektur

## Die drei Repositorien

BEBA-OS besteht aus drei voneinander getrennten Repositorien mit klar abgegrenzten Verantwortlichkeiten.

### monography

**Pfad:** `~/research/monography`  
**Zweck:** Theorie, Kapitel, Wissensbasis, Glossar, ADRs, Publikationsstrategie

Enthält:
- Theoretische Architektur (BEBA-Schichten, Konstrukte, Modelle)
- Kapitelentwürfe
- Knowledge-Objekte (`02_Theory/Knowledge/`)
- Knowledge-Architektur-Dokumentation
- Glossar und Construct Ledger
- Architecture Decision Records
- Publikationsstrategie

Enthält **nicht**:
- Rohdaten
- R-Code
- CFA/SEM-Ausgaben
- operative Analysepipeline

### BrandEquityPipeline

**Pfad:** `~/research/GeraldCzech/BrandEquityPipeline` (separat)  
**Zweck:** Empirische Analysepipeline

Enthält:
- R-Code für CFA und SEM
- `targets`-Pipeline
- DuckDB-Schnittstellen
- Quarto-Reports
- Empirische Ergebnisse

Verbindung zu `monography`: Ergebnisse werden referenziert, nicht kopiert.

### BEBA-Tools

**Pfad:** `~/research/BEBA-Tools`  
**Zweck:** KI-gestützte Literaturverarbeitung und Knowledge-Objekt-Erzeugung

Enthält:
- Python-CLI `beba`
- Literatur-Workflow (7 Schritte)
- Ingestion-Pipeline
- Validator und Regression
- Telemetrie-Layer
- Pricing-Konfiguration

## Abgrenzung in der Praxis

| Aufgabe | Ort |
|---|---|
| Kapitelentwurf schreiben | `monography` |
| Neue Theorie entwickeln | `monography` |
| Literatur verarbeiten | `BEBA-Tools` |
| SEM-Modell schätzen | `BrandEquityPipeline` |
| Knowledge-Objekte erzeugen | `BEBA-Tools` → `monography` |
| Empirische Werte referenzieren | `BrandEquityPipeline` → `monography` |
| Prompt aktualisieren | `monography/prompts/literature/` |

## Datenfluss

```
~/research/literature/inbox/
      |
      | beba ingest
      v
~/research/literature/markdown/
      |
      | beba literature
      v
~/research/literature/synthesized/     (Step 1: Synthese)
      |
      | Steps 2–7: Evidence, Claims, Theory, Ontology, Review, Index
      v
~/research/monography/02_Theory/Knowledge/
      |
      | Manuelles Review + Commit
      v
Kanonische Wissensbasis
```

## Claude Code und Agenten-Rollen

Im `monography`-Repository sind spezifische Agentenrollen definiert (`.claude/agents/`):

| Agent | Aufgabe |
|---|---|
| `knowledge-engineer` | Literatur in Wissensobjekte transformieren |
| `literature-analyst` | Evidenzextraktion und Literaturanalyse |
| `methodology-sem` | Methodologische Fragen zu SEM und Psychometrie |
| `reviewer-simulator` | Gutachtersimulation für Paper-Review |
| `scientific-editor` | Sprachliche und strukturelle Überarbeitung |
| `theory-architect` | Theoretische Architekturentscheidungen |
