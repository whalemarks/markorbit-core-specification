# Core 2.1 Patch 001

## Repository Alignment Patch

---

**Patch ID**

Core-2.1-Patch-001

**Target Version**

MarkOrbit Core Specification v2.1 RC1

**Type**

Repository Alignment

**Status**

Approved

---

# Purpose

This patch aligns the repository after introducing **Mo Business**.

Architecture design is already complete.

The following documents are the architectural source of truth.

- Architecture Amendment 001
- ADR-004 — Introduce Mo Business Layer
- 550_Business Module

This patch shall **NOT redesign the architecture**.

Its only purpose is to make the repository internally consistent.

---

# Scope

Allowed modifications:

- README
- repository navigation
- vocabulary
- architecture manifesto
- constitution
- changelog
- architecture references
- layer relationship descriptions

Not allowed:

- redesign architecture
- rewrite specifications
- modify Amendment 001
- modify ADR-004
- modify 550_Business
- introduce new architectural concepts

---

# File Modifications

---

## File 1

README.md

### Required

Update the Core Architecture overview.

Replace the previous architecture relationship

```
Mo Data

↓

Mo Brain

↓

Mo Intelligence
```

with

```
Mo Data

↓

Mo Brain

+

Mo Business

↓

Mo Intelligence
```

Add a short introduction of **Mo Business** as the Business Evaluation Layer.

Do not modify unrelated sections.

---

## File 2

specification/README.md

### Required

Add

```
550_Business
```

to the module navigation.

Keep numbering unchanged.

Do not reorder existing modules.

---

## File 3

001_Professional_Vocabulary.md

### Required

Add the following canonical vocabulary.

- Mo Business
- Business Evaluation
- Business Evidence
- Evaluation Target
- Evaluation Dimension
- Business Product

Do not rename existing terminology.

Do not remove existing entries.

---

## File 4

099_Architecture_Manifesto.md

### Required

Update the architecture responsibility model.

The canonical responsibility sequence becomes

```
Facts

↓

Professional Understanding

↓

Business Evaluation

↓

Intelligent Reasoning

↓

Capability Execution

↓

Context Organisation

↓

Experience Delivery
```

Do not rewrite the Manifesto.

Only align terminology.

---

## File 5

CONSTITUTION.md

### Required

Add one architecture rule.

Business Evaluation belongs exclusively to Mo Business.

Professional Understanding belongs exclusively to Mo Brain.

Intelligent Reasoning belongs exclusively to Mo Intelligence.

No responsibility overlap is permitted.

Do not modify existing constitutional rules.

---

## File 6

CHANGELOG.md

### Required

Add one new release entry.

Core Specification v2.1 RC1

Include:

- Architecture Amendment 001
- ADR-004
- Introduction of Mo Business
- 550_Business module

---

## File 7

400_Brain

### Required

Review only.

If necessary,

add a short section:

Relationship with Mo Business.

Clarify that

Mo Brain performs Professional Understanding only.

Do not change responsibilities.

---

## File 8

500_Intelligence

### Required

Review only.

Update dependency description.

Replace

```
Mo Data

↓

Mo Brain

↓

Mo Intelligence
```

with

```
Mo Data

↓

Mo Brain

+

Mo Business

↓

Mo Intelligence
```

Clarify that Intelligence consumes

- Professional Understanding
- Business Evaluation

Do not introduce Business logic.

---

## File 9

600_Capability

### Required

Review only.

Clarify that Capability consumes Business Evaluation.

Capability never performs Business Evaluation.

---

## File 10

700_Guide

### Required

Review only.

Verify terminology consistency.

No architectural changes.

---

## File 11

800_Workflow

### Required

Review only.

Clarify that Workflow may consume Business Evaluation.

Workflow never owns Business Evaluation.

---

## File 12

900_Workspace

### Required

Review only.

Clarify that Workspace presents Business Evaluation.

Workspace never calculates Business Evaluation.

---

# Repository Review

Search the entire repository.

Replace outdated architecture references.

Old

```
Mo Data

↓

Mo Brain

↓

Mo Intelligence
```

New

```
Mo Data

↓

Mo Brain

+

Mo Business

↓

Mo Intelligence
```

Only update architecture descriptions.

Do not rewrite documentation.

---

# Consistency Review

Verify:

- vocabulary consistency
- architecture terminology consistency
- module navigation
- broken cross references
- outdated architecture diagrams

---

# Deliverables

Produce

```
docs/review/Core-2.1-Repository-Alignment-Report.md
```

The report shall include

- files modified
- files reviewed
- architecture consistency
- terminology consistency
- cross-reference verification
- remaining issues (if any)

---

# Commit

```
chore: align repository for Core v2.1 RC1
```

---

# Constraints

The following files SHALL NOT be modified.

- Architecture-Amendment-001-Introduce-Mo-Business.md
- ADR-004-Introduce-Mo-Business-Layer.md
- specification/550_Business/*
- theory/09_Business.md

---

# Success Criteria

The repository shall appear as though **Mo Business has always been a native component of the Core Architecture**.

No architectural redesign shall occur.

No specification shall be rewritten.

Only repository alignment is permitted.