# Bibliographie

## Überblick

Die Bibliographieverwaltung in BEBA-OS basiert auf strukturierten Source-Objekten, BibTeX-Stubs und einer akkumulierten Hauptdatei.

Implementiert in: `beba/source_manager.py`

## Source-Objekte

Jede in einem Review zitierte Quelle erhält ein eigenes SRC-Objekt in `Knowledge/Sources/SRC-XXXXXX.md`.

### Felder

| Feld | Beschreibung |
|---|---|
| `id` | Stable ID (SRC-000001) |
| `dedup_key` | `{nachname_lower}_{jahr}` — Deduplizierungsschlüssel |
| `authors` | Autorenliste aus Protokoll |
| `year` | Erscheinungsjahr |
| `title` | Titel (falls extrahiert, sonst `__PLACEHOLDER__`) |
| `journal` | Zeitschrift (falls extrahiert, sonst `__PLACEHOLDER__`) |
| `doi` | DOI (falls vorhanden, sonst `__PLACEHOLDER__`) |
| `url` | URL (falls vorhanden, sonst `__PLACEHOLDER__`) |
| `review` | Erstmals im REVIEW-Objekt |
| `status` | `stub` (automatisch) → `enriched` (manuell) |

Platzhalter (`__PLACEHOLDER__`) markieren Felder, die manuell nachgefüllt werden müssen.

## Deduplizierung

Beim Erzeugen eines neuen SRC-Objekts prüft der Workflow über `find_source_by_dedup()`, ob der `dedup_key` bereits im INDEX existiert. Wenn ja, wird die bestehende ID wiederverwendet — keine doppelten Quellen.

**Format:** `andreoni_1990`, `crumpler_2008`, `harbaugh_1998`

Der Dedup-Key wird aus dem Referenzstring extrahiert und unterstützt zwei Formate:
- `Andreoni, 1990`
- `Andreoni (1990)`

## BibTeX-Stubs

Für jedes neue SRC-Objekt wird ein BibTeX-Stub in `Knowledge/Sources/BibTeX/SRC-XXXXXX.bib` angelegt.

```bibtex
@article{Andreoni1990_SRC-000001,
  author = {Andreoni, J.},
  year   = {1990},
  title  = {__PLACEHOLDER__},
  journal = {__PLACEHOLDER__},
}
```

BibTeX-Keys folgen dem Schema: `{Nachname}{Jahr}_SRC-XXXXXX`.

## master.bib

`Knowledge/Bibliography/master.bib` wird in **Schritt 7** vollständig neu aufgebaut, indem alle `BibTeX/SRC-*.bib`-Stubs zusammengeführt werden.

Der INDEX-Eintrag `bibliography.total_entries` gibt die aktuelle Anzahl der Einträge an.

## unresolved_sources.yaml

`Knowledge/Bibliography/unresolved_sources.yaml` enthält Quellen, die keinem SRC-Objekt zugeordnet werden konnten.

```yaml
total_unresolved: 3
sources:
  - "Harbaugh et al., 2007"
  - "Unknown Author, 2019"
```

Diese Zahl erscheint in der Pipeline Quality Summary als `Unresolved srcs`.

## Arbeitsablauf für Bibliographie-Anreicherung

1. `beba literature` ausführen → Stubs mit Platzhaltern werden angelegt
2. Quellen mit Platzhaltern identifizieren: `grep -r "__PLACEHOLDER__" Knowledge/Sources/`
3. DOIs und Metadaten manuell in SRC-Objekte eintragen
4. BibTeX-Stubs aktualisieren
5. `beba regression --validate-only` ausführen

DOI-Anreicherung ist **nicht automatisiert** — externe Datenbankabfragen werden bewusst nicht implementiert.
