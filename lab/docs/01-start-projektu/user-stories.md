# Jak pisać historyjki użytkownika - Przewodnik

## Czym jest historyjka użytkownika?

Historyjka użytkownika to **krótki opis funkcjonalności z perspektywy użytkownika**. To narzędzie komunikacji między właścicielem produktu a zespołem deweloperskim, które opisuje **kto** potrzebuje **czego** i **dlaczego** - ale nie **jak** (implementację zostawiamy zespołowi).

**Format podstawowy:**
```
Jako [typ użytkownika/profil]
Chcę [wykonać akcję]
Aby [osiągnąć korzyść/cel]
```

## Kiedy pisać historyjkę?

### PISZ historyjkę, gdy:
- Opisujesz funkcjonalność dla użytkownika.
- Funkcjonalność dostarczy wartość biznesową.
- Można ją zaimplementować w ciągu kilku dni.
- Potrzebujesz opisać CO i DLACZEGO, a nie JAK.

### NIE pisz historyjki, gdy:
- To poprawka błędu (użyj szablonu raportu błędu).
- To zadanie badawcze (użyj zadania typu "spike").
- To dług techniczny (refaktoryzacja, aktualizacja biblioteki).

## Struktura historyjki

### Główna część

```
Jako [konkretna osoba/profil, nie ogólny "użytkownik"]
Chcę [jasna akcja: czasownik + przedmiot]
Aby [wymierny benefit dla użytkownika lub biznesu]
```

**Dobre vs. Złe:**

Dobrze:
```
Jako menedżer
Chcę eksportować raport do Excela
Aby przesłać dane do działu kadr
```

Źle:
```
Jako użytkownik
Chcę mieć lepszy system
Aby było lepiej
```

## Kryteria INVEST

Dobra historyjka spełnia kryteria **INVEST**:

### I - Niezależna (Independent)
- Można ją zaimplementować bez czekania na inne historyjki.
- Kolejność nie jest krytyczna.

### N - Negocjowalna (Negotiable)
- Szczegóły są do dyskusji (to nie jest sztywna specyfikacja).
- Zespół może zaproponować alternatywne rozwiązanie.

### V - Wartościowa (Valuable)
- Dostarcza wartość użytkownikowi lub biznesowi.
- Ktoś jest gotów za to zapłacić.

### E - Estymowalna (Estimable)
- Zespół może oszacować jej złożoność.
- Wymagania są wystarczająco jasne.

### S - Mała (Small)
- Mieści się w jednym sprincie (zazwyczaj 1-13 punktów).
- Jeśli jest większa, należy ją podzielić.

### T - Testowalna (Testable)
- Ma jasne kryteria akceptacji.
- Dział jakości wie, co sprawdzać.

## Kryteria akceptacji

Kryteria akceptacji definiują warunki "ukończenia" historyjki.

### Format: Mając-Kiedy-Wtedy (Given-When-Then)

```
Scenariusz: Pomyślna rejestracja
Mając (Given) - warunek początkowy
Kiedy (When) - akcja użytkownika
Wtedy (Then) - oczekiwany rezultat
```

**Przykład:**
```
Scenariusz 1: Pomyślna rejestracja
Mając niezalogowanego użytkownika
Kiedy wypełniam formularz (email, hasło, zgoda)
I klikam "Utwórz Konto"
Wtedy widzę komunikat "Sprawdź email, by aktywować konto"
I otrzymuję email z linkiem

Scenariusz 2: Email już istnieje
Mając informację, że email test@example.com już istnieje
Kiedy próbuję się zarejestrować tym emailem
Wtedy widzę błąd "Email już zarejestrowany"
I formularz się nie wysyła

Scenariusz 3: Walidacja hasła
Mając stronę rejestracji
Kiedy wpisuję hasło krótsze niż 8 znaków
Wtedy widzę błąd "Minimum 8 znaków"
I przycisk jest nieaktywny
```

### Format: Lista kontrolna (Checklist)

Dla prostszych historyjek można użyć listy warunków:

```
Kryteria akceptacji:
- [ ] Formularz zawiera pola: email, hasło, potwierdzenie hasła, pole wyboru z regulaminem.
- [ ] Email jest walidowany (format xxx@yyy.zzz).
- [ ] Hasło ma minimum 8 znaków, 1 cyfrę, 1 wielką literę.
- [ ] Po wysłaniu formularza wysyłany jest email weryfikacyjny.
- [ ] Po wysłaniu następuje przekierowanie na stronę /onboarding.
- [ ] W przypadku błędów wyświetlany jest komunikat, a pole jest podświetlone.
```

