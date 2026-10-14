# Lista kontrolna: Start projektu

**Cel:** Przygotować zespół i infrastrukturę przed rozpoczęciem prac deweloperskich.

---

## 1. Konfiguracja zespołu

### Podział ról
- [ ] Wyznacz **Właściciela Produktu** (Product Owner) – osoba odpowiedzialna za wizję produktu i priorytetyzację zadań.
- [ ] Wyznacz **Scrum Mastera** – osoba wspierająca proces, facylitator, usuwający przeszkody w pracy zespołu.
- [ ] Zdefiniuj członków **Zespołu deweloperskiego** – deweloperzy, projektanci, testerzy.
- [ ] (Opcjonalnie) Wyznacz **Lidera technicznego** (Tech Lead), jeśli zespół jest liczny – osoba odpowiedzialna za kluczowe decyzje techniczne.

**Wskazówka:** W małych zespołach role mogą się pokrywać. Ważne, aby Właściciel Produktu był oddzielną rolą.

### Kanały komunikacji
- [ ] Stwórzcie przestrzeń roboczą na Slacku/Discordzie (lub w Microsoft Teams).
- [ ] Utwórzcie kanały komunikacji:
  - [ ] `#ogolny` – ogólne sprawy zespołu.
  - [ ] `#dewelopment` – dyskusje techniczne, przeglądy kodu (pull requests).
  - [ ] `#projektowanie` – makiety, opinie o doświadczeniu użytkownika (UX).
  - [ ] `#codzienne-spotkania` – codzienne aktualizacje statusu.
- [ ] Ustalcie stałą porę codziennych spotkań statusowych (stand-up).
- [ ] Określcie strefę czasową i godziny pracy, jeśli zespół pracuje zdalnie lub asynchronicznie.
- [ ] (Opcjonalnie) Skonfigurujcie narzędzia do tworzenia bazy wiedzy (np. Notion, Confluence).

**Wskazówka dla studentów:** Ustalcie, kiedy wszyscy członkowie zespołu są dostępni, nawet jeśli to tylko kilka wspólnych godzin dziennie.

### Zasady pracy w zespole
- [ ] Przedyskutujcie i zapiszcie zasady pracy w zespole:
  - [ ] Oczekiwany czas odpowiedzi na wiadomości.
  - [ ] Zasady obecności na spotkaniach.
  - [ ] Oczekiwany czas na przegląd kodu.
  - [ ] Definicja zadań "pilnych" i "ważnych".
- [ ] (Opcjonalnie) Ustalcie, jak będziecie rozwiązywać konflikty w zespole.

---

## 2. Konfiguracja narzędzi

### Kontrola wersji
- [ ] Stwórzcie repozytorium na GitHubie/GitLabie.
- [ ] Dodajcie wszystkich członków zespołu jako współpracowników.
- [ ] Skonfigurujcie ochronę głównej gałęzi (`main`/`master`):
  - [ ] Wymagajcie przeglądu kodu (`pull request`).
  - [ ] Wymagajcie, aby automatyczne testy i sprawdzenia zakończyły się sukcesem przed scaleniem.
  - [ ] (Opcjonalnie) Wymagajcie historii liniowej (bez commitów scalających).
- [ ] Skonfigurujcie plik `.gitignore` dla waszego stosu technologicznego (np. `node_modules`, `.env`).
- [ ] (Opcjonalnie) Ustalcie konwencję nazewnictwa gałęzi (np. `feature/*`, `bugfix/*`).

### Narzędzie do zarządzania projektem
- [ ] Wybierzcie narzędzie do zarządzania projektem (zobacz [Narzędzia PM](../docs/03-realizacja/narzedzia-pm.md)).
- [ ] Stwórzcie tablicę projektu z kolumnami:
  - [ ] **Rejestr (Backlog)** – wszystkie historyjki użytkownika.
  - [ ] **Do zrobienia** – zadania wybrane do obecnego sprintu.
  - [ ] **W toku** – aktywnie rozwijane zadania.
  - [ ] **Weryfikacja** – zadania w trakcie przeglądu kodu.
  - [ ] **Ukończone** – zadania scalone, wdrożone i zaakceptowane.
