# TYPE

**TYPE = a unified type system for describing data, requests, work, cognition, actions, agents, entities, events, relations, and outputs.**

TYPE is not limited to programming-language types. It provides a common vocabulary for describing what something is, what it contains, what it can do, how it relates to other things, and how it changes.

## Core model

```text
Type
├── Identity      what it is
├── Structure     what it contains
├── Constraint    what is allowed
├── Relation      what it relates to
├── Operation     what it can do
└── Transition    how it changes
```

## Type families

```text
TYPE
├── Data          variables, values, documents
├── Request       requests, questions, commands, instructions
├── Work          research, build, fix, design, review
├── Cognition     observe, identify, compare, infer, decide
├── Action        executable operations
├── Agent         execution subjects
├── Entity        person, organization, place, product, concept
├── Event         create, update, delete, publish, merge, deploy
├── Relation      contains, depends_on, references, causes
└── Output        answer, report, dataset, code, document, decision
```

## Request → Work → Cognition → Action → Output

A central purpose of TYPE is to describe the lifecycle of a request using the same type language.

```text
Request
  ↓
Work
  ↓
Cognition
  ↓
Action
  ↓
Output
```

For example:

```text
ResearchRequest
  ↓
ResearchWork
  ↓
Observe → Identify → Classify → Compare → Infer
  ↓
ResearchAction
  ↓
ResearchOutput
```

## Type and Instance

TYPE definitions are distinct from their concrete instances.

```text
Type
 ↓
Instance
 ↓
State
 ↓
Event
 ↓
New State
```

Example:

```text
Type:   ResearchRequest
Instance: "Investigate this subject"
```

## Type and Workflow

A workflow can be represented as a graph of typed transformations and state transitions.

```text
ResearchRequest
      ↓
ResearchWork
      ↓
Observe
      ↓
Collect
      ↓
Classify
      ↓
Analyze
      ↓
ResearchAction
      ↓
ResearchOutput
```

Therefore:

> **Workflow = a graph of type transformations and transitions.**

## Type and Action

Action is the executable operation in the TYPE model.

```text
Action Type
    ↓
Action Instance
    ↓
Execution
    ↓
Effect / Output
```

> **Action = what is done.**

See [action.md](action.md).

## Type and Agent

Agent is the execution subject that observes context, reasons, decides, and executes work through Actions.

```text
Request
   ↓
Agent
   ├── Observe
   ├── Reason
   ├── Decide
   └── Execute
          ↓
       Action
          ↓
       Effect
          ↓
       Output / State
```

```yaml
type: Agent

input:
  - Request
  - Context

cognition:
  - Observe
  - Reason
  - Decide

work:
  - WorkType

actions:
  - ActionType

output:
  - OutputType
```

> **Agent = who / what executes.**

See [agent.md](agent.md).

## Agent × Action × Work

```text
WorkType
    ↓
Task
    ↓
Agent
    ↓ executes
Action
    ↓
Effect
    ↓
Output / State
```

The distinctions are intentional:

```text
WorkType = what work is being defined
Task     = a concrete work instance
Agent    = who / what executes
Action   = what operation is executed
Workflow = how actions are sequenced
```

## Common schema

A TYPE definition may use this minimal structure:

```yaml
type:
name:
description:

input:
  -

output:
  -

constraints:
  -

relations:
  -

operations:
  -

transitions:
  -
```

The schema is intentionally extensible. Domain-specific types may be added without changing the core model.

## Relation to bonsai concepts

TYPE provides the vocabulary in which other bonsai concepts can be described.

```text
TYPE
 │
 ├── intent     → Request / Intent Type
 ├── goal       → Goal Type
 ├── epic       → WorkGroup Type
 ├── issue      → WorkItem Type
 ├── aw         → Action / Workflow Type
 ├── workflow   → Transition Type
 ├── research   → ResearchWork Type
 ├── agent      → Agent Type
 └── output     → Output Type
```

These mappings are conceptual rather than implementations. Each project may define its own concrete schema while remaining compatible with TYPE.

## Principles

### 1. Type is not Instance

A type defines a class of things; an instance is a concrete occurrence.

### 2. Type is not Workflow

A type describes what something is and can do. A workflow describes how typed things transform or transition.

### 3. Agent is not Action

```text
Agent  = execution subject
Action = executable operation
```

An Agent executes Actions; an Action does not become an Agent merely because it is executable.

### 4. Types are composable

```text
Request + Cognition + Work + Agent + Action + Output = a typed workflow
```

### 5. Types are extensible

```text
Core Type
  ↓
Domain Type
  ↓
Project Type
  ↓
Instance
```

### 6. Every important concept should answer

```text
What type is this?
```

## One-line definition

> **TYPE is the canonical vocabulary for describing data, requests, work, cognition, actions, agents, entities, events, relations, and outputs as one composable type system.**
