# 320 Record Specification

> **The Canonical Information Record Model of the MarkOrbit Operating System**

---

Version

**2.0**

Status

**Draft**

Depends

- 300_Persistence_Specification.md
- 310_Source_Specification.md

Related

- 330_Store_Specification.md
- 340_Index_Specification.md
- 350_Product_Specification.md
- 200_Entity_Definition_Specification.md

---

# Purpose

Sources preserve original information.

Professional systems require structured information.

The purpose of Record is to transform original Sources into normalized, structured and traceable information suitable for professional processing.

Record answers one question.

> **What information has been extracted?**

Records preserve facts.

They do not interpret facts.

---

# Record Philosophy

Source represents origin.

Record represents facts.

Brain represents knowledge.

Intelligence represents judgment.

A Record should never contain assumptions.

A Record should never contain recommendations.

Records remain objective.

---

# Scope

Record applies to every normalized information object derived from one or more Sources.

Examples include:

- Trademark Record
- Applicant Record
- Office Record
- Renewal Record
- Assignment Record
- Opposition Record
- Invoice Record
- Contact Record

Every Record references at least one Source.

---

# Responsibilities

Record owns:

- normalized data
- structured attributes
- source lineage
- record identity
- validation status

Record does not own:

- interpretation
- recommendation
- workflow
- business decisions

---

# Record Model

Every Record follows the same model.

```text
Source

↓

Extraction

↓

Normalization

↓

Record
```

A Record represents one structured fact set.

---

# Record Identity

Every Record owns a permanent Record Identity.

Example

```text
REC-000000128
```

Record Identity remains stable.

Entity Identity remains independent.

One Record may later contribute to multiple Entities.

---

# Record Categories

Records belong to one primary category.

```text
Trademark Record

Applicant Record

Organization Record

Office Record

Document Record

Financial Record

Relationship Record

Event Record

Reference Record
```

Additional categories may be introduced.

---

# Trademark Record

Represents structured trademark information.

Typical attributes include:

- mark
- application number
- filing date
- status
- classes
- owner

Trademark Records remain factual.

They do not infer ownership changes.

---

# Applicant Record

Represents structured applicant information.

Examples include:

- organization name
- address
- country
- legal type

Applicant Records may later resolve into Actor Instances.

---

# Relationship Record

Represents factual relationships extracted from Sources.

Example

```text
Trademark

owned by

Company
```

Relationship reasoning belongs to later layers.

---

# Event Record

Represents factual historical observations.

Example

```text
Application Filed

Registration Granted

Renewal Recorded
```

Timeline later organizes Event Records.

---

# Record Structure

Every Record should include:

| Field | Required |
|--------|----------|
| Record ID | ✓ |
| Record Type | ✓ |
| Source Reference | ✓ |
| Extraction Time | ✓ |
| Schema Version | ✓ |
| Attributes | ✓ |
| Validation Status | ✓ |

Optional fields include:

- confidence
- parser version
- language
- notes

---

# Normalization

Normalization should produce:

- consistent field names
- consistent formats
- standardized values
- canonical encoding

Normalization should never alter factual meaning.

---

# Lineage

Every Record must preserve lineage.

```text
Source

↓

Record
```

Lineage should remain traceable throughout the system.

---

# Record Validation

Validation may include:

- schema validation
- required fields
- format consistency
- duplicate detection
- source integrity

Validation verifies Records.

It does not interpret them.

---

# Record Version

Records may evolve.

Corrections generate new Record Versions.

Original Records remain referenceable.

Historical accuracy is preserved.

---

# Record Registry

Registry stores Record Definitions.

Runtime stores Record Instances.

Definitions evolve slowly.

Instances accumulate continuously.

---

# Runtime

Runtime performs:

- extraction
- parsing
- normalization
- validation
- deduplication

Runtime should not interpret business meaning.

---

# Relationship to Entity

Records contribute to Entity creation.

Records are not Entities.

One Entity may aggregate multiple Records.

One Record may contribute to multiple Entities.

Entity resolution occurs after normalization.

---

# Relationship to Store

Stores preserve Records.

Stores organize Records.

Stores do not redefine Records.

---

# Relationship to Brain

Brain consumes Records or Products.

Brain creates knowledge.

Records remain factual evidence.

---

# Relationship to Intelligence

Intelligence reasons from Brain and Products.

Intelligence should not reason directly from unvalidated Records except in specialized scenarios.

---

# Compatibility

Record schemas evolve through versioning.

Historical Records remain valid.

Schema migration must preserve factual meaning.

---

# Extension

Future Record types may include:

- AI Observation Record
- Multimedia Record
- Sensor Record
- Compliance Record

Extensions must preserve normalization principles.

---

# Non Goals

Record is not:

- Source
- Entity
- Knowledge
- Recommendation
- Workflow State

Record represents structured facts.

Nothing more.

---

# Examples

Trademark Record

```text
Record

Trademark

Mark

MARKORBIT

Application Number

12345678

Source

CNIPA Monthly Dataset
```

Relationship Record

```text
Trademark

owned by

MarkOrbit Ltd.
```

Document Record

```text
Registration Certificate

Issued

2026-07-03

Source

USPTO
```

---

# Design Principles

Source before Record.

Facts before Knowledge.

Normalization before Storage.

Lineage before Optimization.

Objectivity before Interpretation.

Consistency before Convenience.

---

# Summary

Record defines the normalized factual information used throughout MarkOrbit.

Records transform original Sources into structured information while preserving traceability and objectivity.

Records provide the trusted factual foundation upon which Stores, Products, Brain and Intelligence are built.

Without Records, reliable professional knowledge cannot emerge.