## Dobre praktyki

### 1. Konkretne kryteria

Źle:
```
- System powinien być szybki.
- Interfejs użytkownika powinien być intuicyjny.
```

Dobrze:
```
- Strona ładuje się w mniej niż 2 sekundy.
- Wyszukiwanie trwa krócej niż 500 ms.
- Kluczowe przyciski mają podpowiedzi (tooltips).
```

### 2. Uwzględnij przypadki brzegowe

Nie tylko "szczęśliwa ścieżka":
```
Szczęśliwa ścieżka: Użytkownik dodaje produkt do koszyka.

Przypadki brzegowe:
- Jeśli produkt jest niedostępny: wyświetl komunikat.
- Jeśli użytkownik jest niezalogowany: poproś o zalogowanie.
- Jeśli wystąpi błąd serwera: ponów próbę 3 razy, a następnie wyświetl komunikat o błędzie.
```

### 3. Nie opisuj implementacji

Historyjka opisuje CO, a nie JAK.

Źle (zbyt technicznie):
```
- Backend używa PostgreSQL.
- Frontend aktualizuje stan za pomocą Redux.
- JWT jest przesyłany w nagłówku.
```

Dobrze (z perspektywy użytkownika):
```
- Dane użytkownika są zapisywane.
- Profil jest aktualizowany.
- Zmiany są widoczne natychmiast.
```

### 4. Opieraj się na profilach użytkowników

```
Jako Anna (zajęty menedżer, korzystająca głównie z urządzeń mobilnych)
Chcę...
```

Zamiast:
```
Jako użytkownik
Chcę...
```

### 5. Twórz z zespołem (nie w pojedynkę)

Proces:
1. Właściciel produktu pisze wersję roboczą.
2. Zespół zadaje pytania (podczas spotkania uszczegóławiającego).
3. Właściciel produktu aktualizuje historyjkę.
4. Zespół osiąga konsensus, że historyjka jest "gotowa".

## Ile kryteriów?

**Optymalnie: 3-7 kryteriów na historyjkę.**

*   Zbyt mało (<3) → historyjka jest niekompletna.
*   Zbyt wiele (>10) → historyjka jest za duża, należy ją podzielić.

## Epik vs. Historyjka vs. Zadanie

```
Epik (duża funkcjonalność, więcej niż jeden sprint)
├── Historyjka 1 (kilka dni, 1-13 punktów)
│   ├── Zadanie 1 (godziny)
│   └── Zadanie 2
├── Historyjka 2
│   └── Zadanie 1
└── Historyjka 3
```

### Epik
- Duża funkcjonalność, >13 punktów.
- Rozbija się na historyjki.

Przykład:
```
Epik: System uwierzytelniania
- Rejestracja
- Logowanie
- Reset hasła
- Weryfikacja emaila
```

### Historyjka użytkownika
- 1-13 punktów (idealnie 3-8).
- Dostarcza wartość niezależnie.
- Mieści się w jednym sprincie.

Przykład:
```
Historyjka: Rejestracja przez email
```

### Zadanie
- Techniczne (niezwiązane bezpośrednio z interfejsem użytkownika).
- Część historyjki.
- Szacowane w godzinach.

Przykład dla historyjki "Rejestracja":
```
- Backend: Model użytkownika
- Backend: Punkt końcowy API do rejestracji
- Frontend: Formularz
- Testy: Jednostkowe i end-to-end
```

## Poker planistyczny (estymacja)

Zespołowa technika do szacowania historyjek.

**Proces:**

1. Właściciel produktu prezentuje historyjkę.
2. Zespół zadaje pytania (doprecyzowanie).
3. Każdy wybiera kartę (1, 2, 3, 5, 8, 13, 21).
4. Jednocześnie odsłaniają karty.
5. Jeśli jest konsensus → gotowe.
6. Jeśli jest rozbieżność → dyskusja, ponowne głosowanie.

**Skala Fibonacciego:**
- 1-3 punkty: mała, dokładna estymacja.
- 5-8 punktów: średnia, więcej niepewności.
- 13+ punktów: za duża, rozważ podział.

## Częste błędy

