# Przewodnik po estymacji w projektach deweloperskich

## Czym jest estymacja?

Estymacja to **przewidywanie wysiłku** potrzebnego do ukończenia zadania lub projektu. W kontekście tworzenia oprogramowania estymujemy historyjki użytkownika, epiki, a czasem pojedyncze zadania.

**Kluczowa kwestia:** Estymacja nie jest obietnicą ani gwarancją. To **najlepsze przewidywanie** w danym momencie, oparte na dostępnej wiedzy.

**Dlaczego estymacja jest trudna?**

1.  **Niepewność (Uncertainty)**
    *   Nieznane wymagania: "Czy klient dostarczy dokumentację API?"
    *   Ukryte zależności: "Okazało się, że musimy najpierw zmigrować bazę danych."
    *   Nieznane niewiadome: "Nie wiedzieliśmy, że ta biblioteka ma błąd w tym przypadku brzegowym."

2.  **Złożoność (Complexity)**
    *   Techniczna: Integracja z API firm trzecich.
    *   Logiki biznesowej: Skomplikowane reguły (np. system podatkowy).
    *   Integracyjna: Funkcjonalność dotyka pięciu różnych mikrousług.

3.  **Zmienność (Variability)**
    *   Różne doświadczenie w zespole: Młodszy programista kontra starszy programista.
    *   Przerwy: Spotkania, zmiana kontekstu, problemy na produkcji.
    *   Czynniki ludzkie: Motywacja, energia, zdrowie.

**Przykład:**
Historyjka: Integracja płatności Stripe.

*   **Starszy programista myśli:** "3 punkty" (zna Stripe, implementował to wielokrotnie, zna przypadki brzegowe).
*   **Młodszy programista myśli:** "13 punktów" (pierwszy raz pracuje ze Stripe, musi przeczytać dokumentację, testować w środowisku testowym).
*   **Rzeczywistość:** 8 punktów (średnia dla zespołu, uwzględniając przegląd kodu i testy).

## Dlaczego estymujemy?

### 1. Planowanie

**Planowanie sprintu:**
*   Prędkość zespołu: 25 punktów/sprint
*   Historyjki z góry rejestru produktu: 8 + 5 + 8 + 5 + 3 = 29 punktów
*   Decyzja: Zobowiązujemy się do 26 punktów (8+5+8+5), ostatnie 3 punkty to cel ambitny.

**Planowanie wydania:**
*   Epik: Nowy proces zakupowy = 80 punktów
*   Prędkość zespołu: 20 punktów/sprint
*   Estymacja: 80 / 20 = 4 sprinty.

### 2. Priorytetyzacja

**Obliczanie zwrotu z inwestycji (ROI):**
*   **Historyjka A:**
    *   Wartość: Wysoka (kluczowa funkcjonalność dla 80% użytkowników).
    *   Wysiłek: 3 punkty.
    *   ROI: Wysoka wartość / Niski wysiłek = Priorytet P0.
*   **Historyjka B:**
    *   Wartość: Średnia (miły dodatek dla 20% użytkowników).
    *   Wysiłek: 13 punktów.
    *   ROI: Średnia wartość / Wysoki wysiłek = Priorytet P3 (do zrobienia później).

**Decyzja:** Robimy Historyjkę A jako pierwszą (lepszy zwrot z inwestycji).

### 3. Śledzenie prędkości

**Prędkość (Velocity)** to suma punktów historyjek ukończonych w sprincie. Służy do:

*   **Przewidywalności:** "Zespół robi średnio 22 punkty na sprint."
*   **Planowania pojemności:** "W następnym sprincie mamy święto, więc nasza pojemność wyniesie około 15 punktów."
*   **Analizy trendów:** "Prędkość spada od trzech sprintów. Co się dzieje?"

**Przykład prędkości:**
*   Sprint 1: 18 punktów (kalibracja)
*   Sprint 2: 22 punkty (uczenie się)
*   Sprint 3: 21 punktów (stabilizacja)
*   Sprint 4: 20 punktów
*   Sprint 5: 23 punkty
*   Średnia: ~21 punktów/sprint (stabilnie).

### 4. Zarządzanie oczekiwaniami interesariuszy

