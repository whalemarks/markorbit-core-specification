# 350 Product Specification

> **The Canonical Information Product Model of the MarkOrbit Operating System**

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
- 340_Index_Specification.md

Related

- 400_Brain_Specification.md
- 500_Intelligence_Specification.md
- 600_Capability_Specification.md
- 700_Guide_Specification.md

---

# Purpose

Persistent information has little value if it cannot be consumed consistently.

The purpose of Product is to publish trusted information as reusable, versioned and contract-driven products.

Product answers one question.

> **What information can the rest of the system consume?**

---

# Product Philosophy

Products are not storage.

Products are not APIs.

Products are published information.

Persistence preserves information.

Products publish information.

Brain consumes Products.

Intelligence reasons from Products.

Guide explains Products.

Products become the public language of MarkOrbit.

---

# Scope

Products include every published information object.

Examples include:

- Trademark Product
- Brand Product
- Portfolio Product
- Opportunity Product
- Deadline Product
- Statistics Product
- Knowledge Dataset
- AI Dataset
- Workspace Dataset

Products may be consumed by:

- Brain
- Intelligence
- Capability
- Workflow
- Guide
- API
- Marketplace
- Workspace

---

# Responsibilities

Product owns:

- published structure
- information contract
- version
- discoverability
- consumption interface

Product does not own:

- raw storage
- normalization
- parsing
- runtime execution

---

# Product Architecture

Every Product follows the same pipeline.

```text
Source

↓

Record

↓

Store

↓

Index

↓

Product
```

Products are the public boundary of the Persistence World.

---

# Product Characteristics

Every Product should satisfy the following principles.

## Published

Products are intended for consumption.

Stores are not.

---

## Versioned

Every Product owns an independent version.

Consumers should explicitly reference Product versions.

---

## Stable

Products evolve conservatively.

Internal storage may change.

Product Contracts should remain stable.

---

## Explainable

Every Product should preserve lineage.

Consumers should be able to trace Products back to their Sources.

---

## Reusable

Products should support multiple consumers.

One Product.

Many consumers.

---

# Product Categories

Products may be organized by purpose.

```text
Entity Product

Reference Product

Business Product

Analytics Product

Knowledge Product

AI Product

Workspace Product
```

---

# Entity Product

Publishes Entity information.

Examples include:

- Trademark Product
- Brand Product
- Portfolio Product

---

# Reference Product

Publishes globally shared references.

Examples include:

- Country Dataset
- Nice Classification
- Office Directory

---

# Business Product

Publishes operational information.

Examples include:

- Renewal Opportunities
- Outstanding Orders
- Customer Dashboard

---

# Analytics Product

Publishes aggregated information.

Examples include:

- Filing Statistics
- Registration Trends
- Portfolio Reports

Analytics Products summarize.

They do not preserve raw facts.

---

# Knowledge Product

Publishes structured professional knowledge.

Examples include:

- Filing Guidelines
- Office Practices
- Examination Rules

Knowledge Products belong to Brain.

Persistence only publishes them.

---

# AI Product

Publishes AI-ready information.

Examples include:

- Embedding Dataset
- RAG Dataset
- Recommendation Dataset

AI Products remain traceable to Source.

---

# Workspace Product

Publishes organization-specific information.

Examples include:

- Customer Overview
- Internal KPI
- Pending Tasks

Workspace Products should preserve Core Contracts.

---

# Product Contract

Every Product exposes:

- Identity
- Version
- Inputs
- Outputs
- Lineage
- Compatibility
- Validation Status

Consumers depend on Product Contracts.

---

# Product Lineage

Every Product preserves lineage.

```text
Product

↓

Index

↓

Store

↓

Record

↓

Source
```

Consumers should always be able to explain where Product information originated.

---

# Product Validation

Validation includes:

- completeness
- lineage integrity
- contract compatibility
- schema consistency
- publication readiness

Only validated Products should be published.

---

# Product Registry

Registry stores:

- Product Definition
- Contract
- Version
- Lifecycle

Runtime publishes Product Instances.

---

# Runtime

Runtime generates Products.

Products are immutable snapshots.

New publication creates a new Product Version.

---

# Relationship to Brain

Brain consumes Products.

Brain should not depend directly on Stores.

Products are the default knowledge input.

---

# Relationship to Intelligence

Intelligence reasons from Products.

Recommendations should reference Product versions whenever possible.

---

# Relationship to Capability

Capabilities consume Products.

Capabilities should avoid implementation-specific persistence.

Products provide stable information interfaces.

---

# Relationship to Guide

Guide explains Products.

Guide never interprets raw storage directly unless explicitly required.

---

# Relationship to API

APIs publish Products.

APIs should avoid exposing Store structures.

Products become the stable external interface.

---

# Relationship to Marketplace

Marketplace consumes Products.

Examples include:

- Trademark Listings

- Brand Opportunities

- Service Packages

Marketplace should remain independent from storage implementation.

---

# Compatibility

Products evolve through versioning.

Breaking changes require:

- new Product Version
- migration strategy
- updated Product Contract

---

# Extension

Future Product types may include:

- Streaming Product
- Real-time Product
- Graph Product
- AI Reasoning Product
- Compliance Product

Extensions should preserve Product Contracts.

---

# Non Goals

Product is not:

- Database View
- SQL Query
- REST Response
- JSON Schema
- Cache

These may implement Products.

They are not Products.

---

# Examples

Trademark Product

```text
Trademark

↓

Trademark Product

↓

Brain
```

Deadline Product

```text
Renewal Records

↓

Deadline Product

↓

Reminder Capability
```

AI Dataset

```text
Trademark Records

↓

AI Product

↓

RAG
```

---

# Design Principles

Store before Product.

Products before Brain.

Contracts before Consumers.

Publication before Optimization.

Lineage before Performance.

Stability before Convenience.

---

# Summary

Product defines the published information units of the MarkOrbit Operating System.

Products transform persistent information into stable, versioned and reusable information interfaces.

Every higher layer—including Brain, Intelligence, Capability, Guide, Workspace, Marketplace and APIs—should consume Products rather than directly accessing persistence.

Products form the boundary between the Persistence World and the Knowledge World.