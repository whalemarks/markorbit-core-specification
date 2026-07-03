# 230 Reference Specification

> **The Canonical Reference System of the Trademark Universe**

---

Version

**2.0**

Status

**Draft**

Depends

- 120_Identity_Specification.md
- 130_Relationship_Specification.md
- 170_Contract_Model.md
- 200_Entity_Definition_Specification.md

Related

- 220_Asset_Specification.md
- 240_Document_Specification.md
- 300_Persistence_Specification.md
- 400_Brain_Specification.md

---

# Purpose

Not every Entity represents a business object.

Some Entities exist to provide common meaning.

Reference defines every standardized object shared throughout the Trademark Universe.

Reference answers one question.

> **What shared knowledge does everyone use?**

---

# Reference Philosophy

Reference does not own business.

Reference defines standards.

Reference is shared.

Reference is stable.

Reference should never become Workspace-specific.

Reference enables consistency.

---

# Scope

Reference includes every globally shared definition.

Examples include:

- Country
- Region
- Language
- Currency
- Nice Class
- Vienna Classification
- Trademark Status
- Office
- Legal Basis
- Procedure Type
- Document Type

Reference Definitions belong to Core.

Workspace may reference them.

Workspace must not redefine them.

---

# Responsibilities

Reference owns:

- standardized meaning
- globally shared values
- identifiers
- canonical definitions

Reference does not own:

- customer data
- workflow state
- runtime values
- organization configuration

---

# Reference Categories

Reference consists of multiple categories.

```
Reference

├── Geography
├── Classification
├── Legal
├── Procedure
├── Status
├── Language
├── Currency
├── Office
├── Document Type
└── Other Reference
```

---

# Geography

Examples include:

- Country
- Territory
- Region

Examples

```
China

United States

European Union

Madrid Members
```

These are shared definitions.

---

# Classification

Examples include:

- Nice Classification
- Vienna Classification
- Goods Group
- Service Group

Classification supports:

- Brain
- Capability
- Validation

Classification Definitions remain versioned.

---

# Legal Reference

Examples include:

- Trademark Law
- Treaty
- Convention
- Regulation
- Administrative Rule

Legal References describe legal foundations.

They do not provide interpretation.

Interpretation belongs to Brain.

---

# Procedure

Examples include:

- Filing
- Renewal
- Assignment
- Opposition
- Cancellation
- Appeal

Procedure Definitions support Workflow.

Workflow executes Procedures.

Reference defines them.

---

# Status

Examples include:

- Filed
- Under Examination
- Published
- Registered
- Renewed
- Expired
- Refused

Status Definitions are shared.

Individual Assets maintain Current State.

---

# Language

Examples include:

- English
- Chinese
- Japanese
- Korean
- Spanish

Language Definitions are globally shared.

Translations belong elsewhere.

---

# Currency

Examples include:

- USD
- EUR
- CNY
- JPY

Currency Definitions support pricing.

Exchange rates belong to Data Products.

---

# Office

Examples include:

- USPTO
- CNIPA
- EUIPO
- WIPO
- JPO
- KIPO

Office is a Reference Definition.

Operational data belongs to Entity Instances.

---

# Document Type

Examples include:

- Application
- Registration Certificate
- Office Action
- Assignment Record
- Power of Attorney

Document Types classify Documents.

They do not store Documents.

---

# Reference Contract

Every Reference Definition exposes:

- Identity
- Category
- Canonical Name
- Supported Relationships
- Lifecycle
- Validation Rules

Reference Contracts evolve conservatively.

---

# Reference Relationships

Reference commonly supports:

- classified_by
- governed_by
- filed_in
- issued_by
- uses_language
- uses_currency

Relationship semantics remain independent.

---

# Reference Lifecycle

Typical lifecycle:

```
Draft

↓

Released

↓

Updated

↓

Deprecated

↓

Archived
```

Many Reference Definitions remain stable for decades.

---

# Reference Registry

Reference Definitions belong to Registry.

Registry stores:

- Identity
- Category
- Version
- Contract
- Lifecycle

Reference data should be globally consistent.

---

# Runtime

Runtime consumes Reference Definitions.

Runtime should never modify them.

Reference Instances are read-only during execution.

---

# Compatibility

Reference Definitions prioritize backward compatibility.

Existing identifiers should remain stable.

Semantic changes require versioning.

---

# Extension

Workspace may extend Reference through:

- aliases
- display names
- localization
- presentation metadata

Workspace must not redefine canonical meaning.

---

# Non Goals

Reference is not:

- business data
- customer configuration
- runtime state
- workflow logic
- knowledge interpretation

Reference provides shared definitions.

Nothing more.

---

# Examples

Country

```
Reference

Country

China
```

Nice Class

```
Reference

Nice Class

Class 25
```

Trademark Status

```
Reference

Registered
```

Office

```
Reference

USPTO
```

---

# Design Principles

Canonical before Local.

Reference before Duplication.

Standard before Configuration.

Meaning before Presentation.

Global before Workspace.

Stability before Convenience.

---

# Summary

Reference defines every globally shared concept used throughout the Trademark Universe.

Reference provides stable definitions for geography, classifications, legal concepts, procedures, statuses, languages, currencies, offices and document types.

Reference Definitions belong to the Core.

Organizations consume them.

Organizations never redefine them.

Reference is the shared vocabulary upon which every other Core component depends.