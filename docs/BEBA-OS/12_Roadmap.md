# Roadmap

## Umgesetzt

### Literatur-Pipeline (7 Schritte)

Vollständig implementiert. Läuft stabil für Warm-Glow-Giving-Reviews.

- Mehrsprachige Provider mit Fallback
- Dreistufige Parser für Evidence, Sources und Claims
- Claim-Normalisierung und Deduplizierung
- Konzeptbasierte Claim-IDs

### Ingestion-Pipeline

`beba ingest` für .docx und .md, mit dry-run, force, concept, limit.

### Validator

Strukturelle Prüfung der Wissensbasis auf broken references, duplicate keys, invalid YAML.

### Regression

Review-scoped strukturelle Tests gegen expected.yaml.

### Reset

Sicheres Zurücksetzen mit Backup-Archiv.

### Observability

Telemetrie-Layer für alle API-Aufrufe:
- Rohes JSONL pro Aufruf
- Workflow-YAML pro Review
- Aggregierte Statistiken (Provider, Modell, Workflow, Prompts)
- `beba telemetry` Dashboard
- `beba telemetry export` (CSV, JSON)

Tokenanzahlen werden geschätzt (~4 Zeichen pro Token), da Provider-APIs keine Tokenzahlen durch den Dispatcher exponieren.

---

## Geplant

Die folgenden Funktionen sind konzeptionell vorgesehen, aber **nicht implementiert**.

### Bayesian Evidence Engine *(geplant)*

**Idee:** Ein probabilistisches Modell, das Claim-Confidence dynamisch aus akkumulierter Evidenz über mehrere Reviews hinweg aktualisiert.

**Mechanismus (Konzept):**
- Prior: initiale Confidence aus Claim-Extraktion
- Update: eingehende EVID-Objekte mit direction und strength
- Posterior: aktualisierter Confidence-Wert und Konsistenz-Score

**Voraussetzungen:**
- Stabile EVID-CLAIM-Verlinkung (noch nicht implementiert)
- Kanonisches Evidenzstärken-Schema
- Entscheidung über Prior-Verteilung

**Status:** Designnotiz. Keine Implementierung ohne explizite Anfrage.

### EVID → CLAIM Verlinkung *(geplant)*

`evidence_ids` im Claim-Frontmatter wird aktuell leer gelassen. Automatisches Matching von Evidenzobjekten zu Claims auf Basis von Konzept und Quellen ist konzeptionell vorgesehen.

### DOI-Anreicherung *(geplant)*

Automatische Abfrage von CrossRef oder OpenAlex für Platzhalter in SRC-Objekten.

**Nicht implementiert:** Externe API-Aufrufe außerhalb des KI-Workflows werden bewusst nicht automatisiert (Kontrollprinzip).

### Multi-Review Concept Workspace *(geplant)*

Vollständiger Concept-Workspace mit `claims.md`, `evidence.md`, `definitions.md`, `boundary_conditions.md`, `measurement.md`, `relationships.md`. Aktuell werden Concepts als kompakte Einzeldateien verwaltet.

### Interaktives Dashboard *(geplant)*

Web-basiertes Telemetrie-Dashboard (z.B. als Quarto-Report) mit Zeitreihen und Kostenverläufen.

### Claim-Versionierung *(geplant)*

Automatische Archivierung überholter Claim-Versionen bei Review-übergreifendem Update.

---

## Bewusst nicht implementiert

| Funktion | Begründung |
|---|---|
| Datenbanken (SQL, DuckDB) | Git + YAML reicht für die aktuelle Skalierung |
| Background-Watcher (cron, systemd) | Manuelle Kontrolle über Verarbeitungszeitpunkt |
| Automatische Commits | Manuelles Review ist Pflicht |
| LangGraph / Agenten-Frameworks | Keine externe Abhängigkeit für Kernfunktionen |
| Automatische DOI-Enrichment | Externe APIs nicht im Kernpfad |
