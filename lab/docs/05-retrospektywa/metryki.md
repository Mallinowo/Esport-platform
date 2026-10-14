# Przewodnik po Metrykach w Zarządzaniu Projektami

## Wprowadzenie

Metryki to mierzalne wskaźniki, które pomagają zespołom śledzić postępy, identyfikować problemy i podejmować decyzje oparte na danych. W zwinnych metodykach zarządzania, takich jak Scrum, metryki służą do ciągłego doskonalenia, a nie do oceny poszczególnych członków zespołu.

### Kluczowe zasady stosowania metryk
1.  **Służą zespołowi, nie managerom:** Pomagają zespołowi w samoorganizacji i poprawie procesów.
2.  **Kontekst jest najważniejszy:** Same liczby bez zrozumienia sytuacji mogą wprowadzać w błąd.
3.  **Trendy są ważniejsze niż pojedyncze wartości:** Obserwuj, jak metryki zmieniają się w czasie.
4.  **Nie manipuluj metrykami:** Jeśli zespół zaczyna "pracować pod metryki", tracą one swoją wartość.

---

## Prędkość Zespołu (Velocity)

### Czym jest Velocity?
**Velocity** to suma punktów historyjek (Story Points) ukończonych przez zespół w jednym sprincie. Mierzy ona tempo pracy zespołu i pomaga w przewidywaniu, ile pracy zespół jest w stanie wykonać w przyszłości.

### Jak mierzyć?
1.  Na początku sprintu zespół estymuje zadania w Story Points.
2.  Na koniec sprintu sumuje się punkty **tylko z tych zadań, które zostały w pełni ukończone** (zgodnie z Definition of Done).

**Przykład:**
- Zadanie A (5 SP) - Ukończone
- Zadanie B (3 SP) - Ukończone
- Zadanie C (8 SP) - W trakcie (nie liczy się)
**Velocity w tym sprincie = 5 + 3 = 8 punktów.**

### Jak interpretować i używać?
- **Stabilne velocity** (np. 20, 18, 22, 21 SP w kolejnych sprintach) oznacza, że zespół pracuje w przewidywalnym tempie.
- **Niestabilne velocity** (np. 30, 10, 25, 5 SP) wskazuje na problemy, takie jak złe estymacje, zewnętrzne blokady czy nierównomierne zaangażowanie.
- **Do planowania:** Jeśli backlog produktu ma 100 SP, a średnie velocity zespołu wynosi 20 SP na sprint, można oszacować, że praca zajmie około 5 sprintów (100 / 20 = 5).

### Typowe błędy
- **Porównywanie velocity między zespołami:** To bezsensowne, ponieważ każdy zespół ma swoją unikalną skalę estymacji.
- **Wywieranie presji na wzrost velocity:** Prowadzi to do sztucznego zawyżania estymacji, a nie do faktycznego wzrostu wydajności.
- **Liczenie niedokończonych zadań:** Zadanie ukończone w 99% to zadanie nieukończone. Do velocity liczy się tylko 100% gotowe zadania.

---

## Wykres Spalania (Burn-down Chart)

### Czym jest Burn-down Chart?
To wykres, który wizualizuje, ile pracy (w Story Points) pozostało do wykonania w sprincie. Idealnie, linia na wykresie powinna systematycznie opadać do zera pod koniec sprintu.

### Jak interpretować?
- **Linia rzeczywista powyżej linii idealnej:** Zespół jest opóźniony. Należy zidentyfikować problem i ewentualnie zmniejszyć zakres sprintu.
- **Linia rzeczywista poniżej linii idealnej:** Zespół jest przed czasem. Świetna robota!
- **Linia płaska przez kilka dni:** Brak postępów. Może to oznaczać blokadę, którą należy natychmiast rozwiązać.
- **Linia idzie w górę:** Do sprintu dodano nowe zadania, co jest anty-wzorem w Scrumie.

---

## Inne przydatne metryki

- **Wykres narastania (Burn-up Chart):** Pokazuje, ile pracy już **ukończono**. Jest przydatny w projektach, gdzie zakres często się zmienia.
- **Diagram przepływu (Cumulative Flow Diagram - CFD):** Wizualizuje przepływ zadań przez poszczególne etapy (np. Do zrobienia, W trakcie, Gotowe). Pomaga identyfikować "wąskie gardła" w procesie.
- **Wskaźnik sukcesu Celu Sprintu (Sprint Goal Success Rate):** Procent sprintów, w których udało się osiągnąć założony Cel Sprintu. Wysoki wskaźnik (>80%) świadczy o dobrym planowaniu i przewidywalności zespołu.
- **Wskaźnik błędów (Defect Rate):** Liczba błędów znalezionych na produkcji. Celem jest utrzymanie tego wskaźnika na jak najniższym poziomie.

---

## Podsumowanie

- Używaj **3-5 kluczowych metryk**, aby nie przytłoczyć zespołu nadmiarem danych.
- Metryki powinny być **widoczne dla całego zespołu** i omawiane, np. na codziennych spotkaniach.
- Pamiętaj, że **trendy są ważniejsze** niż pojedyncze wartości, a **kontekst** jest kluczem do prawidłowej interpretacji.
- **Nigdy nie używaj metryk do karania zespołu.** Służą one do nauki i doskonalenia, a nie do oceny.
- Regularnie **przeglądaj metryki na retrospektywach**, aby wyciągać wnioski i planować działania usprawniające.
