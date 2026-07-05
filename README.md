# BEBA Monography

Zentrale Forschungs- und Schreibumgebung fuer die Monographie zur Dissertation **Nonprofit Brand Equity as a Brand-Enabled Behaviour Architecture (BEBA)**.

## Leitprinzip

**Git ist die Forschungswahrheit.** Alles, was Theorie, Kapitel, Begriffe, Forschungsentscheidungen oder Publikationsstrategie betrifft, wird hier versioniert. KI-Modelle sind austauschbare Linsen auf diese Wissensbasis.

## Abgrenzung

- `GeraldCzech/BrandEquityPipeline` enthaelt Analyse-Code, CFA/SEM, targets, DuckDB-Schnittstellen und empirische Pipeline-Dokumentation.
- Dieses Repository enthaelt Theorie, Monographie, Kapitelstruktur, Ontologie, Research Compass, ADRs, Decision Logs und Publikationsstrategie.
- Rohdaten liegen nicht in GitHub.

## Kernstruktur

```text
01_Project/              Vision, Scope, Timeline
02_Theory/               Theoretische Architektur, BEBA und Wissensbasis
03_Methodology/          Methodologische Grundlagen
04_Empirical_Link/       Bruecke zur Analysepipeline
05_Chapters/             Monographie-Kapitel
06_Papers/               Artikelspinoffs
07_Reviews/              Literaturreview-Notizen und Consensus-Exports
08_Figures/              Mermaid, Diagramme, Abbildungen
09_ResearchCompass/      Kapitelbezogene Forschungslandkarten
10_ADRs/                 Architecture Decision Records
11_DecisionLog/          Laufende wissenschaftliche Entscheidungen
12_PublicationStrategy/  Publikationsstrategie
99_Archive/              Ueberholte Fassungen
```

## Knowledge Architecture

Das Repository wurde um eine BEBA Knowledge Architecture erweitert.

```text
02_Theory/Knowledge_Architecture/
  BEBA_INFORMATION_MODEL_v1.md
  BEBA_ONTOLOGY_GUIDE_v1.md
  BEBA_RELATIONSHIP_MODEL_v1.md
  BEBA_KNOWLEDGE_ENGINEERING_GUIDE_v1.md

02_Theory/Knowledge/
  Concepts/
  Claims/
  Evidence/
  Theory_Integration/
  Ontology_Candidates/
  Relationships/
```

Die zentrale Logik lautet:

```text
Evidence -> Claims -> Concepts -> Theories -> Models -> Chapters / Papers
```

Kapitel und Paper sind Outputs der Wissensbasis, nicht deren Ursprung.

## Status

BEBA-ROS Lite v1.1 - Knowledge Architecture initialisiert.
