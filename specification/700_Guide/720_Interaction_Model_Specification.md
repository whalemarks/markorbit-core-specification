# 720 Interaction Model Specification

> **The Canonical Professional Interaction Methodology of the MarkOrbit Operating System**

---

Version

2.0

Status

Draft

Depends

- 640_Capability_Product_Specification.md
- 700_Guide_Specification.md
- 710_Guide_Object_Specification.md

Related

- 730_Experience_Network.md
- 740_Guide_Product.md
- 800_Workflow_Specification.md

---

# Purpose

Professional interaction should be intentional.

It should guide users from goals to outcomes through structured collaboration.

The purpose of Interaction Model is to organize Guide Objects into reusable professional interaction methodologies.

Interaction Model answers one question.

> **How should professional interaction happen?**

---

# Interaction Philosophy

Capability delivers services.

Guide delivers experiences.

Interaction Models define methodology.

They do not define interfaces.

Interaction is independent of channels.

---

# Scope

Interaction Models describe reusable interaction methodologies.

Examples include:

- Trademark Filing Interaction

- Country Recommendation Interaction

- Goods Selection Interaction

- Portfolio Review Interaction

- Renewal Interaction

- Office Action Interaction

Interaction Models remain reusable across every channel.

---

# Responsibilities

Interaction Model owns:

- interaction methodology

- interaction stages

- interaction transitions

- user feedback handling

- completion criteria

Interaction Model does not own:

- UI

- workflow

- execution

- persistence

---

# Architecture

Every Interaction Model follows one structure.

```text
Guide Objects

↓

Interaction Stages

↓

Interaction Model

↓

Experience Network

↓

Guide Product
```

---

# Characteristics

Every Interaction Model should satisfy:

## Goal-oriented

Every interaction begins with a professional objective.

---

## Explainable

Users should always understand why they are being asked something.

---

## Adaptive

Interaction adapts to context.

---

## Progressive

Information should be revealed progressively.

---

## Recoverable

Interrupted interactions should resume naturally.

---

## Versioned

Interaction methodologies evolve independently.

---

# Interaction Lifecycle

Typical interaction stages include:

```text
Understand

↓

Discover

↓

Recommend

↓

Confirm

↓

Execute

↓

Explain

↓

Follow-up
```

Different interactions may omit or extend stages.

---

# Categories

Interaction Models may include:

Interaction Assistant

Review Model

Consultation Model

Recommendation Model

Configuration Model

Education Model

Monitoring Model

Service Model

---

# Interaction Assistant

Examples

- Trademark Filing Assistant

- Renewal Assistant

---

# Review Model

Examples

- Similarity Review

- Portfolio Review

---

# Consultation Model

Examples

- International Filing Consultation

- Brand Protection Consultation

---

# Recommendation Model

Examples

- Country Recommendation

- Goods Recommendation

---

# Configuration Model

Examples

- Workspace Setup

- Notification Preferences

---

# Education Model

Examples

- Filing Tutorial

- Nice Classification Guide

---

# Monitoring Model

Examples

- Monitoring Center

- Deadline Center

---

# Service Model

Examples

- Online Filing

- Online Renewal

- Online Assignment

---

# Interaction Stages

Each stage should define:

- objective

- expected inputs

- expected outputs

- transition conditions

- completion conditions

Stages remain implementation-independent.

---

# Inputs

Typical inputs include:

- Guide Objects

- Capability Products

- Workspace Policies

- User Context

- Runtime State

---

# Outputs

Typical outputs include:

- Guide Product

- Interaction Events

- User Decisions

- Navigation Requests

- Feedback

---

# Feedback

Every Interaction Model should define feedback loops.

Typical feedback includes:

- clarification

- correction

- approval

- cancellation

- satisfaction

Feedback improves future interactions.

Feedback never changes professional truth.

---

# Validation

Validation should verify:

- interaction completeness

- accessibility

- usability

- consistency

- recoverability

---

# Runtime

Runtime creates Interaction Sessions.

Interaction Models remain immutable.

Session state belongs to Runtime.

---

# Relationship to Experience Network

Interaction Models define methodology.

Experience Networks connect interactions.

The two remain independent.

---

# Relationship to Workflow

Workflow coordinates execution.

Interaction Model coordinates experience.

Workflow answers:

"When should work happen?"

Interaction answers:

"How should users experience it?"

---

# Relationship to Workspace

Workspace customizes:

- branding

- localization

- permissions

- defaults

Core interaction methodology remains reusable.

---

# Compatibility

Interaction Models evolve conservatively.

Interaction contracts remain stable.

Major methodology changes require new versions.

---

# Extension

Future Interaction Models may include:

- Voice-first Interaction

- AR Interaction

- Autonomous Agent Interaction

- Multi-user Collaboration

- Human-AI Co-pilot Interaction

Extensions should preserve interaction principles.

---

# Non Goals

Interaction Model is not:

- Prompt

- Conversation

- Screen Flow

- Wizard

- React Component

These may implement Interaction Models.

They are not Interaction Models.

---

# Examples

Trademark Filing

```text
Understand

↓

Recommend Country

↓

Recommend Classes

↓

Generate Filing

↓

Confirm

↓

Submit

↓

Explain Next Steps
```

Portfolio Review

```text
Discover

↓

Analyze

↓

Recommend

↓

Visualize

↓

Review

↓

Action Plan
```

---

# Design Principles

Goals before Questions.

Understanding before Recommendation.

Recommendation before Execution.

Explanation before Automation.

Interaction before Interface.

Experience before Technology.

---

# Summary

Interaction Model defines the reusable methodologies through which professional services are experienced within MarkOrbit.

It organizes Guide Objects into structured interaction patterns that are adaptive, explainable and channel-independent.

Interaction Models ensure that every professional experience remains consistent across web, mobile, chat, APIs and future interaction channels while preserving the integrity of professional knowledge and execution.