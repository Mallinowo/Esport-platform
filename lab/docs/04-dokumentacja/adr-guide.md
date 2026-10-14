# Przewodnik po Architekturach Decyzyjnych (ADR)

## Czym jest ADR?

Architektura Decyzyjna (ADR) to dokument, który zapisuje kluczowe **decyzje architektoniczne i techniczne** podjęte w trakcie projektu. ADR odpowiada na fundamentalne pytania:
- **Jaką decyzję podjęliśmy?** (np. wybór bazy danych, frameworka, stylu API)
- **Dlaczego?** (kontekst, problem, przeanalizowane opcje)
- **Jakie są konsekwencje?** (plusy, minusy, kompromisy)

ADR dokumentuje proces myślowy zespołu, a nie tylko ostateczny wynik.

### Korzyści ze stosowania ADR

- **Jasność i kontekst:** Nowi członkowie zespołu mogą szybko zrozumieć, dlaczego system jest zbudowany w określony sposób.
- **Unikanie powtórnych dyskusji:** Zamiast ponownie debatować nad tymi samymi problemami, zespół może odwołać się do istniejącego ADR.
- **Dokumentacja kompromisów:** Rejestruje, co zyskano, a co poświęcono, podejmując daną decyzję.
- **Transparentność:** Ułatwia interesariuszom zrozumienie technicznych aspektów projektu, w tym kosztów i ryzyk.
- **Wsparcie dla rozwoju:** Ułatwia wdrażanie nowych osób i wspiera proces refaktoryzacji.

## Kiedy pisać ADR?

### Pisz ADR, gdy decyzja:

- **Ma długoterminowy wpływ na projekt:**
  - Wybór języka programowania, bazy danych, frameworka.
  - Definicja architektury systemu (np. monolit vs. mikroserwisy).
  - Strategia uwierzytelniania czy platforma wdrożeniowa.
- **Jest kosztowna do odwrócenia:**
  - Zmiana wymaga przepisania dużej części kodu.
  - Wiąże się z migracją danych lub potrzebą przeszkolenia zespołu.
  - Powoduje uzależnienie od konkretnego dostawcy technologii.
- **Jest kontrowersyjna lub nieoczywista:**
  - Zespół ma podzielone opinie (np. GraphQL vs. REST).
  - Wymaga szczegółowej analizy i akceptacji interesariuszy.
- **Wymaga analizy wielu opcji:**
  - Porównywane są co najmniej dwie alternatywy.
  - Przeprowadzono testy wydajnościowe lub stworzono dowód koncepcji.

### Nie pisz ADR, gdy decyzja:

- **Jest trywialna:**
  - Dotyczy konwencji nazewnictwa (wystarczy przewodnik po stylu kodu).
  - Wybór prostej biblioteki pomocniczej.
- **Jest łatwo odwracalna:**
  - Wybór frameworka CSS.
  - Narzędzie do formatowania kodu.
- **Dotyczy szczegółów implementacyjnych:**
  - Nazwa zmiennej czy funkcji.
  - Struktura folderów w pojedynczym module.

## Formaty ADR

Wybierz jeden format i stosuj go konsekwentnie w całym projekcie.

### Format Nygarda (najpopularniejszy)

Stworzony przez Michaela Nygarda, najbardziej rozpowszechniony.

- **Tytuł:** Krótki, opisowy (np. "ADR-003: Użycie GraphQL dla API").
- **Status:** Proponowany, Zaakceptowany, Odrzucony, Zastąpiony.
- **Kontekst:** Opis problemu, ograniczeń i wymagań.
- **Decyzja:** Co zostało postanowione.
- **Konsekwencje:** Pozytywne i negatywne skutki decyzji.

### Format MADR (Markdown ADR)

Rozszerzona wersja formatu Nygarda, bardziej szczegółowa.

- **Tytuł, Status, Data, Uczestnicy.**
- **Kontekst i opis problemu.**
- **Czynniki decyzyjne:** Co wpływa na decyzję (np. wymagania, ograniczenia).
- **Rozważane opcje:** Lista opcji wraz z ich zaletami i wadami.
- **Decyzja:** Co wybrano.
- **Uzasadnienie decyzji:** Szczegółowe wyjaśnienie, dlaczego dokonano takiego wyboru.
- **Konsekwencje:** Skutki pozytywne, negatywne i neutralne (w tym zadania do wykonania).

### Format Y (bardzo zwięzły)

Jednoznaczne oświadczenie w formie zdania.

