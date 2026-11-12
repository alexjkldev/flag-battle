# Flag Battle: oma YouTube API -avaimesi

Striimaajatila lukee lähetyksesi chattia YouTube Data API:n kautta. Ilman avainta saat 5 minuutin kokeilun päivässä; omalla ilmaisella avaimella voit striimata tuntikausia. Tähän menee noin 5 minuuttia.

## 1. Avaa Google Cloud

Mene osoitteeseen [console.cloud.google.com](https://console.cloud.google.com/) ja kirjaudu millä tahansa Google-tilillä (sen ei tarvitse olla kanavasi tili). Hyväksy ehdot, jos niitä pyydetään. Luottokorttia ei tarvita.

## 2. Luo projekti

Napsauta sivun yläreunassa projektin valitsinta (**Select a project**) ja sitten **New project**. Nimi voi olla mikä tahansa, esimerkiksi `flag-battle`. Napsauta **Create** ja tarkista, että uusi projekti on valittuna yläreunassa.

## 3. Ota YouTube Data API käyttöön

Avaa [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) ja napsauta **Enable**.

## 4. Luo avain

Avaa [Credentials](https://console.cloud.google.com/apis/credentials) ja napsauta **Create credentials** → **API key**. Avaa uusi avain muokattavaksi:

- **API restrictions** → **Restrict key** → valitse vain **YouTube Data API v3**. Silloin vuotanutta avainta ei voi käyttää mihinkään muuhun.
- **Application restrictions** voi jäädä arvoon **None**.

Napsauta **Save** ja kopioi avain (**Show key** → kopioi).

## 5. Liitä se sovellukseen

Avaa Flag Battlessa **Asetukset → Kaksintaistelu → Striimaajatila** ja napauta YouTube API -avaimen kentän vieressä olevaa liittämispainiketta. Avain tallennetaan vain puhelimeesi sen suojattuun tallennustilaan, eikä sitä näytetä koskaan ruudulla.

## Hyvä tietää

- **Se on ilmaista.** Vakiokiintiö on 10 000 yksikköä päivässä. Tilassa ”Heti” chat tulee reaaliajassa, ja kiintiö riittää noin 6 tunnin striimaukseen päivässä; ”Säästö” venyttää sen noin 12 tuntiin, enintään 10 sekunnin viiveellä. Tilan valitset sovelluksessa.
- **Kiintiö nollautuu keskiyöllä Tyynenmeren aikaa.** Jos se loppuu, sovellus näyttää sen **SEURAAVAT**-lohkossa ja taistelut jatkuvat satunnaisilla lipuilla.
- Käytä projektia vain Flag Battleen, jotta mikään muu ei kuluta sen kiintiötä.
- Avaimen voit perua poistamalla sen kohdassa [Credentials](https://console.cloud.google.com/apis/credentials).
