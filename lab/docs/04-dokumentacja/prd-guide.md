# Przewodnik po Dokumencie Wymagań Produktu (PRD)

## Czym jest PRD?

Dokument Wymagań Produktu (PRD) to centralny dokument opisujący, **co budujemy i dlaczego**. Stanowi on "jedyne źródło prawdy" dla całego zespołu, definiując problem, proponowane rozwiązanie, zakres projektu oraz kryteria sukcesu.

**Kiedy pisać PRD?**
- Przed rozpoczęciem pracy nad dużą funkcjonalnością (tzw. "epikiem").
- Gdy potrzebna jest synchronizacja między zarządzaniem produktem, projektowaniem a programowaniem.
- Gdy funkcjonalność jest na tyle duża, że jej realizacja zajmie więcej niż kilka cykli pracy.
- Gdy interesariusze muszą zatwierdzić zakres i koszt projektu.

**Kiedy NIE pisać PRD?**
- Dla małych zadań (wystarczy historyjka użytkownika).
- Przy poprawianiu błędów (wystarczy zgłoszenie w systemie śledzenia błędów).
- W przypadku zadań badawczych (wystarczy notatka z wynikami).

## Struktura PRD

### 1. Podsumowanie (2-3 zdania)
Zwięzły, nietechniczny opis produktu lub funkcjonalności. Każdy, w tym osoby nietechniczne, powinien zrozumieć jego cel.

### 2. Opis problemu
Wyjaśnij, jaki problem rozwiązujesz, dla kogo i jak użytkownicy radzą sobie z nim obecnie. Używaj danych i wyników badań, aby zilustrować problem.

### 3. Cele i metryki sukcesu
Określ cele biznesowe i cele użytkownika oraz wskaźniki, które pozwolą zmierzyć sukces. Stosuj metodę SMART (Specific, Measurable, Achievable, Relevant, Time-bound) do definiowania celów.

**Przykład:**
- **Cel:** Zwiększenie liczby pomyślnie zakończonych transakcji.
- **Główna metryka:** Wzrost wskaźnika ukończenia procesu zakupowego z 85% do 95%.
- **Metryka kontrolna:** Wskaźnik porzuceń koszyka nie może wzrosnąć.

### 4. Historyjki użytkownika i wymagania
Przedstaw kluczowe historyjki użytkownika oraz wymagania funkcjonalne i niefunkcjonalne. Możesz użyć priorytetyzacji MoSCoW (Must, Should, Could, Won't), aby określić, co jest najważniejsze.

### 5. Zakres
Precyzyjnie określ, co wchodzi w zakres projektu, a co jest **poza zakresem**. Wyjaśnienie, czego nie robimy, jest kluczowe, aby uniknąć "puchnięcia" zakresu w trakcie projektu.

### 6. Doświadczenie użytkownika (UX)
Opisz przepływy użytkownika i załącz linki do makiet lub prototypów. Opisz również, jak system powinien zachowywać się w sytuacjach awaryjnych (np. błędy, brak połączenia z internetem).

### 7. Kwestie techniczne
Ogólny opis architektury, stosu technologicznego i integracji. To nie jest specyfikacja techniczna, a jedynie ogólny zarys, który pomoże zidentyfikować potencjalne ryzyka.

### 8. Zależności i założenia
Wymień zespoły, zasoby zewnętrzne i kluczowe założenia, od których zależy powodzenie projektu.

### 9. Harmonogram i kamienie milowe
Przedstaw ogólny harmonogram projektu z kluczowymi datami (kamieniami milowymi). Harmonogram powinien być realistyczny i skonsultowany z zespołem deweloperskim.

### 10. Ryzyka i sposoby ich ograniczania
Zidentyfikuj 3-5 największych ryzyk, które mogą wpłynąć na projekt. Dla każdego ryzyka określ jego prawdopodobieństwo, wpływ i plan działania w celu jego zminimalizowania.

### 11. Otwarte pytania
Lista pytań, które wymagają odpowiedzi. Każde pytanie powinno mieć przypisaną osobę odpowiedzialną za znalezienie odpowiedzi.

### 12. Załączniki
Linki do dodatkowych materiałów, takich jak notatki z badań, analizy konkurencji czy dokumentacja techniczna.

## Dobre praktyki

- **Pisz jasno i konkretnie:** Używaj danych i wyników badań.
- **Współpracuj:** PRD to dokument tworzony przez cały zespół (product manager, projektanci, programiści).
- **Aktualizuj:** PRD to "żywy" dokument. Prowadź rejestr zmian, aby wszyscy byli na bieżąco.
- **Nie twórz specyfikacji technicznej:** PRD ma odpowiadać na pytania "co" i "dlaczego", a nie "jak".

## Częste błędy

- **Zbyt długi PRD:** Dokument powinien być zwięzły. Nikt nie przeczyta 50-stronicowego elaboratu.
- **Brak metryk sukcesu:** Bez nich nie da się ocenić, czy projekt odniósł sukces.
- **Brak sekcji "Poza zakresem":** Prowadzi to do niekontrolowanego rozszerzania zakresu projektu.
- **Tworzenie PRD w pojedynkę:** Brak konsultacji z zespołem prowadzi do problemów w fazie deweloperskiej.

## Szablony i przykłady

- **Szablon:** Użyj [szablonu PRD](../../templates/05-prd-template.md) do tworzenia nowych dokumentów.
- **Przykład:** Zapoznaj się z [przykładowym PRD](../../examples/example-project/prd-example.md), aby zobaczyć, jak wygląda gotowy dokument.

---

**Pamiętaj:** PRD to narzędzie komunikacji, a nie biurokratyczny obowiązek. Jeśli nie ułatwia pracy zespołowi, należy go poprawić.
