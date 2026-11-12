# Flag Battle: Twój klucz API YouTube

Tryb streamera odczytuje czat Twojej transmisji przez YouTube Data API. Bez klucza masz 5 minut próby dziennie, a z własnym darmowym kluczem możesz nadawać godzinami. Zajmie to około 5 minut.

## 1. Otwórz Google Cloud

Wejdź na [console.cloud.google.com](https://console.cloud.google.com/) i zaloguj się dowolnym kontem Google (nie musi to być konto kanału). Jeśli trzeba, zaakceptuj warunki. Karta płatnicza nie jest potrzebna.

## 2. Utwórz projekt

U góry strony kliknij wybór projektu (**Select a project**), a potem **New project**. Nazwa może być dowolna, np. `flag-battle`. Kliknij **Create** i sprawdź, czy u góry wybrany jest nowy projekt.

## 3. Włącz YouTube Data API

Otwórz [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) i kliknij **Enable**.

## 4. Utwórz klucz

Otwórz [Credentials](https://console.cloud.google.com/apis/credentials) i kliknij **Create credentials** → **API key**. Otwórz nowy klucz do edycji:

- **API restrictions** → **Restrict key** → zaznacz tylko **YouTube Data API v3**. Wtedy wyciek klucza nie pozwoli użyć go do niczego innego.
- **Application restrictions** może zostać **None**.

Kliknij **Save** i skopiuj klucz (**Show key** → kopiuj).

## 5. Wklej go w aplikacji

W Flag Battle otwórz **Ustawienia → Pojedynek → Tryb streamera** i stuknij przycisk wklejania obok pola klucza API YouTube. Klucz jest przechowywany tylko na Twoim telefonie, w bezpiecznym magazynie, i nigdy nie pojawia się na ekranie.

## Warto wiedzieć

- **To nic nie kosztuje.** Standardowy limit to 10 000 jednostek dziennie. Przy odczycie czatu co 8 sekund wystarcza na około 4,4 godziny transmisji dziennie (co 5 s ≈ 2,8 h, co 10 s ≈ 5,6 h); odstęp wybierasz w aplikacji.
- **Limit odnawia się o północy czasu pacyficznego.** Gdy się wyczerpie, aplikacja pokaże to w bloku **NASTĘPNI**, a walki potoczą się dalej z losowymi flagami.
- Używaj projektu tylko do Flag Battle, aby nic innego nie zużywało limitu.
- Aby unieważnić klucz, usuń go w [Credentials](https://console.cloud.google.com/apis/credentials).
