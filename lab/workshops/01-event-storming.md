# Warsztat Event Storming: Przewodnik

## Wprowadzenie

Event Storming to interaktywny warsztat, który pomaga zespołom zrozumieć złożone procesy biznesowe poprzez wizualne mapowanie zdarzeń. Zamiast skupiać się na strukturach danych czy interfejsach, koncentrujemy się na tym, **co dzieje się w systemie** w czasie.

**Cel warsztatu:** Wspólne odkrycie i zrozumienie domeny biznesowej projektu (w tym przypadku: systemu bibliotecznego) poprzez identyfikację kluczowych zdarzeń, akcji i reguł.

---

## Legenda Kolorów

Podczas warsztatu używamy kolorowych karteczek, z których każda ma inne znaczenie:

- **Pomarańczowe (Zdarzenia Domenowe):** Najważniejsze! Opisują fakt, który już się wydarzył. Zawsze w czasie przeszłym (np. "Książka wypożyczona", "Rezerwacja anulowana").

- **Niebieskie (Polecenia):** Akcje, które inicjują zdarzenia (np. "Wypożycz książkę").

- **Żółte (Aktorzy):** Osoby lub systemy, które wykonują polecenia (np. "Czytelnik", "Bibliotekarz", "System").

- **Fioletowe (Reguły/Polityki):** Automatyczne procesy, które działają w tle (np. "Gdy minie termin zwrotu → Nalicz karę").

- **Zielone (Dane/Widoki):** Informacje potrzebne do podjęcia decyzji (np. "Widok dostępności egzemplarzy").

- **Czerwone (Systemy Zewnętrzne):** Inne systemy, z którymi nasza aplikacja się komunikuje (np. "System płatności").

- **Różowe (Pytania/Problemy):** Wszelkie wątpliwości i problemy do omówienia.

---

## Przebieg Warsztatu

### Faza 1: Chaotyczna Eksploracja (Burza Mózgów)
**Cel:** Zebranie jak największej liczby zdarzeń domenowych (pomarańczowe karteczki).

1.  **Cicha praca indywidualna:** Każdy uczestnik w ciszy wypisuje na pomarańczowych karteczkach wszystkie zdarzenia, jakie przychodzą mu do głowy. Nie martwcie się o kolejność – na tym etapie chaos jest pożądany.
2.  **Głośna dyskusja:** Zespół wspólnie przegląda dodane karteczki, zadaje pytania i dodaje kolejne zdarzenia. Moderator zadaje pytania pomocnicze, np. "Co dzieje się przed/po tym zdarzeniu?", "Co może pójść nie tak?".

### Faza 2: Uporządkowanie na Osi Czasu
**Cel:** Ułożenie zebranych zdarzeń w porządku chronologicznym.

1.  **Znajdź początek i koniec:** Zespół identyfikuje pierwsze i ostatnie zdarzenie w procesie.
2.  **Opowiedz historię:** Zespół wspólnie układa zdarzenia od lewej do prawej, tworząc logiczną opowieść o tym, jak działa system.
3.  **Odkryj alternatywne ścieżki:** Zidentyfikujcie różne scenariusze (np. co się dzieje, gdy książka jest dostępna, a co, gdy trzeba ją zarezerwować).

### Faza 3: Wzbogacanie Mapy
**Cel:** Dodanie kontekstu do mapy zdarzeń za pomocą innych kolorów karteczek.

1.  **Dodaj Polecenia (niebieskie):** Przed każdym zdarzeniem umieść karteczkę z akcją, która je wywołała.
2.  **Dodaj Aktorów (żółte):** Określ, kto wykonuje dane polecenie.
3.  **Dodaj Reguły (fioletowe):** Zidentyfikuj procesy, które dzieją się automatycznie.
4.  **Dodaj Pytania (różowe):** Jeśli pojawią się wątpliwości, zapisz je na różowej karteczce i umieść w "parkingu" do późniejszej dyskusji.

### Faza 4: Podsumowanie i Kolejne Kroki
**Cel:** Przegląd stworzonej mapy i zaplanowanie dalszych działań.

1.  **Przeanalizuj mapę:** Zidentyfikujcie główne procesy i "wąskie gardła".
2.  **Omów pytania:** Przedyskutujcie problemy z "parkingu".
3.  **Zdefiniuj granice kontekstów:** Pogrupujcie powiązane ze sobą zdarzenia w logiczne moduły (np. "Zarządzanie kontem", "Wypożyczenia", "Katalog"). Mogą one stać się podstawą architektury mikrousług lub modułów w monolicie.
4.  **Zaplanuj kolejne kroki:** Stworzona mapa jest doskonałą podstawą do tworzenia backlogu produktu, projektowania architektury i pisania dokumentacji.

---

## Wskazówki dla Moderatora

- **Bądź neutralny:** Twoim zadaniem jest prowadzenie warsztatu, a nie narzucanie własnych pomysłów.
- **Zadawaj otwarte pytania:** Prowokuj dyskusję i pomagaj zespołowi odkrywać nieznane obszary.
- **Pilnuj czasu:** Dbaj o to, aby warsztat przebiegał zgodnie z agendą.
- **Stwórz bezpieczną atmosferę:** Zachęcaj do zadawania pytań i pamiętaj o "Prime Directive" – nie ma głupich pomysłów, a każdy działa najlepiej, jak potrafi.

Event Storming to potężne narzędzie, które zamienia abstrakcyjne wymagania w wizualną, zrozumiałą dla wszystkich mapę. Powodzenia!
