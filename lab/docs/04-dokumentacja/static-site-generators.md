# Przewodnik po generatorach stron statycznych (SSG)

Generator stron statycznych (SSG) to narzędzie, które przekształca pliki Markdown w funkcjonalną i estetyczną stronę internetową. Jest to idealne rozwiązanie do tworzenia dokumentacji projektowej.

### Kluczowe kryteria oceny SSG

- **Łatwość użycia:** Jak proste jest rozpoczęcie pracy.
- **Technologia:** Jakie umiejętności są wymagane (np. znajomość React, Vue).
- **Wydajność:** Jak szybko generowana jest strona.
- **Funkcjonalności:** Wbudowane opcje, takie jak wyszukiwarka, tryb ciemny, wielojęzyczność (i18n) czy wersjonowanie.
- **Dostosowywanie:** Jak łatwo można modyfikować wygląd i działanie.
- **Wdrażanie:** Jak proste jest opublikowanie strony.

### Wymagania dla projektu studenckiego

Dobry SSG dla projektu studenckiego powinien obsługiwać:
- Markdown i MDX (osadzanie komponentów w treści).
- Podświetlanie składni kodu.
- Wyszukiwarkę.
- Responsywny design.
- Tryb ciemny.
- Łatwe wdrażanie na platformach takich jak GitHub Pages, Netlify czy Vercel.

## Przegląd popularnych narzędzi

### 1. Retype

- **Technologia:** Niezależna (nie wymaga znajomości frameworków JS).
- **Zalety:**
  - Bardzo prosty w użyciu, działa "prosto z pudełka".
  - Nowoczesny wygląd bez potrzeby konfiguracji.
  - Składnia `[[linków]]` w stylu Obsidian/Notion.
  - Wbudowane adnotacje (podpowiedzi, alerty).
- **Wady:**
  - Mniejsza społeczność i mniej wtyczek niż u konkurencji.
  - Ograniczone możliwości dostosowywania.

### 2. Docsify

- **Technologia:** Czysty JavaScript (renderowanie po stronie klienta).
- **Zalety:**
  - Brak kroku budowania – działa bezpośrednio z plików Markdown.
  - Automatycznie generowany panel boczny.
  - Duża liczba wtyczek.
- **Wady:**
  - Gorsze pozycjonowanie w wyszukiwarkach (SEO).
  - Może być wolny przy dużej ilości dokumentacji.

### 3. Fumadocs

- **Technologia:** Next.js + React.
- **Zalety:**
  - Nowoczesny stos technologiczny (React Server Components).
  - Wsparcie dla dokumentacji API z plików OpenAPI.
  - Duża elastyczność i możliwości rozbudowy.
- **Wady:**
  - Wymaga znajomości React i Next.js.
  - Może być zbyt skomplikowany dla prostych projektów.

### 4. Docusaurus

- **Technologia:** React (stworzony przez Meta/Facebook).
- **Zalety:**
  - Wbudowane wersjonowanie i wielojęzyczność.
  - Możliwość prowadzenia bloga (idealne dla dzienników zmian).
  - Ogromna społeczność i ekosystem wtyczek.
  - Używany przez wiele popularnych projektów (React, Redux, Supabase).
- **Wady:**
  - Wymaga znajomości React do dostosowywania.
  - Może generować więcej kodu niż inne narzędzia.

### 5. Nextra

- **Technologia:** Next.js + MDX.
- **Zalety:**
  - Prostszy niż Docusaurus, ale wciąż potężny.
  - Pełna integracja z Next.js (routing, API).
  - Wbudowana, wydajna wyszukiwarka.
- **Wady:**
  - Mniej wbudowanych funkcji niż Docusaurus.
  - Wymaga znajomości Next.js.

### 6. VitePress

- **Technologia:** Vue 3 + Vite.
- **Zalety:**
  - Bardzo szybki proces budowania dzięki Vite.
  - Możliwość używania komponentów Vue w Markdown.
  - Lekki i wydajny.
- **Wady:**
  - Wymaga znajomości Vue do zaawansowanego dostosowywania.
  - Mniejsza społeczność niż Docusaurus.

### 7. Astro Starlight

- **Technologia:** Astro (agnostyczny frameworkowo).
- **Zalety:**
  - Domyślnie generuje strony bez JavaScriptu, co zapewnia najwyższą wydajność.
  - Umożliwia mieszanie komponentów z różnych frameworków (React, Vue, Svelte).
  - Wbudowane wsparcie dla i18n, wyszukiwarki i trybu ciemnego.
  - Wysoki poziom dostępności (accessibility).
- **Wady:**
  - Wymaga nauki nowego podejścia (Astro).
  - Młodszy projekt z mniejszą bazą zasobów.

## Podsumowanie

Wszystkie wymienione narzędzia są świetne. Najważniejsze jest, aby **zacząć pisać dokumentację**, a nie spędzać zbyt wiele czasu na wyborze narzędzia.

Pamiętaj, że migracja między narzędziami jest stosunkowo prosta, ponieważ treść pozostaje w plikach Markdown. Najlepsza dokumentacja to taka, która istnieje.

---

**Następne kroki:**
- Wybierz jedno narzędzie z listy.
- Postępuj zgodnie z jego przewodnikiem "Quick Start".
- Zacznij tworzyć dokumentację dla swojego projektu.
