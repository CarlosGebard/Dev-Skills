---
name: planner
description: Build a concise, repository-grounded execution plan for non-trivial engineering work. Use before code, infra, CI/CD, database, data pipeline, or architecture changes.
---

# Objective

Convert an engineering request into a minimal, safe, testable execution plan grounded in the current repository state.

# Use this skill when

- the task spans multiple files
- the task affects architecture, infra, CI/CD, database, networking, storage, or runtime behavior
- the task changes public/internal contracts
- the task requires sequencing, migration, rollback, or validation
- the request is ambiguous or high-risk

# Do not use this skill when

- the task is trivial
- the user only wants an explanation
- the change is isolated and low-risk

# Procedure
Inspect the current repository before planning.

Read, in this order:

1. files directly related to the request
2. tests covering those files
3. runtime/config/deploy files that affect the change
4. contracts, schemas, migrations, interfaces, or API boundaries
5. nearby docs
6. `AGENTS.md` only for conventions, not system facts

Treat docs as low-trust unless confirmed by code, tests, configs, or contracts.

Stop before implementation unless the user explicitly asks to implement.

Do not infer repository structure beyond inspected evidence.

## Task classification

Classify the work using one or more labels:

- feature
- bugfix
- refactor
- infra
- CI/CD
- database
- networking
- storage
- observability
- security
- migration
- documentation
- data pipeline
- contract change

## Goal

Restate the request as one concrete engineering outcome.

## Non-goals

List what will not be changed.

Use this to prevent scope creep.

## Current state observations

List only concrete findings directly relevant to the plan.

## Milestones

Break work into small milestones.

For each milestone include:

- purpose
- expected outcome
- likely touch points
- validation commands

optional when relevant:
- rollback/recovery
- blockers/dependencies


# Output format

## Task classification

## Goal

## Non-goals

## Current state observations

## Likely touch points

## Milestones

# Quality bar

A good plan must be:
- minimal
- specific
- testable
- ordered
- explicit about assumptions and unknowns
- Prefer the smallest safe change that matches existing repository patterns.
