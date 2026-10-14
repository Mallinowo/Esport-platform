# Współpraca w zespole deweloperskim - przewodnik

Efektywna współpraca to fundament każdego udanego projektu. Ten przewodnik omawia kluczowe techniki i narzędzia, od programowania w parach po przeglądy kodu i komunikację asynchroniczną.

## Programowanie w parach (Pair Programming)

**Definicja:** Dwóch programistów pracuje razem przy jednym komputerze. Jeden pisze kod (**Kierowca**), a drugi obserwuje i doradza (**Nawigator**). Role te regularnie się zmieniają.

**Kiedy warto?**
- Przy trudnych i krytycznych zadaniach.
- Podczas wdrażania nowego członka zespołu.
- Gdy zespół uczy się nowej technologii.

**Techniki:**
- **Kierowca-Nawigator:** Klasyczne podejście, gdzie jedna osoba pisze kod, a druga myśli strategicznie.
- **Ping-Pong (dla TDD):** Jedna osoba pisze test, który nie przechodzi, a druga implementuje kod, aby test zakończył się sukcesem.
- **Programowanie w grupie (Mob Programming):** Cały zespół pracuje nad jednym zadaniem, z jedną osobą przy klawiaturze i resztą jako nawigatorami.

**Narzędzia do pracy zdalnej:**
- **VS Code Live Share:** Umożliwia współpracę w czasie rzeczywistym, współdzielenie terminala i debugowanie.
- **Zoom/Google Meet:** Podstawowe narzędzia do udostępniania ekranu.

## Przegląd kodu (Code Review)

**Definicja:** Proces systematycznego sprawdzania kodu przez innego dewelopera przed jego włączeniem do głównej gałęzi projektu, najczęściej za pomocą Pull Request (PR) na GitHubie.

**Dlaczego jest to ważne?**
- **Jakość:** Pomaga wyłapać błędy i zapewnić zgodność ze standardami.
- **Dzielenie się wiedzą:** Zarówno autor, jak i recenzent uczą się od siebie.
- **Wspólna odpowiedzialność:** Kod staje się własnością całego zespołu.

**Proces przeglądu kodu:**
1.  **Autor przygotowuje PR:** Opisuje wprowadzone zmiany, ich cel i sposób testowania.
2.  **Recenzent przegląda kod:** Sprawdza funkcjonalność, testy, czytelność i potencjalne błędy.
3.  **Recenzent dodaje komentarze:** Używa jasnych i konstruktywnych sugestii, unikając krytyki personalnej.
4.  **Autor odpowiada na komentarze:** Wprowadza poprawki i kontynuuje dyskusję, jeśli to konieczne.
5.  **Zatwierdzenie i scalenie:** Po uzyskaniu akceptacji, kod jest włączany do głównej gałęzi.

**Dobre praktyki:**
- **Małe Pull Requesty:** Łatwiej je przeglądać i szybciej zatwierdzać.
- **Konstruktywny feedback:** Skupiaj się na kodzie, a nie na osobie. Zadawaj pytania, zamiast wydawać polecenia.
- **Używaj szablonów PR:** Ułatwiają one opisanie zmian i kontekstu.

## Praca asynchroniczna

**Definicja:** Model pracy, w którym członkowie zespołu nie muszą być online w tym samym czasie. Komunikacja odbywa się z opóźnieniem, np. przez wiadomości na Slacku czy komentarze w PR.

**Zalety:**
- **Elastyczność:** Umożliwia pracę w różnych strefach czasowych i o różnych porach.
- **Głęboka praca (Deep Work):** Mniej rozproszeń sprzyja skupieniu i kreatywności.
- **Lepsza dokumentacja:** Wymusza zapisywanie ustaleń i decyzji.

**Wyzwania:**
- **Wolniejsza komunikacja:** Odpowiedzi mogą przychodzić z opóźnieniem.
- **Ryzyko nieporozumień:** Brak tonu głosu i mowy ciała może prowadzić do błędnej interpretacji.

**Narzędzia:**
- **Slack/Discord:** Do codziennej komunikacji, z podziałem na kanały tematyczne.
- **Asynchroniczne stand-upy:** Boty (np. Geekbot) zbierają codzienne raporty od zespołu.
- **Notion/Confluence:** Do tworzenia centralnej bazy wiedzy i dokumentacji.

## Dobre praktyki komunikacji

- **Codzienne spotkania (Stand-upy):** Krótkie, 15-minutowe spotkania, na których zespół synchronizuje swoje działania.
- **Retrospektywy:** Regularne spotkania (np. co dwa tygodnie) w celu omówienia, co działa dobrze, a co można poprawić.
- **Dzielenie się wiedzą:** Organizuj wewnętrzne prezentacje (Tech Talks), promuj programowanie w parach i dbaj o kulturę dokumentowania.

## Narzędzia do współpracy

| Kategoria                  | Narzędzie          | Zastosowanie                                      |
|----------------------------|--------------------|---------------------------------------------------|
| **Komunikacja wideo**      | Zoom, Google Meet  | Spotkania, programowanie w parach                 |
| **Czat**                   | Slack, Discord     | Komunikacja asynchroniczna, codzienne dyskusje    |
| **Współpraca wizualna**    | Miro, FigJam       | Burze mózgów, retrospektywy, mapowanie historyjek |
| **Współpraca przy kodzie** | VS Code Live Share | Programowanie w parach w czasie rzeczywistym      |
| **Dokumentacja**           | Notion, Confluence | Baza wiedzy, dokumentacja projektu                |

## Rozwiązywanie konfliktów

Konflikty są naturalną częścią pracy zespołowej. Ważne jest, aby podchodzić do nich w sposób konstruktywny.

**Rodzaje konfliktów:**
- **Techniczne:** Np. wybór między dwiema technologiami. Rozwiązuj je w oparciu o dane, prototypy i dokumentuj decyzje.
- **Procesowe:** Np. spór o konieczność przeglądu kodu. Eksperymentuj z różnymi podejściami i szukaj kompromisów.
- **Personalne:** Rozwiązuj je w prywatnych rozmowach, zakładając dobre intencje drugiej strony.

**Jak zapobiegać konfliktom?**
- **Stwórz kartę zespołu (Team Charter):** Na początku projektu ustalcie wspólne zasady komunikacji, przeglądu kodu i rozwiązywania sporów.
- **Prowadź regularne retrospektywy:** Omawianie problemów na bieżąco zapobiega ich eskalacji.
- **Dbaj o bezpieczeństwo psychologiczne:** Stwórz atmosferę, w której każdy czuje się swobodnie, wyrażając swoje zdanie.
