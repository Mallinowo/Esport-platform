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
| Kyrylo Shchedrin | backend, devops |

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

## Repozytoria

| Repozytorium | Zawartość |
|---|---|
| [esport-platform](https://github.com/Mallinowo/esport-platform) | dokumentacja projektu (katalog `zaliczenie`), materiały z laboratorium |
| [Esport-frontend](https://github.com/Mallinowo/Esport-frontend) | aplikacja Vue i biblioteka komponentów Storybook |
| [Esport-backend](https://github.com/Mallinowo/Esport-backend) | REST API w Laravelu, specyfikacja OpenAPI, Docker Compose |

Frontend i backend komunikują się wyłącznie przez REST API oraz WebSocket. Typy i klient API we frontendzie powstają ze specyfikacji OpenAPI generowanej przez backend.

## Uruchomienie lokalne

Instrukcje uruchomienia są w README każdego z repozytoriów: najpierw backend, potem frontend.

## Dokumentacja

Dokumentacja produktowa, techniczna, użytkownika i API znajduje się w katalogu `zaliczenie` i jest publikowana jako strona statyczna: LINK_DO_DOKUMENTACJI

## Wdrożenie

Aplikacja: LINK_DO_APLIKACJI
