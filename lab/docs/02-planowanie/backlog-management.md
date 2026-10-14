# Przewodnik po zarządzaniu rejestrem produktu (Product Backlog)

## Czym jest rejestr produktu?

Rejestr produktu (Product Backlog) to **uporządkowana lista wszystkiego, co może być potrzebne w produkcie**. Jest to "żyjący" dokument, który ewoluuje wraz z produktem i zmieniającymi się wymaganiami.

**Definicja:**
*   **Żyjący dokument:** Ciągle aktualizowany, nigdy "skończony".
*   **Jedyne źródło prawdy:** Jeden, autorytatywny rejestr dla całego zespołu.
*   **Uporządkowana lista:** Najważniejsze zadania na górze, mniej ważne na dole.
*   **Własność właściciela produktu:** Właściciel produktu (Product Owner) odpowiada za jego zawartość, kolejność i dostępność.

**Dlaczego jest ważny?**
*   **Przejrzystość:** Każdy wie, co jest w planach.
*   **Skupienie:** Zespół wie, co robić teraz, a co później.
*   **Elastyczność:** Możliwość zmiany priorytetów w odpowiedzi na opinie.
*   **Planowanie:** Podstawa do planowania sprintów.

**Cechy dobrego rejestru produktu (DEEP):**
*   **Odpowiednio szczegółowy (Detailed appropriately):** Zadania na górze listy są szczegółowe, a te na dole ogólne.
*   **Podatny na zmiany (Emergent):** Zmienia się w czasie (nowe pomysły, zmiana priorytetów).
*   **Oszacowany (Estimated):** Historyjki użytkownika mają przypisane punkty (przynajmniej te na górze listy).
*   **Uporządkowany według priorytetów (Prioritized):** Jasna kolejność oparta na wartości.

## Rejestr produktu vs. Rejestr sprintu

To dwa często mylone pojęcia. Kluczowa różnica to **zakres i ramy czasowe**.

| Aspekt            | Rejestr produktu                          | Rejestr sprintu                   |
|-------------------|-------------------------------------------|-----------------------------------|
| **Zakres**        | Wszystko, co może znaleźć się w produkcie | Tylko zadania na bieżący sprint   |
| **Ramy czasowe**  | Cały cykl życia produktu                  | Jeden sprint                      |
| **Właściciel**    | Właściciel produktu                       | Zespół deweloperski               |
| **Zmienność**     | Może się zmieniać w każdej chwili         | "Zamrożony" na czas sprintu       |
| **Szczegółowość** | Historyjki użytkownika                    | Zadania i historyjki              |
| **Priorytet**     | Uporządkowany od góry do dołu             | Wszystkie zadania są równie ważne |

## Elementy rejestru produktu

Rejestr produktu zawiera różne typy elementów, nie tylko historyjki użytkownika.

### 1. Historyjki użytkownika (User Stories)

**Co to:** Funkcjonalność opisana z perspektywy użytkownika.
**Format:**
`Jako [persona], chcę [wykonać akcję], aby [osiągnąć cel].`
**Kryteria akceptacji:**
*   [ ] Kryterium 1
*   [ ] Kryterium 2

### 2. Epiki (Epics)

**Co to:** Duża funkcjonalność, która wymaga rozbicia na mniejsze historyjki.
**Przykład:** "System uwierzytelniania użytkowników" może być epikiem składającym się z historyjek: "Rejestracja przez e-mail", "Logowanie", "Resetowanie hasła".

### 3. Zadania techniczne (Technical Tasks)

**Co to:** Zadania bez bezpośredniej wartości dla użytkownika, ale niezbędne dla działania systemu.
**Przykłady:** Migracja bazy danych, konfiguracja środowiska CI/CD, refaktoryzacja kodu.

### 4. Błędy (Bugs)

**Co to:** Defekty wymagające naprawy. Powinny być opisane krokami do odtworzenia i oczekiwanym zachowaniem.

### 5. Dług techniczny (Technical Debt)

**Co to:** Kod, który działa, ale wymaga poprawy jakości, wydajności lub bezpieczeństwa.

### 6. Zadania badawcze (Spikes)

**Co to:** Ograniczone czasowo zadania badawcze, mające na celu rozwiązanie niepewności technicznych. Wynikiem jest dokumentacja i rekomendacje, a nie kod produkcyjny.

## Struktura rejestru produktu

### Hierarchia: Epiki → Historyjki → Zadania

Dla przejrzystości warto grupować historyjki w ramach większych epików.

### Grupowanie i priorytetyzacja

Można stosować różne metody, np. grupowanie według epików, priorytetów (krytyczne, wysokie, średnie, niskie) lub metody MoSCoW. Najlepiej połączyć grupowanie według epików z porządkowaniem według priorytetów wewnątrz każdego z nich.

*   **Góra rejestru (Top of the Backlog):** Zadania na najbliższe 2-3 sprinty. Powinny być szczegółowo opisane, oszacowane i gotowe do podjęcia.
*   **Dół rejestru (Bottom of the Backlog):** Ogólne pomysły, które mogą nigdy nie zostać zrealizowane. Nie wymagają szczegółów ani estymacji.

