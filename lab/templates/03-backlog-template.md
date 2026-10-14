# Szablon Rejestru Produktu (Product Backlog)

## Opis

Ten szablon w formacie CSV służy do zarządzania historyjkami użytkownika (user stories) i zadaniami w projekcie. Możesz go otworzyć za pomocą dowolnego edytora arkuszy kalkulacyjnych, takiego jak Microsoft Excel, Google Sheets czy LibreOffice Calc.

## Struktura Kolumn

| Kolumna            | Opis                                   | Przykładowe wartości                                     |
|--------------------|----------------------------------------|----------------------------------------------------------|
| **ID**             | Unikalny identyfikator historyjki.     | `US-001`, `US-002`                                       |
| **Historyjka**     | Pełna treść historyjki użytkownika.    | `Jako [rola], chcę [wykonać akcję], aby [osiągnąć cel].` |
| **Priorytet**      | Ważność zadania.                       | `Wysoki`, `Średni`, `Niski`                              |
| **Estymacja (SP)** | Szacowany nakład pracy w Story Points. | `1, 2, 3, 5, 8, 13...` (ciąg Fibonacciego)               |
| **Status**         | Aktualny stan zadania.                 | `Do zrobienia`, `W trakcie`, `Gotowe`                    |

## Jak używać?

1. **Otwórz plik** w swoim ulubionym programie do arkuszy kalkulacyjnych.
2. **Dostosuj go** do potrzeb swojego projektu, usuwając przykładowe dane i dodając własne historyjki.
3. **Zapisz plik** w formacie `.xlsx` (Excel) lub `.csv` (zalecane do pracy z Gitem), albo zaimportuj go do Google Sheets.

## Dobre praktyki

### Priorytety

- **Wysoki:** Kluczowe funkcjonalności, bez których produkt nie może działać.
- **Średni:** Ważne funkcjonalności, ale nie blokujące.
- **Niski:** Funkcjonalności typu "nice-to-have", które można zrealizować później.

### Estymacja w Story Points

Story Points odzwierciedlają złożoność zadania, a nie czas jego wykonania.
- **1-2 SP:** Proste zadanie.
- **3-5 SP:** Zadanie o średniej złożoności.
- **8 SP:** Złożone zadanie.
- **13+ SP:** Bardzo złożone zadanie – rozważ podzielenie go na mniejsze historyjki.

### Utrzymanie backlogu

- **Regularnie przeglądaj backlog:** Upewnij się, że priorytety są aktualne, a najważniejsze historyjki mają szczegółowe opisy i kryteria akceptacji.
- **Planuj sprinty:** Wybieraj zadania z backlogu do realizacji w nadchodzącym cyklu pracy.
- **Aktualizuj statusy:** Na bieżąco odzwierciedlaj postęp prac.

## Alternatywne narzędzia

Zamiast arkusza kalkulacyjnego, możesz używać dedykowanych narzędzi do zarządzania projektami, takich jak:
- **GitHub Projects:** Zintegrowane z repozytorium, idealne dla małych zespołów.
- **Jira:** Popularne w dużych projektach i korporacjach.
- **Trello:** Proste i wizualne zarządzanie zadaniami w formie tablic Kanban.
- **Notion:** Elastyczne narzędzie łączące dokumentację z zarządzaniem projektami.

---

**Wskazówka:** Backlog to żywy dokument. Regularnie go aktualizuj i dostosowuj do potrzeb swojego zespołu!
