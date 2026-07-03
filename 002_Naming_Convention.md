# 002 Naming Convention

> The Canonical Naming Standard of the MarkOrbit Professional Operating System

Version: 2.0

Status: Active

Applies To

- Specifications
- Runtime
- Platform
- Source Code
- APIs
- Events
- Documentation
- AI Agents

---

# Purpose

A consistent architecture requires a consistent naming system.

Naming is part of the architecture.

Every architectural artifact should have one canonical name.

Alternative names should be avoided.

---

# Naming Philosophy

Names should describe architecture.

Not implementation.

Not technology.

Not programming language.

Good names survive implementation changes.

Poor names become technical debt.

---

# General Rules

Every name should satisfy the following principles.

## Prefer nouns

Architecture defines concepts.

Use nouns instead of verbs.

Examples

✓ Capability Product

✓ Knowledge Model

✗ ExecuteCapability

✗ RunningWorkflow

---

## Prefer singular form

Architectural concepts are singular.

Examples

✓ Guide Product

✓ Workflow Object

✗ Guide Products

✗ Workflow Objects

---

## Prefer explicit names

Avoid abbreviations unless universally accepted.

Examples

✓ Professional Operating System

✓ Knowledge Product

✗ POS

✗ KP

---

## Prefer professional language

Names should describe professional meaning.

Not technical implementation.

Examples

✓ Workspace

✗ Tenant

✓ Interaction

✗ Chat

✓ Responsibility

✗ Task

---

# File Naming

Use:

```
NNN_Name.md
```

Examples

```
099_Architecture_Manifesto.md

100_Engineering_Kernel.md

410_Brain_Object_Specification.md

620_Execution_Model_Specification.md

730_Experience_Network_Specification.md
```

Rules

- Three-digit prefix
- Pascal_Case
- Underscore separator
- Singular nouns
- `.md` extension

---

# Directory Naming

Use PascalCase.

Examples

```
Brain/

Capability/

Workflow/

Workspace/

Platform/
```

Avoid

```
brain/

knowledge_layer/

workflow_engine/

```

Directories represent architectural domains.

---

# Specification Naming

Specifications follow one pattern.

```
<Object> Specification

<Model> Specification

<Network> Specification

<Product> Specification
```

Examples

```
Brain Object Specification

Knowledge Model Specification

Decision Graph Specification

Guide Product Specification
```

Avoid

```
Brain Framework

Execution Logic

Workflow Engine
```

---

# Object Naming

Every Object uses:

```
<Domain> Object
```

Examples

```
Brain Object

Capability Object

Workflow Object

Guide Object
```

Avoid

```
Brain Node

Capability Unit

Workflow Task
```

---

# Model Naming

Every methodology uses:

```
<Model Name> Model
```

Examples

```
Knowledge Model

Reasoning Model

Execution Model

Interaction Model

Orchestration Model

Organization Model
```

Avoid

```
Strategy

Framework

Logic

Engine
```

---

# Connection Naming

Connections describe relationships.

Choose the correct semantic.

## Graph

Represents semantic relationships.

Examples

```
Knowledge Graph

Decision Graph
```

---

## Network

Represents collaboration relationships.

Examples

```
Capability Network

Experience Network

Workflow Network

Workspace Network
```

Never mix Graph and Network without semantic justification.

---

# Product Naming

Published outputs always use:

```
<Product Name> Product
```

Examples

```
Knowledge Product

Capability Product

Workflow Product

Guide Product

Workspace Product
```

Avoid

```
Bundle

Artifact

Package

Output

DTO
```

---

# Runtime Naming

Definitions and runtime instances are different.

Preferred

```
Definition

↓

Runtime Instance

↓

Product
```

Runtime terminology

```
Session

Instance

Runtime

Lifecycle
```

Avoid

```
Working Object

Live Object

Temporary Object
```

---

# Workspace Naming

Always use

```
Workspace
```

Never use

```
Tenant

Customer

Company

Project
```

Workspace is an Operating Context.

---

# Role Naming

Roles describe professional responsibilities.

Examples

```
Trademark Attorney

Portfolio Manager

Reviewer

Finance Officer

Compliance Officer
```

Avoid

```
User Type

Operator

Worker
```

---

# Event Naming

Events describe completed facts.

Use past tense.

Examples

```
CaseCreated

ApplicationSubmitted

ReviewCompleted

ApprovalGranted

WorkspaceInitialized
```

Avoid

```
CreateCase

DoReview

Running
```

Events describe facts.

Commands describe intent.

---

# Command Naming

Commands describe requested actions.

Use imperative verbs.

Examples

```
SubmitApplication

GenerateRecommendation

AssignReviewer

InitializeWorkspace
```

Avoid

```
Submitted

RecommendationGenerated
```

---

# API Naming

Resources use nouns.

HTTP methods express actions.

Examples

```
GET /capabilities

GET /knowledge-products

POST /applications

POST /workflow-products
```

Avoid

```
/doSubmit

/getKnowledge

/runWorkflow
```

---

# Class Naming

Use PascalCase.

Examples

```
KnowledgeProduct

GuideProduct

WorkflowNetwork

OrganizationModel
```

Avoid

```
knowledge_product

Guideproduct

WorkflowNETWORK
```

---

# Method Naming

Methods describe behavior.

Use verbs.

Examples

```
evaluate()

publish()

execute()

coordinate()

render()
```

Architecture uses nouns.

Implementation uses verbs.

---

# Variable Naming

Variables describe meaning.

Examples

```
knowledgeProduct

workflowProduct

workspaceContext

interactionModel
```

Avoid

```
obj

tmp

result2

data1
```

---

# Enumeration Naming

Use singular nouns.

Examples

```
CapabilityType

WorkflowState

WorkspaceKind
```

Avoid

```
Types

States

Enums
```

---

# Constant Naming

Use uppercase.

Examples

```
MAX_RETRY

DEFAULT_LANGUAGE

CURRENT_VERSION
```

---

# Version Naming

Architecture

```
v2.0
```

Implementation

```
2.0.5
```

Runtime

```
2026.07
```

Do not mix architectural versions with implementation versions.

---

# Abbreviations

Avoid abbreviations.

Preferred

```
Knowledge Product
```

Avoid

```
KP
```

Exceptions

Widely accepted standards.

Examples

```
API

JSON

HTTP

UUID

OAuth
```

---

# Reserved Words

The following architectural terms are reserved.

```
Concept

Judgment

Action

Responsibility

Interaction

Operating Context

Workspace

Knowledge Product

Capability Product

Workflow Product

Guide Product
```

Reserved words should not be redefined.

---

# Naming Review Checklist

Before approving architecture verify:

✓ Singular nouns

✓ Explicit terminology

✓ Canonical vocabulary

✓ Correct layer terminology

✓ Correct Object naming

✓ Correct Model naming

✓ Correct Product naming

✓ Graph vs Network consistency

✓ No implementation leakage

---

# Final Principle

Architecture should read like a professional language.

A developer should understand the architecture simply by reading its names.

Good architecture begins with good naming.