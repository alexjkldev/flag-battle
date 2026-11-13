# Flag Battle: dein YouTube-API-Schlüssel

Der Streamer-Modus liest deinen Livechat über die YouTube Data API. Ohne Schlüssel gibt es eine Testphase von 5 Minuten am Tag; mit deinem eigenen kostenlosen Schlüssel kannst du stundenlang streamen. Das dauert etwa 5 Minuten.

## 1. Google Cloud öffnen

Öffne [console.cloud.google.com](https://console.cloud.google.com/) und melde dich mit einem beliebigen Google-Konto an (es muss nicht das Konto deines Kanals sein). Akzeptiere bei Bedarf die Bedingungen. Eine Kreditkarte ist nicht nötig.

## 2. Projekt anlegen

Klicke oben auf die Projektauswahl (**Select a project**) und dann auf **New project**. Der Name ist egal, zum Beispiel `flag-battle`. Klicke auf **Create** und prüfe, dass oben das neue Projekt ausgewählt ist — alles Weitere passiert darin.

## 3. YouTube Data API v3 einschalten — vor dem Schlüssel

Öffne [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) und klicke auf **Enable**. Die API ist an, wenn die Schaltfläche zu **Manage** wird. Ohne diesen Schritt funktioniert der Schlüssel nicht.

## 4. Schlüssel erstellen

Öffne [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Hake in der Liste der API-Einschränkungen nur **YouTube Data API v3** an und klicke auf **Create**. Im Fenster **API key created** steht dein Schlüssel — kopiere ihn.

Fehlt YouTube Data API v3 in der Liste, geh zurück zu Schritt 3. Lass die Anwendungseinschränkungen auf **None**.

## 5. In die App einfügen

In Flag Battle: Startbildschirm → **Einstellungen** → Modus **Duell** → **Streamer-Modus** → **An**. Tippe auf die Einfügen-Schaltfläche neben **Dein YouTube-API-v3-Schlüssel** — nicht ins Hinweistext-Feld darunter. Der Schlüssel wird nur auf deinem Handy im sicheren Speicher abgelegt und nie auf dem Bildschirm angezeigt.

## Wenn der Schlüssel abgelehnt wird

Der Grund steht im Block **NÄCHSTE**:

- **„YouTube Data API v3 ist für diesen Schlüssel aus“** — mach Schritt 3 im selben Projekt, zu dem der Schlüssel gehört, und warte ein paar Minuten.
- **„Schlüssel-Einschränkungen blockieren YouTube“** — öffne den Schlüssel in [Credentials](https://console.cloud.google.com/apis/credentials): Unter den API-Einschränkungen muss **YouTube Data API v3** stehen, die Anwendungseinschränkungen auf **None**.
- **„YouTube-Schlüssel ungültig“** — der Schlüssel wurde unvollständig kopiert: Er beginnt mit `AIza` und ist 39 Zeichen lang.

Danach zurück ins Menü und den Stream neu starten.

## Gut zu wissen

- **Es ist kostenlos.** Das Standardkontingent beträgt 10.000 Einheiten pro Tag. Im Modus „Sofort“ kommt der Chat in Echtzeit an, und das Kontingent reicht für etwa 6 Stunden Stream pro Tag; „Sparsam“ streckt es auf etwa 12 Stunden, mit bis zu 10 Sekunden Verzögerung. Den Modus wählst du in der App.
- **Das Kontingent wird um Mitternacht pazifischer Zeit zurückgesetzt.** Ist es aufgebraucht, zeigt die App das im Block **NÄCHSTE**, und die Kämpfe laufen mit zufälligen Flaggen weiter.
- Nutze das Projekt nur für Flag Battle, damit nichts anderes das Kontingent verbraucht.
- Um den Schlüssel zu widerrufen, lösche ihn unter [Credentials](https://console.cloud.google.com/apis/credentials).
