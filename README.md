# Campaign Roster

> A web app for tabletop RPG game masters to share pre-made characters with their players.

## About

When running a tabletop RPG campaign, game masters often prepare several characters in advance so players can pick one, or have a backup if theirs dies. Sharing these characters and keeping track of who took which one usually means scattered files and messages.

**Campaign Roster** solves this: the game master creates a campaign room, shares it with the players through a link, shows the characters as styled cards (image, race, sex, age, class and subclass), and records which player each character belongs to.

## Status

🚧 **In development** — MVP planned for December 2026.

## Features (MVP)

- [ ] Create a campaign with a master link and an invite link
- [ ] Add campaign members with a role (Master or Player)
- [ ] Register characters with an image and a basic sheet
- [ ] Display characters as a grid of cards
- [ ] Assign a character to a player

## Tech stack

| Layer | Technology |
|---|---|
| Front-end | React + TypeScript (Vite) |
| Back-end | C# / ASP.NET Core Web API |
| Database | Entity Framework Core — SQLite (local) / PostgreSQL (production) |

## Project structure

This is a monorepo: the API and the web app live in the same repository as independent projects ([why](docs/adr/0001-use-monorepo.md)).

```
backend/    ASP.NET Core Web API
frontend/   React + TypeScript app
docs/       Architecture, data model and decision records
```

## Documentation

- [Architecture](docs/architecture.md) — components, repository layout and environments
- [Data model](docs/data-model.md) — entities, relationships and conventions
- [Architecture Decision Records](docs/adr/README.md) — why each technical decision was made
- [Contributing](CONTRIBUTING.md) — branches, commits and pull requests

## Roadmap (v2)

- Authentication for masters and players
- Image upload
- Real-time updates with SignalR
- Full character sheet
- Players can request a character

## Author

**Douglas Silva** — Computer Science student

[LinkedIn](https://www.linkedin.com/in/your-profile) · [GitHub](https://github.com/daquino-lvetec)
