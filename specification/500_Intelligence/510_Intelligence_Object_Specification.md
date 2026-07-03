# 510 Intelligence Object Specification

> **The Canonical Building Block of Professional Judgment**

---

Version

**2.0**

Status

**Draft**

Depends

- 170_Contract_Model.md
- 350_Product_Specification.md
- 440_Knowledge_Product_Specification.md
- 500_Intelligence_Specification.md

Related

- 520_Reasoning_Model.md
- 530_Decision_Graph.md
- 540_Intelligence_Product.md
- 600_Capability_Specification.md

---

# Purpose

Professional judgment is not produced by one monolithic intelligence.

It emerges from many reusable reasoning units.

The purpose of Intelligence Object is to define the smallest reusable unit of professional judgment.

Intelligence Object answers one question.

> **What is one professional judgment?**

---

# Intelligence Philosophy

Brain understands.

Intelligence judges.

Capability executes.

Guide communicates.

Every Intelligence Object performs exactly one professional judgment.

No more.

No less.

---

# Scope

Intelligence Objects include reusable judgment units.

Examples include:

- Similarity Assessment
- Registrability Assessment
- Filing Country Recommendation
- Nice Class Recommendation
- Goods Selection Recommendation
- Risk Assessment
- Portfolio Priority Assessment
- Renewal Priority Assessment
- Budget Optimization
- Enforcement Recommendation

Intelligence Objects are permanent Definitions.

Runtime executes their Instances.

---

# Responsibilities

Intelligence Object owns:

- one judgment objective
- reasoning scope
- expected inputs
- expected outputs
- confidence model
- explanation requirements

Intelligence Object does not own:

- workflow
- execution
- user interaction
- storage

---

# Intelligence Object Architecture

Every Intelligence Object follows one structure.

```text
Knowledge Products

↓

Context

↓

Reasoning

↓

Judgment

↓

Confidence

↓

Explanation
```

The object defines the judgment.

Runtime performs the judgment.

---

# Characteristics

Every Intelligence Object should satisfy:

## Atomic

One object performs one judgment.

---

## Context-aware

Different contexts may produce different conclusions.

---

## Explainable

Every judgment should explain why.

---

## Evidence-based

Every judgment should reference Knowledge Products.

---

## Reusable

Many Capabilities may invoke the same Intelligence Object.

---

## Versioned

Judgment logic evolves.

Object identity remains stable.

---

# Categories

Intelligence Objects may include:

```text
Assessment

Recommendation

Prediction

Optimization

Classification

Prioritization

Detection

Comparison
```

---

# Assessment

Produces professional evaluations.

Examples:

- Similarity Assessment
- Registrability Assessment
- Portfolio Assessment

---

# Recommendation

Produces recommended actions.

Examples:

- Filing Recommendation
- Country Recommendation
- Attorney Recommendation

---

# Prediction

Produces future-oriented judgments.

Examples:

- Renewal Risk Prediction
- Office Action Prediction
- Registration Probability

---

# Optimization

Produces improved alternatives.

Examples:

- Filing Cost Optimization
- Portfolio Optimization
- Budget Allocation

---

# Classification

Assigns professional categories.

Examples:

- Nice Class Recommendation
- Goods Categorization
- Risk Classification

---

# Prioritization

Ranks candidates.

Examples:

- Renewal Priority
- Enforcement Priority
- Opportunity Ranking

---

# Detection

Identifies significant conditions.

Examples:

- Conflict Detection
- Deadline Detection
- Duplicate Detection

---

# Comparison

Compares alternatives.

Examples:

- Country Comparison
- Cost Comparison
- Strategy Comparison

---

# Structure

Every Intelligence Object should define:

| Field | Required |
|---------|----------|
| Intelligence ID | ✓ |
| Name | ✓ |
| Category | ✓ |
| Purpose | ✓ |
| Inputs | ✓ |
| Outputs | ✓ |
| Knowledge Dependencies | ✓ |
| Confidence Strategy | ✓ |
| Explanation Strategy | ✓ |
| Version | ✓ |

Optional:

- Constraints
- Assumptions
- Examples

---

# Inputs

Inputs should reference published interfaces.

Typical inputs include:

- Knowledge Products
- Persistence Products
- Runtime Context
- User Intent
- Workspace Configuration

Objects should avoid implementation-specific dependencies.

---

# Outputs

Typical outputs include:

- Judgment
- Confidence
- Alternatives
- Supporting Evidence
- Reasoning Summary

Outputs should remain stable through Contracts.

---

# Confidence

Every Intelligence Object should expose confidence.

Confidence may be:

```text
High

Medium

Low
```

Or expressed numerically.

Confidence represents certainty in the judgment process.

It does not guarantee correctness.

---

# Explanation

Every Intelligence Object should provide explainable reasoning.

Typical explanation includes:

- evidence used
- reasoning summary
- assumptions
- alternatives considered
- uncertainty

Explainability is mandatory.

---

# Validation

Validation should verify:

- required inputs
- knowledge dependencies
- reasoning completeness
- explanation availability
- contract compliance

---

# Runtime

Runtime executes Intelligence Object Instances.

Definitions remain immutable.

Execution results belong to Runtime.

---

# Compatibility

Intelligence Objects evolve conservatively.

Changes to judgment semantics require a major version.

Consumers depend on stable Contracts.

---

# Extension

Future Intelligence Objects may include:

- Industry-specific assessments
- Country-specific recommendations
- Predictive intelligence modules
- AI-assisted reasoning modules

Extensions should preserve explainability and compatibility.

---

# Non Goals

Intelligence Object is not:

- AI Agent
- Workflow
- Capability
- Prompt
- LLM

These may invoke Intelligence Objects.

They do not define them.

---

# Examples

Similarity Assessment

```text
Input

Trademark Product

↓

Knowledge

Likelihood of Confusion

↓

Output

Medium Risk

Confidence

High
```

Country Recommendation

```text
Input

Business Context

↓

Knowledge

International Filing Strategy

↓

Output

US

EU

Madrid
```

Renewal Priority Assessment

```text
Portfolio

↓

Knowledge

Renewal Strategy

↓

Output

Priority Level

High
```

---

# Design Principles

Knowledge before Judgment.

One Judgment per Object.

Context before Conclusion.

Evidence before Confidence.

Explanation before Automation.

Composition before Monolith.

---

# Summary

Intelligence Object is the smallest reusable unit of professional judgment in MarkOrbit.

Each Intelligence Object performs one well-defined judgment based on published Knowledge Products and contextual information.

Intelligence Objects provide explainable, evidence-based and reusable reasoning that serves as the foundation for Reasoning Models, Decision Graphs and Intelligence Products.