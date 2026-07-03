# 160 Runtime Model

> **The Runtime Execution Model of MarkOrbit**

---

Version

**2.0**

Status

**Draft**

Depends

- 100_Specification_Guide.md
- 110_Registry_Framework.md
- 120_Identity_Specification.md
- 130_Relationship_Specification.md
- 140_Timeline_Specification.md
- 150_Event_Specification.md

Related

- 170_Contract_Model.md
- 200_Entity_Specification.md
- 600_Capability_Specification.md
- 700_Guide_Specification.md
- 800_Workflow_Specification.md
- 900_Workspace_Specification.md

---

# Purpose

The Registry defines permanent objects.

Reality changes continuously.

Someone must execute those definitions.

The purpose of the Runtime Model is to define how permanent Core definitions become executable runtime instances.

Runtime answers one question.

> **How does MarkOrbit operate?**

---

# Runtime Philosophy

Registry defines.

Runtime executes.

Registry is static.

Runtime is dynamic.

Definitions are permanent.

Instances are temporary.

History is permanent.

Execution is transient.

---

# Runtime Architecture

MarkOrbit consists of two worlds.

```
Definition World

↓

Runtime World
```

The Definition World describes what exists.

The Runtime World performs work.

Neither replaces the other.

---

# Definition World

The Definition World contains permanent Core objects.

Examples include:

- Ontology
- Entity Definition
- Data Product Definition
- Brain Object
- Intelligence Object
- Capability
- Workflow Definition
- Workspace Definition

Definition objects evolve slowly.

They are managed by Registry.

---

# Runtime World

The Runtime World contains executable instances.

Examples include:

- Entity Instance
- Capability Execution
- Workflow Instance
- Guide Session
- Workspace Session
- Runtime Context

Runtime objects exist only while work is being performed.

---

# Runtime Pipeline

Every execution follows the same lifecycle.

```
Definition

↓

Runtime Instance

↓

Execution

↓

Event

↓

Timeline

↓

Current State
```

Definitions never execute directly.

Runtime executes on behalf of Definitions.

---

# Runtime Instance

A Runtime Instance is a temporary execution object.

Examples include:

```
Capability

↓

Capability Instance
```

```
Workflow

↓

Workflow Instance
```

```
Guide

↓

Guide Session
```

Runtime Instances are temporary.

Definitions remain permanent.

---

# Runtime Identity

Every Runtime Instance owns a Runtime ID.

Example

```
CAPRUN-20260703-000028

WFRUN-20260703-000015

GUIDE-SESSION-000342
```

Runtime IDs never replace Definition IDs.

Definition remains the permanent reference.

---

# Runtime Context

Every Runtime Instance executes within a Context.

Context may include:

- current user
- current workspace
- current entity
- current language
- current permissions
- runtime variables
- temporary decisions

Context exists only during execution.

Context is not part of Registry.

---

# Runtime State

Runtime owns execution state.

Examples include:

```
Created

↓

Running

↓

Waiting

↓

Paused

↓

Completed

↓

Failed

↓

Cancelled
```

Definition never owns Runtime State.

---

# Runtime Ownership

Different runtime objects own different responsibilities.

| Runtime Object | Responsibility |
|----------------|----------------|
| Guide Session | Interaction |
| Workflow Instance | Business Execution |
| Capability Instance | Professional Execution |
| Runtime Context | Temporary Memory |
| Event | Change |
| Timeline | History |

Responsibilities must remain independent.

---

# Runtime Isolation

Every Runtime Instance is isolated.

Execution in one Workspace must not affect another.

Execution in one Workflow must not modify another unrelated Workflow.

Isolation enables reliability.

---

# Runtime Composition

Complex execution is composed from smaller runtime instances.

Example

```
Workflow Instance

↓

Capability Instance

↓

Capability Instance

↓

Capability Instance
```

Each Capability executes independently.

Workflow coordinates execution.

---

# Runtime and Registry

Registry manages definitions.

