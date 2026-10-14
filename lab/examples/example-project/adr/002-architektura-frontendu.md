# ADR-002: Wybór frameworka frontendowego dla "ShopEasy"

- **Status:** Zaakceptowana
- **Data:** 2025-01-12
- **Autorzy:** Maria Kowalczyk, Jan Kowalski

---

## 1. Kontekst

Nasz projekt, platforma e-commerce "ShopEasy", wymaga nowoczesnego frameworka JavaScript do budowy interfejsu użytkownika.

**Kluczowe wymagania:**
- **Responsywność:** Aplikacja musi działać płynnie na urządzeniach mobilnych.
- **Wydajność:** Szybkie ładowanie stron i płynne interakcje są kluczowe dla doświadczenia użytkownika.
- **SEO (Search Engine Optimization):** Strony produktowe muszą być łatwo indeksowane przez wyszukiwarki, takie jak Google.
- **Interaktywność:** Dynamiczny koszyk, filtry produktów i inne elementy interaktywne.
- **Umiejętności zespołu:** Zespół deweloperski ma największe doświadczenie w pracy z Reactem.

---

## 2. Rozważane opcje

### Opcja 1: React z frameworkiem Next.js
Najpopularniejsza biblioteka do budowy interfejsów użytkownika, rozszerzona o możliwości renderowania po stronie serwera (SSR) dzięki Next.js.

- **Zalety:**
  - [+] Zespół ma duże doświadczenie w tej technologii, co przyspieszy prace.
  - [+] Next.js zapewnia doskonałe wsparcie dla SEO dzięki SSR i SSG (Static Site Generation).
  - [+] Ogromny ekosystem bibliotek i gotowych rozwiązań.
  - [+] Duża dostępność deweloperów na rynku pracy.
- **Wady:**
  - [-] Może generować nieco większy rozmiar paczki startowej w porównaniu do innych opcji.

### Opcja 2: Vue.js z frameworkiem Nuxt.js
Popularny, progresywny framework, ceniony za prostotę i dobrą dokumentację.

- **Zalety:**
  - [+] Uważany za łatwiejszy do nauki niż React.
  - [+] Dobra wydajność i mniejszy rozmiar paczki.
- **Wady:**
  - [-] Zespół musiałby poświęcić czas na naukę, co opóźniłoby start projektu.
  - [-] Mniejszy ekosystem i mniejsza dostępność deweloperów niż w przypadku Reacta.

### Opcja 3: Svelte z frameworkiem SvelteKit
Nowoczesny framework, który kompiluje kod do czystego JavaScriptu, co zapewnia najwyższą wydajność.

- **Zalety:**
  - [+] Najlepsza wydajność i najmniejszy rozmiar paczki.
  - [+] Bardzo czytelna i zwięzła składnia.
- **Wady:**
  - [-] Zespół nie ma żadnego doświadczenia w tej technologii.
  - [-] Najmniejszy ekosystem i bardzo mała dostępność deweloperów.
  - [-] Uważany za bardziej ryzykowny wybór ze względu na mniejszą dojrzałość.

---

## 3. Decyzja

**Wybieramy React z frameworkiem Next.js do budowy frontendu naszej aplikacji.**

---

## 4. Uzasadnienie

Decyzja opiera się na trzech kluczowych filarach:
1.  **Doświadczenie zespołu:** Nasz zespół zna Reacta najlepiej, co pozwoli na natychmiastowe rozpoczęcie prac i szybkie dostarczenie wartości. Unikniemy opóźnień związanych z nauką nowej technologii.
2.  **Wymagania SEO:** Next.js jest branżowym standardem, jeśli chodzi o tworzenie zoptymalizowanych pod SEO aplikacji React. Dla sklepu internetowego jest to absolutnie kluczowe.
3.  **Dojrzałość ekosystemu:** Ogromna liczba bibliotek, narzędzi i gotowych rozwiązań dla Reacta znacząco przyspieszy rozwój i ułatwi rozwiązywanie problemów.

Chociaż Svelte oferuje lepszą wydajność, a Vue jest postrzegane jako prostsze, ryzyko związane z krzywą uczenia się i mniejszym ekosystemem jest zbyt duże dla naszego projektu na tym etapie.

---

## 5. Konsekwencje

### Pozytywne
- Szybki start projektu i wysoka produktywność zespołu od samego początku.
- Dobre pozycjonowanie w wyszukiwarkach dzięki SSR.
- Łatwość w znalezieniu gotowych rozwiązań i wsparcia społeczności.
- Łatwiejsze zatrudnianie nowych deweloperów w przyszłości.

### Negatywne
- Rozmiar aplikacji będzie nieco większy niż w przypadku Svelte, co może nieznacznie wpłynąć na czas ładowania na wolniejszych połączeniach internetowych. (Plan mitygacji: Zastosowanie wbudowanych w Next.js mechanizmów optymalizacji, takich jak `next/image` i `next/font`).
- React jest postrzegany jako bardziej złożony niż Vue, co może być wyzwaniem dla przyszłych, mniej doświadczonych członków zespołu.
