# 100 Specification Guide

> **The Engineering Standard for MarkOrbit Core Specification**

---

Version

**2.0**

Status

**In Progress**

Depends

- MarkOrbit Core Foundation v1.3
- README.md
- CONSTITUTION.md
- docs/02_Architecture.md
- docs/04_Ontology.md

Related

- 110_Registry_Framework.md
- 120_Identity_Specification.md
- 130_Relationship_Specification.md
- 140_Timeline_Specification.md
- 150_Event_Specification.md

---

# Purpose

Foundation defines what MarkOrbit is.

Specification defines how MarkOrbit is implemented.

The purpose of this document is to define the writing, design and engineering standards for all MarkOrbit Core Specification documents.

Every Specification document must follow this guide unless there is a clear architectural reason not to.

---

# Specification Philosophy

Specification is not vision.

Specification is not strategy.

Specification is not product planning.

Specification is an engineering contract.

A good Specification should allow a developer or AI coding agent to understand:

- what must be built;
- who owns the responsibility;
- what inputs are accepted;
- what outputs are produced;
- what contracts must remain stable;
- what lifecycle must be supported;
- what examples should pass;
- what must not be implemented.

Specification exists to reduce ambiguity.

---

# Relationship to Foundation

Foundation answers:

> What is MarkOrbit?

Specification answers:

> How should MarkOrbit be implemented?

Foundation is stable.

Specification is executable.

Foundation should not be rewritten by Specification.

Specification must always comply with Foundation.

If a Specification conflicts with Foundation, Foundation takes precedence.

---

# Specification Scope

MarkOrbit Core Specification v2.0 covers engineering standards for:

- Registry
- Identity
- Relationship
- Timeline
- Event
- Entity
- Data Products
- Brain Objects
- Knowledge Products
- Intelligence Objects
- Intelligence Products
- Capability Contracts
- Guide Context
- Workflow Definitions
- Workspace Models

It does not define user interface design.

It does not define marketing strategy.

It does not define pricing.

It does not define business-layer Journey or Marketplace design.

---

# Numbering Standard

Specification documents use numeric ranges.

```text
100–199   Core Engineering Standards
200–299   Entity Specifications
300–399   Data Specifications
400–499   Brain Specifications
500–599   Intelligence Specifications
600–699   Capability Specifications
700–799   Guide Specifications
800–899   Workflow Specifications
900–999   Workspace Specifications
```

Each document should keep its number permanently.

Numbers may be reserved.

Numbers should not be reused for unrelated concepts.

---

# Required Document Structure

Every Specification document should follow this structure.

```text
# Title

Version

Status

Depends

Related

---

Purpose

Responsibility

Owner

Scope

Non Goals

Core Concepts

Contracts

Inputs

Outputs

Lifecycle

States

Events

Validation Rules

Examples

Error Handling

Extension Points

Implementation Notes

Compatibility

Summary
```

Not every section must be long.

But every Specification must explicitly address the sections relevant to its concept.

---

# Version Standard

Every Specification document must declare a version.

Recommended format:

```text
Version: 2.0
```

Patch-level improvements may use:

```text
Version: 2.0.1
```

Version changes should follow this rule:

| Change Type | Version Change |
|------------|----------------|
| wording only | patch |
| examples only | patch |
| validation rule added | minor |
| contract changed | major |
| responsibility changed | major |

Contract changes must be treated carefully.

---

# Status Standard

Each Specification must declare a status.

Allowed values:

```text
Draft
Review
Stable
Deprecated
Archived
```

Meaning:

| Status | Meaning |
|--------|---------|
| Draft | being written |
| Review | ready for review |
| Stable | approved for implementation |
| Deprecated | should not be used for new implementation |
| Archived | historical reference only |

Implementation should only target Stable specifications unless explicitly instructed.

---

# Responsibility Standard

Every Specification must define exactly one primary responsibility.

Example:

```text
Identity Specification

Responsibility:

Provide stable, unique and traceable identifiers for all permanent MarkOrbit objects.
```

A Specification should not own multiple unrelated responsibilities.

If a document has more than one responsibility, split it.

---

# Owner Standard

Every Specification must define an architectural owner.

Examples:

| Specification | Owner |
|--------------|-------|
| Identity | Core |
| Entity | Entity Model |
| Timeline | Data |
| Brain Object | Brain |
| Capability Contract | Capability |
| Workflow Definition | Workflow |
| Guide Context | Guide |
| Workspace Model | Workspace |

Owner means architectural responsibility.

It does not mean human team ownership.

---

# Contract Standard

A Contract defines the stable external behavior of a concept.

Contracts are required for:

- Entity
- Data Product
- Brain Object
- Intelligence Product
- Capability
- Workflow
- Guide Context
- Workspace

A Contract should define:

