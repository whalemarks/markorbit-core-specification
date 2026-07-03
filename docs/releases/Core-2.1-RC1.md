# MarkOrbit Core Specification

# Core v2.1 RC1 Release Notes

**Release**

Core Specification v2.1 RC1

**Status**

Release Candidate

**Release Date**

2026-07

---

# Overview

Core Specification v2.1 RC1 is the first release candidate of the MarkOrbit Core Architecture following the introduction of **Mo Business**.

This release focuses on **architectural maturity rather than feature expansion**.

The Core Architecture now recognises **Business Evaluation** as an independent architectural responsibility, completing the separation between factual information, professional understanding, business evaluation and intelligent reasoning.

No application functionality is introduced in this release.

Instead, Core v2.1 RC1 establishes a more stable architectural foundation for future implementations.

---

# Highlights

## Introduced Mo Business

A new architecture layer, **Mo Business**, has been added to the Core Architecture.

Mo Business owns one responsibility.

> **Business Evaluation**

Business Evaluation measures the business significance of observable facts.

It is independent from:

- Professional Understanding
- Intelligent Reasoning
- Capability Execution
- Workspace Organisation

---

## Architecture Amendment 001

Core v2.1 RC1 incorporates:

**Architecture Amendment 001 — Introduce Mo Business**

The amendment formally extends the Core Architecture without changing the responsibilities of existing layers.

---

## ADR-004

Core v2.1 RC1 introduces:

**ADR-004 — Introduce Mo Business Layer**

The ADR documents the architectural decision behind introducing Business Evaluation as a first-class responsibility.

---

## 550_Business Module

A new Core module has been added.

```
550_Business
```

The module consists of:

- README
- 550_Mo_Business_Specification
- 551 What is Mo Business
- 552 Evaluation Targets
- 553 Evaluation Dimensions
- 554 Evaluation Pipeline
- 555 Business Relationships
- 556 Business Interfaces
- 557 Evolution

This module becomes the canonical specification of the Business layer.

---

## Theory Expansion

The theoretical foundation of the Core Architecture has been extended.

A new theory document has been introduced.

```
Theory 09 — Business
```

This document explains why Business Evaluation exists as an independent architectural concern.

---

# Architecture

The Core Architecture now consists of the following primary layers.

```
Mo Data
        │
        ├─────────────┐
        ▼             ▼
Mo Brain         Mo Business
Understand        Evaluate
        └──────┬──────┘
               ▼
       Mo Intelligence
           Reason
               ▼
        Mo Capability
               ▼
         Mo Workspace
               ▼
        Applications
```

The architecture now clearly separates:

Facts

↓

Professional Understanding

↓

Business Evaluation

↓

Intelligent Reasoning

↓

Capability Execution

↓

Workspace Organisation

↓

Application Experience

---

# Repository Alignment

The repository has been aligned with the new architecture.

Alignment includes:

- repository navigation
- architecture overview
- specification navigation
- professional vocabulary
- architecture manifesto
- constitution
- changelog
- layer relationships

No architectural redesign occurred during repository alignment.

---

# Compatibility

Core v2.1 RC1 is fully compatible with Core v2.0.

Existing architectural responsibilities remain unchanged.

Mo Business extends the architecture.

It does not replace existing layers.

---

# Validation Strategy

Core Specification is no longer validated by a single implementation.

Beginning with v2.1 RC1, the Core Architecture is intended to be validated by multiple independent implementations.

Initial validators include:

- MarkOrbit Lite
- MarkReg.com
- MGSN (Mark Global Service Network)
- Workplace implementations
- Future ecosystem applications

Each implementation validates different aspects of the Core Architecture while sharing the same architectural foundation.

---

# Known Limitations

Core v2.1 RC1 remains a Release Candidate.

The following work is intentionally deferred.

- Runtime Specification
- Reference Runtime
- Business reference implementation
- Capability reference implementation
- Multi-validator architecture verification

These items will be addressed in future releases.

---

# Next Milestone

The next development milestone is:

**MarkOrbit Lite Sprint 1**

Lite becomes the first implementation built on Core v2.1 RC1.

Future validators, including MarkReg.com and MGSN, will further verify the architecture.

Architecture changes after this release shall follow the established process.

```
ADR

↓

Architecture Amendment

↓

Patch

↓

Implementation

↓

Validation

↓

Release
```

---

# Acknowledgements

Core v2.1 RC1 represents the completion of the first major architectural evolution of the MarkOrbit ecosystem.

The introduction of Mo Business establishes Business Evaluation as a permanent architectural capability while preserving the stability of the existing Core Architecture.

This release provides a stronger foundation for future implementations and long-term ecosystem evolution.

---

# Summary

Core Specification v2.1 RC1 introduces **Mo Business** as the Business Evaluation layer of the MarkOrbit Core Architecture.

The release focuses on architectural clarity, responsibility separation and repository consistency.

The architecture is now ready for validation across multiple implementations, including MarkOrbit Lite, MarkReg.com and MGSN.

---

**End of Core v2.1 RC1 Release Notes**