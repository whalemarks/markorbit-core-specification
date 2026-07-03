# MarkOrbit Core

# Important

The documents in this directory are NOT part of the current Core Specification.

They represent architectural research only.

No implementation shall rely on these documents.

Only ADRs and Specifications define the official Core Architecture.

# Next Architecture Ideas

Status

Working Draft

---

# Purpose

This document records architectural ideas that may influence future versions of the MarkOrbit Core Specification.

Ideas listed here are proposals only.

None of them form part of the current Core Architecture.

Each idea must be validated before becoming an ADR.

---

# Idea Template

Every new idea should follow the structure below.

---

## Title

Status

Candidate | Under Validation | Accepted | Rejected | Parking Lot

Priority

High | Medium | Low

Origin

Architecture Review

Lite

MarkReg

MGSN

Production

Other

Architecture Area

Data

Brain

Business

Intelligence

Capability

Workflow

Workspace

Theory

Other

Validators

MarkOrbit Lite

MarkReg.com

MGSN

Other

Background

Proposal

Validation Plan

Current Status

Notes

---

# Active Ideas

---

## Idea 001

### Multi-Validator Architecture

Status

Accepted for Validation

Priority

High

Origin

Architecture Review

Architecture Area

Core Architecture

Validators

- MarkOrbit Lite
- MarkReg.com
- MGSN

### Background

The Core Architecture should not be validated by a single implementation.

Multiple independent implementations provide stronger architectural verification.

### Proposal

Adopt a validator-driven architecture process.

Future Core evolution shall be based on evidence collected from multiple ecosystem validators.

### Validation Plan

Validate through Lite, MarkReg and MGSN.

---

## Idea 002

### Validator-driven Architecture Evolution

Status

Candidate

Priority

High

Origin

Architecture Review

Architecture Area

Architecture Process

Validators

All ecosystem implementations.

### Background

Architecture currently evolves primarily through design discussion.

Future evolution should be driven by implementation validation.

### Proposal

Introduce validation as a mandatory stage before every ADR.

---

## Idea 003

### Business Metrics Framework

Status

Candidate

Priority

Medium

Origin

Mo Business Design

Architecture Area

Mo Business

Validators

- Lite
- Marketplace
- Reporting

### Background

Mo Business currently defines Business Evaluation.

Future versions may introduce a canonical Business Metrics framework.

Possible concepts include:

- Business Value
- Business Score
- Business Indicator
- Business Confidence
- Business Trend

---

## Idea 004

### Business Products Framework

Status

Candidate

Priority

Medium

Origin

Mo Business Design

Architecture Area

Mo Business

Validators

- Lite
- Workspace
- Reporting

### Background

Business Evaluation is expected to generate reusable Business Products.

Potential products include:

- Dashboard
- Report
- Summary
- Insight
- Ranking

---

## Idea 005

### Ecosystem-first Core

Status

Candidate

Priority

High

Origin

Architecture Review

Architecture Area

Core Philosophy

Validators

Entire MarkOrbit Ecosystem

### Background

The Core should evolve for the entire ecosystem rather than any single application.

Lite is one validator.

MarkReg is another.

MGSN is another.

Future applications will continue validating the architecture.

### Proposal

Position the Core as the architectural foundation of the entire MarkOrbit ecosystem.

---

## Idea 006

### Contract-based Architecture

Status

Parking Lot

Priority

Low

Origin

Architecture Review

Architecture Area

Architecture Theory

Validators

TBD

### Background

Future versions may replace simple layer relationships with explicit architectural contracts.

Further theoretical and practical validation is required.

---

## Idea 007

### Unified Layer Module Template

Status

Parking Lot

Priority

Low

Origin

550_Business Module

Architecture Area

Documentation

Validators

Future Core Refactoring

### Background

The documentation structure introduced for the 550_Business module may become the standard template for every Core layer in a future major release.

---

## Idea 008

### Brain Output Model

Status

Parking Lot

Priority

Low

Origin

Brain Review

Architecture Area

Mo Brain

Validators

Lite

MarkReg

### Background

The canonical output of Mo Brain remains intentionally undefined.

Further validation is required before standardisation.

---

## Idea 009

### Intelligence Output Model

Status

Parking Lot

Priority

Low

Origin

Intelligence Review

Architecture Area

Mo Intelligence

Validators

Lite

MarkReg

### Background

The canonical output of Mo Intelligence remains intentionally undefined.

Future validation may determine whether Recommendation, Decision, Strategy or Plan should become the architectural output.

---

# Notes

This document intentionally records ideas rather than decisions.

Ideas may be promoted, revised or rejected over time.

Only accepted ideas that have completed sufficient validation should proceed to an ADR.

---

**End of Core-Next-Ideas**