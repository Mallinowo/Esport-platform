# Platforma do prowadzenia lig i turniejów e-sportowych

Projekt zespołowy realizowany w Collegium Witelona (informatyka, semestr 5) w ramach przedmiotów:

- Projektowanie i programowanie systemów internetowych II (PPSI2)
- Projektowanie interfejsów graficznych (PIG)
- Wprowadzenie do zarządzania projektami deweloperskimi (WDZPD)

## Opis

Aplikacja pozwala organizować ligi (każdy z każdym) i turnieje pucharowe dla wybranych gier. Użytkownicy zakładają konta mailem lub przez Discord, tworzą drużyny i zapisują je do rozgrywek. Kapitanowie zgłaszają wyniki meczów, które potwierdza kapitan przeciwnika albo administrator rozgrywek. Terminarz i drabinka generowane są po stronie serwera, a tabela ligowa, drabinka i wyniki aktualizują się na żywo.

Role w systemie: użytkownik, kapitan, organizator, administrator.

## Zespół

| Osoba | Role |
|---|---|
| Jakub Maliński | lider projektu, project manager, frontend |
| Wojciech Kasprzyk | frontend |
| Michał Kuchar | backend, tester |
| Kyrylo | backend, devops |

## Projekt interfejsu

Figma (dostęp do komentowania): LINK_DO_FIGMY

## Stos technologiczny

| Obszar | Technologie |
|---|---|
| Frontend | Vue 3, TypeScript, Vite, Tailwind CSS, Pinia, Vue Router |
| Biblioteka komponentów | Storybook |
| Backend | Laravel (REST API), Sanctum, Socialite (Discord), Reverb, Scramble (OpenAPI), Spatie Activitylog |
| Baza danych | PostgreSQL |
| Testy | Vitest, Playwright, PHPUnit |
| Infrastruktura | Docker Compose, GitHub Actions |

Frontend i backend są osobnymi aplikacjami i komunikują się wyłącznie przez REST API oraz WebSocket.

## Struktura repozytorium

```
frontend/     aplikacja Vue i Storybook
backend/      API w Laravelu
docker/       konfiguracja kontenerów
zaliczenie/   dokumentacja projektu (WDZPD)
lab/          materiały z laboratorium WDZPD
```

## Uruchomienie lokalne

Wymagania: Docker i Docker Compose.

```bash
git clone https://github.com/Mallinowo/esport-platform.git
cd esport-platform
cp backend/.env.example backend/.env
docker compose up -d
docker compose exec backend composer install
docker compose exec backend php artisan key:generate
docker compose exec backend php artisan migrate --seed
```

| Usługa | Adres |
|---|---|
| Frontend | http://localhost:5173 |
| API | http://localhost:8000/api |
| Dokumentacja API | http://localhost:8000/docs/api |
| Storybook | http://localhost:6006 |

## Testy

```bash
docker compose exec backend php artisan test
docker compose exec frontend npm run test
docker compose exec frontend npm run test:e2e
```

## Biblioteka komponentów

```bash
docker compose exec frontend npm run storybook
```

## Dokumentacja

Dokumentacja produktowa, techniczna, użytkownika i API znajduje się w katalogu `zaliczenie` i jest publikowana jako strona statyczna: LINK_DO_DOKUMENTACJI

## Wdrożenie

Aplikacja: LINK_DO_APLIKACJI
