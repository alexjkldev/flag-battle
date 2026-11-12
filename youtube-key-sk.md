# Flag Battle: váš kľúč YouTube API

Režim streamera číta chat vášho prenosu cez YouTube Data API. Bez kľúča máte 5-minútovú skúšku denne, s vlastným bezplatným kľúčom môžete vysielať celé hodiny. Trvá to asi 5 minút.

## 1. Otvorte Google Cloud

Choďte na [console.cloud.google.com](https://console.cloud.google.com/) a prihláste sa ľubovoľným účtom Google (nemusí to byť účet kanála). Ak treba, prijmite podmienky. Platobná karta nie je potrebná.

## 2. Vytvorte projekt

Hore na stránke kliknite na výber projektu (**Select a project**) a potom na **New project**. Názov môže byť ľubovoľný, napr. `flag-battle`. Kliknite na **Create** a skontrolujte, či je hore vybraný nový projekt.

## 3. Zapnite YouTube Data API

Otvorte [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) a kliknite na **Enable**.

## 4. Vytvorte kľúč

Otvorte [Credentials](https://console.cloud.google.com/apis/credentials) a kliknite na **Create credentials** → **API key**. Otvorte nový kľúč na úpravu:

- **API restrictions** → **Restrict key** → označte iba **YouTube Data API v3**. Uniknutý kľúč potom nepôjde použiť na nič iné.
- **Application restrictions** môže zostať **None**.

Kliknite na **Save** a skopírujte kľúč (**Show key** → kopírovať).

## 5. Vložte ho do aplikácie

Vo Flag Battle otvorte **Nastavenia → Súboj → Režim streamera** a ťuknite na tlačidlo vloženia vedľa poľa kľúča YouTube API. Kľúč sa ukladá iba vo vašom telefóne, v zabezpečenom úložisku, a nikdy sa nezobrazuje na obrazovke.

## Dobré vedieť

- **Je to zadarmo.** Štandardná kvóta je 10 000 jednotiek denne. Pri čítaní chatu každých 8 sekúnd vystačí približne na 4,4 hodiny vysielania denne (každých 5 s ≈ 2,8 h, každých 10 s ≈ 5,6 h); interval si vyberiete v aplikácii.
- **Kvóta sa obnovuje o polnoci tichomorského času.** Keď sa minie, aplikácia to ukáže v bloku **ĎALEJ** a súboje pokračujú s náhodnými vlajkami.
- Projekt používajte iba pre Flag Battle, aby kvótu nemíňalo nič iné.
- Ak chcete kľúč zrušiť, odstráňte ho v [Credentials](https://console.cloud.google.com/apis/credentials).
