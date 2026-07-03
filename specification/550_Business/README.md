# 550_Business

**Module**

MarkOrbit Core Specification

**Status**

Draft

**Version**

Core Specification v2.1 RC1

---

# Overview

The **550_Business** module defines the **Business Evaluation** layer of the MarkOrbit Core Architecture.

Mo Business extends the Core by introducing an independent architectural responsibility for evaluating the business significance of observable facts.

Business Evaluation complements Professional Understanding and Intelligent Reasoning while remaining independent from both.

This module specifies the architecture of Mo Business.

It does not define implementation details.

---

# Architectural Position

```
                Applications
                      │
                Mo Workspace
                      │
                Mo Capability
                      │
               Mo Intelligence
                 /           \
         Mo Brain         Mo Business
        Understand         Evaluate
                 \           /
                   Mo Data
                    Facts
```

Mo Business consumes factual information from **Mo Data** and publishes reusable **Business Evaluation** for downstream layers.

---

# Primary Responsibility

Mo Business owns exactly one architectural responsibility.

> **Business Evaluation**

Business Evaluation measures the business significance of observable facts.

Typical examples include:

- business value
- business opportunity
- business performance
- business growth
- business contribution
- business ROI

Business Evaluation is independent from:

- Professional Understanding (Mo Brain)
- Intelligent Reasoning (Mo Intelligence)

---

# Module Structure

| Document | Description |
|----------|-------------|
| **550_Mo_Business_Specification.md** | Module entry specification |
| **551_What_is_Mo_Business.md** | Identity and architectural purpose |
| **552_Evaluation_Targets.md** | Objects evaluated by Mo Business |
| **553_Evaluation_Dimensions.md** | Dimensions of Business Evaluation |
| **554_Evaluation_Pipeline.md** | Canonical evaluation pipeline |
| **555_Business_Relationships.md** | Relationships with other Core layers |
| **556_Business_Interfaces.md** | Architectural interfaces |
| **557_Evolution.md** | Evolution principles |

---

# Reading Order

For readers unfamiliar with Mo Business, the recommended order is:

1. README.md
2. 550_Mo_Business_Specification.md
3. 551 — What is Mo Business
4. 552 — Evaluation Targets
5. 553 — Evaluation Dimensions
6. 554 — Evaluation Pipeline
7. 555 — Business Relationships
8. 556 — Business Interfaces
9. 557 — Evolution

---

# Design Principles

Mo Business follows the core principles of the MarkOrbit Architecture.

- Facts remain in **Mo Data**.
- Professional Understanding remains in **Mo Brain**.
- Business Evaluation belongs exclusively to **Mo Business**.
- Intelligent Reasoning remains in **Mo Intelligence**.
- Execution belongs to **Mo Capability**.
- Context organisation belongs to **Mo Workspace**.

Each layer owns one primary responsibility.

---

# Related Documents

- Core Specification v2.0 RC1
- Architecture Amendment 001 — Introduce Mo Business
- ADR-004 — Introduce Mo Business Layer
- 550_Mo_Business_Specification.md

---

# Scope

This module specifies the Business Evaluation layer only.

Implementation, APIs, storage models and runtime behaviour are intentionally outside the scope of this module.

Reference implementations are expected to conform to the architecture defined here.

---

**End of README**