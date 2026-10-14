# Przykładowy Plan Sprintu 1 - Projekt "ShopEasy"

- **Sprint:** #1
- **Okres:** [data rozpoczęcia] - [data zakończenia]
- **Zespół:** 3 deweloperów, Product Owner, Scrum Master

---

## Cel Sprintu (Sprint Goal)

> **Umożliwienie użytkownikom rejestracji, logowania i podstawowego zarządzania kontem, aby mogli rozpocząć korzystanie z aplikacji.**

### Kryteria sukcesu dla celu:
- Użytkownik może założyć konto za pomocą adresu e-mail.
- Użytkownik może zalogować się i wylogować.
- Użytkownik może edytować podstawowe dane w swoim profilu.

---

## Wybrane Historyjki Użytkownika (Backlog Sprintu)

Na podstawie priorytetów i pojemności zespołu, wybrano następujące historyjki do realizacji w tym sprincie.

### 1. US-001: Rejestracja użytkownika (8 SP) - **Priorytet: Wysoki**
- **Jako** nowy użytkownik, **chcę** zarejestrować konto, **aby** móc korzystać z aplikacji.
- **Kryteria akceptacji:**
  - [ ] Formularz rejestracji zawiera pola na e-mail, hasło i imię.
  - [ ] System waliduje poprawność adresu e-mail i siłę hasła.
  - [ ] Po rejestracji na podany adres e-mail wysyłana jest wiadomość z linkiem aktywacyjnym.
  - [ ] System obsługuje błędy (np. "Ten e-mail jest już zajęty").

### 2. US-002: Logowanie użytkownika (5 SP) - **Priorytet: Wysoki**
- **Jako** zarejestrowany użytkownik, **chcę** zalogować się za pomocą e-maila i hasła, **aby** uzyskać dostęp do mojego konta.
- **Kryteria akceptacji:**
  - [ ] Formularz logowania zawiera pola na e-mail i hasło.
  - [ ] Po poprawnym zalogowaniu użytkownik jest przekierowany do panelu głównego.
  - [ ] System obsługuje błędy (np. "Nieprawidłowy e-mail lub hasło").

### 3. US-003: Edycja profilu użytkownika (5 SP) - **Priorytet: Średni**
- **Jako** zalogowany użytkownik, **chcę** edytować dane w moim profilu, **aby** były one zawsze aktualne.
- **Kryteria akceptacji:**
  - [ ] Użytkownik ma dostęp do strony "Mój profil".
  - [ ] Możliwa jest zmiana imienia, nazwiska i adresu dostawy.
  - [ ] Zmiany są zapisywane po kliknięciu przycisku "Zapisz".

---

## Podsumowanie Planu

- **Łączna liczba Story Points:** 18
- **Pojemność zespołu (przewidywana):** ok. 20-25 SP
- **Status:** Plan realistyczny, w granicach możliwości zespołu.

---

## Definicja Ukończenia (Definition of Done) dla tego Sprintu

Historyjka użytkownika jest "ukończona", gdy:
- [ ] Spełnia wszystkie swoje kryteria akceptacji.
- [ ] Kod został sprawdzony i zatwierdzony w procesie `code review`.
- [ ] Zostały napisane i pomyślnie przechodzą testy jednostkowe.
- [ ] Funkcjonalność została wdrożona na środowisko testowe (staging).
- [ ] Product Owner zaakceptował jej działanie.

---

## Kluczowe Ryzyka

- **Ryzyko 1: Złożoność integracji z zewnętrznymi usługami (np. wysyłka e-maili).**
  - **Plan mitygacji:** Rozpoczęcie pracy od tych zadań, aby wcześnie zidentyfikować potencjalne problemy. W razie trudności, użycie tymczasowych rozwiązań (mocków).
- **Ryzyko 2: Niedoszacowanie zadań (pierwszy sprint).**
  - **Plan mitygacji:** Skupienie się na zadaniach o najwyższym priorytecie. Zadania o niższym priorytecie mogą zostać przeniesione do następnego sprintu, jeśli zabraknie czasu.

---

**Plan został zaakceptowany przez zespół i Product Ownera.**
