# ADR-004 — Introduce Mo Business Layer

**Status**

Accepted

**Date**

2026-07

**Version**

MarkOrbit Core Specification v2.1 RC1

**Decision Type**

Architecture Decision Record

**Related Documents**

- Architecture Amendment 001 — Introduce Mo Business Layer
- 550_Business Module
- Core Specification v2.0 RC1

---

# 1. Context

MarkOrbit Core Specification v2.0 established a layered architecture that separates the responsibilities of factual persistence, professional understanding, intelligent reasoning, capability execution and workspace organisation.

The architecture proved stable during the design of MarkOrbit Lite.

However, while implementing Lite, several independent product scenarios repeatedly exposed an architectural concern that could not be naturally assigned to any existing layer.

Examples included:

- evaluating the commercial value of trademarks;
- measuring the contribution of generated content;
- calculating business return on investment (ROI);
- ranking marketplace opportunities;
- evaluating partner performance;
- measuring workflow contribution;
- analysing customer lifetime value.

These scenarios all required **Business Evaluation**.

Business Evaluation is fundamentally different from factual persistence, professional understanding and intelligent reasoning.

This ADR records the architectural decision to introduce a dedicated Business Evaluation layer.

---

# 2. Problem

The Core Architecture already defines:

- Mo Data
- Mo Brain
- Mo Intelligence
- Mo Capability
- Mo Workspace

None of these layers owns Business Evaluation.

Without an explicit architectural responsibility, Business Evaluation would gradually become distributed across multiple layers.

Typical consequences include:

- duplicated evaluation logic;
- inconsistent business metrics;
- responsibility ambiguity;
- tighter coupling between business logic and reasoning.

Such evolution would violate the Single Responsibility Principle adopted throughout the Core Architecture.

---

# 3. Decision Drivers

The following principles guided this decision.

## 3.1 Single Responsibility

Every Core layer owns exactly one primary architectural responsibility.

Business Evaluation represents an independent responsibility.

---

## 3.2 Explainability

Business Evaluation shall remain explainable through observable business evidence.

Evaluation shall never become an opaque reasoning process.

---

## 3.3 Reusability

Business Evaluation should become a reusable architectural capability rather than application-specific logic.

---

## 3.4 Long-Term Stability

The Core Architecture should evolve by extending responsibilities rather than redefining existing layers.

---

# 4. Considered Options

## Option A — Extend Mo Brain

Business Evaluation becomes part of Professional Understanding.

### Rejected

Professional Understanding answers:

> What does this mean professionally?

Business Evaluation answers:

> What is its business significance?

These represent different architectural responsibilities.

Combining them would increase coupling and reduce conceptual clarity.

---

## Option B — Extend Mo Intelligence

Business Evaluation becomes part of Intelligent Reasoning.

### Rejected

Reasoning consumes interpretations.

Evaluation is itself an interpretation.

If Intelligence performs evaluation directly, reasoning and evaluation become inseparable.

This violates the separation established by the Core Architecture.

---

## Option C — Extend Mo Workspace

Business Evaluation becomes part of Workspace.

### Rejected

Workspace organises work.

Workspace presents information.

Workspace does not evaluate business value.

Business Evaluation therefore does not belong to Workspace.

---

## Option D — Introduce Mo Business

Create a dedicated architecture layer responsible for Business Evaluation.

### Accepted

This option preserves existing responsibilities while introducing one additional interpretation layer.

No existing architectural responsibility changes.

---

# 5. Decision

The MarkOrbit Core Architecture introduces a new architecture layer:

**Mo Business**

Mo Business owns one primary responsibility:

> Business Evaluation.

Mo Business:

- consumes factual information from Mo Data;
- evaluates business significance;
- publishes Business Evaluation;
- remains independent from Professional Understanding;
- remains independent from Intelligent Reasoning.

Mo Intelligence consumes Business Evaluation rather than producing it.

---

# 6. Architectural Consequences

After this decision the interpretation pipeline becomes:

```
Mo Data
      │
      ├──────────────┐
      ▼              ▼
Mo Brain        Mo Business
Understand      Evaluate
      └──────┬───────┘
             ▼
      Mo Intelligence
           Reason
```

The architecture now distinguishes three independent stages of interpretation.

- Professional Understanding
- Business Evaluation
- Intelligent Reasoning

---

# 7. Positive Consequences

This decision provides the following architectural benefits.

## Clear Responsibility Boundaries

Professional understanding and business evaluation become independent responsibilities.

---

## Better Reusability

Business Evaluation becomes reusable across:

- Lite
- Marketplace
- Partner Platform
- Future applications

---

## Better Explainability

Every Business Evaluation can be traced back to observable Business Evidence.

---

## Better Scalability

Future evaluation dimensions can be added without modifying Brain or Intelligence.

---

# 8. Trade-offs

The decision also introduces additional complexity.

Examples include:

- one new architecture layer;
- one additional specification module;
- additional vocabulary;
- additional repository maintenance.

The architecture team considers these costs acceptable because they preserve long-term architectural clarity.

---

# 9. Rejected Alternatives

The following alternatives were intentionally rejected.

- Business Evaluation inside Mo Data
- Business Evaluation inside Mo Brain
- Business Evaluation inside Mo Intelligence
- Business Evaluation inside Workspace
- Application-specific Business Evaluation

The Core Architecture adopts a single canonical Business Evaluation layer.

---

# 10. Relationship to Existing Architecture

This decision does not modify the responsibilities of existing architecture layers.

Mo Data remains the factual foundation.

Mo Brain remains responsible for Professional Understanding.

Mo Intelligence remains responsible for Intelligent Reasoning.

Mo Capability remains responsible for execution.

Mo Workspace remains responsible for context organisation.

Mo Business extends the architecture without redefining existing responsibilities.

---

# 11. Implementation

Implementation is intentionally outside the scope of this ADR.

Implementation guidance is defined by:

- Architecture Amendment 001
- 550_Business Module
- Reference Implementations

This ADR records the architectural decision only.

---

# 12. References

- MarkOrbit Core Specification v2.0 RC1
- Core 2.1 Architecture Amendment 001
- 550_Business Module
- MarkOrbit Lite Reference Implementation

---

# Summary

This ADR introduces **Mo Business** as the canonical Business Evaluation layer of the MarkOrbit Core Architecture.

The decision preserves the existing layered architecture while extending it with an independent evaluation responsibility.

The architecture therefore evolves by addition rather than modification, maintaining long-term stability and conceptual clarity.

---

**End of ADR-004**