## Techniki priorytetyzacji

### A. Metoda MoSCoW

*   **Must Have (Musi być):** Krytyczne funkcjonalności, bez których produkt nie zadziała.
*   **Should Have (Powinno być):** Ważne, ale nie krytyczne. Można je zrealizować w późniejszych iteracjach.
*   **Could Have (Może być):** "Miłe dodatki", które zostaną zrobione, jeśli starczy czasu.
*   **Won't Have (Nie będzie):** Funkcjonalności świadomie wykluczone z danego wydania.

### B. Macierz Wartość vs. Wysiłek (Value vs. Effort)

Zadania umieszcza się na macierzy 2x2, co pozwala zidentyfikować:
1.  **Szybkie wygrane (Quick Wins):** Wysoka wartość, niski wysiłek. **Rób je w pierwszej kolejności!**
2.  **Duże zakłady (Big Bets):** Wysoka wartość, wysoki wysiłek. Planuj je strategicznie.
3.  **Wypełniacze (Fill-ins):** Niska wartość, niski wysiłek. Rób, jeśli zostanie czas.
4.  **Pochłaniacze czasu (Time Sinks):** Niska wartość, wysoki wysiłek. **Unikaj ich!**

### C. Model RICE (Reach, Impact, Confidence, Effort)

Formuła do obliczania priorytetu: `(Zasięg × Wpływ × Pewność) / Wysiłek`. Wyższy wynik oznacza wyższy priorytet.
*   **Zasięg (Reach):** Ilu użytkowników dotknie zmiana?
*   **Wpływ (Impact):** Jak duży będzie wpływ na każdego użytkownika? (skala 0.25-3)
*   **Pewność (Confidence):** Jak pewni jesteśmy naszych szacunków? (skala 50-100%)
*   **Wysiłek (Effort):** Ile pracy to wymaga? (np. w osobomiesiącach lub punktach)

### D. Model Kano

Kategoryzuje funkcje na podstawie ich wpływu na satysfakcję użytkownika:
1.  **Podstawowe (Basic):** Oczekiwane przez użytkowników. Ich brak powoduje niezadowolenie, ale obecność jest neutralna.
2.  **Wydajnościowe (Performance):** Im więcej, tym lepiej (np. szybkość ładowania strony).
3.  **Zachwycające (Delight):** Niespodziewane dodatki, które wywołują efekt "wow".

## Pielęgnacja rejestru produktu (Backlog Grooming/Refinement)

To regularne spotkania zespołu w celu przeglądu i aktualizacji rejestru.

**Cele:**
*   Doprecyzowanie niejasnych historyjek.
*   Oszacowanie nowych zadań.
*   Podział dużych epików na mniejsze historyjki.
*   Zmiana priorytetów w odpowiedzi na nowe informacje.
*   Usunięcie nieaktualnych zadań.

**Format:**
*   **Częstotliwość:** 1-2 razy na sprint.
*   **Uczestnicy:** Właściciel produktu, zespół deweloperski, opcjonalnie inni interesariusze.
*   **Agenda:** Przegląd nowych zadań, estymacja, podział epików, zmiana priorytetów, czyszczenie.

**Wynik:** Rejestr produktu jest zawsze gotowy na kolejne sprinty, a zadania na jego szczycie spełniają **definicję gotowości (Definition of Ready)** – są jasne, oszacowane i wystarczająco małe.

## Antywzorce (czego unikać)

*   **Zbyt długi rejestr (>100 zadań):** Przytłaczający i trudny w zarządzaniu.
*   **Nieaktualne zadania:** Zaśmiecają rejestr i wprowadzają zamieszanie.
*   **Brak priorytetów:** Jeśli wszystko jest "wysokim priorytetem", to nic nim nie jest.
*   **Właściciel produktu decyduje sam:** Brak zaangażowania zespołu prowadzi do niedoszacowań i problemów w trakcie sprintu.
*   **Brak definicji gotowości:** Powoduje chaos i opóźnienia w planowaniu sprintu.

## Dobre praktyki

1.  **Góra rejestru zawsze gotowa:** Zadania na najbliższe 2-3 sprinty powinny być zawsze dopracowane.
2.  **Regularna pielęgnacja:** Utrzymuj rejestr w dobrej kondycji dzięki regularnym spotkaniom.
3.  **Stosuj zasadę DEEP:** Dbaj o to, by rejestr był szczegółowy, podatny na zmiany, oszacowany i uporządkowany.
4.  **Planuj szczegółowo tylko na 2-3 sprinty do przodu:** Unikaj marnowania czasu na zadania, które mogą się zmienić.
5.  **Utrzymuj jeden rejestr produktu:** Zapewnia to przejrzystość i spójność.

---

**Pamiętaj:** Rejestr produktu to żywy dokument. Nie dąż do perfekcji, ale do ciągłego dostosowywania go do zmieniającej się rzeczywistości. Skupiaj się na dostarczaniu wartości i utrzymuj górę rejestru zawsze gotową do pracy.
