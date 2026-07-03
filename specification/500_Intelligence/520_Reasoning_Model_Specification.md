# 520 Reasoning Model Specification

> **The Canonical Professional Reasoning Model of the MarkOrbit Operating System**

---

Version

**2.0**

Status

**Draft**

Depends

- 440_Knowledge_Product_Specification.md
- 500_Intelligence_Specification.md
- 510_Intelligence_Object_Specification.md

Related

- 530_Decision_Graph.md
- 540_Intelligence_Product.md
- 600_Capability_Specification.md

---

# Purpose

Professional judgment should never be arbitrary.

Judgment should follow explicit reasoning patterns.

The purpose of Reasoning Model is to organize Intelligence Objects into reusable professional reasoning structures.

Reasoning Model answers one question.

> **How should professional judgment be produced?**

---

# Reasoning Philosophy

Knowledge explains.

Reasoning evaluates.

Decision concludes.

Capability executes.

Reasoning is not AI thinking.

Reasoning is professional methodology.

---

# Scope

Reasoning Models describe reusable reasoning structures.

Examples include:

- Registrability Analysis
- Similarity Evaluation
- Filing Strategy Analysis
- Country Selection
- Goods Recommendation
- Renewal Planning
- Portfolio Review
- Risk Evaluation

Reasoning Models are reusable.

---

# Responsibilities

Reasoning Model owns:

- reasoning sequence
- reasoning dependencies
- evaluation criteria
- judgment methodology
- reusable reasoning logic

Reasoning Model does not own:

- facts
- knowledge
- execution
- workflow

---

# Architecture

Every Reasoning Model follows one structure.

```text
Knowledge Products

↓

Intelligence Objects

↓

Reasoning Model

↓

Decision Graph

↓

Intelligence Product
```

Reasoning organizes judgment.

Decision Graph connects reasoning.

---

# Characteristics

Every Reasoning Model should satisfy:

## Explicit

Reasoning should be visible.

---

## Explainable

Every reasoning step should be understandable.

---

## Modular

Reasoning should reuse Intelligence Objects.

---

## Deterministic where possible

Rule-based reasoning should remain deterministic.

AI may assist uncertain reasoning.

---

## Versioned

Reasoning evolves through explicit versions.

---

# Reasoning Structure

A Reasoning Model normally consists of:

```text
Goal

↓

Inputs

↓

Constraints

↓

Evaluation

↓

Alternatives

↓

Judgment
```

Every reasoning model should clearly define each stage.

---

# Categories

Reasoning Models may include:

```text
Assessment Model

Recommendation Model

Comparison Model

Optimization Model

Prediction Model

Risk Model

Planning Model
```

---

# Assessment Model

Evaluates current conditions.

Examples:

- Registrability Assessment
- Similarity Assessment

---

# Recommendation Model

Produces preferred options.

Examples:

- Filing Recommendation
- Country Recommendation

---

# Comparison Model

Compares alternatives.

Examples:

- Madrid vs National Filing
- Country Cost Comparison

---

# Optimization Model

Searches for improved outcomes.

Examples:

- Budget Optimization
- Portfolio Optimization

---

# Prediction Model

Forecasts future outcomes.

Examples:

- Office Action Prediction
- Registration Probability

---

# Risk Model

Evaluates uncertainty.

Examples:

- Conflict Risk
- Non-use Risk
- Enforcement Risk

---

# Planning Model

Produces structured plans.

Examples:

- Filing Plan
- Renewal Plan
- Portfolio Strategy

---

# Dependencies

Reasoning Models may depend on:

- Knowledge Products
- Intelligence Objects
- Context
- Constraints

Dependencies should remain explicit.

---

# Context

Context influences reasoning.

Typical context includes:

- jurisdiction
- customer objective
- budget
- timeline
- business strategy
- portfolio maturity

Reasoning without context is incomplete.

---

# Alternatives

Professional reasoning should evaluate alternatives.

Example

```text
US Filing

↓

Madrid Filing

↓

EU Filing
```

The preferred option should be explainable.

---

# Validation

Validation should verify:

- reasoning completeness
- missing dependencies
- explainability
- reproducibility
- contract compliance

---

# Runtime

Runtime executes Reasoning Model Instances.

Reasoning Definitions remain immutable.

---

# Relationship to Decision Graph

Reasoning defines methodology.

Decision Graph organizes decision flow.

The two should remain independent.

---

# Relationship to Capability

Capabilities invoke Reasoning Models.

Capabilities should not embed professional reasoning.

---

# Relationship to Guide

Guide explains reasoning.

Reasoning remains professional.

Guide adapts presentation.

---

# Compatibility

Reasoning Models evolve conservatively.

Breaking methodological changes require a new major version.

---

# Extension

Future Reasoning Models may include:

- AI-assisted reasoning
- Industry reasoning
- Regional reasoning
- Compliance reasoning

Extensions should preserve explainability.

---

# Non Goals

Reasoning Model is not:

- Chain of Thought
- Prompt
- LLM
- Workflow
- Capability

Reasoning Models describe professional methodology.

---

# Examples

Registrability Analysis

```text
Trademark

↓

Knowledge

↓

Similarity Assessment

↓

Distinctiveness Assessment

↓

Legal Constraints

↓

Judgment
```

Country Recommendation

```text
Business Goal

↓

Budget

↓

Knowledge

↓

Country Evaluation

↓

Recommendation
```

Renewal Planning

```text
Portfolio

↓

Renewal Risk

↓

Business Priority

↓

Renewal Plan
```

---

# Design Principles

Knowledge before Reasoning.

Methodology before AI.

Reasoning before Decision.

Explanation before Automation.

Composition before Complexity.

Professionalism before Convenience.

---

# Summary

Reasoning Model defines the reusable methodologies used to produce professional judgment within MarkOrbit.

It organizes Intelligence Objects into explainable reasoning structures independent of AI models or implementation technologies.

Reasoning Models transform professional understanding into consistent, transparent and reusable judgment methodologies that support every intelligent capability in the Operating System.