Kierownictwo potrzebuje odpowiedzi na pytania:
*   "Kiedy funkcjonalność będzie gotowa?" → Estymacja + prędkość = przybliżony termin.
*   "Ile to będzie kosztować?" → Wysiłek (punkty) może być powiązany z kosztem.
*   "Czy zmieścimy się w terminie?" → Punkty epika / prędkość = czy to możliwe?

**Przykład:**
*   **CEO:** "Kiedy będzie nowy panel?"
*   **PM:** "Epik ma 60 punktów, nasza prędkość to 20 punktów, więc potrzebujemy około 3 sprintów."
*   **CEO:** "Możemy to przyspieszyć?"
*   **PM:** "Dodatkowy programista może zwiększyć prędkość, ale jego wdrożenie też zajmie czas."

**Bez estymacji:**
*   Chaos w planowaniu.
*   Nierealistyczne obietnice.
*   Brak danych do podejmowania decyzji biznesowych.

## Punkty historyjek (Story Points) vs. Zadania

### Porównanie

| Aspekt                         | Punkty historyjek                                            | Zadania                                                                |
|--------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| **Typ miary**                  | Względna (5 punktów to więcej niż 2 punkty)                  | Absolutna (konkretne, małe kroki)                                      |
| **Co mierzymy**                | Złożoność + Niepewność + Wysiłek                             | Konkretne czynności do wykonania                                       |
| **Specyfika zespołu**          | TAK (5 punktów dla Zespołu A ≠ 5 punktów dla Zespołu B)      | TAK (zadania definiowane przez zespół)                                 |
| **Stabilność**                 | Stabilne w czasie (złożoność zadania się nie zmienia)        | Zmienne (zadania mogą być różne dla tej samej historyjki)              |
| **Zróżnicowanie programistów** | Uwzględnione (zespół estymuje razem)                         | Problem (starszy programista może potrzebować mniej zadań niż młodszy) |
| **Niepewność**                 | Obsługiwana naturalnie (większa niepewność = więcej punktów) | Trudna do określenia (niepewność może oznaczać więcej zadań)           |
| **Manipulowanie systemem**     | Trudniejsze (punkty są względne i specyficzne dla zespołu)   | Łatwiejsze (można dodawać niepotrzebne zadania)                        |
| **Planowanie**                 | Długoterminowe (sprinty, wydania)                            | Krótkoterminowe (dzienne, tygodniowe)                                  |

### Punkty historyjek – szczegóły

**Co wpływa na punkty historyjek:**

1.  **Złożoność (Complexity)**
    *   Historyjka A: "Zmień tekst na przycisku" = 1 punkt (prosta zmiana w kodzie).
    *   Historyjka B: "Formularz wieloetapowy z walidacją i zapisem do 3 tabel" = 8 punktów (złożona logika, przypadki brzegowe, integracje).

2.  **Niepewność (Uncertainty)**
    *   Historyjka A: "Formularz logowania (robiliśmy to 10 razy)" = 3 punkty (zerowa niepewność, znana implementacja).
    *   Historyjka B: "Integracja z nowym API (brak dokumentacji, wersja beta)" = 13 punktów (wysoka niepewność, wiele niewiadomych).

3.  **Wysiłek (Effort)**
    *   Historyjka A: "Dodaj podpowiedź do jednego przycisku" = 1 punkt (mało pracy).
    *   Historyjka B: "Przeprojektowanie całego panelu (15 komponentów)" = 13 punktów (dużo pracy, nawet jeśli jest prosta).

**Kluczowe informacje:**
*   **Wymiarowanie względne:** 5 punktów nie oznacza konkretnego czasu, ale jest "bardziej złożone niż 2 punkty".
*   **Kalibracja zespołu:** Wartość punktów jest specyficzna dla danego zespołu.
*   **Punkty to nie czas:** Doświadczenie programisty nie zmienia punktów. Zadanie o złożoności 5 punktów pozostaje takie samo, niezależnie od tego, kto je wykonuje.

**Stabilność w czasie:**
Historyjka "Formularz logowania" ma 5 punktów. Nawet jeśli za rok zespół będzie w stanie zrobić ją szybciej, jej złożoność się nie zmieniła, więc nadal ma 5 punktów. Zmieni się prędkość zespołu (więcej punktów na sprint), ale punkty historyjek pozostaną stabilne.

### Zadania – kiedy ich używać

