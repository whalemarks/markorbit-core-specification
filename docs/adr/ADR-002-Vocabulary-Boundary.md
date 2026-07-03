# ADR-002 — Vocabulary Boundary

Version: 1.0

Status: Accepted

Date: 2026-07

---

# Context

Professional vocabulary is defined by:

001_Professional_Vocabulary.md

However, multiple architectural layers intentionally use different terminology.

This ADR defines vocabulary boundaries.

---

# Decision

Vocabulary shall be interpreted according to architectural context.

The same word may have different meanings in different layers.

Automatic replacement is prohibited.

---

# Theory Layer

The following terms are valid:

- Entity
- Data
- Universe
- Ontology
- Model

These terms SHALL remain unchanged.

---

# Specification Layer

Canonical terms include:

- Workspace
- Brain
- Capability
- Guide
- Workflow
- Product
- Contract
- Runtime

---

# Runtime Layer

Runtime-specific terminology is permitted when required.

Examples include:

- Output
- Session
- Execution
- State

---

# Domain Terminology

Legal terminology shall not be normalized.

Examples:

- Filing Package
- Renewal Package
- POA Package
- Examination Report

---

# Conversation

Guide specifications intentionally use the word Conversation.

Conversation SHALL NOT be replaced automatically.

---

# Implementation

AI-assisted editorial tools shall preserve contextual vocabulary.

Vocabulary normalization must respect architectural boundaries.

---

# Consequences

Different architectural layers maintain precise terminology without forcing unnecessary consistency.