- [ ] (Opcjonalnie) Skonfigurujcie automatyzację (np. utworzenie `pull requesta` automatycznie przenosi zadanie do kolumny "Weryfikacja").
- [ ] (Opcjonalnie) Ustalcie limity pracy w toku (WIP).

**Wskazówka:** Darmowa wersja GitHub Projects jest wystarczająca dla większości projektów studenckich. Jest prosta i zintegrowana ze zgłoszeniami (issues) i `pull requestami`.

### Potok CI/CD (Ciągła Integracja / Ciągłe Dostarczanie)
- [ ] Skonfigurujcie podstawowy potok CI (np. GitHub Actions):
  - [ ] Automatyczne uruchamianie testów dla każdego `pull requesta`.
  - [ ] Automatyczne uruchamianie lintera (narzędzia do statycznej analizy kodu).
  - [ ] Automatyczne uruchamianie procesu budowania aplikacji.
- [ ] (Opcjonalnie) Skonfigurujcie raportowanie pokrycia kodu testami.
- [ ] (Opcjonalnie) Skonfigurujcie automatyczne wdrażanie na środowisko przejściowe (staging).

**Wskazówka:** Zacznijcie prosto – najpierw tylko testy, potem dodawajcie linter, budowanie i wdrożenie.

### Platforma dokumentacji
- [ ] Stwórzcie folder `docs/` w tym repozytorium w folderze `zaliczenie`.
- [ ] Wybierzcie generator stron statycznych (SSG) (zobacz [Generatory stron statycznych](../docs/04-dokumentacja/static-site-generators.md)).
- [ ] Stwórzcie podstawową strukturę dokumentacji:
  - [ ] `README.md` – ogólny opis projektu, instrukcje konfiguracji.
  - [ ] `CONTRIBUTING.md` – jak wnosić wkład w projekt (proces `pull request`, standardy kodowania).
  - [ ] `docs/architektura.md` – ogólny diagram architektury.
  - [ ] `docs/api.md` – dokumentacja API.
- [ ] (Opcjonalnie) Skonfigurujcie automatyczne wdrażanie dokumentacji (np. na GitHub Pages).

**Wskazówka:** W małym zespole dobrze napisany plik `README.md` i komentarze w kodzie mogą na początku wystarczyć.

---

## 3. Analiza i planowanie

### Zbieranie wymagań
- [ ] Przeprowadźcie wywiady z potencjalnymi użytkownikami (zobacz [Analiza wymagań](../docs/01-start-projektu/analiza-wymagań.md)).
- [ ] (Opcjonalnie) Przygotujcie ankietę dla użytkowników.
- [ ] Przeprowadźcie analizę konkurencji.
- [ ] Zdefiniujcie wymagania funkcjonalne (lista funkcji, np. "Użytkownik może zarejestrować konto przez e-mail").
- [ ] Zdefiniujcie wymagania niefunkcjonalne (np. wydajność, bezpieczeństwo, skalowalność, dostępność).

### Dokument wymagań produktu (PRD)
- [ ] Stwórzcie dokument wymagań produktu (PRD), który centralizuje wszystkie ustalenia. Powinien on zawierać:
  - [ ] **Cel projektu:** Jaki problem rozwiązujecie i dla kogo?
  - [ ] **Kluczowe funkcje:** Opis najważniejszych funkcji i ich działania.
  - [ ] **Persony użytkowników:** Do kogo kierowany jest produkt.
  - [ ] **Wymagania niefunkcjonalne:** Kwestie takie jak wydajność, bezpieczeństwo, wygląd.
  - [ ] **Makiety i przepływy użytkownika (User Flows):** Wizualne przedstawienie działania produktu.

