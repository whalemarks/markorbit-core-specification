# 05 Entity Model

> **The Digital Representation of the Trademark Universe**

---

Version

**1.3**

Status

**Frozen**

Depends

- README.md
- CONSTITUTION.md
- 01_Universe.md
- 02_Architecture.md
- 04_Ontology.md

Related

- 06_Data_Model.md
- 07_Brain.md
- 10_Workflow.md

---

# Purpose

The Trademark Universe exists independently of software.

MarkOrbit cannot operate directly on reality.

It therefore requires a digital representation.

This representation is called an Entity.

Entity is the fundamental modeling unit of MarkOrbit.

Every permanent object that requires independent identity is represented as an Entity.

---

# What Is an Entity

An Entity is the digital representation of an object within the Trademark Universe.

An Entity represents reality.

It is not reality itself.

Reality exists first.

Entity exists because software requires a stable representation of reality.

---

# Why Entity

Reality contains many different kinds of objects.

Examples include:

- trademarks
- brands
- owners
- agencies
- documents
- opportunities
- orders

Without a unified model, every product would define these objects differently.

Entity provides one common representation shared across the entire MarkOrbit ecosystem.

---

# Entity Principles

Every Entity follows the same permanent principles.

## Identity

Every Entity owns one permanent identity.

Identity never changes.

Names may change.

Status may change.

Relationships may change.

Identity remains constant.

---

## Lifecycle

Every Entity has a lifecycle.

Typical stages include:

```
Created

↓

Updated

↓

Referenced

↓

Archived
```

Lifecycle belongs to the Entity.

History should never be lost.

---

## Relationships

Entities never exist independently.

Every Entity may establish relationships with other Entities.

Examples include:

Owner owns Trademark.

Trademark belongs to Brand.

Agency represents Owner.

Customer manages Portfolio.

Relationships are independent objects of reality.

Relationships may evolve over time.

---

## Timeline

Every Entity may accumulate history.

History is represented through a Timeline.

Timeline records change.

Current State represents the latest observation.

Timeline preserves every significant event.

Current State should never replace history.

---

# Entity Categories

MarkOrbit defines several primary Entity categories.

## Actor

Actors perform actions.

Examples:

- Applicant
- Owner
- Customer
- Agency
- Attorney
- Examiner

---

## Asset

Assets possess legal or commercial value.

Examples:

- Trademark
- Brand
- Portfolio
- Domain
- Certificate

---

## Event

Events describe change.

Examples:

- Filing
- Registration
- Renewal
- Assignment
- Opposition
- Cancellation

Events generate timelines.

---

## Document

Documents preserve evidence.

Examples:

- Office Action
- Registration Certificate
- POA
- Agreement
- Invoice

Documents may reference many Entities.

Documents remain independent Entities.

---

## Business

Business Entities support commercial operation.

Examples:

- Opportunity
- Quote
- Order
- Invoice
- Project

Business Entities belong to operational activities.

---

# Global Entity

Global Entities belong to MarkOrbit Core.

Examples include:

- Trademark
- Brand
- Country
- Nice Class
- Goods
- Trademark Office

Global Entities are shared by every Workspace.

---

# Local Entity

Workspace may create local Entities.

Examples include:

- Internal Lead
- Local Tag
- Sales Note
- Customer Remark

Local Entities never replace Global Entities.

Local Entities may reference Global Entities.

---

# Entity Mirror

Workspace may mirror Global Entities.

```
Global Entity

↓

Workspace Mirror

↓

Local Operation
```

Mirror enables localization.

Mirror never modifies the original Entity.

---

# Entity State

Every Entity maintains one Current State.

Current State represents the latest known truth.

Historical changes belong to Timeline.

Applications primarily consume Current State.

Analysis consumes Timeline.

---

# Entity Relationships

Relationships are first-class structures.

A relationship may contain:

- identity
- lifecycle
- timeline
- attributes

Relationships should never be reduced to simple foreign keys.

The relationship itself often carries business meaning.

---

# Entity Evolution

Not every Entity deserves the same level of investment.

MarkOrbit supports progressive enrichment.

```
Entity

↓

Current State

↓

Timeline

↓

Knowledge Reference

↓

Intelligence

↓

Workspace Memory

↓

Digital Twin
```

High-value Entities gradually become richer.

Low-value Entities remain lightweight.

---

# Entity and Data

Data stores Entity facts.

Data never changes Entity identity.

Entity defines structure.

Data describes state.

---

# Entity and Brain

Brain never owns Entities.

Brain references Entities.

Brain explains Entities.

One Entity may generate multiple Brain Objects.

---

# Entity and Intelligence

Intelligence evaluates Entities.

It may produce:

- recommendations
- risks
- opportunities
- priorities

Intelligence never changes Entity identity.

---

# Entity and Capability

Capabilities consume Entities.

Capabilities never own Entities.

Capabilities may create new Entities as business results.

---

# Entity and Workflow

Workflow operates upon Entities.

Workflow creates Events.

Events update Timelines.

Timelines update Current State.

---

# Entity and Workspace

Workspace extends Entity through localization.

Workspace may attach:

- local configuration
- business context
- operational records
- organizational memory

Workspace never changes the Core definition of an Entity.

---

# Design Principles

Reality before Entity.

Identity before attributes.

Relationship before duplication.

Timeline before overwrite.

Reference before copy.

Global before local.

Entity before implementation.

---

# Summary

Entity is the universal modeling language of MarkOrbit.

Every permanent object in the Trademark Universe is represented as an Entity.

Entities possess identity, lifecycle, relationships and timelines.

They become richer through Data, Brain, Intelligence and Workspace.

Entity is the foundation upon which every higher layer of MarkOrbit is built.