# Słownik pojęć - zarządzanie projektami deweloperskimi

Słownik kluczowych terminów używanych w Agile, Scrum, Kanban i ogólnym zarządzaniu projektami deweloperskimi.

## A

### Kryteria akceptacji (Acceptance Criteria)
Zestaw warunków, które muszą być spełnione, aby historyjka użytkownika została uznana za ukończoną. Definiowane przez Właściciela Produktu.

**Przykład:**
```
Historyjka użytkownika: Jako użytkownik chcę się zalogować
Kryteria akceptacji:
- Logowanie działa z poprawnym email i hasłem
- Błędne dane pokazują komunikat błędu
- Po nieudanych próbach konto jest blokowane
```

### Zapis decyzji architektonicznych (ADR - Architecture Decision Record)
Dokument opisujący ważną decyzję architektoniczną: kontekst, rozważane opcje, wybraną opcję i konsekwencje.

### Metodyka zwinna (Agile)
Filozofia wytwarzania oprogramowania oparta na iteracyjnym dostarczaniu wartości, współpracy i adaptacji do zmian. Oparta na Manifeście Agile z 2001 roku.

**Dokumentacja:** https://agilemanifesto.org/

### Wytwór (Artifact)
Element dostarczający informację i przejrzystość. Trzy wytworzy w Scrum: Rejestr Produktu, Rejestr Sprintu, Przyrost.

## B

### Rejestr zadań (Backlog)
Uporządkowana lista pracy do wykonania. Może być Rejestr Produktu (cały produkt) lub Rejestr Sprintu (wybrany sprint).

### Doprecyzowanie rejestru (Backlog Grooming / Refinement)
Proces doprecyzowywania, szacowania i ustalania priorytetów elementów rejestru produktu.

### Przeszkoda (Blocker)
Przeszkoda uniemożliwiająca postęp pracy. Identyfikowana na Codziennym Scrum.

**Przykład:** "Nie mogę dokończyć API, bo czekam na dostęp do bazy danych"

### Wykres spalania (Burn-down Chart)
Wykres pokazujący pozostałą pracę w sprincie. Oś X: dni, Oś Y: pozostałe punkty. Pomaga monitorować postęp.

### Wykres narastania (Burn-up Chart)
Wykres pokazujący ukończoną pracę (rośnie w górę). Lepiej wizualizuje zmiany zakresu niż wykres spalania.

## C

### Wydarzenie (Ceremony)
Formalne wydarzenie w Scrum: Planowanie Sprintu, Codzienny Scrum, Przegląd Sprintu, Retrospektywa Sprintu. Każde ma określony cel i ograniczenie czasowe.

### Ciągła integracja / Ciągłe wdrażanie (CI/CD)
Praktyka automatycznego budowania, testowania i wdrażania kodu. Każdy commit prowadzi do automatycznego budowania, testów i wdrożenia.

**Dokumentacja:**
- https://github.com/resources/articles/ci-cd
- https://about.gitlab.com/topics/ci-cd/

### Przegląd kodu (Code Review)
Proces przeglądu kodu przez innych programistów przed scaleniem. Cel: jakość, znajomość kodu w zespole, wykrywanie błędów.

### Zespół wielofunkcyjny (Cross-functional Team)
Zespół posiadający wszystkie umiejętności potrzebne do dostarczenia przyrostu. Np. frontend, backend, tester, projektant UX.

### Czas cyklu (Cycle Time)
Czas od rozpoczęcia pracy nad zadaniem do jego ukończenia. Używany do optymalizacji procesu.

## D

### Codzienny Scrum (Daily Scrum / Daily Standup)
Codzienne spotkanie zespołu. Każdy odpowiada: co zrobiłem wczoraj, co zrobię dziś, jakie widzę przeszkody.

### Definicja ukończenia (Definition of Done - DoD)
Wspólne zrozumienie tego, co znaczy "ukończone". Lista warunków, które muszą być spełnione dla każdego przyrostu.

**Przykład:** Kod + testy + przegląd kodu + wdrożenie na środowisko testowe + akceptacja Właściciela Produktu

### Definicja gotowości (Definition of Ready - DoR)
Kryteria określające kiedy historyjka użytkownika jest gotowa do wzięcia do sprintu.

**Przykład:** Opis + kryteria akceptacji + szacowanie + projekt graficzny (jeśli dotyczy)

### Zespół Deweloperski (Development Team)
Zespół profesjonalistów wykonujących pracę dostarczenia przyrostu. Samoorganizujący się i wielofunkcyjny.

## E

### Epik (Epic)
Duża historyjka użytkownika, zbyt duża na jeden sprint. Musi być rozbita na mniejsze historyjki użytkownika.

**Przykład:** Epik "System płatności" → Historyjki: Dodaj kartę, Zapłać kartą, Historia płatności, Zwroty

### Szacowanie (Estimation)
Proces oceny rozmiaru lub złożoności pracy. Często używa się punktów historyjek (1, 2, 3, 5, 8, 13) lub rozmiarów (S, M, L, XL).

