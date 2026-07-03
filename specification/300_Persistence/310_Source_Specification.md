# 310 Source Specification

> **The Canonical Source of Truth Model of the MarkOrbit Operating System**

---

Version

**2.0**

Status

**Draft**

Depends

- 300_Persistence_Specification.md

Related

- 320_Record_Specification.md
- 330_Store_Specification.md
- 340_Index_Specification.md
- 350_Product_Specification.md

---

# Purpose

Every piece of information originates somewhere.

Professional systems should preserve where information comes from.

The purpose of Source is to define every authoritative origin of information used within MarkOrbit.

Source answers one question.

> **Where does this information originate?**

Without Source, information cannot be trusted.

---

# Source Philosophy

Source is the origin.

Source is not the Record.

Source is not the Product.

Source is evidence.

Everything else derives from Source.

Whenever possible,

Source should remain immutable.

---

# Scope

Source represents every original provider of information.

Examples include:

- National Trademark Offices
- WIPO
- Government APIs
- Official Publications
- Uploaded Files
- Internal Documents
- User Submissions
- Partner Systems
- Third-party APIs

Every persisted Record should reference at least one Source.

---

# Responsibilities

Source owns:

- origin
- authenticity
- acquisition metadata
- lineage root
- trust level

Source does not own:

- normalization
- interpretation
- indexing
- recommendation

Source provides facts.

Other layers create value.

---

# Source Model

Every Source consists of:

```text
Source Definition

↓

Source Instance

↓

Acquisition

↓

Verification

↓

Persistence
```

Definitions describe the Source.

Instances represent one acquired dataset or document.

---

# Source Categories

Sources belong to one category.

```
Official Source

Government Source

Partner Source

Customer Source

Internal Source

Generated Source

External Source
```

---

# Official Source

Produced by an official authority.

Examples include:

- CNIPA
- USPTO
- EUIPO
- WIPO
- JPO

Official Sources usually have the highest trust level.

---

# Government Source

Produced by governmental agencies.

Examples include:

- Customs
- Courts
- Corporate Registries
- Administrative Authorities

Government Sources may supplement trademark information.

---

# Partner Source

Provided by trusted partners.

Examples include:

- Foreign Associates
- Law Firms
- Commercial Partners

Partner Sources require provenance tracking.

---

# Customer Source

Submitted by customers.

Examples include:

- POA
- Business License
- Logo
- Use Evidence
- Product Images

Customer Sources require validation.

---

# Internal Source

Generated inside MarkOrbit.

Examples include:

- Internal Reviews
- Generated Reports
- Knowledge Articles
- Workflow Outputs

Internal Sources remain traceable.

---

# Generated Source

Created automatically.

Examples include:

- OCR Results
- AI Summaries
- AI Classifications
- Machine Translation

Generated Sources must reference their parent Source.

Generated Sources are never considered original evidence.

---

# External Source

Provided by third-party systems.

Examples include:

- CRM
- ERP
- Payment Gateway
- News Feed

External Sources require synchronization policies.

---

# Source Identity

Every Source owns a permanent Identity.

Example

```text
SRC-00000128
```

Source Identity remains stable.

Individual acquisitions receive separate Runtime IDs.

---

# Source Metadata

Every Source should record:

- identity
- provider
- acquisition time
- acquisition method
- jurisdiction
- language
- format
- version
- checksum (optional)
- trust level

Metadata supports traceability.

---

# Trust Levels

Every Source declares a Trust Level.

Suggested levels:

```text
Authoritative

Verified

Trusted

Unverified

Experimental
```

Trust describes confidence in the origin.

It does not guarantee correctness.

---

# Source Lineage

Every derived object should preserve lineage.

```text
Source

↓

Record

↓

Store

↓

Product

↓

Brain

↓

Intelligence
```

Lineage should never be broken.

---

# Source Version

Some Sources evolve.

Examples:

- Monthly trademark data
- Daily publications
- API snapshots

Each acquisition becomes a new Source Instance.

The Source Definition remains unchanged.

---

# Source Verification

Verification may include:

- checksum
- digital signature
- source URL
- issuing authority
- acquisition completeness
- schema validation

Verification strengthens trust.

It does not replace Source.

---

# Source Registry

Registry stores Source Definitions.

Registry records:

- Identity
- Category
- Contract
- Provider
- Lifecycle

Runtime stores Source Instances.

---

# Runtime

Runtime performs:

- acquisition
- download
- import
- synchronization
- verification

Runtime never changes Source Definitions.

---

# Relationship to Records

Source produces Records.

Records normalize Source.

Records never replace Source.

The original Source should remain recoverable whenever possible.

---

# Relationship to Brain

Brain consumes Products.

Brain may inspect original Sources for verification.

Knowledge should remain explainable through Source lineage.

---

# Relationship to Intelligence

Intelligence reasons using trusted Products.

Whenever necessary,

Intelligence should be able to trace recommendations back to Source.

Explainability depends on Source.

---

# Compatibility

Source Definitions evolve conservatively.

Historical acquisitions remain referenceable.

Source lineage must survive migration.

---

# Extension

Future Source types may include:

- Blockchain Evidence
- IoT Devices
- Digital Identity Providers
- AI-native Sources
- Federated Knowledge Sources

All extensions should preserve traceability.

---

# Non Goals

Source is not:

- Record
- Store
- Product
- Knowledge
- Recommendation

Source defines origin.

Nothing more.

---

# Examples

Official Source

```text
Source

CNIPA Monthly Data

Trust Level

Authoritative
```

Customer Source

```text
Source

Trademark Use Evidence

Origin

Customer Upload

Trust Level

Verified
```

Generated Source

```text
OCR Result

Parent Source

Registration Certificate

Trust Level

Generated
```

---

# Design Principles

Origin before Interpretation.

Source before Record.

Lineage before Optimization.

Evidence before Knowledge.

Trust before Intelligence.

Authenticity before Convenience.

---

# Summary

Source defines every authoritative origin of information within MarkOrbit.

Every Record, Product, Brain Object and Intelligence Product should ultimately trace back to one or more Sources.

Source establishes the trust foundation of the Persistence World.

Without trusted Sources, there can be no trusted knowledge or trusted intelligence.