# Decisions Documentation Skill

## Purpose

Create lightweight decision documentation that explains:

- why important technical decisions were made
- which tradeoffs were accepted
- which alternatives were considered
- which constraints influenced the outcome

Decision documentation preserves architectural reasoning over time.

It is not:
- architecture documentation
- operational documentation
- implementation detail
- changelog history
- contract specification

---

# Core Philosophy

Good decision documentation:

- captures reasoning explicitly
- reduces repeated debates
- preserves historical context
- exposes tradeoffs clearly
- helps future contributors reason safely
- helps AI agents understand intent behind system design

Decision documents should optimize for:

- clarity
- explicit reasoning
- low ambiguity
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

Recommended optional fields:

    supersedes:
    related_docs:
    tags:

Avoid excessive process metadata.

---

# Recommended Structure

A strong decision document usually contains:

## 1. Context

Explain the problem or constraint that required a decision.

Examples:

- scaling limitations
- operational complexity
- architectural inconsistency
- performance bottlenecks
- deployment friction
- ecosystem constraints

Context should explain why the decision mattered.

---

## 2. Decision

Describe the chosen solution clearly and directly.

Keep this section concise.

---

## 3. Tradeoffs

Explain important consequences.

Examples:

Positive:
- simpler deployment
- reduced coupling
- lower memory usage
- easier observability

Negative:
- reduced flexibility
- tighter constraints
- increased implementation complexity
- smaller ecosystem

Tradeoffs should remain explicit.

---

## 4. Alternatives Considered

Briefly document meaningful alternatives that were evaluated.

Explain why they were rejected.

Avoid exhaustive comparisons.

---

## 5. Consequences

Describe long-term implications.

Examples:

- migration requirements
- operational impact
- architectural constraints
- compatibility expectations
- future limitations

Focus on system-level consequences.

---

## 6. Related Documents

Link related:

- architecture documents
- contracts
- operations
- related decisions
- modules

Decision documents should remain connected to broader system context.

---

# Writing Style

Prefer:

- concise sections
- direct reasoning
- explicit tradeoffs
- stable terminology
- deterministic language

Good decision documentation should feel:

- intentional
- inspectable
- trustworthy
- historically useful

---

# What To Avoid

Avoid:

- implementation walkthroughs
- operational procedures
- architecture duplication
- giant historical narratives
- excessive theory
- meeting notes
- changelog-style updates

Decision documents should remain reasoning-focused.

---

# AI-Agent Compatibility

Decision documents should help agents:

- understand design intent
- understand tradeoffs
- avoid reverting intentional decisions
- identify architectural constraints
- reason safely about future modifications

Agents should understand why systems evolved in a particular direction.

---

# Scaling Rule

As systems grow:

- split decisions into dedicated files
- maintain stable identifiers
- avoid giant decision indexes
- keep reasoning concise
- preserve important tradeoffs explicitly

Decision systems should scale through decomposition, not verbosity.

---

# Guiding Principle

Decision documentation explains:

- why a decision was made
- which tradeoffs were accepted
- which constraints mattered
- how the decision influences the system

It should preserve architectural reasoning without mixing operational or structural documentation.