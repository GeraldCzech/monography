# Verzeichnisstruktur

## monography

```
~/research/monography/
├── 01_Project/              Vision, Scope, Timeline
├── 02_Theory/
│   ├── Knowledge_Architecture/
│   │   ├── BEBA_INFORMATION_MODEL_v1.md
│   │   ├── BEBA_KNOWLEDGE_ENGINEERING_GUIDE_v1.md
│   │   ├── BEBA_ONTOLOGY_GUIDE_v1.md
│   │   └── BEBA_RELATIONSHIP_MODEL_v1.md
│   └── Knowledge/
│       ├── INDEX.yaml               ← Zentraler Index aller Objekte
│       ├── README.md
│       ├── Claims/                  ← Claim-Objekte (WG-000001.md, TR-000001.md …)
│       ├── Concepts/                ← Konzept-Dateien
│       ├── Evidence/                ← EVID-Objekte
│       ├── Reviews/                 ← REVIEW-Objekte
│       ├── Sources/
│       │   └── BibTeX/              ← BibTeX-Stubs pro SRC-Objekt
│       ├── Theory_Integration/      ← Theorieintegrations-Outputs
│       ├── Ontology_Candidates/     ← Ontologie-Kandidaten
│       ├── Relationships/           ← Beziehungs-Notizen
│       ├── Bibliography/
│       │   ├── master.bib           ← Akkumulierte BibTeX-Einträge
│       │   └── unresolved_sources.yaml
│       └── Processing/              ← Ältere Verarbeitungs-Manifeste
├── 03_Methodology/
├── 04_Empirical_Link/
├── 05_Chapters/
├── 06_Papers/
├── 07_Reviews/
├── 08_Figures/
├── 09_ResearchCompass/
├── 10_ADRs/
├── 11_DecisionLog/
├── 12_PublicationStrategy/
├── 99_Archive/
├── docs/BEBA-OS/                    ← Dieses Handbuch
├── .claude/
│   ├── agents/                      ← Agentendefinitionen
│   └── commands/                    ← Wiederverwendbare Aufgabenvorlagen
├── 00_MASTER_OUTLINE.md
├── 01_THEORETICAL_MAP.md
├── ConstructLedger.md
├── glossary.md
├── README.md
└── START_HERE.md
```

## literature

```
~/research/literature/
├── inbox/                   ← Eingangsfach für neue Dateien
│   ├── processed/           ← Nach erfolgreicher Verarbeitung
│   └── failed/              ← Nach fehlgeschlagener Verarbeitung
├── raw/                     ← Kopien aller eingehenden DOCX-Dateien
├── markdown/                ← Konvertierte oder direkt eingehende MD-Dateien
├── synthesized/             ← Schritt-1-Ausgaben (Literatursynthese)
├── processing/              ← YAML-Manifeste pro Review
├── logs/
│   ├── api/
│   │   └── api_calls.jsonl  ← Rohe API-Aufrufe
│   ├── workflow/
│   │   └── REVIEW-*.yaml    ← Workflow-Zusammenfassungen
│   └── dashboard/
│       ├── provider_statistics.yaml
│       ├── model_statistics.yaml
│       ├── workflow_statistics.yaml
│       └── prompt_statistics.yaml
├── prompts/                 ← Ältere Prompt-Dateien (Referenz)
├── scripts/                 ← Shell-Skripte
├── notes/
├── evidence/
├── ontology/
└── figures/
```

## BEBA-Tools

```
~/research/BEBA-Tools/
├── beba/
│   ├── __init__.py
│   ├── cli.py                   ← Typer CLI
│   ├── claim_normalizer.py      ← Dedup und Normalisierung
│   ├── config.py                ← Konfigurationsloader
│   ├── dispatcher.py            ← Provider-Routing
│   ├── ingest_workflow.py       ← Ingestion-Pipeline
│   ├── knowledge_index.py       ← INDEX.yaml-Verwaltung
│   ├── literature_parser.py     ← Parsing-Funktionen
│   ├── literature_workflow.py   ← Haupt-Workflow (7 Schritte)
│   ├── paths.py                 ← Pfadkonstanten
│   ├── prompt_loader.py         ← Prompt-Loader
│   ├── providers.py             ← API-Aufrufe
│   ├── regression.py            ← Regressionstests
│   ├── reset.py                 ← Projektbereinigung
│   ├── source_manager.py        ← Source-Objekte und BibTeX
│   ├── telemetry.py             ← Observability-Layer
│   └── validator.py             ← Wissensbasis-Validierung
├── docs/
│   ├── HARDENING_SPRINT_1.md
│   └── INGEST_WORKFLOW.md
├── tests/
│   └── warm_glow/
│       └── expected.yaml
├── pricing.yaml
├── pyproject.toml
└── README.md
```

## Konfiguration

```
~/.config/beba/
├── config.yaml      ← Projektpfade
├── providers.yaml   ← Provider-Routing und Modelle
└── .env             ← API-Keys (nicht in Git)
```

## Prompts

```
~/research/monography/prompts/literature/
├── CLAIM_EXTRACTION_PROTOCOL.md
└── EVIDENCE_EXTRACTION_PROTOCOL.md
```
