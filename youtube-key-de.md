# Flag Battle: dein YouTube-API-Schlüssel

Der Streamer-Modus liest deinen Livechat über die YouTube Data API. Ohne Schlüssel gibt es eine Testphase von 5 Minuten am Tag; mit deinem eigenen kostenlosen Schlüssel kannst du stundenlang streamen. Das dauert etwa 5 Minuten.

## 1. Google Cloud öffnen

Öffne [console.cloud.google.com](https://console.cloud.google.com/) und melde dich mit einem beliebigen Google-Konto an (es muss nicht das Konto deines Kanals sein). Akzeptiere bei Bedarf die Bedingungen. Eine Kreditkarte ist nicht nötig.

## 2. Projekt anlegen

Klicke oben auf die Projektauswahl (**Select a project**) und dann auf **New project**. Der Name ist egal, z. B. `flag-battle`. Klicke auf **Create** und prüfe, dass oben das neue Projekt ausgewählt ist.

## 3. YouTube Data API aktivieren

Öffne [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) und klicke auf **Enable**.

## 4. Schlüssel erstellen

Öffne [Credentials](https://console.cloud.google.com/apis/credentials) und klicke auf **Create credentials** → **API key**. Öffne den neuen Schlüssel zum Bearbeiten:

- **API restrictions** → **Restrict key** → nur **YouTube Data API v3** anhaken. Dann lässt sich ein geleakter Schlüssel für nichts anderes nutzen.
- **Application restrictions** kann auf **None** bleiben.

Klicke auf **Save** und kopiere den Schlüssel (**Show key** → kopieren).

## 5. In die App einfügen

Öffne in Flag Battle **Einstellungen → Duell → Streamer-Modus** und tippe auf die Einfügen-Schaltfläche neben dem Feld für den YouTube-API-Schlüssel. Der Schlüssel wird nur auf deinem Handy im sicheren Speicher abgelegt und nie auf dem Bildschirm angezeigt.

## Gut zu wissen

- **Es ist kostenlos.** Das Standardkontingent beträgt 10.000 Einheiten pro Tag. Im Modus „Sofort“ kommt der Chat in Echtzeit an, und das Kontingent reicht für etwa 6 Stunden Stream pro Tag; „Sparsam“ streckt es auf etwa 12 Stunden, mit bis zu 10 Sekunden Verzögerung. Den Modus wählst du in der App.
- **Das Kontingent wird um Mitternacht pazifischer Zeit zurückgesetzt.** Ist es aufgebraucht, zeigt die App das im Block **NÄCHSTE**, und die Kämpfe laufen mit zufälligen Flaggen weiter.
- Nutze das Projekt nur für Flag Battle, damit nichts anderes das Kontingent verbraucht.
- Um den Schlüssel zu widerrufen, lösche ihn unter [Credentials](https://console.cloud.google.com/apis/credentials).
