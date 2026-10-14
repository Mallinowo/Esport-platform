# Event Storming - Przewodnik po warsztatach

## Czym jest Event Storming?

**Event Storming** to warsztatowa technika mapowania procesów biznesowych i odkrywania domeny problemu, stworzona przez **Alberto Brandoliniego**. To szybka, kolaboratywna metoda eksploracji złożonych domen biznesowych przy użyciu kolorowych karteczek samoprzylepnych.

### Kluczowe cechy

1.  **Szybka nauka:** Intensywne warsztaty pozwalają całemu zespołowi jednocześnie poznać domenę.
2.  **Wizualne modelowanie:** Kolorowe karteczki na dużej ścianie tworzą oś czasu zdarzeń, co pozwala każdemu zobaczyć cały system.
3.  **Wspólne odkrywanie:** Eksperci domenowi, programiści, przedstawiciele biznesu i projektanci pracują razem, co pozwala szybko ujawnić różnice w postrzeganiu systemu.
4.  **Koncentracja na zdarzeniach:** Skupienie na tym, "co się dzieje" (zdarzenia), a nie na tym, "co system ma" (encje). Zdarzenia domenowe to fakty, które miały miejsce.

### Kiedy używać Event Storming?

**Używaj, gdy:**
*   Rozpoczynaszn nowy projekt i musisz zrozumieć proces od początku do końca.
*   Próbujesz zrozumieć, jak działa istniejący, złożony system.
*   Chcesz poprawić komunikację między zespołem technicznym a ekspertami biznesowymi.
*   Chcesz zidentyfikować wąskie gardła i możliwości automatyzacji w istniejących procesach.
*   Planujesz podzielić duży, monolityczny system na mniejsze mikrousługi.

**Nie używaj, gdy:**
*   Projekt jest prosty (np. typowa aplikacja CRUD).
*   Pracujesz sam – to aktywność zespołowa.
*   Wszystkie wymagania są już sztywno ustalone.
*   W zespole brakuje eksperta domenowego.

## Przygotowanie do warsztatów

### Materiały

1.  **Przestrzeń:**
    *   **Fizyczna:** Duża, gładka ściana (4-8 metrów szerokości) lub rolka papieru. Potrzebujesz dużo miejsca, aby wszyscy mogli swobodnie stać i pracować.
    *   **Wirtualna:** Narzędzia takie jak Miro lub Mural, które oferują dużą przestrzeń roboczą i szablony do Event Stormingu.

2.  **Karteczki samoprzylepne:**
    *   **Pomarańczowe (zdarzenia domenowe):** Najważniejsze i najliczniejsze.
    *   **Niebieskie (polecenia):** Akcje inicjujące zdarzenia.
    *   **Żółte (aktorzy/persony):** Użytkownicy lub systemy wykonujące polecenia.
    *   **Różowe (gorące punkty):** Problemy, pytania, niejasności.
    *   **Inne kolory (opcjonalnie):** Fioletowe (polityki), zielone (modele odczytu), czerwone (systemy zewnętrzne).

3.  **Markery:** Grube, czarne markery, czytelne z daleka.

### Uczestnicy

1.  **Facylitator:** Neutralna osoba, która prowadzi warsztat, tłumaczy zasady, pilnuje czasu i zarządza dyskusją. Nie powinien to być właściciel produktu ani menedżer.
2.  **Eksperci domenowi:** Osoby, które znają proces biznesowy od podszewki (np. analitycy biznesowi, menedżerowie produktu, pracownicy wsparcia klienta).
3.  **Programiści:** Cały zespół deweloperski, który będzie implementować system. Zadają pytania techniczne i identyfikują ograniczenia.
4.  **Opcjonalnie:** Projektanci UX/UI, testerzy.

**Idealna wielkość grupy to 6-12 osób.**

## Etapy Event Storming

### Faza 1: Chaotyczna eksploracja

**Cel:** Wypisanie na pomarańczowych karteczkach wszystkich zdarzeń domenowych, jakie przychodzą uczestnikom do głowy. Na tym etapie chaos jest pożądany.

**Proces:**
1.  **Wprowadzenie:** Facylitator wyjaśnia zasady: zdarzenia zapisujemy w czasie przeszłym (np. "Zamówienie złożone"), a karteczki przyklejamy w dowolnym miejscu.
2.  **Cicha burza mózgów:** Uczestnicy w ciszy zapisują zdarzenia i przyklejają je na ścianie.
3.  **Dyskusja i rozszerzanie:** Facylitator zadaje pytania, aby odkryć więcej zdarzeń, w tym przypadki brzegowe i ścieżki błędów (np. "Co się stanie, jeśli płatność się nie powiedzie?").

### Faza 2: Wymuszanie osi czasu

**Cel:** Uporządkowanie chaotycznie rozrzuconych zdarzeń w logiczną oś czasu, od lewej do prawej.

**Proces:**
1.  **Znajdź początek i koniec:** Zespół wspólnie decyduje, które zdarzenie rozpoczyna, a które kończy proces.
2.  **Sortowanie:** Uczestnicy wspólnie układają pozostałe karteczki w porządku chronologicznym. W trakcie usuwane są duplikaty i dodawane brakujące zdarzenia.
3.  **Identyfikacja ścieżek (opcjonalnie):** Jeśli procesy przebiegają równolegle, można je ułożyć w osobnych poziomych torach (swimlanes), np. "Akcje użytkownika", "Przetwarzanie płatności".

