# Historyjki Użytkownika - Projekt Sklepu Internetowego

Przykładowe historyjki użytkownika dla projektu platformy e-commerce.

## Epik: Uwierzytelnianie i Zarządzanie Kontem

### US-001: Rejestracja użytkownika

**Jako** nowy użytkownik
**Chcę** zarejestrować konto za pomocą adresu e-mail lub konta Google/Facebook
**Aby** móc zamawiać produkty i śledzić historię zamówień

**Kryteria akceptacji:**
- Użytkownik może zarejestrować się przez e-mail i hasło.
- Użytkownik może zarejestrować się przez konto Google.
- Użytkownik może zarejestrować się przez konto Facebook.
- Adres e-mail jest weryfikowany przez link aktywacyjny.
- Hasło ma co najmniej 8 znaków, zawiera jedną cyfrę i jedną wielką literę.
- Po rejestracji użytkownik jest przekierowywany do samouczka.
- Walidacja zapewnia, że adres e-mail jest unikalny i ma poprawny format.

---

### US-002: Szybkie ponawianie zamówienia dla stałych klientów

**Jako** zapracowana osoba
**Chcę** szybko zamówić ponownie produkty, które regularnie kupuję
**Aby** zaoszczędzić czas

**Kryteria akceptacji:**
- Na pulpicie użytkownika widoczna jest sekcja "Twoje regularne zamówienia".
- System automatycznie wykrywa powtarzające się zakupy.
- Jeden przycisk "Zamów ponownie" dodaje wszystkie produkty do koszyka.
- Użytkownik może edytować ilości przed finalizacją zamówienia.
- Możliwość finalizacji zakupu jednym kliknięciem (z zapisaną kartą i adresem).
- Potwierdzenie zamówienia jest wysyłane SMS-em i e-mailem.

---

## Epik: Odkrywanie i Wyszukiwanie Produktów

### US-003: Zaawansowane filtrowanie produktów

**Jako** entuzjasta technologii
**Chcę** filtrować produkty po szczegółowych specyfikacjach technicznych
**Aby** znaleźć dokładnie to, czego potrzebuję

**Kryteria akceptacji:**
- Kategoria "Elektronika" posiada zaawansowane filtry (marka, specyfikacja, zakres cen).
- Dla klawiatur dostępne są filtry: typ przełączników, układ, podświetlenie, łączność.
- Dla monitorów dostępne są filtry: rozdzielczość, częstotliwość odświeżania, typ panelu, rozmiar.
- Filtry pozwalają na wielokrotny wybór (np. kilka marek jednocześnie).
- Przycisk "Wyczyść wszystkie filtry".
- Adres URL jest aktualizowany, aby można było udostępnić link z filtrami.
- Wyniki aktualizują się na żywo, bez przeładowania strony.

---

### US-004: Porównywanie produktów obok siebie

**Jako** osoba lubiąca analizować produkty
**Chcę** porównać od 2 do 4 produktów obok siebie (specyfikacje, cena, opinie)
**Aby** łatwiej podjąć decyzję zakupową

**Kryteria akceptacji:**
- Na liście produktów znajduje się pole wyboru "Porównaj" (maksymalnie 4 produkty).
- Przycisk "Porównaj wybrane" pojawia się po zaznaczeniu co najmniej dwóch produktów.
- Strona porównawcza przedstawia tabelę z danymi (specyfikacje, cena, ocena, liczba opinii).
- Różnice między produktami są podświetlone.
- Przycisk "Dodaj do koszyka" jest dostępny dla każdego produktu.
- Można dodawać i usuwać produkty z porównania.

---

## Epik: Finalizacja Zamówienia i Płatność

### US-005: Płatność za pobraniem

**Jako** osoba starsza, robiąca zakupy online
**Chcę** płacić za pobraniem (przy odbiorze paczki)
**Aby** nie musieć wpisywać danych karty w internecie i czuć się bezpieczniej

**Kryteria akceptacji:**
- Opcja "Płatność za pobraniem" jest dostępna przy finalizacji zamówienia.
- Obowiązuje limit na zamówienia (np. do 500 zł) w celu zapobiegania oszustwom.
- Informacja o dodatkowej opłacie za pobraniem jest widoczna.
- Potwierdzenie z numerem zamówienia jest wysyłane SMS-em.
- Kurier pobiera płatność (gotówką lub kartą).
- System oznacza zamówienie jako "Płatność przy odbiorze".