**1. Małe, konkretne czynności**
Zadania dla historyjki "Rejestracja użytkownika":
*   [ ] Backend: Model użytkownika
*   [ ] Backend: Logika walidacji
*   [ ] Frontend: Formularz rejestracji
*   [ ] Testy: Scenariusze rejestracji

Każde zadanie można śledzić osobno.

**2. Ograniczenie czasowe (Time-boxing)**
*   **Badanie:** Nowa biblioteka do wykresów.
*   **Limit:** Ustal, ile czasu chcesz poświęcić na badanie.
*   **Rezultat:** Porównanie możliwości bibliotek.

**Problem z używaniem jednostek czasu dla historyjek użytkownika:**

*   **Różnice w zespole:** Doświadczony programista wykona zadanie szybciej niż początkujący. Punkty historyjek rozwiązują ten problem, ponieważ zespół estymuje razem.
*   **Niepewność:** Trudno przewidzieć dokładny czas, gdy istnieje wiele niewiadomych. Punkty historyjek lepiej radzą sobie z niepewnością.
*   **Presja:** Łatwiej jest naciskać na zmniejszenie szacunków czasowych niż punktowych.

**Kiedy NIE używać jednostek czasu:**
*   Historyjki użytkownika → Użyj punktów historyjek.
*   Epiki → Użyj punktów historyjek.
*   Planowanie długoterminowe → Użyj punktów historyjek.

## Techniki estymacji

### A. Poker planistyczny (najpopularniejsza)

**Poker planistyczny** to zespołowa technika estymacji używająca kart z wartościami ciągu Fibonacciego.

#### Przygotowanie

**1. Karty:**
Używa się kart z wartościami: 0, 1, 2, 3, 5, 8, 13, 21, 40, 100, ?, "kawa"
*   **0:** Brak pracy (już zrobione lub banalne).
*   **1-3:** Małe zadania.
*   **5-8:** Średnie zadania.
*   **13:** Duże zadanie (rozważ podział).
*   **21+:** Epik (zdecydowanie do podziału).
*   **?:** Brak pomysłu (potrzeba więcej informacji).
*   **"kawa":** Potrzebna przerwa.

**2. Uczestnicy:**
*   **Właściciel produktu:** Prezentuje historyjkę, odpowiada na pytania.
*   **Zespół deweloperski:** Wszyscy programiści estymują.
*   **Opcjonalnie:** Tester, projektant.

#### Proces (krok po kroku)

**1. Prezentacja**
Właściciel produktu czyta historyjkę i jej kryteria akceptacji.
`"Jako użytkownik, chcę zresetować hasło przez e-mail, aby odzyskać dostęp, gdy je zapomnę."`

**2. Pytania i odpowiedzi**
Zespół zadaje pytania, aby wyjaśnić wątpliwości.
`"Czy mamy już skonfigurowaną usługę e-mail?"`
`"Czy stosujemy ograniczenie liczby zapytań?"`

**3. Wycena indywidualna**
Każdy programista po cichu wybiera kartę, która jego zdaniem najlepiej oddaje złożoność zadania.

**4. Odsłonięcie kart**
Wszyscy jednocześnie pokazują swoje karty.

**5. Dyskusja**
Jeśli są duże rozbieżności (np. 3 kontra 8), osoby z skrajnymi głosami wyjaśniają swoje rozumowanie.
`"Dlaczego 3?"`
`"Myślałem, że to proste, ale zapomniałem o obsłudze tokenów i bezpieczeństwie. Zgadzam się, że to bardziej złożone."`

**6. Ponowne głosowanie**
Zespół głosuje ponownie, dążąc do konsensusu.

**7. Zapisanie wyniku**
Wynik jest zapisywany w rejestrze produktu (np. w Jirze).

#### Dlaczego ciąg Fibonacciego?

Rosnące odstępy między liczbami w ciągu (1, 2, 3, 5, 8...) odzwierciedlają rosnącą niepewność przy większych zadaniach. Trudniej jest precyzyjnie oszacować duże zadanie, więc większe luki zmuszają do dyskusji, czy zadanie jest "średnie" (5) czy "duże" (8), zamiast tracić czas na spieranie się o 6 czy 7.

#### Wskazówki do pokera planistycznego

