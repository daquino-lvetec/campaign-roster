# 0007. MVP access through campaign codes, without login

- **Status:** Accepted
- **Date:** 2026-11-23

## Context

A full authentication system (accounts, passwords, sessions, password recovery) does not fit in the four-week MVP. The game master still needs to share the campaign with players while keeping editing rights.

## Decision

Each campaign gets two random codes when it is created:

- **MasterCode** — gives full access to edit the campaign, its members and characters.
- **InviteCode** — gives read-only access, for players.

The front-end uses these codes in the links that the game master shares.

## Consequences

- The game master can share a campaign immediately, with no sign-up.
- Anyone who has the master link can edit the campaign, so the codes must be long and random, and the master link must not be shared.
- `CreatedBy` and `UpdatedBy` cannot be filled reliably until there is login ([ADR 0005](0005-audit-fields-via-base-entity.md)).
- When login arrives in v2, the master is identified by the `Master` role and `MasterCode` can be removed in a new ADR. `InviteCode` remains useful for invitations.
