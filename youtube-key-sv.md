# Flag Battle: din YouTube API-nyckel

Streamerläget läser chatten i din livesändning via YouTube Data API. Utan nyckel får du en provperiod på 5 minuter om dagen; med din egen gratis nyckel kan du streama i timmar. Det tar ungefär 5 minuter.

## 1. Öppna Google Cloud

Gå till [console.cloud.google.com](https://console.cloud.google.com/) och logga in med valfritt Google-konto (det behöver inte vara kanalens konto). Godkänn villkoren om du ombeds. Inget kreditkort behövs.

## 2. Skapa ett projekt

Klicka på projektväljaren högst upp (**Select a project**) och sedan på **New project**. Vilket namn som helst fungerar, till exempel `flag-battle`. Klicka på **Create** och kontrollera att det nya projektet är valt högst upp.

## 3. Aktivera YouTube Data API

Öppna [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) och klicka på **Enable**.

## 4. Skapa nyckeln

Öppna [Credentials](https://console.cloud.google.com/apis/credentials) och klicka på **Create credentials** → **API key**. Öppna den nya nyckeln för redigering:

- **API restrictions** → **Restrict key** → markera bara **YouTube Data API v3**. Då kan en läckt nyckel inte användas till något annat.
- **Application restrictions** kan stå kvar på **None**.

Klicka på **Save** och kopiera nyckeln (**Show key** → kopiera).

## 5. Klistra in den i appen

Öppna **Inställningar → Duell → Streamerläge** i Flag Battle och tryck på klistra in-knappen bredvid fältet för YouTube API-nyckeln. Nyckeln sparas bara på din telefon, i dess säkra lagring, och visas aldrig på skärmen.

## Bra att veta

- **Det är gratis.** Standardkvoten är 10 000 enheter per dag. I läget ”Direkt” kommer chatten i realtid och kvoten räcker till ungefär 6 timmars streaming per dag; ”Sparläge” drar ut den till ungefär 12 timmar, med upp till 10 sekunders fördröjning. Läget väljer du i appen.
- **Kvoten nollställs vid midnatt Stillahavstid.** Tar den slut visar appen det i blocket **NÄSTA**, och striderna fortsätter med slumpade flaggor.
- Använd projektet bara till Flag Battle, så att inget annat förbrukar kvoten.
- Vill du återkalla nyckeln tar du bort den under [Credentials](https://console.cloud.google.com/apis/credentials).
