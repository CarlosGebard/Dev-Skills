# Architecture Documentation Skill

## Purpose

Create architecture documentation that helps humans and AI agents understand:

- how a system is shaped
- how major components interact
- where boundaries exist
- how ownership is distributed
- how data or artifacts flow through the system

Architecture documentation explains system structure and composition.

It is not:
- repository onboarding
- operational documentation
- implementation walkthroughs
- decision history
- contract specification

---

# Core Philosophy

Good architecture documentation:

- explains system shape clearly
- exposes boundaries explicitly
- reduces hidden coupling
- clarifies ownership
- makes flows understandable
- improves safe system evolution
- helps agents reason about structure safely

Architecture documentation should optimize for:

- clarity
- navigability
- structural reasoning
- composability
- long-term maintainability

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

Optional:

    related_docs:
    related_modules:
    tags:

Avoid excessive metadata.

---

# Recommended Structure

A strong architecture document usually contains:

## 1. Architectural Overview

Describe the overall system shape.

Examples:

- modular monolith
- orchestration system
- distributed pipeline
- event-driven system
- agent runtime
- processing platform

Focus on structural understanding.

Do not explain historical reasoning here.

---

## 2. Major Components

Describe the major system components.

Each component should explain:

- responsibility
- ownership
- inputs
- outputs
- dependencies
- boundaries

Focus on structural roles, not implementation details.

---

## 3. System Boundaries

Explicitly define:

- internal boundaries
- external systems
- ownership limits
- responsibility separation

Architecture quality improves dramatically when boundaries are visible.

---

## 4. Runtime Flow

Describe the high-level runtime flow of the system.

Focus on:

- orchestration
- processing stages
- component interaction
- lifecycle transitions
- runtime sequencing

Prefer simple flows over exhaustive detail.

---

## 5. Artifact or Data Flow

If the system processes data or artifacts, explain:

- major artifacts
- stage transitions
- ownership transitions
- persistence locations
- lifecycle movement

Examples:

- documents
- jobs
- claims
- embeddings
- events
- batches
- runtime state

Focus on movement through the system.

Do not define strict invariants here.

---

## 6. Quality Attributes

Describe important architectural qualities.

Examples:

- scalability
- reliability
- observability
- recoverability
- reproducibility
- performance
- operational transparency

Focus on architectural consequences.

Avoid operational procedures.

---

## 7. External Dependencies

Describe important external systems that influence architecture.

Examples:

- databases
- queues
- object storage
- orchestration platforms
- external APIs

Only include dependencies relevant to system structure.

---

## 8. Documentation Links

Link related documents:

- Operations
- Decisions
- Contracts
- Runbooks
- Modules
- Related repositories

Architecture documents should help readers navigate deeper system areas safely.

---

# Writing Style

Prefer:

- concise sections
- explicit ownership
- stable terminology
- lightweight diagrams
- strong boundaries
- deterministic language

Good architecture documentation should feel:

- inspectable
- intentional
- composable
- trustworthy

---

# What To Avoid

Avoid:

- onboarding explanations
- operational commands
- troubleshooting procedures
- implementation walkthroughs
- historical reasoning
- contract specifications
- invariants
- giant diagrams
- excessive code snippets

Architecture should remain structure-focused.

---

# AI-Agent Compatibility

Architecture documents should help agents:

- identify system shape
- understand component ownership
- understand runtime flow
- identify dependencies
- locate system boundaries
- navigate safely toward implementation

Agents should understand system composition before modifying code.

---

# Scaling Rule

As systems grow:

- move decisions into dedicated decision documents
- move invariants into contracts
- move runtime procedures into operations
- split domains into dedicated modules
- keep architecture focused on structure and interaction

Architecture should scale through decomposition, not document size.

---

# Guiding Principle

Architecture documentation explains:

- how the system is shaped
- how major parts interact
- where boundaries exist
- how ownership is distributed

It should help humans and agents reason safely about system structure without mixing operational, contractual, or historical concerns.