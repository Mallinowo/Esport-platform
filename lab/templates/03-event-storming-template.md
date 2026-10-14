# Szablon Event Storming

Event Storming to technika warsztatowa służąca do modelowania złożonych domen biznesowych. Pomaga zwizualizować procesy, zidentyfikować zdarzenia (eventy), komendy (commands), agregaty (aggregates) i polityki (policies).

## Jak przeprowadzić?

1.  **Zbierzcie się w zespole:** Najlepiej z udziałem ekspertów domenowych (jeśli to możliwe).
2.  **Użyjcie kolorowych karteczek:** Każdy kolor reprezentuje inny element:
    *   **Pomarańczowy:** Zdarzenie domenowe (coś, co się wydarzyło, np. "Użytkownik zarejestrowany").
    *   **Niebieski:** Komenda (akcja, która powoduje zdarzenie, np. "Zarejestruj użytkownika").
    *   **Żółty:** Agregat (grupa obiektów traktowana jako całość, np. "Konto użytkownika").
    *   **Fioletowy:** Polityka (reguła "jeśli zdarzenie X, to wykonaj komendę Y", np. "Jeśli użytkownik się zarejestrował, wyślij e-mail powitalny").
    *   **Zielony:** Widok (dane, które użytkownik widzi, np. "Panel użytkownika").
    *   **Inne kolory (opcjonalnie):** czerwone (systemy zewnętrzne), różowe (pytania/problemy), itp.
3.  **Mapujcie proces:** Zaczynijcie od zdarzeń, układając je w porządku chronologicznym. Następnie dodawajcie komendy, agregaty i inne elementy.

## Wynik warsztatu

Wklej tutaj zdjęcie waszej tablicy z warsztatu lub opiszcie cyfrowo zidentyfikowane elementy.

### Zdarzenia (Events)

*   [Zdarzenie 1]
*   [Zdarzenie 2]
*   ...

### Komendy (Commands)

*   [Komenda 1]
*   [Komenda 2]
*   ...

### Agregaty (Aggregates)

*   [Agregat 1]
*   [Agregat 2]
*   ...

### Polityki (Policies)

*   [Polityka 1]
*   [Polityka 2]
*   ...
