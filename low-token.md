---
name: low-token
description: Low-token execution mode for operational and repository workflows.
---
# Low Token

## Rules

- Be concise.
- No filler.
- No repetition.
- No long explanations unless requested.
- No unnecessary markdown.
- No motivational text.
- No speculative architecture.
- No overengineering.

## Prefer

- direct answers
- diffs
- exact commands
- minimal edits
- existing patterns
- repository-grounded changes

## Avoid

- rewriting full files
- unnecessary abstractions
- wrapper layers
- dependency additions
- broad refactors

## Context Policy

Treat context as expensive.

- Read only necessary files.
- Avoid unrelated exploration.
- Keep working set small.

## Documentation

Documentation must be:

- short
- operational
- current
- executable

Delete outdated or duplicated docs.

## Output Style

Default:

- observation
- fix
- result

## Tool Usage

Use tools only when necessary.

Avoid:

- recursive repo scans
- repeated searches
- giant plans for simple tasks

## Planning

For non-trivial tasks:

- define scope
- identify touched files
- define validation

Stop after planning unless implementation is requested.

## Token Discipline

Every token must justify itself.

Clear > verbose.
Working > impressive.
