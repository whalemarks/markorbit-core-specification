# 250 Business Object Specification

> **The Canonical Definition of Operational Objects in the Trademark Universe**

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
- 240_Document_Specification.md
- 800_Workflow_Specification.md
- 900_Workspace_Specification.md

---

# Purpose

Reality contains Actors.

Reality contains Assets.

Reality contains Documents.

Business creates operational objects in order to organize professional work.

Business Object answers one question.

> **What is being managed?**

Business Objects organize work.

They do not redefine reality.

---

# Business Philosophy

Business Objects exist because organizations need coordination.

They are operational.

Not natural.

Not legal.

Not physical.

A Trademark exists without MarkOrbit.

A Filing Order does not.

Business Objects are created by organizations.

---

# Scope

Business Objects include every operational object created to organize business.

Examples include:

- Opportunity
- Lead
- Customer
- Matter
- Case
- Filing Request
- Quotation
- Order
- Invoice
- Payment
- Renewal Project
- Opposition Project
- Journey
- Task Group

Business Objects belong to operation.

They are not Reality Objects.

---

# Responsibilities

Business Object owns:

- business coordination
- operational status
- workflow participation
- organizational ownership
- commercial relationships

Business Object does not own:

- legal rights
- professional knowledge
- documents
- assets

Business Objects organize.

They do not replace reality.

---

# Business Categories

```
Business Object

├── CRM
├── Service
├── Commercial
├── Financial
├── Project
├── Journey
└── Collaboration
```

---

# CRM Objects

Examples include:

- Lead
- Opportunity
- Customer
- Contact

CRM Objects support customer development.

They are Workspace-oriented.

---

# Service Objects

Examples include:

- Filing Request
- Renewal Request
- Assignment Request
- Search Request

Service Objects initiate professional work.

They normally become Workflows.

---

# Commercial Objects

Examples include:

- Quotation
- Order
- Contract
- Subscription

Commercial Objects support commercial activities.

---

# Financial Objects

Examples include:

- Invoice
- Payment
- Refund
- Settlement

Financial Objects support financial processes.

---

# Project Objects

Examples include:

- Opposition Project
- Global Filing Project
- Brand Protection Project

Projects coordinate multiple Assets and Workflows.

---

# Journey Objects

Journey represents long-running customer progress.

Examples include:

- Trademark Journey
- Brand Journey
- International Expansion Journey

Journey is not Workflow.

Journey coordinates multiple Workflows.

---

# Collaboration Objects

Examples include:

- Shared Review
- External Assignment
- Partner Cooperation

Collaboration Objects organize cooperation between Workspaces.

---

# Business Contract

Every Business Object exposes:

- Identity
- Business Type
- Lifecycle
- Relationships
- Validation Rules
- Supported Workflows

---

# Relationships

Business Objects commonly reference:

- Actor
- Asset
- Document
- Workflow
- Workspace

Business Objects aggregate.

They do not own.

---

# Lifecycle

Typical lifecycle

```
Created

↓

Open

↓

In Progress

↓

Completed

↓

Closed

↓

Archived
```

Lifecycle varies by Business Type.

---

# Runtime

Business Objects execute through Runtime.

Workflow changes Business Object state.

Business Objects themselves do not execute.

---

# Validation

Validation may include:

- required participants
- required Assets
- required Documents
- commercial rules
- approval requirements

Validation Framework performs verification.

---

# Registry

Business Object Definitions belong to Registry.

Instances belong to Runtime.

Definitions remain stable.

Business data evolves continuously.

---

# Workspace

Business Objects are primarily owned by Workspace.

Different Workspaces may organize business differently.

Core Definitions remain unchanged.

Workspace configuration determines local behavior.

---

# Compatibility

Business Definitions evolve through versioning.

Commercial customization should occur through Extension.

Core semantics remain stable.

---

# Extension

Workspace may extend Business Objects with:

- custom stages
- internal policies
- approval chains
- pricing models
- reporting dimensions

Extensions should never change Core meaning.

---

# Non Goals

Business Object is not:

- Entity Definition
- Asset
- Document
- Workflow
- Capability

Business Objects coordinate these concepts.

They do not replace them.

---

# Examples

Opportunity

```
Business Object

Opportunity

↓

Customer

↓

Potential Trademark Filing
```

Order

```
Business Object

Order

↓

Workflow

Trademark Filing
```

Journey

```
Business Object

International Brand Journey

↓

Workflow

CN Filing

↓

US Filing

↓

EU Filing

↓

Renewal
```

---

# Design Principles

Reality before Business.

Business before Workflow.

Aggregation before Ownership.

Journey before Project.

Workspace before Customization.

Operation before Implementation.

---

# Summary

Business Object defines the operational objects used to organize professional work within the Trademark Universe.

Unlike Actors, Assets and Documents, Business Objects are created by organizations rather than reality.

They coordinate Workflows, Assets, Documents and Participants into manageable business operations.

Business Objects enable organizations to operate efficiently while preserving the integrity of the underlying reality.