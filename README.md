# MarkOrbit Core Specification

> **A Professional Operating System for Intellectual Property**

Version: **2.0**  
Status: **Architecture Freeze Candidate**

---

# Overview

MarkOrbit is not another AI application.

It is not another Workflow Engine.

It is not another CRM.

It is not another SaaS template.

MarkOrbit defines a **Professional Operating System (Professional OS)** for Intellectual Property, designed to model how professional work is understood, reasoned, executed, coordinated and delivered.

Rather than organizing software around data, prompts or user interfaces, MarkOrbit organizes systems around **professional value creation**.

The architecture separates professional knowledge from implementation technology, allowing the same professional model to be implemented by humans, AI systems, workflow engines or future technologies.

---

# Vision

Professional knowledge evolves slowly.

Technology evolves rapidly.

MarkOrbit separates the two.

Professional expertise becomes architecture.

Technology becomes implementation.

This separation enables one stable Professional Operating System to support decades of technological evolution without redesigning its professional foundation.

---

# Design Philosophy

Every professional activity follows a common progression.

```text
Reality

↓

Facts

↓

Professional Understanding

↓

Business Evaluation

↓

Intelligent Reasoning

↓

Action

↓

Coordination

↓

Experience
```

MarkOrbit models this progression directly.

Every architectural layer owns exactly one transformation.

Responsibilities never overlap.

---

# Universal Architecture Pattern

Every architectural layer follows the same structural pattern.

```text
Object

↓

Model

↓

Connection

↓

Product
```

Each layer defines:

- a canonical Object
- a reusable Model
- explicit Connections
- published Products

Products expose stable contracts.

Implementations remain replaceable.

---

# Professional Operating System

The MarkOrbit Professional Operating System consists of seven professional layers operating inside one organizational context.

```text
Platform

↓

Workspace

↓

Professional Operating System

    Persistence

    Brain

    Business

    Intelligence

    Capability

    Workflow

    Guide
```

Workspace provides organizational context.

Platform hosts multiple independent Workspaces.

The Professional Operating System remains universal.

---

# Architecture

The Core Architecture relationship is:

```text
Mo Data

↓

Mo Brain

+

Mo Business

↓

Mo Intelligence
```

## Persistence

Responsible for recording professional facts.

Question answered:

> **What happened?**

---

## Brain

Responsible for transforming facts into professional understanding.

Question answered:

> **What does it mean?**

---

## Business

Responsible for Business Evaluation.

Mo Business evaluates the business significance of facts as the Business Evaluation Layer.

Question answered:

> **What is its business value?**

---

## Intelligence

Responsible for intelligent reasoning and judgment.

Question answered:

> **What should we conclude?**

---

## Capability

Responsible for professional execution.

Question answered:

> **What should we do?**

---

## Workflow

Responsible for organizational coordination.

Question answered:

> **How should professional work be organized?**

---

## Guide

Responsible for professional interaction and user experience.

Question answered:

> **How should professional work be experienced?**

---

## Workspace

Provides organizational operating context.

Workspace is not:

- Tenant
- Company
- Project
- Database

Workspace is an independent operating environment hosting one complete Professional Operating System.

---

# Canonical Objects

Every professional layer defines one canonical Object.

| Layer | Canonical Object |
|--------|------------------|
| Brain | Concept |
| Intelligence | Judgment |
| Capability | Action |
| Workflow | Responsibility |
| Guide | Interaction |
| Workspace | Operating Context |

These Objects form the core vocabulary of MarkOrbit.

---

# Published Products

Professional value flows through published Products.

```text
Persistence Product

↓

Knowledge Product

↓

Intelligence Product

↓

Capability Product

↓

Workflow Product

↓

Guide Product
```

Products communicate between layers.

Products are immutable.

Products are versioned.

Products expose stable contracts.

---

# Repository Structure