**Przykład:**
> W kontekście budowy aplikacji czasu rzeczywistego, w obliczu potrzeby dwukierunkowej komunikacji, zdecydowaliśmy się użyć WebSockets zamiast odpytywania HTTP, aby osiągnąć niskie opóźnienia w przesyłaniu wiadomości, akceptując wyższe koszty serwera.

## Jak napisać dobry ADR (na przykładzie formatu MADR)

### 1. Tytuł i metadane

**Format:** `ADR-XXX: [Czasownik] [Rzeczownik]`
- **Dobre:** "ADR-001: Użycie PostgreSQL jako głównej bazy danych"
- **Złe:** "ADR-003: Baza danych" (zbyt ogólne)

Dodaj metadane: **Status**, **Data**, **Uczestnicy decyzji**.

### 2. Kontekst i opis problemu

Opisz problem, który rozwiązujesz, oraz kontekst projektu. Używaj konkretnych danych, wymieniaj wymagania i ograniczenia (techniczne, biznesowe, zespołowe).

### 3. Czynniki decyzyjne (opcjonalne, ale zalecane)

Wymień, co jest priorytetem przy podejmowaniu decyzji. To pokazuje, co jest dla projektu najważniejsze (np. doświadczenie zespołu, koszty, bezpieczeństwo).

### 4. Rozważane opcje

Przedstaw listę co najmniej dwóch opcji, każda z obiektywną listą zalet i wad. Unikaj przedstawiania jednej opcji jako idealnej, a drugiej jako beznadziejnej.

### 5. Decyzja

Jasno i zwięźle przedstaw, co zostało wybrane.

### 6. Uzasadnienie decyzji

Szczegółowo wyjaśnij, dlaczego wybrana opcja jest najlepsza w danym kontekście. Odnoś się do czynników decyzyjnych i wyjaśnij, dlaczego odrzucono inne alternatywy.

### 7. Konsekwencje

Opisz skutki decyzji.
- **Pozytywne:** Co zyskujemy?
- **Negatywne:** Jakie są wady i jak planujemy je minimalizować (mitygacja)?
- **Neutralne:** Jakie zadania należy wykonać w związku z podjętą decyzją?

## Dobre praktyki

- **Pisz zespołowo:** ADR to decyzja zespołu, nie jednej osoby. Opracujcie wersję roboczą, przedyskutujcie ją i wspólnie zatwierdźcie.
- **Numeruj sekwencyjnie:** Używaj formatu `ADR-001`, `ADR-002` itd. Ułatwia to odwoływanie się i śledzenie historii.
- **Traktuj ADR jako niezmienne:** Po zaakceptowaniu nie edytuj dokumentu. Jeśli decyzja się zmienia, napisz nowy ADR i oznacz stary jako "zastąpiony".
- **Używaj danych, nie opinii:** Zamiast "MongoDB jest wolniejszy", napisz "W naszych testach MongoDB miało średni czas odpowiedzi 120ms, a PostgreSQL 150ms. Obie wartości spełniają nasze wymaganie poniżej 200ms."
- **Korzystaj z szablonów:** Użyj gotowego szablonu, aby zapewnić spójność dokumentów.

## Częste błędy

- **ADR jest za długi:** Dokument powinien być zwięzły. Dłuższe analizy umieść w załącznikach.
- **Brak konkretów:** Unikaj ogólników. Decyzje muszą być poparte faktami.
- **Brak rozważanych opcji:** Zawsze porównuj co najmniej dwie alternatywy, nawet jeśli wybór wydaje się oczywisty.
- **ADR jako przewodnik implementacji:** ADR wyjaśnia "co" i "dlaczego", a nie "jak". Szczegóły implementacyjne umieść w osobnej dokumentacji technicznej.
- **Niejasny status:** Upewnij się, że status ADR (Proponowany, Zaakceptowany) odzwierciedla jego faktyczny stan. Nie rozpoczynaj implementacji, dopóki ADR nie jest zaakceptowany.

## Powiązane dokumenty

- [Szablon ADR](../../templates/06-adr-template.md)
- [Jak pisać PRD](prd-guide.md)

## Dodatkowe źródła
- https://adr.github.io/
- https://adr.github.io/madr/
- https://github.com/joelparkerhenderson/architecture-decision-record
- https://patoarchitekci.io/13/
- https://docs.aws.amazon.com/prescriptive-guidance/latest/architectural-decision-records/adr-process.html
- https://docs.cloud.google.com/architecture/architecture-decision-records

---

**Pamiętaj:** ADR dokumentuje DLACZEGO, nie tylko CO. Dobry ADR wyjaśnia kontekst, kompromisy i uzasadnienie. Twój przyszły zespół (a nawet Ty z przyszłości) będzie Ci wdzięczny!