- identity
- version
- inputs
- outputs
- required fields
- optional fields
- validation rules
- error behavior
- compatibility rules

Implementation may change.

Contract should remain stable.

---

# Input Standard

Every Specification that accepts input must define:

- input name
- input type
- required or optional
- validation rule
- default behavior
- failure behavior

Inputs should be explicit.

Implicit inputs should be avoided.

---

# Output Standard

Every Specification that produces output must define:

- output name
- output type
- required or optional
- meaning
- downstream consumer
- stability level

Outputs should be predictable.

Outputs should not depend on hidden implementation details.

---

# Lifecycle Standard

Every permanent object should define a lifecycle.

Example:

```text
Draft

↓

Active

↓

Updated

↓

Deprecated

↓

Archived
```

Lifecycle should answer:

- how the object is created;
- how it is updated;
- how it is versioned;
- how it is deprecated;
- how it is archived.

No permanent object should disappear silently.

---

# State Standard

State describes current condition.

Lifecycle describes long-term evolution.

The two must not be confused.

Example:

Workflow lifecycle:

```text
Defined

↓

Released

↓

Deprecated
```

Workflow instance state:

```text
Created

↓

Running

↓

Waiting Approval

↓

Completed

↓

Cancelled
```

Specifications must clearly distinguish lifecycle from state.

---

# Event Standard

Events describe meaningful changes.

Every Event should include:

- event identity
- event type
- subject
- timestamp
- actor
- source
- payload
- previous state when applicable
- resulting state when applicable

Events should be append-only whenever possible.

Events should update Timeline.

Events should not overwrite history.

---

# Validation Standard

Every Specification should define validation rules.

Validation rules may include:

- required fields
- allowed values
- uniqueness
- compatibility
- dependency checks
- permission checks
- business constraints

Invalid data should fail clearly.

Failure should explain what is missing or wrong.

---

# Example Standard

Every Specification should include examples.

Examples should be:

- realistic
- minimal
- executable where possible
- consistent with ontology
- easy for Codex to convert into tests

Good examples are part of the Specification.

Bad examples should be avoided.

---

# Error Handling Standard

Every executable Specification should define error behavior.

Errors should include:

- error code or type
- human-readable message
- recoverability
- suggested next action

Failure should never be silent.

Failure should help Guide, Workflow or human operators continue.

---

# Compatibility Standard

Specifications should preserve compatibility whenever possible.

Breaking changes must be explicit.

Compatibility should consider:

- previous versions
- stored data
- existing workflows
- existing capabilities
- existing workspaces

Backward compatibility is preferred.

Migration should be documented when breaking change is unavoidable.

---

# Extension Standard

Every Specification should define extension points.

Extension points may include:

- custom fields
- plugin hooks
- local configuration
- workspace overrides
- external integrations

Extension must not break Core responsibility.

Extension should preserve contract compatibility.

---

# Naming Standard

Specification names should be explicit.

Use:

```text
120_Identity_Specification.md
610_Capability_Contract.md
820_Workflow_State.md
```

Avoid vague names:

```text
Core.md
Common.md
Utils.md
AI.md
Manager.md
```

Names should describe responsibility.

---

# Language Standard

Specification language should be precise and executable.

Prefer:

```text
Capability MUST declare an input contract.
```

Avoid:

```text
Capability should probably include some input information.
```

Use requirement keywords consistently.

- MUST: required
- SHOULD: recommended
- MAY: optional
- MUST NOT: prohibited

---

# AI Agent Standard

Specifications are written for humans and AI coding agents.

Therefore each Specification should be:

- explicit
- structured
- consistent
- example-driven
- contract-oriented

AI agents should not infer missing architecture.

If a rule matters, it must be written.

---

# Non Goals

Specification v2.0 does not define:

- UI layout
- visual design
- marketing copy
- business pricing
- sales process
- legal advice content
- country-specific service details unless required by schema

Those belong to Product, Business Layer or Knowledge Products.

---

# Review Checklist

Before a Specification becomes Stable, it must answer:

1. What is its single responsibility?
2. Who owns it?
3. What contract does it expose?
4. What inputs does it accept?
5. What outputs does it produce?
6. What lifecycle does it follow?
7. What states can it enter?
8. What events does it produce or consume?
9. How does it fail?
10. How can it be extended?
11. How does it preserve compatibility?
12. Can Codex implement from it without guessing?

If the answer to question 12 is no, the Specification is not ready.

---

# Summary

This document defines how all MarkOrbit Core Specification documents should be written.

Foundation defines the permanent architecture.

Specification defines executable engineering standards.

Every Specification must be precise, stable, contract-oriented and implementation-ready.

The goal is simple:

> A developer or AI coding agent should be able to implement MarkOrbit Core from the Specification without guessing.