### Burza wydarzeń (Event Storming)
Warsztat eksploracji domeny biznesowej i projektowania systemu przy użyciu kolorowych karteczek.

## F

### Funkcjonalność (Feature)
Funkcjonalność produktu dostarczająca wartość użytkownikowi. Może składać się z kilku historyjek użytkownika.

### Ciąg Fibonacciego (Fibonacci Sequence)
Sekwencja liczb używana w szacowaniu (1, 2, 3, 5, 8, 13, 21). Większe odstępy dla większych liczb odzwierciedlają wyższą niepewność.

## I

### Przeszkoda (Impediment)
Synonim Blocker - przeszkoda w pracy zespołu.

### Przyrost (Increment)
Suma wszystkich elementów rejestru produktu ukończonych w sprincie plus wartość poprzednich przyrostów. Musi być "Ukończony" i potencjalnie możliwy do wydania.

### INVEST
Akronim dla dobrych historyjek użytkownika:
- **I**ndependent (niezależna)
- **N**egotiable (negocjowalna)
- **V**aluable (wartościowa)
- **E**stimable (możliwa do oszacowania)
- **S**mall (mała)
- **T**estable (testowalna)

### Iteracja (Iteration)
Synonim sprintu. Okres pracy ograniczony czasowo, kończący się dostarczeniem przyrostu.

## K

### Kanban
Metoda zarządzania pracą oparta na wizualizacji przepływu i ograniczeniu pracy w toku. Wywodzi się z Toyota Production System.

### Tablica Kanban (Kanban Board)
Tablica wizualizująca przepływ pracy. Kolumny reprezentują etapy (Do zrobienia, W trakcie, Ukończone), karty to zadania.

## L

### Czas realizacji (Lead Time)
Całkowity czas od utworzenia zadania do jego ukończenia. Używany do umów SLA i planowania.

**Formuła:** Czas realizacji = Data ukończenia - Data utworzenia

## M

### Minimalny Opłacalny Produkt (MVP - Minimum Viable Product)
Najmniejsza wersja produktu, która dostarcza wartość i pozwala zbierać informacje zwrotne od użytkowników.

### Programowanie grupowe (Mob Programming)
Cały zespół pracuje nad jednym zadaniem, przy jednym komputerze. Forma współpracy dobra dla trudnych problemów.

## P

### Programowanie parami (Pair Programming)
Dwie osoby programują przy jednym komputerze. Jedna pisze kod (kierowca), druga przegląda i nawiguje (nawigator). Rotacja co jakiś czas.

### Persona
Fikcyjna reprezentacja użytkownika produktu. Zawiera: imię, zdjęcie, cel, frustracje, kontekst techniczny.

**Przykład:** "Anna, 32 lata, kierownik projektu, używa laptopa, pracuje zdalnie, ceni prostotę"

### Poker planistyczny (Planning Poker)
Technika szacowania zespołowego. Każdy ma karty (1,2,3,5,8,13), szacuje jednocześnie, dyskusja przy rozbieżnościach.

### Dokument wymagań produktu (PRD - Product Requirements Document)
Dokument opisujący wymagania produktu: problem, cele, historyjki użytkownika, metryki sukcesu. Pisany przez Właściciela Produktu.

### Rejestr produktu (Product Backlog)
Uporządkowana lista wszystkiego, co może być potrzebne w produkcie. Zarządzana przez Właściciela Produktu.

### Właściciel Produktu (Product Owner - PO)
Rola odpowiedzialna za maksymalizację wartości produktu. Zarządza rejestrem produktu, komunikuje się z interesariuszami, akceptuje pracę.

## R

### Refaktoryzacja (Refactoring)
Restrukturyzacja kodu bez zmiany jego zachowania. Cel: czytelność, łatwość utrzymania, redukcja długu technicznego.

### Wydanie (Release)
Udostępnienie nowej wersji oprogramowania użytkownikom.

### Retrospektywa (Retrospective / Retro)
Wydarzenie na końcu sprintu, gdzie zespół reflektuje: co poszło dobrze, co źle, co poprawić. Cel: ciągłe doskonalenie.

### Mapa drogowa (Roadmap)
Plan rozwoju produktu na wyższym poziomie. Pokazuje główne funkcjonalności i kamienie milowe.

## S

### Scrum
Struktura zwinna oparta na iteracjach (Sprintach). Definiuje role (PO, SM, Zespół), wydarzenia i wytworzy.

### Mistrz Scruma (Scrum Master)
Rola odpowiedzialna za facylitację procesu, usuwanie przeszkód, wsparcie zespołu w Scrum. Przywódca służebny.

**Dokumentacja:** https://scrumguides.org/

### Scrumban
Hybryda Scrum i Kanban. Zazwyczaj: wydarzenia ze Scrum (retrospektywa, codzienny) plus tablica Kanban z limitami pracy w toku.