**Wskazówka:** PRD jest "pojedynczym źródłem prawdy" o produkcie. Pomaga to utrzymać spójność wizji w całym zespole. Historyjki użytkownika często wynikają bezpośrednio z funkcji opisanych w PRD.

### Definiowanie person
- [ ] Stwórzcie 3-5 person (zobacz [Definiowanie person](../docs/01-start-projektu/definiowanie-person.md)).
- [ ] Dla każdej persony zdefiniujcie:
  - [ ] Dane demograficzne.
  - [ ] Cele i motywacje.
  - [ ] Problemy i potrzeby.
  - [ ] Wzorce zachowań.
- [ ] Użyjcie [Szablonu persony](../templates/01-personas-template.md).
- [ ] Udostępnijcie persony zespołowi i przeprowadźcie sesję przeglądową.

**Wskazówka:** Persony muszą opierać się na badaniach (np. wywiadach), a nie na założeniach.

### Przeprowadzenie sesji Event Stormingu

### Tworzenie historyjek użytkownika
- [ ] Napiszcie wstępne historyjki użytkownika (zobacz [Przewodnik po historyjkach użytkownika](../docs/01-start-projektu/user-stories.md)).
  - [ ] Stosujcie format: "Jako [persona], chcę [wykonać akcję], aby [osiągnąć korzyść]".
- [ ] Dla każdej historyjki sprawdźcie kryteria INVEST (niezależna, negocjowalna, wartościowa, oszacowalna, mała, testowalna).
- [ ] Dodajcie kryteria akceptacji (np. w formacie Given-When-Then).
- [ ] Użyjcie [Szablonu historyjki użytkownika](../templates/02-user-story-template.md).
- [ ] Pogrupujcie powiązane historyjki w większe jednostki (Epiki).

---

## 4. Rejestr produktu i szacowanie

### Tworzenie rejestru produktu (Product Backlog)
- [ ] Zaimportujcie wszystkie historyjki użytkownika do narzędzia do zarządzania projektem.
- [ ] Ustalcie priorytety dla każdej historyjki, np. metodą MoSCoW:
  - [ ] **Must Have** (Niezbędne) – kluczowe dla MVP (minimalnie satysfakcjonującego produktu).
  - [ ] **Should Have** (Wskazane) – ważne, ale nie blokujące wydania.
  - [ ] **Could Have** (Możliwe) – miły dodatek, jeśli starczy czasu.
  - [ ] **Won't Have** (Nie będzie) – poza zakresem obecnej wersji.
- [ ] Zdefiniujcie zakres MVP (tylko historyjki "Must Have").
- [ ] Uporządkujcie rejestr produktu według priorytetów.

**Wskazówka:** MVP to nie "wersja z połową funkcji", ale "najprostszy produkt, który rozwiązuje główny problem użytkownika".

### Szacowanie historyjek
- [ ] Przeprowadźcie sesję pokerowego planowania (cały zespół).
- [ ] Używajcie punktów historyjek (story points) do oceny względnego wysiłku.
- [ ] Oszacujcie najważniejsze historyjki.
- [ ] Zidentyfikujcie ryzykowne historyjki (np. o dużej niepewności) i oznaczcie je jako zadania badawcze (SPIKE), jeśli wymagają dodatkowej analizy.

---

## 5. Architektura i stos technologiczny

### Decyzja o stosie technologicznym
- [ ] Zorganizujcie sesję burzy mózgów na temat opcji stosu technologicznego.
- [ ] Oceńcie opcje na podstawie:
  - [ ] Umiejętności zespołu.
  - [ ] Wymagań projektu.
  - [ ] Dostępności dokumentacji i wsparcia społeczności.
  - [ ] Kosztów (darmowe plany, środki dla studentów).
- [ ] Podejmijcie ostateczną decyzję (przez głosowanie lub decyzję lidera technicznego).

### Rejestr decyzji architektonicznych (ADR)
- [ ] Napiszcie ADR dla kluczowych decyzji (zobacz [Przewodnik po ADR](../docs/04-dokumentacja/adr-guide.md)), np.:
  - [ ] Wybór bazy danych.
  - [ ] Wybór frameworka front-endowego.
  - [ ] Strategia uwierzytelniania.
