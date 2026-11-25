# 0003. Tech stack: React + TypeScript, ASP.NET Core, EF Core

- **Status:** Accepted
- **Date:** 2026-11-23

## Context

The MVP must be delivered in four weekly sprints by one developer with about one year of C# experience and early experience with React and TypeScript. The project should also show full-stack skills in a portfolio.

## Decision

- **Front-end:** React + TypeScript, created with Vite.
- **Back-end:** C# with ASP.NET Core Web API.
- **Data access:** Entity Framework Core with migrations.
- **Database:** SQLite for local development and PostgreSQL in production.

## Consequences

- The back-end uses the developer's strongest skill, which lowers the risk of delay.
- SQLite needs no installation locally. Free hosting providers usually have temporary file systems, so production uses PostgreSQL to keep data between restarts.
- Switching databases only changes the EF Core provider and the connection string, but both must be tested, since SQL behavior can differ slightly.
