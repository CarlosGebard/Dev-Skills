# System Context Documentation Skill

## Purpose

Create lightweight system context documentation that helps humans and AI agents quickly understand:

- why a repository exists
- what the repository owns
- how the documentation is organized
- which concepts define the system
- where deeper documentation lives

System Context documentation acts as the stable entrypoint to the repository.

It should optimize for orientation and navigation.

It is not architecture documentation, operational documentation, or implementation documentation.

---

# Core Philosophy

Good System Context documentation:

- explains purpose before structure
- reduces onboarding friction
- defines repository boundaries early
- exposes important terminology
- provides navigational clarity
- helps agents build an initial mental model safely

System Context should remain:

- lightweight
- stable
- easy to scan
- low maintenance

---

# Recommended Metadata

Use lightweight YAML frontmatter.

Minimum:

    ---
    id:
    title:
    status:
    updated_at:
    owners:
    ---

Avoid excessive metadata.

---

# Recommended Structure

A strong System Context document usually contains:

## 1. Purpose

Explain:

- why the repository exists
- which problem it solves
- which role it plays

Keep this section concise.

---

## 2. System Goals

Describe the major goals guiding the repository.

Examples:

- deterministic processing
- operational simplicity
- contract-first design
- reproducible execution
- explicit boundaries

Optionally define non-goals.

---

## 3. Repository Scope

Explicitly define:

- what the repository owns
- major responsibilities
- what is intentionally out of scope

Clear boundaries improve reasoning quality significantly.

---

## 4. Documentation Map

Link the important documentation areas.

Examples:

- Architecture
- Operations
- Decisions
- Contracts
- Modules
- Runbooks

System Context documents should function as navigation hubs.

---

## 5. Core Concepts

Define important repository terminology.

Examples:

- artifacts
- jobs
- stages
- claims
- bridges
- runtimes

Terminology should remain stable across the repository.

---

## 6. Repository Structure

Provide a lightweight overview of the repository layout.

Example:

```text
src/        → application code
config/     → runtime configuration
docs/       → system documentation
scripts/    → operational tooling
```
Avoid exhaustive repository trees.

---

## 7. Design Principles

Document important guiding principles.

Examples:

- deterministic pipelines
- explicit contracts
- low hidden state
- operational simplicity
- stable artifact ownership
- agent-friendly structures

Principles should remain relatively stable over time.

---

# Writing Style

Prefer:

- concise sections
- explicit wording
- stable terminology
- lightweight structure
- deterministic language

Good System Context documentation should feel:

- approachable
- stable
- easy to navigate
- trustworthy

---

# What To Avoid

Avoid:

- implementation walkthroughs
- operational commands
- deep architectural explanations
- troubleshooting steps
- giant repository trees
- duplicated documentation
- excessive diagrams

System Context should remain lightweight and orientation-focused.

---

# AI-Agent Compatibility

System Context documents should help agents:

- understand repository purpose
- identify repository boundaries
- learn terminology
- locate high-trust documentation
- navigate safely toward deeper documents

Agents should understand repository intent before reading implementation code.

---

# Scaling Rule

As repositories grow:

- move architecture into dedicated documents
- move operations into runbooks
- move invariants into contracts
- move reasoning into decisions
- keep System Context lightweight

System Context should scale through navigation, not size.

---

# Guiding Principle

System Context documentation explains:

- why the repository exists
- what it owns
- how documentation is organized
- how readers should navigate the system

It should function as the lightweight entrypoint to the repository ecosystem.