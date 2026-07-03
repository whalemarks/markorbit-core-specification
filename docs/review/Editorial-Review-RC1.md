# Editorial Review RC1

> Repository editorial review for the MarkOrbit Core Specification after Architecture Design completion.

Version: RC1

Status: Review

Scope:

- Repository structure
- Markdown consistency
- Numbering consistency
- Heading hierarchy
- Cross references
- Depends / Related references
- Naming consistency
- Professional Vocabulary consistency
- README quality
- GitHub readability
- Release readiness

Constraints:

- This review is editorial only.
- This review does not redesign architecture.
- This review does not introduce new architecture concepts.
- This review does not rewrite specifications.

References:

- CONSTITUTION.md
- 001_Professional_Vocabulary.md
- 002_Naming_Convention.md
- 003_Document_Style.md

---

# Executive Summary

The repository is coherent and close to release-ready as an architectural specification set. The high-level architecture is stable, the major domains are present, and the repository communicates the Professional Operating System concept clearly.

The main release blockers are editorial rather than architectural:

- Several Depends and Related references use legacy or shortened filenames that do not exist in the repository.
- The specification set uses two filename-reference styles: canonical full filenames and shortened filenames without `_Specification`.
- Some specification documents do not fully follow the standard section structure defined in `003_Document_Style.md`.
- Directory names under `specification/` use numeric prefixes and underscores, while the naming standard says directories should use PascalCase.
- Professional Vocabulary is mostly consistent, but forbidden or avoided terms appear in explanatory content and some specification examples.

No architecture redesign is recommended. The repository should enter release cleanup with targeted editorial fixes only.

Release Readiness Score: 82 / 100

---

# Repository Structure Review

## Strengths

The repository has a readable top-level structure:

```text
/
├── CONSTITUTION.md
├── 001_Professional_Vocabulary.md
├── 002_Naming_Convention.md
├── 003_Document_Style.md
├── 099_Architecture_Manifesto.md
├── README.md
├── CHANGELOG.md
├── theory/
└── specification/
```

The `specification/` tree is organized by numbered architectural domains:

| Directory | File Count | Review |
|---|---:|---|
| `100_Engineering_Kernel/` | 10 | Complete kernel sequence from 100 to 190. |
| `200_Core_Foundation/` | 6 | Complete foundation sequence from 200 to 250. |
| `300_Persistence/` | 6 | Complete persistence sequence from 300 to 350. |
| `400_Brain/` | 5 | Complete Brain sequence from 400 to 440. |
| `500_Intelligence/` | 5 | Complete Intelligence sequence from 500 to 540. |
| `600_Capability/` | 5 | Complete Capability sequence from 600 to 640. |
| `700_Guide/` | 5 | Complete Guide sequence from 700 to 740. |
| `800_Workflow/` | 5 | Complete Workflow sequence from 800 to 840. |
| `900_Workspace/` | 5 | Complete Workspace sequence from 900 to 940. |

The `theory/` directory provides a coherent conceptual sequence from `00_Vision.md` through `12_Workspace.md`.

## Editorial Issues

### Directory naming mismatch

`002_Naming_Convention.md` says directory names should use PascalCase. The repository uses numbered directory names with underscores under `specification/`, such as:

- `100_Engineering_Kernel/`
- `200_Core_Foundation/`
- `300_Persistence/`
- `900_Workspace/`

This is not necessarily incorrect if the repository intentionally treats specification directories as ordered sections, but it should be explicitly documented as an allowed repository-level exception.

### Missing review directory before RC1

The requested report path requires `docs/review/`. The repository did not previously expose a review/reporting area. Creating `docs/review/Editorial-Review-RC1.md` is appropriate and does not affect architecture.

---

# File Naming Review

## Strengths

All reviewed Markdown filenames follow a consistent numeric prefix and title format.

Examples:

- `001_Professional_Vocabulary.md`
- `099_Architecture_Manifesto.md`
- `410_Brain_Object_Specification.md`
- `620_Execution_Model_Specification.md`
- `940_Workspace_Product_Specification.md`

The specification filenames consistently use three-digit prefixes and Pascal_Case word separation.

## Editorial Issues

### Short references do not match actual filenames

