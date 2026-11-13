# Flag Battle: din YouTube API-nøkkel

Strømmermodus leser chatten i direktesendingen din via YouTube Data API. Uten nøkkel får du en prøveperiode på 5 minutter om dagen; med din egen gratis nøkkel kan du strømme i timevis. Det tar omtrent 5 minutter.

## 1. Åpne Google Cloud

Gå til [console.cloud.google.com](https://console.cloud.google.com/) og logg inn med en hvilken som helst Google-konto (det trenger ikke være kanalens konto). Godta vilkårene hvis du blir bedt om det. Du trenger ikke kredittkort.

## 2. Lag et prosjekt

Klikk på prosjektvelgeren øverst (**Select a project**), deretter **New project**. Hvilket som helst navn, for eksempel `flag-battle`. Klikk på **Create** og sjekk at det nye prosjektet er valgt øverst — alt videre gjøres i det.

## 3. Slå på YouTube Data API v3 — før du lager nøkkelen

Åpne [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) og klikk på **Enable**. Det er på når knappen endres til **Manage**. Uten dette steget virker ikke nøkkelen.

## 4. Lag nøkkelen

Åpne [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Huk bare av **YouTube Data API v3** i listen over API-begrensninger og klikk på **Create**. Vinduet **API key created** viser nøkkelen din — kopier den.

Hvis YouTube Data API v3 ikke står i listen, gå tilbake til steg 3. La appbegrensningene stå på **None**.

## 5. Lim den inn i appen

I Flag Battle: startskjermen → **Innstillinger** → modus **Duell** → **Strømmermodus** → **På**. Trykk på lim inn-knappen ved siden av **Din YouTube API v3-nøkkel** — ikke i feltet for hinttekst under. Nøkkelen lagres bare på telefonen din, i den sikre lagringen, og vises aldri på skjermen.

## Hvis nøkkelen blir avvist

Blokken **NESTE** viser hvorfor:

- **«YouTube Data API v3 er slått av for nøkkelen»** — gjør steg 3 i samme prosjekt som nøkkelen, og vent noen minutter.
- **«nøkkelens begrensninger blokkerer YouTube»** — åpne nøkkelen i [Credentials](https://console.cloud.google.com/apis/credentials): API-begrensningene må inneholde **YouTube Data API v3**, appbegrensningene stå på **None**.
- **«YouTube-nøkkelen er ugyldig»** — nøkkelen ble ikke kopiert helt: den begynner med `AIza` og er 39 tegn lang.

Gå deretter tilbake til menyen og start strømmen på nytt.

## Greit å vite

- **Det er gratis.** Standardkvoten er 10 000 enheter per dag. I modusen «Umiddelbart» kommer chatten i sanntid, og kvoten holder til omtrent 6 timer strømming per dag; «Sparemodus» strekker den til omtrent 12 timer, med opptil 10 sekunders forsinkelse. Modusen velger du i appen.
- **Kvoten nullstilles ved midnatt stillehavstid.** Går den tom, viser appen det i blokken **NESTE**, og kampene fortsetter med tilfeldige flagg.
- Bruk prosjektet bare til Flag Battle, så ikke noe annet bruker opp kvoten.
- For å trekke tilbake nøkkelen sletter du den under [Credentials](https://console.cloud.google.com/apis/credentials).
