# Architecture Decision Records

ADRs dokumentieren **wesentliche Architekturentscheidungen** — warum etwas so gebaut wurde, welche Alternativen erwogen wurden und welche Konsequenzen die Entscheidung hat.

Ablage: `10_ADRs/` im `monography`-Repository.

---

## ADR-0001: Repository als einzige Wahrheitsquelle

**Status:** Accepted

**Entscheidung:**  
Das GitHub-Repository `GeraldCzech/monography` ist die einzige Quelle der Wahrheit für Theorie, Kapitel, Glossar, Construct Ledger, Research Compass, Decision Logs und Publikationsstrategie.

KI-Modelle sind austauschbare Linsen auf dieses Repository. Inhalte werden erst Teil des Forschungsprogramms, wenn sie hier committed sind.

**Konsequenzen:**
- Kein Content in Chatverläufen, Word-Dokumenten oder lokalen Textdateien außerhalb des Repos
- Jede Theorieentscheidung braucht einen Commit
- KI-Agenten schreiben in das Repository, nicht in externe Dokumente

---

## ADR-0002: Separate empirische Pipeline

**Status:** Accepted

**Entscheidung:**  
CFA/SEM-Code, targets-Pipeline, DuckDB-Datenbank und empirische Reports liegen in `GeraldCzech/BrandEquityPipeline` — getrennt von `monography`.

**Begründung:**
- Empirische Daten und Rohdaten liegen nicht in GitHub
- Analysecode ändert sich häufig; Theoriecode ändert sich langsam
- Klare Trennung verhindert unbeabsichtigte Kopplung

**Konsequenzen:**
- Empirische Werte werden von `monography` referenziert, nicht kopiert
- Kein R-Code in `monography`

---

## Architekturentscheidungen in BEBA-Tools

Die folgenden Entscheidungen wurden im Entwicklungsprozess von BEBA-Tools getroffen und sind hier dokumentiert, auch wenn kein formales ADR-Dokument dafür existiert.

### JSONL + YAML statt Datenbank

Alle generierten Objekte und Logs werden als Plaintext-Dateien gespeichert. Keine SQL-Datenbank, kein ORM.

**Begründung:** Git-Versionierung funktioniert optimal mit Textdateien. Keine externe Abhängigkeit. Ausreichend für aktuelle Skalierung (hunderte, nicht Millionen von Objekten).

### Dreistufige Parser mit Fallback

Evidence-, Claims- und Sources-Parser versuchen strukturierte Protokollausgaben zuerst und fallen auf Legacy-Formate und heuristische Methoden zurück.

**Begründung:** LLM-Ausgaben sind nicht vollständig deterministisch. Robustheit durch Degradation statt Abbruch. Qualitätsverlust wird über `extraction_confidence` signalisiert.

### Claim-IDs sind konzeptbasiert

Claim-IDs tragen konzeptbasierte Präfixe (`WG-000001` statt `C-000001`).

**Begründung:** Dateinamen sollen ohne Öffnen der Datei Auskunft über den Inhalt geben. Konzeptpräfixe ermöglichen semantische Navigation.

### Telemetrie ist passiv

Der Observability-Layer beeinflusst die Workflow-Ausführung nicht. Alle Telemetriemethoden swallown Exceptions.

**Begründung:** Kostenmessung und Debugging-Unterstützung dürfen nie eine Ursache für Workflow-Fehler sein.

### Kein automatischer Commit

BEBA-Tools committet nie automatisch.

**Begründung:** Manuelles Review aller generierten Objekte ist Pflicht. Automatische Commits würden unüberprüfte KI-Ausgaben in die Forschungswahrheit einschreiben.

---

## Neue ADRs erstellen

Neue ADRs werden in `10_ADRs/` als `ADR-NNNN-<kurztitel>.md` abgelegt.

Pflichtfelder: **Status**, **Entscheidung**, **Begründung**, **Konsequenzen**.

Mögliche Status: `Proposed`, `Accepted`, `Deprecated`, `Superseded by ADR-XXXX`.
