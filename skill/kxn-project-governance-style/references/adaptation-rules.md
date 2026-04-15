# Adaptation Rules

## Keep The Governance Moves, Drop The Case-Specific Names

Translate repository-specific implementation names into generic categories.

Examples:

- workspace-first routing -> ownership should follow the primary operating context
- Feishu UI boundary -> surface-specific view and interaction boundaries
- `/preview` fallback -> unified fallback access path for generated artifacts
- setup redesign -> onboarding and capability-discovery information architecture
- token usage plumbing -> shared telemetry or usage substrate before presentation

## What Must Stay Generic In The Main Skill

- no original command names
- no original route names
- no adapter or projector type names
- no repository-specific product labels

## When To Mention Source Specifics

Only references should mention:

- issue numbers
- commit SHAs
- exact file paths
- source repository name

## Failure Test For Abstraction

If the skill becomes meaningless once the original repo name and path names are hidden, the abstraction is not strong enough yet.
