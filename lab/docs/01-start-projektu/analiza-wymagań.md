# Jak zbierać i analizować wymagania - Przewodnik

## Czym jest Analiza Wymagań?

Analiza wymagań to proces **zbierania, dokumentowania i weryfikacji tego, co produkt ma robić** oraz **jak ma to robić**. Jest to fundament każdego projektu - bez dobrych wymagań budujesz na niepewnym gruncie.

**Składa się z:**
- Zbierania: rozmowy z użytkownikami, analiza konkurencji.
- Dokumentowania: zapis wymagań w ustrukturyzowanej formie.
- Walidacji: weryfikacja, czy wymagania są możliwe do zrealizowania.

**Dlaczego jest ważna:**
- Budujesz to, co jest potrzebne, a nie to, co wydaje się interesujące.
- Zapobiega niekontrolowanemu rozszerzaniu zakresu projektu.
- Zmiana wymagań po rozpoczęciu kodowania jest znacznie droższa.
- Ujednolica wizję w zespole - wszyscy rozumieją cel.

## Typy Wymagań

### Funkcjonalne (Co system robi)

Opisują konkretne funkcje i zachowania systemu.

| Wymaganie         | Opis                                            |
|-------------------|-------------------------------------------------|
| Rejestracja       | Użytkownik może założyć konto.                  |
| Resetowanie hasła | Użytkownik może zresetować hasło przez e-mail.  |
| Wyszukiwanie      | Szukanie produktów po nazwie, kategorii, cenie. |
| Koszyk            | Dodawanie produktów i edycja ich ilości.        |

### Niefunkcjonalne (Jak system działa)

Opisują jakość, wydajność i ograniczenia systemu.

| Kategoria          | Przykłady                                                                      |
|--------------------|--------------------------------------------------------------------------------|
| **Wydajność**      | Czas odpowiedzi poniżej 2 sekund, wsparcie dla 1000 użytkowników jednocześnie. |
| **Bezpieczeństwo** | Uwierzytelnianie JWT, szyfrowane hasła, protokół HTTPS.                        |
| **Skalowalność**   | Obsługa ponad 100 tysięcy produktów.                                           |
| **Użyteczność**    | Projektowanie responsywne, dostępność dla osób z niepełnosprawnościami.        |
| **Niezawodność**   | Dostępność na poziomie 99.5%, codzienne kopie zapasowe.                        |

## Techniki Zbierania Wymagań

### Wywiady z Użytkownikami

**Format:** spotkanie z grupą 5-10 osób, nagrywanie i sporządzanie notatek.

**Przykładowe pytania:**
- "Opowiedz, jak obecnie wykonujesz [zadanie X]?"
- "Co Cię frustruje w [istniejącym rozwiązaniu]?"
- "Co byś zmienił w pierwszej kolejności?"

### Ankiety

**Format:** 10-15 pytań, skierowane do 50-500 respondentów.

**Zastosowanie:** badania ilościowe, walidacja hipotez na dużej próbie, priorytetyzacja funkcji.

### Warsztaty

**Format:** spotkanie z zespołem i interesariuszami.

**Techniki:** Burza zdarzeń (Event Storming), mapowanie historyjek użytkownika, identyfikacja wzorców.

### Obserwacja

**Format:** obserwacja użytkowników w ich naturalnym środowisku.

**Zastosowanie:** optymalizacja procesów pracy, zrozumienie rzeczywistego kontekstu użycia.

### Analiza Konkurencji

Badanie 3-5 konkurencyjnych produktów pod kątem funkcji, wad i zalet.

**Wartość:** poznanie standardów rynkowych, analiza porównawcza (benchmarking).

### Dane Analityczne

Analiza istniejących produktów: w których miejscach użytkownicy rezygnują, co klikają, z których funkcji korzystają.

### Wywiady z Interesariuszami

Rozmowy z Właścicielami Produktu (Product Owner) i menedżerami o celach biznesowych, metrykach sukcesu i ograniczeniach.

## Przeprowadzanie Wywiadu

### Przygotowanie

- Rekrutacja reprezentatywnych uczestników.
- Przygotowanie 8-12 pytań otwartych.
- Zarezerwowanie spokojnego miejsca na rozmowę.

### Prowadzenie

- Wyjaśnij cel rozmowy.
- Uzyskaj zgodę na nagrywanie.
- Zadawaj pytania i słuchaj uważnie.
- Pytaj "dlaczego?", aby zrozumieć problem głębiej.
- Notuj najważniejsze cytaty.

### Analiza

**Po każdej rozmowie:**
- Podsumuj główne wnioski.
- Zidentyfikuj wspólne tematy.
- Połącz informacje z innych wywiadów.
- Stwórz profile użytkowników (persony).

**Po wszystkich wywiadach:**
- Szukaj wzorców (jeśli 5 na 10 osób mówi to samo, jest to istotna informacja).
- Priorytetyzuj: duża częstotliwość + duży wpływ = wymaganie kluczowe.

## Priorytetyzacja MoSCoW

Metoda MoSCoW pomaga określić priorytety wymagań, dzieląc je na cztery kategorie:

