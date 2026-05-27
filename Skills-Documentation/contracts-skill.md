# Contracts Documentation Skill

## Purpose

Create contract documentation that defines:

- stable system guarantees
- interfaces between components
- invariants that must remain true
- ownership expectations
- artifact or API expectations

Contracts documentation protects systems from architectural drift.

It is not:
- architecture documentation
- operational documentation
- historical reasoning
- implementation walkthroughs

---

# Core Philosophy

Good contract documentation:

- defines guarantees explicitly
- reduces ambiguity
- stabilizes system interactions
- clarifies ownership
- improves safe evolution
- helps AI agents avoid breaking invariants

Contracts should optimize for:

- precision
- stability
- explicit boundaries
- low ambiguity
- long-term compatibility

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

    related_components:
    related_docs:
    tags:

Avoid excessive metadata.

---

# Recommended Structure

A strong contract document usually contains:

## 1. Purpose

Explain what the contract governs.

Examples:

- artifact storage
- event envelopes
- pipeline stages
- naming conventions
- API payloads
- runtime interfaces

Keep this section concise.

---

## 2. Scope

Define:

- what is covered
- which systems participate
- which boundaries the contract applies to

Contracts should have explicit ownership boundaries.

---

## 3. Guarantees

Define stable guarantees explicitly.

Examples:

- deterministic naming
- immutable identifiers
- required fields
- stable locations
- ordering guarantees
- compatibility guarantees

Guarantees should be precise and inspectable.

---

## 4. Invariants

Define rules that must remain true across future system evolution.

Examples:

- artifact locations
- ID formats
- schema guarantees
- lifecycle rules
- ownership constraints
- validation requirements

Invariants should remain stable over time.

---

## 5. Inputs and Outputs

If applicable, define:

- accepted inputs
- produced outputs
- expected structure
- validation expectations

Examples:

- payload schemas
- file structures
- event envelopes
- stage outputs

Focus on interfaces, not implementation.

---

## 6. Failure Expectations

Describe important failure behaviors.

Examples:

- retry expectations
- validation failures
- partial failure behavior
- idempotency guarantees
- recovery assumptions

Focus on contract-level behavior.

---

## 7. Related Documents

Link related:

- architecture documents
- operations
- decisions
- modules
- schemas

Contracts should remain connected to surrounding system context.

---

# Writing Style

Prefer:

- explicit wording
- deterministic language
- stable terminology
- concise sections
- inspectable guarantees

Good contract documentation should feel:

- precise
- stable
- enforceable
- trustworthy

---

# What To Avoid

Avoid:

- architectural reasoning
- operational commands
- troubleshooting procedures
- implementation walkthroughs
- vague wording
- unstable terminology
- hidden assumptions

Contracts should remain invariant-focused.

---

# AI-Agent Compatibility

Contracts documents should help agents:

- identify safe assumptions
- understand boundaries
- preserve invariants
- avoid breaking interfaces
- reason safely about compatibility

Agents should treat contracts as high-trust system guarantees.

---

# Scaling Rule

As systems grow:

- split contracts into focused documents
- keep contracts narrowly scoped
- avoid giant universal contracts
- maintain stable terminology
- preserve backward compatibility expectations explicitly

Contracts should scale through modularity, not centralization.

---

# Guiding Principle

Contracts documentation explains:

- which guarantees exist
- which invariants must remain true
- which interfaces systems depend on
- which assumptions are considered stable

It should define the stable agreements that allow systems and components to evolve safely.