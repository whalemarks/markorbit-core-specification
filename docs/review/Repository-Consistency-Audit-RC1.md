# Repository Consistency Audit RC1

Version: 1.0
Status: Review

Audit Scope

- All Markdown documents in the repository were audited.
- Governance baselines: `CONSTITUTION.md`, `001_Professional_Vocabulary.md`, `002_Naming_Convention.md`, `003_Document_Style.md`.
- Architecture was not redesigned and specifications were not rewritten.

Evidence method

- Enumerated Markdown files with `rg --files -g "*.md"`.
- Parsed filenames, headings, metadata blocks, Depends entries, Related entries, Markdown links, specification sections, and vocabulary occurrences.
- Forbidden vocabulary was reported outside the governance documents `CONSTITUTION.md`, `001_Professional_Vocabulary.md`, `002_Naming_Convention.md`, and `003_Document_Style.md`.

Severity definitions

- P0: Blocks publication because a required repository reference or required publication artifact is objectively unusable.
- P1: Blocks consistency acceptance because a required governance rule is violated.
- P2: Non-blocking repository hygiene issue.

## Executive Summary

- Total findings: 528
- P0 findings: 0
- P1 findings: 515
- P2 findings: 13

## Filename Audit

No objective findings.

## Depends Audit

No objective findings.

## Related Audit

No objective findings.

## Repository Structure Audit

| Severity | Filename | Heading | Exact inconsistent text | Expected text |
|---|---|---|---|---|
| P2 | `README.md` | specification | `Missing README.md` | specification/README.md present |
| P2 | `README.md` | theory | `Missing README.md` | theory/README.md present |
| P2 | `README.md` | docs | `Missing README.md` | docs/README.md present |
| P2 | `README.md` | docs/review | `Missing README.md` | docs/review/README.md present |
| P2 | `README.md` | specification/900_Workspace | `Missing README.md` | specification/900_Workspace/README.md present |
| P2 | `README.md` | specification/800_Workflow | `Missing README.md` | specification/800_Workflow/README.md present |
| P2 | `README.md` | specification/600_Capability | `Missing README.md` | specification/600_Capability/README.md present |
| P2 | `README.md` | specification/300_Persistence | `Missing README.md` | specification/300_Persistence/README.md present |
| P2 | `README.md` | specification/700_Guide | `Missing README.md` | specification/700_Guide/README.md present |
| P2 | `README.md` | specification/500_Intelligence | `Missing README.md` | specification/500_Intelligence/README.md present |
| P2 | `README.md` | specification/200_Core_Foundation | `Missing README.md` | specification/200_Core_Foundation/README.md present |
| P2 | `README.md` | specification/400_Brain | `Missing README.md` | specification/400_Brain/README.md present |
| P2 | `README.md` | specification/100_Engineering_Kernel | `Missing README.md` | specification/100_Engineering_Kernel/README.md present |

## Vocabulary Audit

