# Przewodnik po GitHub Projects

Ten przewodnik krok po kroku pomoże Ci uruchomić i efektywnie używać GitHub Projects do zarządzania zadaniami w Twoim projekcie studenckim.

https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects

## Czym jest GitHub Projects?

GitHub Projects to narzędzie do zarządzania projektami, zintegrowane bezpośrednio z Twoim repozytorium na GitHubie. Umożliwia tworzenie tablic Kanban, które pomagają wizualizować i śledzić postęp prac.

**Kluczowe cechy:**
- Tablice Kanban do zarządzania zadaniami.
- Pełna integracja z `Issues` (zgłoszeniami) i `Pull Requests`.
- Automatyzacje (np. automatyczne przenoszenie zadań do kolumny "Gotowe").
- Różne widoki: tablica, tabela, oś czasu (roadmapa).
- **W 100% darmowe** dla wszystkich typów repozytoriów.

Dla projektów studenckich jest to idealne rozwiązanie, ponieważ łączy zarządzanie zadaniami z kodem w jednym miejscu.

---

## Konfiguracja Krok po Kroku

### 1. Utwórz Projekt
1.  W swoim repozytorium na GitHubie przejdź do zakładki **"Projects"**.
2.  Kliknij **"New project"**.
3.  Wybierz szablon **"Board"**. To klasyczna tablica Kanban z kolumnami: `Todo`, `In Progress` i `Done`.
4.  Nazwij swój projekt (np. "NazwaProjektu Development") i ustaw widoczność na **"Private"**.

### 2. Skonfiguruj Kolumny
Dostosuj domyślne kolumny do przepływu pracy w Scrumie:
1.  Dodaj kolumnę **"Backlog"** na początku – będzie to miejsce na wszystkie zadania w projekcie.
2.  Dodaj kolumnę **"Review"** między `In Progress` a `Done` – na zadania, które czekają na `code review`.

Twój przepływ pracy (kolumny od lewej do prawej) powinien wyglądać tak:
**Backlog → Todo → In Progress → Review → Done**

### 3. Dodaj Zadania (Issues)
Każde zadanie na Twojej tablicy powinno być osobnym `Issue`.
1.  Przejdź do zakładki **"Issues"** w repozytorium i kliknij **"New issue"**.
2.  Stwórz `Issue` dla każdej historyjki użytkownika (User Story). Pamiętaj o dobrym opisie, zawierającym **kryteria akceptacji**.
3.  Używaj **etykiet (Labels)** do kategoryzacji zadań, np. `feature`, `bug`, `priority-high`, `epic-auth`.
4.  Wróć do tablicy projektu i w kolumnie **"Backlog"** kliknij **"+ Add item"**, aby dodać stworzone `Issues`.

### 4. Skonfiguruj Automatyzacje
Automatyzacje oszczędzają czas i utrzymują porządek na tablicy.
1.  Na tablicy projektu kliknij menu **"..."** i wybierz **"Workflows"**.
2.  Skonfiguruj następujące reguły:
    - Kiedy `Pull Request` jest otwierany → przenieś go do kolumny **"Review"**.
    - Kiedy `Pull Request` jest scalany (merged) → przenieś powiązane `Issue` do kolumny **"Done"**.
    - Kiedy `Issue` jest zamykane → przenieś je do kolumny **"Done"**.

---

## Codzienna Praca z GitHub Projects

### Przepływ Pracy Dewelopera
1.  **Rozpocznij pracę:** Przenieś zadanie z `Todo` do `In Progress` i przypisz je do siebie.
2.  **Twórz gałęzie (branches):** Używaj numeru `Issue` w nazwie gałęzi, np. `feature/login-#42`.
3.  **Commituj zmiany:** W wiadomościach commitów odwołuj się do numeru `Issue`, np. `git commit -m "Dodano formularz logowania #42"`.
4.  **Stwórz Pull Request:** Gdy skończysz, stwórz `Pull Request`. W opisie użyj słowa kluczowego `Closes #42`, aby automatycznie zamknąć `Issue` po scaleniu.
5.  **Code Review:** Twój `Pull Request` automatycznie pojawi się w kolumnie `Review`, gotowy do sprawdzenia przez innego członka zespołu.
6.  **Zakończ pracę:** Po scaleniu `Pull Requesta`, zadanie automatycznie trafi do kolumny `Done`.

---

## Dobre Praktyki

- **Jedno zadanie = jedno `Issue`:** Unikaj tworzenia "luźnych" notatek na tablicy. `Issues` mają historię, komentarze i można je śledzić.
- **Łącz `Pull Requests` z `Issues`:** Zawsze używaj słów kluczowych typu `Closes #numer`, aby zachować pełną śledzalność od zadania do kodu.
- **Aktualizuj tablicę codziennie:** Najlepiej podczas codziennych spotkań (Daily Standup). Tablica powinna być waszym "jedynym źródłem prawdy".
- **Używaj etykiet (Labels):** Pomagają w filtrowaniu i organizacji. Trzymaj się prostego zestawu: typ zadania, priorytet i epik.
- **Używaj kamieni milowych (Milestones) do planowania sprintów:** Jeden kamień milowy = jeden sprint.

---

## Podsumowanie

GitHub Projects to proste, darmowe i potężne narzędzie, idealne dla projektów studenckich. Jego największą zaletą jest natywna integracja z kodem, co pozwala utrzymać cały proces deweloperski w jednym miejscu.
