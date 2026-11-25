# 0008. Race, class and subclass as free text in the MVP

- **Status:** Accepted
- **Date:** 2026-11-23

## Context

A character has a race, a class and a subclass, and the subclass depends on the class. These could be lookup tables, with subclasses filtered by class, or free text. Each tabletop RPG system has its own races and classes, and game masters often create custom ones.

## Decision

Store `Race`, `Class` and `Subclass` as free text in the MVP.

## Consequences

- Works with any RPG system and with homebrew content.
- No validation that a subclass belongs to the class, and typos can create inconsistent values.
- If lookup lists are added later, the existing text must be migrated to the new tables. This should be recorded in a new ADR.
