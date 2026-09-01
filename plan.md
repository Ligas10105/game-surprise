Zadanie: Stwórz interaktywną grę przeglądarkową w HTML5/JS (z użyciem elementu <canvas>), zoptymalizowaną pod urządzenia mobilne (pionowy ekran, sterowanie dotykiem). Gra łączy gatunek 'Endless Runner' z Quizem z wiedzy o związku.

Fabuła i Cel: Gracz (reprezentowany przez emoji walizki 🧳 lub prostą grafikę) biegnie w górę ekranu, aby zdążyć na lot. Gra ma płynnie przesuwające się tło przypominające korytarz lotniska lub pas startowy. Cel to zebranie 5 poprawnych odpowiedzi na pytania quizowe.

1. Ekran Startowy (Menu):

Tytuł: "Gotowa na odlot? Ostatnie wezwanie dla pasażerów!"

Przycisk: "START" (Wymagany do zainicjowania gry i odblokowania ewentualnego audio).

Instrukcja pod przyciskiem: "Przesuwaj w lewo/prawo (Swipe). Omijaj przeszkody i odpowiadaj na pytania!"

2. Mechanika Zręcznościowa (Endless Runner):

Ekran jest podzielony na 3 pionowe tory (lanes). Postać znajduje się zawsze na jednym z nich.

Sterowanie: Przeciągnięcie palcem (Swipe w lewo/prawo) na mobile, strzałki na klawiaturze na desktopie.

Z góry ekranu w dół przemieszczają się losowe przeszkody (np. wózki bagażowe 🛒, barierki 🚧).

Kolizja: Zderzenie z przeszkodą powoduje odjęcie 1 życia (zaczynamy z 3 sercami ❤️ widocznymi w rogu ekranu). Ekran może lekko mignąć na czerwono.

3. Mechanika Quizu:

Co około 10 sekund faza zręcznościowa ulega wstrzymaniu (nowe przeszkody przestają się pojawiać).

Na górze ekranu (jako element UI) pojawia się okno z Pytaniem.

Z góry ekranu, na każdym z 3 torów, nadjeżdżają "Bramki" (lub kafelki) z odpowiedziami (A, B, C).

Gracz musi zmienić tor na ten z poprawną odpowiedzią.

Rozstrzygnięcie: Wjechanie w poprawną odpowiedź generuje efekt konfetti/dźwięk sukcesu i dodaje +1 do licznika poprawnych odpowiedzi. Wjechanie w złą odpowiedź odejmuje 1 życie.

4. Struktura Danych (Pytania):

Zbuduj logikę tak, by pytania znajdowały się w prostej tablicy obiektów w kodzie JS, abym mógł je łatwo edytować. Przykład formatu:

JavaScript
const quizQuestions = [
    { question: "Gdzie była nasza pierwsza randka?", options: ["W kinie", "Restauracja", "Spacer"], correctIndex: 1 },
    // ... i tak dalej
];
5. Warunki Końca Gry:

Przegrana (Game Over): Jeśli serca (życia) spadną do 0. Pojawia się ekran z napisem "Uciekł nam samolot!" i przyciskiem "Spróbuj ponownie" (resetuje grę, ale nie resetuje już zdobytych biletów/punktów, by nie frustrować gracza).

Wygrana (Sukces): Gdy gracz odpowie poprawnie na 5 pytań (lub na wszystkie z tablicy).

Gra (canvas) się zatrzymuje.

Pojawia się piękny ekran końcowy z wakacyjnym tłem.

Duży napis: "Udało się! Pakuj walizkę, lecimy do PORTUGALII! 🇵🇹❤️".

Najważniejszy element: Duży, estetyczny przycisk pobierania z tagiem HTML: <a href="twoj-plik.pkpass" download id="walletBtn">Odbierz Kartę Pokładową (Apple Wallet)</a>.

6. Styl i UI/UX:

Stylistyka lekka, pastelowe i ciepłe kolory (żółty, błękitny, jasny pomarańczowy).

Użyj nowoczesnych fontów sans-serif.

Całość zaimplementuj używając Vanilla JS, HTML i CSS. Nie używaj zewnętrznych frameworków do silnika gry. Kod powinien być podzielony strukturalnie, ale łatwy do wklejenia na prosty hosting.