---

### US-006: Zakup jednym kliknięciem dla zalogowanych użytkowników

**Jako** zapracowana osoba
**Chcę** kupić produkt jednym kliknięciem, bez wypełniania formularzy
**Aby** zaoszczędzić czas

**Kryteria akceptacji:**
- Zalogowani użytkownicy widzą przycisk "Kup teraz" obok "Dodaj do koszyka".
- Kliknięcie "Kup teraz" używa domyślnego adresu, metody płatności i dostawy.
- Proces pomija koszyk i przechodzi bezpośrednio do potwierdzenia zamówienia.
- Wyświetlane jest potwierdzenie: "Zamówienie złożone! Dotrze jutro."
- W przypadku braku domyślnego adresu lub płatności, użytkownik jest przekierowywany do standardowego procesu finalizacji zakupu.

---

## Epik: Wsparcie Klienta i Pomoc

### US-007: Czat na żywo z konsultantem

**Jako** osoba, która potrzebuje pomocy
**Chcę** rozmawiać z prawdziwą osobą przez czat
**Aby** uzyskać pomoc, gdy czegoś nie rozumiem

**Kryteria akceptacji:**
- Przycisk "Pomoc" jest widoczny na każdej stronie.
- Kliknięcie otwiera okno czatu z opcjami "Czat z konsultantem" lub "FAQ".
- Czas oczekiwania na połączenie z konsultantem jest krótki w godzinach pracy.
- Konsultant ma wgląd w informacje o użytkowniku, aktualnie przeglądaną stronę i zawartość koszyka.
- Konsultant może pomóc w zakupie (np. dodać produkt do koszyka za klienta).
- Po zakończeniu rozmowy użytkownik otrzymuje e-mail z jej transkrypcją.

---

## Epik: Opinie i Dowód Społeczny

### US-008: Zweryfikowane opinie o zakupach

**Jako** osoba analizująca produkty
**Chcę** czytać tylko zweryfikowane opinie (od osób, które faktycznie kupiły produkt)
**Aby** uniknąć fałszywych recenzji

**Kryteria akceptacji:**
- Opinię może dodać tylko osoba, która kupiła dany produkt.
- Przy opinii widnieje oznaczenie "Zweryfikowany zakup".
- Dostępny jest filtr "Pokaż tylko zweryfikowane".
- Możliwość sortowania opinii według: najbardziej pomocnych, najnowszych, najwyższej/najniższej oceny.
- Opcja głosowania: "Czy ta opinia była pomocna? Tak/Nie".
- Możliwość dodawania zdjęć do opinii.
- E-mail z przypomnieniem o możliwości wystawienia opinii jest wysyłany 14 dni po dostawie.

---

## Epik: Doświadczenie Mobilne

### US-009: Responsywny projekt mobilny

**Jako** osoba często korzystająca z telefonu
**Chcę** wygodnie używać sklepu na telefonie
**Aby** robić zakupy w drodze lub podczas przerwy

**Kryteria akceptacji:**
- Projekt jest responsywny (dostosowuje się do urządzeń mobilnych, tabletów i komputerów).
- Na urządzeniach mobilnych układ jest jednokolumnowy, a przyciski są duże i łatwe do kliknięcia.
- Dostępna jest dolna nawigacja (Strona główna, Wyszukiwanie, Koszyk, Konto).
- Galeria zdjęć produktu obsługuje gest przesuwania na urządzeniach mobilnych.
- Wyszukiwarka oferuje autouzupełnianie.
- Czas ładowania strony jest krótki, nawet przy wolniejszym połączeniu internetowym.

---

## Epik: Dostępność

### US-010: Duże czcionki i wysoki kontrast

**Jako** osoba ze słabszym wzrokiem
**Chcę** bez problemu czytać tekst na stronie
**Aby** móc korzystać z platformy samodzielnie

**Kryteria akceptacji:**
- Domyślny rozmiar czcionki jest odpowiednio duży (minimum 16px).
- Przycisk "A+" w nagłówku powiększa czcionki.
- Dostępny jest tryb wysokiego kontrastu.
- Przyciski są wystarczająco duże, aby łatwo w nie trafić.
- Elementy interaktywne mają wyraźne wskaźniki fokusu dla nawigacji klawiaturą.
- Wszystkie obrazy mają tekst alternatywny.
- Strona jest zgodna ze standardami dostępności (np. WCAG 2.1 na poziomie AA).