### Badanie (Spike)
Badanie lub prototypowanie ograniczone czasowo w celu zmniejszenia niepewności technicznej. Dostarcza wiedzę, nie kod produkcyjny.

**Przykład:** "Badanie: Sprawdzić czy biblioteka X obsługuje nasz przypadek użycia"

### Sprint
Iteracja ograniczona czasowo. Zawiera Planowanie Sprintu, Codzienne Scrumy, pracę, Przegląd Sprintu, Retrospektywę Sprintu.

### Rejestr sprintu (Sprint Backlog)
Zestaw elementów rejestru produktu wybranych do sprintu plus plan ich dostarczenia. Własność zespołu.

### Cel sprintu (Sprint Goal)
Cel sprintu. Daje kierunek i pozwala na elastyczność w szczegółach.

**Przykład:** "Umożliwić użytkownikom podstawowe zarządzanie kontem"

### Planowanie sprintu (Sprint Planning)
Wydarzenie rozpoczynające sprint. Zespół ustala: co zrobimy (cel sprintu i wybór historyjek) i jak to zrobimy (zadania).

### Przegląd sprintu (Sprint Review)
Wydarzenie kończące sprint. Prezentacja przyrostu dla interesariuszy, informacje zwrotne, adaptacja rejestru produktu.

### Retrospektywa sprintu (Sprint Retrospective)
Wydarzenie po Przeglądzie Sprintu. Zespół dyskutuje proces, identyfikuje ulepszenia, planuje 1-3 akcje na następny sprint.

### Interesariusz (Stakeholder)
Osoba zainteresowana produktem: klient, użytkownik, zarząd, inne zespoły. Uczestniczy w Przeglądzie Sprintu.

### Spotkanie statusowe (Standup)
Synonim Codziennego Scrum. Spotkanie na stojąco (wszyscy stoją), co zachęca do krótkości.

### Punkt historyjki (Story Point)
Względna jednostka szacowania złożoności historyjki użytkownika. Bazują na: złożoność, ilość pracy, niepewność.

**Przykład:** 1 punkt = bardzo proste, 13 punktów = bardzo złożone

## T

### Zadanie (Task)
Mała jednostka pracy, często techniczne rozbicie historyjki użytkownika. Np. "Stworzyć endpoint API", "Napisać testy jednostkowe".

### Dług techniczny (Technical Debt)
Skróty w kodzie, które przyspieszają teraz, ale spowalniają w przyszłości. Wymaga świadomego zarządzania i spłacania.

**Przykład:** Brak testów, skopiowany kod, rozwiązanie tymczasowe

### Przepustowość (Throughput)
Liczba zadań ukończonych w jednostce czasu. Używana do prognozowania i optymalizacji.

**Przykład:** 12 zadań/tydzień

### Ograniczenie czasowe (Time-box)
Ograniczenie czasowe dla wydarzenia. Nie można przekroczyć, ale można skończyć wcześniej.

## U

### Historyjka użytkownika (User Story)
Opis funkcjonalności z perspektywy użytkownika. Format: "Jako [kto] chcę [co] aby [po co]". Zawiera kryteria akceptacji.

**Przykład:**
```
Jako zalogowany użytkownik
Chcę edytować swój profil
Aby zaktualizować moje dane kontaktowe

Kryteria akceptacji:
- Mogę zmienić imię, nazwisko, email
- Email wymaga potwierdzenia
- Zmiany są zapisywane
```

## V

### Prędkość (Velocity)
Suma punktów historyjek ukończonych w sprincie. Używana do planowania przyszłych sprintów.

**Przykład:** Średnia prędkość 21 punktów → planujemy około 20 punktów na następny sprint

## W

### Model kaskadowy (Waterfall)
Tradycyjny model wytwarzania oprogramowania. Sekwencyjne fazy: Wymagania → Projekt → Implementacja → Testowanie → Wdrożenie.

### Praca w toku (WIP - Work In Progress)
Praca aktualnie wykonywana. Ograniczana limitami na każdej kolumnie w Kanban. Zasada: "Przestań zaczynać, zacznij kończyć".

**Przykład:** Limit "W trakcie" = 3 → maksymalnie 3 zadania jednocześnie

### Limit WIP (WIP Limit)
Maksymalna liczba zadań w danej kolumnie Kanban. Zmusza do skupienia, szybszego przepływu, wykrywania wąskich gardeł.

## Dodatkowe zasoby

**Więcej informacji:**
- [Wprowadzenie do zarządzania projektami](01-wprowadzenie.md)
- [Agile, Scrum i Kanban - szczegóły](02-agile-scrum-kanban.md)
- [Źródła wiedzy](zrodla.md)

**Oficjalne źródła:**
- Scrum Guide: https://scrumguides.org/
- Kanban Guide: https://www.atlassian.com/agile/kanban
- Agile Manifesto: https://agilemanifesto.org/

---

**Uwaga:** Definicje mogą się różnić między organizacjami. Ważne jest wspólne zrozumienie w zespole.