### Faza 3: Odwrócona narracja

**Cel:** Weryfikacja osi czasu poprzez opowiadanie historii od końca do początku.

**Proces:** Zaczynając od ostatniego zdarzenia, narrator (ekspert domenowy) cofa się krok po kroku, zadając pytanie "Jak do tego doszło?". Ta technika często ujawnia ukryte założenia i brakujące kroki, które zostały pominięte w narracji "do przodu".

### Faza 4: Polecenia i aktorzy

**Cel:** Dodanie informacji o tym, co wywołuje zdarzenia (polecenia) i kto je inicjuje (aktorzy).

**Proces:**
1.  **Dodaj polecenia (niebieskie karteczki):** Przed każdym zdarzeniem umieszczana jest karteczka z poleceniem w trybie rozkazującym (np. "Złóż zamówienie" → "Zamówienie złożone").
2.  **Dodaj aktorów (żółte karteczki):** Nad każdym poleceniem umieszczana jest karteczka z nazwą aktora – osoby lub systemu (np. "Klient", "System płatności").

### Faza 5: Agregaty i konteksty ograniczone

**Cel:** Zgrupowanie powiązanych zdarzeń w agregaty i zidentyfikowanie granic między różnymi częściami systemu (konteksty ograniczone).

**Proces:**
1.  **Identyfikuj agregaty:** Zdarzenia dotyczące tego samego obiektu (np. "Zamówienie") są grupowane razem. Agregat reprezentuje spójną całość, która zarządza swoim stanem.
2.  **Identyfikuj konteksty ograniczone:** Agregaty, które współdziałają i używają wspólnego języka, są grupowane w konteksty. Każdy kontekst oprogramowania to potencjalny kandydat na osobną mikrousługę.

### Faza 6: Gorące punkty (Hotspots)

**Cel:** Identyfikacja problemów, pytań, ryzyka i możliwości usprawnień.

**Proces:** Uczestnicy oznaczają niejasne lub problematyczne miejsca na osi czasu za pomocą **różowych karteczek**. Mogą to być pytania do eksperta, konflikty w zespole, ryzyka techniczne lub pomysły na nowe funkcjonalności. Na koniec "gorące punkty" są priorytetyzowane, a najważniejsze z nich stają się zadaniami do wykonania.

## Rezultaty

Po warsztacie Event Storming zespół powinien dysponować:

*   **Wizualną mapą procesów:** Zdjęcia ściany lub link do tablicy w Miro.
*   **Listą zdarzeń domenowych:** Spis wszystkich zidentyfikowanych zdarzeń.
*   **Mapą kontekstów ograniczonych:** Diagram pokazujący granice między częściami systemu, co jest podstawą do projektowania architektury (np. mikrousług).
*   **Listą "gorących punktów" i zadań do wykonania:** Konkretne problemy do rozwiązania i pomysły do wdrożenia.
*   **Słownikiem wspólnego języka (Ubiquitous Language):** Zestaw terminów zrozumiałych zarówno dla biznesu, jak i dla programistów.

## Wskazówki praktyczne

*   **Zapraszaj właściwych ludzi:** Kluczowa jest obecność ekspertów domenowych i całego zespołu deweloperskiego.
*   **Przygotuj przestrzeń:** Upewnij się, że masz wystarczająco dużo miejsca i materiałów.
*   **Pilnuj czasu:** Facylitator musi rygorystycznie zarządzać czasem, aby warsztat był produktywny.
*   **Dokumentuj na bieżąco:** Rób zdjęcia, notatki i od razu twórz zadania w systemie (np. Jira).
*   **Świętuj odkrycia:** Pozytywna atmosfera i docenianie wkładu uczestników zwiększają zaangażowanie.
*   **W przypadku pracy zdalnej:** Używaj narzędzi takich jak Miro i zadbaj o dobrą organizację wirtualnej przestrzeni oraz częste przerwy.

---

**Pamiętaj:** Event Storming to narzędzie **odkrywania**, a nie tworzenia formalnej dokumentacji. Celem jest zbudowanie wspólnego zrozumienia domeny. Akceptuj chaos, zadawaj pytania i słuchaj różnych perspektyw – najlepsze odkrycia rodzą się z dyskusji i konstruktywnych konfliktów.

## Polecane materiały

*   [EventStorming](https://www.eventstorming.com/)
*   [Miro - Event Storming Template](https://miro.com/templates/event-storming/) - Praktyczny przewodnik i gotowy szablon do przeprowadzenia warsztatu online w Miro.
*   [Boiling Frogs 2018 - Mariusz Gil - Discovering unknown domain with Event Storming](https://www.youtube.com/watch?v=dhoXYRqghws)
*   [Event Storming jako narzędzie znajdowania granic kontekstów - Rafał Szymański](https://www.youtube.com/watch?v=U5tI48UpcfY) 
*   https://devstyle.pl/najobszerniejsze-wprowadzenie-do-event-stormingu-z-przykladem
*   https://devstyle.pl/process-level-event-storming
*   https://github.com/mariuszgil/awesome-eventstorming