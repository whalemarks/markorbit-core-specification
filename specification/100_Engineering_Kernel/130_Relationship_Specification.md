# 130 Relationship Specification

> **The Relationship System of MarkOrbit**

---

Version

**2.0**

Status

**Draft**

Depends

- 100_Specification_Guide.md
- 110_Registry_Framework.md
- 120_Identity_Specification.md
- MarkOrbit Core Foundation v1.3

Related

- 140_Timeline_Specification.md
- 200_Entity_Definition_Specification.md
- 300_Persistence_Specification.md

---

# Purpose

Reality is not a collection of isolated objects.

Reality is a network of relationships.

The purpose of Relationship is to define how permanent objects are connected within the Trademark Universe.

Relationship answers one question.

> **How are two objects connected?**

Objects create the operating system.

Relationships create the universe.

---

# Relationship Philosophy

Identity defines an object.

Relationship defines meaning.

An isolated Trademark has limited value.

A Trademark connected to its Owner, Brand, Portfolio, Attorney, Customer and Workspace becomes meaningful.

Relationship is therefore a first-class object in MarkOrbit.

Relationship is never treated as a simple foreign key.

---

# Scope

Relationship applies to every permanent object that references another permanent object.

Examples include:

- Trademark → Owner
- Trademark → Brand
- Trademark → Goods
- Trademark → Country
- Customer → Workspace
- Capability → Brain Object
- Workflow → Capability
- Brain Object → Ontology

Relationships exist across all Core domains.

---

# Responsibilities

Relationship owns:

- connection
- semantics
- direction
- cardinality
- validity
- relationship lifecycle

Relationship does not own:

- object identity
- object state
- object data
- business execution

---

# Relationship Model

Every Relationship consists of:

```
Subject

↓

Relationship Type

↓

Object
```

Example

```
Trademark

owned_by

Owner
```

Another example

```
Capability

depends_on

Brain Object
```

Relationship itself is an independent Core object.

---

# Relationship Identity

Every Relationship owns a permanent Identity.

Example

```
REL-00000028
```

Relationship Identity follows the Identity Specification.

Relationship Identity never changes.

---

# Relationship Characteristics

Every Relationship must satisfy the following principles.

## Explicit

Relationships should always be explicitly defined.

Implicit relationships should be avoided.

---

## Directional

Every Relationship has a direction.

Example

```
Trademark

owned_by

Owner
```

does not automatically imply

```
Owner

owns

Trademark
```

Reverse relationships should be derived rather than duplicated whenever possible.

---

## Typed

Every Relationship belongs to one Relationship Type.

Examples include:

- owns
- belongs_to
- represents
- filed_by
- depends_on
- produces
- consumes
- references
- manages
- contains

Relationship Type defines meaning.

---

## Semantic

Relationships carry business meaning.

A relationship is not merely a technical link.

Example

```
Trademark

belongs_to

Brand
```

contains professional meaning.

This meaning should be preserved.

---

## Independent

Relationship should never be stored merely as an object attribute.

Relationship owns:

- identity
- metadata
- lifecycle
- timeline

Relationship is an independent resource.

---

# Relationship Categories

MarkOrbit recognizes several categories of relationships.

## Ownership

Examples

```
Trademark

owned_by

Owner
```

```
Portfolio

owned_by

Customer
```

---

## Composition

Examples

```
Brand

contains

Trademark
```

```
Portfolio

contains

Trademark
```

---

## Reference

Examples

```
Brain Object

references

Ontology
```

```
Capability

references

Brain Object
```

---

## Dependency

Examples

```
Workflow

depends_on

Capability
```

```
Capability

depends_on

Knowledge Product
```

---

## Operation

Examples

```
Guide

selects

Capability
```

```
Workflow

executes

Capability
```

---

## Association

Examples

```
Workspace

manages

Customer
```

```
Attorney

handles

Trademark
```

Association represents collaboration rather than ownership.

---

# Cardinality

Every Relationship defines cardinality.

