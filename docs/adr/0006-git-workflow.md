# 0006. Git workflow: GitHub Flow and Conventional Commits

- **Status:** Accepted
- **Date:** 2026-11-25

## Context

Even with one developer, the repository should show how work is done in a team: small, reviewed and traceable changes, and a `main` branch that always works.

## Decision

- **GitHub Flow:** `main` is always deployable. All work happens in short-lived branches that are merged into `main` through pull requests.
- **Branch names:** `type/short-description`, for example `feat/campaign-endpoints` or `docs/architecture-decisions`.
- **Commit messages:** [Conventional Commits](https://www.conventionalcommits.org/), for example `feat: add campaign creation endpoint`.
- **Protected `main`:** a repository rule requires a pull request to change `main`. Approvals are set to zero, because GitHub does not allow approving your own pull request.

Details are in [CONTRIBUTING.md](../../CONTRIBUTING.md).

## Consequences

- The history shows what changed, why and when.
- Every change can be reviewed before it reaches `main`.
- Each task in the project board maps to one branch and one pull request.
- Small changes take a few extra steps compared with committing directly to `main`.
