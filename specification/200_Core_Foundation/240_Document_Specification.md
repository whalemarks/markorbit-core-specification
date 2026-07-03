# 240 Document Specification

> **The Canonical Evidence Model of the Trademark Universe**

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
- 220_Asset_Specification.md
- 230_Reference_Specification.md
- 300_Data_Specification.md
- 400_Brain_Specification.md
- 800_Workflow_Specification.md

---

# Purpose

Professional work requires evidence.

Evidence must be permanent.

Evidence must be traceable.

The purpose of Document is to represent every authoritative document used throughout the Trademark Universe.

Document answers one question.

> **What proves this?**

---

# Document Philosophy

A Document is not a file.

A file is a storage artifact.

A Document is a business object.

One Document may have:

- many files
- many versions
- many translations
- many signatures

The Document remains one object.

Evidence is more important than storage.

---

# Scope

Document includes every persistent evidence object.

Examples include:

- Trademark Application
- Registration Certificate
- Office Action
- Office Action Response
- Assignment Agreement
- License Agreement
- Power of Attorney
- Renewal Certificate
- Court Decision
- Opposition Notice
- Cancellation Decision
- Invoice
- Receipt

Documents belong to the business domain.

Storage belongs to infrastructure.

---

# Responsibilities

Document owns:

- evidence
- legal meaning
- document type
- issuing authority
- lifecycle
- relationships

Document does not own:

- file storage
- OCR
- thumbnails
- binary data

Those belong to implementation.

---

# Document Model

```
Document Definition

↓

Document Instance

↓

Document Version

↓

File

↓

Evidence
```

Document is the business object.

Files are representations.

---

# Document Characteristics

Every Document should satisfy the following principles.

## Permanent

Documents should remain referenceable.

Even when archived.

---

## Traceable

Every Document should identify:

- issuer
- subject
- creation date
- effective date
- source

---

## Versioned

Documents evolve.

New versions should not overwrite previous versions.

---

## Authentic

Authenticity should be preserved.

Examples include:

- digital signature
- issuing office
- checksum
- notarization

Authenticity is evidence.

---

## Independent

Documents should not be embedded inside Assets.

Documents reference Assets.

Assets reference Documents.

---

# Document Categories

Document Definitions include:

```
Application

Certificate

Official Decision

Legal Agreement

Evidence

Financial Document

Communication

Internal Document

Other
```

---

# Application

Examples

- Trademark Application
- Madrid Application

Applications initiate procedures.

---

# Certificate

Examples

- Registration Certificate
- Renewal Certificate

Certificates prove legal status.

---

# Official Decision

Examples

- Office Action
- Refusal
- Opposition Decision
- Appeal Decision

Official Decisions originate from authoritative offices.

---

# Legal Agreement

Examples

- Assignment
- License
- Coexistence Agreement
- POA

Legal Agreements define legal relationships.

---

# Evidence

Examples

- Product Photograph
- Packaging
- Website Screenshot
- Invoice
- Advertisement

Evidence supports legal arguments.

Evidence does not determine legal conclusions.

---

# Financial Document

Examples

- Invoice
- Payment Receipt
- Official Fee Receipt

Financial Documents support commercial processes.

---

# Communication

Examples

- Official Letter
- Client Notice
- Attorney Opinion

Communications preserve professional interaction.

---

# Internal Document

Examples

- Internal Review
- Meeting Minutes
- Approval Record

Internal Documents belong to Workspace.

Core Document semantics remain unchanged.

---

# Document Contract

Every Document Definition exposes:

- Identity
- Document Type
- Required Attributes
- Supported Relationships
- Lifecycle
- Validation Rules

---

# Document Relationships

Common Relationships include:

- issued_by
- belongs_to
- proves
- references
- attached_to
- generated_from

Relationship semantics remain independent.

---

# Document Lifecycle

Typical lifecycle

```
Created

↓

Received

↓

Verified

↓

Effective

↓

Superseded

↓

Archived
```

Verification should not modify historical versions.

---

# Document Version

Document Versions preserve evolution.

```
Version 1

↓

Version 2

↓

Version 3
```

Every Version remains referenceable.

---

# Document Registry

Registry stores:

- Definition
- Contract
- Version
- Lifecycle

Registry never stores document files.

---

# Runtime

Runtime creates Document Instances.

Runtime may:

- upload files
- validate signatures
- perform OCR
- extract metadata

These are runtime behaviors.

They do not redefine the Document.

---

# Validation

Validation may verify:

- completeness
- authenticity
- required signatures
- issuing authority
- supported format
- expiration

Validation Framework performs verification.

---

# Brain

Brain consumes Documents.

Documents become knowledge sources.

Brain never changes Documents.

Documents remain evidence.

---

# Workflow

Workflow consumes Documents.

Examples

```
POA Received

↓

Validation

↓

Application Submitted
```

Workflow progresses through verified Documents.

---

# Workspace

Workspace may attach:

- internal notes
- translations
- labels
- folders

Workspace metadata never changes Document meaning.

---

# Compatibility

Document Definitions evolve through versioning.

Historical Documents remain valid.

Breaking changes require migration.

---

# Extension

Workspace may extend Documents with:

- local categories
- retention policy
- internal approval
- AI summaries

Extensions preserve Core semantics.

---

# Non Goals

Document is not:

- PDF
- Word
- Image
- Attachment
- Blob Storage
- File System

Those implement Document.

They are not the Document.

---

# Examples

Registration Certificate

```
Document

Registration Certificate

↓

Version

1

↓

Files

certificate.pdf

certificate.jpg
```

Power of Attorney

```
Document

POA

↓

Signed

↓

Verified

↓

Workflow Continues
```

Office Action

```
Document

Office Action

↓

Brain Source

↓

Response Workflow
```

---

# Design Principles

Evidence before Files.

Document before Storage.

Reference before Embedding.

Authenticity before Convenience.

Version before Overwrite.

Meaning before Format.

---

# Summary

Document defines every authoritative evidence object within the Trademark Universe.

Documents provide legal, commercial and operational proof.

They are independent business objects rather than stored files.

Files represent Documents.

Documents support Brain, Workflow, Validation and every professional activity built upon evidence.

Evidence is permanent.

Storage is replaceable.