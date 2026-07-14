# AI-Architektur

## Überblick

BEBA-Tools verwendet mehrere KI-Provider. Der Dispatcher wählt den Provider anhand der Task-Konfiguration und fällt bei Fehler automatisch auf den nächsten zurück.

## Provider

Implementiert in: `beba/providers.py` (nicht ändern)

| Provider | Funktion |
|---|---|
| OpenAI | `ask_openai(prompt, model, api_key)` |
| Google Gemini | `ask_gemini(prompt, model, api_key)` |
| Anthropic | `ask_anthropic(prompt, model, api_key)` |

API-Keys werden aus `~/.config/beba/.env` gelesen und über `load_config()` bereitgestellt.

## Dispatcher

Implementiert in: `beba/dispatcher.py` (nicht ändern)

`dispatch(task, prompt)` löst den Task auf eine priorisierte Provider-Liste auf und versucht jeden in der angegebenen Reihenfolge. Der erste erfolgreiche Aufruf wird zurückgegeben.

```python
dispatch("literature", prompt_text)
# → versucht gemini-2.5-pro, dann gpt-5.5, dann claude-sonnet-4
```

## Task-Routing

Tasks werden in `~/.config/beba/providers.yaml` konfiguriert.

Aktuelle Standardkonfiguration:

```yaml
providers:
  literature:
    - provider: gemini
      model: gemini-2.5-pro
    - provider: openai
      model: gpt-5.5
    - provider: anthropic
      model: claude-sonnet-4-20250514

  theory:
    - provider: openai
      model: gpt-5.5
    - provider: anthropic
      model: claude-sonnet-4-20250514
    - provider: gemini
      model: gemini-2.5-pro

  extraction:
    - provider: anthropic
      model: claude-sonnet-4-20250514
    - provider: openai
      model: gpt-5.5
    - provider: gemini
      model: gemini-2.5-pro

  review:
    - provider: openai
      model: gpt-5.5
    - provider: anthropic
      model: claude-sonnet-4-20250514
    - provider: gemini
      model: gemini-2.5-pro
```

**Hinweis:** Tasks ohne expliziten Eintrag (z.B. `evidence`, `claims`, `ontology`) verwenden den `theory`-Standard (openai zuerst).

## Task-Zuordnung im Workflow

| Workflow-Schritt | Task-Name | Standard-Provider |
|---|---|---|
| 1 Synthese | `literature` | Gemini |
| 2 Evidenz | `evidence` | OpenAI (Fallback zu theory) |
| 3 Claims | `claims` | OpenAI (Fallback zu theory) |
| 4 Theorie | `theory` | OpenAI |
| 5 Ontologie | `ontology` | OpenAI (Fallback zu theory) |

## Konfiguration ändern

Nur `~/.config/beba/providers.yaml` ändern — niemals `dispatcher.py` oder `providers.py`.

Neue Provider werden in `providers.py` implementiert und in `dispatcher.py` registriert (erfordert explizite Anfrage).

## Fallback-Verhalten

Wenn alle konfigurierten Provider eines Tasks fehlschlagen, wird eine `RuntimeError`-Exception geworfen und der Workflow bricht ab. Das Manifest enthält in diesem Fall keinen abgeschlossenen Status.

## API-Key-Konfiguration

```bash
~/.config/beba/.env
```

Inhalte (nicht in Git):

```
OPENAI_API_KEY=sk-...
GEMINI_API_KEY=AI...
ANTHROPIC_API_KEY=sk-ant-...
```
