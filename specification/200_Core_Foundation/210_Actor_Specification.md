# 210 Actor Specification

> **The Canonical Definition of Active Participants in the Trademark Universe**

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
- 250_Business_Entity_Specification.md

---

# Purpose

The Trademark Universe consists of objects.

Some objects act.

Some objects are acted upon.

Actor defines every object capable of participating in professional activities.

Actor answers one question.

> **Who performs or participates?**

---

# Actor Philosophy

Actors perform actions.

Assets receive actions.

Documents record actions.

Events preserve actions.

An Actor may own Assets.

An Actor may create Documents.

An Actor may initiate Workflows.

Actor represents participation.

---

# Scope

Actor includes every person, organization or system capable of participating in professional activities.

Examples include:

- Individual
- Company
- Government Office
- Trademark Office
- Law Firm
- Attorney
- Trademark Agent
- Customer
- Partner
- AI Agent
- System Account

Actor does not include:

- Trademark
- Brand
- Goods
- Documents

Those belong to other Entity categories.

---

# Responsibilities

Actor owns:

- identity
- participation
- roles
- authority
- relationships

Actor does not own:

- trademarks
- documents
- workflows
- business history

Actors participate.

They do not become the activities themselves.

---

# Actor Hierarchy

```
Actor

├── Person
├── Organization
├── Government
├── Office
├── Team
├── AI Agent
└── System
```

Every Actor belongs to exactly one primary type.

---

# Person

Represents a natural person.

Examples:

- Applicant
- Attorney
- Examiner
- Customer
- Sales Representative

Person may participate in multiple Roles.

Identity remains unchanged.

---

# Organization

Represents a legal organization.

Examples:

- Company
- Law Firm
- Agency
- Enterprise

Organizations own legal responsibilities.

Organizations may contain Persons.

---

# Government

Represents government authorities.

Examples:

- National IP Office
- Customs Authority
- Court

Government Actors are authoritative.

---

# Office

Represents operational institutions.

Examples:

- USPTO
- CNIPA
- EUIPO
- WIPO

Office participates in trademark procedures.

Office is a specialized Organization.

---

# Team

Represents internal collaboration units.

Examples:

- Sales Team
- Legal Team
- Finance Team

Teams exist within Organizations.

---

# AI Agent

Represents autonomous software participants.

Examples:

- Guide
- Validation Agent
- Recommendation Agent
- Import Agent

AI Agents may initiate Runtime execution.

They do not own professional responsibility.

---

# System

Represents technical participants.

Examples:

- Scheduler
- API Gateway
- Import Service
- Notification Service

System Actors support operation.

---

# Roles

Role is not Actor.

Actor performs one or more Roles.

Example

```
Person

↓

Attorney

↓

Reviewer

↓

Partner
```

Roles are runtime assignments.

Actor Identity remains constant.

---

# Authority

Actor may possess authority.

Examples include:

- approve
- sign
- submit
- review
- administer

Authority should be validated through Contracts and Workspace configuration.

Authority is not identity.

---

# Ownership

Actors may own Assets.

Examples:

```
Company

owns

Trademark
```

```
Customer

owns

Portfolio
```

Ownership is represented through Relationships.

Actor does not contain Assets.

---

# Representation

Actors may represent other Actors.

Examples:

```
Attorney

represents

Applicant
```

```
Agency

represents

Brand Owner
```

Representation is a Relationship.

It should always be explicit.

---

# Collaboration

Actors collaborate.

Examples include:

- Customer ↔ Attorney
- Agency ↔ Foreign Associate
- Examiner ↔ Applicant

Collaboration should be represented through Relationships.

---

# Actor Contract

Every Actor Definition exposes:

- Identity
- Actor Type
- Required Attributes
- Supported Relationships
- Lifecycle
- Validation Rules

Contracts remain stable.

---

# Actor Lifecycle

Typical lifecycle:

```
Created

↓

Verified

↓

Active

↓

Inactive

↓

Archived
```

Actor Identity never changes.

---

# Actor Validation

Validation may include:

- legal existence
- identity verification
- organization status
- authority validation
- duplicate detection

Validation rules vary by Actor Type.

---

# Actor Registry

All Actor Definitions belong to the Entity Registry.

Registry stores:

- Definition
- Contract
- Lifecycle
- Version

Registry does not store runtime participants.

---

# Runtime

Runtime creates Actor Instances.

Example

```
Person Definition

↓

Attorney Instance

↓

Workflow Participant
```

Instances execute.

Definitions remain permanent.

---

# Compatibility

Actor Definitions evolve conservatively.

Existing Relationships should remain valid.

Breaking semantic changes require a new major version.

---

# Extension

Workspace may extend Actors with:

- internal employee ID
- department
- regional office
- performance metrics

Extensions must not change Actor semantics.

---

# Non Goals

Actor is not:

- User Account
- Login Identity
- Permission Model
- Organization Chart

These consume Actor Definitions.

They do not define Actors.

---

# Examples

Company

```
Definition

Organization

Identity

ACT-ORG

Relationships

owns Trademark

appoints Attorney
```

Attorney

```
Definition

Person

Role

Attorney

Relationships

represents Applicant

handles Case
```

Trademark Office

```
Definition

Office

Examples

USPTO

CNIPA

EUIPO
```

---

# Design Principles

Actor before Role.

Identity before Authority.

Representation before Ownership.

Relationships before Embedding.

Definition before Runtime.

Semantics before Implementation.

---

# Summary

Actor defines every active participant in the Trademark Universe.

Actors include people, organizations, offices, AI agents and systems.

Actors participate in professional activities through explicit Roles, Authorities and Relationships.

They provide the human and organizational foundation for all business operations within MarkOrbit.