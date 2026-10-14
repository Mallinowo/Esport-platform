# Przewodnik po Konfiguracji Jira

Ten przewodnik krok po kroku pomoże Ci uruchomić i efektywnie używać Jira do zarządzania projektem w metodyce Scrum.

https://www.atlassian.com/software/jira/guides/getting-started/introduction#what-is-jira-software

## Czym jest Jira?

Jira to profesjonalne narzędzie do zarządzania projektami, stworzone przez firmę Atlassian. Jest to standard branżowy, używany przez większość firm technologicznych na świecie.

**Kluczowe funkcje:**
- Zaawansowane tablice Scrum i Kanban.
- Potężne raporty (wykresy prędkości, spalania, przepływu).
- Integracja z innymi narzędziami, takimi jak Confluence (do dokumentacji) i GitHub.
- Możliwość zaawansowanej automatyzacji procesów.

Dla studentów, nauka Jiry to cenne doświadczenie, które przygotowuje do pracy w profesjonalnych zespołach deweloperskich.

---

## Plan Darmowy – Co Oferuje?

Jira oferuje w pełni funkcjonalny plan darmowy, idealny dla zespołów studenckich.

- **Użytkownicy:** Do 10 osób.
- **Projekty:** Nieograniczona liczba.
- **Funkcje:** Pełne wsparcie dla Scrum (sprinty, backlog, estymacje) i Kanban.
- **Raporty:** Dostęp do kluczowych raportów, takich jak wykres prędkości (velocity) i spalania (burndown).
- **Automatyzacja:** 100 darmowych wykonań reguł automatyzacji miesięcznie.
- **Integracje:** Możliwość połączenia z GitHubem, Slackiem i innymi narzędziami.

**Ograniczenia:** Limit 10 użytkowników i 2 GB na załączniki. Dla większości projektów studenckich jest to w zupełności wystarczające.

---

## Konfiguracja Krok po Kroku

### 1. Utwórz Przestrzeń Jira
1.  Przejdź na stronę [atlassian.com/software/jira/free](https://www.atlassian.com/software/jira/free) i zarejestruj darmowe konto.
2.  Podczas konfiguracji, nadaj swojej przestrzeni unikalną nazwę, np. `twojprojekt.atlassian.net`.
3.  Wybierz szablon projektu **"Scrum"**. Jest on idealny do pracy w sprintach.
4.  Nazwij swój projekt, np. "Rozwój Aplikacji ShopEasy".

### 2. Zaproś Zespół
1.  W ustawieniach projektu przejdź do sekcji **"People"** (Ludzie).
2.  Kliknij **"Invite people"** (Zaproś osoby) i wprowadź adresy e-mail członków swojego zespołu.
3.  Pamiętaj, że w planie darmowym możesz zaprosić maksymalnie 9 dodatkowych osób.

### 3. Skonfiguruj Tablicę
Domyślna tablica Scrum ma trzy kolumny: `To Do`, `In Progress`, `Done`. Warto ją rozbudować, aby lepiej odzwierciedlała proces deweloperski.
1.  W ustawieniach tablicy (`Board settings`) przejdź do sekcji **"Columns"**.
2.  Dodaj nowe kolumny, aby uzyskać następujący przepływ pracy:
    **Backlog → To Do → In Progress → Code Review → Testing → Done**

### 4. Dodaj Zadania (Issues)
1.  **Utwórz Epiki:** W widoku **"Backlog"** stwórz kilka Epików, czyli dużych grup funkcjonalności, np. "Uwierzytelnianie", "Katalog produktów", "Koszyk".
2.  **Dodaj Historyjki Użytkownika:** Kliknij przycisk **"+ Create"**, aby dodać zadania.
    - Wybierz typ zadania: **"Story"**.
    - Wpisz zwięzły tytuł, np. "Rejestracja użytkownika".
    - W opisie umieść pełną treść historyjki (`Jako... chcę... aby...`) oraz **kryteria akceptacji**.
    - Przypisz historyjkę do odpowiedniego Epiku.
    - Dodaj estymację w **Story Points**.

---

## Codzienna Praca i Planowanie Sprintów

### Planowanie Sprintu
1.  W widoku **"Backlog"** kliknij **"Create sprint"**.
2.  Przeciągnij zadania z backlogu do nowo utworzonego sprintu, aż osiągniesz pojemność zespołu (np. 20-25 Story Points).
3.  Ustal **Cel Sprintu** (Sprint Goal).
4.  Kliknij **"Start sprint"**.

### Codzienna Praca
- **Rozpocznij zadanie:** Przeciągnij kartę z `To Do` do `In Progress` i przypisz ją do siebie.
- **Aktualizuj status:** W miarę postępów przesuwaj kartę do kolejnych kolumn (`Code Review`, `Testing`).
- **Loguj pracę i komentuj:** Dodawaj komentarze o postępach lub napotkanych problemach.

---

## Śledzenie Postępów

Jira oferuje potężne narzędzia do monitorowania pracy zespołu. Najważniejsze z nich to:
- **Wykres Prędkości (Velocity Chart):** Pokazuje, ile Story Points zespół realizuje w każdym sprincie. Pomaga w planowaniu przyszłych sprintów.
- **Wykres Spalania (Burndown Chart):** Pokazuje, ile pracy pozostało do końca sprintu. Pomaga ocenić, czy zespół jest na dobrej drodze do osiągnięcia celu.
- **Raport Sprintu (Sprint Report):** Podsumowuje, które zadania zostały ukończone, a które nie.

---

## Dobre Praktyki

- **Pisz dobre historyjki użytkownika:** Każda powinna być niezależna, wartościowa, estymowalna, mała i testowalna (INVEST).
- **Używaj Story Points, a nie godzin:** Estymuj złożoność zadań, a nie czas ich wykonania.
- **Utrzymuj porządek w backlogu:** Regularnie go przeglądajcie i priorytetyzujcie.
- **Integruj Jirę z Gitem:** W wiadomościach commitów umieszczaj klucz zadania (np. `SHOP-42`), aby połączyć kod ze zgłoszeniem.

---

## Podsumowanie

Jira to zaawansowane narzędzie, którego nauka jest inwestycją w przyszłą karierę. Mimo że na początku może wydawać się skomplikowana, jej funkcje do zarządzania sprintami i raportowania znacząco ułatwiają pracę w zwinnych projektach. Dla zespołów studenckich, które chcą zdobyć profesjonalne doświadczenie, darmowy plan Jiry jest doskonałym wyborem.
