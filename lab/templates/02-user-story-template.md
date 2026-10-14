# Szablon Historyjki Użytkownika (User Story)

## Czym jest Historyjka Użytkownika?

Historyjka użytkownika to zwięzły opis funkcjonalności z perspektywy użytkownika. Odpowiada na pytania: **kto** potrzebuje **czego** i **dlaczego**. Celowo nie opisuje "jak" coś ma być zrobione – te decyzje pozostawia się zespołowi deweloperskiemu.

**Format:**
> **Jako** [typ użytkownika],
> **chcę** [wykonać akcję],
> **aby** [osiągnąć korzyść].

## Zasada INVEST

Dobra historyjka użytkownika jest:
- **Niezależna (Independent):** Można ją zrealizować niezależnie od innych.
- **Negocjowalna (Negotiable):** Szczegóły można doprecyzować w dyskusji.
- **Wartościowa (Valuable):** Przynosi realną korzyść użytkownikowi.
- **Estymowalna (Estimable):** Zespół jest w stanie oszacować jej pracochłonność.
- **Mała (Small):** Możliwa do ukończenia w ramach jednego cyklu pracy (Sprintu).
- **Testowalna (Testable):** Można zweryfikować, czy działa poprawnie.

---

# Historyjka: [Krótki, zwięzły tytuł]

## Opis

**Jako** [typ użytkownika / persona, np. "zarejestrowany klient"]
**Chcę** [wykonać akcję, np. "dodać produkt do koszyka"]
**Aby** [osiągnąć cel, np. "móc go później kupić"]

## Kryteria akceptacji

Są to warunki, które muszą zostać spełnione, aby uznać historyjkę za zrealizowaną ("Done").

**Przykład (prosta lista):**
- [ ] Użytkownik może dodać produkt do koszyka z poziomu listy produktów.
- [ ] Użytkownik może dodać produkt do koszyka ze strony szczegółów produktu.
- [ ] Po dodaniu produktu, ikona koszyka pokazuje zaktualizowaną liczbę przedmiotów.
- [ ] System wyświetla komunikat potwierdzający dodanie produktu.
- [ ] Jeśli produkt jest już w koszyku, jego ilość zostaje zwiększona.

**Przykład (format Given-When-Then):**
> **Scenariusz:** Pomyślne dodanie produktu
> - **Mając (Given)** otwartą stronę produktu,
> - **Kiedy (When)** kliknę przycisk "Dodaj do koszyka",
> - **Wtedy (Then)** produkt pojawi się w moim koszyku, a ja zobaczę komunikat "Produkt dodany do koszyka".

## Dodatkowe informacje (opcjonalnie)

- **Zależności:** Czy ta historyjka jest powiązana z innymi?
- **Notatki techniczne:** Wskazówki dla deweloperów (np. dotyczące API, bibliotek).
- **Makiety/Projekty graficzne:** Linki do Figmy, szkiców, zrzutów ekranu.
- **Przypadki brzegowe:** Co powinno się stać w nietypowych sytuacjach (np. brak połączenia z internetem)?

## Priorytet i estymacja

- **Priorytet:** [np. Wysoki, Średni, Niski lub MoSCoW: Must Have, Should Have, Could Have]
- **Estymacja (Story Points):** [np. 1, 2, 3, 5, 8...] - liczba odzwierciedlająca złożoność, a nie czas pracy.

---

## Dobre praktyki

- **Pisz z perspektywy użytkownika:** Unikaj technicznego języka.
- **Skup się na wartości:** Zawsze wyjaśniaj, jaką korzyść przynosi dana funkcja.
- **Dbaj o odpowiedni rozmiar:** Jeśli historyjka jest zbyt duża (to tzw. "Epic"), podziel ją na mniejsze.
- **Traktuj historyjkę jako punkt wyjścia do rozmowy,** a nie sztywną specyfikację.
