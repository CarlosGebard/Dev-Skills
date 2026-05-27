# Operations Documentation Skill

## Purpose

Create operations documentation that helps humans and AI agents safely operate, execute, debug, deploy, and maintain a system.

Operations documentation explains how the system behaves at runtime and how operators interact with it safely.

It is not:
- architecture documentation
- repository onboarding
- historical reasoning
- contract specification
- implementation walkthrough documentation

---

# Core Philosophy

Good operations documentation:

- prioritizes operational clarity
- minimizes runtime ambiguity
- explains execution workflows explicitly
- improves recoverability
- reduces operational friction
- helps agents perform tasks safely
- keeps runtime procedures inspectable

Operations documentation should optimize for:

- practical execution
- operational safety
- recoverability
- reproducibility
- low ambiguity
- fast troubleshooting

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

    related_services:
    related_docs:
    tags:

Avoid excessive operational ceremony.

---

# Recommended Structure

A strong operations document usually contains:

## 1. Operational Overview

Briefly explain:

- what operational responsibilities exist
- how the system is typically executed
- which runtime environments exist
- which workflows matter operationally

Focus on runtime understanding.

Avoid architecture duplication.

---

## 2. Runtime Environments

Describe important environments.

Examples:

- local development
- staging
- production
- offline processing
- CI execution
- containerized runtime

Clarify important operational differences between environments.

---

## 3. Execution Workflows

Document common execution flows.

Examples:

- local startup
- pipeline execution
- synchronization workflows
- batch processing
- scheduled jobs
- ingestion flows
- deployment flow

Focus on operator actions and runtime lifecycle.

Commands should remain copy-paste-friendly.

---

## 4. Configuration

Explain important runtime configuration.

Examples:

- environment variables
- config files
- secrets sources
- runtime flags
- feature toggles

Clarify:

- which configuration is required
- which configuration is optional
- where configuration is loaded from

Avoid duplicating full schema definitions.

---

## 5. Observability

Describe how the system is monitored and inspected.

Examples:

- logs
- metrics
- tracing
- dashboards
- runtime outputs
- health checks

Explain how operators validate system behavior safely.

---

## 6. Failure and Recovery

Document important operational recovery expectations.

Examples:

- retry behavior
- restart procedures
- partial failure handling
- cleanup workflows
- idempotent reruns
- artifact recovery
- rollback expectations

Focus on operational resilience.

---

## 7. Troubleshooting

Document common operational problems.

Examples:

- dependency failures
- missing configuration
- API quota issues
- filesystem problems
- resource exhaustion
- container failures

Prefer concise troubleshooting guidance.

Avoid giant debugging dumps.

---

## 8. Operational Boundaries

Clarify what operations documentation owns.

Examples:

Owns:
- execution workflows
- runtime procedures
- deployment steps
- monitoring guidance

Does not own:
- architecture reasoning
- stable contracts
- implementation details
- historical decisions

Strong operational boundaries reduce documentation drift.

---

## 9. Related Documentation

Link related documents:

- System Context
- Architecture
- Contracts
- Decisions
- Runbooks
- Modules

Operations documents should help readers navigate deeper operational context safely.

---

# Writing Style

Prefer:

- concise sections
- copy-paste-friendly commands
- deterministic wording
- explicit operational flows
- stable terminology
- low ambiguity

Good operations documentation should feel:

- practical
- reliable
- executable
- operationally safe

---

# What To Avoid

Avoid:

- deep architecture explanation
- historical reasoning
- giant command dumps
- implementation walkthroughs
- vague operational guidance
- duplicated documentation
- excessive theory
- hidden assumptions

Operations documentation should remain runtime-focused.

---

# AI-Agent Compatibility

Operations documents should help agents:

- execute workflows safely
- understand runtime expectations
- debug operational issues
- identify required configuration
- recover from common failures
- avoid unsafe operational assumptions

Agents should treat operations documents as the primary runtime authority.

---

# Scaling Rule

As systems grow:

- split large operational areas into runbooks
- keep operational procedures task-focused
- move invariants into contracts
- move reasoning into decisions
- avoid giant centralized operations documents

Operations documentation should scale through decomposition, not expansion.

---

# Guiding Principle

Operations documentation explains:

- how the system runs
- how operators interact with it
- how runtime workflows behave
- how failures are handled safely

It should help humans and agents operate systems confidently without mixing architectural or historical concerns.