- [ ] Użyjcie [Szablonu ADR](../templates/06-adr-template.md).
- [ ] Przechowujcie ADR-y w folderze `docs/adr/`.

**Wskazówka:** ADR dokumentuje tylko kluczowe decyzje, które trudno później zmienić.

### Inicjalizacja projektu
- [ ] Zainicjujcie projekt (np. używając szablonu startowego `create-next-app`).
- [ ] Skonfigurujcie zależności (w `package.json`, `requirements.txt` itp.).
- [ ] Skonfigurujcie zmienne środowiskowe:
  - [ ] Stwórzcie plik `.env.example` (szablon bez danych wrażliwych).
  - [ ] Dodajcie `.env` do `.gitignore` (NIGDY nie commitujcie danych wrażliwych!).
  - [ ] Udokumentujcie wymagane zmienne w pliku `README.md`.
- [ ] Skonfigurujcie bazę danych (lokalnie i dla środowiska przejściowego).
- [ ] Sprawdźcie, czy projekt uruchamia się lokalnie u każdego członka zespołu.

**Wskazówka:** Każdy członek zespołu powinien być w stanie szybko uruchomić projekt lokalnie. Jeśli konfiguracja jest czasochłonna, zaktualizujcie `README.md` o instrukcje rozwiązywania problemów.

---

## 6. Definicja Ukończenia (Definition of Done)

### Definicja standardów jakości
- [ ] Zorganizujcie warsztaty zespołowe, aby zdefiniować kryteria ukończenia (zobacz [Szablon DoD](../templates/08-definition-of-done.md)).
- [ ] Zdefiniujcie DoD na poziomie **zadania** (np. kod napisany, testy przechodzą, przegląd kodu zrobiony, CI przechodzi).
- [ ] Zdefiniujcie DoD na poziomie **historyjki** (np. wszystkie kryteria akceptacji spełnione, wdrożone na środowisko przejściowe, zaakceptowane przez Właściciela Produktu).
- [ ] Zdefiniujcie DoD na poziomie **sprintu** (np. wszystkie historyjki ukończone, przeprowadzono przegląd i retrospektywę sprintu).
- [ ] Udostępnijcie DoD całemu zespołowi – wszyscy muszą się na niego zgodzić.

**Wskazówka:** Zacznijcie od prostej Definicji Ukończenia i rozwijajcie ją w miarę postępów. Lepiej mieć kilka zasad, których wszyscy przestrzegają, niż wiele, które są ignorowane.

---

## 7. Planowanie sprintu

### Sesja planowania sprintu
- [ ] Zorganizujcie spotkanie planistyczne:
  - [ ] **Część 1: Zdefiniujcie Cel Sprintu.** Przykład: "Użytkownik może założyć konto i zalogować się".
  - [ ] **Część 2: Wybierzcie historyjki do sprintu.** Określcie prędkość zespołu (na pierwszy sprint zachowawczo) i wybierzcie zadania, które realizują Cel Sprintu.
- [ ] Podzielcie każdą historyjkę na mniejsze zadania techniczne.
- [ ] Przydzielcie zadania członkom zespołu (najlepiej, aby każdy sam wybrał, co chce robić).

**Wskazówka:** Cel Sprintu to spójny cel, a nie tylko lista funkcji do zrobienia.

### Ustalenie harmonogramu sprintu
- [ ] Ustalcie długość sprintu (rekomendacja dla studentów: 2 tygodnie).
- [ ] Zaplanujcie ceremonie Scruma:
  - [ ] **Codzienny Stand-up:** Krótkie spotkanie statusowe.
  - [ ] **Przegląd Sprintu (Sprint Review):** Prezentacja ukończonych zadań i zbieranie opinii.
  - [ ] **Retrospektywa Sprintu (Sprint Retrospective):** Omówienie tego, co poszło dobrze, a co można poprawić.