Runtime consumes definitions.

Runtime never modifies Registry.

Registry remains authoritative.

---

# Runtime and Identity

Runtime references permanent Identity.

Example

```
CAP-000201

↓

CAPRUN-20260703-000051
```

The Runtime Instance references the Definition.

It never replaces it.

---

# Runtime and Relationship

Runtime may create or modify Relationships.

Relationship changes are represented through Events.

Runtime never edits Relationship history directly.

---

# Runtime and Event

Every meaningful runtime action produces Events.

Example

```
Workflow Started

↓

Capability Executed

↓

Approval Granted

↓

Workflow Completed
```

Events become permanent history.

---

# Runtime and Timeline

Runtime never writes Timeline directly.

Runtime produces Events.

Timeline consumes Events.

Timeline reconstructs Current State.

---

# Runtime and Current State

Runtime may read Current State.

Runtime should never modify Current State directly.

Current State changes only through:

```
Runtime

↓

Event

↓

Timeline

↓

Replay

↓

Current State
```

---

# Runtime and Guide

Guide owns Runtime Context.

Guide Runtime ends when interaction ends.

Guide Sessions are temporary.

Knowledge remains permanent.

---

# Runtime and Capability

Capability Definitions are permanent.

Capability Executions are temporary.

Execution metrics belong to Runtime.

Capability definitions remain unchanged.

---

# Runtime and Workflow

Workflow Definitions belong to Registry.

Workflow Instances belong to Runtime.

Workflow execution produces Events.

Workflow history belongs to Timeline.

---

# Runtime and Workspace

Workspace Definitions belong to Core.

Workspace Runtime represents active organizational operation.

Workspace Runtime should never redefine Workspace Definition.

---

# Runtime Failure

Runtime failures are expected.

Examples include:

- validation failure
- timeout
- dependency unavailable
- permission denied
- external service failure

Runtime should recover whenever possible.

History should always remain consistent.

---

# Runtime Recovery

Runtime should support:

- retry
- resume
- restart
- manual continuation

Recovery should continue from Runtime State whenever possible.

Replay should remain deterministic.

---

# Runtime Metrics

Runtime may produce metrics.

Examples include:

- execution duration
- success rate
- retry count
- latency
- approval time

Metrics support optimization.

Metrics do not change history.

---

# Runtime Validation

Runtime must validate:

- Definition exists
- Identity is valid
- Context is complete
- Permissions are satisfied
- Dependencies are available

Execution should fail early when prerequisites are not met.

---

# Runtime Compatibility

Definitions evolve independently.

Runtime should execute against compatible Definition versions.

Version compatibility rules are defined by Contract Model.

---

# Extension

Future Runtime extensions may include:

- distributed execution
- parallel execution
- event streaming
- workflow orchestration engines
- AI runtime optimization
- edge execution

Extensions must preserve Runtime principles.

---

# Non Goals

Runtime is not:

- Registry
- Database
- Event Store
- Timeline
- Current State
- Capability Definition
- Workflow Definition

Runtime executes.

It does not define.

---

# Examples

Capability Execution

```
Definition

CAP-000021

↓

Runtime

CAPRUN-20260703-000021

↓

Event

Capability Executed
```

Workflow Execution

```
Definition

WF-000032

↓

Runtime

WFRUN-20260703-000008

↓

Events

Started

↓

Approved

↓

Completed
```

Guide Session

```
Guide Definition

↓

Guide Session

↓

Context

↓

Capability Selection

↓

Workflow Started
```

---

# Design Principles

Definition before Runtime.

Registry before Execution.

Runtime before Event.

Event before Timeline.

Timeline before Current State.

Temporary before Permanent.

Execution before Optimization.

Isolation before Performance.

---

# Summary

Runtime is the execution engine of MarkOrbit.

Definitions describe what exists.

Runtime executes those definitions.

Execution produces Events.

Events construct Timelines.

Timelines reconstruct Current State.

Registry defines the Operating System.

Runtime brings it to life.