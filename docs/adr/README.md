# Architecture Decision Records (ADRs)

An ADR is a short document that records one important technical decision: the context, what was decided and its consequences. ADRs are never rewritten. If a decision changes, a new ADR is added and the old one is marked as **Superseded**.

## Index

| # | Decision | Status |
|---|---|---|
| [0001](0001-use-monorepo.md) | Use a monorepo for front-end and back-end | Accepted |
| [0002](0002-english-as-repository-language.md) | English as the repository language | Accepted |
| [0003](0003-tech-stack.md) | Tech stack: React + TypeScript, ASP.NET Core, EF Core | Accepted |
| [0004](0004-users-and-campaign-members-with-roles.md) | Users and campaign members with roles | Accepted |
| [0005](0005-audit-fields-via-base-entity.md) | Audit fields through a `BaseEntity` class | Accepted |
| [0006](0006-git-workflow.md) | Git workflow: GitHub Flow and Conventional Commits | Accepted |
| [0007](0007-mvp-access-via-campaign-codes.md) | MVP access through campaign codes, without login | Accepted |
| [0008](0008-race-class-subclass-as-free-text.md) | Race, class and subclass as free text in the MVP | Accepted |

## Template

Copy this when adding a new ADR, using the next number:

```markdown
# NNNN. Title of the decision

- **Status:** Proposed | Accepted | Superseded by [NNNN](NNNN-file.md)
- **Date:** YYYY-MM-DD

## Context
What problem or situation requires a decision?

## Decision
What was decided.

## Consequences
What becomes easier, what becomes harder, and what to watch for.
```
