# 001 Professional Vocabulary

> The Canonical Vocabulary of the MarkOrbit Professional Operating System

Version: 2.0

Status: Active

Applies To

- Specifications
- Runtime
- Platform
- Documentation
- Source Code
- APIs
- AI Agents
- Prompt Engineering

---

# Purpose

Professional systems require a shared language.

Every specification, implementation and discussion should use one consistent vocabulary.

When multiple terms exist for the same concept, this document defines the canonical term.

Consistency is preferred over synonym diversity.

---

# Vocabulary Principles

Every important architectural concept has exactly one preferred name.

Preferred terms should always be used.

Alternative terms should be avoided unless required by external standards.

---

# Core Architectural Vocabulary

## Professional Operating System

Definition

The complete architecture for professional work.

Preferred

Professional Operating System

Abbreviation

Professional OS

Avoid

- AI Operating System
- Business Platform
- Workflow Platform
- SaaS Architecture

---

## Workspace

Definition

An independent operating context hosting one Professional Operating System.

Preferred

Workspace

Avoid

- Tenant
- Company
- Project
- Instance

---

## Platform

Definition

The federation and hosting layer responsible for managing multiple Workspaces.

Preferred

Platform

Avoid

- SaaS
- Cloud
- System

---

# Canonical Objects

Every professional layer defines exactly one canonical Object.

---

## Concept

Layer

Brain

Definition

The smallest reusable unit of professional knowledge.

Avoid

- Entity
- Knowledge Node
- Brain Node

---

## Judgment

Layer

Intelligence

Definition

The smallest reusable unit of professional reasoning.

Avoid

- Decision Result
- AI Decision
- Conclusion

---

## Action

Layer

Capability

Definition

The smallest reusable unit of professional execution.

Avoid

- Task
- Operation
- Function

---

## Responsibility

Layer

Workflow

Definition

The smallest reusable unit of professional coordination.

Avoid

- Approval Node
- Workflow Task
- BPMN Task

---

## Interaction

Layer

Guide

Definition

The smallest reusable unit of professional experience.

Avoid

- Conversation
- Wizard
- Chat
- UI Flow

---

## Operating Context

Layer

Workspace

Definition

The organizational environment within which one Professional Operating System operates.

Avoid

- Tenant
- Organization
- Company

---

# Business Vocabulary

## Mo Business

Definition

The architectural layer responsible for Business Evaluation.

Preferred

Mo Business


---

## Business Evaluation

Definition

The interpretation of observable facts as business significance.

Preferred

Business Evaluation


---

## Business Evidence

Definition

Observable factual evidence used for Business Evaluation.

Preferred

Business Evidence


---

## Evaluation Target

Definition

The object or context being evaluated by Mo Business.

Preferred

Evaluation Target


---

## Evaluation Dimension

Definition

A business perspective used to evaluate an Evaluation Target.

Preferred

Evaluation Dimension


---

## Business Product

Definition

The published Product of Mo Business.

Preferred

Business Product


---

# Canonical Models

Preferred

Knowledge Model

Reasoning Model

Execution Model

Interaction Model

Orchestration Model

Organization Model

Avoid

- Strategy
- Framework
- Logic
- Engine

---

# Canonical Connections

Preferred

Knowledge Graph

Decision Graph

Capability Network

Experience Network

Workflow Network

Workspace Network

Guideline

Graph represents semantic relationships.

Network represents collaboration relationships.

---

# Canonical Products

Preferred

Persistence Product

Knowledge Product

Intelligence Product

Capability Product

Workflow Product

Guide Product

Workspace Product

Avoid

- Output
- Bundle
- Artifact
- Package
- Result

---

# Runtime Vocabulary

Preferred

Definition

Runtime Instance

Session

Product

Avoid

- Live Object
- Runtime Object
- Working Copy

---

# Professional Flow

Preferred

Facts

Understanding

Judgment

Action

Coordination

Experience

Avoid

- Information
- Processing
- Decision Tree
- Execution Flow

---

# Organizational Vocabulary

Preferred

Workspace

Professional Role

Responsibility

Authority

Governance

Operating Context

Avoid

- Department
- Employee
- Organization Chart
- Tenant Structure

---

# Product Vocabulary

Products are:

- Published
- Immutable
- Versioned
- Contract-based

Products are not:

- Runtime Objects
- Database Records
- UI Components
- Internal Models

---

# Naming Conventions

Use nouns.

Avoid verbs whenever possible.

Examples

✓ Capability Product

✗ Execute Capability

---

Use singular nouns.

Examples

✓ Knowledge Product

✗ Knowledge Products

---

Prefer architectural terms over technical terms.

Examples

✓ Workspace

✗ Tenant

✓ Product

✗ DTO

✓ Interaction

✗ Chat

---

# Forbidden Vocabulary

The following terms should not be used in architectural documents unless required by external standards.

| Avoid | Preferred |
|--------|-----------|
| Tenant | Workspace |
| Company | Operating Context |
| Entity | Concept |
| Task | Action / Responsibility |
| Conversation | Interaction |
| Output | Product |
| Artifact | Product |
| Bundle | Product |
| Package | Product |
| Decision Result | Judgment |
| Workflow Task | Responsibility |
| Organization Chart | Organization Model |

---

# Review Checklist

Before approving any architectural document, verify:

- Canonical vocabulary is used.
- Forbidden terms are avoided.
- Layer names are correct.
- Product names are consistent.
- Object names are consistent.
- Model names are consistent.

Architectural consistency begins with language.

---

# Final Principle

Architecture is communicated through language.

Consistent language produces consistent architecture.

Professional Vocabulary is therefore considered part of the architecture itself.