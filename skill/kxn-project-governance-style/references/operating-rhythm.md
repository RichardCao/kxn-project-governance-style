# Operating Rhythm

## Default Cadence

1. Restate the work as an implementation contract.
2. Identify the source of truth, shared definition, or state boundary first.
3. Split the plan into stages.
4. Land the primary path.
5. Revisit hidden structure debt, compatibility edge cases, and user-facing semantics.
6. Lock behavior with docs, tests, or state-machine notes.

## What This Style Optimizes For

- reduced scope drift
- clearer ownership boundaries
- safer delivery of cross-surface behavior
- better survivability under fallback and compatibility stress

## Anti-Patterns

- adding a new surface without first clarifying the shared model
- leaving old paths alive after the new path becomes primary
- treating maintainability as unplanned leftover work
- delaying failure semantics until after rollout
- accepting "it works" when the interaction model still mismatches the intended user journey
- changing product wording or route structure as a late cosmetic task instead of part of the main execution path

## Review Questions

- Is the issue or plan specific enough to act as a contract?
- What is the source of truth here?
- Which old paths should be removed, not just bypassed?
- Is there a staged plan, or is everything being attempted in one opaque rewrite?
- Which risk, fallback, rollback, or expiry semantics belong in the mainline?
- Which docs or tests need to move with this change?
- Does the user-facing structure match the intended task flow, not just the implementation structure?