- [Constitution](CONSTITUTION.md)
- [Professional Vocabulary](001_Professional_Vocabulary.md)
- [Naming Convention](002_Naming_Convention.md)
- [Document Style](003_Document_Style.md)
- [Architecture Manifesto](099_Architecture_Manifesto.md)
- [Theory](theory/README.md)
- [Specification](specification/README.md)
- [Docs](docs/README.md)

Specification domains:

- [Engineering Kernel](specification/100_Engineering_Kernel/README.md)
- [Core Foundation](specification/200_Core_Foundation/README.md)
- [Persistence](specification/300_Persistence/README.md)
- [Brain](specification/400_Brain/README.md)
- [Business](specification/550_Business/README.md)
- [Intelligence](specification/500_Intelligence/README.md)
- [Capability](specification/600_Capability/README.md)
- [Guide](specification/700_Guide/README.md)
- [Workflow](specification/800_Workflow/README.md)
- [Workspace](specification/900_Workspace/README.md)

Every specification directory represents one architectural domain.

Each domain follows the same internal pattern.

```text
Specification

↓

Object

↓

Model

↓

Connection

↓

Product
```

---

# Recommended Reading Order

## New Readers

```text
README

↓

099_Architecture_Manifesto

↓

100_Engineering_Kernel

↓

Core Foundation

↓

Persistence

↓

Brain

+

Business

↓

Intelligence

↓

Capability

↓

Guide

↓

Workflow

↓

Workspace

↓

Platform
```

---

## Architects

Recommended order:

1. Architecture Manifesto
2. Engineering Kernel
3. Brain
4. Intelligence
5. Capability
6. Workflow
7. Guide
8. Workspace
9. Platform

---

## Developers

Recommended order:

1. Engineering Kernel
2. Core Foundation
3. Target Domain Specification
4. Reference Implementation

---

# Architectural Principles

MarkOrbit follows thirteen architectural principles.

1. One Layer, One Responsibility.

2. One Layer, One Canonical Object.

3. Products before Integrations.

4. Contracts before Implementations.

5. Professional Understanding before Business Evaluation.

6. Business Evaluation before Intelligent Reasoning.

7. Intelligent Reasoning before Capability Execution.

8. Capability Execution before Context Organisation.

9. Context Organisation before Experience Delivery.

10. Workspace before Organization.

11. Federation before Centralization.

12. Professional Architecture before Artificial Intelligence.

13. Evolution without Architectural Drift.

---

# Technology Independence

MarkOrbit does not depend upon any implementation technology.

Possible implementations include:

- Human professionals
- AI models
- Rule engines
- Workflow engines
- MCP tools
- REST APIs
- Event systems
- Microservices
- Future AI architectures

Professional architecture remains unchanged.

---

# Current Status

Current Version

**2.0**

Architecture Status

**Architecture Freeze Candidate**

Current Focus

- Architecture Review
- Consistency Review
- Reference Implementation
- Engineering Validation

---

# Future Roadmap

## Phase 1

Professional Operating System Architecture

**Status: Complete**

---

## Phase 2

Reference Implementation

- Core Runtime
- Knowledge Runtime
- Workflow Runtime
- Guide Runtime

---

## Phase 3

Platform

- Multi-workspace Platform
- Federation
- Marketplace
- Extension System

---

## Phase 4

Professional Ecosystem

- Capability Marketplace
- Knowledge Marketplace
- Guide Marketplace
- Cross-organization Federation

---

# Contributing

Before contributing, please read:

1. `099_Architecture_Manifesto.md`
2. `CONSTITUTION.md`
3. Relevant domain specifications

All contributions should preserve architectural consistency.

Implementation details may evolve.

Architectural principles should remain stable.

---

# License

Apache License 2.0

---

# Final Statement

MarkOrbit is designed around one fundamental belief.

Artificial Intelligence is replaceable.

Professional Architecture is not.

By separating professional knowledge from implementation technology, MarkOrbit establishes a Professional Operating System capable of evolving across decades of technological change while preserving one consistent professional model.