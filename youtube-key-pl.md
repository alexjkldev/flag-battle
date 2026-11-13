# Flag Battle: Twój klucz API YouTube

Tryb streamera odczytuje czat Twojej transmisji przez YouTube Data API. Bez klucza masz 5 minut próby dziennie, a z własnym darmowym kluczem możesz nadawać godzinami. Zajmie to około 5 minut.

## 1. Otwórz Google Cloud

Wejdź na [console.cloud.google.com](https://console.cloud.google.com/) i zaloguj się dowolnym kontem Google (nie musi to być konto kanału). Jeśli trzeba, zaakceptuj warunki. Karta płatnicza nie jest potrzebna.

## 2. Utwórz projekt

U góry strony kliknij wybór projektu (**Select a project**), a potem **New project**. Nazwa dowolna, np. `flag-battle`. Kliknij **Create** i sprawdź, czy u góry wybrany jest nowy projekt — wszystko dalej robisz w nim.

## 3. Włącz YouTube Data API v3 — przed utworzeniem klucza

Otwórz [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) i kliknij **Enable**. API jest włączone, gdy przycisk zmieni się na **Manage**. Bez tego kroku klucz nie zadziała.

## 4. Utwórz klucz

Otwórz [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Na liście ograniczeń API zaznacz tylko **YouTube Data API v3** i kliknij **Create**. W oknie **API key created** zobaczysz klucz — skopiuj go.

Jeśli na liście nie ma YouTube Data API v3, wróć do kroku 3. Ograniczenia aplikacji zostaw na **None**.

## 5. Wklej go w aplikacji

W Flag Battle: ekran główny → **Ustawienia** → tryb **Pojedynek** → **Tryb streamera** → **Wł.**. Stuknij przycisk wklejania obok pola **Twój klucz YouTube API v3** — nie w pole tekstu podpowiedzi poniżej. Klucz jest przechowywany tylko na Twoim telefonie, w bezpiecznym magazynie, i nigdy nie jest pokazywany na ekranie.

## Jeśli klucz zostanie odrzucony

Przyczynę widać w bloku **NASTĘPNI**:

- **„YouTube Data API v3 jest wyłączone dla tego klucza”** — wykonaj krok 3 w tym samym projekcie, w którym jest klucz, i odczekaj kilka minut.
- **„ograniczenia klucza blokują YouTube”** — otwórz klucz w [Credentials](https://console.cloud.google.com/apis/credentials): w ograniczeniach API musi być **YouTube Data API v3**, a ograniczenia aplikacji na **None**.
- **„klucz YouTube jest nieprawidłowy”** — klucz skopiowano niecały: zaczyna się od `AIza` i ma 39 znaków.

Potem wróć do menu i uruchom transmisję ponownie.

## Warto wiedzieć

- **To nic nie kosztuje.** Standardowy limit to 10 000 jednostek dziennie. W trybie „Natychmiast” czat dociera na bieżąco, a limit wystarcza na około 6 godzin transmisji dziennie; tryb „Oszczędnie” wydłuża go do około 12 godzin, z opóźnieniem do 10 sekund. Tryb wybierasz w aplikacji.
- **Limit odnawia się o północy czasu pacyficznego.** Gdy się wyczerpie, aplikacja pokaże to w bloku **NASTĘPNI**, a walki potoczą się dalej z losowymi flagami.
- Używaj projektu tylko do Flag Battle, aby nic innego nie zużywało limitu.
- Aby unieważnić klucz, usuń go w [Credentials](https://console.cloud.google.com/apis/credentials).
