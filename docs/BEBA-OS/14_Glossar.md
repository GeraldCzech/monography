# Glossar

Kanonische Begriffe für BEBA-OS. Abweichende Verwendung in anderen Dokumenten ist nicht zulässig.

Für wissenschaftliche Konstrukte: `glossary.md` im Repository-Wurzelverzeichnis.

---

## Systemkonzepte

**BEBA-OS**  
Brand-Enabled Behaviour Architecture Operating System. Die Gesamtheit der Werkzeuge, Repositorien und Konventionen, die Gerards Forschungsinfrastruktur bilden.

**Knowledge Base**  
Die Sammlung aller Knowledge-Objekte in `02_Theory/Knowledge/`. Nicht identisch mit dem gesamten monography-Repository.

**Knowledge Object**  
Eine strukturierte Markdown-Datei mit YAML-Frontmatter, die einen wissenschaftlichen Baustein repräsentiert (REVIEW, SRC, EVID, Claim, Concept, Theory Integration, Ontology Candidate).

**Manifest**  
YAML-Datei in `literature/processing/<stem>.yaml`, die einen abgeschlossenen Workflow-Lauf protokolliert. Enthält IDs aller erzeugten Objekte, TODOs, Warnungen.

**INDEX.yaml**  
Zentrale Navigationsdatei in `Knowledge/INDEX.yaml`. Enthält Sequenzwerte (nächste ID), alle bekannten Objekt-IDs mit Metadaten.

**Stem**  
Dateiname ohne Erweiterung einer Eingabe-Markdown-Datei. Beispiel: `LoitRev_Warm_Glow_Giving`. Wird als Schlüssel in Manifesten und INDEX verwendet.

**Dedup-Key**  
`{nachname_lower}_{jahr}` — eindeutiger Schlüssel zur Deduplizierung von Quellen. Beispiel: `andreoni_1990`.

---

## Pipeline-Begriffe

**Structured Parser (Tier 1)**  
Parser für `## SOURCES / ### SOURCE` und `## EVIDENCE_ITEMS / ### EVIDENCE` bzw. `## CLAIMS / ### CLAIM`. Bevorzugtes Verfahren.

**Legacy Parser (Tier 2)**  
Parser für ältere LLM-Ausgabeformate (Abschnitte „Key References", „Positive Evidence" oder `---`-getrennte `## Claim ID`-Blöcke).

**Heuristic Parser (Tier 3)**  
Fallback-Parser für Überschriften-basierte oder `**Fett**`-Schlüssel-Formate.

**Blob**  
Nicht-strukturierter Fallback: Der gesamte LLM-Output wird als einzelne Datei gespeichert. Erkennbar an `extraction_confidence: low` oder `type: report`.

**Extraction Confidence**  
Qualitätskennzahl für EVID-Objekte: `high`, `medium`, `low`.

**Claims Unavailable**  
Manifest-Flag `claims_unavailable: true` — zeigt an, dass ein Review ohne Claims abgeschlossen wurde und dieser Zustand beabsichtigt ist. Verhindert Regression-Fehler.

---

## Claim-Präfixe

| Präfix | Konzept |
|---|---|
| `WG` | Warm_Glow_Giving |
| `TR` | Trust |
| `BE` | Brand_Equity |
| `CO` | Commitment |
| `EU` | Epistemic_Uncertainty |

Unbekannte Konzepte: Initialen der ersten zwei Wörter.

---

## CLI-Befehle

| Befehl | Funktion |
|---|---|
| `beba literature <datei>` | Einzelne Datei durch den 7-Schritte-Workflow |
| `beba ingest` | Inbox-Verzeichnis scannen und verarbeiten |
| `beba regression` | Strukturelle Tests gegen Baseline |
| `beba reset --yes` | Generierte Objekte löschen, Backup erstellen |
| `beba telemetry` | Telemetrie-Dashboard anzeigen |
| `beba telemetry export` | Rohlogdaten als CSV oder JSON exportieren |
| `beba status` | Workspace-Pfade anzeigen |
| `beba check-config` | API-Key-Status prüfen |

---

## Wissenschaftliche Konzepte (Kurzreferenz)

Eine vollständige Begriffsliste findet sich in `glossary.md`.

**BEBA**  
Brand-Enabled Behaviour Architecture. Mehrstufige Architektur, die Signale, Brand Equity, Überzeugungsbildung, Intention und Ressourcenverhalten verbindet.

**Impure Altruism**  
Philanthropisches Verhalten, das durch eine Mischung aus altruistischen und egozentrierten Motiven getrieben wird (Andreoni 1989, 1990).

**Warm Glow**  
Nutzenzuwachs durch die Handlung des Gebens selbst, unabhängig vom Ergebnis für das öffentliche Gut.

**Epistemic Uncertainty**  
Unsicherheit über Qualität, Integrität, Wirkung und zukünftiges Verhalten einer Organisation — das Grundproblem des Donationsmarkts.

**Credence Goods**  
Güter oder Dienstleistungen, deren Qualität auch nach dem Konsum schwer zu beurteilen ist. Zentrales Analogon für philanthropische Entscheidungen.

**Signalling Theory**  
Theoretischer Rahmen, der erklärt, wie beobachtbare Signale nicht beobachtbare Eigenschaften kommunizieren (Spence 1973).

**TPB / IBM**  
Theory of Planned Behaviour / Integrated Behavioural Model. Erklärungsrahmen für Intentionsbildung und Verhaltensausführung.
