# Flag Battle: din YouTube API-nyckel

Streamerläget läser chatten i din livesändning via YouTube Data API. Utan nyckel får du en provperiod på 5 minuter om dagen; med din egen gratis nyckel kan du streama i timmar. Det tar ungefär 5 minuter.

## 1. Öppna Google Cloud

Gå till [console.cloud.google.com](https://console.cloud.google.com/) och logga in med valfritt Google-konto (det behöver inte vara kanalens konto). Godkänn villkoren om du ombeds. Inget kreditkort behövs.

## 2. Skapa ett projekt

Klicka på projektväljaren högst upp (**Select a project**) och sedan på **New project**. Vilket namn som helst, till exempel `flag-battle`. Klicka på **Create** och kontrollera att det nya projektet är valt högst upp — allt därefter görs i det.

## 3. Slå på YouTube Data API v3 — innan du skapar nyckeln

Öppna [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) och klicka på **Enable**. Det är på när knappen ändras till **Manage**. Utan det här steget fungerar inte nyckeln.

## 4. Skapa nyckeln

Öppna [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Bocka bara i **YouTube Data API v3** i listan med API-begränsningar och klicka på **Create**. Fönstret **API key created** visar din nyckel — kopiera den.

Om YouTube Data API v3 inte finns i listan, gå tillbaka till steg 3. Låt appbegränsningarna stå på **None**.

## 5. Klistra in den i appen

I Flag Battle: startskärmen → **Inställningar** → läget **Duell** → **Streamerläge** → **På**. Tryck på klistra in-knappen bredvid **Din YouTube API v3-nyckel** — inte i fältet för tipstexten under. Nyckeln sparas bara i din telefon, i dess säkra lagring, och visas aldrig på skärmen.

## Om nyckeln avvisas

Blocket **NÄSTA** visar varför:

- **”YouTube Data API v3 är avstängt för nyckeln”** — gör steg 3 i samma projekt som nyckeln hör till och vänta några minuter.
- **”nyckelns begränsningar blockerar YouTube”** — öppna nyckeln i [Credentials](https://console.cloud.google.com/apis/credentials): API-begränsningarna måste innehålla **YouTube Data API v3** och appbegränsningarna stå på **None**.
- **”YouTube-nyckeln är ogiltig”** — nyckeln kopierades inte helt: den börjar med `AIza` och är 39 tecken lång.

Gå sedan tillbaka till menyn och starta streamen igen.

## Bra att veta

- **Det är gratis.** Standardkvoten är 10 000 enheter per dag. I läget ”Direkt” kommer chatten i realtid och kvoten räcker till ungefär 6 timmars streaming per dag; ”Sparläge” drar ut den till ungefär 12 timmar, med upp till 10 sekunders fördröjning. Läget väljer du i appen.
- **Kvoten nollställs vid midnatt Stillahavstid.** Tar den slut visar appen det i blocket **NÄSTA**, och striderna fortsätter med slumpade flaggor.
- Använd projektet bara till Flag Battle, så att inget annat förbrukar kvoten.
- Vill du återkalla nyckeln tar du bort den under [Credentials](https://console.cloud.google.com/apis/credentials).
