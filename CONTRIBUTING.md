# Contributing

How work is done in this repository. The reasons behind these rules are in [ADR 0006](docs/adr/0006-git-workflow.md).

## Workflow

1. Update your local `main`:
   ```bash
   git checkout main
   git pull
   ```
2. Create a branch for the task:
   ```bash
   git checkout -b feat/short-description
   ```
3. Commit your work in small steps.
4. Push the branch:
   ```bash
   git push -u origin feat/short-description
   ```
5. Open a pull request into `main`, review the changes and merge.
6. Delete the branch after merging.

## Branch names

`type/short-description`, in lowercase with hyphens.

| Type | Use for |
|---|---|
| `feat` | A new feature |
| `fix` | A bug fix |
| `docs` | Documentation only |
| `refactor` | Code changes that do not change behavior |
| `test` | Adding or fixing tests |
| `chore` | Setup, configuration, dependencies |

Examples: `feat/character-cards`, `fix/invite-link`, `docs/architecture-decisions`.

## Commit messages

Follow [Conventional Commits](https://www.conventionalcommits.org/): `type: short description`, in English and in the imperative.

```
feat: add campaign creation endpoint
fix: prevent duplicate campaign members
docs: add data model documentation
```

Use a scope when it helps: `feat(api): ...`, `feat(web): ...`.

## Pull requests

- One task per pull request.
- The title follows the commit format, for example `feat: add character cards grid`.
- The description says **what** changed, **why**, and **how to test** it.
- Before merging, check that the project builds and the tests pass.

## Documentation

- Important technical decisions get a new ADR in [`docs/adr`](docs/adr/README.md).
- Changes to the database update [`docs/data-model.md`](docs/data-model.md).
