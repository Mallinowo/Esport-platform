# Przykładowy Backlog Produktu - Sklep Internetowy "ShopEasy"

Ten dokument przedstawia przykład backlogu dla fikcyjnego projektu sklepu internetowego. Zawiera on listę historyjek użytkownika, które reprezentują funkcjonalności do zaimplementowania.

**Uwaga:** Ten sam backlog jest dostępny w formacie `backlog.csv`, który można zaimportować do narzędzi takich jak Jira, Trello czy GitHub Projects.

---

## Legenda

- **Priorytet:**
  - **P0 (Must Have):** Funkcjonalności krytyczne, bez których produkt nie może istnieć.
  - **P1 (Should Have):** Ważne funkcjonalności, które powinny zostać zaimplementowane wkrótce po starcie.
  - **P2 (Could Have):** Funkcjonalności "nice-to-have", które można zrealizować w późniejszym czasie.
- **Status:**
  - **Do zrobienia:** Zaplanowane do realizacji w najbliższym czasie.
  - **W trakcie:** Aktualnie w implementacji.
  - **Ukończono:** Zaimplementowane i przetestowane.
  - **W backlogu:** Pomysły i zadania do późniejszej priorytetyzacji.
- **Estymacja:** Złożoność zadania w Story Points (np. 1, 2, 3, 5, 8...).

---

## Przykładowe Historyjki Użytkownika

### Epik: Uwierzytelnianie i Konto Użytkownika

| ID     | Tytuł                                     | Priorytet | Estymacja | Status       |
|--------|-------------------------------------------|-----------|-----------|--------------|
| US-001 | Rejestracja i logowanie użytkownika       | P0        | 8         | Ukończono    |
| US-012 | Resetowanie hasła przez email             | P1        | 3         | Ukończono    |
| US-014 | Edycja profilu użytkownika                | P1        | 3         | Do zrobienia |
| US-015 | Zarządzanie zapisanymi adresami dostawy   | P0        | 5         | Ukończono    |
| US-016 | Zarządzanie zapisanymi metodami płatności | P0        | 5         | W trakcie    |
| US-017 | Dostęp do historii zamówień               | P0        | 5         | Ukończono    |

### Epik: Wyszukiwanie i Przeglądanie Produktów

| ID     | Tytuł                                        | Priorytet | Estymacja | Status       |
|--------|----------------------------------------------|-----------|-----------|--------------|
| US-018 | Wyszukiwarka z autouzupełnianiem             | P0        | 8         | Ukończono    |
| US-003 | Zaawansowane filtrowanie produktów           | P1        | 8         | Do zrobienia |
| US-021 | Strona szczegółów produktu                   | P0        | 8         | Ukończono    |
| US-023 | Obsługa wariantów produktów (kolor, rozmiar) | P0        | 5         | Ukończono    |
| US-004 | Porównywanie produktów                       | P2        | 5         | W backlogu   |

### Epik: Proces Zakupowy (Koszyk i Płatność)

| ID     | Tytuł                                         | Priorytet | Estymacja | Status     |
|--------|-----------------------------------------------|-----------|-----------|------------|
| US-025 | Funkcjonalność koszyka (dodawanie, usuwanie)  | P0        | 5         | Ukończono  |
| US-006 | Zakup jednym kliknięciem (One-click checkout) | P1        | 8         | W trakcie  |
| US-030 | Integracja płatności kartą (Stripe)           | P0        | 8         | Ukończono  |
| US-031 | Integracja płatności PayPal                   | P1        | 5         | W trakcie  |
| US-032 | Integracja płatności BLIK                     | P1        | 8         | W backlogu |
| US-005 | Płatność za pobraniem                         | P1        | 5         | Ukończono  |
| US-029 | Email z potwierdzeniem zamówienia             | P0        | 3         | Ukończono  |

### Epik: Dostawa i Zwroty

| ID     | Tytuł                                  | Priorytet | Estymacja | Status       |
|--------|----------------------------------------|-----------|-----------|--------------|
| US-035 | Możliwość wyboru różnych metod dostawy | P0        | 5         | Ukończono    |
| US-033 | Śledzenie statusu zamówienia           | P0        | 5         | Ukończono    |
| US-034 | Powiadomienia SMS o statusie wysyłki   | P1        | 5         | Do zrobienia |
| US-036 | Możliwość zgłoszenia zwrotu produktu   | P1        | 8         | W backlogu   |

### Epik: Panel Administracyjny

| ID     | Tytuł                                 | Priorytet | Estymacja | Status       |
|--------|---------------------------------------|-----------|-----------|--------------|
| US-046 | Logowanie do panelu administracyjnego | P0        | 3         | Ukończono    |
| US-047 | Zarządzanie produktami                | P0        | 8         | Ukończono    |
| US-048 | Przeglądanie zamówień                 | P0        | 5         | Ukończono    |
| US-049 | Zarządzanie użytkownikami             | P1        | 5         | Do zrobienia |
| US-050 | Panel analityczny sprzedaży           | P1        | 13        | W backlogu   |

---

## Zarządzanie Backlogiem

- **Spotkania pielęgnacji backlogu (Backlog Refinement):** Regularnie przeglądaj i doprecyzowuj zadania, aby były gotowe do wzięcia na sprint.
- **Definicja Gotowości (Definition of Ready - DoR):** Ustalcie w zespole, jakie warunki musi spełniać historyjka, aby mogła zostać włączona do sprintu (np. musi mieć kryteria akceptacji i estymację).
- **Priorytetyzacja:** Używajcie prostych metod, takich jak MoSCoW (Must, Should, Could, Won't) lub numerycznych (P0, P1, P2), aby określić, co jest najważniejsze.

---

**Wskazówka:** Backlog jest dynamiczny. Jego zawartość i priorytety powinny być regularnie weryfikowane i dostosowywane do zmieniających się potrzeb projektu i informacji zwrotnych od użytkowników.
