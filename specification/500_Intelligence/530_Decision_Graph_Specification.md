# 530 Decision Graph Specification

> **The Professional Decision Network of the MarkOrbit Operating System**

---

Version

**2.0**

Status

**Draft**

Depends

- 500_Intelligence_Specification.md
- 510_Intelligence_Object_Specification.md
- 520_Reasoning_Model_Specification.md

Related

- 540_Intelligence_Product_Specification.md
- 600_Capability_Specification.md

---

# Purpose

Professional decisions rarely exist in isolation.

One judgment influences another.

Some decisions enable future decisions.

Others introduce constraints.

The purpose of Decision Graph is to organize professional judgments into an explainable decision network.

Decision Graph answers one question.

> **How are professional decisions connected?**

---

# Decision Graph Philosophy

Knowledge Graph connects understanding.

Decision Graph connects judgment.

Workflow executes decisions.

Decision Graph is neither Workflow nor Process.

Decision Graph represents decision logic.

---

# Scope

Decision Graph represents reusable professional decision structures.

Examples include:

- Trademark Filing Decision
- Country Selection Decision
- Similarity Decision
- Goods Selection Decision
- Renewal Decision
- Portfolio Decision
- Enforcement Decision

Decision Graphs remain independent from execution.

---

# Responsibilities

Decision Graph owns:

- decision relationships
- dependency paths
- alternative branches
- constraints
- decision context

Decision Graph does not own:

- facts
- knowledge
- workflow
- execution

---

# Architecture

Every Decision Graph follows one structure.

```text
Intelligence Objects

↓

Reasoning Models

↓

Decision Graph

↓

Intelligence Products
```

Reasoning produces judgments.

Decision Graph organizes judgments.

---

# Characteristics

Every Decision Graph should satisfy:

## Explainable

Every decision path should be understandable.

---

## Context-aware

Different contexts may activate different paths.

---

## Connected

Professional decisions should not exist independently.

---

## Traceable

Every decision should reference its supporting reasoning.

---

## Versioned

Decision structures evolve through versioning.

---

# Decision Structure

Every decision consists of:

```text
Context

↓

Decision

↓

Alternative

↓

Constraint

↓

Outcome
```

A Decision Graph connects these structures.

---

# Decision Relationships

Typical relationships include:

```text
depends_on

enables

blocks

recommends

requires

conflicts_with

alternative_to

supports
```

Relationship semantics should remain explicit.

---

# Decision Categories

Decision Graphs may include:

```text
Assessment Graph

Recommendation Graph

Planning Graph

Optimization Graph

Risk Graph

Portfolio Graph

Business Strategy Graph
```

---

# Assessment Graph

Connects assessment decisions.

Example:

Similarity

↓

Distinctiveness

↓

Registrability

---

# Recommendation Graph

Connects recommendation decisions.

Example:

Country

↓

Classes

↓

Goods

↓

Attorney

---

# Planning Graph

Connects planning decisions.

Example:

Budget

↓

Timeline

↓

Filing Plan

---

# Optimization Graph

Connects optimization decisions.

Example:

Cost

↓

Coverage

↓

Priority

↓

Recommendation

---

# Risk Graph

Connects risk evaluations.

Example:

Conflict Risk

↓

Business Risk

↓

Renewal Risk

---

# Portfolio Graph

Connects portfolio decisions.

Example:

Trademark

↓

Brand

↓

Portfolio

↓

Investment

---

# Context

Decision Graphs are context-sensitive.

Typical context includes:

- jurisdiction
- industry
- customer objectives
- business strategy
- regulations
- historical events

Context determines which decision paths are applicable.

---

# Alternatives

Decision Graph should preserve alternatives.

Example

```text
National Filing

↓

Madrid Filing

↓

Regional Filing
```

Rejected alternatives remain valuable for explanation.

---

# Outcomes

Every decision path should define possible outcomes.

Examples include:

- Recommended
- Optional
- High Priority
- Manual Review Required
- Not Recommended

Outcomes should remain explainable.

---

# Validation

Validation should verify:

- disconnected decisions
- circular dependencies
- missing alternatives
- inconsistent outcomes
- reasoning integrity

---

# Runtime

Runtime traverses Decision Graphs.

Runtime never changes decision semantics.

Execution belongs to Capability.

---

# Relationship to Capability

Capabilities consume Decision Graphs.

Capabilities perform execution after decisions have been produced.

---

# Relationship to Guide

Guide explains decision paths.

Guide may visualize alternatives.

Decision logic remains unchanged.

---

# Compatibility

Decision Graphs evolve conservatively.

Decision semantics remain versioned.

Historical decision paths remain reproducible.

---

# Extension

Future Decision Graphs may include:

- Industry Decision Graphs
- Regional Decision Graphs
- Litigation Decision Graphs
- Financial Decision Graphs

Extensions should preserve explainability.

---

# Non Goals

Decision Graph is not:

- Workflow
- BPMN
- State Machine
- Graph Database
- AI Agent

Decision Graph organizes professional decisions.

Nothing more.

---

# Examples

International Filing

```text
Business Goal

↓

Country Recommendation

↓

Budget Evaluation

↓

Madrid Decision

↓

National Filing Decision
```

Similarity Assessment

```text
Similarity

↓

Distinctiveness

↓

Conflict Risk

↓

Registrability
```

Renewal Planning

```text
Portfolio Value

↓

Renewal Priority

↓

Budget

↓

Renewal Decision
```

---

# Design Principles

Reasoning before Decision.

Decision before Execution.

Alternatives before Conclusions.

Context before Automation.

Explainability before Complexity.

Professional Judgment before Technology.

---

# Summary

Decision Graph defines how professional judgments are connected within MarkOrbit.

It transforms individual reasoning results into explainable decision networks that preserve alternatives, constraints and dependencies.

Decision Graph bridges reusable reasoning and executable capabilities, allowing professional decisions to remain transparent, reusable and independent of workflow implementation.