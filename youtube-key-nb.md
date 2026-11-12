# Flag Battle: din YouTube API-nøkkel

Strømmermodus leser chatten i direktesendingen din via YouTube Data API. Uten nøkkel får du en prøveperiode på 5 minutter om dagen; med din egen gratis nøkkel kan du strømme i timevis. Det tar omtrent 5 minutter.

## 1. Åpne Google Cloud

Gå til [console.cloud.google.com](https://console.cloud.google.com/) og logg inn med en hvilken som helst Google-konto (det trenger ikke være kanalens konto). Godta vilkårene hvis du blir bedt om det. Du trenger ikke kredittkort.

## 2. Opprett et prosjekt

Klikk på prosjektvelgeren øverst (**Select a project**) og deretter på **New project**. Alle navn fungerer, for eksempel `flag-battle`. Klikk på **Create** og sjekk at det nye prosjektet er valgt øverst.

## 3. Slå på YouTube Data API

Åpne [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) og klikk på **Enable**.

## 4. Opprett nøkkelen

Åpne [Credentials](https://console.cloud.google.com/apis/credentials) og klikk på **Create credentials** → **API key**. Åpne den nye nøkkelen for redigering:

- **API restrictions** → **Restrict key** → kryss av bare for **YouTube Data API v3**. Da kan en lekket nøkkel ikke brukes til noe annet.
- **Application restrictions** kan stå på **None**.

Klikk på **Save** og kopier nøkkelen (**Show key** → kopier).

## 5. Lim den inn i appen

Åpne **Innstillinger → Duell → Strømmermodus** i Flag Battle og trykk på lim inn-knappen ved siden av feltet for YouTube API-nøkkelen. Nøkkelen lagres bare på telefonen din, i den sikre lagringen, og vises aldri på skjermen.

## Greit å vite

- **Det er gratis.** Standardkvoten er 10 000 enheter per dag. I modusen «Umiddelbart» kommer chatten i sanntid, og kvoten holder til omtrent 6 timer strømming per dag; «Sparemodus» strekker den til omtrent 12 timer, med opptil 10 sekunders forsinkelse. Modusen velger du i appen.
- **Kvoten nullstilles ved midnatt stillehavstid.** Går den tom, viser appen det i blokken **NESTE**, og kampene fortsetter med tilfeldige flagg.
- Bruk prosjektet bare til Flag Battle, så ikke noe annet bruker opp kvoten.
- For å trekke tilbake nøkkelen sletter du den under [Credentials](https://console.cloud.google.com/apis/credentials).
