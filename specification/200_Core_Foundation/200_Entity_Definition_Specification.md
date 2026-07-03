# 200 Entity Definition Specification

> **The Canonical Definition Model of Permanent Objects in MarkOrbit**

---

Version

**2.0**

Status

**Draft**

Depends

- 100_Specification_Guide.md
- 110_Registry_Framework.md
- 120_Identity_Specification.md
- 130_Relationship_Specification.md
- 170_Contract_Model.md

Related

- 210_Actor_Specification.md
- 220_Asset_Specification.md
- 150_Event_Specification.md
- 240_Document_Specification.md
- 250_Business_Object_Specification.md

---

# Purpose

Reality consists of identifiable objects.

MarkOrbit represents those objects through Entity Definitions.

The purpose of Entity Definition is to provide a canonical and reusable description of every permanent object in the Trademark Universe.

Entity Definition answers one question.

> **What is this object?**

Entity Definition describes the object.

Entity Instances represent individual occurrences.

---

# Entity Philosophy

Reality exists.

Entities describe reality.

Instances represent reality.

Entity Definitions are permanent.

Entity Instances are temporary representations of reality.

One Definition.

Many Instances.

---

# Scope

Entity Definitions apply to every permanent object represented by MarkOrbit.

Examples include:

- Trademark
- Brand
- Applicant
- Organization
- Person
- Country
- Office
- Goods
- Services
- Case
- Portfolio
- Document

Definitions belong to the Core.

Instances belong to Runtime.

---

# Responsibilities

Entity Definition owns:

- semantic definition
- required attributes
- optional attributes
- identity rules
- relationship rules
- lifecycle definition
- validation rules

Entity Definition does not own:

- instance data
- runtime state
- business workflow
- current values

---

# Entity Model

Every Entity consists of two layers.

```
Entity Definition

↓

Entity Instance
```

Definition is architectural.

Instance is operational.

---

# Entity Definition

An Entity Definition describes one object type.

Example

```
Trademark
```

Definition specifies:

- attributes
- relationships
- lifecycle
- contracts
- validation

Definition never stores business data.

---

# Entity Instance

Entity Instance represents one object in reality.

Example

```
Trademark

↓

TM-00000128

↓

"MARKORBIT"
```

Every Instance references exactly one Entity Definition.

---

# Entity Characteristics

Every Entity Definition should satisfy the following principles.

## Canonical

One Definition should describe one concept.

Duplicate Definitions should not exist.

---

## Stable

Definitions evolve slowly.

Business data changes frequently.

---

## Reusable

Definitions should be reused across:

- Workspace
- Products
- Guide
- Workflow
- Capability

---

## Independent

Definitions should not depend on implementation.

Implementation consumes Definitions.

---

## Extensible

Definitions may declare Extension Points.

Extensions must preserve the original Definition.

---

# Entity Contract

Every Entity Definition exposes a Contract.

The Contract defines:

- identity
- attributes
- relationships
- lifecycle
- validation
- compatibility

Implementations depend on the Contract.

---

# Entity Attributes

Attributes describe the Entity itself.

Each Attribute defines:

- name
- type
- required
- default value
- validation rule

Example

Trademark

```
Name

Jurisdiction

Application Number

Registration Number

Status
```

Attributes should describe the Entity.

Not its relationships.

---

# Entity Relationships

Relationships belong to Relationship Specification.

Entity Definition only declares supported Relationship Types.

Example

Trademark

supports:

- owned_by
- belongs_to
- filed_in
- represented_by

Relationship instances are managed independently.

---

# Entity Lifecycle

Every Entity Definition declares its Lifecycle.

Example

Trademark

```
Draft

↓

Filed

↓

Published

↓

Registered

↓

Renewed

↓

Expired

↓

Archived
```

Lifecycle belongs to the Definition.

State belongs to the Instance.

---

# Entity Validation

Entity Definitions declare validation requirements.

Examples:

- required attributes
- required relationships
- unique constraints
- lifecycle constraints

Validation Framework performs validation.

---

# Entity Registry

Every Entity Definition belongs to the Entity Registry.

Registry stores:

- Identity
- Name
- Version
- Contract
- Lifecycle
- Validation Rules

Registry does not store Entity Instances.

---

# Entity Runtime

Runtime creates Entity Instances.

Instances reference:

```
Entity Definition

↓

Runtime Context

↓

Current State
```

Runtime never modifies the Definition.

---

# Entity Versioning

Entity Definitions evolve.

Examples:

```
Trademark v1.0

↓

Trademark v1.1

↓

Trademark v2.0
```

Entity Identity remains unchanged.

Contracts determine compatibility.

---

# Entity Extension

Entity Definitions expose Extension Points.

Workspace may add:

- local fields
- local metadata
- local validation

Extensions must not redefine Core semantics.

---

# Entity Categories

Entity Definitions are organized into categories.

```
Actor

Asset

Document

Business

Reference

Infrastructure
```

Detailed specifications begin with:

- 210 Actor
- 220 Asset
- 230 Event Entity
- 240 Document
- 250 Business Entity

---

# Entity Compatibility

Existing Entity Definitions should remain compatible.

Breaking semantic changes require:

- new major version
- migration path
- compatibility documentation

---

# Non Goals

Entity Definition is not:

- a database table
- an ORM model
- a JSON schema
- a UI form
- a runtime object

Those implement the Definition.

They are not the Definition.

---

# Examples

Entity Definition

```
Trademark

Identity

ENT-000021

Attributes

Name

Jurisdiction

Application Number

Lifecycle

Trademark Lifecycle
```

Entity Instance

```
TM-00000128

Definition

Trademark

Name

MARKORBIT

Current State

Registered
```

---

# Design Principles

Definition before Instance.

Semantics before Storage.

Relationships before Foreign Keys.

Contract before Implementation.

Registry before Runtime.

Stability before Convenience.

---

# Summary

Entity Definition is the canonical semantic description of every permanent object in MarkOrbit.

Definitions describe object types.

Instances represent real-world objects.

Definitions are managed by Registry.

Instances execute in Runtime.

Together they provide the foundation for every higher-level capability in the MarkOrbit Operating System.