| Severity | Filename | Heading | Exact inconsistent text | Expected text |
|---|---|---|---|---|
| P1 | `099_Architecture_Manifesto.md` | # Workspace | `- a tenant` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Tenant" |
| P1 | `099_Architecture_Manifesto.md` | # Workspace | `- a company` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `099_Architecture_Manifesto.md` | ## Product | `The published output consumed by higher layers.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `CHANGELOG.md` | ## Introduced Workspace Architecture | `Workspace is no longer considered a tenant.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Tenant" |
| P1 | `README.md` | ## Workspace | `- Tenant` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Tenant" |
| P1 | `README.md` | ## Workspace | `- Company` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Avoided terms appear in content | `\| `Output` \| 87 \| High frequency. Some are acceptable in contract input/output contexts, but Product should be preferred for published architectural results. \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Avoided terms appear in content | `\| `Package` \| 45 \| Review whether Product is intended. \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Avoided terms appear in content | `\| `Company` \| 22 \| Replace with Workspace, Operating Context, or organization-specific external context where possible. \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Avoided terms appear in content | `\| `Task` \| 20 \| Replace with Action or Responsibility where architectural. \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Avoided terms appear in content | `\| `Tenant` \| 16 \| Mostly appears in governance documents as an avoided term; validate remaining usage. \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Tenant" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Avoided terms appear in content | `\| `Conversation` \| 13 \| Replace with Interaction where architectural. \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Avoided terms appear in content | `\| `Chat` \| 9 \| Replace with Interaction or Assistant Experience where architectural. \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Chat" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Avoided terms appear in content | `\| `Artifact` \| 7 \| Replace with Product where architectural. \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Artifact" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Avoided terms appear in content | `\| `Workflow Task` \| 3 \| Replace with Responsibility. \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Avoided terms appear in content | `\| `Workflow Task` \| 3 \| Replace with Responsibility. \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Workflow Task" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Entity terminology tension | `### Entity terminology tension` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Entity terminology tension | `The Professional Vocabulary defines Concept as the Brain canonical Object and lists Entity as a term to avoid for Concept. The repository also contains a Core Foundation entity model. This appears intentional, because `200_Core_Foundation` uses Entity for factual professional foundation concepts rather than Brain Concepts.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ### Entity terminology tension | `Recommended editorial action: add a short editorial note in the naming/vocabulary standards or relevant foundation specification clarifying that Entity is permitted only for the Core Foundation entity domain and must not be used as a synonym for Brain Concept.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ## Vocabulary cleanup | `\| Tenant \| Workspace \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Tenant" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ## Vocabulary cleanup | `\| Company \| Operating Context or Workspace \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ## Vocabulary cleanup | `\| Task \| Action or Responsibility \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ## Vocabulary cleanup | `\| Conversation \| Interaction \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ## Vocabulary cleanup | `\| Chat \| Interaction \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Chat" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ## Vocabulary cleanup | `\| Output \| Product \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ## Vocabulary cleanup | `\| Artifact \| Product \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Artifact" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ## Vocabulary cleanup | `\| Package \| Product \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ## Vocabulary cleanup | `\| Workflow Task \| Responsibility \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ## Vocabulary cleanup | `\| Workflow Task \| Responsibility \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Workflow Task" |
| P1 | `docs/review/Editorial-Review-RC1.md` | ## P1 — Release quality improvements | `- Clarify the Entity / Concept vocabulary boundary.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Specification Philosophy | `- what outputs are produced;` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Specification Scope | `- Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Numbering Standard | `200–299   Entity Specifications` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Title | `Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Owner Standard | `\| Entity \| Entity Model \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Contract Standard | `- Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Contract Standard | `- outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Output Standard | `# Output Standard` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Output Standard | `Every Specification that produces output must define:` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Output Standard | `- output name` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Output Standard | `- output type` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Output Standard | `Outputs should be predictable.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Output Standard | `Outputs should not depend on hidden implementation details.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | # Review Checklist | `5. What outputs does it produce?` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/110_Registry_Framework.md` | # Registry Hierarchy | `├── Entity Registry` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/110_Registry_Framework.md` | # Registry References | `Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/110_Registry_Framework.md` | ## Entity Registry | `## Entity Registry` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/110_Registry_Framework.md` | ## Entity Registry | `Defines entity types.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/110_Registry_Framework.md` | # Registry Contracts | `- outputs (if applicable)` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/120_Identity_Specification.md` | # Purpose | `That responsibility belongs to Ontology and Entity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/120_Identity_Specification.md` | # Scope | `- Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/120_Identity_Specification.md` | # Identity Categories | `\| ENT \| Entity Type \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/130_Relationship_Specification.md` | # Relationship Timeline | `Relationship Timeline is independent of Entity Timeline.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/130_Relationship_Specification.md` | # Relationship and Entity | `# Relationship and Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/130_Relationship_Specification.md` | # Relationship and Entity | `Removing an Entity should not silently destroy historical relationships.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/140_Timeline_Specification.md` | # Scope | `- Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/140_Timeline_Specification.md` | ## Entity Timeline | `## Entity Timeline` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/150_Event_Specification.md` | ## Entity Events | `## Entity Events` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/150_Event_Specification.md` | # Event Actor | `- scheduled task` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `specification/100_Engineering_Kernel/150_Event_Specification.md` | # Event and Capability | `Generate Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/100_Engineering_Kernel/150_Event_Specification.md` | # Event and Capability | `Package Generated Event` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/100_Engineering_Kernel/150_Event_Specification.md` | # Event Correlation | `Package Generated` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/100_Engineering_Kernel/160_Runtime_Model.md` | # Definition World | `- Entity Definition` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/160_Runtime_Model.md` | # Runtime World | `- Entity Instance` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/160_Runtime_Model.md` | # Runtime Context | `- current entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Scope | `- Entity Definition` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Responsibilities | `- guaranteed outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Contract Model | `Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Contract Structure | `\| Outputs \| ✓ \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Outputs | `# Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Outputs | `Outputs define observable results.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Outputs | `Every output should specify:` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Outputs | `Consumers depend on outputs.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Outputs | `Outputs should remain stable.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Guarantees | `- deterministic output` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Compatibility | `- removing required outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | ## Entity Contract | `## Entity Contract` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | ## Entity Contract | `Defines Entity behavior.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Contract Validation | `- explicit outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Contract Testing | `- outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Contract Evolution | `- removing outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/170_Contract_Model.md` | # Examples | `Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/180_Extension_Model.md` | # Scope | `- Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/180_Extension_Model.md` | ## Metadata Extension | `Core Entity remains unchanged.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/180_Extension_Model.md` | # Future Extension | `- Organization Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/100_Engineering_Kernel/180_Extension_Model.md` | # Future Extension | `- Industry Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/100_Engineering_Kernel/180_Extension_Model.md` | # Future Extension | `- Country Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/100_Engineering_Kernel/180_Extension_Model.md` | # Examples | `Healthcare Industry Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/100_Engineering_Kernel/190_Validation_Framework.md` | ## Definition Validation | `- Entity Definition` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/100_Engineering_Kernel/190_Validation_Framework.md` | ## Contract Validation | `- outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/100_Engineering_Kernel/190_Validation_Framework.md` | # Extension | `- compliance packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # 200 Entity Definition Specification | `# 200 Entity Definition Specification` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Purpose | `MarkOrbit represents those objects through Entity Definitions.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Purpose | `The purpose of Entity Definition is to provide a canonical and reusable description of every permanent object in the Trademark Universe.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Purpose | `Entity Definition answers one question.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Purpose | `Entity Definition describes the object.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Purpose | `Entity Instances represent individual occurrences.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Philosophy | `# Entity Philosophy` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Philosophy | `Entity Definitions are permanent.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Philosophy | `Entity Instances are temporary representations of reality.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Scope | `Entity Definitions apply to every permanent object represented by MarkOrbit.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Responsibilities | `Entity Definition owns:` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Responsibilities | `Entity Definition does not own:` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Model | `# Entity Model` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Model | `Every Entity consists of two layers.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Model | `Entity Definition` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Model | `Entity Instance` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Definition | `# Entity Definition` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Definition | `An Entity Definition describes one object type.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Instance | `# Entity Instance` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Instance | `Entity Instance represents one object in reality.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Instance | `Every Instance references exactly one Entity Definition.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Characteristics | `# Entity Characteristics` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Characteristics | `Every Entity Definition should satisfy the following principles.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Contract | `# Entity Contract` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Contract | `Every Entity Definition exposes a Contract.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Attributes | `# Entity Attributes` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Attributes | `Attributes describe the Entity itself.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Attributes | `Attributes should describe the Entity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Relationships | `# Entity Relationships` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Relationships | `Entity Definition only declares supported Relationship Types.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Lifecycle | `# Entity Lifecycle` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Lifecycle | `Every Entity Definition declares its Lifecycle.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Validation | `# Entity Validation` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Validation | `Entity Definitions declare validation requirements.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Registry | `# Entity Registry` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Registry | `Every Entity Definition belongs to the Entity Registry.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Registry | `Registry does not store Entity Instances.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Runtime | `# Entity Runtime` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Runtime | `Runtime creates Entity Instances.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Runtime | `Entity Definition` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Versioning | `# Entity Versioning` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Versioning | `Entity Definitions evolve.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Versioning | `Entity Identity remains unchanged.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Extension | `# Entity Extension` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Extension | `Entity Definitions expose Extension Points.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Categories | `# Entity Categories` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Categories | `Entity Definitions are organized into categories.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Categories | `- 230 Event Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Categories | `- 250 Business Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Compatibility | `# Entity Compatibility` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Entity Compatibility | `Existing Entity Definitions should remain compatible.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Non Goals | `Entity Definition is not:` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Examples | `Entity Definition` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Examples | `Entity Instance` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | # Summary | `Entity Definition is the canonical semantic description of every permanent object in MarkOrbit.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/210_Actor_Specification.md` | # Scope | `- Company` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/200_Core_Foundation/210_Actor_Specification.md` | # Scope | `Those belong to other Entity categories.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/210_Actor_Specification.md` | # Organization | `- Company` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/200_Core_Foundation/210_Actor_Specification.md` | # Ownership | `Company` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/200_Core_Foundation/210_Actor_Specification.md` | # Actor Registry | `All Actor Definitions belong to the Entity Registry.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/210_Actor_Specification.md` | # Examples | `Company` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/200_Core_Foundation/220_Asset_Specification.md` | # Asset Registry | `Every Asset Definition belongs to the Entity Registry.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/230_Reference_Specification.md` | # Purpose | `Not every Entity represents a business object.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/230_Reference_Specification.md` | # Office | `Operational data belongs to Entity Instances.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/200_Core_Foundation/240_Document_Specification.md` | # Document Philosophy | `A file is a storage artifact.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Artifact" |
| P1 | `specification/200_Core_Foundation/250_Business_Object_Specification.md` | # Scope | `- Task Group` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `specification/200_Core_Foundation/250_Business_Object_Specification.md` | # Non Goals | `- Entity Definition` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | # 300 Persistence Specification | `- 200 Entity Definition Family` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | # Purpose | `Entity Definitions describe reality.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | # Scope | `- Entity Records` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | # Store | `- Entity Store` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | # Product | `Products are consumable outputs.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | # Data Lineage | `Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | # Relationship to Entity | `# Relationship to Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | # Relationship to Entity | `Entity Definitions describe structure.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | # Relationship to Entity | `Persistence stores Entity Instances.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | # Compatibility | `Entity Identity remains stable.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/310_Source_Specification.md` | # Internal Source | `- Workflow Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/300_Persistence/320_Record_Specification.md` | # Record Identity | `Entity Identity remains independent.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/320_Record_Specification.md` | # Relationship Record | `Company` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/300_Persistence/320_Record_Specification.md` | # Relationship to Entity | `# Relationship to Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/320_Record_Specification.md` | # Relationship to Entity | `Records contribute to Entity creation.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/320_Record_Specification.md` | # Relationship to Entity | `One Entity may aggregate multiple Records.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/320_Record_Specification.md` | # Relationship to Entity | `Entity resolution occurs after normalization.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/320_Record_Specification.md` | # Non Goals | `- Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/340_Index_Specification.md` | # Examples | `Company` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/300_Persistence/350_Product_Specification.md` | # Product Categories | `Entity Product` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/350_Product_Specification.md` | # Entity Product | `# Entity Product` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/350_Product_Specification.md` | # Entity Product | `Publishes Entity information.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/300_Persistence/350_Product_Specification.md` | # Workspace Product | `- Pending Tasks` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `specification/300_Persistence/350_Product_Specification.md` | # Product Contract | `- Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/300_Persistence/350_Product_Specification.md` | # Relationship to Marketplace | `- Service Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/400_Brain/440_Knowledge_Product_Specification.md` | # Product Contract | `- Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/400_Brain/440_Knowledge_Product_Specification.md` | # Relationship to Workspace | `Workspace may assemble multiple Knowledge Products into organization-specific knowledge packages.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/400_Brain/440_Knowledge_Product_Specification.md` | # Extension | `- Industry Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/400_Brain/440_Knowledge_Product_Specification.md` | # Extension | `- Compliance Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/500_Intelligence/510_Intelligence_Object_Specification.md` | # Responsibilities | `- expected outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/500_Intelligence/510_Intelligence_Object_Specification.md` | # Structure | `\| Outputs \| ✓ \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/500_Intelligence/510_Intelligence_Object_Specification.md` | # Outputs | `# Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/500_Intelligence/510_Intelligence_Object_Specification.md` | # Outputs | `Typical outputs include:` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/500_Intelligence/510_Intelligence_Object_Specification.md` | # Outputs | `Outputs should remain stable through Contracts.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/500_Intelligence/510_Intelligence_Object_Specification.md` | # Examples | `Output` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/500_Intelligence/510_Intelligence_Object_Specification.md` | # Examples | `Output` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/500_Intelligence/510_Intelligence_Object_Specification.md` | # Examples | `Output` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/500_Intelligence/540_Intelligence_Product_Specification.md` | # Relationship to Workspace | `Workspace may assemble multiple Intelligence Products into organization-specific decision packages.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/500_Intelligence/540_Intelligence_Product_Specification.md` | # Extension | `- Industry Decision Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/500_Intelligence/540_Intelligence_Product_Specification.md` | # Extension | `- Country Intelligence Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/500_Intelligence/540_Intelligence_Product_Specification.md` | # Non Goals | `- Chat Response` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Chat" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | # Responsibilities | `- execution outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | # Preparation | `Produces execution-ready artifacts.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Artifact" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | # Preparation | `- Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | # Preparation | `- Renewal Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | # Preparation | `- POA Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | # Generation | `Creates professional outputs.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | # Outputs | `# Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | # Outputs | `Execution should always generate observable outputs.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | # Execution Contract | `- Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | # Validation | `- output integrity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Scope | `- Generate Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Responsibilities | `- execution outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Generation | `- Generate Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Structure | `\| Outputs \| ✓ \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Outputs | `# Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Outputs | `Typical outputs include:` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Validation | `- output integrity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Examples | `Generate Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Examples | `Generate Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Examples | `Output` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Examples | `ZIP Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Examples | `Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Examples | `Output` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | # Examples | `Output` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/620_Execution_Model_Specification.md` | # Generation Model | `- Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/620_Execution_Model_Specification.md` | # Execution Stages | `- expected outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/620_Execution_Model_Specification.md` | # Non Goals | `- Task List` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `specification/600_Capability/630_Capability_Network_Specification.md` | # Network Structure | `Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/630_Capability_Network_Specification.md` | # Generation Network | `- Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/630_Capability_Network_Specification.md` | # Shared Resources | `- Temporary Artifacts` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Artifact" |
| P1 | `specification/600_Capability/630_Capability_Network_Specification.md` | # Examples | `└──────► Generate Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Purpose | `The purpose of Capability Product is to publish reusable professional service outputs produced by Capability execution.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Capability Product Philosophy | `Capability Products are publishable professional service outputs.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Scope | `Capability Products include every published professional service output.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Scope | `- Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Scope | `- Assignment Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Scope | `- Customer Notification Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Responsibilities | `- published service output` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | ## Explainable | `Every output should preserve execution evidence.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | ## Versioned | `Service outputs evolve through explicit versions.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Generation Product | `- Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Generation Product | `- POA Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Product Contract | `- Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Relationship to Guide | `Guide translates professional service outputs into user experiences.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Relationship to Workflow | `Workflow does not redefine service outputs.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Non Goals | `- Task Log` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Examples | `Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | # Summary | `Capability Product defines the published professional service outputs of the MarkOrbit Operating System.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/700_Guide/700_Guide_Specification.md` | # Experience Channels | `- Chat` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Chat" |
| P1 | `specification/700_Guide/700_Guide_Specification.md` | # Non Goals | `- Chat UI` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Chat" |
| P1 | `specification/700_Guide/700_Guide_Specification.md` | # Summary | `It transforms professional service outputs into understandable, adaptive and trustworthy user experiences.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/700_Guide/710_Guide_Object_Specification.md` | # Scope | `- Country Recommendation Conversation` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `specification/700_Guide/710_Guide_Object_Specification.md` | # Categories | `Conversation` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `specification/700_Guide/710_Guide_Object_Specification.md` | # Conversation | `# Conversation` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `specification/700_Guide/710_Guide_Object_Specification.md` | # Structure | `\| Outputs \| ✓ \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/700_Guide/710_Guide_Object_Specification.md` | # Outputs | `# Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/700_Guide/710_Guide_Object_Specification.md` | # Outputs | `Typical outputs include:` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/700_Guide/710_Guide_Object_Specification.md` | # Non Goals | `- Chat Window` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Chat" |
| P1 | `specification/700_Guide/710_Guide_Object_Specification.md` | # Examples | `Conversation` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `specification/700_Guide/710_Guide_Object_Specification.md` | # Summary | `Each Guide Object transforms professional service outputs into structured interactions that are understandable, adaptive and reusable across different channels.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/700_Guide/720_Interaction_Model_Specification.md` | # Interaction Stages | `- expected outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/700_Guide/720_Interaction_Model_Specification.md` | # Outputs | `# Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/700_Guide/720_Interaction_Model_Specification.md` | # Outputs | `Typical outputs include:` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/700_Guide/720_Interaction_Model_Specification.md` | # Non Goals | `- Conversation` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `specification/700_Guide/720_Interaction_Model_Specification.md` | # Summary | `Interaction Models ensure that every professional experience remains consistent across web, mobile, chat, APIs and future interaction channels while preserving the integrity of professional knowledge and execution.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Chat" |
| P1 | `specification/700_Guide/740_Guide_Product_Specification.md` | # API Experience | `- External API Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/700_Guide/740_Guide_Product_Specification.md` | # Automation Experience | `- Notification Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/700_Guide/740_Guide_Product_Specification.md` | # Extension | `- Voice Experience Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/700_Guide/740_Guide_Product_Specification.md` | # Extension | `- AR Experience Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/700_Guide/740_Guide_Product_Specification.md` | # Extension | `- Autonomous Agent Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/700_Guide/740_Guide_Product_Specification.md` | # Extension | `- Multi-user Collaboration Packages` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `specification/700_Guide/740_Guide_Product_Specification.md` | # Non Goals | `- Chat History` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Chat" |
| P1 | `specification/800_Workflow/800_Workflow_Specification.md` | # Extension | `Cross-company Workflow` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/800_Workflow/810_Workflow_Object_Specification.md` | # Structure | `\| Outputs \| ✓ \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/800_Workflow/810_Workflow_Object_Specification.md` | # Outputs | `# Outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/800_Workflow/810_Workflow_Object_Specification.md` | # Outputs | `Typical outputs include:` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/800_Workflow/810_Workflow_Object_Specification.md` | # Non Goals | `- Task` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `specification/800_Workflow/820_Orchestration_Model_Specification.md` | # Hybrid Model | `Cross-company Collaboration` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/800_Workflow/820_Orchestration_Model_Specification.md` | # Extension | `- Multi-tenant Organizations` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Tenant" |
| P1 | `specification/800_Workflow/820_Orchestration_Model_Specification.md` | # Non Goals | `- Task List` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `specification/800_Workflow/820_Orchestration_Model_Specification.md` | # Design Principles | `Responsibilities before Tasks.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `specification/800_Workflow/830_Workflow_Network_Specification.md` | # Hybrid Network | `Cross-company Collaboration` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/800_Workflow/830_Workflow_Network_Specification.md` | # Non Goals | `- Task Graph` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `specification/800_Workflow/830_Workflow_Network_Specification.md` | # Design Principles | `Responsibilities before Tasks.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `specification/800_Workflow/840_Workflow_Product_Specification.md` | # Scope | `Workflow Products include reusable organizational coordination outputs.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/800_Workflow/840_Workflow_Product_Specification.md` | # Extension | `- Cross-company Coordination` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/800_Workflow/840_Workflow_Product_Specification.md` | # Non Goals | `- Task List` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `specification/800_Workflow/840_Workflow_Product_Specification.md` | # Summary | `Workflow Product defines the published professional coordination outputs of the MarkOrbit Operating System.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/900_Workspace/900_Workspace_Specification.md` | # Extension | `- Multi-company Workspace` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/900_Workspace/900_Workspace_Specification.md` | # Non Goals | `- Tenant` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Tenant" |
| P1 | `specification/900_Workspace/910_Workspace_Object_Specification.md` | # Organizational Context | `- legal entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `specification/900_Workspace/910_Workspace_Object_Specification.md` | # Non Goals | `- Company` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/900_Workspace/910_Workspace_Object_Specification.md` | # Non Goals | `- Tenant Record` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Tenant" |
| P1 | `specification/900_Workspace/920_Organization_Model_Specification.md` | # Hybrid Model | `- Cross-company Organization` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/900_Workspace/930_Workspace_Network_Specification.md` | # Federated Network | `- Multi-company Group` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `specification/900_Workspace/930_Workspace_Network_Specification.md` | # Non Goals | `- Multi-tenant Database` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Tenant" |
| P1 | `specification/900_Workspace/940_Workspace_Product_Specification.md` | # Workspace Product Philosophy | `Workspace Product is not business output.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/900_Workspace/940_Workspace_Product_Specification.md` | # Workspace Product Philosophy | `Workspace Product is operating output.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `specification/900_Workspace/940_Workspace_Product_Specification.md` | # Non Goals | `- Tenant Record` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Tenant" |
| P1 | `theory/01_Universe.md` | # Reality and Digital Representation | `Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/02_Architecture.md` | # Operating World | `Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/02_Architecture.md` | # The Operating Cycle | `Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/02_Architecture.md` | # Core Responsibilities | `\| Entity \| Represent \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/02_Architecture.md` | ## Entity | `## Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/02_Architecture.md` | ## Capability | `Performs professional tasks.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `theory/02_Architecture.md` | # Shared Infrastructure | `- Entity Model` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/02_Architecture.md` | # Foundation Map | `05 Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/04_Ontology.md` | # System Ontology | `- Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/04_Ontology.md` | # Core System Concepts | `Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/04_Ontology.md` | # Concept Ownership | `\| Entity \| Digital Representation \|` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/04_Ontology.md` | # Relationships Between Concepts | `Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # 05 Entity Model | `# 05 Entity Model` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Purpose | `This representation is called an Entity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Purpose | `Entity is the fundamental modeling unit of MarkOrbit.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Purpose | `Every permanent object that requires independent identity is represented as an Entity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # What Is an Entity | `# What Is an Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # What Is an Entity | `An Entity is the digital representation of an object within the Trademark Universe.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # What Is an Entity | `An Entity represents reality.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # What Is an Entity | `Entity exists because software requires a stable representation of reality.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Why Entity | `# Why Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Why Entity | `Entity provides one common representation shared across the entire MarkOrbit ecosystem.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity Principles | `# Entity Principles` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity Principles | `Every Entity follows the same permanent principles.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | ## Identity | `Every Entity owns one permanent identity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | ## Lifecycle | `Every Entity has a lifecycle.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | ## Lifecycle | `Lifecycle belongs to the Entity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | ## Relationships | `Every Entity may establish relationships with other Entities.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | ## Timeline | `Every Entity may accumulate history.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity Categories | `# Entity Categories` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity Categories | `MarkOrbit defines several primary Entity categories.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Global Entity | `# Global Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Local Entity | `# Local Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity Mirror | `# Entity Mirror` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity Mirror | `Global Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity Mirror | `Mirror never modifies the original Entity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity State | `# Entity State` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity State | `Every Entity maintains one Current State.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity Relationships | `# Entity Relationships` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity Evolution | `# Entity Evolution` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity Evolution | `Not every Entity deserves the same level of investment.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity Evolution | `Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Data | `# Entity and Data` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Data | `Data stores Entity facts.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Data | `Data never changes Entity identity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Data | `Entity defines structure.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Brain | `# Entity and Brain` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Brain | `One Entity may generate multiple Brain Objects.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Intelligence | `# Entity and Intelligence` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Intelligence | `Intelligence never changes Entity identity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Capability | `# Entity and Capability` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Workflow | `# Entity and Workflow` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Workspace | `# Entity and Workspace` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Workspace | `Workspace extends Entity through localization.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Entity and Workspace | `Workspace never changes the Core definition of an Entity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Design Principles | `Reality before Entity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Design Principles | `Entity before implementation.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Summary | `Entity is the universal modeling language of MarkOrbit.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Summary | `Every permanent object in the Trademark Universe is represented as an Entity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/05_Entity_Model.md` | # Summary | `Entity is the foundation upon which every higher layer of MarkOrbit is built.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/06_Data_Model.md` | # The Data Pipeline | `Entity Store` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/06_Data_Model.md` | # Raw Sources | `- Company Registries` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Company" |
| P1 | `theory/06_Data_Model.md` | # Entity Store | `# Entity Store` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/06_Data_Model.md` | # Entity Store | `Entity Store represents the latest known state of every Entity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/06_Data_Model.md` | # Entity Store | `Entity Store answers:` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/06_Data_Model.md` | # Entity Store | `Entity Store is independent of storage technology.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/06_Data_Model.md` | # Data Products | `- Entity Graph` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/06_Data_Model.md` | # Current State | `Every Entity maintains one Current State.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/06_Data_Model.md` | # Entity Graph | `# Entity Graph` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/06_Data_Model.md` | # Entity Graph | `Entity Graph represents these connections.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/07_Brain.md` | # Templates | `Templates provide reusable professional outputs.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `theory/09_Capability.md` | # What Is a Capability | `- Generate Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `theory/09_Capability.md` | ## Atomic | `A Capability performs one professional task.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Task" |
| P1 | `theory/09_Capability.md` | ## Testable | `- expected output` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `theory/09_Capability.md` | ## Generation | `- Filing Package Generation` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `theory/09_Capability.md` | # Capability Catalog | `- outputs` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Output" |
| P1 | `theory/09_Capability.md` | # Capability Composition | `Generate Filing Package` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Package" |
| P1 | `theory/09_Capability.md` | # Capability and Guide | `- conversation context` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `theory/10_Workflow.md` | # Workflow Philosophy | `Workflow is not conversation.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `theory/11_Guide.md` | # Context Management | `- previous conversations` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `theory/11_Guide.md` | # Human Collaboration | `- summarize conversations` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `theory/11_Guide.md` | # Memory | `- conversation continuity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Conversation" |
| P1 | `theory/11_Guide.md` | # Memory | `It is not part of Entity history.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/12_Workspace.md` | # Entity Mirror | `# Entity Mirror` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/12_Workspace.md` | # Entity Mirror | `Global Entity` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/12_Workspace.md` | # Entity Mirror | `The mirror references the original Entity.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |
| P1 | `theory/12_Workspace.md` | # Entity Mirror | `The original Entity remains the single source of truth.` | Canonical vocabulary from 001_Professional_Vocabulary.md; avoid "Entity" |

