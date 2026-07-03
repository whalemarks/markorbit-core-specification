# 330 Store Specification

> **The Canonical Persistence Store Model of the MarkOrbit Operating System**

---

Version

**2.0**

Status

**Draft**

Depends

- 300_Persistence_Specification.md
- 310_Source_Specification.md
- 320_Record_Specification.md

Related

- 340_Index_Specification.md
- 350_Product_Specification.md
- 200_Entity_Definition_Specification.md
- 140_Timeline_Specification.md

---

# Purpose

Records preserve structured facts.

Professional systems require those Records to be organized for reliable retrieval, governance and long-term evolution.

The purpose of Store is to define how Records are grouped into persistent semantic collections.

Store answers one question.

> **Where should this information live?**

---

# Store Philosophy

Store is not a database.

Store is a semantic collection.

Different databases may implement the same Store.

Different Stores may share one database.

Technology changes.

Semantic responsibility remains.

---

# Scope

Store applies to every persistent collection of Records inside MarkOrbit.

Examples include:

- Trademark Store
- Actor Store
- Asset Store
- Relationship Store
- Event Store
- Timeline Store
- Document Store
- Reference Store

Store organizes information.

Store does not interpret information.

---

# Responsibilities

Store owns:

- persistence organization
- collection boundaries
- retention
- retrieval
- consistency
- lineage preservation

Store does not own:

- parsing
- normalization
- reasoning
- recommendation
- workflow execution

---

# Store Model

Every Store follows the same architecture.

```text
Records

↓

Validation

↓

Store

↓

Index

↓

Product
```

Store accepts validated Records.

Store publishes persistent collections.

---

# Store Categories

Stores are organized by semantic responsibility.

```
Reference Store

↓

Actor Store

↓

Asset Store

↓

Relationship Store

↓

Document Store

↓

Event Store

↓

Timeline Store

↓

Business Store
```

Additional Stores may be introduced.

---

# Reference Store

Stores globally shared Reference Records.

Examples include:

- Countries
- Offices
- Nice Classes
- Vienna Codes
- Languages

Reference Store changes infrequently.

---

# Actor Store

Stores Actor Records.

Examples include:

- Organizations
- Persons
- Government Offices
- AI Agents

Actor Store supports identity resolution.

---

# Asset Store

Stores Asset Records.

Examples include:

- Trademark
- Brand
- Portfolio
- Patent

Asset Store becomes one of the primary operational Stores.

---

# Relationship Store

Stores Relationship Records.

Relationship Store enables graph traversal.

Relationships remain explicit.

---

# Document Store

Stores Document metadata.

Binary files remain implementation-specific.

Document Store preserves evidence metadata.

---

# Event Store

Stores immutable Event Records.

Event Store is append-only.

Existing Events should never be modified.

---

# Timeline Store

Stores reconstructed Timelines.

Timeline Store supports:

- replay
- auditing
- historical analysis

Timeline remains derived from Events.

---

# Business Store

Stores Business Object Records.

Examples include:

- Opportunities
- Orders
- Projects
- Journeys

Business Store supports operational activities.

---

# Store Identity

Every Store owns a Store Definition.

Example

```text
STORE-000021

Asset Store
```

Stores are Registry Definitions.

Runtime implementations remain independent.

---

# Store Characteristics

Every Store should satisfy the following principles.

## Persistent

Information should survive Runtime.

---

## Traceable

Every Record preserves Source lineage.

---

## Versioned

Schema evolution should remain compatible.

---

## Consistent

Records should satisfy validation before persistence.

---

## Recoverable

Store should support reconstruction from preserved Records.

---

# Retention

Every Store defines a retention policy.

Examples include:

- permanent
- configurable
- regulatory
- workspace-specific

Retention policies belong to Store Definitions.

---

# Store Validation

Before persistence:

- schema validation
- contract validation
- duplicate detection
- lineage validation
- reference validation

Validation should complete before storage.

---

# Store Registry

Registry stores:

- Store Definition
- Contract
- Lifecycle
- Retention Policy
- Compatibility Rules

Runtime stores Store Instances.

---

# Runtime

Runtime performs:

- persistence
- retrieval
- synchronization
- backup
- migration

Runtime never changes Store semantics.

---

# Relationship to Index

Stores preserve information.

Indexes optimize access.

Indexes never replace Stores.

---

# Relationship to Product

Products consume one or more Stores.

Products expose curated information.

Stores remain neutral.

---

# Relationship to Brain

Brain consumes Products.

Brain should avoid coupling directly to implementation-specific Stores.

---

# Relationship to Intelligence

Intelligence reasons from Products.

Stores provide trusted persistence.

They do not generate recommendations.

---

# Compatibility

Store Definitions evolve conservatively.

Historical Records remain available.

Schema migration must preserve lineage.

---

# Extension

Future Store types may include:

- Graph Store
- Vector Store
- Knowledge Store
- Archive Store
- Analytics Store
- Compliance Store

Extensions must preserve Store responsibilities.

---

# Non Goals

Store is not:

- Database
- Table
- Bucket
- File System
- Object Storage
- Search Engine

Those implement Stores.

They are not Stores.

---

# Examples

Asset Store

```text
Asset Store

Contains

Trademark Records

Brand Records

Patent Records
```

Event Store

```text
Append Only

↓

Event Records

↓

Replay
```

Reference Store

```text
Countries

Languages

Currencies

Nice Classes
```

---

# Design Principles

Record before Store.

Semantics before Technology.

Persistence before Optimization.

Lineage before Performance.

Consistency before Scalability.

Meaning before Implementation.

---

# Summary

Store defines the persistent semantic collections used by MarkOrbit.

Stores organize validated Records into long-lived repositories while preserving lineage, consistency and recoverability.

Stores are semantic concepts rather than database implementations.

They provide the durable foundation upon which Indexes, Products, Brain and Intelligence are built.