Supported cardinalities include:

```
One → One

One → Many

Many → One

Many → Many
```

Cardinality belongs to the Relationship.

It should never be inferred.

---

# Relationship Attributes

A Relationship may contain metadata.

Examples include:

- effective date
- expiration date
- role
- priority
- confidence
- source
- notes

Attributes describe the relationship.

They do not describe either object.

---

# Relationship Lifecycle

Relationships evolve independently.

Typical lifecycle:

```
Draft

↓

Active

↓

Updated

↓

Deprecated

↓

Archived
```

Removing a relationship should not erase history.

---

# Relationship Timeline

Relationships generate events.

Example

```
Ownership Created

↓

Ownership Changed

↓

Ownership Transferred

↓

Ownership Archived
```

Relationship Timeline is independent of Entity Timeline.

---

# Relationship Version

Relationship contracts may evolve.

Relationship Identity remains stable.

Relationship Version changes only when its definition changes.

Relationship data changes do not require a new version.

---

# Relationship Validation

Every Relationship must pass validation.

Validation includes:

- valid subject
- valid object
- valid relationship type
- cardinality compliance
- lifecycle compatibility
- circular dependency detection (where applicable)

Invalid relationships should never enter the Registry.

---

# Relationship and Registry

Relationship definitions belong to Registry.

Registry maintains:

- relationship type
- semantics
- constraints
- version
- compatibility

Relationship instances belong to runtime data.

---

# Relationship and Entity

Entities do not own relationships.

Relationships connect Entities.

Removing an Entity should not silently destroy historical relationships.

---

# Relationship and Timeline

Relationship changes produce Events.

Events update Relationship Timeline.

Relationship Timeline preserves historical evolution.

---

# Relationship and Brain

Brain references Entities through Relationships.

Knowledge Graph is fundamentally a graph of Relationships.

Brain should not duplicate relationship definitions.

---

# Relationship and Intelligence

Intelligence reasons across Relationships.

Examples include:

- portfolio completeness
- ownership risk
- dependency analysis
- opportunity discovery

Rich relationships enable richer reasoning.

---

# Relationship and Capability

Capabilities consume Relationships.

Capabilities may also create or modify Relationships.

Relationship rules remain governed by this specification.

---

# Relationship and Workflow

Workflow orchestrates relationship changes.

Examples include:

- ownership transfer
- attorney assignment
- customer onboarding

Workflow executes change.

Relationship preserves structure.

---

# Relationship and Workspace

Workspace may create local Relationships.

Examples include:

- internal account manager
- customer segment
- sales ownership

Local Relationships must never overwrite Core Relationships.

Workspace Relationships remain isolated.

---

# Compatibility

Relationship Types should evolve carefully.

Existing Relationship Identities remain stable.

Breaking semantic changes require a new Relationship Type rather than redefining an existing one.

---

# Extension

Future extensions may include:

- inferred relationships
- temporal relationships
- confidence-weighted relationships
- semantic relationship reasoning
- graph optimization

Extensions must preserve explicit semantics.

---

# Non Goals

Relationship is not:

- a foreign key
- a join table
- a database implementation
- a UI navigation structure

Those belong to implementation.

Relationship defines meaning.

---

# Examples

Ownership

```
REL-00000128

Trademark

owned_by

Owner
```

Dependency

```
REL-00000876

Workflow

depends_on

Capability
```

Knowledge Reference

```
REL-00002108

Brain Object

references

Ontology
```

---

# Design Principles

Relationship before navigation.

Semantics before storage.

Explicit before implicit.

Reference before duplication.

Meaning before implementation.

History before deletion.

---

# Summary

Relationship is the semantic connection system of MarkOrbit.

It transforms independent objects into an interconnected professional universe.

Every Relationship has its own identity, lifecycle, semantics and history.

Relationships are first-class Core objects.

They enable knowledge graphs, professional reasoning, workflow orchestration and organizational collaboration throughout the Trademark Universe.