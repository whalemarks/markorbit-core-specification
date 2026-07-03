# 340 Index Specification

> **The Discoverability Model of the MarkOrbit Operating System**

---

Version

**2.0**

Status

**Draft**

Depends

- 300_Persistence_Specification.md
- 310_Source_Specification.md
- 320_Record_Specification.md
- 330_Store_Specification.md

Related

- 350_Product_Specification.md
- 400_Brain_Specification.md
- 500_Intelligence_Specification.md

---

# Purpose

Stores preserve information.

Professionals must be able to discover information quickly, consistently and intelligently.

The purpose of Index is to organize persistent information for efficient discovery.

Index answers one question.

> **How can this information be found?**

---

# Index Philosophy

Store preserves.

Index discovers.

Store focuses on persistence.

Index focuses on retrieval.

Indexes should never become the source of truth.

Indexes exist only to improve discoverability.

---

# Scope

Index applies to every searchable, filterable or navigable collection.

Examples include:

- Trademark Name Index
- Registration Number Index
- Applicant Index
- Brand Index
- Nice Class Index
- Country Index
- Relationship Index
- Timeline Index
- Full Text Index

Indexes serve every higher layer.

---

# Responsibilities

Index owns:

- discoverability
- search optimization
- filtering
- sorting
- navigation
- lookup acceleration

Index does not own:

- source data
- persistence
- business meaning
- recommendations
- workflow logic

---

# Index Model

Every Index follows one architecture.

```text
Store

↓

Index Builder

↓

Index

↓

Query

↓

Result
```

Indexes are always derived.

They never replace Stores.

---

# Index Categories

Indexes may be organized by purpose.

```
Identity Index

Attribute Index

Relationship Index

Timeline Index

Text Index

Geographic Index

Semantic Index

Composite Index
```

---

# Identity Index

Optimizes lookup by permanent Identity.

Examples:

- TM Identity
- Brand Identity
- Actor Identity

Identity Index should be unique.

---

# Attribute Index

Indexes structured attributes.

Examples:

- Trademark Name
- Registration Number
- Filing Date
- Applicant Name

Supports filtering and sorting.

---

# Relationship Index

Indexes graph relationships.

Examples:

- owned_by
- represented_by
- belongs_to
- references

Supports graph traversal.

---

# Timeline Index

Indexes historical events.

Examples:

- filing date
- renewal date
- assignment date

Supports chronological analysis.

---

# Text Index

Indexes textual content.

Examples:

- Office Actions
- Decisions
- Knowledge Articles
- Client Notes

Supports full-text search.

---

# Geographic Index

Indexes geographic dimensions.

Examples:

- Country
- Region
- Office
- Madrid Members

Supports regional discovery.

---

# Semantic Index

Indexes concepts rather than literal values.

Examples:

- Brand Category
- Industry
- Trademark Similarity
- Legal Topic

Semantic Index may leverage Brain.

---

# Composite Index

Combines multiple dimensions.

Example

```text
Trademark

+

Country

+

Nice Class

+

Status
```

Composite Index optimizes complex retrieval.

---

# Index Characteristics

Every Index should satisfy:

## Derived

Indexes are generated from Stores.

---

## Rebuildable

Indexes should be reproducible.

They should never contain unique information unavailable elsewhere.

---

## Consistent

Indexes should reflect the current persisted state.

---

## Independent

One Index should not depend on another unnecessarily.

---

## Disposable

Indexes may be rebuilt without losing business information.

---

# Index Lifecycle

Typical lifecycle:

```text
Created

↓

Built

↓

Updated

↓

Rebuilt

↓

Retired
```

Rebuilding should not change semantic meaning.

---

# Index Validation

Validation may include:

- completeness
- consistency
- duplicate detection
- synchronization
- rebuild verification

Indexes should remain synchronized with Stores.

---

# Runtime

Runtime performs:

- indexing
- rebuilding
- synchronization
- optimization

Runtime never changes Store semantics.

---

# Relationship to Store

Stores preserve information.

Indexes organize information.

Stores remain authoritative.

---

# Relationship to Product

Products query Indexes.

Products should avoid scanning raw Stores whenever practical.

---

# Relationship to Brain

Brain may consume semantic Indexes.

Brain should not depend on implementation-specific indexing engines.

---

# Relationship to Intelligence

Intelligence benefits from efficient discovery.

Indexes improve retrieval speed.

Indexes do not create intelligence.

---

# Compatibility

Index definitions evolve independently.

Rebuilding should preserve discoverability.

Historical Stores remain unaffected.

---

# Extension

Future Index types may include:

- Vector Index
- Embedding Index
- Graph Index
- Hybrid Search Index
- AI Retrieval Index

All extensions should preserve the principles of discoverability.

---

# Non Goals

Index is not:

- Database
- Store
- Cache
- Knowledge
- Recommendation

Index accelerates discovery.

Nothing more.

---

# Examples

Trademark Name Index

```text
Trademark Name

↓

TM-00000128
```

Relationship Index

```text
Trademark

↓

owned_by

↓

Company
```

Timeline Index

```text
Renewal Date

↓

Trademark Portfolio
```

---

# Design Principles

Store before Index.

Discovery before Optimization.

Rebuild before Backup.

Consistency before Performance.

Navigation before Implementation.

Derived before Persistent.

---

# Summary

Index defines how persistent information becomes discoverable within MarkOrbit.

Indexes organize Stores into efficient retrieval structures without becoming the source of truth.

They provide fast, reliable and consistent discovery for Products, Brain and Intelligence while remaining fully rebuildable from persistent data.