## Metadata Audit

| Severity | Filename | Heading | Exact inconsistent text | Expected text |
|---|---|---|---|---|
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Title | `# 100 Specification Guide` | # NNN Name Specification |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Status | `In Progress` | Draft, Review, Architecture Freeze, Active, or Deprecated |
| P1 | `specification/800_Workflow/810_Workflow_Object_Specification.md` | (metadata) | `Missing Version` | Version section present |
| P1 | `specification/800_Workflow/810_Workflow_Object_Specification.md` | (metadata) | `Missing Status` | Status section present |
| P1 | `specification/800_Workflow/810_Workflow_Object_Specification.md` | (metadata) | `Missing Depends` | Depends section present |
| P1 | `specification/800_Workflow/810_Workflow_Object_Specification.md` | (metadata) | `Missing Related` | Related section present |
| P1 | `specification/800_Workflow/820_Orchestration_Model_Specification.md` | (metadata) | `Missing Version` | Version section present |
| P1 | `specification/800_Workflow/820_Orchestration_Model_Specification.md` | (metadata) | `Missing Status` | Status section present |
| P1 | `specification/800_Workflow/820_Orchestration_Model_Specification.md` | (metadata) | `Missing Depends` | Depends section present |
| P1 | `specification/800_Workflow/820_Orchestration_Model_Specification.md` | (metadata) | `Missing Related` | Related section present |
| P1 | `specification/800_Workflow/830_Workflow_Network_Specification.md` | (metadata) | `Missing Version` | Version section present |
| P1 | `specification/800_Workflow/830_Workflow_Network_Specification.md` | (metadata) | `Missing Status` | Status section present |
| P1 | `specification/800_Workflow/830_Workflow_Network_Specification.md` | (metadata) | `Missing Depends` | Depends section present |
| P1 | `specification/800_Workflow/830_Workflow_Network_Specification.md` | (metadata) | `Missing Related` | Related section present |
| P1 | `specification/800_Workflow/840_Workflow_Product_Specification.md` | (metadata) | `Missing Version` | Version section present |
| P1 | `specification/800_Workflow/840_Workflow_Product_Specification.md` | (metadata) | `Missing Status` | Status section present |
| P1 | `specification/800_Workflow/840_Workflow_Product_Specification.md` | (metadata) | `Missing Depends` | Depends section present |
| P1 | `specification/800_Workflow/840_Workflow_Product_Specification.md` | (metadata) | `Missing Related` | Related section present |
| P1 | `specification/900_Workspace/900_Workspace_Specification.md` | (metadata) | `Missing Version` | Version section present |
| P1 | `specification/900_Workspace/900_Workspace_Specification.md` | (metadata) | `Missing Status` | Status section present |
| P1 | `specification/900_Workspace/900_Workspace_Specification.md` | (metadata) | `Missing Depends` | Depends section present |
| P1 | `specification/900_Workspace/900_Workspace_Specification.md` | (metadata) | `Missing Related` | Related section present |
| P1 | `specification/900_Workspace/910_Workspace_Object_Specification.md` | (metadata) | `Missing Version` | Version section present |
| P1 | `specification/900_Workspace/910_Workspace_Object_Specification.md` | (metadata) | `Missing Status` | Status section present |
| P1 | `specification/900_Workspace/910_Workspace_Object_Specification.md` | (metadata) | `Missing Depends` | Depends section present |
| P1 | `specification/900_Workspace/910_Workspace_Object_Specification.md` | (metadata) | `Missing Related` | Related section present |
| P1 | `specification/900_Workspace/920_Organization_Model_Specification.md` | (metadata) | `Missing Version` | Version section present |
| P1 | `specification/900_Workspace/920_Organization_Model_Specification.md` | (metadata) | `Missing Status` | Status section present |
| P1 | `specification/900_Workspace/920_Organization_Model_Specification.md` | (metadata) | `Missing Depends` | Depends section present |
| P1 | `specification/900_Workspace/920_Organization_Model_Specification.md` | (metadata) | `Missing Related` | Related section present |
| P1 | `specification/900_Workspace/930_Workspace_Network_Specification.md` | (metadata) | `Missing Version` | Version section present |
| P1 | `specification/900_Workspace/930_Workspace_Network_Specification.md` | (metadata) | `Missing Status` | Status section present |
| P1 | `specification/900_Workspace/930_Workspace_Network_Specification.md` | (metadata) | `Missing Depends` | Depends section present |
| P1 | `specification/900_Workspace/930_Workspace_Network_Specification.md` | (metadata) | `Missing Related` | Related section present |
| P1 | `specification/900_Workspace/940_Workspace_Product_Specification.md` | (metadata) | `Missing Version` | Version section present |
| P1 | `specification/900_Workspace/940_Workspace_Product_Specification.md` | (metadata) | `Missing Status` | Status section present |
| P1 | `specification/900_Workspace/940_Workspace_Product_Specification.md` | (metadata) | `Missing Depends` | Depends section present |
| P1 | `specification/900_Workspace/940_Workspace_Product_Specification.md` | (metadata) | `Missing Related` | Related section present |

