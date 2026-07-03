# ADR-001 — Repository Editorial Policy

Version: 1.0

Status: Accepted

Date: 2026-07

---

# Context

MarkOrbit Core Specification has completed its architectural design.

From this point forward, repository changes should prioritize publication quality and consistency rather than architectural redesign.

This ADR defines the editorial policy governing all repository maintenance activities.

---

# Decision

Editorial work SHALL improve repository quality without changing architectural intent.

Editorial work includes:

- Markdown normalization
- Heading consistency
- Metadata completion
- Cross-reference correction
- Navigation improvement
- Repository organization
- Broken link repair
- README improvements

Editorial work SHALL NOT:

- Redesign architecture
- Introduce new concepts
- Rename architectural objects
- Change responsibilities
- Modify architectural philosophy
- Rewrite specifications for style only

---

# Editorial Priority

Changes shall follow this order:

1. Broken repository structure
2. Broken references
3. Missing metadata
4. Navigation
5. Markdown consistency
6. Readability

Architecture always has higher priority than editorial consistency.

---

# Repository Authority

Architectural authority belongs to:

- CONSTITUTION.md
- Architecture Manifesto
- Architecture Specifications

Editorial work shall never override these documents.

---

# Implementation

Publishing tools, AI assistants and contributors shall follow this policy.

When uncertainty exists, preserve architecture rather than improve wording.

---

# Consequences

The repository remains stable while publication quality continuously improves.

Editorial work becomes repeatable and predictable.