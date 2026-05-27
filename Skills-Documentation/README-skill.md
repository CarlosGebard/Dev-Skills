# README Documentation Skill

## Purpose

Create lightweight README documentation that helps humans quickly understand:

- what the repository is
- what the repository does
- how to start using it
- where deeper documentation exists
- what the repository owns

README documentation acts as the primary human-facing entrypoint to the repository.

It should optimize for fast onboarding and practical usage.

It is not:
- architecture documentation
- operational documentation
- decision history
- contract specification
- implementation walkthrough documentation

---

# Core Philosophy

Good README documentation:

- explains purpose immediately
- minimizes onboarding friction
- prioritizes practical usage
- remains lightweight
- exposes repository ownership clearly
- links deeper documentation instead of duplicating it

README files should optimize for:

- readability
- quick scanning
- practical onboarding
- navigability
- low maintenance

README files are primarily for humans.

---

# Recommended Structure

A strong README usually contains:

## 1. Repository Title

Repository name at the top.

Example:

```md
# victus-processing
```
## 2. Short Description

One or two short paragraphs explaining:

- what the repository does
- what role it plays
- what problem it solves

Readers should understand the repository quickly without reading the entire codebase.

Avoid deep technical explanation.

---

## 3. Localization Link

If the primary README is written in English, include a localized README link when useful.

Recommended:

```
[Español](docs/README.es.md)
```

Localized READMEs should:

- remain lightweight
- preserve the same structure
- prioritize accessibility
- avoid diverging from the primary README

The English README should remain the canonical source when possible.

---

## 4. Quick Start

Explain the minimal setup required to run the repository.

Examples:

- dependencies
- installation
- sync commands
- CLI inspection
- first execution flow

Quick Start should prioritize:

- copy-pasteability
- low friction
- fast success

Avoid excessive setup explanation.

---

## 5. Validation

Optionally include:

- smoke tests
- validation commands
- sanity-check commands

Keep this section lightweight.

---

## 6. Documentation Links

Link deeper documentation.

Examples:

- Architecture
- Operations
- Contracts
- CLI
- Modules
- Runbooks

README files should function as navigation entrypoints, not documentation dumps.

---

## 7. Responsibilities

Clearly define:

- what the repository owns
- what the repository does not own

Explicit ownership boundaries reduce confusion significantly.

Examples:

Owns:

- local processing
- orchestration
- artifact generation

Does not own:

- infrastructure
- analytics
- deployment
- external provider behavior

---

# Writing Style

Prefer:

- short paragraphs
- lightweight structure
- practical wording
- stable terminology
- copy-paste-friendly commands
- deterministic language

Good README documentation should feel:

- approachable
- practical
- lightweight
- trustworthy

---

# What To Avoid

Avoid:

- giant READMEs
- deep architecture explanation
- operational runbooks
- troubleshooting dumps
- implementation walkthroughs
- excessive badges
- large diagrams
- duplicated documentation
- vendor marketing language

README files should remain onboarding-focused.

---

# AI-Agent Compatibility

README files may still help AI agents by providing:

- repository purpose
- repository boundaries
- entrypoint commands
- documentation navigation
- high-level ownership

However, README files should remain human-first.

Detailed reasoning belongs in dedicated documents.

---

# Scaling Rule

As repositories grow:

- move architecture into architecture documents
- move operations into runbooks
- move invariants into contracts
- move reasoning into decisions
- keep README lightweight

README files should scale through linking, not expansion.

---

# Guiding Principle

README documentation explains:

- what the repository is
- how to start using it
- what it owns
- where deeper documentation exists

It should provide fast human onboarding without attempting to document the entire system.