Many Depends and Related entries use shortened filenames, such as:

- `410_Brain_Object_Specification.md`
- `420_Knowledge_Model_Specification.md`
- `430_Knowledge_Graph_Specification.md`
- `440_Knowledge_Product_Specification.md`

The actual files include `_Specification`, such as:

- `410_Brain_Object_Specification.md`
- `420_Knowledge_Model_Specification.md`
- `430_Knowledge_Graph_Specification.md`
- `440_Knowledge_Product_Specification.md`

This is the most common cross-reference inconsistency and should be resolved before release.

### Legacy filenames appear in dependency blocks

Several dependency entries refer to files that do not exist in the current repository structure:

- `200_Entity_Definition_Specification.md`
- `300_Persistence_Specification.md`
- `250_Business_Object_Specification.md`
- `150_Event_Specification.md`
- `1000_Platform_Specification.md`
- `theory/02_Architecture.md`
- `theory/04_Ontology.md`

These references appear to be legacy names or planned files. They should be corrected to current canonical filenames or explicitly listed as missing/future documents.

---

# Markdown Style Review

## Strengths

The repository is readable in GitHub Markdown. Most documents use:

- clear top-level titles;
- short paragraphs;
- unordered lists;
- simple tables;
- plain text diagrams;
- consistent Summary sections.

This aligns well with `003_Document_Style.md`.

## Heading hierarchy

Most files use `#` for major sections and `##` for subsections. This is visually consistent, but there are some editorial concerns:

- Metadata sections such as `Version`, `Status`, `Depends`, and `Related` sometimes appear as plain labels and sometimes as `##` headings.
- Some documents begin with `# Title` followed immediately by `## Version`, while others use plain `Version` text.
- The style guide examples show plain labels for `Version`, `Status`, `Depends`, and `Related`, while some 900-series specifications use heading-form metadata.

Recommended editorial action: select one metadata style and apply it consistently.

## Standard section structure coverage

The required and recommended section model is mostly present, but not uniformly applied.

Observed gaps include:

| Section | Files Missing Section |
|---|---:|
| Purpose | 0 |
| Philosophy | 0 |
| Scope | 2 |
| Responsibilities | 2 |
| Architecture | 19 |
| Characteristics | 12 |
| Categories | 9 |
| Validation | 3 |
| Runtime | 8 |
| Compatibility | 0 |
| Extension | 0 |
| Non Goals | 0 |
| Examples | 8 |
| Design Principles | 2 |
| Summary | 0 |

Most missing sections are in older Engineering Kernel and base layer overview documents. This is an editorial consistency issue, not an architectural defect.

## Numbering consistency

The numeric sequencing is strong:

- `001` to `003` define governance standards.
- `099` provides the manifesto.
- `100` through `190` define the Engineering Kernel.
- `200` through `940` define architectural domains.
- `00` through `12` define theory documents.

No duplicate numeric prefixes were observed in the reviewed Markdown set.

---

# Cross Reference Review

## Markdown link validation

No broken inline Markdown links were found in standard `[text](path)` form during this review.

## Depends / Related validation

Depends and Related validation found significant filename mismatches.

The most frequent unresolved references were:

| Unresolved Reference | Count |
|---|---:|
| `300_Persistence_Specification.md` | 14 |
| `200_Entity_Definition_Specification.md` | 12 |
| `440_Knowledge_Product_Specification.md` | 8 |
| `740_Guide_Product_Specification.md` | 8 |
| `640_Capability_Product_Specification.md` | 8 |
| `540_Intelligence_Product_Specification.md` | 8 |
| `430_Knowledge_Graph_Specification.md` | 6 |
| `730_Experience_Network_Specification.md` | 6 |
| `630_Capability_Network_Specification.md` | 6 |
| `250_Business_Object_Specification.md` | 6 |
| `530_Decision_Graph_Specification.md` | 6 |
| `620_Execution_Model_Specification.md` | 5 |

The pattern is clear: dependency references often omit `_Specification`, while actual filenames include it.

## Missing architecture references

Two references point to a `docs/` path that is not present in the repository:

- `theory/02_Architecture.md`
- `theory/04_Ontology.md`

Equivalent theory documents appear to exist:

