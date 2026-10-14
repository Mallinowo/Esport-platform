# Przykładowy PRD: System Płatności Online dla Sklepu "ShopEasy"

- **Autor:** Anna Nowak (Product Owner)
- **Data:** 2025-01-15
- **Status:** Zatwierdzony

---

## 1. Podsumowanie

Wprowadzenie systemu płatności online (karta i BLIK) dla sklepu ShopEasy. Obecnie oferujemy tylko płatność za pobraniem, co generuje wysokie koszty i jest przyczyną rezygnacji z zakupów przez część klientów. Nowe metody płatności mają na celu zwiększenie konwersji i poprawę doświadczeń użytkowników.

---

## 2. Opis Problemu

### Jaki problem rozwiązujemy?
Obecnie jedyną formą płatności jest "płatność za pobraniem", co jest niewygodne dla wielu klientów i kosztowne dla firmy. Klienci oczekują nowoczesnych, szybkich i bezpiecznych metod płatności, takich jak karta czy BLIK. Brak tych opcji powoduje, że tracimy potencjalnych kupujących.

### Dla kogo jest ten produkt?
- **Anna (zabiegana profesjonalistka):** Chce płacić szybko i wygodnie, bez konieczności posiadania gotówki.
- **Tomek (entuzjasta technologii):** Oczekuje nowoczesnych metod płatności, takich jak BLIK.
- **Maria (seniorka):** Nadal będzie mogła korzystać z płatności za pobraniem, ale jej dzieci i znajomi coraz częściej używają kart.

---

## 3. Cele i Mierniki Sukcesu

### Cele projektu
- **Zwiększenie konwersji:** Umożliwienie większej liczbie klientów sfinalizowania zakupów.
- **Poprawa doświadczenia użytkownika:** Oferowanie nowoczesnych i wygodnych metod płatności.
- **Redukcja kosztów operacyjnych:** Zmniejszenie liczby kosztownych przesyłek za pobraniem.

### Mierniki sukcesu
- **Wskaźnik ukończenia zakupów:** Wzrost z 85% do 95%.
- **Adopcja nowych metod płatności:** 60% zamówień opłacanych online w ciągu 3 miesięcy.
- **Satysfakcja klienta (CSAT):** Wzrost satysfakcji z procesu zakupowego.

---

## 4. Wymagania i Zakres

### Kluczowe historyjki użytkownika
- **US-011:** Jako klient, chcę zapłacić kartą, aby szybko sfinalizować zamówienie.
- **US-013:** Jako klient, chcę zapłacić BLIK-iem, ponieważ jest to moja ulubiona metoda płatności.
- **US-015:** Jako klient, chcę nadal mieć możliwość płatności za pobraniem.

### Zakres projektu

**Co jest w zakresie (In Scope):**
- Płatność kartą (Visa, Mastercard).
- Płatność BLIK.
- Integracja z bezpiecznym operatorem płatności (np. Stripe).
- Zachowanie opcji płatności za pobraniem.

**Co jest poza zakresem (Out of Scope):**
- Płatności ratalne (np. Klarna).
- PayPal.
- Płatności w kryptowalutach.

---

## 5. Doświadczenie Użytkownika (UX)

### Przepływ użytkownika (płatność kartą)
1. Klient przechodzi do kasy i wybiera metodę płatności "Karta płatnicza".
2. Pojawia się bezpieczny formularz do wprowadzenia danych karty.
3. Klient jest proszony o autoryzację płatności w aplikacji swojego banku (3D Secure).
4. Po pomyślnej autoryzacji, klient widzi stronę z potwierdzeniem zamówienia.

### Kluczowe zasady projektowe
- **Zaufanie:** Wyraźne oznaczenia bezpieczeństwa (logo Visa/Mastercard, kłódka SSL).
- **Prostota:** Minimalna liczba kroków i pól do wypełnienia.
- **Jasność:** Czytelne komunikaty o błędach i statusie płatności.

---

## 6. Kwestie Techniczne

- **Operator płatności:** Wybieramy **Stripe** ze względu na dobrą dokumentację, wsparcie dla BLIK i wbudowane mechanizmy bezpieczeństwa (PCI DSS, 3D Secure).
- **Architektura:**
  - **Frontend:** Użycie `Stripe Elements` do bezpiecznego osadzenia formularza karty.
  - **Backend:** Integracja z API Stripe do tworzenia i zarządzania płatnościami.
- **Bezpieczeństwo:** Nie przechowujemy danych kart w naszej bazie danych. Wszystkie wrażliwe informacje są zarządzane po stronie Stripe.

*Warto podlinkować ADR.*

---

## 7. Otwarte Pytania i Ryzyka

- **Otwarte pytanie:** Czy powinniśmy oferować zniżkę na pierwszą płatność online, aby zachęcić do korzystania z nowej formy?
- **Ryzyko:** Niska adopcja nowych metod płatności.
  - **Plan mitygacji:** Kampania informacyjna dla klientów i ewentualne wprowadzenie zachęt (np. mały rabat).
- **Ryzyko:** Problemy techniczne z integracją operatora płatności.
  - **Plan mitygacji:** Stworzenie "spajka" (krótkiego zadania badawczego) w celu przetestowania integracji przed pełną implementacją.
