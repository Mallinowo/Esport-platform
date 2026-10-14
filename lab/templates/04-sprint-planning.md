# Szablon Planowania Sprintu

## Czym jest Planowanie Sprintu?

Planowanie Sprintu to spotkanie na początku każdego sprintu, podczas którego zespół decyduje, co zostanie zrobione i jak zostanie to zrobione.

- **Część 1: Co robimy?** Zespół, w porozumieniu z Właścicielem Produktu, wybiera historyjki użytkownika z backlogu produktu.
- **Część 2: Jak to zrobimy?** Zespół dzieli wybrane historyjki na mniejsze zadania techniczne.

**Rezultat:** Ustalony **Cel Sprintu** i **Backlog Sprintu** (lista zadań do wykonania).

---

# Plan Sprintu nr [Numer Sprintu]

- **Data:** [RRRR-MM-DD]
- **Okres trwania:** [data początkowa] - [data końcowa]
- **Uczestnicy:** [Lista obecnych]

---

## 1. Cel Sprintu (Sprint Goal)

> [Jedno zwięzłe zdanie opisujące główny cel, który zespół chce osiągnąć w tym sprincie. Powinien on dostarczać spójną wartość. Na przykład: "Użytkownik może w pełni zarządzać swoim profilem, włączając w to edycję danych i zmianę zdjęcia."]

---

## 2. Wybrane Historyjki Użytkownika (Backlog Sprintu)

Poniżej znajduje się lista historyjek użytkownika, które zespół zobowiązuje się zrealizować w tym sprincie, aby osiągnąć Cel Sprintu.

### Historyjka 1: [ID] - [Tytuł]

- **Opis:** Jako [rola], chcę [wykonać akcję], aby [osiągnąć cel].
- **Priorytet:** [Wysoki/Średni/Niski]
- **Estymacja:** [X] Story Points
- **Kryteria akceptacji:**
  - [ ] [Warunek 1, który musi być spełniony]
  - [ ] [Warunek 2, który musi być spełniony]

---

### Historyjka 2: [ID] - [Tytuł]

- **Opis:** Jako [rola], chcę [wykonać akcję], aby [osiągnąć cel].
- **Priorytet:** [Wysoki/Średni/Niski]
- **Estymacja:** [X] Story Points
- **Kryteria akceptacji:**
  - [ ] [Warunek 1]
  - [ ] [Warunek 2]

---

*(... powtórz dla każdej kolejnej historyjki ...)*

### Podsumowanie

- **Łączna suma Story Points:** [Suma punktów z wybranych historyjek]
- **Pojemność zespołu (opcjonalnie):** [Historyczna średnia prędkość zespołu]

---

## 3. Podział na zadania (opcjonalnie)

Zespół może zdecydować o podziale historyjek na mniejsze, techniczne zadania.

### Zadania dla Historyjki 1: [Tytuł]

- [ ] Zadanie 1 (np. "Zaprojektowanie interfejsu formularza")
- [ ] Zadanie 2 (np. "Stworzenie endpointu API do zapisu danych")
- [ ] Zadanie 3 (np. "Implementacja formularza w aplikacji")
- [ ] Zadanie 4 (np. "Napisanie testów jednostkowych")

---

*(... powtórz dla każdej historyjki ...)*

## 4. Definicja Ukończenia (Definition of Done)

Historyjka jest uznana za "ukończoną", gdy spełnia następujące kryteria:
- [ ] Kod został napisany i działa zgodnie z kryteriami akceptacji.
- [ ] Testy jednostkowe i integracyjne zostały napisane i przechodzą pomyślnie.
- [ ] Kod został sprawdzony i zatwierdzony w procesie Code Review.
- [ ] Funkcjonalność została wdrożona na środowisko testowe.
- [ ] Właściciel Produktu zaakceptował działanie funkcjonalności.
- [ ] Dokumentacja została zaktualizowana (jeśli to konieczne).

---

## Jak używać tego szablonu?

1. **Przed spotkaniem:** Właściciel Produktu przygotowuje priorytety w backlogu. Zespół zapoznaje się z najważniejszymi zadaniami.
2. **Podczas spotkania:**
   - Ustalcie Cel Sprintu.
   - Wybierzcie historyjki, które pomogą go osiągnąć.
   - (Opcjonalnie) Podzielcie historyjki na mniejsze zadania.
3. **Po spotkaniu:** Przenieście zaplanowane zadania do narzędzia do zarządzania projektami (np. GitHub Projects, Jira) i rozpocznijcie pracę.
