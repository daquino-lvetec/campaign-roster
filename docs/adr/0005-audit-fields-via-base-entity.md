# 0005. Audit fields through a `BaseEntity` class

- **Status:** Accepted
- **Date:** 2026-11-23

## Context

Every table should record when a record was created and changed, and by whom. Adding these columns later, when data already exists, is harder than adding them from the start. Repeating the same five properties in every entity class is error-prone.

## Decision

All entities inherit from an abstract `BaseEntity` class with `Id`, `CreatedAt`, `CreatedBy`, `UpdatedAt` and `UpdatedBy`. `BaseEntity` is not a table: Entity Framework Core adds its columns to the table of each entity. `CreatedAt` and `UpdatedAt` are filled automatically when changes are saved.

## Consequences

- Audit columns are defined in one place and are consistent across tables.
- `CreatedBy` and `UpdatedBy` stay optional until there is login, because the system cannot reliably know who made a change before that.
- New entities must inherit from `BaseEntity` to get auditing.