| Kategoria                     | Definicja                                  | Przykład                                  |
|-------------------------------|--------------------------------------------|-------------------------------------------|
| **Musi być (Must have)**      | Krytyczne dla produktu w wersji MVP.       | Rejestracja, katalog produktów, płatność. |
| **Powinno być (Should have)** | Ważne, ale nie krytyczne na starcie.       | Resetowanie hasła, opinie o produktach.   |
| **Może być (Could have)**     | Funkcje typu "nice to have", miły dodatek. | Rekomendacje, tryb ciemny.                |
| **Nie będzie (Won't have)**   | Funkcje poza zakresem obecnej wersji.      | Obsługa wielu walut, czat na żywo.        |

**Proces:** Stwórz listę wszystkich wymagań → każdy członek zespołu przypisuje kategorię (M/S/C/W) → omówcie różnice → osiągnijcie konsensus.

## Formaty Dokumentacji Wymagań

### Historyjki użytkownika (User Stories) - dla metodyk zwinnych (Agile)

```
Jako [persona]
Chcę [wykonać akcję]
Aby [osiągnąć korzyść]

Kryteria akceptacji:
- Kryterium 1
- Kryterium 2
```

### Specyfikacja Wymagań Produktu (PRD) - dla dużych funkcji

**Struktura:** Problem → Cele → Wymagania → Zakres → Doświadczenie użytkownika (UX) → Implementacja.

### Lista Funkcji (dla Minimalnie Opłacalnego Produktu - MVP)

```
Musi mieć:
- Rejestracja użytkownika
- Katalog produktów

Powinno mieć:
- Resetowanie hasła

Nie będzie (w tej wersji):
- Obsługa wielu walut
```

## Dobre Praktyki

### 1. Angażuj użytkowników wcześnie
Prowadź rozmowy PRZED rozpoczęciem kodowania, twórz prototypy, angażuj testerów beta.

### 2. Zadawaj "dlaczego" kilka razy
To pomaga dotrzeć do źródła problemu. Przykład:
- Poziom 1: "Użytkownicy nie kończą procesu zakupowego." → Dlaczego?
- Poziom 2: "Strona dostawy jest myląca." → Dlaczego?
- Poziom 3: "Jest na niej zbyt wiele pól." → Dlaczego?
- Poziom 4: "Zbieramy niepotrzebne dane." → **Przyczyna źródłowa**: usuń zbędne pola.

### 3. Dokumentuj wszystko
Notatki ze spotkań, ustalenia i decyzje powinny być przechowywane w jednym, dostępnym miejscu.

### 4. Waliduj pomysły danymi
Korzystaj z ankiet, analityki i testów. Nie opieraj się wyłącznie na założeniach.

### 5. Priorytetyzuj bezwzględnie
Zadaj sobie pytanie: "Czego NIE będziemy robić?". Skup się na tym, co najważniejsze.

### 6. Iteruj
Stwórz MVP → uruchom produkt → zbieraj informację zwrotną → ulepszaj.

## Częste Błędy

### 1. Pytania sugestywne
- **Źle:** "Nasz proces finalizacji zakupu jest szybki, prawda?"
- **Dobrze:** "Opowiedz o swoim ostatnim doświadczeniu z finalizacją zakupu."

### 2. Założenia bez weryfikacji
Myślisz, że użytkownicy chcą funkcji X → budujesz ją → nikt jej nie używa.

### 3. Zbyt wiele wymagań na start
Zamiast 30 funkcji, skup się na 3-5 kluczowych, aby jak najszybciej dostarczyć wartość.

### 4. Ignorowanie wymagań niefunkcjonalnych
Wydajność, bezpieczeństwo i dostępność są kluczowe dla sukcesu produktu.

### 5. Analiza w pojedynkę
Kierownik projektu pisze wymagania, a zespół programistów odkrywa problemy techniczne dopiero w trakcie prac.

### 6. Brak udziału użytkowników
Budujesz produkt w oparciu o własne założenia, a nie rzeczywiste potrzeby.

## Lista kontrolna: Czy analiza jest zakończona?

### Zbieranie Danych
- [ ] Przeprowadzono wywiady lub ankiety.
- [ ] Zebrano dane ilościowe.
- [ ] Przeanalizowano konkurencję.
- [ ] Przeprowadzono rozmowy z interesariuszami.

### Dokumentacja
- [ ] Wnioski są spisane i dostępne dla zespołu.
- [ ] Zidentyfikowano kluczowe wzorce i problemy.
- [ ] Stworzono listę wymagań (funkcjonalnych i niefunkcjonalnych).

### Priorytetyzacja
- [ ] Zastosowano metodę MoSCoW lub podobną.
- [ ] Określono zakres MVP.

### Walidacja
- [ ] Wymagania zostały zweryfikowane danymi.
- [ ] Zespół zapoznał się z wymaganiami.
- [ ] Kierownictwo zatwierdziło zakres.

### Format
- [ ] Wymagania zapisano w formie historyjek użytkownika, PRD lub listy.
- [ ] Określono kryteria akceptacji.
- [ ] Stworzono profile użytkowników.

## Następne Kroki

1. Stwórz profile użytkowników (persony).
2. Napisz historyjki użytkownika.
3. Stwórz dokument wymagań produktu (PRD), jeśli jest potrzebny.
4. Przejdź do planowania sprintu.

---

**Kluczowa zasada:** Dobra analiza wymagań to fundament skutecznego produktu.
