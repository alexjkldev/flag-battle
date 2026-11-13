# Flag Battle: je YouTube API-sleutel

De streamermodus leest de chat van je livestream via de YouTube Data API. Zonder sleutel krijg je een proefperiode van 5 minuten per dag; met je eigen gratis sleutel kun je urenlang streamen. Het kost ongeveer 5 minuten.

## 1. Open Google Cloud

Ga naar [console.cloud.google.com](https://console.cloud.google.com/) en log in met een willekeurig Google-account (het hoeft niet het account van je kanaal te zijn). Accepteer de voorwaarden als dat wordt gevraagd. Een creditcard is niet nodig.

## 2. Maak een project

Klik bovenaan op de projectkiezer (**Select a project**) en dan op **New project**. Elke naam is goed, bijvoorbeeld `flag-battle`. Klik op **Create** en controleer dat bovenaan het nieuwe project is geselecteerd — al het volgende gebeurt daarin.

## 3. Zet YouTube Data API v3 aan — vóór je de sleutel maakt

Open [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) en klik op **Enable**. Hij staat aan als de knop verandert in **Manage**. Zonder deze stap werkt de sleutel niet.

## 4. Maak de sleutel

Open [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Vink in de lijst met API-beperkingen alleen **YouTube Data API v3** aan en klik op **Create**. Het venster **API key created** toont je sleutel — kopieer hem.

Staat YouTube Data API v3 niet in de lijst, ga dan terug naar stap 3. Laat de app-beperkingen op **None**.

## 5. Plak hem in de app

In Flag Battle: hoofdscherm → **Instellingen** → modus **Duel** → **Streamermodus** → **Aan**. Tik op de plakknop naast **Jouw YouTube API v3-sleutel** — niet in het veld voor de hinttekst eronder. De sleutel staat alleen op je telefoon, in de beveiligde opslag, en wordt nooit op het scherm getoond.

## Als de sleutel wordt geweigerd

Het blok **VOLGENDE** toont waarom:

- **‘YouTube Data API v3 staat uit voor deze sleutel’** — doe stap 3 in hetzelfde project als de sleutel en wacht een paar minuten.
- **‘sleutelbeperkingen blokkeren YouTube’** — open de sleutel in [Credentials](https://console.cloud.google.com/apis/credentials): bij de API-beperkingen moet **YouTube Data API v3** staan, de app-beperkingen op **None**.
- **‘YouTube-sleutel ongeldig’** — de sleutel is niet volledig gekopieerd: hij begint met `AIza` en is 39 tekens lang.

Ga daarna terug naar het menu en start de stream opnieuw.

## Goed om te weten

- **Het is gratis.** Het standaardquotum is 10.000 eenheden per dag. In de modus ‘Direct’ komt de chat in realtime binnen en is het quotum genoeg voor ongeveer 6 uur streamen per dag; ‘Zuinig’ rekt het op tot ongeveer 12 uur, met tot 10 seconden vertraging. De modus kies je in de app.
- **Het quotum wordt om middernacht Pacific Time gereset.** Is het op, dan toont de app dat in het blok **VOLGENDE** en gaan de gevechten door met willekeurige vlaggen.
- Gebruik het project alleen voor Flag Battle, zodat niets anders het quotum opmaakt.
- Om de sleutel in te trekken, verwijder je hem in [Credentials](https://console.cloud.google.com/apis/credentials).
