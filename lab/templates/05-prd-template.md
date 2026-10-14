# Szablon Dokumentu Wymagań Produktu (PRD)

## Czym jest PRD?

Dokument Wymagań Produktu (PRD) to centralny dokument, który wyjaśnia, **co budujemy i dlaczego**. Służy jako "jedyne źródło prawdy" dla całego zespołu, definiując problem, który rozwiązujemy, cele projektu, jego zakres oraz sposób mierzenia sukcesu.

---

# PRD: [Nazwa produktu lub funkcjonalności]

- **Autor:** [Imię i nazwisko, rola np. Product Owner]
- **Data:** [RRRR-MM-DD]
- **Status:** [Szkic / W trakcie recenzji / Zatwierdzony]
- **Zespół:** [Lista kluczowych osób, np. Tech Lead, Design Lead]

---

## 1. Podsumowanie

[W 2-3 zdaniach opisz, czym jest ten produkt/funkcjonalność, jaki problem rozwiązuje i dla kogo jest przeznaczony.]

---

## 2. Opis Problemu

### Jaki problem rozwiązujemy?
[Szczegółowo opisz problem z perspektywy użytkownika. Dlaczego obecne rozwiązania są niewystarczające?]

### Dla kogo jest ten produkt?
[Wymień kluczowe persony użytkowników, których dotyczy ten problem. Możesz tu wstawić linki do pełnych opisów person.]

- **Główna persona:** [np. "Anna, studentka informatyki"]
- **Poboczne persony:** [np. "Marek, początkujący programista"]

---

## 3. Cele i Mierniki Sukcesu

### Cele projektu
[Co chcemy osiągnąć, tworząc ten produkt? Wymień 1-3 główne cele.]

- **Cel 1:** [np. "Ułatwienie studentom zarządzania notatkami z wykładów."]
- **Cel 2:** [np. "Zwiększenie efektywności nauki poprzez organizację materiałów."]

### Mierniki sukcesu
[Jak zmierzymy, czy osiągnęliśmy nasze cele? Podaj konkretne, mierzalne wskaźniki.]

- **Miernik 1:** [np. "Liczba aktywnych użytkowników tygodniowo (WAU) na poziomie 100."]
- **Miernik 2:** [np. "Średni czas tworzenia nowej notatki poniżej 30 sekund."]
- **Miernik 3:** [np. "Wskaźnik Net Promoter Score (NPS) powyżej 40."]

---

## 4. Wymagania i Zakres

### Kluczowe historyjki użytkownika
[Wymień najważniejsze historyjki użytkownika, które składają się na tę funkcjonalność. Możesz podać link do pełnego backlogu.]

- **US-001:** Jako student, chcę tworzyć notatki w formacie Markdown, aby łatwo formatować tekst.
- **US-002:** Jako student, chcę organizować notatki w folderach tematycznych, aby utrzymać porządek.

### Zakres projektu

**Co jest w zakresie (In Scope):**
[Wymień kluczowe funkcjonalności, które muszą znaleźć się w produkcie.]
- Tworzenie i edycja notatek.
- Organizacja notatek w foldery.
- Wyszukiwarka pełnotekstowa.

**Co jest poza zakresem (Out of Scope):**
[Wyraźnie określ, czego NIE będziecie budować w tej wersji. Pomaga to uniknąć "puchnięcia" projektu.]
- Współpraca w czasie rzeczywistym.
- Aplikacja mobilna.
- Integracja z kalendarzem.

---

## 5. Doświadczenie Użytkownika (UX) i Projekt Interfejsu (UI)

[Wstaw linki do makiet, prototypów lub projektów graficznych w narzędziach takich jak Figma. Możesz też opisać kluczowe przepływy użytkownika (user flows).]

- **Link do projektu w Figmie:** [wstaw link]
- **Kluczowy przepływ:** [np. "Rejestracja -> Stworzenie pierwszej notatki -> Organizacja w folderze"]

---

## 6. Kwestie Techniczne (opcjonalnie)

[Ogólny opis proponowanej architektury lub stosu technologicznego. Ta sekcja nie musi być szczegółowa.]

- **Stack technologiczny:** [np. "Frontend: React, Backend: Node.js, Baza danych: PostgreSQL"]
- **Integracje:** [np. "Logowanie przez konto Google"]

---

## 7. Otwarte Pytania i Ryzyka

[Lista pytań, które zespół musi jeszcze przedyskutować, oraz potencjalne ryzyka, które mogą wpłynąć na projekt.]

- **Otwarte pytanie:** [np. "Czy powinniśmy wspierać import notatek z innych aplikacji?"]
- **Ryzyko:** [np. "Ograniczone zasoby deweloperskie mogą opóźnić projekt."]
  - **Plan mitygacji:** [np. "Skupienie się wyłącznie na kluczowych funkcjonalnościach MVP."]
