# ADR-001: Wybór bazy danych dla projektu "ShopEasy"

- **Status:** Zaakceptowana
- **Data:** 2025-01-15
- **Autorzy:** Jan Kowalski, Anna Nowak

---

## 1. Kontekst

Nasz projekt, platforma e-commerce "ShopEasy", wymaga bazy danych do przechowywania informacji o użytkownikach, produktach i zamówieniach.

**Kluczowe wymagania:**
- **Transakcyjność (ACID):** Niezbędna do poprawnego przetwarzania płatności i zamówień.
- **Relacyjność danych:** Dane w naszym systemie są silnie powiązane (użytkownik ma zamówienia, zamówienie ma produkty).
- **Wyszukiwanie pełnotekstowe:** Użytkownicy muszą mieć możliwość wyszukiwania produktów po nazwie i opisie.
- **Umiejętności zespołu:** Zespół deweloperski ma doświadczenie w pracy z relacyjnymi bazami danych (SQL).

---

## 2. Rozważane opcje

### Opcja 1: PostgreSQL
Relacyjna baza danych o otwartym kodzie źródłowym, znana z niezawodności i zaawansowanych funkcji.

- **Zalety:**
  - [+] Pełne wsparcie dla transakcji ACID.
  - [+] Doskonale nadaje się do modelowania danych relacyjnych.
  - [+] Posiada wbudowane, zaawansowane mechanizmy wyszukiwania pełnotekstowego.
  - [+] Zespół zna tę technologię, co przyspieszy prace.
- **Wady:**
  - [-] Mniejsza elastyczność schematu w porównaniu do baz NoSQL.

### Opcja 2: MongoDB
Popularna, dokumentowa baza danych NoSQL, znana z elastyczności i skalowalności.

- **Zalety:**
  - [+] Elastyczny schemat ułatwia wprowadzanie zmian.
  - [+] Dobra wydajność przy odczycie danych.
- **Wady:**
  - [-] Bardziej skomplikowana obsługa transakcji, co jest ryzykowne przy przetwarzaniu płatności.
  - [-] Wymaga od zespołu nauki nowej technologii.
  - [-] Modelowanie danych relacyjnych jest mniej naturalne.

---

## 3. Decyzja

**Wybieramy PostgreSQL jako główną bazę danych dla naszego projektu.**

---

## 4. Uzasadnienie

PostgreSQL został wybrany, ponieważ:
1.  **Gwarantuje bezpieczeństwo transakcji:** Pełne wsparcie dla ACID jest kluczowe dla systemu e-commerce, gdzie przetwarzane są płatności.
2.  **Jest naturalnym wyborem dla naszych danych:** Struktura danych w projekcie jest silnie relacyjna, co idealnie pasuje do modelu SQL.
3.  **Wykorzystuje kompetencje zespołu:** Znajomość SQL w zespole pozwoli na szybsze rozpoczęcie i realizację projektu.
4.  **Oferuje wbudowane funkcje:** Posiada zaawansowane wyszukiwanie pełnotekstowe, co eliminuje potrzebę wdrażania dodatkowych narzędzi na wczesnym etapie projektu.

Chociaż MongoDB oferuje większą elastyczność, ryzyko związane z obsługą transakcji oraz konieczność nauki nowej technologii przeważyły na korzyść sprawdzonego i znanego zespołowi rozwiązania.

---

## 5. Konsekwencje

### Pozytywne
- Szybszy start i rozwój projektu.
- Wysoki poziom bezpieczeństwa i spójności danych.
- Łatwiejsze wdrożenie nowych członków zespołu dzięki popularności SQL.

### Negatywne
- Mniejsza elastyczność schematu będzie wymagała formalnego procesu migracji przy każdej zmianie w modelu danych.
- Przy bardzo dużej skali (setki tysięcy użytkowników) może być konieczne wdrożenie bardziej złożonych technik skalowania.
