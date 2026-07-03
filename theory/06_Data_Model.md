# 06 Data Model

> **The Factual Foundation of the Trademark Universe**

---

Version

**1.3**

Status

**Frozen**

Depends

- README.md
- CONSTITUTION.md
- 02_Architecture.md
- 03_Cognitive_Architecture.md
- 05_Entity_Model.md

Related

- 07_Brain.md
- 08_Intelligence.md

---

# Purpose

The Trademark Universe continuously changes.

MarkOrbit requires a trusted representation of those changes.

The purpose of Data is not simply to store information.

Its purpose is to continuously observe, preserve and publish facts about the Trademark Universe.

Data answers one question.

> **What is true?**

---

# Data Philosophy

Reality exists.

Reality is observed.

Observation becomes facts.

Facts become reusable data.

Data should faithfully describe reality.

It should never explain reality.

Explanation belongs to Brain.

Judgment belongs to Intelligence.

---

# The Data Pipeline

MarkOrbit continuously transforms observations through one permanent pipeline.

```
Reality

↓

Raw Sources

↓

Raw Data

↓

Entity Store

↓

Timeline

↓

Data Products
```

Each layer has exactly one responsibility.

---

# Reality

Reality exists outside MarkOrbit.

Examples include:

- Trademark Offices
- Government Registries
- Courts
- Enterprises
- Agencies
- Public Information
- Internal Business Systems

Reality is observed.

Reality is never modified.

---

# Raw Sources

Raw Sources describe where observations originate.

Examples include:

Official Sources

- CNIPA
- USPTO
- WIPO
- EUIPO

Commercial Sources

- Company Registries
- Domain Registries
- Marketplaces

Partner Sources

- Agencies
- Customers
- External Systems

Knowledge Sources belong to Brain.

They are not Raw Sources.

---

# Raw Data

Raw Data preserves original observations.

Raw Data should remain immutable.

Its purposes are:

- reproducibility
- auditing
- future reprocessing
- historical preservation

Raw Data should rarely be modified.

Raw Data may be archived.

---

# Entity Store

Raw observations are standardized into Entities.

Entity Store represents the latest known state of every Entity.

Entity Store answers:

> What is true now?

Entity Store is independent of storage technology.

---

# Timeline

Reality changes continuously.

Timeline records those changes.

Timeline answers:

> What changed?

Timeline is append-only.

History should never be overwritten.

Current State is derived from Timeline.

Timeline is the permanent historical record of MarkOrbit.

---

# Data Products

Applications should consume Data Products rather than storage systems.

Examples include:

- Trademark Current
- Trademark Timeline
- Brand Portfolio
- Owner Portfolio
- Entity Graph
- Renewal Queue
- Opportunity Feed

Data Products publish trusted facts.

They do not contain professional interpretation.

---

# Current State

Every Entity maintains one Current State.

Current State represents the latest verified observation.

Most operational systems consume Current State.

Current State should remain lightweight.

---

# Historical State

Timeline preserves history.

Historical State enables:

- auditing
- legal review
- statistical analysis
- intelligence
- business insight

Current State answers today.

Timeline explains yesterday.

---

# Entity Graph

Reality is interconnected.

Entities become valuable through relationships.

Examples include:

Trademark

↓

Owner

↓

Brand

↓

Customer

↓

Agency

↓

Attorney

↓

Workspace

Entity Graph represents these connections.

Relationships are first-class facts.

---

# Data Quality

Every Data Product should be measurable.

Quality dimensions include:

- Completeness
- Accuracy
- Freshness
- Consistency
- Traceability
- Confidence

Data quality should improve continuously.

---

# Data Evolution

Reality evolves continuously.

Data should evolve with reality.

New observations enrich existing Entities.

History accumulates.

Facts remain traceable.

Data should never lose historical integrity.

---

# Data and Brain

Data describes facts.

Brain explains facts.

Data should never contain professional conclusions.

Brain should never rewrite facts.

---

# Data and Intelligence

Intelligence evaluates facts.

Intelligence may recommend actions.

Data remains objective.

Recommendations never become facts until reality changes.

---

# Data and Capability

Capabilities consume Data.

Capabilities may create new Events.

Events update Timelines.

Timelines update Current State.

---

# Data and Workspace

Workspace consumes Data Products.

Workspace may enrich local information.

Workspace never modifies Core Data Products.

Global truth remains within MarkOrbit Core.

---

# Data Independence

Data defines facts.

Storage defines implementation.

Storage technologies may evolve.

Examples include:

- Parquet
- DuckDB
- PostgreSQL
- Iceberg
- ClickHouse

Implementation may change.

The Data Model should not.

---

# Design Principles

Observe before standardize.

Facts before knowledge.

History before overwrite.

Reference before duplication.

Products before storage.

Reality before implementation.

---

# Summary

Data is the factual foundation of MarkOrbit.

Reality becomes observations.

Observations become Entities.

Entities accumulate Timelines.

Timelines publish trusted Data Products.

Everything built upon MarkOrbit begins with trustworthy facts.