# 220 Asset Specification

> **The Canonical Definition of Valuable Objects in the Trademark Universe**

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

- 210_Actor_Specification.md
- 230_Reference_Specification.md
- 240_Document_Specification.md
- 250_Business_Entity_Specification.md

---

# Purpose

The Trademark Universe exists to create, protect, manage and commercialize valuable assets.

Asset defines every object that possesses legal, commercial or operational value.

Asset answers one question.

> **What is valuable?**

---

# Asset Philosophy

Actors participate.

Assets create value.

Documents describe Assets.

Events change Assets.

Relationships connect Assets.

An Asset exists independently of the people managing it.

Its value may evolve.

Its Identity does not.

---

# Scope

Asset includes every persistent object with identifiable value.

Examples include:

- Trademark
- Brand
- Trademark Portfolio
- Domain Name
- Copyright
- Patent
- Design
- License
- Franchise Right
- Trade Secret

Future Asset types may be added.

The Asset model remains unchanged.

---

# Responsibilities

Asset owns:

- identity
- legal existence
- commercial value
- operational status
- ownership relationships
- lifecycle

Asset does not own:

- owner
- attorney
- workflow
- document
- runtime execution

Those are connected through Relationships.

---

# Asset Hierarchy

```
Asset

├── Trademark
├── Brand
├── Portfolio
├── Domain
├── Patent
├── Copyright
├── Design
├── License
└── Other Asset
```

Every Asset belongs to one primary Asset Type.

---

# Trademark

Represents one trademark right or application.

Typical attributes include:

- Mark
- Jurisdiction
- Classes
- Application Number
- Registration Number
- Status

Trademark is the primary Asset of MarkOrbit.

---

# Brand

Represents a commercial brand.

A Brand may contain multiple Assets.

Example

```
Brand

↓

Trademark

↓

Domain

↓

Copyright
```

Brand is a business concept.

Trademark is a legal right.

The two should not be confused.

---

# Portfolio

Represents a managed collection of Assets.

Examples include:

- Global Trademark Portfolio
- Chinese Trademark Portfolio
- Defensive Portfolio

Portfolio is itself an Asset.

It is not merely a list.

---

# Domain

Represents a registered Internet domain.

Examples:

- markorbit.com
- markorbit.cn

Domains may relate to Brands and Trademarks.

Relationships remain explicit.

---

# Patent

Represents patent rights.

Patent follows the same engineering model.

Different legal rules belong to Knowledge Products.

The Asset Definition remains consistent.

---

# Copyright

Represents copyright ownership.

Examples include:

- software
- artwork
- manuals
- logos

Copyright is an Asset.

---

# Design

Represents industrial design rights.

Design Assets may relate to Trademarks.

Relationships define the connection.

---

# License

Represents transferable usage rights.

License may reference:

- Trademark
- Patent
- Copyright

License is an Asset because it possesses operational and commercial value.

---

# Asset Contract

Every Asset Definition exposes:

- Identity
- Asset Type
- Required Attributes
- Lifecycle
- Validation Rules
- Supported Relationships

Asset behavior is defined through Contract.

---

# Asset Relationships

Assets commonly support:

- owned_by
- belongs_to
- licensed_to
- protected_in
- related_to
- managed_by

Relationship semantics belong to the Relationship Specification.

---

# Asset Lifecycle

Typical lifecycle:

```
Draft

↓

Created

↓

Active

↓

Transferred

↓

Suspended

↓

Expired

↓

Archived
```

Individual Asset types may define additional lifecycle states.

---

# Asset Value

Asset Value is not fixed.

Examples include:

- Legal Value
- Commercial Value
- Strategic Value
- Operational Value

Value changes over time.

Identity remains unchanged.

---

# Asset Validation

Validation may include:

- required attributes
- legal status
- ownership integrity
- lifecycle compatibility
- uniqueness rules

Validation Framework performs verification.

---

# Asset Registry

Every Asset Definition belongs to the Entity Registry.

Registry stores:

- Definition
- Version
- Contract
- Lifecycle

Runtime stores Asset Instances.

---

# Runtime

Runtime creates Asset Instances.

Example

```
Trademark Definition

↓

Trademark Instance

↓

TM-00000128

↓

Current State
```

Definitions remain permanent.

Instances evolve.

---

# Compatibility

Asset Definitions evolve through versioning.

Existing Asset Identities remain stable.

Breaking semantic changes require a new major version.

---

# Extension

Workspace may extend Assets with:

- internal valuation
- customer labels
- business categories
- custom metadata

Extensions must preserve Core semantics.

---

# Non Goals

Asset is not:

- a database record
- an ownership record
- a workflow
- a document
- a financial transaction

Those interact with Assets.

They are not Assets.

---

# Examples

Trademark

```
Asset

Trademark

Identity

TM-00000128
```

Brand

```
Asset

Brand

Contains

Trademark

Domain

Copyright
```

Portfolio

```
Asset

Portfolio

Contains

Trademark

Trademark

Trademark
```

---

# Design Principles

Assets before Documents.

Relationships before Embedding.

Identity before Ownership.

Brand before Collection.

Definition before Instance.

Value before Implementation.

---

# Summary

Asset defines every valuable object in the Trademark Universe.

Assets carry legal, commercial or operational value.

They exist independently of their owners and are connected through explicit Relationships.

Trademark is the primary Asset of MarkOrbit, while the Asset model is designed to support future expansion into patents, copyrights, domains and other intellectual property without changing the Engineering Kernel.