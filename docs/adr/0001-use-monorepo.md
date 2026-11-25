# 0001. Use a monorepo for front-end and back-end

- **Status:** Accepted
- **Date:** 2026-11-25

## Context

The project has a React front-end and an ASP.NET Core API. They could live in two repositories (polyrepo) or in one (monorepo). Polyrepos fit separate teams, independent release cycles and APIs consumed by many clients. Here, one developer builds both parts, and most features change the API and the front-end together.

## Decision

Keep both parts in a single repository, each in its own top-level folder (`backend/` and `frontend/`), treated as independent projects with their own build, conventions and deployment.

## Consequences

- A feature that touches both parts is delivered and reviewed in a single pull request.
- One repository shows the whole project, its documentation and history.
- CI must run only the checks of the part that changed, using path filters.
- Hosting must be configured to deploy each subfolder separately.
- If the API ever serves other clients or other teams join, splitting the repository can be reconsidered in a new ADR.
