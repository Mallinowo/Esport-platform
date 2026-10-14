# Esports leagues and tournaments platform

A team project built at Collegium Witelona (computer science, semester 5) for the following courses:

- Projektowanie i programowanie systemów internetowych II (PPSI2)
- Projektowanie interfejsów graficznych (PIG)
- Wprowadzenie do zarządzania projektami deweloperskimi (WDZPD)

## About

The application lets organizers run round-robin leagues and knockout tournaments for selected games. Users sign up by email or with Discord, create teams and register them for competitions. Team captains report match results, which are confirmed by the opposing captain or by a competition administrator. The schedule and the bracket are generated on the server, and the league table, the bracket and the results update live.

Roles: user, captain, organizer, administrator.

## Team

| Name | Role |
|---|---|
| Jakub Maliński | project lead, project manager, frontend |
| Wojciech Kasprzyk | frontend |
| Michał Kuchar | backend, tester |
| Kyrylo Shchedrin | backend, devops |

## Interface design

Figma (comments enabled): LINK_DO_FIGMY

## Tech stack

| Area | Technologies |
|---|---|
| Frontend | Vue 3, TypeScript, Vite, Tailwind CSS, Pinia, Vue Router |
| Component library | Storybook |
| Backend | Laravel (REST API), Sanctum, Socialite (Discord), Reverb, Scramble (OpenAPI), Spatie Activitylog |
| Database | PostgreSQL |
| Testing | Vitest, Playwright, PHPUnit |
| Infrastructure | Docker Compose, GitHub Actions |

## Repositories

| Repository | Contents |
|---|---|
| [esport-platform](https://github.com/Mallinowo/esport-platform) | project documentation (the `zaliczenie` directory), lab materials |
| [Esport-frontend](https://github.com/Mallinowo/Esport-frontend) | Vue application and Storybook component library |
| [Esport-backend](https://github.com/Mallinowo/Esport-backend) | Laravel REST API, OpenAPI specification, Docker Compose |

The frontend and the backend communicate only through the REST API and WebSocket. The API types and client in the frontend are generated from the OpenAPI specification produced by the backend.

## Running locally

Setup instructions are in the README of each repository: backend first, then frontend.

## Documentation

Product, technical, user and API documentation lives in the `zaliczenie` directory and is published as a static site: LINK_DO_DOKUMENTACJI

## Deployment

Application: LINK_DO_APLIKACJI
