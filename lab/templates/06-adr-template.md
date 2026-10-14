# Szablon Rejestru Decyzji Architektonicznych (ADR)

## Czym jest ADR?

Rejestr Decyzji Architektonicznych (ADR) to zwięzły dokument opisujący **ważną decyzję techniczną** podjętą w projekcie. Jego celem jest zapisanie kontekstu, rozważanych opcji i konsekwencji wyboru.

**Dlaczego warto prowadzić ADR?**
- **Zachowanie historii:** Odpowiada na pytanie "dlaczego użyliśmy technologii X, a nie Y?".
- **Wsparcie dla zespołu:** Ułatwia nowym członkom zespołu zrozumienie architektury systemu.
- **Unikanie powtórnych dyskusji:** Zapobiega wielokrotnemu wracaniu do tych samych dylematów.

**Kiedy pisać ADR?**
- Przy wyborze kluczowej technologii (baza danych, framework).
- Przy podejmowaniu decyzji o architekturze (np. monolit vs mikroserwisy, REST vs GraphQL).
- Przy wyborze ważnych wzorców projektowych (np. strategia uwierzytelniania).

---

# ADR-[NUMER]: [Krótki tytuł decyzji]

- **Status:** [Proponowana / Zaakceptowana / Odrzucona / Zastąpiona]
- **Data:** [RRRR-MM-DD]
- **Autorzy:** [Imiona i nazwiska osób biorących udział w decyzji]

---

## 1. Kontekst

[Opisz problem lub sytuację, która wymaga podjęcia decyzji. Jakie są wymagania (funkcjonalne i niefunkcjonalne)? Jakie są ograniczenia (np. budżet, czas, umiejętności zespołu)?]

**Przykład:**
> Nasza aplikacja e-commerce musi przechowywać dane o produktach, użytkownikach i zamówieniach. Oczekujemy szybkiego wzrostu liczby użytkowników. Zespół ma największe doświadczenie w pracy z relacyjnymi bazami danych. Kluczowe wymagania to transakcyjność (ACID) oraz możliwość wyszukiwania pełnotekstowego.

---

## 2. Rozważane opcje

[Przedstaw co najmniej dwie alternatywy, które były brane pod uwagę.]

### Opcja 1: [Nazwa opcji, np. "Użycie bazy danych PostgreSQL"]

- **Zalety:**
  - [+] [Zaleta 1, np. "Pełne wsparcie dla transakcji ACID."]
  - [+] [Zaleta 2, np. "Dojrzała technologia z dużym wsparciem społeczności."]
- **Wady:**
  - [-] [Wada 1, np. "Mniejsza elastyczność schematu w porównaniu do baz NoSQL."]

### Opcja 2: [Nazwa opcji, np. "Użycie bazy danych MongoDB"]

- **Zalety:**
  - [+] [Zaleta 1, np. "Elastyczny schemat, łatwy do modyfikacji."]
  - [+] [Zaleta 2, np. "Dobra skalowalność horyzontalna."]
- **Wady:**
  - [-] [Wada 1, np. "Bardziej skomplikowana obsługa transakcji obejmujących wiele dokumentów."]
  - [-] [Wada 2, np. "Wymaga od zespołu nauki nowej technologii."]

---

## 3. Decyzja

[Jasno i zwięźle przedstaw, która opcja została wybrana.]

**Przykład:**
> Wybieramy **PostgreSQL** jako główną bazę danych dla naszej aplikacji.

---

## 4. Uzasadnienie

[Wyjaśnij, dlaczego dokonano takiego wyboru. Odwołaj się do kontekstu i porównania opcji.]

**Przykład:**
> Wybraliśmy PostgreSQL, ponieważ gwarantuje on spójność danych dzięki transakcjom ACID, co jest kluczowe dla systemu e-commerce. Doświadczenie zespołu w technologiach SQL pozwoli na szybsze wdrożenie. Wbudowane mechanizmy wyszukiwania pełnotekstowego eliminują potrzebę wprowadzania dodatkowych, zewnętrznych narzędzi.

---

## 5. Konsekwencje

[Opisz pozytywne i negatywne skutki podjętej decyzji.]

### Pozytywne
- [+] [np. "Szybszy start projektu dzięki znajomości technologii przez zespół."]
- [+] [np. "Wysoka niezawodność i spójność danych."]

### Negatywne
- [-] [np. "Każda zmiana w strukturze danych będzie wymagała przeprowadzenia migracji schematu."]

---

## Dobre praktyki

- **Pisz krótko i na temat:** ADR powinien być zwięzły (najlepiej 1-2 strony).
- **Dokumentuj na bieżąco:** Twórz ADR w momencie podejmowania decyzji, a nie po fakcie.
- **Traktuj ADR jako niezmienne:** Po zaakceptowaniu nie edytuj treści. Jeśli decyzja się zmienia, stwórz nowy ADR, który zastępuje stary.
- **Przechowuj ADR w repozytorium:** Traktuj je jak kod – wersjonuj i recenzuj.