- `theory/02_Architecture.md`
- `theory/04_Ontology.md`

Recommended editorial action: update references to canonical repository paths if these are intended to point to the theory documents.

---

# Vocabulary Review

## Strengths

The repository strongly reinforces canonical vocabulary:

- Professional Operating System
- Workspace
- Concept
- Judgment
- Action
- Responsibility
- Interaction
- Operating Context
- Product
- Knowledge Model
- Reasoning Model
- Execution Model
- Orchestration Model
- Organization Model

The major layer names and product names are broadly consistent with the Constitution and Professional Vocabulary.

## Editorial Issues

### Avoided terms appear in content

The following avoided or forbidden vocabulary appears in the repository. Some occurrences are acceptable because they appear inside vocabulary standards as examples of terms to avoid. Others should be reviewed in specifications and theory documents.

| Term | Observed Count | Review |
|---|---:|---|
| `Output` | 87 | High frequency. Some are acceptable in contract input/output contexts, but Product should be preferred for published architectural results. |
| `Package` | 45 | Review whether Product is intended. |
| `Company` | 22 | Replace with Workspace, Operating Context, or organization-specific external context where possible. |
| `Task` | 20 | Replace with Action or Responsibility where architectural. |
| `Tenant` | 16 | Mostly appears in governance documents as an avoided term; validate remaining usage. |
| `Conversation` | 13 | Replace with Interaction where architectural. |
| `Chat` | 9 | Replace with Interaction or Assistant Experience where architectural. |
| `Artifact` | 7 | Replace with Product where architectural. |
| `Organization Chart` | 7 | Replace with Organization Model where architectural. |
| `Wizard` | 3 | Replace with Interaction. |
| `Workflow Task` | 3 | Replace with Responsibility. |
| `DTO` | 2 | Acceptable only as avoided vocabulary example. |
| `Decision Result` | 2 | Acceptable only as avoided vocabulary example. |

Recommended editorial action: exclude the standards documents from vocabulary violation counts, then review remaining occurrences in theory and specification files.

### Entity terminology tension

The Professional Vocabulary defines Concept as the Brain canonical Object and lists Entity as a term to avoid for Concept. The repository also contains a Core Foundation entity model. This appears intentional, because `200_Core_Foundation` uses Entity for factual professional foundation concepts rather than Brain Concepts.

Recommended editorial action: add a short editorial note in the naming/vocabulary standards or relevant foundation specification clarifying that Entity is permitted only for the Core Foundation entity domain and must not be used as a synonym for Brain Concept.

---

# Missing Files

The following referenced files were not found as exact filenames or paths:

## Likely renamed files

- `200_Entity_Definition_Specification.md`
- `300_Persistence_Specification.md`
- `410_Brain_Object_Specification.md`
- `420_Knowledge_Model_Specification.md`
- `430_Knowledge_Graph_Specification.md`
- `440_Knowledge_Product_Specification.md`
- `510_Intelligence_Object_Specification.md`
- `520_Reasoning_Model_Specification.md`
- `530_Decision_Graph_Specification.md`
- `540_Intelligence_Product_Specification.md`
- `610_Capability_Object_Specification.md`
- `620_Execution_Model_Specification.md`
- `630_Capability_Network_Specification.md`
- `640_Capability_Product_Specification.md`
- `710_Guide_Object_Specification.md`
- `720_Interaction_Model_Specification.md`
- `730_Experience_Network_Specification.md`
- `740_Guide_Product_Specification.md`

## Likely legacy or renamed foundation files

- `150_Event_Specification.md`
- `250_Business_Object_Specification.md`

Possible current equivalents:

- `150_Event_Specification.md`
- `250_Business_Object_Specification.md`

## Possibly planned files

- `1000_Platform_Specification.md`

If Platform is outside Core Specification RC1 scope, it should be referenced as future or external rather than as an unresolved local dependency.

## Incorrect path references

- `theory/02_Architecture.md`
- `theory/04_Ontology.md`

Possible current equivalents:

- `theory/02_Architecture.md`
- `theory/04_Ontology.md`

---

# Suggested Fixes

## Fix Depends / Related references

Update Depends and Related entries to exact canonical filenames.

Examples:

```text
410_Brain_Object_Specification.md
```