### 1. Zbyt duża historyjka

```
Historyjka: Pełny system e-commerce (200 punktów)
```

Rozwiązanie: Podziel na mniejsze:
- Historyjka 1: Katalog produktów
- Historyjka 2: Koszyk
- Historyjka 3: Proces zakupowy
- Historyjka 4: Płatność

### 2. Brak kryteriów akceptacji

```
Historyjka: Rejestracja użytkownika
(brak kryteriów akceptacji)
```

Rozwiązanie: Dodaj co najmniej 3 kryteria, uwzględniając "szczęśliwą ścieżkę" i przypadki brzegowe.

### 3. Język techniczny

```
Jako programista
Chcę zaimplementować OAuth 2.0 z PKCE
```

Rozwiązanie:
```
Jako użytkownik
Chcę zalogować się przez Google
Aby nie tworzyć nowego hasła
```

### 4. Opisywanie rozwiązania

```
Jako użytkownik
Chcę rozwijane menu z 10 opcjami, niebieskie, po lewej stronie
```

Rozwiązanie:
```
Jako użytkownik
Chcę wybrać kraj
Aby ustawić walutę i opcje dostawy

Kryteria akceptacji: Lista 193 krajów, autouzupełnianie do szybkiego wyszukiwania
```

### 5. Ignorowanie definicji gotowości

Jeśli historyjka nie jest "gotowa" → nie może trafić do sprintu!

Historyjka jest GOTOWA, gdy:
- [ ] Kryteria akceptacji są jasne.
- [ ] Estymacja jest zakończona.
- [ ] Projekt graficzny jest gotowy (jeśli potrzebny).
- [ ] Zespół ją zaakceptował.

## Pisanie historyjki - krok po kroku

### Krok 1: Zidentyfikuj profil i problem

```
Profil: Anna (zajęty menedżer)
Problem: Regularne zakupy tych samych produktów zajmują mi zbyt dużo czasu.
```

### Krok 2: Sformułuj historyjkę

```
Jako Anna
Chcę szybko zamówić ponownie regularne produkty
Aby zaoszczędzić czas
```

### Krok 3: Określ wartość

- Dla Anny: oszczędność czasu.
- Dla biznesu: wyższa częstotliwość zakupów, utrzymanie klienta.

### Krok 4: Napisz kryteria akceptacji

Uwzględnij "szczęśliwą ścieżkę" i co najmniej 2 przypadki brzegowe.

### Krok 5: Oszacuj (poker planistyczny)

Zespół osiąga konsensus na 8 punktów.

### Krok 6: Uszczegółowienie z zespołem

- Pytania, doprecyzowanie.
- Aktualizacja kryteriów akceptacji, jeśli potrzeba.
- Status: Gotowa do sprintu.

## Lista kontrolna: Czy historyjka jest gotowa?

### Format
- [ ] Tytuł - opisowy (np. "Reset hasła przez email").
- [ ] Jako-Chcę-Aby - wszystkie 3 części.
- [ ] Profil - konkretny (nie "użytkownik").
- [ ] Akcja - jasna (czasownik + przedmiot).
- [ ] Wartość - wymierny benefit.

### Kryteria INVEST
- [ ] Niezależna.
- [ ] Negocjowalna.
- [ ] Wartościowa.
- [ ] Estymowalna.
- [ ] Mała (1-13 punktów).
- [ ] Testowalna.

### Kryteria akceptacji
- [ ] ≥3 kryteria.
- [ ] Uwzględniona "szczęśliwa ścieżka".
- [ ] ≥2 przypadki brzegowe.
- [ ] Obsługa błędów.
- [ ] Testowalne (dział jakości wie, co sprawdzać).

### Estymacja
- [ ] Punkty historyjki (poker planistyczny).
- [ ] Priorytet (np. MoSCoW).
- [ ] Uzasadnienie.

### Przegląd zespołowy
- [ ] Uszczegółowiona z zespołem.
- [ ] Osiągnięto konsensus w kwestii pytań.
- [ ] Właściciel produktu zaakceptował.
- [ ] Spełniona definicja gotowości.

---

**Pamiętaj:** Historyjka użytkownika to zaproszenie do rozmowy, a nie kompletny dokument. Ważne jest jasne określenie CZEGO (co ma być zrobione) i DLACZEGO (po co), a zespół wybiera JAK (sposób realizacji).
