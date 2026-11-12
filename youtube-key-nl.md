# Flag Battle: je YouTube API-sleutel

De streamermodus leest de chat van je livestream via de YouTube Data API. Zonder sleutel krijg je een proefperiode van 5 minuten per dag; met je eigen gratis sleutel kun je urenlang streamen. Het kost ongeveer 5 minuten.

## 1. Open Google Cloud

Ga naar [console.cloud.google.com](https://console.cloud.google.com/) en log in met een willekeurig Google-account (het hoeft niet het account van je kanaal te zijn). Accepteer de voorwaarden als dat wordt gevraagd. Een creditcard is niet nodig.

## 2. Maak een project

Klik bovenaan op de projectkiezer (**Select a project**) en daarna op **New project**. Elke naam is goed, bijvoorbeeld `flag-battle`. Klik op **Create** en controleer dat bovenaan het nieuwe project is geselecteerd.

## 3. Schakel de YouTube Data API in

Open [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) en klik op **Enable**.

## 4. Maak de sleutel

Open [Credentials](https://console.cloud.google.com/apis/credentials) en klik op **Create credentials** → **API key**. Open de nieuwe sleutel om hem te bewerken:

- **API restrictions** → **Restrict key** → vink alleen **YouTube Data API v3** aan. Dan is een gelekte sleutel voor niets anders te gebruiken.
- **Application restrictions** kan op **None** blijven.

Klik op **Save** en kopieer de sleutel (**Show key** → kopiëren).

## 5. Plak hem in de app

Open in Flag Battle **Instellingen → Duel → Streamermodus** en tik op de plakknop naast het veld voor de YouTube API-sleutel. De sleutel wordt alleen op je telefoon bewaard, in de beveiligde opslag, en nooit op het scherm getoond.

## Goed om te weten

- **Het is gratis.** Het standaardquotum is 10.000 eenheden per dag. Als de chat elke 8 seconden wordt gelezen, is dat genoeg voor ongeveer 4,4 uur streamen per dag (elke 5 s ≈ 2,8 u, elke 10 s ≈ 5,6 u); het interval kies je in de app.
- **Het quotum wordt om middernacht Pacific Time gereset.** Is het op, dan toont de app dat in het blok **VOLGENDE** en gaan de gevechten door met willekeurige vlaggen.
- Gebruik het project alleen voor Flag Battle, zodat niets anders het quotum opmaakt.
- Om de sleutel in te trekken, verwijder je hem in [Credentials](https://console.cloud.google.com/apis/credentials).
