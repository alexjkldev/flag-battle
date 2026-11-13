# Flag Battle: oma YouTube API -avaimesi

Striimaajatila lukee lähetyksesi chattia YouTube Data API:n kautta. Ilman avainta saat 5 minuutin kokeilun päivässä; omalla ilmaisella avaimella voit striimata tuntikausia. Tähän menee noin 5 minuuttia.

## 1. Avaa Google Cloud

Mene osoitteeseen [console.cloud.google.com](https://console.cloud.google.com/) ja kirjaudu millä tahansa Google-tilillä (sen ei tarvitse olla kanavasi tili). Hyväksy ehdot, jos niitä pyydetään. Luottokorttia ei tarvita.

## 2. Luo projekti

Napsauta sivun yläreunassa projektivalitsinta (**Select a project**) ja sitten **New project**. Nimi voi olla mikä tahansa, esimerkiksi `flag-battle`. Napsauta **Create** ja tarkista, että ylhäällä on valittuna uusi projekti — kaikki seuraava tehdään siinä.

## 3. Ota YouTube Data API v3 käyttöön — ennen avaimen luomista

Avaa [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) ja napsauta **Enable**. Se on käytössä, kun painike muuttuu muotoon **Manage**. Ilman tätä vaihetta avain ei toimi.

## 4. Luo avain

Avaa [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Valitse API-rajoitusten listasta vain **YouTube Data API v3** ja napsauta **Create**. Ikkunassa **API key created** näkyy avaimesi — kopioi se.

Jos YouTube Data API v3 puuttuu listasta, palaa vaiheeseen 3. Jätä sovellusrajoitukset tilaan **None**.

## 5. Liitä se sovellukseen

Flag Battlessa: aloitusnäyttö → **Asetukset** → tila **Kaksintaistelu** → **Striimaajatila** → **Päällä**. Napauta liitä-painiketta kohdan **Oma YouTube API v3 -avaimesi** vieressä — ei sen alla olevaan vihjetekstin kenttään. Avain tallennetaan vain puhelimeesi, sen suojattuun tallennustilaan, eikä sitä koskaan näytetä ruudulla.

## Jos avain hylätään

Syy näkyy **SEURAAVAT**-lohkossa:

- **”YouTube Data API v3 ei ole päällä tälle avaimelle”** — tee vaihe 3 samassa projektissa, johon avain kuuluu, ja odota muutama minuutti.
- **”avaimen rajoitukset estävät YouTuben”** — avaa avain kohdassa [Credentials](https://console.cloud.google.com/apis/credentials): API-rajoituksissa pitää olla **YouTube Data API v3** ja sovellusrajoitukset tilassa **None**.
- **”YouTube-avain on virheellinen”** — avain kopioitui vajaana: se alkaa `AIza` ja on 39 merkkiä pitkä.

Palaa sen jälkeen valikkoon ja käynnistä striimi uudelleen.

## Hyvä tietää

- **Se on ilmaista.** Vakiokiintiö on 10 000 yksikköä päivässä. Tilassa ”Heti” chat tulee reaaliajassa, ja kiintiö riittää noin 6 tunnin striimaukseen päivässä; ”Säästö” venyttää sen noin 12 tuntiin, enintään 10 sekunnin viiveellä. Tilan valitset sovelluksessa.
- **Kiintiö nollautuu keskiyöllä Tyynenmeren aikaa.** Jos se loppuu, sovellus näyttää sen **SEURAAVAT**-lohkossa ja taistelut jatkuvat satunnaisilla lipuilla.
- Käytä projektia vain Flag Battleen, jotta mikään muu ei kuluta sen kiintiötä.
- Avaimen voit perua poistamalla sen kohdassa [Credentials](https://console.cloud.google.com/apis/credentials).