should become:

```text
410_Brain_Object_Specification.md
```

Use the same rule across Brain, Intelligence, Capability, Guide, Workflow, and Workspace specifications.

## Normalize metadata format

Choose one metadata style for all specifications:

```text
Version

2.0

Status

Active

Depends

...

Related

...
```

or:

```markdown
## Version

2.0
```

The style guide currently implies plain labels. If heading-form metadata is preferred, update the style guide first in a future editorial pass.

## Normalize standard sections

For release consistency, add missing standard sections where absent, especially:

- Architecture
- Characteristics
- Categories
- Runtime
- Examples

Do not rewrite content. Add brief editorial sections only where the missing section is required for consistency.

## Clarify directory naming exception

Either:

- rename directories to PascalCase, or
- document that numbered repository directories are an allowed exception for ordered specification navigation.

The second option is lower risk for RC1 because it avoids moving files and changing many links.

## Vocabulary cleanup

Review avoided vocabulary outside the standards documents. Prioritize high-impact architectural documents and specifications first.

Recommended replacements:

| Avoid | Prefer |
|---|---|
| Tenant | Workspace |
| Company | Operating Context or Workspace |
| Task | Action or Responsibility |
| Conversation | Interaction |
| Chat | Interaction |
| Output | Product |
| Artifact | Product |
| Package | Product |
| Organization Chart | Organization Model |
| Workflow Task | Responsibility |

## README improvements

The README is strong and readable. Suggested refinements:

- Add a short “Release Status” block near the top.
- Add explicit links to `CONSTITUTION.md`, `001_Professional_Vocabulary.md`, `002_Naming_Convention.md`, and `003_Document_Style.md`.
- Add a small “How to validate references” section once validation scripts or editorial rules are formalized.
- Clarify whether Platform is in or out of Core Specification RC1 scope.

---

# Priority List: P0 / P1 / P2

## P0 — Release blockers

- Correct unresolved Depends and Related references to exact existing filenames.
- Resolve references to missing or legacy files:
  - `200_Entity_Definition_Specification.md`
  - `300_Persistence_Specification.md`
  - `250_Business_Object_Specification.md`
  - `150_Event_Specification.md`
  - `1000_Platform_Specification.md`
  - `theory/02_Architecture.md`
  - `theory/04_Ontology.md`
- Decide whether Platform references are external/future or missing from RC1.

## P1 — Release quality improvements

- Normalize metadata formatting across all specification files.
- Add missing standard sections in specifications where required by `003_Document_Style.md`.
- Review vocabulary violations outside the governance standards.
- Clarify the Entity / Concept vocabulary boundary.

## P2 — Post-RC editorial polish

- Document the numbered directory naming exception.
- Add a repository validation checklist to README.
- Add automated editorial checks for Depends / Related references.
- Add a future review index under `docs/review/` if editorial reports continue.

---

# Release Readiness Score

Score: 82 / 100

## Scoring rationale

| Category | Score | Notes |
|---|---:|---|
| Repository structure | 8 / 10 | Clear and navigable; directory naming exception needs clarification. |
| File naming | 8 / 10 | Strong file naming; internal references often use shortened names. |
| Markdown consistency | 7 / 10 | Readable; metadata and section structures need normalization. |
| Numbering consistency | 9 / 10 | Strong sequence and no duplicate prefixes observed. |
| Heading hierarchy | 7 / 10 | Generally readable; metadata heading style is inconsistent. |
| Cross references | 6 / 10 | Inline Markdown links pass, but Depends / Related references need cleanup. |
| Vocabulary consistency | 7 / 10 | Strong canonical vocabulary; avoided terms require targeted review. |
| README quality | 8 / 10 | Strong overview; release status and validation guidance would improve readiness. |
| GitHub readability | 9 / 10 | Clear Markdown, lists, diagrams, and navigation. |
| Release readiness | 8 / 10 | Ready for RC cleanup, not yet final release. |

## Final assessment

The repository is architecturally coherent and editorially mature. The main remaining work is reference normalization, metadata consistency, and vocabulary cleanup. After P0 fixes are complete, the repository should be suitable for RC1 publication. After P1 fixes, it should be suitable for final release review.