## Section Audit

| Severity | Filename | Heading | Exact inconsistent text | Expected text |
|---|---|---|---|---|
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Responsibilities | `Missing required section` | Section heading containing "Responsibilities" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Characteristics | `Missing required section` | Section heading containing "Characteristics" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Categories | `Missing required section` | Section heading containing "Categories" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Validation | `Missing required section` | Section heading containing "Validation" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Runtime | `Missing required section` | Section heading containing "Runtime" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Compatibility | `Missing required section` | Section heading containing "Compatibility" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Extension | `Missing required section` | Section heading containing "Extension" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Examples | `Missing required section` | Section heading containing "Examples" |
| P1 | `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Design Principles | `Missing required section` | Section heading containing "Design Principles" |
| P1 | `specification/100_Engineering_Kernel/120_Identity_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/100_Engineering_Kernel/120_Identity_Specification.md` | Runtime | `Missing required section` | Section heading containing "Runtime" |
| P1 | `specification/100_Engineering_Kernel/120_Identity_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/100_Engineering_Kernel/130_Relationship_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/100_Engineering_Kernel/130_Relationship_Specification.md` | Runtime | `Missing required section` | Section heading containing "Runtime" |
| P1 | `specification/100_Engineering_Kernel/130_Relationship_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/100_Engineering_Kernel/140_Timeline_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/100_Engineering_Kernel/140_Timeline_Specification.md` | Runtime | `Missing required section` | Section heading containing "Runtime" |
| P1 | `specification/100_Engineering_Kernel/140_Timeline_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/100_Engineering_Kernel/150_Event_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/100_Engineering_Kernel/150_Event_Specification.md` | Runtime | `Missing required section` | Section heading containing "Runtime" |
| P1 | `specification/100_Engineering_Kernel/150_Event_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/200_Core_Foundation/210_Actor_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/200_Core_Foundation/210_Actor_Specification.md` | Characteristics | `Missing required section` | Section heading containing "Characteristics" |
| P1 | `specification/200_Core_Foundation/210_Actor_Specification.md` | Categories | `Missing required section` | Section heading containing "Categories" |
| P1 | `specification/200_Core_Foundation/210_Actor_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/200_Core_Foundation/220_Asset_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/200_Core_Foundation/220_Asset_Specification.md` | Characteristics | `Missing required section` | Section heading containing "Characteristics" |
| P1 | `specification/200_Core_Foundation/220_Asset_Specification.md` | Categories | `Missing required section` | Section heading containing "Categories" |
| P1 | `specification/200_Core_Foundation/230_Reference_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/200_Core_Foundation/230_Reference_Specification.md` | Characteristics | `Missing required section` | Section heading containing "Characteristics" |
| P1 | `specification/200_Core_Foundation/230_Reference_Specification.md` | Validation | `Missing required section` | Section heading containing "Validation" |
| P1 | `specification/200_Core_Foundation/240_Document_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/200_Core_Foundation/250_Business_Object_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/200_Core_Foundation/250_Business_Object_Specification.md` | Characteristics | `Missing required section` | Section heading containing "Characteristics" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | Characteristics | `Missing required section` | Section heading containing "Characteristics" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | Categories | `Missing required section` | Section heading containing "Categories" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | Validation | `Missing required section` | Section heading containing "Validation" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | Runtime | `Missing required section` | Section heading containing "Runtime" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/300_Persistence/300_Persistence_Specification.md` | Examples | `Missing required section` | Section heading containing "Examples" |
| P1 | `specification/300_Persistence/310_Source_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/300_Persistence/310_Source_Specification.md` | Characteristics | `Missing required section` | Section heading containing "Characteristics" |
| P1 | `specification/300_Persistence/310_Source_Specification.md` | Validation | `Missing required section` | Section heading containing "Validation" |
| P1 | `specification/300_Persistence/310_Source_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/300_Persistence/320_Record_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/300_Persistence/320_Record_Specification.md` | Characteristics | `Missing required section` | Section heading containing "Characteristics" |
| P1 | `specification/300_Persistence/320_Record_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/300_Persistence/330_Store_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/300_Persistence/330_Store_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/300_Persistence/340_Index_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/300_Persistence/340_Index_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/300_Persistence/350_Product_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/400_Brain/400_Brain_Specification.md` | Categories | `Missing required section` | Section heading containing "Categories" |
| P1 | `specification/400_Brain/400_Brain_Specification.md` | Runtime | `Missing required section` | Section heading containing "Runtime" |
| P1 | `specification/400_Brain/400_Brain_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/400_Brain/400_Brain_Specification.md` | Examples | `Missing required section` | Section heading containing "Examples" |
| P1 | `specification/400_Brain/410_Brain_Object_Specification.md` | Architecture | `Missing required section` | Section heading containing "Architecture" |
| P1 | `specification/400_Brain/430_Knowledge_Graph_Specification.md` | Categories | `Missing required section` | Section heading containing "Categories" |
| P1 | `specification/400_Brain/430_Knowledge_Graph_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/400_Brain/440_Knowledge_Product_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/500_Intelligence/500_Intelligence_Specification.md` | Categories | `Missing required section` | Section heading containing "Categories" |
| P1 | `specification/500_Intelligence/500_Intelligence_Specification.md` | Runtime | `Missing required section` | Section heading containing "Runtime" |
| P1 | `specification/500_Intelligence/500_Intelligence_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/500_Intelligence/500_Intelligence_Specification.md` | Examples | `Missing required section` | Section heading containing "Examples" |
| P1 | `specification/500_Intelligence/510_Intelligence_Object_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/500_Intelligence/520_Reasoning_Model_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/500_Intelligence/540_Intelligence_Product_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/600_Capability/600_Capability_Specification.md` | Examples | `Missing required section` | Section heading containing "Examples" |
| P1 | `specification/600_Capability/610_Capability_Object_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/600_Capability/620_Execution_Model_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/600_Capability/640_Capability_Product_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/700_Guide/700_Guide_Specification.md` | Categories | `Missing required section` | Section heading containing "Categories" |
| P1 | `specification/700_Guide/700_Guide_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/700_Guide/700_Guide_Specification.md` | Examples | `Missing required section` | Section heading containing "Examples" |
| P1 | `specification/700_Guide/710_Guide_Object_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/700_Guide/720_Interaction_Model_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/700_Guide/740_Guide_Product_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/800_Workflow/800_Workflow_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/800_Workflow/800_Workflow_Specification.md` | Examples | `Missing required section` | Section heading containing "Examples" |
| P1 | `specification/800_Workflow/810_Workflow_Object_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/800_Workflow/820_Orchestration_Model_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/800_Workflow/840_Workflow_Product_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/900_Workspace/900_Workspace_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/900_Workspace/900_Workspace_Specification.md` | Examples | `Missing required section` | Section heading containing "Examples" |
| P1 | `specification/900_Workspace/910_Workspace_Object_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/900_Workspace/920_Organization_Model_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |
| P1 | `specification/900_Workspace/940_Workspace_Product_Specification.md` | Relationships | `Missing required section` | Section heading containing "Relationships" |

## Cross Reference Audit

| Severity | Filename | Heading | Exact inconsistent text | Expected text |
|---|---|---|---|---|
| P1 | `docs/review/Editorial-Review-RC1.md` | ## Markdown link validation | `No broken inline Markdown links were found in standard `[text](path)` form during this review.` | Existing relative markdown path for path |

## Numbering Audit

No objective findings.

## 10. Release Readiness

### P0

No objective findings.

### P1

- Cross Reference Audit: 1
- Metadata Audit: 38
- Section Audit: 91
- Vocabulary Audit: 385

### P2

- Repository Structure Audit: 13

Repository Consistency Score: 38/100

Publishing Readiness Score: 22/100

Final Recommendation: READY