*   **Ograniczaj czas:** Ustal limit czasowy na jedną historyjkę, aby uniknąć paraliżu analitycznego.
*   **Unikaj kotwiczenia:** Odsłaniajcie karty jednocześnie, aby uniknąć sugerowania się głosami innych.
*   **Używaj historyjek referencyjnych:** Porównuj nowe historyjki do już oszacowanych.
*   **Dziel zadania:** Jeśli historyjka otrzymuje więcej niż 13 punktów, powinna zostać podzielona na mniejsze.

### B. Rozmiary koszulek (T-Shirt Sizes)

To prosta technika używająca rozmiarów: XS, S, M, L, XL.

#### Kiedy używać

*   Na wczesnym etapie projektu, gdy jest mało informacji.
*   Do szybkiej priorytetyzacji dużej liczby zadań.

#### Skala i mapowanie na punkty

Można przyjąć przybliżone mapowanie na punkty historyjek:
*   **XS** → 1 punkt
*   **S** → 3 punkty
*   **M** → 5 punktów
*   **L** → 8 punktów
*   **XL** → 13 punktów

#### Zalety i wady

*   **Zalety:** Szybka, intuicyjna, dobra do planowania na wysokim poziomie.
*   **Wady:** Niedokładna, trudna do śledzenia prędkości, wymaga późniejszej konwersji na punkty.

**Dobra praktyka:** Używaj rozmiarów koszulek do wstępnego, zgrubnego szacowania, a punktów historyjek do szczegółowej estymacji zadań o wysokim priorytecie.

### C. Inne techniki

*   **Głosowanie kropkowe (Dot Voting):** Szybka, wizualna technika do estymacji względnego wysiłku przez przyznawanie "kropek" (głosów). Dobra dla wielu małych zadań.
*   **System kubełkowy (Bucket System):** Sortowanie historyjek do predefiniowanych "kubełków" odpowiadających punktom. Skalowalna dla dużych rejestrów produktu.
*   **Mapowanie powinowactwa (Affinity Mapping):** Grupowanie podobnych zadań i estymowanie całych grup. Wspiera współpracę i budowanie wspólnego zrozumienia.
*   **Estymacja trzypunktowa (Three-Point Estimation):** Używa trzech scenariuszy (optymistyczny, najbardziej prawdopodobny, pesymistyczny) do obliczenia średniej ważonej. Przydatna dla zadań o wysokim ryzyku.

## Skala punktów historyjek – historyjki referencyjne

**Historyjki referencyjne** to przykłady zadań dla każdego poziomu skali Fibonacciego, które służą jako punkt odniesienia.

### Przykłady dla każdego poziomu

*   **1 punkt: Banalne**
    *   Zmiana tekstu na przycisku.
    *   Aktualizacja roku w stopce.
*   **2 punkty: Bardzo małe**
    *   Dodanie walidacji formatu e-mail w formularzu.
    *   Dodanie prostej podpowiedzi (tooltip).
*   **3 punkty: Małe**
    *   Formularz logowania z walidacją.
    *   Edycja profilu użytkownika (kilka pól).
*   **5 punktów: Średnie**
    *   Proces resetowania hasła przez e-mail.
    *   Koszyk na zakupy (dodawanie/usuwanie/aktualizacja).
*   **8 punktów: Duże**
    *   Integracja z logowaniem przez Google (OAuth).
    *   Katalog produktów z filtrami i paginacją.
*   **13 punktów: Bardzo duże**
    *   Kompletny proces zakupowy (koszyk → wysyłka → płatność → potwierdzenie).
    *   Panel administracyjny (zarządzanie użytkownikami, analityka).
    *   **Zalecenie:** Rozważ podział na mniejsze historyjki.
*   **20+ punktów: Epik (wymaga podziału)**
    *   To nie jest pojedyncza historyjka, ale epik, który musi być rozbity.
    *   Przykład: "Kompletny system uwierzytelniania", "Platforma e-commerce".

### Tworzenie własnych historyjek referencyjnych

1.  **Wybierzcie** kilka ukończonych historyjek, które dobrze reprezentują każdy poziom złożoności.
2.  **Udokumentujcie** je w dostępnym dla wszystkich miejscu (np. Confluence, Wiki).
3.  **Używajcie** ich podczas pokera planistycznego do porównań.
4.  **Aktualizujcie** listę okresowo, aby odzwierciedlała umiejętności i doświadczenie zespołu.

## Prędkość (Velocity)

### Definicja

**Prędkość** to suma punktów historyjek, które zespół ukończył (zgodnie z definicją ukończenia – Definition of Done) w jednym sprincie. Niedokończone historyjki nie wliczają się do prędkości.

