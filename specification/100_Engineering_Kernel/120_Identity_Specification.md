# 120 Identity Specification

> **The Global Identity System of MarkOrbit**

---

Version

**2.0**

Status

**Draft**

Depends

- 100_Specification_Guide.md
- 110_Registry_Framework.md
- MarkOrbit Core Foundation v1.3

Related

- 130_Relationship_Specification.md
- 140_Timeline_Specification.md
- 200_Entity_Specification.md

---

# Purpose

Every permanent object in MarkOrbit requires a stable identity.

Identity enables references.

References enable relationships.

Relationships enable the Operating System.

The purpose of Identity is to provide globally unique, stable and permanent identifiers for every Core object.

Identity answers one question.

> **Which object is this?**

Identity never answers:

> What is it?

That responsibility belongs to Ontology and Entity.

---

# Identity Philosophy

Identity is permanent.

Names change.

Attributes change.

Relationships change.

Versions change.

Identity does not.

Every permanent object should have exactly one identity.

Identity should never be reused.

Identity should never be reassigned.

---

# Scope

Identity applies to every permanent Core object.

Including:

- Ontology
- Entity
- Data Product
- Brain Object
- Knowledge Product
- Intelligence Object
- Intelligence Product
- Capability
- Workflow
- Workspace Definition

Runtime instances use separate Runtime IDs.

---

# Identity Responsibilities

Identity owns:

- uniqueness
- permanence
- referenceability

Identity does not own:

- business meaning
- lifecycle
- state
- version
- storage location

Identity is purely identification.

---

# Identity Model

Every Identity consists of two parts.

```
Identity

=

Type Prefix

+

Global Number
```

Example

```
TM-00000001

CAP-00000342

WF-00000108

BO-00000451
```

Identity format should remain human-readable.

---

# Identity Characteristics

Every Identity must satisfy the following principles.

## Global

Identity must be globally unique.

No two permanent objects may share one Identity.

---

## Stable

Identity never changes.

Even if:

- name changes
- owner changes
- schema changes
- version changes

Identity remains identical.

---

## Permanent

Identity is never recycled.

Archived objects retain their Identity.

Deleted runtime data does not release Identity.

---

## Meaningless

Identity should not encode business meaning.

Avoid embedding:

- country
- customer
- date
- owner
- workspace

Identity identifies.

Metadata describes.

---

## Referenceable

Every permanent object should be referenced by Identity.

Objects should not be referenced by name.

Names are mutable.

Identity is immutable.

---

# Identity Categories

Each permanent object type owns a dedicated prefix.

Examples

| Prefix | Object |
|---------|--------|
| ONT | Ontology |
| ENT | Entity Type |
| TM | Trademark |
| BR | Brand |
| ACT | Actor |
| DOC | Document |
| DP | Data Product |
| BO | Brain Object |
| KP | Knowledge Product |
| IO | Intelligence Object |
| IP | Intelligence Product |
| CAP | Capability |
| WF | Workflow |
| WS | Workspace Definition |

Additional prefixes may be introduced through Registry.

Prefixes should never overlap.

---

# Runtime Identity

Definitions and runtime instances are different.

Example

```
Capability

CAP-000201

↓

Execution

CAPRUN-20260703-000018
```

Definition Identity remains permanent.

Runtime Identity exists only during execution.

Runtime Identity should never replace Definition Identity.

---

# Identity Lifecycle

Identity itself has no lifecycle.

The object referenced by the Identity owns the lifecycle.

Example

```
Identity

TM-00000321

↓

Trademark

Draft

↓

Active

↓

Archived
```

Identity remains unchanged throughout the lifecycle.

---

# Identity and Version

Version belongs to the object.

Not to the Identity.

Example

```
CAP-000201

Version 1.0

↓

Version 2.0

↓

Version 2.1
```

Identity remains constant.

Version evolves.

---

# Identity and Registry

Registry assigns Identity.

Registry guarantees uniqueness.

Registry records:

- identity
- object type
- owner
- status
- version

Identity should never be created outside Registry.

---

# Identity and Relationship

Relationships reference Identities.

Example

```
TM-00000321

owned_by

ACT-00000872
```

Relationships should never depend on names.

Relationships always reference Identity.

---

# Identity and Timeline

Timeline records events against Identity.

Example

```
TM-00000321

↓

Filed

↓

Registered

↓

Renewed

↓

Assigned
```

Timeline belongs to Identity.

Identity connects every historical event.

---

# Identity and Workspace

Workspace never changes Core Identity.

Workspace may assign:

- aliases
- local codes
- internal references

These remain local metadata.

Core Identity remains authoritative.

---

# Identity Validation

Every Identity must satisfy:

- globally unique
- immutable
- registered
- correctly prefixed
- non-null
- non-reusable

Validation failure should prevent object creation.

---

# Reserved Identity

Reserved Identities may exist before object creation.

Example

```
CAP-000450

Status

Reserved
```

Reserved Identities should expire if unused.

Reservation policies are defined by Registry.

---

# Deprecated Identity

Deprecated objects retain Identity.

Identity should never be reassigned.

Deprecated Identity remains referenceable for historical consistency.

---

# Compatibility

Identity is the foundation of backward compatibility.

Applications may evolve.

Schemas may evolve.

Contracts may evolve.

Identity should remain stable across all versions.

---

# Extension

Future extensions may include:

- distributed identity generation
- offline identity allocation
- federation between MarkOrbit installations
- cross-registry identity resolution

Extensions must preserve global uniqueness.

---

# Non Goals

Identity is not:

- a database primary key
- a UUID implementation
- a storage address
- a business code
- a display name

Implementation details remain independent.

---

# Examples

Trademark

```
TM-00000128
```

Capability

```
CAP-00000412
```

Brain Object

```
BO-00000987
```

Workflow

```
WF-00000076
```

Workspace Definition

```
WS-00000015
```

---

# Design Principles

Identity before Relationship.

Identity before Timeline.

Identity before Version.

Reference before Duplication.

Registry before Implementation.

Permanence before Convenience.

---

# Summary

Identity is the permanent identification system of MarkOrbit.

Every permanent object receives one globally unique and immutable Identity.

Identity enables references.

References enable relationships.

Relationships enable the Operating System.

Without stable Identity, no other Core specification can function reliably.