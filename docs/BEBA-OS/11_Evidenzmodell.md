# Evidenzmodell

## Grundprinzip

Im BEBA-Informationsmodell ist Evidenz eine **nicht-interpretive Extraktion** aus der Primärliteratur. Sie dokumentiert, was in den Quellen steht — nicht, was es für BEBA bedeutet.

Die Interpretation erfolgt auf Ebene der Claims und der Theory Integration.

## Evidenz-Typen

| Typ | Bedeutung |
|---|---|
| `positive` | Befund unterstützt die untersuchte Beziehung |
| `negative` | Befund widerspricht der untersuchten Beziehung |
| `mixed` | Befund zeigt sowohl bestätigende als auch widersprechende Muster |
| `neutral` | Befund hat keine direkte Richtung (deskriptiv, methodisch) |
| `report` | Zusammenfassender Blob ohne strukturierte Extraktion |

## Strukturiertes Evidenz-Protokoll (v2)

Das EVIDENCE_EXTRACTION_PROTOCOL v2 schreibt strukturierte Blöcke vor:

```markdown
## EVIDENCE_ITEMS

### EVIDENCE
finding: Donors respond to warm glow even when marginal impact is zero.
direction: positive
strength: strong
concepts: [Warm_Glow_Giving, Impure_Altruism]
sources: Andreoni, 1990; Crumpler & Grossman, 2008
limitations: Laboratory setting, US students.
notes:
```

## Extraction Confidence

Jedes EVID-Objekt trägt ein `extraction_confidence`-Feld:

| Wert | Bedingung |
|---|---|
| `high` | Strukturierter `## EVIDENCE_ITEMS`-Block **und** Quellen aufgelöst zu SRC-IDs |
| `medium` | Strukturierter Block **oder** aufgelöste Quellen (nicht beides) |
| `low` | Blob-Fallback oder keine Attribution |

## Quellenattribution

Attribution erfolgt in zwei Schritten:

**Schritt 1 — explizites `sources`-Feld (strukturierter Parser):**
Der Referenzstring aus `sources:` wird über den Dedup-Key gegen bekannte SRC-Objekte abgeglichen.

**Schritt 2 — Namensabgleich (Legacy-Fallback):**
Autorennamen aus bekannten Quellen werden im Text des Evidenzblocks gesucht.

**Ergebnis `unresolved`:** Wenn keine Attribution möglich ist, wird ein TODO ins Manifest eingetragen und `source_assignment: unresolved` gesetzt.

## Fallback-Verhalten

Wenn der strukturierte Parser (`## EVIDENCE_ITEMS`) keine Blöcke findet:

1. Legacy-Parser: Abschnitte „Positive Evidence", „Mixed Evidence", „Negative Evidence"
2. Kein Ergebnis: Blob-EVID mit `type: report` und `extraction_confidence: low`

Der Blob enthält den gesamten Evidenz-Response des KI-Providers.

## Evidenz und Claims

Evidenz und Claims sind **getrennte Objekte** mit unterschiedlichem Abstraktionsniveau:

| | Evidenz (EVID) | Claim |
|---|---|---|
| Inhalt | Was die Quelle berichtet | Was das bedeutet (interpretiert) |
| Quelle | Direkt aus Primärliteratur | Aus Synthese + Interpretation |
| Attribution | SRC-IDs | SRC-IDs (über EVID) |
| Granularität | Ein Befund | Eine wissenschaftliche Aussage |

## Bekannte Einschränkungen

- Quellen-Attribution ist nicht vollständig automatisierbar bei unstrukturiertem Protokoll-Output.
- `extraction_confidence` ist ein Proxy für Prozessqualität, keine inhaltliche Gütebeurteilung.
- Duplikate über Reviews hinweg sind möglich (keine EVID-Deduplizierung — nur SRC-Deduplizierung).
