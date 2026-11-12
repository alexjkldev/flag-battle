# Integritetspolicy

*12 november 2026*

Denna integritetspolicy förklarar hur personuppgifter behandlas när du använder mobilappen Flag Battle ("Appen").

## Personuppgiftsansvarig

Personuppgiftsansvarig för behandlingen av dina personuppgifter är:

**AlexJKL Oy** (Finland)
E-post: [support@alexjkl.fi](mailto:support@alexjkl.fi)

## Uppgifter som lagras på din enhet

Appen kräver inget konto och sparar allt ditt innehåll (valda länder, stridsnamn, inställningar) lokalt på din enhet.

## Uppgifter som behandlas av tredjepartstjänster

Appen använder följande tjänster, som behandlar uppgifter som enhetsidentifierare (annons-ID, installations-ID), IP-adress, information om enhet och operativsystem samt interaktioner med appen och annonser:

- **Unity LevelPlay** (Unity Technologies) — annonsmedling: väljer vilket annonsnätverk som visar varje annons och mäter annonser. Samlar in annons-ID, enhetsinformation, annonsinteraktioner och SDK-diagnostik. [Unitys integritetspolicy](https://unity.com/legal/privacy-policy)
- **Google AdMob** — visar och mäter annonser. Samlar in annons-ID, enhetsinformation, annonsinteraktioner (klick, visningar, vilka annonser du har sett) och SDK-diagnostik. [Googles integritetspolicy](https://policies.google.com/privacy)
- **Unity Ads** — visar annonser via Unity LevelPlay- eller AdMob-medling. Samlar in annons-ID, enhetsinformation, annonsinteraktioner och SDK-diagnostik. [Unitys integritetspolicy](https://unity.com/legal/privacy-policy)
- **Liftoff Monetize (Vungle)** — visar annonser via Unity LevelPlay- eller AdMob-medling. Samlar in annons-ID, enhetsinformation, annonsinteraktioner och SDK-diagnostik. [Liftoffs integritetspolicy](https://liftoff.io/privacy-policy/)
- **Pangle** (Bytedance Pte. Ltd., Singapore) — visar annonser via Unity LevelPlay- eller AdMob-medling. Samlar in annons-ID, IP-adress och den ungefärliga plats som härleds från den, enhetsinformation, annonsinteraktioner och SDK-diagnostik. [Pangles integritetspolicy](https://www.pangleglobal.com/privacy/enduser-en)
- **RevenueCat** — hanterar prenumerationsköp, lagrar din köphistorik och tilldelar ett anonymt app-användar-ID. På iOS tar den även emot Apples annonsattribution (om Appen installerades från en Apple Ads-kampanj, och från vilken kampanj och vilket sökord) så att vi kan mäta vår egen annonsering. [RevenueCats integritetspolicy](https://www.revenuecat.com/privacy)
- **Firebase (Google)**:
  - *Crashlytics* — krasch- och felrapporter: stackspår, operativsystemversion, enhetsmodell, installations-ID.
  - *Analytics* — användningshändelser i appen, kopplade till ett ID för appinstansen.
  - *Remote Config* — hämtar appens konfiguration från Googles servrar.

  [Googles integritetspolicy](https://policies.google.com/privacy)

Annonsnätverk agerar som självständigt personuppgiftsansvariga för de uppgifter de samlar in eller, där deras villkor föreskriver det, som gemensamt personuppgiftsansvariga med oss (till exempel Pangle för viss behandling enligt artikel 26 i GDPR). Deras integritetspolicyer, länkade ovan, beskriver deras behandling i detalj.

## Streamerläge (YouTube)

Streamerläget (Duell, Premium) använder **YouTube API Services**. När du slår på det och anger en länk till din YouTube-livesändning läser Appen den offentliga livechatten för sändningen direkt från YouTube: tittarnas visningsnamn, kanal-ID:n, meddelanden och belopp för Super Chat / Super Sticker. Uppgifterna visas på skärmen under sändningen (röster, kön, fans, Super Chat-meddelanden) och finns bara i enhetens minne medan streamerläget är igång. De sparas inte, skickas inte till oss och delas inte med någon, och de kastas när du lämnar streamerläget eller stänger Appen.

Förfrågningarna går direkt från din enhet till Googles servrar, så Google tar emot din IP-adress och själva förfrågningarna. Om du anger en egen YouTube Data API-nyckel lagras den bara på din enhet, i systemets säkra lagring (Keychain / Keystore), och skickas bara till Google med varje förfrågan — aldrig till oss. Utan egen nyckel använder Appen sin egen nyckel för en kort daglig provperiod; hur mycket av dagens provperiod som använts lagras lokalt på din enhet.

Genom att använda streamerläget godkänner du [YouTubes användarvillkor](https://www.youtube.com/t/terms). Hur Google hanterar uppgifter beskrivs i [Googles integritetspolicy](https://policies.google.com/privacy). Du kan när som helst stoppa Appens åtkomst genom att stänga av streamerläget; din egen nyckel tar du bort genom att rensa den i Appen eller radera den i din Google Cloud Console.

## Ändamål och rättslig grund

| Ändamål | Rättslig grund (GDPR) |
|---|---|
| Personanpassade annonser | Ditt samtycke (art. 6.1 a) |
| Icke-personanpassade annonser och annonsmätning | Ditt samtycke eller vårt berättigade intresse av att finansiera den kostnadsfria versionen av Appen (art. 6.1 a eller f), enligt samtyckesformuläret |
| Premiumprenumeration | Fullgörande av ett avtal med dig (art. 6.1 b) |
| Kraschrapportering och appkonfiguration | Vårt berättigade intresse av en stabil och väl fungerande App (art. 6.1 f) |
| Användningsanalys | Vårt berättigade intresse av att förstå och förbättra Appen (art. 6.1 f) |
| Mätning av våra egna annonskampanjer (Apple Ads-attribution) | Vårt berättigade intresse av att veta vilka av våra annonser som ger Appen nya användare (art. 6.1 f) |
| Svar på dina meddelanden | Vårt berättigade intresse av att svara dig (art. 6.1 f) |
| Streamerläge (läsa chatten för din YouTube-sändning) | Fullgörande av avtal med dig — funktionen du slår på (art. 6.1 b); för tittare vars meddelanden visas, vårt berättigade intresse av att erbjuda funktionen (art. 6.1 f) |

## Dina samtyckesval

I Europeiska ekonomiska samarbetsområdet, Storbritannien och Schweiz ber Appen om ditt samtycke via Googles samtyckesformulär innan personanpassade annonser visas. Du kan när som helst ändra eller återkalla ditt samtycke i Appen under **Inställningar → Sekretessalternativ för annonser**. Återkallelsen påverkar inte behandling som skett före återkallelsen.

På iOS kräver personanpassade annonser även ditt tillstånd via App Tracking Transparency, som du kan ändra i iOS-appen Inställningar.

## Överföringar till tredjeland

Vissa av tjänsterna ovan behandlar uppgifter utanför Europeiska ekonomiska samarbetsområdet, särskilt i USA (Google, Unity, Liftoff, RevenueCat) samt i Singapore och USA (Pangle), och deras koncernbolag och tjänsteleverantörer kan komma åt uppgifter från andra länder. Sådana överföringar grundar sig på EU–US Data Privacy Framework när mottagaren är certifierad enligt det, eller på Europeiska kommissionens standardavtalsklausuler.

## Lagringstid

- **Kraschrapporter (Crashlytics)** — sparas av Google i 90 dagar.
- **Analysdata** — sparas enligt Googles lagringsinställningar för Firebase Analytics.
- **Uppgifter som samlas in av annonsnätverk och RevenueCat** — sparas enligt deras egna integritetspolicyer.
- **Dina meddelanden till oss** — sparas så länge det behövs för att hantera ditt ärende och raderas därefter.
- **YouTube-chattdata (streamerläge)** — bara i minnet medan streamerläget är igång; sparas aldrig.

## Dina rättigheter

Enligt GDPR har du rätt att:

- få tillgång till dina personuppgifter och få en kopia av dem
- få felaktiga uppgifter rättade
- få dina uppgifter raderade
- begränsa behandlingen
- dataportabilitet
- invända mot behandling som grundar sig på berättigat intresse
- när som helst återkalla ditt samtycke

Kontakta oss på [support@alexjkl.fi](mailto:support@alexjkl.fi) för att utöva dina rättigheter. Eftersom de flesta uppgifter behandlas av tjänsterna ovan under enhetsidentifierare som vi inte kan koppla till dig, kan vi behöva hänvisa vissa förfrågningar till dessa tjänster. Du kan också kontakta dem direkt via deras integritetspolicyer.

Du har också rätt att lämna in ett klagomål till en tillsynsmyndighet, särskilt i det EU-land där du bor eller arbetar. I Finland är det [Dataombudsmannens byrå](https://tietosuoja.fi/en).

## Barns integritet

Appen riktar sig inte till barn. Vi samlar inte medvetet in personuppgifter från barn som inte har uppnått åldern för digitalt samtycke i sitt land (13–16 år i EU). Om du tror att ett barn har lämnat personuppgifter till oss, kontakta oss så raderar vi dem.

## Ändringar av denna policy

Vi kan uppdatera denna integritetspolicy då och då. Den aktuella versionen finns alltid på denna sida, och datumet överst visar när den senast ändrades.

## Kontakt

AlexJKL Oy — [support@alexjkl.fi](mailto:support@alexjkl.fi)

Du kan också kontakta oss via Appen eller via Appens sida i App Store eller Google Play. När du kontaktar oss får vi din e-postadress, innehållet i ditt meddelande och eventuella bilagor. Vi använder denna information endast för att svara dig och förbättra Appen, och vi delar den inte med tredje part.
