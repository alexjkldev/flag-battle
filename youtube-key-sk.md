# Flag Battle: váš kľúč YouTube API

Režim streamera číta chat vášho prenosu cez YouTube Data API. Bez kľúča máte 5-minútovú skúšku denne, s vlastným bezplatným kľúčom môžete vysielať celé hodiny. Trvá to asi 5 minút.

## 1. Otvorte Google Cloud

Choďte na [console.cloud.google.com](https://console.cloud.google.com/) a prihláste sa ľubovoľným účtom Google (nemusí to byť účet kanála). Ak treba, prijmite podmienky. Platobná karta nie je potrebná.

## 2. Vytvorte projekt

Hore na stránke kliknite na výber projektu (**Select a project**) a potom na **New project**. Názov môže byť ľubovoľný, napríklad `flag-battle`. Kliknite na **Create** a skontrolujte, že hore je vybraný nový projekt — všetko ďalej sa robí v ňom.

## 3. Zapnite YouTube Data API v3 — pred vytvorením kľúča

Otvorte [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) a kliknite na **Enable**. API je zapnuté, keď sa tlačidlo zmení na **Manage**. Bez tohto kroku kľúč nebude fungovať.

## 4. Vytvorte kľúč

Otvorte [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. V zozname obmedzení API označte iba **YouTube Data API v3** a kliknite na **Create**. V okne **API key created** uvidíte svoj kľúč — skopírujte ho.

Ak YouTube Data API v3 v zozname nie je, vráťte sa ku kroku 3. Obmedzenia aplikácií nechajte na **None**.

## 5. Vložte ho do aplikácie

Vo Flag Battle: hlavná obrazovka → **Nastavenia** → režim **Súboj** → **Režim streamera** → **Zap.**. Ťuknite na tlačidlo vloženia vedľa **Tvoj kľúč YouTube API v3** — nie do poľa textu nápovedy pod ním. Kľúč je uložený iba vo vašom telefóne, v zabezpečenom úložisku, a nikdy sa nezobrazuje na obrazovke.

## Ak je kľúč odmietnutý

Dôvod uvidíte v bloku **ĎALEJ**:

- **„YouTube Data API v3 je pre tento kľúč vypnuté“** — urobte krok 3 v tom istom projekte, kde je kľúč, a počkajte pár minút.
- **„obmedzenia kľúča blokujú YouTube“** — otvorte kľúč v [Credentials](https://console.cloud.google.com/apis/credentials): v obmedzeniach API musí byť **YouTube Data API v3**, obmedzenia aplikácií na **None**.
- **„kľúč YouTube je neplatný“** — kľúč sa neskopíroval celý: začína sa `AIza` a má 39 znakov.

Potom sa vráťte do menu a spustite stream znova.

## Dobré vedieť

- **Je to zadarmo.** Štandardná kvóta je 10 000 jednotiek denne. V režime „Okamžite“ prichádza chat v reálnom čase a kvóta vystačí približne na 6 hodín vysielania denne; režim „Úsporne“ ju natiahne približne na 12 hodín, s oneskorením do 10 sekúnd. Režim si vyberiete v aplikácii.
- **Kvóta sa obnovuje o polnoci tichomorského času.** Keď sa minie, aplikácia to ukáže v bloku **ĎALEJ** a súboje pokračujú s náhodnými vlajkami.
- Projekt používajte iba pre Flag Battle, aby kvótu nemíňalo nič iné.
- Ak chcete kľúč zrušiť, odstráňte ho v [Credentials](https://console.cloud.google.com/apis/credentials).
