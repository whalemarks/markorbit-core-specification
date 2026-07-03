# MarkOrbit Core Releases

**Repository**

MarkOrbit Core Specification

---

# Purpose

This directory contains the official release history of the MarkOrbit Core Specification.

Each release documents the architectural state of the Core at a specific point in time.

Release documents are historical records.

They are never modified after publication except for correcting obvious typographical errors.

---

# Release Philosophy

The MarkOrbit Core evolves slowly.

Architecture changes are deliberate, reviewed and versioned.

Applications may evolve rapidly.

The Core should remain stable.

A release represents an architectural baseline for all downstream implementations.

---

# Release Lifecycle

Every Core release follows the same lifecycle.

```
Idea

↓

ADR

↓

Architecture Amendment

↓

Specification

↓

Repository Alignment

↓

Release Candidate

↓

Validation

↓

Stable Release
```

No release skips these stages.

---

# Release Types

## Release Candidate (RC)

A Release Candidate freezes the architecture for validation.

Reference implementations are expected to validate the architecture before a stable release.

Example:

```
Core v2.1 RC1
```

---

## Stable Release

A Stable Release represents the official architectural baseline.

Stable releases are intended for long-term implementation.

Example:

```
Core v2.1
```

---

# Validation

A Core release is validated by independent implementations.

Validation is not limited to a single application.

Current validators include:

- MarkOrbit Lite
- MarkReg.com
- MGSN (Mark Global Service Network)
- Workplace implementations
- Future ecosystem applications

Each validator exercises different parts of the architecture.

The Core evolves based on validated architectural feedback.

---

# Versioning Policy

Core uses semantic architectural versioning.

| Version | Meaning |
|----------|---------|
| Major | Architectural evolution introducing new architectural capabilities or responsibilities. |
| Minor | Backward-compatible architectural extensions. |
| Patch | Repository alignment, editorial improvements and non-architectural corrections. |
| RC | Release Candidate intended for validation before a stable release. |

Examples:

```
Core v2.0

Core v2.1 RC1

Core v2.1

Core v2.2

Core v3.0
```

---

# Release History

| Version | Status | Description |
|----------|--------|-------------|
| Core v2.1 RC1 | Release Candidate | Introduces Mo Business and establishes Business Evaluation as a first-class architectural responsibility. |

Future releases will be added to this directory.

---

# Repository Relationship

This directory complements, but does not replace:

- CHANGELOG.md
- Architecture Amendments
- ADRs
- Core Specifications

Their responsibilities remain distinct.

| Document | Purpose |
|----------|---------|
| ADR | Records architectural decisions. |
| Architecture Amendment | Records architectural changes. |
| Specification | Defines the architecture. |
| Release | Records an official architectural baseline. |
| CHANGELOG | Records repository changes. |

---

# Summary

Every release in this directory represents a stable architectural milestone of the MarkOrbit Core Specification.

Applications should reference a released Core version rather than a moving branch whenever possible.

---

**End of Releases README**