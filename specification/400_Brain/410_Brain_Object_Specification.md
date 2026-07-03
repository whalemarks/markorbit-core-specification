# 410 Brain Object Specification

> **The Canonical Building Block of Professional Understanding**

---

Version

**2.0**

Status

**Draft**

Depends

- 120_Identity_Specification.md
- 170_Contract_Model.md
- 300_Persistence_Specification.md
- 350_Product_Specification.md
- 400_Brain_Specification.md

Related

- 420_Knowledge_Model.md
- 430_Knowledge_Graph.md
- 440_Knowledge_Product.md
- 500_Intelligence_Specification.md

---

# Purpose

Professional knowledge is not one large document.

It is composed of many reusable units.

The purpose of Brain Object is to define the smallest reusable semantic unit of professional understanding.

Brain Object answers one question.

> **What is one professional concept?**

---

# Brain Object Philosophy

Facts belong to Persistence.

Understanding belongs to Brain.

Brain should not store documents.

Brain should organize understanding.

Every Brain Object represents one professional concept.

No more.

No less.

---

# Scope

Brain Objects include reusable professional concepts.

Examples include:

- Likelihood of Confusion
- Distinctiveness
- Bad Faith
- Priority
- Genuine Use
- Disclaimer
- Nice Classification
- Trademark Examination Rule
- Office Practice
- Similar Goods Principle

Brain Objects are permanent.

---

# Responsibilities

Brain Object owns:

- one professional concept
- semantic definition
- explanation
- professional meaning
- related concepts

Brain Object does not own:

- facts
- recommendations
- workflows
- execution

---

# Brain Object Model

Every Brain Object consists of:

```text
Identity

↓

Concept

↓

Definition

↓

Explanation

↓

Relationships

↓

Evidence

↓

Version
```

---

# Brain Object Characteristics

Every Brain Object should satisfy:

## Atomic

One Brain Object explains one concept.

---

## Reusable

Many Capabilities should reuse one Brain Object.

---

## Explainable

A Brain Object should explain itself.

---

## Traceable

Every Brain Object should reference supporting Products.

---

## Independent

Brain Objects should not depend on Workflow.

---

## Versioned

Knowledge evolves.

Brain Objects evolve through versions.

---

# Categories

Brain Objects may include:

```text
Legal Concept

Professional Principle

Office Practice

Procedure Knowledge

Classification Knowledge

Risk Knowledge

Strategy Knowledge

Terminology
```

---

# Legal Concept

Examples

- Distinctiveness
- Bad Faith
- Genuine Use
- Priority

---

# Professional Principle

Examples

- Similarity Principle
- Dominant Element Principle
- Consumer Perception

---

# Office Practice

Examples

- USPTO Disclaimer Practice
- CNIPA Examination Practice
- EUIPO Relative Grounds

---

# Procedure Knowledge

Examples

- Filing
- Renewal
- Assignment
- Opposition
- Appeal

---

# Classification Knowledge

Examples

- Nice Classification
- Vienna Classification

---

# Risk Knowledge

Examples

- Genericness Risk
- Non-use Risk
- Conflict Risk

---

# Strategy Knowledge

Examples

- Defensive Filing
- Multi-country Filing
- Madrid Strategy

---

# Terminology

Examples

- Applicant
- Registrant
- Priority Date
- Office Action

---

# Brain Object Structure

Every Brain Object should include:

| Field | Required |
|---------|----------|
| Brain ID | ✓ |
| Name | ✓ |
| Category | ✓ |
| Definition | ✓ |
| Explanation | ✓ |
| Related Concepts | ✓ |
| Source Products | ✓ |
| Version | ✓ |

Optional:

- Jurisdiction
- Examples
- Exceptions

---

# Evidence

Brain Objects should preserve supporting evidence.

```text
Source

↓

Product

↓

Brain Object
```

Professional understanding should always be explainable.

---

# Relationships

Brain Objects may relate to:

- Brain Objects
- Ontology
- Reference
- Capability
- Workflow

Relationships remain explicit.

---

# Validation

Validation may verify:

- semantic consistency
- ontology alignment
- source lineage
- duplicate concepts
- terminology consistency

---

# Runtime

Brain Objects are permanent.

Runtime only reads Brain Objects.

Runtime never modifies them.

---

# Compatibility

Brain Objects evolve conservatively.

Meaning should remain stable.

Breaking semantic changes require a new major version.

---

# Extension

Future Brain Objects may include:

- Industry Knowledge
- Country Knowledge
- Community Knowledge
- AI-generated Knowledge

Extensions should preserve semantic quality.

---

# Non Goals

Brain Object is not:

- Document
- AI Prompt
- Workflow
- Recommendation
- Training Data

Brain Objects represent reusable understanding.

---

# Examples

Brain Object

```text
Likelihood of Confusion
```

Brain Object

```text
Distinctiveness
```

Brain Object

```text
USPTO Disclaimer Practice
```

---

# Design Principles

Concept before Document.

Understanding before Automation.

Atomic before Comprehensive.

Reusable before Redundant.

Evidence before Assertion.

Semantics before Algorithms.

---

# Summary

Brain Object is the smallest reusable unit of professional understanding in MarkOrbit.

Each Brain Object represents one professional concept supported by traceable evidence and structured explanation.

Brain Objects are the building blocks from which Knowledge Models, Knowledge Graphs and Knowledge Products are constructed.