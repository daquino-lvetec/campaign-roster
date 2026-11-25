# 0004. Users and campaign members with roles

- **Status:** Accepted
- **Date:** 2026-11-23

## Context

Everyone in a campaign takes part in the game, but with different roles: the game master proposes challenges and applies the rules, and the players build the story through their choices. Modeling this as a `Player` table with a "master" role is confusing. The same person can also be the master in one campaign and a player in another.

Options considered:

1. A single `Participant` table with a `Role` column — simple, but the same person in two campaigns becomes two unrelated records.
2. A `User` table plus a `CampaignMember` join table with a `Role` — models a person and their role in each campaign separately.
3. The master as a field in `Campaign` and a `Player` table — simplest, but treats the master differently and makes co-masters or a change of master hard.

## Decision

Use option 2: `User` (the person) and `CampaignMember` (`UserId`, `CampaignId`, `Role`), where `Role` is `Master` or `Player`. A `Character` points to the `CampaignMember` that owns it, not directly to the `User`.

## Consequences

- When login is added in v2, it only needs new columns on `User`; the model does not change.
- A character can only be assigned to someone who belongs to its campaign.
- A unique index on (`UserId`, `CampaignId`) prevents adding the same person twice to a campaign.
- The master can also own characters (for example NPCs) if that is needed later.
