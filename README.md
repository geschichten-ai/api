<pre>
<code>
# Geschichten API

Die Geschichten API liefert zufällige Geschichten im JSON-Format, inklusive Titel, Text, Bild-URL und Audio-URL.

## Endpunkt

```
GET /v1/
```

## Authentifizierung

Die API verwendet einen API-Schlüssel zur Authentifizierung. Der API-Schlüssel muss im `Authorization`-Header der Anfrage gesendet werden:

```
Authorization: Bearer API_KEY
```

Ersetzen Sie `API_KEY` durch Ihren gültigen API-Schlüssel.

## Antwort

Die API liefert eine JSON-Antwort mit den folgenden Feldern:

- `id`: Die eindeutige ID der Geschichte
- `title`: Der Titel der Geschichte
- `text`: Der Text der Geschichte
- `image`: Die vollständige URL zum Bild der Geschichte (kann `null` sein, falls kein Bild vorhanden ist)
- `audio`: Die vollständige URL zur Audio-Datei der Geschichte (kann `null` sein, falls keine Audio-Datei vorhanden ist)

## Beispielanfrage

```
curl -H "Authorization: Bearer API_KEY" https://api.geschichten.ai/v1/
```

## Beispielantwort

```json
{
  "id": "1",
  "title": "Eine schöne Geschichte",
  "text": "Es war einmal...",
  "image": "https://www.geschichten.ai/stories/img/1.png",
  "audio": "https://www.geschichten.ai/stories/mp3/1.mp3"
}
```

## Fehlerbehandlung

Fehler werden als JSON-Objekte zurückgegeben, die ein `error`-Feld enthalten, welches eine Beschreibung des aufgetretenen Fehlers enthält.

### Beispiel

```json
{
  "error": "API-Schlüssel fehlt oder ist ungültig."
}
```
</code>
</pre>