### Jak używać prędkości

1.  **Planowanie sprintu (pojemność):** Na podstawie średniej prędkości z ostatnich sprintów zespół może określić, ile pracy jest w stanie podjąć w kolejnym.
2.  **Planowanie wydania (termin):** Dzieląc całkowitą liczbę punktów dla epika przez średnią prędkość, można oszacować, ile sprintów potrzeba na jego realizację.
3.  **Analiza trendów:** Monitorowanie prędkości pozwala zauważyć problemy. Spadająca prędkość może sygnalizować dług techniczny, częste przerwy lub inne przeszkody.

**Ważne:** Prędkość jest narzędziem do planowania dla zespołu, a nie wskaźnikiem jego wydajności. Porównywanie prędkości między różnymi zespołami jest błędem, ponieważ każdy zespół ma swoją unikalną skalę punktów.

## Reestymacja

Reestymacja powinna być wyjątkiem, a nie regułą.

### Kiedy reestymować?

*   **W trakcie sprintu:** Gdy odkryjesz coś, co drastycznie zmienia złożoność zadania (np. z 5 na 13 punktów).
*   **Podczas retrospektywy:** Gdy zespół systematycznie myli się w szacunkach, warto zrewidować historyjki referencyjne i skalę.
*   **Przy znacznej zmianie zakresu:** Gdy do historyjki dodawane są nowe, istotne wymagania.

### Kiedy NIE reestymować?

*   Przy drobnych korektach.
*   Ze względu na indywidualną szybkość programisty.
*   Po zakończeniu historyjki (lepiej wyciągnąć wnioski na przyszłość).

## Antywzorce w estymacji

*   **Wywieranie presji na niższe estymacje:** Prowadzi do nierealistycznych planów i wypalenia zespołu.
*   **Przeliczanie punktów na godziny przez menedżera:** Niszczy cel estymacji względnej i prowadzi do fałszywych obietnic.
*   **Indywidualna estymacja:** Powoduje brak zaangażowania zespołu i pomijanie ważnych perspektyw.
*   **Zbyt szczegółowa estymacja na wczesnym etapie:** Marnowanie czasu na zadania, które mogą nigdy nie być realizowane.
*   **Brak historyjek referencyjnych:** Prowadzi do niespójnych i powolnych estymacji.

## Dobre praktyki

1.  **Cały zespół estymuje:** Zapewnia to różnorodność perspektyw i wspólne zrozumienie.
2.  **Używajcie historyjek referencyjnych:** Zwiększa to spójność i szybkość estymacji.
3.  **Ograniczajcie czas na poker planistyczny:** Unikajcie paraliżu analitycznego.
4.  **Dzielcie duże historyjki (>13 punktów):** Zmniejsza to ryzyko i pozwala na szybsze dostarczanie wartości.
5.  **Śledźcie prędkość:** Umożliwia to bardziej przewidywalne planowanie.

## Estymacja dla różnych typów pracy

*   **Nowe funkcjonalności:** Używaj pokera planistycznego i punktów historyjek.
*   **Błędy:** Można je szacować w mniejszych jednostkach (np. jako małe/średnie/duże) lub w punktach, jeśli są złożone.
*   **Zadania badawcze (Spikes):** Używaj ograniczenia czasowego (time-box), aby skupić się na dostarczeniu odpowiedzi, a nie kodu.
*   **Dług techniczny:** Traktuj jak normalne historyjki i estymuj w punktach, ponieważ również zużywa pojemność zespołu.

## Estymacja w różnych kontekstach

*   **Startup:** Estymacja jest szybka i zgrubna (np. rozmiary koszulek). Szybkość jest ważniejsza niż precyzja.
*   **Korporacja:** Estymacja jest szczegółowa i ostrożna (np. poker planistyczny, estymacja trzypunktowa). Ważne jest zarządzanie ryzykiem i zgodnością.
*   **Projekt studencki:** Estymacja powinna uwzględniać czas na naukę i dokumentację. To świetna okazja do nauki kalibracji i współpracy w zespole.

---

**Pamiętaj:** Estymacja to narzędzie do planowania, a nie obietnica. Akceptuj niepewność, iteruj i ulepszaj proces. Celem nie są idealne estymacje, ale spójność i ciągłe uczenie się.
