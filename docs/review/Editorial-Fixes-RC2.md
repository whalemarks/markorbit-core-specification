# Editorial Fixes RC2

Version: 2.0

Status: Complete

Date: 2026-07-03

## Purpose

This report records the Publishing Sprint B RC2 editorial fixes applied to the MarkOrbit Core Specification.

## Scope

The changes are editorial only:

- completed repository navigation README files
- corrected obsolete filenames and paths in references
- improved top-level repository navigation
- preserved contextual vocabulary boundaries
- avoided optional section additions that would only create artificial consistency

No architecture was redesigned.

## Modified Files

| File | What changed | Why it changed |
|---|---|---|
| `README.md` | Replaced legacy repository structure text with concise linked navigation to theory, specification, docs and specification domains. | Improves GitHub readability and removes obsolete structure entries. |
| `002_Naming_Convention.md` | Updated example filenames to current canonical specification filenames. | Fixes legacy filename references. |
| `003_Document_Style.md` | Updated example references to current canonical specification filenames. | Fixes legacy filename references. |
| `docs/README.md` | Added documentation directory index. | Creates missing navigation README. |
| `docs/review/README.md` | Added review directory index. | Creates missing navigation README. |
| `docs/review/Editorial-Review-RC1.md` | Corrected obsolete theory paths and README references now satisfied by RC2. | Fixes broken or legacy references in prior review material. |
| `docs/review/Editorial-Fixes-RC2.md` | Added this RC2 change report. | Records all editorial fixes as requested. |
| `theory/README.md` | Added theory directory index and reading guidance. | Creates missing navigation README. |
| `specification/README.md` | Added specification directory index and reading guidance. | Creates missing navigation README. |
| `specification/100_Engineering_Kernel/README.md` | Added Engineering Kernel directory index. | Creates domain navigation README. |
| `specification/200_Core_Foundation/README.md` | Added Core Foundation directory index. | Creates domain navigation README. |
| `specification/300_Persistence/README.md` | Added Persistence directory index. | Creates domain navigation README. |
| `specification/400_Brain/README.md` | Added Brain directory index. | Creates domain navigation README. |
| `specification/500_Intelligence/README.md` | Added Intelligence directory index. | Creates domain navigation README. |
| `specification/600_Capability/README.md` | Added Capability directory index. | Creates domain navigation README. |
| `specification/700_Guide/README.md` | Added Guide directory index. | Creates domain navigation README. |
| `specification/800_Workflow/README.md` | Added Workflow directory index. | Creates domain navigation README. |
| `specification/900_Workspace/README.md` | Added Workspace directory index. | Creates domain navigation README. |
| `specification/100_Engineering_Kernel/100_Specification_Guide.md` | Corrected obsolete theory paths. | Fixes broken references to moved theory files. |
| `specification/100_Engineering_Kernel/110_Registry_Framework.md` | Corrected legacy Core Foundation filename. | Fixes incorrect Related entry. |
| `specification/100_Engineering_Kernel/120_Identity_Specification.md` | Corrected legacy Core Foundation filename. | Fixes incorrect Related entry. |
| `specification/100_Engineering_Kernel/130_Relationship_Specification.md` | Corrected legacy Core Foundation and Persistence filenames. | Fixes incorrect Related entries. |
| `specification/100_Engineering_Kernel/140_Timeline_Specification.md` | Corrected legacy Persistence filename. | Fixes incorrect Related entry. |
| `specification/100_Engineering_Kernel/150_Event_Specification.md` | Corrected legacy Persistence filename. | Fixes incorrect Related entry. |
| `specification/100_Engineering_Kernel/160_Runtime_Model.md` | Corrected legacy Core Foundation filename. | Fixes incorrect Related entry. |
| `specification/100_Engineering_Kernel/170_Contract_Model.md` | Corrected legacy Core Foundation and Persistence filenames. | Fixes incorrect Related entries. |
| `specification/100_Engineering_Kernel/190_Validation_Framework.md` | Corrected legacy Core Foundation and Persistence filenames. | Fixes incorrect Related entries. |
| `specification/200_Core_Foundation/200_Entity_Definition_Specification.md` | Corrected obsolete Event and Business Object filenames. | Fixes incorrect Related entries while preserving Core Foundation terminology. |
| `specification/200_Core_Foundation/210_Actor_Specification.md` | Corrected obsolete Business Object filename. | Fixes incorrect Related entry. |
| `specification/200_Core_Foundation/220_Asset_Specification.md` | Corrected obsolete Business Object filename. | Fixes incorrect Related entry. |
| `specification/200_Core_Foundation/230_Reference_Specification.md` | Corrected legacy Persistence filename. | Fixes incorrect Related entry. |
| `specification/200_Core_Foundation/240_Document_Specification.md` | Corrected legacy Persistence filename. | Fixes incorrect Related entry. |
| Brain, Intelligence, Capability, Guide, Workflow and Workspace domain specification files | Added missing `_Specification` suffixes in Related entries and removed missing Platform specification references where no target file exists. | Fixes obsolete filenames and broken references without changing architecture. |

## Architecture Confirmation

No architecture was redesigned.

No new concepts were introduced.

No architectural objects were renamed.

No vocabulary replacements were applied automatically.

No optional sections were added merely for consistency.
