# 710 Guide Object Specification

> **The Canonical Building Block of Professional Interaction**

---

Version

2.0

Status

Draft

Depends

- 170_Contract_Model.md
- 640_Capability_Product_Specification.md
- 700_Guide_Specification.md

Related

- 720_Interaction_Model_Specification.md
- 730_Experience_Network_Specification.md
- 740_Guide_Product_Specification.md
- 900_Workspace_Specification.md

---

# Purpose

Professional experience is composed of reusable interactions.

The purpose of Guide Object is to define the smallest reusable unit of professional interaction.

Guide Object answers one question.

> **What is one professional interaction?**

---

# Guide Philosophy

Capability delivers professional services.

Guide delivers professional interactions.

Every Guide Object represents one complete interaction.

Not one page.

Not one widget.

Not one prompt.

---

# Scope

Guide Objects include reusable professional interactions.

Examples include:

- Trademark Filing Assistant

- Country Recommendation Conversation

- Goods Selection Assistant

- Similarity Review Session

- Renewal Reminder Experience

- Portfolio Review Session

- Office Action Response Assistant

- Customer Onboarding

Guide Objects are interaction Definitions.

Runtime creates interaction Sessions.

---

# Responsibilities

Guide Object owns:

- interaction objective

- interaction contract

- interaction flow

- presentation strategy

- feedback strategy

Guide Object does not own:

- execution

- reasoning

- workflow

- storage

---

# Architecture

Every Guide Object follows one structure.

```text
Capability Product

↓

Interaction Context

↓

Professional Interaction

↓

User Feedback

↓

Guide Product
```

Guide Object defines interaction.

Runtime renders interaction.

---

# Characteristics

Every Guide Object should satisfy:

## Goal-oriented

Every interaction should accomplish one professional objective.

---

## Human-centered

Interactions should reduce cognitive effort.

---

## Explainable

Professional services should remain understandable.

---

## Adaptive

Interactions adapt to user context.

---

## Reusable

Guide Objects should support multiple channels.

---

## Versioned

Interaction evolves independently.

---

# Categories

Guide Objects may include:

Conversation

Assistant

Review

Navigation

Explanation

Configuration

Visualization

Confirmation

Education

---

# Conversation

Examples

- Country Recommendation

- Goods Selection

- Filing Consultation

---

# Assistant

Examples

- Trademark Filing Assistant

- Renewal Assistant

- Portfolio Assistant

---

# Review

Examples

- Similarity Review

- Portfolio Review

- Cost Review

---

# Navigation

Examples

- Filing Journey

- Renewal Journey

- Registration Timeline

---

# Explanation

Examples

- Office Action Explanation

- Risk Explanation

- Cost Explanation

---

# Configuration

Examples

- Workspace Setup

- Filing Preferences

- Notification Preferences

---

# Visualization

Examples

- Portfolio Dashboard

- Timeline Viewer

- Network Viewer

---

# Confirmation

Examples

- Filing Confirmation

- Payment Confirmation

- Submission Confirmation

---

# Education

Examples

- Filing Guide

- Nice Classification Tutorial

- Madrid Tutorial

---

# Structure

Every Guide Object should define:

| Field | Required |
|---------|----------|
| Guide ID | ✓ |
| Name | ✓ |
| Category | ✓ |
| Objective | ✓ |
| Inputs | ✓ |
| Outputs | ✓ |
| Interaction Strategy | ✓ |
| Feedback Strategy | ✓ |
| Version | ✓ |

Optional:

- Personalization Rules

- Accessibility Rules

- Localization

---

# Inputs

Typical inputs include:

- Capability Products

- Workspace Configuration

- User Context

- Runtime State

Guide Objects should never consume internal implementation directly.

---

# Outputs

Typical outputs include:

- Guide Product

- User Feedback

- Interaction Events

- Navigation Requests

---

# Feedback

Guide Objects collect feedback.

Examples include:

- confirmation

- corrections

- satisfaction

- abandonment

- user intent

Feedback improves future interactions.

Feedback does not change professional truth.

---

# Validation

Validation should verify:

- interaction completeness

- usability

- accessibility

- consistency

- contract compliance

---

# Runtime

Runtime creates Guide Object Sessions.

Definitions remain immutable.

Sessions remain ephemeral.

---

# Relationship to Capability

Guide Objects consume Capability Products.

Guide Objects never execute professional work.

---

# Relationship to Workflow

Workflow invokes Guide Objects.

Guide Objects remain interaction Definitions.

---

# Relationship to Workspace

Workspace customizes Guide Objects.

Examples include:

- branding

- language

- permissions

- regional experience

Core interaction remains reusable.

---

# Compatibility

Guide Objects evolve conservatively.

Interaction Contracts remain stable.

Breaking interaction semantics require major versions.

---

# Extension

Future Guide Objects may include:

- Voice Assistant

- AR Assistant

- VR Workspace

- Autonomous Guide

- Multi-agent Guide

Extensions should preserve interaction principles.

---

# Non Goals

Guide Object is not:

- Page

- React Component

- Prompt

- Chat Window

- API

These may implement Guide Objects.

They are not Guide Objects.

---

# Examples

Trademark Filing Assistant

```text
Capability Product

↓

Guide Object

↓

Conversation

↓

Guide Product
```

Similarity Review

```text
Capability Product

↓

Review Session

↓

Professional Explanation
```

Portfolio Review

```text
Capability Product

↓

Visualization

↓

Decision Support
```

---

# Design Principles

Service before Interaction.

Interaction before Interface.

Goal before Navigation.

Understanding before Decoration.

Reuse before Customization.

Trust before Convenience.

---

# Summary

Guide Object is the smallest reusable unit of professional interaction in MarkOrbit.

Each Guide Object transforms professional service outputs into structured interactions that are understandable, adaptive and reusable across different channels.

Guide Objects provide the interaction building blocks from which professional user experiences are composed.