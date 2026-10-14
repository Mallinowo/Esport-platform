# Zwinne Metodyki Zarządzania Projektami: Agile, Scrum i Kanban

## Spis treści
1. [Agile - Filozofia i Wartości](#agile---filozofia-i-wartości)
2. [Scrum - Szczegółowy Opis](#scrum---szczegółowy-opis)
3. [Kanban - Szczegółowy Opis](#kanban---szczegółowy-opis)
4. [Porównanie i Wybór Metodyki](#porównanie-i-wybór-metodyki)
5. [Dobre Praktyki](#dobre-praktyki)
6. [Podsumowanie](#podsumowanie)

## Agile - Filozofia i Wartości

### Czym Agile NIE jest
- **To NIE jest brak planowania:** Planowanie jest kluczowe, ale odbywa się częściej i jest bardziej elastyczne.
- **To NIE jest chaos:** Wymaga dyscypliny i jasno określonej struktury.
- **To NIE jest tylko dla programistów:** Sprawdza się w marketingu, zarządzaniu i wielu innych dziedzinach.
- **To NIE jest jedna, konkretna metodyka:** To zbiór wartości i zasad, które można realizować na różne sposoby.

### Sposób myślenia Agile
Przejście na Agile to przede wszystkim zmiana sposobu myślenia o pracy.

**Od tradycyjnego podejścia:**
- "Musimy trzymać się planu za wszelką cenę."
- "Zmiany w projekcie to problem."
- "Im więcej dokumentacji, tym lepiej."
- "Więcej funkcji oznacza lepszy produkt."

**Do zwinnego podejścia:**
- "Dostarczamy wartość w małych, regularnych krokach."
- "Zmiany to okazja do stworzenia lepszego produktu."
- "Działające oprogramowanie jest ważniejsze niż obszerna dokumentacja."
- "Tylko potrzebne funkcje tworzą lepszy produkt."

## Scrum - Szczegółowy Opis

### Podstawy Scrum
Scrum to framework, który pomaga zespołom tworzyć produkty w złożonym środowisku. Składa się z:
- **Ról:** Właściciel Produktu, Mistrz Scruma, Zespół Deweloperski.
- **Wydarzeń:** Sprint, Planowanie Sprintu, Codzienny Scrum, Przegląd Sprintu, Retrospektywa Sprintu.
- **Wytworów (Artefaktów):** Rejestr Produktu, Rejestr Sprintu, Przyrost.

### Wytwory Scrum

#### 1. Rejestr Produktu (Product Backlog)
To uporządkowana lista wszystkiego, co może być potrzebne w produkcie. Zarządza nią **Właściciel Produktu**. Lista ta ewoluuje wraz z rozwojem produktu – im wyżej na liście znajduje się element, tym jest bardziej szczegółowy.

**Przykład elementu (Historyjka Użytkownika):**
```
Jako [użytkownik]
Chcę [wykonać akcję]
Aby [osiągnąć cel]

Kryteria akceptacji:
- [ ] Warunek 1 do spełnienia
- [ ] Warunek 2 do spełnienia
```

#### 2. Rejestr Sprintu (Sprint Backlog)
To zestaw elementów z Rejestru Produktu wybranych do realizacji w danym Sprincie, wraz z planem ich wykonania. Jest własnością **Zespołu Deweloperskiego**.

**Przykład rozbicia historyjki na zadania:**
**Historyjka:** "Jako użytkownik, chcę móc zresetować hasło."
**Zadania:**
- [ ] Stworzenie interfejsu API do resetowania hasła.
- [ ] Implementacja wysyłki e-maila z linkiem.
- [ ] Stworzenie formularza do wpisania nowego hasła.
- [ ] Testy.

#### 3. Przyrost (Increment)
To suma wszystkich ukończonych elementów z Rejestru Produktu z bieżącego Sprintu oraz wartość przyrostów z poprzednich Sprintów. Każdy Przyrost musi być "Ukończony" zgodnie z **Definicją Ukończenia (Definition of Done)** i potencjalnie gotowy do wydania.

**Przykładowa Definicja Ukończenia (DoD):**
- [ ] Kod został napisany.
- [ ] Testy jednostkowe przechodzą.
- [ ] Kod został sprawdzony przez innego programistę (Code Review).
- [ ] Funkcjonalność została zaakceptowana przez Właściciela Produktu.

### Wydarzenia Scrum

#### Sprint
To stały, powtarzalny okres (zwykle 1-4 tygodnie), w którym zespół pracuje nad Przyrostem. Sprintu nie można skracać ani wydłużać.

#### Planowanie Sprintu (Sprint Planning)
Spotkanie, na którym zespół planuje pracę na nadchodzący Sprint.
- **Część 1: "Co zrobimy?"** - Zespół wybiera elementy z Rejestru Produktu.
- **Część 2: "Jak to zrobimy?"** - Zespół rozbija wybrane elementy na konkretne zadania.

#### Codzienny Scrum (Daily Scrum)
Krótkie, codzienne spotkanie (do 15 minut), na którym zespół synchronizuje pracę i planuje działania na najbliższe 24 godziny. Każdy członek zespołu odpowiada na trzy pytania:
1. Co zrobiłem wczoraj, aby pomóc w osiągnięciu Celu Sprintu?
2. Co zrobię dzisiaj?
3. Czy napotkałem jakieś problemy?

#### Przegląd Sprintu (Sprint Review)
Spotkanie na koniec Sprintu, podczas którego zespół prezentuje "Ukończony" Przyrost interesariuszom (np. klientom, zarządowi). Celem jest zebranie opinii i dostosowanie Rejestru Produktu.

#### Retrospektywa Sprintu (Sprint Retrospective)
Spotkanie tylko dla Zespołu Scrum, które odbywa się po Przeglądzie Sprintu. Zespół analizuje, co poszło dobrze, co można poprawić, i tworzy plan ulepszeń na następny Sprint.

## Kanban - Szczegółowy Opis

### Filozofia Kanban
Kanban koncentruje się na wizualizacji pracy, ograniczaniu pracy w toku (WIP) i maksymalizacji przepływu. Główne zasady to:
1. **Zacznij od tego, co robisz teraz:** Nie musisz wprowadzać rewolucji.
2. **Zgódź się na ewolucyjne zmiany:** Wprowadzaj małe, stopniowe ulepszenia.
3. **Szanuj obecne role i procesy:** Kanban nie narzuca zmian w strukturze zespołu.

### Tablica Kanban
To narzędzie do wizualizacji przepływu pracy. Najprostsza tablica składa się z trzech kolumn:
- **Do zrobienia (To Do):** Zadania czekające na realizację.
- **W trakcie (In Progress):** Zadania, nad którymi zespół aktualnie pracuje.
- **Ukończone (Done):** Zadania, które zostały zakończone.

### Limity Pracy w Toku (WIP Limits)
To kluczowy element Kanban. Ograniczenie liczby zadań w kolumnie "W trakcie" zmusza zespół do skupienia się na kończeniu pracy, a nie na rozpoczynaniu nowej. Pomaga to zidentyfikować "wąskie gardła" w procesie.

### Metryki w Kanban
- **Czas realizacji (Lead Time):** Całkowity czas od momentu zgłoszenia zadania do jego ukończenia.
- **Czas cyklu (Cycle Time):** Czas od momentu rozpoczęcia pracy nad zadaniem do jego ukończenia.
- **Przepustowość (Throughput):** Liczba zadań ukończonych w danym okresie (np. na tydzień).

## Porównanie i Wybór Metodyki

| Aspekt                 | Scrum                                                   | Kanban                                                             |
|------------------------|---------------------------------------------------------|--------------------------------------------------------------------|
| **Iteracje**           | Stałe Sprinty (np. 2 tygodnie)                          | Ciągły przepływ pracy                                              |
| **Role**               | Właściciel Produktu, Mistrz Scruma, Zespół Deweloperski | Brak narzuconych ról                                               |
| **Wydarzenia**         | Regularne (Planowanie, Daily, Przegląd, Retrospektywa)  | Opcjonalne, często stosuje się codzienne spotkania i retrospektywy |
| **Zmiany**             | Zmiany wprowadzane są po zakończeniu Sprintu            | Możliwe w dowolnym momencie                                        |
| **Główne metryki**     | Prędkość (Velocity)                                     | Czas cyklu, Czas realizacji, Przepustowość                         |
| **Ograniczenie pracy** | Limit zadań w Sprincie                                  | Limity WIP na każdym etapie pracy                                  |

### Kiedy co wybrać?
- **Scrum** jest dobrym wyborem dla projektów, które można podzielić na regularne cykle wydań i gdzie zespół potrzebuje struktury oraz regularnych spotkań do synchronizacji.
- **Kanban** sprawdza się w sytuacjach, gdy praca jest ciągła i nieprzewidywalna (np. wsparcie techniczne, utrzymanie produktu) lub gdy zespół chce stopniowo optymalizować istniejący proces bez wprowadzania radykalnych zmian.

### Scrumban - Połączenie Najlepszych Cech
Scrumban to hybryda, która łączy strukturę Scruma z elastycznością Kanbana.
- **Ze Scruma bierze:** Regularne spotkania (np. retrospektywy), role (opcjonalnie).
- **Z Kanbana bierze:** Tablicę z limitami WIP, ciągły przepływ pracy, metryki oparte na czasie.

## Dobre Praktyki

### Wspólne dla Obu Metodyk
1.  **Przejrzystość:** Tablica z zadaniami powinna być widoczna dla wszystkich. Problemy i postępy muszą być jawne.
2.  **Ciągłe doskonalenie:** Regularnie analizujcie proces i wprowadzajcie małe usprawnienia.
3.  **Współpraca:** Zespół powinien wspólnie rozwiązywać problemy. Praktyki takie jak programowanie w parach mogą być bardzo pomocne.
4.  **Definicja "Gotowości" (Definition of Ready):** Określcie jasne kryteria, kiedy zadanie jest gotowe do rozpoczęcia.

### Specyficzne dla Scrum
- **Koncentracja na Celu Sprintu:** Każda decyzja powinna przybliżać zespół do realizacji celu.
- **Pielęgnacja Rejestru Produktu:** Regularnie przeglądajcie i doprecyzowujcie zadania na przyszłe Sprinty.

### Specyficzne dla Kanban
- **Zarządzaj przepływem:** Skupcie się na jak najszybszym kończeniu zadań, a nie na rozpoczynaniu wielu naraz.
- **Eksperymentuj z limitami WIP:** Jeśli praca idzie zbyt komfortowo, być może limit WIP jest za wysoki. Spróbujcie go obniżyć.

## Podsumowanie
- **Scrum** oferuje strukturę i regularność, idealną dla złożonych projektów rozwojowych.
- **Kanban** zapewnia elastyczność i koncentruje się na optymalizacji przepływu pracy, co jest świetne dla zadań o charakterze ciągłym.

Najważniejsze jest, aby nie trzymać się sztywno jednej metodyki. Adaptujcie zasady do kontekstu waszego projektu, eksperymentujcie i mierzcie efekty, zawsze skupiając się na dostarczaniu wartości.
