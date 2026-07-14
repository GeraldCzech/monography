# Ingestion

## Zweck

`beba ingest` ist der Eintrittspunkt für neue Literatur. Der Befehl scannt das Inbox-Verzeichnis und verarbeitet Dateien automatisch durch den Literatur-Workflow.

Implementiert in: `beba/ingest_workflow.py`

## Verzeichnisstruktur

```
~/research/literature/
├── inbox/                ← Neue Dateien hier ablegen
│   ├── processed/        ← Originaldatei nach Erfolg
│   └── failed/           ← Originaldatei nach Fehler
├── raw/                  ← Kopie aller DOCX-Dateien
├── markdown/             ← Konvertierte/kopierte MD-Dateien
├── synthesized/
└── processing/
```

Alle Verzeichnisse werden automatisch beim ersten Aufruf angelegt.

## Befehl

```bash
beba ingest [OPTIONS]
```

### Optionen

| Option | Beschreibung |
|---|---|
| `--dry-run` | Zeigt, was passieren würde — ohne Änderungen |
| `--force` | Verarbeitet auch bereits vorhandene Dateien neu |
| `--concept TEXT` | Konzept-Slug für alle Dateien dieses Laufs |
| `--limit N` | Nur N Dateien verarbeiten |

## Verarbeitungsreihenfolge

Dateien werden **alphabetisch** verarbeitet. Bei `--limit 1` wird genau eine Datei verarbeitet.

## DOCX-Dateien

1. Originaldatei wird nach `raw/` kopiert
2. Konvertierung nach `markdown/<stem>.md` via `pandoc`
3. Wenn Markdown bereits existiert und `--force` nicht gesetzt: Konvertierung übersprungen
4. `beba literature` auf der Markdown-Datei ausführen
5. Erfolg → Original nach `inbox/processed/`
6. Fehler → Original nach `inbox/failed/`

## MD-Dateien

1. Datei wird nach `markdown/` kopiert
2. `beba literature` auf der kopierten Datei ausführen
3. Erfolg → Original nach `inbox/processed/`
4. Fehler → Original nach `inbox/failed/`

## Sicherheitsregeln

- Originaldateien werden **niemals gelöscht** — nur verschoben
- `processed/` und `failed/` überschreiben keine vorhandenen Dateien: Zeitstempel wird angehängt (`_20260705T185000Z`)
- Fehler bei einer Datei unterbrechen den Lauf nicht — die nächste Datei wird verarbeitet
- `--dry-run` löst keine API-Aufrufe aus

## Empfohlener Workflow

```bash
# 1. Datei ins Inbox-Verzeichnis legen
cp ~/Downloads/LoitRev_WarmGlow.docx ~/research/literature/inbox/

# 2. Dry-Run prüfen
beba ingest --dry-run --concept Warm_Glow_Giving

# 3. Verarbeiten
beba ingest --concept Warm_Glow_Giving --limit 1

# 4. Ergebnis prüfen
beba regression --validate-only
```

## Zusammenfassung am Ende

Nach dem Lauf wird ausgegeben:

```
Summary:  3 succeeded  1 failed  0 skipped  (total 4)
Failed files archived in: ~/research/literature/inbox/failed
```

Bei Fehlern wird Exit-Code 1 zurückgegeben.
