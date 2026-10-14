# Przewodnik po bieżącej dokumentacji projektu

## Wprowadzenie

Dokumentacja bieżąca to proces **ciągłego dokumentowania zmian, decyzji i postępów** w projekcie. To nie jest jednorazowa czynność, ale codzienna praktyka zespołu deweloperskiego.

**Dlaczego jest ważna?**
- Śledzenie historii zmian (co, kiedy, dlaczego).
- Komunikacja z użytkownikami i interesariuszami.
- Ułatwienie wdrażania nowych członków zespołu.
- Pomoc w debugowaniu i rozwiązywaniu problemów.

**Kluczowe komponenty:**
1.  **Dziennik zmian (Changelog)** - dla deweloperów.
2.  **Informacje o wydaniu (Release Notes)** - dla użytkowników.
3.  **Dokumentacja API** - dla integratorów.
4.  **Instrukcje operacyjne (Runbooks)** - dla administratorów i zespołu DevOps.

## Dziennik zmian (Changelog)

### Czym jest dziennik zmian?

To **uporządkowana, chronologiczna lista zmian** w każdej wersji projektu. Odpowiada na pytanie: "Co się zmieniło od ostatniej wersji?". Jest przeznaczona głównie dla deweloperów, testerów i menedżerów technicznych.

### Standard "Keep a Changelog"

https://keepachangelog.com/

Jest to popularna konwencja, która ułatwia tworzenie i czytanie dzienników zmian.

**Zasady:**
- **Pisz dla ludzi, nie dla maszyn:** Unikaj technicznego żargonu.
- **Grupuj zmiany:** Używaj kategorii: `Dodano`, `Zmieniono`, `Przestarzałe`, `Usunięto`, `Naprawiono`, `Bezpieczeństwo`.
- **Najnowsze zmiany na górze.**
- **Data wydania:** Używaj formatu RRRR-MM-DD.

### Struktura i kategorie zmian

- **Dodano (Added):** Nowe funkcjonalności.
- **Zmieniono (Changed):** Modyfikacje w istniejących funkcjonalnościach.
- **Przestarzałe (Deprecated):** Funkcjonalności, które będą usunięte w przyszłości.
- **Usunięto (Removed):** Usunięte funkcjonalności.
- **Naprawiono (Fixed):** Poprawki błędów.
- **Bezpieczeństwo (Security):** Poprawki związane z bezpieczeństwem.

### Wersjonowanie Semantyczne (SemVer)

https://semver.org/lang/pl/

Używaj formatu `MAJOR.MINOR.PATCH` (np. `2.3.1`).
- **MAJOR:** Zmiany niekompatybilne wstecz.
- **MINOR:** Nowe funkcjonalności, kompatybilne wstecz.
- **PATCH:** Poprawki błędów, kompatybilne wstecz.

## Informacje o wydaniu (Release Notes)

### Czym są informacje o wydaniu?

To komunikat **dla użytkowników końcowych** o nowej wersji. Skupia się na korzyściach, a nie na szczegółach technicznych.

| Aspekt        | Dziennik zmian   | Informacje o wydaniu                    |
|---------------|------------------|-----------------------------------------|
| **Odbiorcy**  | Deweloperzy      | Użytkownicy końcowi                     |
| **Język**     | Techniczny       | Nietechniczny, zorientowany na korzyści |
| **Szczegóły** | Wszystkie zmiany | Najważniejsze nowości i poprawki        |
| **Format**    | Ustrukturyzowany | Narracyjny, marketingowy                |

### Struktura informacji o wydaniu

- **Nagłówek:** Tytuł i data wydania.
- **Nowe funkcje:** 3-5 najważniejszych nowości z opisem korzyści.
- **Ulepszenia:** Lista usprawnień, najlepiej z konkretnymi danymi (np. "szybsze ładowanie o 65%").
- **Poprawki błędów:** Opis naprawionych problemów w zrozumiały dla użytkownika sposób.
- **Wezwanie do działania (Call-to-Action):** Zachęta do podzielenia się opinią lub wypróbowania nowej funkcji.

## Kultura ciągłej dokumentacji

### "Dokumentuj na bieżąco"

Zamiast pisać dokumentację na końcu, twórz ją równolegle z kodem. Dzięki temu jest zawsze aktualna i wymaga mniej wysiłku.

**"Definicja Ukończenia" (Definition of Done) powinna zawierać aktualizację dokumentacji.** Funkcjonalność nie jest gotowa, dopóki jej dokumentacja nie jest kompletna.

### Rodzaje bieżącej dokumentacji

- **Dokumentacja w kodzie (komentarze):** Używaj JSDoc, Docstrings itp. do opisywania funkcji, klas i skomplikowanej logiki.
- **Dokumentacja API:** Używaj standardów takich jak OpenAPI dla REST API lub dokumentacji w schemacie dla GraphQL.
- **Aktualizacje `README.md`:** Plik `README.md` to "żywy" dokument, który powinien być regularnie aktualizowany.
- **Diagramy architektury:** Używaj narzędzi takich jak Mermaid, Draw.io czy PlantUML do tworzenia i aktualizowania diagramów.
- **Instrukcje operacyjne (Runbooks):** Szczegółowe przewodniki krok po kroku dla operacji takich jak wdrożenia, odzyskiwanie po awarii czy rozwiązywanie problemów.

## Automatyzacja dokumentacji

### Konwencjonalne komunikaty Git (Conventional Commits)

Stosowanie standardu [Conventional Commits](https://www.conventionalcommits.org/) pozwala na automatyczne generowanie dzienników zmian.

**Format:** `<typ>(<zakres>): <opis>`
- `feat:` - nowa funkcjonalność.
- `fix:` - poprawka błędu.
- `docs:` - zmiany w dokumentacji.
- `perf:` - poprawa wydajności.
- `refactor:` - refaktoryzacja kodu.

### Narzędzia do automatyzacji

- **`release-phase`:** Narzędzie do automatycznego generowania `CHANGELOG.md`, aktualizowania numeru wersji i tworzenia tagów Git na podstawie konwencjonalnych komunikatów.
  https://github.com/googleapis/release-please
- **Integracja z CI/CD:** Skonfiguruj swoje narzędzia CI/CD (np. GitHub Actions, GitLab CI), aby automatycznie generowały i publikowały dzienniki zmian oraz informacje o wydaniu.

## Podsumowanie

- **Dokumentuj na bieżąco:** To klucz do utrzymania aktualnej i użytecznej dokumentacji.
- **Dostosuj komunikację do odbiorcy:** Inaczej pisz dla deweloperów, a inaczej dla użytkowników.
- **Automatyzuj, co się da:** Wykorzystaj narzędzia do generowania dokumentacji z kodu i komunikatów Git.
- **Dokumentacja to część pracy:** Uwzględnij ją w definicji ukończenia zadania i w procesie przeglądu kodu.

---

**Pamiętaj:** Dokumentacja to inwestycja, która procentuje. Dobrze udokumentowany projekt to szczęśliwszy zespół i bardziej zadowoleni użytkownicy.
