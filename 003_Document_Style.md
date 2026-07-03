# 003 Document Style

> The Canonical Documentation Standard of the MarkOrbit Professional Operating System

Version: 2.0

Status: Active

Applies To

- Core Specification
- Platform Specification
- Runtime Specification
- Extension Specification
- API Specification
- Design Documents
- RFC Documents
- Architecture Reviews

---

# Purpose

Architecture should be communicated consistently.

A consistent documentation style improves readability, maintainability and architectural integrity.

Every architectural document in MarkOrbit should follow one unified writing style.

---

# Documentation Philosophy

Documentation is architecture.

Documentation is not marketing.

Documentation is not implementation.

Documentation should describe professional architecture with precision, stability and consistency.

Every document should be readable independently.

Every document should also integrate naturally into the complete specification.

---

# Writing Principles

Every document should satisfy six principles.

## Consistent

Documents follow one structure.

---

## Professional

Use professional terminology.

Avoid marketing language.

---

## Technology Independent

Describe architecture.

Avoid implementation details.

---

## Explainable

Readers should understand why a design exists.

Not only what it does.

---

## Stable

Architecture changes slowly.

Documentation should avoid implementation-specific language.

---

## Reusable

Documents should remain useful for many future versions.

---

# Standard Document Structure

Every Specification document should follow this order.

```text
Title

Version

Status

Depends

Related

Purpose

Philosophy

Scope

Responsibilities

Architecture

Characteristics

Categories

Core Definitions

Validation

Runtime

Relationships

Compatibility

Extension

Non Goals

Examples

Design Principles

Summary
```

Do not reorder sections unless necessary.

---

# Required Sections

Every Specification should include the following.

## Title

Use

```
# XXX Specification
```

Example

```
# Capability Specification
```

---

## Version

Specify architectural version.

Example

```
Version

2.0
```

---

## Status

One of:

```
Draft

Review

Architecture Freeze

Active

Deprecated
```

---

## Depends

List prerequisite specifications.

Example

```
Depends

170_Contract_Model.md

620_Execution_Model.md
```

---

## Related

List associated specifications.

---

## Purpose

Always answer one question.

```
The purpose of ...

... answers one question.

> ...
```

Every specification should define one primary architectural question.

---

## Philosophy

Explain why the architecture exists.

Do not describe implementation.

---

## Scope

Clearly define what belongs to this specification.

Equally important:

State what does NOT belong.

---

## Responsibilities

Separate ownership.

Always include:

```
Owns

Does not own
```

Responsibilities should never overlap.

---

## Architecture

Every document should include one architecture diagram.

Use simple text diagrams.

Example

```text
Knowledge

↓

Reasoning

↓

Execution
```

Avoid complicated diagrams.

---

## Characteristics

Describe architectural qualities.

Typical characteristics include:

- Explainable
- Reusable
- Versioned
- Observable
- Extensible
- Configurable

Use only relevant characteristics.

---

## Categories

List major reusable categories.

Each category should include examples.

---

## Validation

Every specification defines validation rules.

Validation verifies architecture.

Not implementation.

---

## Runtime

Separate Definition from Runtime.

Describe:

- Definition
- Runtime Instance
- Published Product

Never mix them.

---

## Relationships

Explicitly describe relationships with other architectural layers.

Example

```
Relationship to Workflow

Relationship to Guide

Relationship to Workspace
```

---

## Compatibility

Describe compatibility expectations.

Examples

- Versioning
- Migration
- Backward Compatibility

---

## Extension

Describe future extension points.

Extensions should preserve architectural principles.

---

## Non Goals

Every document must explicitly define what it is NOT.

This prevents architectural ambiguity.

---

## Examples

Provide architectural examples.

Do not provide implementation code.

Prefer diagrams.

---

## Design Principles

Summarize architectural principles.

Usually between three and six principles.

---

## Summary

End every document with a concise summary.

One or two paragraphs.

---

# Writing Style

Use concise language.

Example

✓

```
Capability performs professional work.
```

Avoid

```
Capability is designed to perform professional work in a highly flexible and scalable manner.
```

---

Use present tense.

Example

```
Guide presents experiences.
```

Avoid

```
Guide will present experiences.
```

---

Prefer short sentences.

Avoid long paragraphs.

---

# Terminology

Always use Professional Vocabulary.

Never introduce synonyms.

Example

Use

```
Interaction
```

Not

```
Conversation

Wizard

Dialogue
```

---

# Tables

Use tables only when comparison improves clarity.

Example

| Layer | Responsibility |
|--------|----------------|
| Brain | Understanding |
| Capability | Action |

Avoid unnecessary tables.

---

# Diagrams

Prefer plain text diagrams.

Example

```text
Facts

↓

Understanding

↓

Judgment

↓

Action
```

Rules

- Top-down only
- Simple arrows
- One concept per line
- Avoid ASCII art

---

# Lists

Prefer short unordered lists.

Avoid nested lists deeper than two levels.

Good

```
- Knowledge
- Capability
- Workflow
```

Avoid

```
1.
  a.
    i.
```

---

# Examples

Examples should describe architecture.

Not implementation.

Good

```
Trademark Filing

↓

Capability Product

↓

Guide Product
```

Avoid

```
Python

Java

SQL
```

---

# Code Blocks

Architecture documents should minimize code.

When code is necessary:

- use pseudocode
- avoid implementation language
- focus on concepts

---

# References

Depends

Required architectural dependencies.

Related

Conceptually associated specifications.

Do not confuse the two.

---

# Cross References

Always reference files by canonical filename.

Example

```
620_Execution_Model.md
```

Avoid

```
Execution Model

Capability Model
```

---

# File Length

Recommended length

1,500–4,000 words.

Avoid extremely short specifications.

Avoid excessively long chapters.

Split when necessary.

---

# Revision Rules

Architectural revisions should preserve:

- terminology
- section order
- responsibilities
- architectural consistency

Editorial improvements are encouraged.

Architectural changes require review.

---

# Review Checklist

Before approving any document verify:

✓ Correct document structure

✓ Canonical terminology

✓ One responsibility

✓ Clear purpose

✓ Explicit scope

✓ Runtime separated from Definition

✓ Examples included

✓ Non Goals included

✓ Summary included

✓ Cross references valid

---

# Final Principle

Every document should answer one architectural question.

Every document should own one architectural responsibility.

Every document should strengthen one consistent Professional Operating System.

Documentation is part of the architecture.

Therefore, documentation should be designed with the same discipline as software.